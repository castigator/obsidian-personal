---
tags:
  - hosting
  - site
---

# Site - Parish Council

Pebmarsh Parish Council's website. **To hand off to the council.** Back to [[Hosting]].

- **URL:** https://parishcouncil.pebmarsh.com. About 1,550 visits a month.
- **Type:** WordPress 7.1.3 on [[DreamHost]], folder `~/www/pebmarsh/parishcouncil.pebmarsh.com`. Dates from 2007.
- **Database:** `pbdb_parish` on `mysql.pebmarsh.com`.
- **Plugins:** Akismet, Classic Editor. `wp-flv` and `exploit-scanner` were no longer there when checked on 28 Oct 2026.
- **Themes:** twentyfifteen, twentytwentyfive, plus old unused themes (Qwilm! blue, kino, darknight2.0, newzen, nolimits) waiting to be removed.
- **Users:**
  - rupert.
  - PPotter, the parish clerk: edits pages, from IP 145.224.67.126.
  - The old `admin` account (2007) was deleted on 27 Oct 2026.
- **Email:** `clerk@` forwards to pebmarshparishclerk@gmail.com; `info@` forwards to `clerk@` (fixed 28 Oct 2026). See [[Hosting Email]].
- **Security:** the config file had **no security keys** (salts) until 27 Oct 2026, when they were added. Sessions were cleared the same day.

## Handoff

- The council should own its hosting and, ideally, its own domain (a parish council domain), with a redirect from the old subdomain for a while.
- It's the busiest of the organisation sites, so agree a date with the clerk.
- The clerk's email address and the forwards need to move with it.
