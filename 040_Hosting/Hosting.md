---
tags:
  - hosting
icon: 🌐
---

## Hosting

Everything about the pebmarsh.com domains, websites, email and the providers behind them. The aim is to leave DreamHost: DNS on Cloudflare, static sites on Cloudflare Pages, email on a cheap provider, and the organisations' WordPress sites handed to their owners. See [[Hosting Migration Plan]].

Claude works on this from `~/workspace/gitlab/private/pebmarsh` (with `/refresh` and `/close`). These notes are the primary record.

### Where Things Stand (4 Nov 2026)

- **DNS:** pebmarsh.com and friendsofpebmarshchurch.uk are on [[Cloudflare]]. No DNS is left on [[DreamHost]].
- **Hosting:** [[DreamHost]] Shared Unlimited on **monthly** billing since 28 Oct 2026. Left there: [[Site - Friends of Pebmarsh Church]] (WordPress), plus the old copies of the Parish Council and PCP sites (no longer reachable; kept until Kate confirms). FoPC is to move to uk-cheapest first. No mail is left on DreamHost (4 Nov 2026).
- **Static sites on Cloudflare Workers:** [[Site - pebmarsh.com]] (30 Oct), [[Site - Ernis]] and [[Site - Honeycode]] (29 Oct), [[Site - Courtyard Stores]] (2 Nov), [[Site - Pebmarsh Community Pub]] (4 Nov). Old WordPress for pebmarsh.com and Courtyard Stores archived to Drive and removed.
- **Email:** all on Forward Email ($3/month), forward-only with Gmail "Send mail as"; DreamHost mail and its DNS leftovers removed 4 Nov 2026. See [[Hosting Email]].
- **Security:** [[Incident 2026-10 Backdoor]] contained; SEO-spam cloaking malware found in the old pebmarsh.com theme on 30 Oct (follow-ups parked).
- **Old files:** everything archived to Google Drive; `~/data`, `~/archive`, `~/Backups` deleted 2 Nov. See [[Hosting Archive]].
- **GitLab:** group `pebmarsh`, one private repo per site (`ernis`, `pebmarsh-com`, `courtyardstores`, `pcp`) plus `pebmarsh/pebmarsh` for the ops folder.

### Map

| Area | Notes |
|---|---|
| Plan | [[Hosting Migration Plan]] |
| Domains and registrars | [[Hosting Domains]], [[Joker]] |
| DNS | [[Cloudflare]] |
| Hosting | [[DreamHost]] |
| Email | [[Hosting Email]], [[Mailchimp]] |
| Sites | [[Site - pebmarsh.com]], [[Site - Parish Council]], [[Site - Courtyard Stores]], [[Site - Friends of Pebmarsh Church]], [[Site - Pebmarsh Community Pub]], [[Site - Honeycode]], [[Site - Ernis]], [[Site - Glanceboard]] |
| Security | [[Incident 2026-10 Backdoor]], [[Incident 2026-07 Malware]], [[Security Audit]] |
| Old files | [[Hosting Archive]] |
| Email trail | [[Hosting Correspondence Log]] |

### Open Items

- **Email** ([[Hosting Email]]): move done 4 Nov 2026. Last step: tighten DMARC to `p=quarantine` after about a week of clean reports (around 11 Nov).
- **FoPC (in progress, 4 Nov):** move it to uk-cheapest Micro (£4.95 + VAT a month), then move its DNS back to uk-cheapest, then later to Krystal's free charity hosting. Waiting to hear from **Denzil Fellows** (with Belinda, now running FoPC); John Flack, who owns the uk-cheapest account, has passed the thread to him. Need to confirm they still want the site and will take over the domain (expires 8 Apr 2027). See [[Site - Friends of Pebmarsh Church]].
- **PCP:** static on Cloudflare since 4 Nov. Kate told on 4 Nov; once she's happy, delete the WordPress copy on DreamHost and the `mysql.pcp`/`ftp.pcp`/`ssh.pcp` records, and trim the pcp SPF.
- **Parish Council:** on WordPress.com since 5 Nov (Rupert's account, Personal monthly). Next: invite Shelley, tell her, archive and delete the DreamHost copy, transfer the site to a council account. See [[Site - Parish Council]].
- Security follow-ups (parked 2 Nov): search PCP for the cloaking malware, add theme checks to `wp-audit.sh`, check Google Search Console. See [[Incident 2026-10 Backdoor]].
- Parish Council: remove 5 unused themes (awaiting yes). FoPC: 4 plugin updates.
- [[Mailchimp]]: Courtyard Stores welcome emails keep failing.
