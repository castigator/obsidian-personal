---
tags:
  - hosting
  - security
---

# Security Audit

A read-only check of the whole [[DreamHost]] account, built after the [[Incident 2026-10 Backdoor]]. Back to [[Hosting]].

- **Script:** `wp-audit.sh` in the project (`~/workspace/gitlab/private/pebmarsh`). It runs over SSH, takes about 4 minutes and changes nothing.
- **What it checks:**
  - the account's scheduled jobs, SSH keys and recently changed files;
  - for each WordPress site:
    - core and plugin file checksums;
    - users, read straight from the database, because a backdoor can hide them from wp-admin;
    - login sessions, settings and scheduled hooks;
    - injected content;
  - malware signatures, auto-login code, PHP in uploads and `.htaccess` files;
  - access logs: backdoor-style query keys, successful logins, new users and plugin uploads.
- **When:** `/refresh` runs it if the last report is more than 7 days old. Reports are saved as `reports/audit-YYYY-MM-DD.txt` in the project. They stay out of this vault because they can contain backdoor keys.
- **Known IP addresses:**
  - Rupert's home: 92.24.171.21.
  - The parish clerk: 145.224.67.126.
  - 78.147.225.80, from the July clean-up sessions, is probably Rupert's but not confirmed.
- **Signs to act on:**
  - New WordPress users, especially admins.
  - A "New User Registration" or "Admin Email Change" email.
  - Unknown plugins.
  - Failed core checksums.
