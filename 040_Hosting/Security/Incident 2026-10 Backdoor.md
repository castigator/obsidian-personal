---
tags:
  - hosting
  - security
---

# Incident 2026-10 Backdoor

The second compromise of pebmarsh.com in 2026, after [[Incident 2026-07 Malware]]. Back to [[Hosting]].

## What happened

- **27 Oct 2026, 06:55 UTC:** a "New User Registration" email arrived for `svcykfk1bjr6` (@example.invalid). Rupert deleted the user.
- **Cause:** two fake plugins on [[Site - pebmarsh.com]], both active:
  - `query6guard`, disguised as "PixelForge" and installed 18 Oct. It could log a visitor in as the first admin and create a hidden admin `webteam644` that didn't show in the Users list.
  - `site-guard-c89e`, installed 19 Oct. It logged a visitor in as the first admin.
- **Used from:**
  - 74.82.105.156 on 20 Oct.
  - 43.250.53.42 on 25 Oct, and on 26 Oct at 23:55 PDT, when it created the new user. Rupert confirmed this address isn't his.
- **Entry point: unknown.** The plugins were installed before the oldest access log (DreamHost keeps about 7 days).
  - Candidates: a stolen login, a vulnerable plugin, or the hosting panel or SFTP.
  - Note that [[DreamHost]] reported a security incident of its own on 25 Oct 2026, affecting its file manager and webmail, and expired some users' passwords.

## Fixed (27 Oct 2026)

- **pebmarsh.com:** Rupert deleted both plugins and changed his password. The leftover settings were removed, every login session was cleared, and the security keys (salts) were replaced. No hidden admin was left.
- **All 4 live WordPress sites:** sessions cleared and salts replaced. On [[Site - Parish Council]], which had no salts at all, salts were added and the dormant `admin` account deleted.
- **Not found:** no core file tampering, no PHP files in uploads, no injected content.

## Found 30 Oct 2026: SEO-spam cloaking on pebmarsh.com, missed since June

Found while archiving the old WordPress site, after pebmarsh.com had moved to a static site.

- `wp-content/themes/kelly/functions.php` (the active theme) had code labelled "Implement the LightSpeed cache". For any request whose user agent or referrer contained "gle" (Googlebot, and visitors arriving from Google), it posted the visitor's IP, user agent, referrer and URL to `http://buffer.secureplace4allimages.com/server_permanent2.php`. If the reply contained spam links it added them before `</body>`; if it was a whole page or a 404, it replaced the page.
- `engine/wp-ajax.php` in the site root: a standalone copy that posts to `.../server_new.php` and echoes whatever comes back.
- Both files are dated 17 Jun 2026 (the `engine/` folder 17 Jul, the July clean-up). So it was planted during the June–July compromise ([[Incident 2026-07 Malware]]) and survived that clean-up and the October audit. `wp core verify-checksums` can't see theme changes, and the audit doesn't look at theme files.
- Ordinary visitors saw the normal site, so nobody noticed. Google may have indexed spam under pebmarsh.com.
- It stopped when pebmarsh.com moved to the Cloudflare Worker on 30 Oct 2026. The old URLs now return 404, so any spam pages will drop out of Google.
- Searched every PHP file under `~/www`: no copies on Parish Council, Courtyard Stores or FoPC. PCP (`/home/pebmarsh_pcp`, separate user) could not be searched from the `rupert` login.
- Evidence: kept in the Drive archive `www-pebmarsh-wp.pebmarsh.com.tar.gz` (md5 645960e37ca0c70078bcf6deb8b90a8a).
- Follow-ups: search PCP for `secureplace4allimages` / "LightSpeed cache"; add a theme-file check for these markers to `wp-audit.sh`; look in Google Search Console for pebmarsh.com spam pages or a security warning.

## Still open

- Ask DreamHost for the 15–20 Oct access logs, and whether its own incident is related.
- Two-factor login on the WordPress sites.
- Blocking plugin installs from wp-admin (`DISALLOW_FILE_MODS`): Rupert decided to skip this unless it happens again.
- Weekly audits: see [[Security Audit]].
- Possible lead on the entry point (found 30 Oct 2026): pebmarsh.com had an empty `wp-content/uploads/wp-file-manager-pro/fm_backup/` folder, dated 17 Jul 2026 (its `index.html` 20 Jun 2026). The WP File Manager plugin itself is not installed. File-manager plugins are a common way in, and DreamHost's own 25 Oct notice mentioned a file manager. pebmarsh.com no longer runs WordPress (see [[Site - pebmarsh.com]]).

The full report is in the project: `reports/findings-2026-10-27.md`.
