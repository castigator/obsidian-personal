---
tags:
  - hosting
icon: 🌐
claude_project: /Users/rupert.thomas/workspace/gitlab/private/pebmarsh
claude_sessions:
  - "[[2026-11-10 pebmarsh 0c6dfdff]]"
  - "[[2026-11-13 pebmarsh 5d0addd8]]"
  - "[[2026-11-19 pebmarsh adf8362f]]"
---

## Hosting

Everything about the pebmarsh.com domains, websites, email and the providers behind them. The aim is to leave DreamHost: DNS on Cloudflare, static sites on Cloudflare Pages, email on a cheap provider, and the organisations' WordPress sites handed to their owners. See [[Hosting Migration Plan]].

Claude works on this from `~/workspace/gitlab/private/pebmarsh` (with `/refresh` and `/close`). These notes are the primary record.

### Where Things Stand (20 Nov 2026)

- **DNS:** pebmarsh.com and friendsofpebmarshchurch.uk are on [[Cloudflare]]. `dns/verify-zone.sh` now checks Cloudflare against the zone files.
- **Hosting:** **[[DreamHost]] closed 6 Nov 2026.** Static sites on Cloudflare; the three organisations' WordPress sites on WordPress.com: [[Site - Parish Council]] (the council's account since 16 Nov 2026), [[Site - Pebmarsh Community Pub]] (Kate's account, pebmarshcommunitypub.com), [[Site - Friends of Pebmarsh Church]] (Belynda's account, fopc.co.uk; the old address redirects).
- **Static sites on Cloudflare Workers:** [[Site - pebmarsh.com]] (30 Oct), [[Site - Ernis]] and [[Site - Honeycode]] (29 Oct), [[Site - Courtyard Stores]] (2 Nov). Old WordPress for pebmarsh.com and Courtyard Stores archived to Drive and removed.
- **Email:** all on Forward Email ($3/month), forward-only with Gmail "Send mail as"; DreamHost mail and its DNS leftovers removed 4 Nov 2026. See [[Hosting Email]].
- **Security:** [[Incident 2026-10 Backdoor]] contained; the affected sites went with DreamHost. `wp-audit.sh` retired.
- **Mailchimp:** Courtyard Stores is its own Mailchimp account (Free plan). Cleaned of 158 bot sign-ups on 9 Nov 2026; double opt-in and reCAPTCHA on; courtyardstores.pebmarsh.com authenticated. See [[Mailchimp]].
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
- **Email** ([[Hosting Email]]): move done 4 Nov 2026. DMARC tightened to `p=quarantine` on 11 Nov 2026; Early look 16 Nov 2026: every pebmarsh.com report 11–16 Nov (Google, Outlook, Enterprise Outlook, Yahoo) 100% pass, 0 quarantined, 0 rejected; SPF aligned 0% on the Mailchimp rows is expected (Mailchimp's own bounce domain), DKIM aligned 100%. parishcouncil and courtyardstores have no reports (no mail sent from them). Formal check 19 Nov 2026: reports 12–17 Nov all 100% pass, 0 quarantined, 0 rejected; `p=quarantine` stays, and `p=reject` is the next step to consider around 2 Dec. **20 Nov 2026:** the six dead old-ISP forwards deleted at Forward Email (17 pebmarsh.com addresses left); noreply@ stays as Mailchimp's silent-discard From/Reply-To. See [[Hosting Email]]. Parish Council site emails now pass DKIM/DMARC via WordPress.com (6 Nov); pcp and parishcouncil SPF trimmed to Forward Email only.
- **PCP (6 Nov):** on Kate's WordPress.com site, pebmarshcommunitypub.com; pcp.pebmarsh.com retired. End of December: delete the pcp Forward Email addresses (`chair@`, `admin@`, `rupert@`) and the pcp MX/TXT records. Before that, the site's WPForms weekly summary (and possibly its admin email) must stop using admin@pcp.pebmarsh.com (Forward Email flagged it as possible phishing, 9 Nov; Rupert asked Kate to confirm the admin email change the same day; on 9 Nov she couldn't find the confirmation email). **Fixed 11 Nov 2026:** admin email set to rupertthomas@gmail.com, WPForms sends from noreply@pebmarshcommunitypub.com to pcpshareholder@gmail.com, summaries off. Nothing on the site uses a pcp.pebmarsh.com address now. See [[Site - Pebmarsh Community Pub]]. Kate (17 Nov) will take up Rupert's offer of a half-hour walkthrough in the New Year; the admin email switch to her waits until then.
- **FoPC (6 Nov):** on WordPress.com at **fopc.co.uk** (Belynda's account, Personal); migrated and archived to Drive. friendsofpebmarshchurch.uk redirects to it via a Cloudflare Redirect Rule (Belynda chose fopc.co.uk). Rupert is Administrator; forms now notify team@ only; unneeded plugins removed. See [[Site - Friends of Pebmarsh Church]].
- **Parish Council: handed over 16 Nov 2026.** Shelley accepted the WordPress.com transfer (pebmarshparishclerk@gmail.com) and changed the admin email to that address. Plan (Personal, $9/month) is the council's, auto-renew on, renews 4 Dec; Rupert removed his own payment method and stays administrator. Rupert keeps the `parishcouncil` DNS records in Cloudflare. Nothing left to do. See [[Site - Parish Council]].
- [[Mailchimp]]: Courtyard Stores account was paused on 9 Nov (bot sign-ups pushed it past the 250-contact free limit). Fixed the same day: 158 bots archived, double opt-in and reCAPTCHA turned on, domain authenticated. Check that sending is restored.
