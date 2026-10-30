---
tags:
  - hosting
  - site
---

# Site - Pebmarsh Community Pub

Pebmarsh Community Pub Limited, a community benefit society. **To hand off to the society.** Back to [[Hosting]].

- **URL:** https://pcp.pebmarsh.com. About 1,200 visits a month.
- **Type:** WordPress on [[DreamHost]], under a **separate SFTP user, `pebmarsh_pcp`**. Rupert's own login can't see its files.
- **Database:** `pcpwp` on `mysql.pcp.pebmarsh.com`.
- **Admins:** Kate Stubbs and Maud-May Cuthbert (both had passwords force-reset in July 2026).
- **Email:** `admin@` and `rupert@` forward to rupert@pebmarsh.com; `chair@` forwards to Peter Hele (peter.hele57@gmail.com). See [[Hosting Email]].
- **Not the King's Head's own site.** The pub's booking email problem was on its own domain, kingsheadpebmarsh.co.uk.
- **Handoff:** the society should own its hosting and domain. Keep `ftp.pcp` and `ssh.pcp` in DNS until then, because its SFTP user may rely on them.
