---
tags:
  - hosting
  - site
---

# Site - Honeycode

Rupert's HoneyBooks app site. Back to [[Hosting]].

- **URL:** https://honeycode.pebmarsh.com. About 75 visits a month, plus the HoneyBooks app itself (sign-in, update checks).
- **Status:** served by [[Cloudflare]] since **29 Oct 2026**. All 52 files were byte-identical to [[DreamHost]] at the switch, and Rupert tested Google sign-in on Android, web and macOS afterwards. **Fully off DreamHost the same day:** the domain was deleted in the DreamHost panel and the folder removed after archiving. There's no fallback host; everything served rebuilds from the two repos.
- **Source:** GitLab group `honeycode`, cloned on the Mac at `~/workspace/gitlab/honeycode/`. The move's progress is also recorded in HoneyBooks' `STATUS.md` ("Hosting move"), so HoneyBooks sessions see it.

## What serves what

| URL | Source | On Cloudflare |
|---|---|---|
| `/`, `/privacy/`, `/changelog/`, `/oauth/android-callback/`, `/version.json`, `/.well-known/assetlinks.json` | `honeycode-site` (Astro) | Worker `honeycode` (custom domain) |
| `/downloads/HoneyBooks-latest.apk`, `.dmg` | HoneyBooks release builds | R2 bucket `honeycode-downloads`, served by the `honeycode` Worker |
| `/app/` (the PWA) | `honeybooks/apps/web` | Worker `honeybooks-app`, route `honeycode.pebmarsh.com/app*` |

The app depends on four URLs that must never change: the OAuth callback page, `assetlinks.json` (Android App Links), `version.json` (update checks) and the two downloads. `assetlinks.json` names the APK signing certificate (SHA-256 `ED:74:F4…F4:54`); the keystore is in 1Password, "HoneyBooks Android signing key".

Only the two `-latest` downloads moved to R2. The older versioned builds (1.0.0–1.6.0) are in the DreamHost folder's archive, `www-pebmarsh-honeycode.pebmarsh.com.tar.gz` in [[Hosting Archive]] (85 files, checksums verified). APKs can't be rebuilt exactly from a commit, because the Android project folder isn't in git.

## Releases and DNS

- HoneyBooks' `/release` deploys everything to Cloudflare with `npx wrangler` (logged in as Rupert@pebmarsh.com): the site Worker, the app Worker and the two R2 downloads. The DreamHost rsync paths were removed on 29 Oct 2026.
- DNS: `honeycode` is a Cloudflare-managed Worker record (like `ernis`), with its own certificate. `www.honeycode` was deleted on 29 Oct 2026.

## How the move was done (29 Oct 2026)

1. Built and compared each part on `workers.dev`, then both Workers together on a throwaway `honeycode-test.pebmarsh.com`.
2. Switched by proxying the existing `honeycode` A record (orange cloud) with Worker routes in place: one click, with one-click rollback.
3. Once Android, web and macOS sign-in were confirmed, converted it to a Worker custom domain. Cloudflare's API won't replace an existing record, so the A record was deleted and the domain attached by a script that retried every 2 seconds.
4. Release scripts made Cloudflare-only; folder archived; domain and folder removed from DreamHost.

Lessons: a route Worker runs before a custom-domain Worker on the same host; `/app/*` misses `/app` and an exact `/app` route misses `/app?…`, so use `/app*`; `wrangler deploy` doesn't remove custom domains or routes dropped from the config (removed through the API).

## Notes

- `/app/invoices`-style deep links 404'd on DreamHost (its `app/.htaccess` was missing, possibly lost in the July 2026 clean-up). Cloudflare serves them correctly.
- The splash and About logo load from the site root rather than `/app/`; fixed on HoneyBooks branch `fix-app-logo-path`, for the next release.
