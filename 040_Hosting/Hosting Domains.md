---
tags:
  - hosting
---

# Hosting Domains

None of the domains is registered at DreamHost, so leaving DreamHost involves no domain transfers. Back to [[Hosting]].

| Domain | Registrar | Expires | DNS | Email | Notes |
|---|---|---|---|---|---|
| pebmarsh.com | [[Joker]] (customer 22916) | 9 Feb 2030 | [[Cloudflare]] (since 28 Oct 2026) | [[DreamHost]], inbound via MailChannels | Rupert's primary domain. Registrant address updated to 19 Westgate Street on 28 Oct 2026. |
| friendsofpebmarshchurch.uk | uk-cheapest.co.uk (UKC Labs, tag MICROLITE) | 8 Apr 2027 | [[Cloudflare]] (since 29 Oct 2026) | none | [[Site - Friends of Pebmarsh Church]] |
| thecodecollective.com | GoDaddy | 8 Oct 2027 | GoDaddy (parked) | none | Old business; nothing on DreamHost |
| coditecture.com | Hostinger | lapsed Aug 2026 | none | none | Letting it go |
| melbury.org | Joker | deleted Nov 2025 | — | — | Gone |

## pebmarsh.com subdomains in use

- **Websites:**
  - www
  - parishcouncil
  - courtyardstores
  - pcp
  - honeycode (Cloudflare Worker, since 29 Oct 2026; www.honeycode deleted)
  - ernis (Cloudflare Worker, since 29 Oct 2026)
  - glanceboard
- **Mail:** MX records on the apex, parishcouncil, courtyardstores and pcp. See [[Hosting Email]].
- **DreamHost service names:** mysql, mysql.courtyardstores, mysql.pcp (WordPress database hosts), ftp, ssh, mail, mailboxes, webmail and autoconfig.
- **Mailchimp signing records:** k2/k3._domainkey. See [[Mailchimp]].
