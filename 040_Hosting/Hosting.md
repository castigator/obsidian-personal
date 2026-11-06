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
- **Hosting:** [[DreamHost]] Shared Unlimited on **monthly** billing since 28 Oct 2026, to be cancelled around 10 Nov. Nothing live is left there (6 Nov): FoPC, the Parish Council and PCP are all on WordPress.com and archived to Drive. Only the unused FoPC copy and the `pebmarsh_pcp` user remain. No mail is left on DreamHost (4 Nov 2026).
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

- **Email** ([[Hosting Email]]): move done 4 Nov 2026. Last step: tighten DMARC to `p=quarantine` after about a week of clean reports (around 11 Nov). Parish Council site emails now pass DKIM/DMARC via WordPress.com (6 Nov); pcp and parishcouncil SPF trimmed to Forward Email only.
- **FoPC (6 Nov):** on WordPress.com at **fopc.co.uk** (Belynda's account, Personal); migrated and archived to Drive. friendsofpebmarshchurch.uk redirects to it via a Cloudflare Redirect Rule (Belynda chose fopc.co.uk). Waiting for Belynda to change Rupert from Contributor to Administrator; then set the admin email to her and take rupert@ off the form notifications. The DreamHost copy is unused and can go with the account. See [[Site - Friends of Pebmarsh Church]].
- **PCP (5 Nov):** Kate emailed: if the committee is likely to want WordPress, she creates the pub's WordPress.com account and Personal site now and adds Rupert as admin; he migrates it from the DreamHost copy before 10 Nov. Otherwise the static site stays and the Drive archive covers a later rebuild. Rupert is not paying for a speculative WordPress.com site.
- **PCP (earlier):** static on Cloudflare since 4 Nov. Kate wants to use the site more and may want WordPress; PCP committee decides Mon 9 Nov (if yes: WordPress.com Personal, migrated from the DreamHost copy). Once decided, delete the WordPress copy on DreamHost and the `mysql.pcp`/`ftp.pcp`/`ssh.pcp` records, and trim the pcp SPF.
- **Parish Council:** on WordPress.com since 5 Nov (Rupert's account, Personal monthly). Old copy archived and its folder deleted (5 Nov); delete the `pbdb_parish` database in the panel. Shelley emailed 5 Nov: the council must send a WordPress.com account email by **Fri 27 Nov**; Rupert then transfers the site before the plan renews on **4 Dec**, and won't renew it himself. Rupert keeps the `parishcouncil` DNS records. See [[Site - Parish Council]].
- Security follow-ups (parked 2 Nov): search PCP for the cloaking malware, add theme checks to `wp-audit.sh`, check Google Search Console. See [[Incident 2026-10 Backdoor]].
- Parish Council: remove 5 unused themes (awaiting yes).
- [[Mailchimp]]: Courtyard Stores welcome emails keep failing.
