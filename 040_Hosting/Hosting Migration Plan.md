---
tags:
  - hosting
---

# Hosting Migration Plan

Goal: stop paying DreamHost (about $156 a year) for hosting that's mostly unused, and stop running WordPress sites that keep getting hacked. Back to [[Hosting]].

## Target

| Concern | Now | Target | Cost |
|---|---|---|---|
| Domains | [[Joker]] (pebmarsh.com), uk-cheapest (FoPC) | stay where they are | renewals only |
| DNS | [[Cloudflare]] for both (done 28–29 Oct 2026) | [[Cloudflare]] | free |
| Static sites | DreamHost | Cloudflare Pages | free |
| Email | DreamHost (inbound via MailChannels) | to choose: Migadu, [[Joker]] Mailbox, Cloudflare Email Routing for forwards | about $20–50 a year |
| Organisation WordPress sites | DreamHost, paid by Rupert | owners' own hosting, paid by them | £0 to Rupert |
| pebmarsh.com | WordPress on DreamHost | static export on Pages, or WordPress on cheap hosting | to decide |

## Steps

1. **DNS to Cloudflare.**
   - pebmarsh.com: **done 28 Oct 2026** (52 records, all DNS only, verified).
   - friendsofpebmarshchurch.uk: **done 29 Oct 2026** (3 records, nameservers changed at uk-cheapest).
2. **Static sites to Cloudflare:** each site gets its own private repo in the GitLab `pebmarsh` group, and Cloudflare deploys it as a Worker with static assets on every push. **[[Site - Ernis]] done 29 Oct 2026.** Next: [[Site - Honeycode]] (source already in `honeycode/honeycode-site`). [[Site - Glanceboard]] is empty: retire it or put up a placeholder.
3. **Email:** see [[Hosting Email]]. Copy the stored mail out of the 12 mailboxes, recreate the forwards, switch MX/SPF/DKIM in Cloudflare, and keep DreamHost mail running for a week or two as a safety net.
4. **Hand off the organisation sites:**
   - [[Site - Parish Council]], [[Site - Friends of Pebmarsh Church]], [[Site - Courtyard Stores]] and [[Site - Pebmarsh Community Pub]].
   - Each owner buys hosting, such as a UK managed WordPress host or WordPress.com. UpdraftPlus is already on most of the sites, which makes moving them easy.
   - Prefer each organisation having its own domain, with a redirect from the old subdomain for a while. Otherwise Rupert stays their DNS gatekeeper for good.
   - Set a deadline. If an owner stalls, move their site to a cheap temporary host so they don't keep DreamHost alive.
5. **pebmarsh.com:** decide between going static and keeping WordPress.
6. **Cancel DreamHost** once nothing depends on it. Then delete the leftover DNS records (mysql, ftp, ssh, webmail).

## While DreamHost still hosts things

- DreamHost can no longer change DNS itself. If it moves a server, the record has to be updated by hand in [[Cloudflare]]. `/refresh` runs `dns/verify-zone.sh` to catch this.
- Don't edit DNS in the DreamHost panel; changes there no longer take effect.
