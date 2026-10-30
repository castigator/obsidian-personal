---
tags:
  - hosting
---

# Hosting Correspondence Log

**Last checked:** 2026-10-28

Newest first. One line per email that matters; routine noise (backup succeeded, marketing) is not logged. Kept up to date by `/refresh`. Back to [[Hosting]].

| Date | From | What | Action |
|---|---|---|---|
| 2026-10-28 | Joker.com | Change of registrant for pebmarsh.com: address updated to 19 Westgate Street, Long Melford. Done by Rupert; classed as a non-material change. | None |
| 2026-10-28 | Joker.com | modify-domain: nameservers switched to Cloudflare (order 33961546) | None |
| 2026-10-28 | Cloudflare | pebmarsh.com active (Free plan); email verified | None |
| 2026-10-28 | DreamHost Billing | New Shared Unlimited **monthly** plan added (Rupert switched from annual) | None |
| 2026-10-25 | DreamHost | **Security incident** (file manager and webmail): passwords expired for some email and SFTP users; owner must set new ones and review forwards | **Open:** set passwords, tell users, check forwards |
| 2026-10-24 | DreamHost | Upcoming price change to Shared Unlimited; renewal notice | Superseded by the switch to monthly |
| 2026-10-23 | DreamHost | Database server `iad1-mysql-e2-17b` upgrade (Ubuntu 26.04, MySQL 8.4) on **30 Oct, 7–8am PT (2–3pm UK)**; sites offline for about 15 min. `mysql.pebmarsh.com` is on this server. | **Open:** after the upgrade, run `dns/verify-zone.sh` and check the sites |
| 2026-10-15 → 25 | Mailchimp | Repeated "Someone subscribed to Courtyard Stores but they did not receive a welcome email" | **Open:** check the Courtyard Stores audience's welcome automation |
| 2026-10-27 | WordPress (pebmarsh.com) | New User Registration `svcykfk1bjr6`: the backdoor incident trigger | Handled (see `reports/`) |
