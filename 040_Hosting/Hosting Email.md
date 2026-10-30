---
tags:
  - hosting
---

# Hosting Email

Email on pebmarsh.com and its subdomains. It's all on [[DreamHost]] today. This is the critical, must-not-break part of the move. Back to [[Hosting]].

## What's needed

- **Routing, not storage:** most people only need mail forwarded to their own inbox.
- **Sending as @pebmarsh.com:** needed by Rupert and anyone else who replies from their address.
- **Proper SPF, DKIM and DMARC,** which Gmail enforces.

## Inventory (28 Oct 2026, from the DreamHost panel)

### pebmarsh.com (26 addresses)

**Mailboxes (12):** each needs its stored mail copied when moving.

| Address | Forwards to | Used |
|---|---|---|
| castigator@ | — | 0% |
| daisy@ | daisy.jessica.thomas@gmail.com | 5% |
| dylan@ | — | 0% |
| heather@ | heather.heather.thomas@gmail.com (+1) | **85%** |
| jim@ | — | 2% |
| linda@ | — | 1% |
| lucy@ | lucy.rowan.thomas@gmail.com | 3% |
| noreply@ | — | 1% |
| private@ | — | 4% |
| rupert@ | rupertthomas@gmail.com | 6% |
| twitter@ | — | **57%** |
| webmaster@ | — | 0% |

**Forwards (13):**

| Address | Forwards to | Note |
|---|---|---|
| chris.nott@ | chris@jwpnottfarms.fsnet.co.uk | old ISP: check |
| tricia.nott@ | chris@jwpnottfarms.fsnet.co.uk | old ISP: check |
| gary.storrar@ | garystorrar@cvshipping.co.uk | |
| harryness@ | maqj01@dial.pipex.com | old ISP: check |
| heidi@ | heidi@hpage.fslife.co.uk | old ISP: check |
| mailinglist@ | roger@cuthbert.uk.net (+1) | |
| mapletree@ | rupertthomas@gmail.com | |
| norman.brown@ | norm@beechcot.fslife.co.uk | old ISP: check |
| ray.hales@ | ray.hales@btopenworld.com | old ISP: check |
| roger@ | roger@cuthbert.uk.net (+1) | |
| roger.cuthbert@ | roger@cuthbert.uk.net (+1) | |
| swanny@ | swanny@brambles20.fsnet.co.uk | old ISP: check |
| terry@ | terry@the-barnes.freeserve.co.uk | old ISP: check |

**Discarded:** `postmaster@` (DreamHost throws its mail away). It should point at a real inbox at the new provider.

### Subdomains (forwards only)

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

## Follow-ups

- **Forwards to old ISP mailboxes** (Pipex, Freeserve/fsnet, fslife, BT Openworld) have probably closed, so mail to them bounces. Ask each person whether they still want the address, and where it should go.
- **DreamHost's 25 Oct 2026 notice:** some email users' passwords were expired. See [[DreamHost]].

## Provider options

| Option | Cost | Fit |
|---|---|---|
| Cloudflare Email Routing | free | Ideal for the forwards. Inbound only: no sending. |
| Migadu | about $19–48 a year, flat | Unlimited addresses and mailboxes, send-as on all of them. Strong fit. |
| [[Joker]] Mailbox | about $12 a year **per mailbox** | Good for one or two mailboxes with aliases; too expensive for 12. |
| Purelymail | about $10–20 a year | Cheapest; less polished. |
| Google Workspace | $84 a year **per user** | Ruled out (per-user cost). |

Leading idea: forwards on Cloudflare Email Routing, plus Migadu (or a couple of Joker mailboxes) for whoever needs to send or keep mail. Decide which of the 12 mailboxes really need storage; several already forward to Gmail.

## When moving

1. Create the addresses at the new provider.
2. Copy the stored mail (IMAP) for the mailboxes.
3. Switch MX, SPF and DKIM in [[Cloudflare]] (on the apex, parishcouncil, courtyardstores and pcp).
4. Keep DreamHost mail running for a week or two.
5. Tighten DMARC from `p=none` once everything passes.
