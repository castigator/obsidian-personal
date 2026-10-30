---
tags:
  - hosting
---

# Cloudflare

DNS for pebmarsh.com and friendsofpebmarshchurch.uk, and the future home of the static sites (Pages). Back to [[Hosting]].

- **Account:** Rupert@pebmarsh.com (email verified 28 Oct 2026). **Free plan.**
- **pebmarsh.com zone:** active since 28 Oct 2026. Nameservers `agustin.ns.cloudflare.com` and `susan.ns.cloudflare.com`, set at [[Joker]].
- **friendsofpebmarshchurch.uk zone:** active since 29 Oct 2026, with the same nameservers, set at uk-cheapest. 3 records, all DNS only: `@`, `www` and `mysql` (WordPress DB_HOST). `ftp`/`ssh` were dropped. Zone file `dns/friendsofpebmarshchurch.uk.zone`; check it with `dns/verify-zone.sh agustin.ns.cloudflare.com friendsofpebmarshchurch.uk`.
- **DNSSEC:** off for both domains (no DS record at .com or Nominet). It can be switched on in Cloudflare later, with the DS record added at the registrar.

## How the records are set up

- 52 records were imported from the project file `dns/pebmarsh.com.zone` (rebuilt from DreamHost and trimmed). Now 50, plus the `ernis` record that Cloudflare manages for the Ernis Worker (see [[Site - Ernis]]).
- **Every record is "DNS only" (grey cloud); nothing is proxied.** Visitors go straight to [[DreamHost]], as before. Ignore Cloudflare's "Proxy DNS records" and "not fully protected" nags.
  - Proxying would break the `mysql`, `ftp`, `ssh` and `mail` names (the proxy only carries web traffic) and could break WordPress logins.
  - Turn on proxying site by site, only once a site has left DreamHost.
- The zone-file import set 29 records to Proxied by itself; they all had to be switched off by hand.
- TTL "1" in the dashboard means Auto (5 minutes).
- The AI and bot settings (crawl control, Bot Preference Sync) only affect proxied traffic, so they don't matter yet.

## Records that matter most

- **`mysql`, `mysql.courtyardstores`, `mysql.pcp`:** WordPress connects to its database through these. If DreamHost moves the database server (as on the 30 Oct 2026 upgrade of `iad1-mysql-e2-17b`), these must be updated here, or the sites go down.
- **MX, SPF (TXT) and `dreamhost._domainkey`:** mail for pebmarsh.com and the parishcouncil, courtyardstores and pcp subdomains. See [[Hosting Email]].
- **`k2._domainkey`, `k3._domainkey`:** [[Mailchimp]] DKIM. Mailchimp recreated these itself through a one-time authorisation (TTL 1 hour).

## Drift check

DreamHost keeps updating its own (now unused) copy of the zone. `dns/verify-zone.sh agustin.ns.cloudflare.com` in the project compares the two. Any `DIFF` means DreamHost moved something: copy the new value into Cloudflare. `/refresh` runs this.

## Dropped when moving from DreamHost

- `rupert`, `mapletree` and `*.internal`: stale home-broadband and home-network addresses.
- `www.mailboxes.*` and `www.webmail.*`.
- `ftp.`/`ssh.` on courtyardstores, ernis, glanceboard, honeycode and parishcouncil (kept on the apex and pcp).
- Mail-client names on the subdomains.
- ernis's mail records.

## Free plan

DNS, unlimited static sites on Pages, and certificates are all included. Email Routing is free but inbound only (no sending). Pro ($20 a month) adds firewall and image features that aren't needed.
