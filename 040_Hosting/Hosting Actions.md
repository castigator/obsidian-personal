---
type: Claude Actions
project: pebmarsh
claude_project: /Users/rupert.thomas/workspace/gitlab/private/pebmarsh
claude_sessions:
  - "[[2026-11-09 finance dfd038ee]]"
  - "[[2026-11-10 pebmarsh 0c6dfdff]]"
---
## Hosting Actions

Open action points for the pebmarsh (hosting) project. This note is the only list: the project's CLAUDE.md points here, and each session loads it at start. Tick items off here; `/close` ticks off what a session did, adds new items, and clears ticked items older than a couple of weeks. All items carry `#claude-action` so they show on [[Claude Actions]] and stay out of the daily note. The narrative state stays in [[Hosting]] ("Where Things Stand" and "Open Items").

### Actions

- [x] Parish Council: council WordPress.com account created by Shelley: pebmarshparishclerk@gmail.com (council agreed 11 Nov). #claude-action ⏫ ✅ 2026-11-11
- [x] Parish Council: replied to Shelley: the account is enough, skip the domain step, watch for the transfer email. #claude-action ⏫ ✅ 2026-11-12
- [ ] Parish Council: transfer the site to the council before the plan renews on 4 Dec (Rupert won't renew). #claude-action ⏫ 📅 2026-12-04
- [ ] Mailchimp Courtyard Stores: confirm the "Upgrade to restore sending" banner has cleared (about 105 contacts). #claude-action 🔼
- [x] PCP: admin email off admin@pcp.pebmarsh.com (Kate never confirmed; set to rupertthomas@gmail.com instead), WPForms notification From noreply@pebmarshcommunitypub.com / To pcpshareholder@gmail.com, email summaries disabled. #claude-action 🔼 ✅ 2026-11-11
- [x] Tighten `_dmarc` from p=none to p=quarantine (Rupert, Cloudflare). #claude-action ✅ 2026-11-11
- [ ] DMARC: check the Forward Email DMARC dashboard's Quarantined column for genuine mail; revert to p=none if anything real is caught. #claude-action 🔼 📅 2026-11-18
- [ ] DMARC: consider tightening `_dmarc` from p=quarantine to p=reject (Forward Email's recommendation), if the 18 Nov check and the reports since are clean. Leave the subdomains' red DKIM/DMARC crosses in the Forward Email dashboard alone: they have no outbound sending, and the apex record covers them. #claude-action 🔽 📅 2026-12-02
- [ ] PCP: switch the site's admin email from rupertthomas@gmail.com to Kate (she clicks the WordPress confirmation; example screenshot in [[Site - Pebmarsh Community Pub]]). #claude-action 🔽
- [ ] End of December: delete the pcp.pebmarsh.com Forward Email addresses (`chair@`, `admin@`, `rupert@`) and the pcp MX/TXT records. #claude-action 📅 2026-12-31
- [ ] PCP: <chair@pebmarshcommunitypub.com> forwarding awaits verification by <pcpshareholder@gmail.com>; tell Kate if it lapses. #claude-action 🔽
- [ ] Watch for DreamHost's closure confirmation and any further charge. #claude-action 🔽

### Open Questions

- [ ] Was the Mailchimp Courtyard Stores login from Gorleston (92.24.171.21, 9 Nov 09:42) Rupert's? Assumed yes. #claude-action 🔽
