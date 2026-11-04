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
2. **Static sites to Cloudflare:** each site gets its own private repo in the GitLab `pebmarsh` group, and Cloudflare deploys it as a Worker with static assets on every push. **[[Site - Ernis]] done 29 Oct 2026.** Next: [[Site - Honeycode]] (source already in `honeycode/honeycode-site`). [[Site - Glanceboard]] was empty and was retired 3 Nov 2026.
3. **Email:** see [[Hosting Email]]. Copy the stored mail out of the 12 mailboxes, recreate the forwards, switch MX/SPF/DKIM in Cloudflare, and keep DreamHost mail running for a week or two as a safety net.
4. **Hand off the organisation sites:**
   - [[Site - Parish Council]], [[Site - Friends of Pebmarsh Church]], [[Site - Courtyard Stores]] and [[Site - Pebmarsh Community Pub]].
   - Each owner buys hosting, such as a UK managed WordPress host or WordPress.com. UpdraftPlus is already on most of the sites, which makes moving them easy.
   - Prefer each organisation having its own domain, with a redirect from the old subdomain for a while. Otherwise Rupert stays their DNS gatekeeper for good.
   - Set a deadline. If an owner stalls, move their site to a cheap temporary host so they don't keep DreamHost alive.
   - **Hosting options (researched 4 Nov 2026; prices are list prices, so check at checkout):**
     - Sizes: Parish Council 533 MB files + 7 MB DB (plugins: akismet, classic-editor). FoPC 403 MB + 5 MB DB (updraftplus, wpforms-lite, wp-google-maps, wp-super-cache, image-regenerate-select-crop). PCP not measured (separate SFTP user).
     - **Krystal free charity hosting** (Amethyst: 1 site, 10 GB, daily backups). The applicant must be a trustee or director of a charity registered with the Charity Commission, OSCR or CCNI, with photo ID, and the site needs a link back to Krystal. Fits FoPC (charity 1184947). Other not-for-profits, such as PCP, are considered case by case.
     - **Krystal shared hosting:** Amethyst £7/month (1 site), Ruby £11/month (5 sites); 16% off if paid yearly. Not managed: the owner does the updates.
     - **Krystal Managed WordPress:** Personal £15 + VAT a month (about £151 + VAT a year). Automatic core, plugin and theme updates, malware scanning, Patchstack virtual patching, staging.
     - **WordPress.com:** Personal about $4/month and Premium about $8/month, paid yearly. Fully hosted, with no server to look after. Reports say plugins are allowed on every paid plan since Apr 2026 (unverified).
     - **uk-cheapest.co.uk** (FoPC's registrar): Plesk shared hosting with the WordPress Toolkit. Micro £4.95 + VAT a month (1 site, 1 GB, 1 DB). Basic £9.95 + VAT (3 sites but only 1 DB). Professional £14.95 + VAT (15 sites, 5 DBs). No charity discount and not managed.
     - Hostinger is cheap in year one, but renews at about £8/month.
5. **pebmarsh.com:** decide between going static and keeping WordPress.
6. **Cancel DreamHost** once nothing depends on it. Then delete the leftover DNS records (mysql, ftp, ssh, webmail).

## While DreamHost still hosts things

- DreamHost can no longer change DNS itself. If it moves a server, the record has to be updated by hand in [[Cloudflare]]. `/refresh` runs `dns/verify-zone.sh` to catch this.
- Don't edit DNS in the DreamHost panel; changes there no longer take effect.
