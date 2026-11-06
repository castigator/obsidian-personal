---
tags:
  - hosting
  - site
---

# Site - Friends of Pebmarsh Church

**On WordPress.com at fopc.co.uk since 6 Nov 2026** (Belynda's account). The old address redirects there. Back to [[Hosting]].

- **URL:** https://fopc.co.uk since 6 Nov 2026 (was https://friendsofpebmarshchurch.uk). About 580 visits a month. It has its own domain, registered at uk-cheapest until April 2027. See [[Hosting Domains]].
- **DNS:** on [[Cloudflare]] since 29 Oct 2026 (records `@`, `www`, `mysql`, all DNS only). There's no email on this domain. When the site moves host, point `@` and `www` at the new host.
- **Type:** WordPress 7.1.4 (PHP 8.2) on DreamHost, folder `~/www/pebmarsh/friendsofpebmarshchurch.uk`. Size 403 MB: 136 MB of it is old UpdraftPlus backup sets in `wp-content/updraft` (don't copy them; about 270 MB without), plugins 124 MB, uploads 21 MB.
- **Database:** `friendsofpebmarshchurch_` on `mysql.friendsofpebmarshchurch.uk`, 5 MB. `siteurl`/`home` are `https://www.friendsofpebmarshchurch.uk`.
- **Login:** one user, `rupert` (administrator), email rupertthomas@gmail.com. Log in with the **username**, not the email. Rupert reset his password on 4 Nov 2026.
- **Plugins:**
  - Image Regenerate & Select Crop
  - UpdraftPlus (emails a daily backup)
  - WP Google Maps
  - WP Super Cache
  - WPForms Lite

  4 plugin updates are pending.
- **Themes:** bravada, twentytwentyfive.
- **Handoff:** the easiest of the four, because it already has its own domain. Transfer the domain to the Friends as well, or at least give them access to it.
- **Plan (decided 4 Nov 2026):**
  1. Move the site to uk-cheapest **Micro** hosting (£4.95 + VAT a month: 1 site, 1 GB, 1 DB, Plesk with WordPress Toolkit), in the account that holds the domain.
  2. Move the domain's DNS from Rupert's Cloudflare back to uk-cheapest, so nothing depends on Rupert.
  3. Later, move to Krystal's free charity hosting (a trustee applies with charity no. 1184947 and photo ID; the site must carry a Krystal link). See [[Hosting Migration Plan]].
  - Make the export on the day, not in advance; UpdraftPlus made a full backup on 4 Nov as a safety net. After the move, stop UpdraftPlus keeping copies on the server (1 GB limit).
- **People:** the uk-cheapest account and the domain are **John Flack's** (john@ealp.co.uk); Rupert has the login. Rupert emailed him the plan on 4 Nov 2026. John replied that he left FoPC about 18 months ago, and said he had copied in **Perry and Jonathan**, who are still involved. At 11:34 Rupert replied to John, Perry Crimmins (perrycrimmins@hotmail.com) and Jonathan Nott (jonathannott44@hotmail.com): do they still want the site, and will they take over the domain (it expires 8 Apr 2027)? At 12:25 John forwarded the thread to **Denzil Fellows** (denzil.fellows@gmail.com), copying Rupert. Jonathan had told John he's no longer involved and that **Denzil and Belinda** now run FoPC, so Denzil is to contact Rupert. The account and domain need to pass to whoever runs it now.
- **3 Nov 2026:** admin email and Rupert's user email changed to rupertthomas@gmail.com (was rupert@pebmarsh.com), ahead of removing the DreamHost mailbox.

- **5 Nov 2026: plan changed.** Belynda Fellows (belyndarozalyn@me.com), the new chair, wants to keep and update the site. Rupert replied the same day: she creates an FoPC WordPress.com account and Personal monthly site and adds rupert@pebmarsh.com as admin; Rupert migrates the site there (full migration, as for the Parish Council) and connects friendsofpebmarshchurch.uk (DNS on Rupert's Cloudflare); later she applies for Krystal's free charity hosting (krystal.io/hosting/charity) and moves it from WordPress.com. The uk-cheapest Micro step is dropped. The domain is still in John Flack's uk-cheapest account and needs moving into FoPC's name.
- **Email (5 Nov 2026):** team@friendsofpebmarshchurch.uk (an old DreamHost forwarding list, dead for some time) re-created with **Cloudflare Email Routing** on Rupert's Cloudflare, forwarding to Belynda (belyndarozalyn@me.com). Records added by Cloudflare: MX route1/2/3.mx.cloudflare.net, SPF `v=spf1 include:_spf.mx.cloudflare.net ~all`, DKIM `cf2024-1._domainkey`. Catch-all left disabled. Belynda verified her address and Rupert created the `team` routing rule the same day. uk-cheapest's free forwarding only works on its own nameservers (ns.ukc.uk), so move it there when the nameservers go back.
- **6 Nov 2026: moved to WordPress.com.**
  - Belynda created the WordPress.com account (login team@friendsofpebmarshchurch.uk) and site `chocolate-lady-bread` on the Personal plan, invited Rupert as admin, and claimed **fopc.co.uk** as the plan's domain (on WordPress.com nameservers, in her account).
  - Archived first: `www-pebmarsh-friendsofpebmarshchurch.uk.tar.gz` in Drive "Hosting Archives" (89 MB, 12,937 entries, md5 ce40d59b08fe27067b67583d3fceeed5): site folder without `wp-content/updraft`, plus dump `fopc-db-2026-11-06.sql`. See [[Hosting Archive]].
  - `wpcom-migration` 6.78 installed on DreamHost by wp-cli (Rupert's SSH key works for `rupert`; no password needed). Rupert ran the full migration. Checked: 7 pages, 6 posts, 28 media, all pages 200, WPForms (Subscriber, Volunteer) and WP Google Maps working.
  - **Lockout:** the migration replaced the site's users with the old ones (`rupert`, email rupertthomas@gmail.com), so Rupert's WordPress.com account no longer matched any user and the site's login forces WordPress.com sign-in. Belynda re-invited him, but as **Contributor** (local username `admin`, rupert@pebmarsh.com); Rupert asked her to make him Administrator.
  - **Address:** Belynda chose to keep fopc.co.uk ("move away from John Flack"). friendsofpebmarshchurch.uk now redirects: `@`/`www` Proxied, Redirect Rule "To fopc.co.uk" (`https://*friendsofpebmarshchurch.uk/*` to `https://fopc.co.uk/${2}`, 301, query kept), Always Use HTTPS on. Tested: every path lands on the same page, without touching DreamHost. The redirect ends when the domain lapses (8 Apr 2027, John's account).
  - **To do once Administrator:** admin email to Belynda (still rupertthomas@gmail.com); remove rupert@pebmarsh.com from both WPForms notifications (they go to team@ and rupert@).
  - **DreamHost copy:** no longer reached by anyone; delete it, the `friendsofpebmarshchurch_` database and the `mysql` record when DreamHost is closed.
