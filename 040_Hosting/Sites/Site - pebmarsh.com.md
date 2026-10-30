---
tags:
  - hosting
  - site
---

# Site - pebmarsh.com

Rupert's own village site. Back to [[Hosting]].

- **URL:** https://pebmarsh.com (and www). About 2,500 visits a month.
- **Type:** static site on a [[Cloudflare]] Worker (`pebmarsh-com`, static assets) since 30 Oct 2026, replacing WordPress. No database, no plugins.
- **Source:** GitLab `pebmarsh/pebmarsh-com` (private), cloned on the Mac at `~/workspace/gitlab/private/pebmarsh/sites/pebmarsh-com`.
  - `public/` is what's served; `original/` holds the WordPress export (pages, menu, export file, image) for reference.
  - Cloudflare deploys automatically on every push to `main`. Preview builds are on for other branches.
  - The header and footer are repeated in each of the four pages (home, Mailing List, About, 404); there's no build step.
- **Pages:** home (photo header, mailing-list sign-up, "Around the village" links, OpenStreetMap), Mailing List, About.
  - The mailing list itself is in [[Mailchimp]]; the site links to its sign-up form and its archive of past emails.
  - The live RSS feeds the WordPress home page showed were dropped at Rupert's request. The "Mailing List" feed (via Zapier) had been empty for a long time anyway.
- **Header photo:** "Pebmarsh and church of St John the Baptist" by Bikeboy on Geograph (photo 5890319), CC BY-SA 2.0. The licence requires a credit; it's at the bottom of the About page, because Rupert didn't want it on the home page. Swapping in a photo of Rupert's own would remove the need for it.
- **DNS:** `pebmarsh.com` and `www` are Worker custom domains, managed by Cloudflare. The DreamHost A/AAAA records (173.236.245.51) were deleted on 30 Oct 2026. The apex MX and TXT records are unchanged.

## The old WordPress site

- WordPress 7.1.3, theme kelly, folder `~/www/pebmarsh/wp.pebmarsh.com` on [[DreamHost]], database `wp_pebmarsh_com` on `mysql.pebmarsh.com`. No longer reachable through pebmarsh.com.
- Plugins at the end: BoldGrid Easy SEO, BoldGrid Gallery, RSS Import, UpdraftPlus, WP Google Maps (its only marker was in California), WP Super Cache, WPForms Lite (not used on any page), DreamHost Panel Login.
- Hacked in June–July 2026 ([[Incident 2026-07 Malware]]) and again in October 2026 ([[Incident 2026-10 Backdoor]]).
- **Still to do:** archive the folder and a database dump to Drive, then remove the *website* (not the domain: mail lives there) from DreamHost.
