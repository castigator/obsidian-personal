---
tags:
  - hosting
  - site
---

# Site - Pebmarsh Community Pub

Pebmarsh Community Pub Limited, a community benefit society. **Static on Cloudflare since 4 Nov 2026**, maintained by Rupert. Back to [[Hosting]].

- **URL:** https://pcp.pebmarsh.com. About 1,200 visits a month.
- **Now (4 Nov 2026):** a static site on a [[Cloudflare]] Worker (`pcp`, static assets), replacing WordPress. 9 pages and 5 galleries (with a small photo viewer), at the same addresses as before, so old links work. The look is based on Twenty Seventeen.
  - Source: GitLab `pebmarsh/pcp` (private), cloned at `sites/pcp/`; Cloudflare deploys on every push. `original/mirror/` holds the wget copy of the WordPress site; `tools/build.py` converted it.
  - **DNS:** `pcp` is a Worker custom domain. The DreamHost A records for `pcp` and `www.pcp` (173.236.245.51) were deleted by Rupert on 4 Nov 2026. MX, TXT, `ftp.pcp`, `ssh.pcp` and `mysql.pcp` are unchanged.
  - **Left out:** the WPForms contact form (now an email link to pcpshareholder@gmail.com), Google Analytics, and the unlinked "Gallery Sampler" page.
  - **Archive:** `www-pebmarsh_pcp-pcp.pebmarsh.com.tar.gz` in Drive "Hosting Archives" (858 MB, md5 4bdca796c0515e31649cf260999d2963, 30,239 entries matching the server). It holds the site folder without `wp-content/updraft` (3.1 GB of old UpdraftPlus sets), `pcp.pebmarsh.com.old`, and a dump of `pcpwp` from 4 Nov. See [[Hosting Archive]].
  - **The WordPress copy is still on DreamHost**, in case Kate wants it back, but it can't be reached through pcp.pebmarsh.com any more. Delete it, and the `mysql.pcp`/`ftp.pcp`/`ssh.pcp` records, once she's happy.
- **Was:** WordPress on [[DreamHost]], under a **separate SFTP user, `pebmarsh_pcp`**. Rupert's own login can't see its files.
- **Login:** shell user `pebmarsh_pcp`, password reset by Rupert on 4 Nov 2026 (it's in 1Password; the old one had stopped working, probably expired by DreamHost on 25 Oct).
- **Database:** `pcpwp` on `mysql.pcp.pebmarsh.com`, 7 MB.
- **Content (4 Nov 2026):** WordPress 7.1.4, theme Twenty Seventeen. 10 pages and no posts; the last page edit was 11 Apr 2024 ("About Us"), so it's rarely updated, and mostly by Rupert. 175 NextGEN gallery images in `wp-content/gallery`.
- **Plugins (all active):** NextGEN Gallery, WPForms Lite (1 form), Staff Team, Team Members, MonsterInsights (Google Analytics), WP Mail SMTP, UpdraftPlus, WP Super Cache, DreamHost panel login.
- **Size:** the account uses 5.1 GB, but most of that is backups: `wp-content/updraft` 3.1 GB of old UpdraftPlus sets, plus a `~/pcp.pebmarsh.com.old` folder. The real site is about 0.9 GB: gallery 433 MB, uploads 290 MB, plugins 162 MB, core about 140 MB.
- **Odd files to check (security follow-up):** `wp-login.php.1309912658` and `wp-signup.php.1309912658` in the site root.
- **Admins:** Kate Stubbs (`kate`, stubbskeepers@btinternet.com), Maud-May Cuthbert (`maud-may`, maud-may@cuthbert.uk.net) and Rupert (`rupert`, rupert@pebmarsh.com). Kate and Maud-May had their passwords force-reset in July 2026.
- **Hosting options (4 Nov 2026):** either a static site on Cloudflare (free; Rupert keeps updating it; the contact form becomes an email link or a small form), or WordPress.com Personal (about £40 a year, society's own account). Kate was told on 4 Nov 2026 that it's done, with WordPress on offer if she wants it back; waiting for her reply.
- **Email (Forward Email):** `admin@` and `rupert@` forward to rupertthomas@gmail.com; `chair@` forwards to pcpshareholder@gmail.com (since 3 Nov 2026; it was Peter Hele before). See [[Hosting Email]].
- **Not the King's Head's own site.** The pub's booking email problem was on its own domain, kingsheadpebmarsh.co.uk.
- **Handoff:** the society should own its hosting and domain. Keep `ftp.pcp` and `ssh.pcp` in DNS until then, because its SFTP user may rely on them.
