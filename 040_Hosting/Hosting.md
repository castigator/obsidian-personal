---
tags:
  - hosting
icon: 🌐
---

## Hosting

Everything about the pebmarsh.com domains, websites, email and the providers behind them. The aim is to leave DreamHost: DNS on Cloudflare, static sites on Cloudflare Pages, email on a cheap provider, and the organisations' WordPress sites handed to their owners. See [[Hosting Migration Plan]].

Claude works on this from `~/workspace/gitlab/private/pebmarsh` (with `/refresh` and `/close`). These notes are the primary record.

### Where Things Stand (6 Nov 2026)

- **DNS:** pebmarsh.com and friendsofpebmarshchurch.uk are on [[Cloudflare]]. `dns/verify-zone.sh` now checks Cloudflare against the zone files.
- **Hosting:** **[[DreamHost]] closed 6 Nov 2026.** Static sites on Cloudflare; the three organisations' WordPress sites on WordPress.com: [[Site - Parish Council]] (Rupert's account until the council takes it), [[Site - Pebmarsh Community Pub]] (Kate's account, pebmarshcommunitypub.com), [[Site - Friends of Pebmarsh Church]] (Belynda's account, fopc.co.uk; the old address redirects).
- **Static sites on Cloudflare Workers:** [[Site - pebmarsh.com]] (30 Oct), [[Site - Ernis]] and [[Site - Honeycode]] (29 Oct), [[Site - Courtyard Stores]] (2 Nov). Old WordPress for pebmarsh.com and Courtyard Stores archived to Drive and removed.
- **Email:** all on Forward Email ($3/month), forward-only with Gmail "Send mail as"; DreamHost mail and its DNS leftovers removed 4 Nov 2026. See [[Hosting Email]].
- **Security:** [[Incident 2026-10 Backdoor]] contained; the affected sites went with DreamHost. `wp-audit.sh` retired.
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

- **DreamHost:** closed 6 Nov 2026; watch for the closure confirmation and make sure no further charge appears.
- **Email** ([[Hosting Email]]): move done 4 Nov 2026. Last step: tighten DMARC to `p=quarantine` after about a week of clean reports (around 11 Nov). Parish Council site emails now pass DKIM/DMARC via WordPress.com (6 Nov); pcp and parishcouncil SPF trimmed to Forward Email only.
- **PCP (6 Nov):** on Kate's WordPress.com site, pebmarshcommunitypub.com; pcp.pebmarsh.com retired. End of December: delete the pcp Forward Email addresses (`chair@`, `admin@`, `rupert@`) and the pcp MX/TXT records. See [[Site - Pebmarsh Community Pub]].
- **FoPC (6 Nov):** on WordPress.com at **fopc.co.uk** (Belynda's account, Personal); migrated and archived to Drive. friendsofpebmarshchurch.uk redirects to it via a Cloudflare Redirect Rule (Belynda chose fopc.co.uk). Rupert is Administrator; forms now notify team@ only; unneeded plugins removed. See [[Site - Friends of Pebmarsh Church]].
- **Parish Council:** on WordPress.com since 5 Nov (Rupert's account, Personal monthly). Old copy archived; DreamHost copy gone. Shelley emailed 5 Nov: the council must send a WordPress.com account email by **Fri 27 Nov**; Rupert then transfers the site before the plan renews on **4 Dec**, and won't renew it himself. Rupert keeps the `parishcouncil` DNS records. See [[Site - Parish Council]].
- [[Mailchimp]]: Courtyard Stores welcome emails keep failing.
