---
tags:
  - hosting
  - security
---

# Incident 2026-10 Backdoor

The second compromise of pebmarsh.com in 2026, after [[Incident 2026-07 Malware]]. Back to [[Hosting]].

## What happened

- **27 Oct 2026, 06:55 UTC:** a "New User Registration" email arrived for `svcykfk1bjr6` (@example.invalid). Rupert deleted the user.
- **Cause:** two fake plugins on [[Site - pebmarsh.com]], both active:
  - `query6guard`, disguised as "PixelForge" and installed 18 Oct. It could log a visitor in as the first admin and create a hidden admin `webteam644` that didn't show in the Users list.
  - `site-guard-c89e`, installed 19 Oct. It logged a visitor in as the first admin.
- **Used from:**
  - 74.82.105.156 on 20 Oct.
  - 43.250.53.42 on 25 Oct, and on 26 Oct at 23:55 PDT, when it created the new user. Rupert confirmed this address isn't his.
- **Entry point: unknown.** The plugins were installed before the oldest access log (DreamHost keeps about 7 days).
  - Candidates: a stolen login, a vulnerable plugin, or the hosting panel or SFTP.
  - Note that [[DreamHost]] reported a security incident of its own on 25 Oct 2026, affecting its file manager and webmail, and expired some users' passwords.

## Fixed (27 Oct 2026)

- **pebmarsh.com:** Rupert deleted both plugins and changed his password. The leftover settings were removed, every login session was cleared, and the security keys (salts) were replaced. No hidden admin was left.
- **All 4 live WordPress sites:** sessions cleared and salts replaced. On [[Site - Parish Council]], which had no salts at all, salts were added and the dormant `admin` account deleted.
- **Not found:** no core file tampering, no PHP files in uploads, no injected content.

## Still open

- Ask DreamHost for the 15–20 Oct access logs, and whether its own incident is related.
- Two-factor login on the WordPress sites.
- Blocking plugin installs from wp-admin (`DISALLOW_FILE_MODS`): Rupert decided to skip this unless it happens again.
- Weekly audits: see [[Security Audit]].

The full report is in the project: `reports/findings-2026-10-27.md`.
