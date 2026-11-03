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
| roger@ | roger@cuthbert.uk.net, rsc@icloud.com | |
| roger.cuthbert@ | roger@cuthbert.uk.net, rsc@icloud.com | |
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

### Decision: Forward Email (2 Nov 2026)

- **Provider:** [Forward Email](https://forwardemail.net), Enhanced Protection plan, $3/month ($18 per 6 months), paid by Rupert on 2 Nov 2026; account signed up with rupertthomas@gmail.com, deliberately not an @pebmarsh.com address. Auto-refund until 2 Dec 2026.
- **Model:** no stored mailboxes. Every address forwards (double forwards supported); senders use Gmail "Send mail as" with `smtp.forwardemail.net`, port 465, SSL, username = the full address, password generated per address in the Forward Email dashboard.
- **Phases:** 1 set up in parallel (DNS records added, aliases recreated); 2 Rupert tests sending; 3 receiving tested on courtyardstores; 4 Heather, Daisy, Lucy switch Gmail; 5 pebmarsh.com MX switched; 6 parishcouncil and pcp; 7 two weeks' overlap; 8 remove DreamHost mail, its SPF/DKIM/autodiscover records, tighten DMARC.
- **Phase 1 DNS, done 2 Nov 2026:** verification TXT, DKIM `fe-1f98178cbf._domainkey`, `fe-bounces` CNAME (DNS only), `include:spf.forwardemail.net` added to the apex SPF, DMARC reports to Forward Email (policy still `p=none`). MX unchanged. Not added: Forward Email's autoconfig/SRV records (no mailboxes) and its suggested `p=reject`.
- **Aliases created 2 Nov 2026 (via the API):** rupert, heather (→ Heather + Rupert), daisy, lucy, dylan, gary.storrar, harryness, ray.hales, mailinglist (→ Roger + rupertthomas@gmail.com directly), mapletree, postmaster (→ Rupert; was discarded); noreply and webmaster disabled with silent drop (code 250). roger@ and roger.cuthbert@ (→ roger@cuthbert.uk.net + rsc@icloud.com). The 6 dead-ISP forwards are listed but disabled with a hard reject (550), so senders get an immediate "no such address" and Forward Email never retries or backscatters. Catch-all `*` deleted (unknown addresses are rejected, as at DreamHost). Not yet: jim@, linda@ (waiting on Rupert's test email).
- **Phase 2 (2 Nov 2026):** rupert@ SMTP password generated (in 1Password); Gmail accepted the login. Outbound SMTP DNS verified 16:49, but the domain is **pending Forward Email admin approval** ("typically less than 24 hours"; they may email rupertthomas@gmail.com with questions). Until approved, Gmail send-as for rupert@ stays on DreamHost.
- **Phase 3 done (2 Nov 2026):** courtyardstores.pebmarsh.com added to Forward Email (facebook@, mailinglist@, team@ → rupertthomas@gmail.com; noreply@ silent drop; catch-all deleted); its MX switched to mx1/mx2.forwardemail.net. Test from an outside p=reject domain arrived in 11 s with SPF, DKIM, DMARC and ARC all passing. The four @courtyardstores addresses in the DreamHost panel are now unused (delete in Phase 8).
- **Phase 6 done early (2 Nov 2026):** parishcouncil (clerk@, info@ → pebmarshparishclerk@gmail.com) and pcp (chair@ → peter.hele57@gmail.com; admin@, rupert@ → rupertthomas@gmail.com) added to Forward Email, catch-alls deleted, MX switched and verified immediately. Their DreamHost addresses are now unused (delete in Phase 8). All three subdomains are off DreamHost mail; only the pebmarsh.com apex remains. Tested 2 Nov: info@parishcouncil (Rupert's Gmail added temporarily, then removed) and admin@pcp both delivered within seconds, all checks passing.
- **Phase 2 done (3 Nov 2026):** outbound SMTP approved by Forward Email 2 Nov 20:36. Rupert's Gmail send-as switched to smtp.forwardemail.net; test to his work address passed SPF, DKIM (d=pebmarsh.com, s=fe-1f98178cbf) and DMARC at the first hop (Mimecast). Microsoft's later "fail" lines are Mimecast rewriting the message (banner, links); ARC passed. Spare password file deleted.
- **API key:** stored in `~/.config/pebmarsh/forwardemail-token` (mode 600) on the Mac; curl reads it via `-K <(printf …)` so it never appears on a command line.
- Don't use Forward Email's "1-Click Setup": it would swap the MX records in one go.

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
