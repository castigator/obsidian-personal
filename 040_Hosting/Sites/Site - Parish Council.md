---
tags:
  - hosting
  - site
---

# Site - Parish Council

Pebmarsh Parish Council's website. **On WordPress.com since 5 Nov 2026 (held by Rupert, to transfer to the council).** Back to [[Hosting]].

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
- **3 Nov 2026:** admin email and Rupert's user email changed to rupertthomas@gmail.com (was rupert@pebmarsh.com), ahead of removing the DreamHost mailbox.
- **Clerk (2026):** Shelley Boydell, pebmarshparishclerk@gmail.com. The WordPress login `PPotter` is presumably a previous clerk's.
- **Handoff (4 Nov 2026):** Rupert drafted an email asking the council to set up WordPress.com Personal (council-owned account, with rupert@pebmarsh.com as an administrator), or to choose a parish-council specialist. Rupert will do the move. WordPress.com can serve `parishcouncil.pebmarsh.com` on Personal: in the site's dashboard, Domains → Use a domain name I own, then add the records it shows in Cloudflare and keep the MX records. Install the Classic Editor plugin so editing stays the same. Draft saved in rupertthomas@gmail.com.
- **Moved to WordPress.com (4–5 Nov 2026):**
  - Site `pebmarshparishcouncil1.wordpress.com` (really `pebmarshparishcouncil1.wpcomstaging.com`), Personal plan, monthly (US$9 + VAT; the first month was US$8.10 with coupon DONTGO25), renews 4 Dec 2026, paid by Rupert via PayPal. Account: rupert@pebmarsh.com (Rupert's existing WordPress.com account; an abandoned first checkout created `pebmarshparishcouncil.wordpress.com` under his old rupert.thomas@roxorgaming.com account, unpaid, which can be deleted).
  - Copied with WordPress.com's full migration (the `wpcom-migration` plugin, installed with wp-cli on the old site). IDs are kept, so the 119 posts with `?page_id=` links still work. Checked: 26 pages, 312 posts, 520 media on both; PDFs open; the home page looks identical.
  - DNS (Cloudflare, 5 Nov, by Rupert): `parishcouncil` A 192.0.78.164 and 192.0.78.192, `www.parishcouncil` CNAME to it, all DNS only. MX/TXT unchanged. WordPress.com shows the connection as Active.
  - Old site on DreamHost: untouched apart from the migration plugin, and no edits since 26 Oct 2026. Rupert's `rupert` password was reset on 5 Nov (in 1Password).
  - **Live 5 Nov 2026:** `parishcouncil.pebmarsh.com` set as the primary address; its certificate was issued (5 Nov, until Feb 2027); `www.parishcouncil` and the staging address both redirect to it. Served by WordPress.com (Atomic).
  - **Still to do:** give Shelley a login (invite her through WordPress.com Users, as the old `PPotter` login may not work there); tell her it has moved; transfer the site to a council-owned WordPress.com account (Settings → Danger zone → Transfer); archive the old site to Drive, then delete it and its database from DreamHost.
  - **Don't send** the Gmail draft "Moving the Parish Council website: action needed" (4 Nov): it asks the council to set up hosting, which is now done.
