---
tags:
  - hosting
---

# DreamHost

The current host for the websites, email and databases. Leaving it is the plan: see [[Hosting Migration Plan]]. Back to [[Hosting]].

- **Plan:** Shared Unlimited, about $156 a year. **Switched to monthly billing on 28 Oct 2026** so it can be cancelled as soon as everything has moved. A price rise was announced on 24 Oct 2026.
- **Panel:** panel.dreamhost.com (owner rupert@pebmarsh.com).
- **Server:** `iad1-shared-b8-45.dreamhost.com` (US East). SSH as `rupert`, key-based. The remote shell is zsh.
- **Database server:** `iad1-mysql-e2-17b`, reached as `mysql.pebmarsh.com` (208.113.244.71).
- **SFTP users:**
  - `rupert`: everything except the pub.
  - `pebmarsh_pcp`: [[Site - Pebmarsh Community Pub]].
  - Old leftovers to delete: `dh_cs5sg7` and `dylanalfie` (Dylan), and `dh_cwdey6` (King's Head, 2018).
- **Databases (6):**

  | Database | Site |
  |---|---|
  | `wp_pebmarsh_com` | pebmarsh.com |
  | `pbdb_parish` | parishcouncil |
  | `courtyardstores_pebmarsh` | courtyardstores |
  | `friendsofpebmarshchurch_` | FoPC |
  | `pcpwp` | pcp |
  | `next_pebmarsh_com` | old concrete5 site, archived; **to delete** |

- **Mail:** 26 addresses on pebmarsh.com, plus forwards on 3 subdomains. See [[Hosting Email]]. Inbound mail is filtered through MailChannels.
- **DNS:** no longer used for pebmarsh.com (now [[Cloudflare]]). **Edits in the DreamHost DNS panel no longer take effect.** It no longer runs DNS for friendsofpebmarshchurch.uk either (moved 29 Oct 2026).

## Open with DreamHost

- **25 Oct 2026 security incident (their file manager and webmail):** DreamHost expired the passwords of some email and SFTP users. Set new passwords in Mail → Manage Email and Websites → SFTP Users, tell the people affected (by phone or text, not their DreamHost email), and remove any forward you don't recognise. DreamHost never emails users about password resets, so any such email is phishing.
  - This may relate to the [[Incident 2026-10 Backdoor]]: the plugins appeared 18–19 Oct, and the file-time changes across the whole account on 24 Oct came from DreamHost's side.
- **30 Oct 2026, 7–8am PT (2–3pm UK):** `iad1-mysql-e2-17b` upgrade to Ubuntu 26.04 / MySQL 8.4. Sites go offline for about 15 minutes. Afterwards, check that the `mysql*` addresses haven't changed (see [[Cloudflare]]).
- **Ticket to raise:**
  - Remove `~/stuart.pebmarsh.com` (uid 30070) and `~/archive/mindseye` (uid 15274). Both are owned by old, deleted users, so the account can't remove them.
  - Ask for the 15–20 Oct 2026 access logs, and whether the 25 Oct incident relates to the backdoor.

## Gotchas

- The panel stores a custom record name typed with the full domain as `name.pebmarsh.com.pebmarsh.com` (this broke the Mailchimp DKIM for years).
- DreamHost refuses zone transfers.
- ModSecurity returns HTTP 418 on some WordPress lost-password requests. Reset passwords with wp-cli over SSH instead.
- A hidden `dreamhost-panel-login` plugin sits on every WordPress site (panel single sign-on); its `one_time_login_token` user data is legitimate.
- Access logs are kept for only about 7 days.
