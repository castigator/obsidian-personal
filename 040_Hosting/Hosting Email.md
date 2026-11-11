---
tags:
  - hosting
claude_project: /Users/rupert.thomas/workspace/gitlab/private/pebmarsh
claude_sessions:
  - "[[2026-11-10 pebmarsh 0c6dfdff]]"
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
| chair@pcp | pcpshareholder@gmail.com (was peter.hele57@gmail.com until 3 Nov 2026) |
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
- **Phase 6 done early (2 Nov 2026):** parishcouncil (clerk@, info@ → pebmarshparishclerk@gmail.com) and pcp (chair@ → pcpshareholder@gmail.com since 3 Nov; admin@, rupert@ → rupertthomas@gmail.com) added to Forward Email, catch-alls deleted, MX switched and verified immediately. Their DreamHost addresses are now unused (delete in Phase 8). All three subdomains are off DreamHost mail; only the pebmarsh.com apex remains. Tested 2 Nov: info@parishcouncil (Rupert's Gmail added temporarily, then removed) and admin@pcp both delivered within seconds, all checks passing.
- **Phase 2 done (3 Nov 2026):** outbound SMTP approved by Forward Email 2 Nov 20:36. Rupert's Gmail send-as switched to smtp.forwardemail.net; test to his work address passed SPF, DKIM (d=pebmarsh.com, s=fe-1f98178cbf) and DMARC at the first hop (Mimecast). Microsoft's later "fail" lines are Mimecast rewriting the message (banner, links); ARC passed. Spare password file deleted.
- **Phase 4 in progress (3 Nov 2026):** SMTP passwords generated for heather@, daisy@, lucy@ and dylan@ (in Rupert's 1Password; Rupert shares them his own way). Guide for them, in Rupert's voice, with two paths (edit an existing send-as entry, or add a new one): PDF `~/Desktop/pebmarsh-email-sending-guide.pdf` and page <https://claude.ai/artifact/2hngJtiY8y21kZEPprgcBe> (private until shared). Heather is believed to use send-as already; Lucy and Dylan don't; Daisy unknown.
- **Phase 5 done (3 Nov 2026):** pebmarsh.com MX switched to mx1/mx2.forwardemail.net by Rupert; verified immediately. jim@ and linda@ added as forwards to rupertthomas@gmail.com (Rupert filters them to a label), so all 23 DreamHost addresses have a Forward Email entry. Tests: mailinglist@ delivered (Rupert + Roger); terry@ refused with "no such address". **All pebmarsh.com mail now runs through Forward Email.** DreamHost mail is the fallback until Phase 8, which is triggered by events, not a date: every sender has switched Gmail (or confirmed they don't send), and a few days of DMARC reports show nothing unexpected sending via DreamHost. parishcouncil and pcp keep DreamHost in their SPF until their WordPress sites move. `mail.pebmarsh.com` still has MailChannels MX records: DreamHost leftovers, remove in Phase 8.
- **DreamHost clean-up started (3 Nov 2026):** Rupert converted lucy@ to forward-only, then deleted all 15 pebmarsh.com forward-only addresses (including lucy@) in the DreamHost panel. Kept until Phase 8: mailboxes rupert@ (the WordPress sites' admin email), heather@, daisy@, jim@, linda@. Kept until their sites move: clerk@/info@parishcouncil, admin@/chair@/rupert@pcp. The 3 garbage addresses and the 4 @courtyardstores addresses were deleted too: DreamHost now shows exactly 10 addresses.
- **3 Nov 2026, before deleting rupert@'s DreamHost mailbox:** admin@pcp and rupert@pcp (DreamHost) repointed to rupertthomas@gmail.com by Rupert; **chair@pcp now goes to pcpshareholder@gmail.com** (Rupert's change, mirrored at Forward Email). Parish Council and FoPC WordPress: admin_email and user `rupert` email changed from rupert@pebmarsh.com to rupertthomas@gmail.com (wp-cli, --skip-email), so nothing on DreamHost depends on the rupert@ mailbox.
- **Tested 3 Nov 2026: DreamHost does NOT deliver internally.** Mail sent from the DreamHost server with sendmail (as WordPress does, From wordpress@parishcouncil.pebmarsh.com) to mapletree@pebmarsh.com and team@courtyardstores.pebmarsh.com, both already deleted at DreamHost, arrived in Rupert's Gmail via Forward Email. So DreamHost follows the public MX and its remaining address entries can be deleted without affecting the WordPress sites. (A first attempt with a forged From: rupertthomas@gmail.com was silently dropped: don't test with a spoofed Gmail sender.)
- **3 Nov 2026, later:** Rupert deleted rupert@ (after the WordPress admin emails moved to Gmail), jim@, linda@, daisy@ (doesn't send) and the 5 parishcouncil/pcp forwards. **Only heather@ remains at DreamHost**, for her sending until she switches Gmail. Mailbox contents of rupert@, daisy@, jim@, linda@ were dropped, not archived (Rupert's decision).
- **Phase 4 done (3 Nov 2026):** Heather switched her Gmail send-as; Forward Email's outbound log shows heather@ sending through it 3 Nov 18:59. Lucy and Dylan don't send; Daisy deleted.
- **Phase 8 done (4 Nov 2026):** Rupert deleted heather@ (the last DreamHost address; its 21 GB mailbox was not archived) in the DreamHost panel. In Cloudflare he deleted the apex `dreamhost._domainkey`, `_autodiscover._tcp` SRV, `autoconfig` CNAME, `mail` A and its 2 MailChannels MX, `mailboxes` and `webmail` A, plus `mysql.courtyardstores` (database gone). Apex and courtyardstores SPF are now `v=spf1 include:spf.forwardemail.net -all`. Forward Email re-verified both; all sites 200. **DreamHost now handles no pebmarsh.com mail.** parishcouncil and pcp SPF still include DreamHost while their WordPress sites send from it.
- **DMARC tightened (11 Nov 2026):** `_dmarc` changed from `p=none` to `p=quarantine` by Rupert in Cloudflare. No `sp=` tag, so it covers parishcouncil, courtyardstores and pcp too. The Forward Email DMARC dashboard (no API for it, and nothing clickable) showed failures only on 5–9 Nov, all matching senders since fixed: the Parish Council site on WordPress.com before its DKIM records (6 Nov), the PCP site's WPForms mail as admin@pcp.pebmarsh.com (fixed 11 Nov), and Courtyard Stores Mailchimp mail before domain authentication (9 Nov). The 11 Nov report was 6/6 pass. Reading the dashboard: "Pass Rate" is messages accepted, not DMARC passes; a message passes if SPF **or** DKIM is aligned. Check the Quarantined column around 18 Nov; reverting is one TXT edit.
- **Forward Email dashboard warnings (checked 11 Nov 2026), leave alone:** courtyardstores, parishcouncil and pcp show red DKIM and DMARC crosses. DKIM only matters for sending through Forward Email, and outbound SMTP is off for all three (API: `has_smtp` false; only pebmarsh.com has it, verified 2 Nov). DMARC: Forward Email wants a `_dmarc` record per subdomain and doesn't recognise that the apex record (no `sp=`) covers them; receivers do. pebmarsh.com's amber DMARC flag is Forward Email recommending `p=reject`; consider it around 2 Dec if quarantine stays clean.
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
