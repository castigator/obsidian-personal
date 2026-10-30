---
tags:
  - hosting
icon: 🌐
---

## Hosting

Everything about the pebmarsh.com domains, websites, email and the providers behind them. The aim is to leave DreamHost: DNS on Cloudflare, static sites on Cloudflare Pages, email on a cheap provider, and the organisations' WordPress sites handed to their owners. See [[Hosting Migration Plan]].

Claude works on this from `~/workspace/gitlab/private/pebmarsh` (with `/refresh` and `/close`). These notes are the primary record.

### Where Things Stand (29 Oct 2026)

- **DNS:** pebmarsh.com moved to [[Cloudflare]] on 28 Oct 2026, and friendsofpebmarshchurch.uk on 29 Oct 2026. No DNS is left on [[DreamHost]].
- **Hosting:** [[DreamHost]] Shared Unlimited, switched to **monthly** billing on 28 Oct 2026, so it can be cancelled once everything has moved.
- **Security:** the [[Incident 2026-10 Backdoor]] is contained. The entry point is unknown.
- **Old files:** archived to Google Drive and mostly deleted from DreamHost; see [[Hosting Archive]].
- **First site off DreamHost:** [[Site - Ernis]], on a Cloudflare Worker deployed from GitLab `pebmarsh/ernis` (29 Oct 2026).
- **GitLab:** a `pebmarsh` group with one private repo per site, plus `pebmarsh/pebmarsh` for this project.

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

- DreamHost's 25 Oct security notice expired some email and SFTP passwords: set new ones, tell the users, check the forwards. See [[DreamHost]].
- 30 Oct 2026, 2–3pm UK: DreamHost database-server upgrade. Afterwards, check DNS for drift and that the sites load. See [[Cloudflare]].
- Verify the last three archives in Drive, then delete `~/data`, `~/archive` and `~/Backups`. See [[Hosting Archive]].
- DreamHost ticket: remove `~/stuart.pebmarsh.com` and `~/archive/mindseye`.
- [[Site - Honeycode]] moved to Cloudflare and fully removed from DreamHost on 29 Oct 2026 (Workers + R2).

- Choose the email provider; follow up the dead-ISP forwards. See [[Hosting Email]].
- Hand off the four organisation sites.
- [[Mailchimp]]: Courtyard Stores welcome emails are failing.
