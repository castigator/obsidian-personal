---
tags:
  - hosting
---

## Hosting Email

Email on pebmarsh.com and its subdomains. It's all on [[DreamHost]] today. This is the critical, must-not-break part of the move. Back to [[Hosting]].

### What's Needed

- **Routing, not storage:** most people only need mail forwarded to their own inbox.
- **Sending as @pebmarsh.com:** needed by Rupert and anyone else who replies from their address.
- **Proper SPF, DKIM and DMARC,** which Gmail enforces.

### Inventory (2 Nov 2026, from the DreamHost panel)

#### pebmarsh.com (23 addresses)

Changes since 28 Oct (made by Rupert): `castigator@`, `private@` and `twitter@` deleted; `dylan@` became a forward to dylan010299@gmail.com; `noreply@` and `webmaster@` now discard their mail.

**Mailboxes (6):** each needs its stored mail copied when moving (or archiving, if nobody reads it there).

| Address | Name | Also forwards to | Used |
|---|---|---|---|
| daisy@ | Daisy | daisy.jessica.thomas@gmail.com | 5% (1.3 GB) |
| heather@ | Heather | heather.heather.thomas@gmail.com, rupertthomas@gmail.com | **86%** (21 GB of 25) |
| jim@ | Jim Holder | — (mailbox only) | 2% (448 MB) |
| linda@ | Linda Holder | — (mailbox only) | 1% (150 MB) |
| lucy@ | Lucy | lucy.rowan.thomas@gmail.com | 3% |
| rupert@ | Rupert - Pebmarsh | rupertthomas@gmail.com | 6% |

**Forwards (14):**

| Address | Forwards to | Note |
|---|---|---|
| chris.nott@ | chris@jwpnottfarms.fsnet.co.uk | undeliverable (fsnet) |
| tricia.nott@ | chris@jwpnottfarms.fsnet.co.uk | undeliverable (fsnet) |
| swanny@ | swanny@brambles20.fsnet.co.uk | undeliverable (fsnet) |
| heidi@ | heidi@hpage.fslife.co.uk | undeliverable (fslife) |
| norman.brown@ | norm@beechcot.fslife.co.uk | undeliverable (fslife) |
| terry@ | terry@the-barnes.freeserve.co.uk | undeliverable (freeserve) |
| dylan@ | dylan010299@gmail.com | was a mailbox until Nov 2026 |
| gary.storrar@ | garystorrar@cvshipping.co.uk | |
| harryness@ | maqj01@dial.pipex.com | |
| ray.hales@ | ray.hales@btopenworld.com | |
| mailinglist@ | roger@cuthbert.uk.net, rupert@pebmarsh.com | |
| roger@ | roger@cuthbert.uk.net (+1) | |
| roger.cuthbert@ | roger@cuthbert.uk.net (+1) | |
| mapletree@ | rupertthomas@gmail.com | |

**Discarded (3):** `noreply@`, `postmaster@` and `webmaster@` throw their mail away. `postmaster@` should point at a real inbox at the new provider.

#### Subdomains (forwards only)

| Address | Forwards to |
|---|---|
| facebook@courtyardstores | rupertthomas@gmail.com |
| mailinglist@courtyardstores | rupertthomas@gmail.com |
| team@courtyardstores | rupertthomas@gmail.com |
| noreply@courtyardstores | discarded |
| clerk@parishcouncil | pebmarshparishclerk@gmail.com |
| info@parishcouncil | clerk@parishcouncil (**fixed 28 Oct 2026**: it pointed at the non-existent joe@) |
| admin@pcp | rupert@pebmarsh.com |
| chair@pcp | peter.hele57@gmail.com |
| rupert@pcp | rupert@pebmarsh.com |

`bollox@ernis` was removed with the ernis domain on 29 Oct 2026. friendsofpebmarshchurch.uk, glanceboard and honeycode have no addresses.

### Follow-ups

- **Checked 2 Nov 2026 (MX lookup):** 6 forwards go to domains whose name servers refuse every query, so no mail server can be found and mail almost certainly can't be delivered. The domains are still registered (with CSC, probably for EE), so this isn't proof the mailboxes are closed; a test email or asking the people would confirm. Affected: chris.nott@ and tricia.nott@ (fsnet), swanny@ (fsnet), heidi@ and norman.brown@ (fslife), terry@ (freeserve). Still deliverable: gary.storrar@ (cvshipping, Microsoft 365), harryness@ (pipex, now TalkTalk), ray.hales@ (btopenworld, BT), and roger@, roger.cuthbert@, mailinglist@ (cuthbert.uk.net, Freeola).

- **Forwards to old ISP mailboxes** (Pipex, Freeserve/fsnet, fslife, BT Openworld) have probably closed, so mail to them bounces. Ask each person whether they still want the address, and where it should go.
- **DreamHost's 25 Oct 2026 notice:** some email users' passwords were expired. See [[DreamHost]].

### Provider Options

| Option                   | Cost                             | Fit                                                                    |
| ------------------------ | -------------------------------- | ---------------------------------------------------------------------- |
| Cloudflare Email Routing | free                             | Ideal for the forwards. Inbound only: no sending.                      |
| Migadu                   | about $19–48 a year, flat        | Unlimited addresses and mailboxes, send-as on all of them. Strong fit. |
| [[Joker]] Mailbox        | about $12 a year **per mailbox** | Good for one or two mailboxes with aliases; too expensive for 12.      |
| Purelymail               | about $10–20 a year              | Cheapest; less polished.                                               |
| Google Workspace         | $84 a year **per user**          | Ruled out (per-user cost).                                             |

Leading idea: forwards on Cloudflare Email Routing, plus Migadu (or a couple of Joker mailboxes) for whoever needs to send or keep mail. Decide which of the 12 mailboxes really need storage; several already forward to Gmail.

- **Cloudflare Email Routing for a subdomain only (tried 2 Nov 2026):** the dashboard's "Onboard Domain" only offers the whole zone, and its first step adds Cloudflare MX (route1/2/3.mx.cloudflare.net), a DKIM key and probably SPF to **pebmarsh.com itself**, which would break the DreamHost mail. Not activated. Subdomains are added from the apex's settings after that. The API may allow subdomain-only, unconfirmed. Decision: subdomain forwards stay on DreamHost until the main email move.

### When Moving

1. Create the addresses at the new provider.
2. Copy the stored mail (IMAP) for the mailboxes.
3. Switch MX, SPF and DKIM in [[Cloudflare]] (on the apex, parishcouncil, courtyardstores and pcp).
4. Keep DreamHost mail running for a week or two.
5. Tighten DMARC from `p=none` once everything passes.
