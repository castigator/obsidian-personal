# Correspondence

**Migrated from the git repo to the vault 1 Sep 2026** (Westgate-style: Obsidian is the sole
content store, the git repo is operational scaffolding only). This note and the `heather/`,
`subsidence/`, `insurance/`, `pensions/`, `rbs/`, `solicitors/`, `housebits/` subfolders here are
the only copies — the git repo's `correspondence/` no longer exists (recoverable from git history
if ever needed, `git log -- correspondence/` in the divorce repo). New findings from `/refresh` are
written straight here going forward, not to the repo.

Emails pulled from Gmail (rupert@pebmarsh.com). Last checked: **2 Sep 2026** via direct
Gmail API — see note below. Covering April 2024 – August 2026.

**OAuth token note (28 Jul 2026):** the Gmail API refresh token expired (`invalid_grant: Token has
been expired or revoked`) — likely the 7-day refresh-token lifetime Google enforces on OAuth apps
still in "Testing" publishing status, not something Rupert did. Confirmed the token was still
valid when finance's own `/refresh` ran successfully at 10:18am on 28 Jul, so it expired sometime
between then and the divorce project's refresh later that day — consistent with a 7-day window
from whatever time on 21 Jul the original consent was granted. Re-authorized via
`~/.claude-personal/gmail-api/auth.py` (run with `-u` for unbuffered output so the consent URL
actually appears when redirected to a log file — plain `python auth.py` piped to a file buffers
the URL until process exit, hanging with no visible prompt). Fixed; working again as of 28 Jul.
If this happens again, the same permanent fix would be publishing the OAuth consent screen (moves
it out of the 7-day testing-token limit) — flagged, not yet done.
**Recurred 4 Aug 2026** (same `invalid_grant` error, consistent with the 7-day testing-token
pattern) — re-authorized again the same way, Rupert approved the consent screen. Publishing the
OAuth consent screen remains the actual fix, still not done.
Note: searches use `in:anywhere` to include archived mail.

**Search tooling note (21 Jul 2026):** the standard `mcp__claude_ai_Gmail__search_threads` tool
was found to have a genuine index/matching defect — it silently omits specific messages from
results under every query shape, including a completely unfiltered inbox listing. Confirmed via
a working comparison: Gmail's own native web search found messages instantly that the tool
could not find at all. Fixed by setting up direct Gmail API access (OAuth, read-only scope) —
scripts at `~/.claude-personal/gmail-api/` (`search.py`, `get.py`, `attach.py`) now used for all
correspondence discovery instead. See `feedback_gmail_search_unreliable.md` in the memory store
for the full diagnostic trail.

### Source marking (important)

Entries are tagged by **where the email actually lives**, because it governs what Rupert can openly act on:

- **🔒H — Heather's mailbox** (addressed to/from `heather@pebmarsh.com`, visible via domain access). Rupert was
  **not** a recipient. He cannot act on this knowledge openly without revealing he can see her mail — work only
  from his own independent paper trail.
- *(unmarked)* — **Rupert's own** correspondence (to/from `rupert@pebmarsh.com`, or where he was a named
  recipient/cc). Safe to act on openly.

### Attachment rule

Every Gmail sweep: capture + read + log anything relevant, and **always surface a list of any substantive
attachments Rupert needs to download** (ignore logos/signature images). If none, say so explicitly.

## Folders

### [heather/](heather/)

**[whatsapp-transcript.md](heather/whatsapp-transcript.md)** — verbatim, word-for-word WhatsApp
transcript (started 28 Jul 2026, potential evidentiary record). Separate from the topical summary
notes below — no paraphrasing, built only from screenshots Rupert provides.

Emails from/involving Heather Thomas (heather.heather.thomas@gmail.com / heather@pebmarsh.com):

| Date | File | Summary |
|------|------|---------|
| 2024-07-21 | — | AA policy change (forwarded) |
| 2024-10-06 | [coop-estate-planning.md](heather/2024-10-06_coop-estate-planning.md) | Co-op Estate Planning appointment (wills) |
| 2025-08-27 | [rbs-mortgage-early-redemption.md](heather/2025-08-27_rbs-mortgage-early-redemption.md) | RBS mortgage early redemption penalty. Mortgage #11177343, ~£311k outstanding |
| 2025-09-08 | [property-valuations.md](heather/2025-09-08_property-valuations.md) | Valuations from Michaels Property & St George Property Group (attachments) |
| 2025-09-19 | [aa-cancellation.md](heather/2025-09-19_aa-cancellation.md) | AA membership cancelled |
| 2025-11-08 | [house-shit-subsidence-discovery.md](heather/2025-11-08_house-shit-subsidence-discovery.md) | **Subsidence discovered** — huge cracks, utility room + front room window |
| 2026-03-12 | [fwd-subsidence-update.md](heather/2026-03-12_fwd-subsidence-update.md) | Forwarded GHG Solutions level monitoring update |
| 2026-04-17 | [house-bits.md](heather/2026-04-17_house-bits.md) | "house bits" — HomeServe drain insurance (policy 443906608) + E.ON Next statement |
| 2026-04-27 | [po-home-insurance-renewal.md](heather/2026-04-27_po-home-insurance-renewal.md) | **PO Home Insurance renewal** — H0000011333/06, Silver Plus, renews 04/05/2026, £655.27/yr. Rupert is joint policyholder. |
| 2026-04-27 | [anglian-water-bills.md](heather/2026-04-27_anglian-water-bills.md) | Anglian Water bills (Dec 2024 + Dec 2025). **Water usage doubled** — 204→371 m³, possible leak. |
| 2026-05-06 | [po-insurance-renewal-finance.md](heather/2026-05-06_po-insurance-renewal-finance.md) | **PO Home Insurance renewed** — Premium Credit financing £741.52 (£655.27 premium + fees), ref D647985GCE. 11 monthly DDs from May 2026. |
| 2026-05-11 | [ghg-liability-accepted.md](heather/2026-05-11_ghg-liability-accepted.md) | **SUBSIDENCE LIABILITY ACCEPTED** — insurer accepts claim under subsidence peril. £1,000 excess. GHG chasing tree removal schedule. |
| 2026-05-15 | [heather-prudential-db-pension.md](heather/2026-05-15_heather-prudential-db-pension.md) | **HEATHER'S PENSION FOUND** — XPS Admin notification: Heather has DB pension with Prudential Staff Pension Scheme. CETV available online. First evidence of her pension. |
| 2026-05-20 | [heather-pension-quotation-uploaded.md](heather/2026-05-20_heather-pension-quotation-uploaded.md) 🔒H | **Retirement quotation uploaded to Heather's MyPension portal** — proves her DB CETV has been sitting ready since 20 May, not something still to be requested. Found only via year-back sweep after standard Gmail search proved broken. |
| 2026-05-19 | [eon-next-fixed-tariff-ending.md](heather/2026-05-19_eon-next-fixed-tariff-ending.md) | E.ON Next fixed tariff ending on account A-666D053F (Pebmarsh). Risk of higher variable rate — Rupert pays 80% of electricity. |
| 2026-05-19 | [tree-removal-quote.md](heather/2026-05-19_tree-removal-quote.md) | **Tree removal quote** — Heather forwarded quote from HJ Tree Care (Hamish Jenkins). Willow £700 + Maple £500 = £1,200 (or £2,000 with full stump removal). Available within weeks. |
| 2026-05-19 | [eon-next-new-fixed-tariff.md](heather/2026-05-19_eon-next-new-fixed-tariff.md) | **E.ON tariff resolved** — Heather signed up to Next Fixed 12m v132. £147.98/mo estimated. Starts 21 May 2026. |
| 2026-05-26 | [council-tax-single-occupancy.md](heather/2026-05-26_council-tax-single-occupancy.md) | Heather looking at **single occupancy council tax discount** (25% off) at Braintree. Confirms living alone at Pebmarsh. |
| 2026-05-26 | [ellisons-initial-appointment.md](heather/2026-05-26_ellisons-initial-appointment.md) | **Ellisons follow-up:** Francesca Easter available **4 Jun or 8 Jun** at Bury St Edmunds. Rate **£335/hr + VAT (£402)**. 1hr initial consultation payable in advance. 20% Blue Light discount available. |
| 2026-05-27 | [atkins-dellow-appointment.md](heather/2026-05-27_atkins-dellow-appointment.md) | **Atkins Dellow appointment:** Alan Caldwell confirmed meeting **Tue 2 Jun 2026 at 12:00 noon**, 2 Friars Street, Sudbury. Needs Verify365 ID check + confirmation of time. |
| 2026-05-28 | [ellisons-onboarding.md](heather/2026-05-28_ellisons-onboarding.md) | **Ellisons onboarding:** Amy Allston opening file. AML ID check required via Client Portal (link from noreply@legl.com). Need 1x name/DOB doc + 2x address docs. Attached: acceptable ID checklist PDF. |
| 2026-06-01 | [atkins-dellow-verify365-id-check.md](heather/2026-06-01_atkins-dellow-verify365-id-check.md) | **Atkins Dellow ID check:** Verify365 onboarding link arrived (the one Rupert chased). Needs passport + 2 proof-of-address docs (ID doc can't double up). App or desktop (portal.verify365.app). Complete before/at the 2 Jun meeting. |
| 2026-06-01 | [atkins-dellow-verify365-submitted.md](heather/2026-06-01_atkins-dellow-verify365-submitted.md) | **Verify365 ID COMPLETED 1 Jun PM.** Documents show "Verified" in portal; firm confirms onboarding process complete but **submission still under review** ("should anymore information be needed, you will be notified"). MyID profile + screenshot saved to Obsidian `Analysis/`. |
| 2026-06-02 | [atkins-dellow-advice-meeting-followup.md](heather/2026-06-02_atkins-dellow-advice-meeting-followup.md) | **Post-consultation follow-up** (subject "Re: Advice Meeting"). Alan: pleasure to meet; gov divorce portal link + NFM mediation finder link; engage Family Mediation Service "as soon as practicable". Full meeting notes in Obsidian `Analysis/2026-06-02_atkins-dellow-consultation.md`. |
| 2026-06-04 | [message-proposing-talk.md](heather/2026-06-04_message-proposing-talk.md) | **Rupert → Heather (text msg, not email).** Opened the cooperative conversation — thanked her for forwarding the drain claim, flagged trees-cost holding position, mentioned his solicitor consultation, proposed they **talk soon** about cost + tackling it together sensibly. Left timing to her. The pivotal "talk to Heather" next step now in motion. |
| 2026-06-06 | [heather-started-divorce-application.md](heather/2026-06-06_heather-started-divorce-application.md) 🔒H | **HEATHER STARTED AN ONLINE DIVORCE APPLICATION** (gov.uk portal) the morning after the 5 Jun talk. Created HMCTS account (10:24) + saved application (10:40). **SAVED, NOT SUBMITTED** (held 6 months). To Heather only — Rupert not a recipient, can't act openly. ❓ Can't tell SOLE vs JOINT from these — ask Heather directly. The process is now actually moving. |
| 2026-06-09 | [whatsapp-divorce-fee-and-michaels-valuation.md](heather/2026-06-09_whatsapp-divorce-fee-and-michaels-valuation.md) | **WhatsApp.** (1) Michaels Property valuation booked **Fri 12 Jun 9:30am** (Aaron Wilcock; prev £550k pre-subsidence — flag subsidence if attending). (2) **Heather paid £300 toward the divorce fee, wants Rupert to pay his share, then she confirms + submits** ("14 days to pay" ≈ 22 Jun deadline). ⚠️ Payment mechanism + £12 gap (£300+£300≠£612) to clarify — sign into HMCTS portal for the authoritative amount. |
| 2026-06-08 | [joint-divorce-application-rupert-invited.md](heather/2026-06-08_joint-divorce-application-rupert-invited.md) | ✅ **JOINT APPLICATION — Rupert invited as Applicant 2 and HAS JOINED.** gov.uk emails to Rupert's own inbox (open): 16:56 invite (it's a **joint** app; URN 1780-7415-8911-6303, code DMPZ8L9S; review by **22 Jun**); 20:00 he created his HMCTS account; 20:10 confirms **he reviewed Heather's answers + added his Applicant-2 info**. Resolves SOLE-vs-JOINT — it's JOINT. **Next gate: Heather confirms + pays £612 by 22 Jun → app submitted → 20-wk clock starts.** |
| 2026-06-12 | [divorce-application-submitted.md](heather/2026-06-12_divorce-application-submitted.md) | ✅ **DIVORCE APPLICATION SUBMITTED + PAID (£612).** HMCTS confirms to Rupert's own inbox (open): joint application submitted & paid, case ref 1780-7415-8911-6303. Heather submitted + paid the full £612 on her card this morning (receipt ref RC-1781-2510-1430-3186, 🔒H). **Court checks it; acceptance email by 10 July 2026 → then 20-week clock starts.** Hold Final Order until consent order sealed. |
| 2026-06-12 | [whatsapp-valuation-questions.md](heather/2026-06-12_whatsapp-valuation-questions.md) | **WhatsApp Rupert → Heather.** Notes the submission (queries when 20 weeks starts) + sets four questions for today's Michaels valuation (Aaron Wilcock): as-seen price, post-repair price, speed of sale, and whether accepted liability / transferable cash settlement helps a sale. Underlying call: wait for repairs vs sell sooner. |
| 2026-06-13 | [michaels-valuation-aaron-wilcock.md](heather/2026-06-13_michaels-valuation-aaron-wilcock.md) | **MICHAELS VALUATION (Aaron Wilcock).** Forwarded by Heather to Rupert (open). **£550k once subsidence rectified; £400k–£425k if sold now** (mortgage lenders won't lend on an active claim → cash buyers only, hard to sell). Clear recommendation: complete claim + works first. ~£125k–£150k gap vs ~£44k/11mo dual-housing carry → strong steer to wait; cash-settlement is the lever to shorten the wait. St George 2nd opinion still to arrange. |
| 2026-06-16 | [divorce-application-accepted-issued.md](heather/2026-06-16_divorce-application-accepted-issued.md) | ✅ **APPLICATION ACCEPTED & ISSUED (16 Jun).** HMCTS Notice of Proceedings to both (open). Court checks done; **20-week clock running.** **Conditional Order: apply from 4 Nov 2026.** Rupert has confirmed receipt on the portal; Heather should too. Runway 16 Jun→4 Nov is the window to sort finances (CETVs → consent order). Hold Final Order until consent order sealed. |
| 2026-07-06 | [whatsapp-trees-catalyst-valuation-rbs.md](heather/2026-07-06_whatsapp-trees-catalyst-valuation-rbs.md) | **WhatsApp.** Willow tree cancelled for heat (36°C), rearranged **Thu 9 Jul**. Catalyst drain engineer visit **happened Fri 3 Jul** (cameras down drains, reviewed GHG report). **Valuations day confirmed Sat 11 Jul** — Heather will leave Rupert to show agents round. Heather asks whether "notify RBS" means subsidence or divorce. Council tax now ~£182/mo; Heather proposes putting monthly surplus toward a credit card. |
| 2026-07-15 | [whatsapp-four-points.md](heather/2026-07-15_whatsapp-four-points.md) | **WhatsApp Rupert → Heather (17:48) — FOUR-POINT MONEY PROPOSAL.** (1) Split the shared cards now — Rupert finances his ~£7,400 half, remainder hers, each controls own 0% deals; (2) monthly 80/20 rebalance (£128/mo, waived if cards split; otherwise redirected at card balances); (3) cats become Heather's, £65/mo stops; (4) RBS letter coming (separation + subsidence + payment-support ask), will share first. ⚠️ No money moves on (1) until Alan advises on documentation. |
| 2026-07-15 | [whatsapp-heather-reply-four-points.md](heather/2026-07-15_whatsapp-heather-reply-four-points.md) | ✅ **HEATHER AGREES TO ALL FOUR (18:27, 39 min later).** (1) Card split YES, her allocation: she takes Halifax + mum's Barclaycard (£7,222 ex-int); Rupert takes big Barclaycard (£7,283 ex-int) — near-perfect 50/50, "does that work?" needs a reply. (2) Bills continue 80/20 (£128 waived per split-world framing). (3) Cats: "fair enough". (4) RBS: "up to you". (5) **Ann loans corrected to £8,840** (£3,318 MBNA + £5,522 loan) — repay from house sale. **Alan documentation question now un-gated.** |
| 2026-07-16 | [atkins-dellow-instruction-card-split.md](heather/2026-07-16_atkins-dellow-instruction-card-split.md) | **RUPERT INSTRUCTS ATKINS DELLOW (16:31).** Formal engagement email to Alan Caldwell: status update (issued 16 Jun, clock running), asks structure (sole client vs one-couple-one-lawyer — the banked 3 Jun question), and the live advice request: **agreed card split** (Rupert: Barclaycard £7,283 via pre-approved personal loan, NOT drawn; Heather: Halifax + mum's card £7,222) — what to document at payment + consent-order treatment. £300/hr quoted back; payment structure asked. **No money moves until Alan replies.** |
| 2026-07-17 | [whatsapp-agreement-impasse.md](heather/2026-07-17_whatsapp-agreement-impasse.md) | **WhatsApp — card-split note STALLED on signature.** Heather's objection is form not terms ("you made a bloody contract"); "will think about it again as well as utilities". On hold — she's away from 18 Jul. |
| 2026-07-23 | [whatsapp-cards-and-drains-followup.md](heather/2026-07-23_whatsapp-cards-and-drains-followup.md) | **WhatsApp Rupert → Heather.** Re-opens the card split (plain yes/no + needs an answer to sort loan financing; names the 84%/16% rebalance as the fallback if not) and flags the Catalyst drain repair booked 28 Jul, £200 excess half set aside. Awaiting reply. |
| 2026-07-23 | [whatsapp-heather-reply-cards-drains-utilities.md](heather/2026-07-23_whatsapp-heather-reply-cards-drains-utilities.md) | **WhatsApp Heather → Rupert.** Cards still "thinking about it"; **Heather switching Eon electricity/water/oil to her own name/DD from Aug**, out of the 80/20 flow; drain excess confirmed paid direct to contractor on the day. Also: updated RBS repayment-guide photo (**£309,845.38 outstanding, £176,606.30 behind guide, 30 Jun 2026**) and a Barclaycard statement PDF sent but not yet reviewed. |
| 2026-07-18 | [heather-mailbox-sweep-holiday-window.md](heather/2026-07-18_heather-mailbox-sweep-holiday-window.md) 🔒H | **Holiday-window sweep (4 items, all 🔒H):** (1) easyJet — **Heather returns Fri 24 Jul** (Palma→Southend, lands 13:00); (2) **Halifax statement — card ends 3123, NOT 0664** as in the draft split note ⚠️ verify before signing; (3) she cancelled her Braintree District (council tax) Direct Debit — unexplained, watch the bills flow; (4) E.ON Pebmarsh account **£528.55 in credit**, DD £107.11/mo over-collecting. |
| 2026-07-16 | [atkins-dellow-reply-instruction-accepted.md](heather/2026-07-16_atkins-dellow-reply-instruction-accepted.md) | ✅ **ALAN ACCEPTS INSTRUCTION (19:35, ~3hrs later)** + answers inline: (1) **documentation = both sign + date a written note setting out the agreed card split, scan to Alan**; (2) consent order records it as a **Recital** "recording what you have already agreed and implemented". Warm on the cooperative path. Doesn't work Fridays — fuller action + Terms of Business/Client Care Letter/Costs Schedule **Monday 20 Jul**; structure question presumably then too. Split effectively GREEN-LIT once the note is signed. |
| 2026-06-25 | [atkins-dellow-first-appointment-invoice.md](heather/2026-06-25_atkins-dellow-first-appointment-invoice.md) | Atkins Dellow invoice (ref 26033) for the 2 Jun first appointment — £90.00 (£75 + VAT), paid in full from funds already on account. Surfaced only via direct Gmail API access, not the standard search tool. |
| 2026-07-20 | [atkins-dellow-engagement-pack.md](heather/2026-07-20_atkins-dellow-engagement-pack.md) | ✅ **ENGAGEMENT PACK RECEIVED (16:49).** Matter THO130/0001 "Financial Remedy". **£1,982 fixed fee inc. VAT is CONDITIONAL on staying amicable/agreement with Heather — reverts to hourly (£300–£325/hr) if contested.** Same £1,982 payment-on-account required. Anticipated 6+ months. **Cost Schedule needs Rupert's signature** (Alan's side already signed). No answer yet on the sole-client-vs-Resolution-Together structure question. Attachments in `Correspondence/heather/`. ⚠️ This email did not surface via Gmail search/list this session (tool indexing lag on recent mail) — found only via Rupert's screenshot; see correspondence file for detail. |
| 2026-07-24 | [whatsapp-utilities-correction-sent.md](heather/2026-07-24_whatsapp-utilities-correction-sent.md) | **WhatsApp Rupert → Heather (09:14).** Corrects the 23 Jul £200/mo utilities-handover figure to ~£300 (actual £305.90), flags the cats £65/mo stopping stacks on top — asks if she can manage it. |
| 2026-07-24 | [whatsapp-rbs-message-preview-sent.md](heather/2026-07-24_whatsapp-rbs-message-preview-sent.md) | **WhatsApp Rupert → Heather (09:47), PDF attached.** RBS draft communication (separation + subsidence, support ask) sent for her sight before sending, per the 7 Jul agreement. Awaiting her sign-off. |
| 2026-07-24 | [whatsapp-consent-order-route-options.md](heather/2026-07-24_whatsapp-consent-order-route-options.md) | **WhatsApp Rupert → Heather (11:31).** Lays out four routes to get the financial consent order done — DIY, mediation+drafting (~£1,200, e.g. Amicable), separate solicitors, or Alan drafting for Rupert only (£2k, Heather not advised) — asks her plan, decoupled explicitly from "amicability". Gates whether Rupert signs Atkins Dellow's Cost Schedule. |
| 2026-07-24 | [atkins-dellow-holding-response.md](heather/2026-07-24_atkins-dellow-holding-response.md) | **Rupert → Alan (11:41).** Holding response — thanks for the pack, delay is because he's discussing the route with Heather first, will come back once settled. Doesn't re-press the unanswered one-couple-one-lawyer question. |
| 2026-07-25 | [fwd-one-account-redemption-aug2025.md](heather/2026-07-25_fwd-one-account-redemption-aug2025.md) | **Old RBS redemption statement forwarded** (29 Aug 2025: balance £309,937.07, total payable £311,725.72 — no separate ERC line shown, worth weighing against the "penalty applies" note once RBS replies to the 27 Jul letter). |
| 2026-07-27 | [heather-self-mailed-signed-rbs-letter_LOCKH.md](heather/2026-07-27_heather-self-mailed-signed-rbs-letter_LOCKH.md) 🔒H | Heather self-mailed a scan of Rupert's signed RBS letter, same day. **Resolved** — Rupert confirms he sent it to her via WhatsApp himself; just her filing a copy. |
| 2026-07-27 | [atkins-dellow-signed-cost-schedule-sent.md](heather/2026-07-27_atkins-dellow-signed-cost-schedule-sent.md) | ✅ **Signed Cost Schedule sent to Alan (20:07)**, un-gating the Atkins Dellow engagement — route question resolved, signed at home to preserve the 14-day cancellation right. ⚠️ Sent as a new Gmail thread rather than appended to the original. Next: call to pay £1,982 by card, 28 Jul morning. |
| 2026-07-28 | [whatsapp-solicitor-details-rbs-sent.md](heather/2026-07-28_whatsapp-solicitor-details-rbs-sent.md) | ✅ **RBS letter confirmed sent** + **solicitor details shared with Heather** (Alan Caldwell's contact). Mediation flagged by Heather as "probably a good thing" once she's spoken to her solicitor — still open. Bills-table £5 difference resolved informally (not worth adjusting). New: Apple + Barclays Blue subscriptions cancelled. |
| 2026-05-27 | [certas-energy-oil-order-delivery_LOCKH.md](heather/2026-05-27_certas-energy-oil-order-delivery_LOCKH.md) 🔒H | First Certas activity in a 12-month backfill — one-off oil order + delivery, account 9778375 opened/first used. Precedes the 28 Jul DD setup on the same account. |
| 2026-07-28 | [certas-energy-dd-confirmation_LOCKH.md](heather/2026-07-28_certas-energy-dd-confirmation_LOCKH.md) 🔒H | Heather set up her own **£200/month Direct Debit with Certas Energy** (oil, Predict plan) — follows through on her 23 Jul "I'll contact certas" comment. ⚠️ Certas wasn't on the tracked-sender list — this is why it didn't surface in the sweep; added going forward. |
| 2026-08-04 | [halifax-payment-received.md](heather/2026-08-04_halifax-payment-received.md) 🔒H | Routine Halifax notice — £62.83 min payment made on the card ending **3123**, confirming the card-split ⚠️ (was mistakenly noted as 0664). ⚠️ Halifax wasn't on the tracked-sender list — added going forward. |

### [subsidence/](subsidence/)

Subsidence claim timeline. Claim ref: **6843593K** / Policy ref: **S2520891** / Post Office policy: **H0000011333**.

| Date | File | Summary |
|------|------|---------|
| 2025-11-08 to 2025-11-27 | [claim-initiation.md](subsidence/2025-11-08_to_2025-11-27_claim-initiation.md) | Full thread: discovery, post-visit, insurance history, Rupert asks to stay in loop |
| 2025-12-11 | [awaiting-insurer-instructions.md](subsidence/2025-12-11_awaiting-insurer-instructions.md) | Kim Salter: awaiting insurer instructions |
| 2026-01-09 | [ghg-solutions-correspondence.md](subsidence/2026-01-09_ghg-solutions-correspondence.md) | Kim Salter: attached correspondence |
| 2026-02-10 | [ghg-solutions-correspondence.md](subsidence/2026-02-10_ghg-solutions-correspondence.md) | Kim Salter: attached correspondence |
| 2026-03-11 | [ghg-solutions-level-monitoring.md](subsidence/2026-03-11_ghg-solutions-level-monitoring.md) | Kim Salter: level monitoring + site investigations pending |
| 2026-04-11 | [ghg-solutions-correspondence.md](subsidence/2026-04-11_ghg-solutions-correspondence.md) | Vicky Salter (Ops Manager): attached correspondence. First escalation. |
| 2026-05-11 | [ghg-liability-accepted.md](subsidence/2026-05-11_ghg-liability-accepted.md) | **LIABILITY ACCEPTED.** Insurer accepts subsidence claim. £1,000 excess at repair stage. Awaiting May readings. Chasing tree removal. |
| 2026-05-12 | [rupert-to-ghg-questions.md](subsidence/2026-05-12_rupert-to-ghg-questions.md) | Rupert → GHG: asking for indicative repair costs, whether tree removal is insurer-funded, and whether monitoring period can be shortened. CC'd Heather. |
| 2026-05-15 | [ghg-replies-to-questions.md](subsidence/2026-05-15_ghg-replies-to-questions.md) | **GHG replies:** No repair estimate yet (need contractor post-monitoring). Tree removal is policyholder's cost but insurer funding possible if financial hardship. Monitoring timeline reviewed periodically, no shortening committed. **Cash settlement option confirmed.** |
| 2026-05-19 | [ghg-tree-removal-funding-response.md](subsidence/2026-05-19_ghg-tree-removal-funding-response.md) | **GHG will submit funding request** to insurer for tree removal. Needs a tree removal quote first. |
| 2026-05-26 | [may-crack-monitoring-tree-quote-forwarded.md](subsidence/2026-05-26_may-crack-monitoring-tree-quote-forwarded.md) | May 2026 crack readings — no significant movement (0.15mm closure / 0.01mm opening). GHG forwards HJ Tree Care £1,200 quote to insurer for funding decision. CC'd to Rupert. |
| 2026-06-05 | [tree-funding-approved.md](subsidence/2026-06-05_tree-funding-approved.md) | ✅ **TREE FUNDING APPROVED.** Insurer approves full **£1,200** tree surgery (GHG/Kim Salter, to both Rupert + Heather). GHG: proceed with works. Company-headed quote/invoice + completion photo needed for payment. Blocker on instructing HJ Tree Care now gone. |
| 2026-06-08 | [whatsapp-trees-scheduled.md](subsidence/2026-06-08_whatsapp-trees-scheduled.md) | 📅 **Trees BOOKED 18–19 Jun** (Hamish/HJ Tree Care) — Heather arranged it (WhatsApp). ⚠️ Both away those dates (Rupert busy, Heather away); Rupert asked Heather how access/sign-off works for Hamish. |
| 2026-07-14 | [june-crack-monitoring-tree-status-chase.md](subsidence/2026-07-14_june-crack-monitoring-tree-status-chase.md) | **June 2026 crack readings show more movement** (0.73mm opening, one station) than May. GHG chasing Heather on whether tree works are done — as of 14 Jul GHG still didn't know. Confirms trees remain the active blocker. Found via year-back sweep 21 Jul (🔒H at the time); lock lifted 23 Jul — Heather forwarded it to Rupert openly. |
| 2026-07-23 | [trees-removed-and-poisoned.md](subsidence/2026-07-23_trees-removed-and-poisoned.md) | ✅ **Willow & Maple trees removed and poisoned.** Heather to GHG, Rupert cc'd. Quote + invoice + completion photos to follow — needed before insurer pays the £1,200. |
| 2026-07-30 | [tree-removal-quote-invoice-submitted.md](subsidence/2026-07-30_tree-removal-quote-invoice-submitted.md) | ✅ **Quote + invoice sent to GHG** (HJ Tree Care, £1,200: Willow £700 + Maple £500). GHG will now issue the reimbursement request to the insurer. ⚠️ No completion photo in this thread — GHG's 5 Jun approval required one; worth confirming it's covered. |
| 2026-08-04 | [ghg-bank-details-verification-request.md](subsidence/2026-08-04_ghg-bank-details-verification-request.md) 🔒H | GHG requests Heather verify bank details (single-use link + phone call) for the £1,200 tree reimbursement, claim ref S2520891. |
| 2026-08-07 | [ghg-tree-invoice-to-insurers.md](subsidence/2026-08-07_ghg-tree-invoice-to-insurers.md) 🔒H | GHG confirms tree invoice passed to insurer for direct payment. Next crack-monitoring round due August 2026, report to follow. |

`subsidence/attachments/legacy-download/` — a raw dump of .eml/PDF files from before the topical
notes above existed (claim correspondence, blank letters, CCTV/SI reports). Not deduped against
the notes above — worth a declutter pass at some point, kept as-is for now.

### [housebits/](housebits/)

Downloaded attachments from Heather's "house bits" email (17 Apr 2026). See [housebits/README.md](housebits/README.md).

- `YourDocuments.pdf` — HomeServe Plumbing & Drainage Plus policy (443906608)
- `Your renewal document.pdf` — Same policy, renewal notice
- `eon-next-statement-2026-04-14.pdf` — E.ON Next electricity statement (Pebmarsh)

Also filed directly in `heather/` (received 27 Apr 2026):
- `POHOMESALEAILH05100000000H000001133306260410000184.pdf` — PO Home Insurance renewal pack (H0000011333/06)
- `Anglian water bill Dec 24.pdf` — Anglian Water bill Nov 2023–Nov 2024
- `Anglian water bill Dec 25.pdf` — Anglian Water bill Nov 2024–Nov 2025
- `eon-next-statement-2026-04-14.pdf` — E.ON Next electricity (copy, also in housebits/)
- `Your renewal document.pdf` — HomeServe renewal (copy, also in housebits/)

### [insurance/](insurance/)

- [README.md](insurance/README.md) — Insurance history, policy documents index, and drain claim policy wording analysis
- [2024-07-21_policy-documents.md](insurance/2024-07-21_policy-documents.md) — Policy documents PDF from Heather
- [2026-05-12_po-drain-claim-submission.md](insurance/2026-05-12_po-drain-claim-submission.md) — **DRAIN CLAIM SUBMITTED** to Post Office. Forwarded GHG's Apr 2026 email with 3 evidence PDFs. Awaiting claim ref.
- [2026-05-12_po-drain-claim-autoreply.md](insurance/2026-05-12_po-drain-claim-autoreply.md) — PO auto-reply confirming receipt. Review within 2 working days (by 14 May). No claim ref yet.
- [2026-05-29_po-drain-claim-chase.md](insurance/2026-05-29_po-drain-claim-chase.md) — **DRAIN CLAIM CHASE** sent. 17+ working days overdue, no claim ref received. Reply-all on original thread (PO + Heather + GHG CC'd).
- [2026-06-04_drain-claim-registered-catalyst.md](insurance/2026-06-04_drain-claim-registered-catalyst.md) 🔒H — **DRAIN CLAIM REGISTERED — ref 6866220H.** Ageas opened it as a separate underground-services claim; handler Gemma Steels. **Catalyst Services UK** appointed to manage (Seren Rowley, 0333 004 8008 ext 314). Heather has agreed to upload damage evidence (Ageas portal, expires 11 Jun). ⚠️ All 5 emails to Heather only — Rupert not in loop; Catalyst couldn't reach Heather by phone.
- [2026-06-04_drain-claim-visibility-resolved.md](insurance/2026-06-04_drain-claim-visibility-resolved.md) — **VISIBILITY RESOLVED.** Rupert sent his PO chase (10:58); **PO replied to BOTH Rupert + Heather** (13:28, case #577576386 — confirms active Ageas claim, gives Ageas line 0345 165 0915). Then **Heather forwarded** all the Ageas/Catalyst claim emails to Rupert (16:15, no note). Drain-claim details (ref 6866220H, Gemma Steels, Catalyst) are now openly in Rupert's mailbox — `🔒H` lock effectively lifted. He can now contact Gemma/Catalyst directly as joint policyholder.
- [2026-06-08_catalyst-call-site-visit-prep.md](insurance/2026-06-08_catalyst-call-site-visit-prep.md) — **Catalyst phoned Rupert directly** (his own call, fully open). Took basic property info (what/where/animals) for the site engineer visit. **Catalyst will now phone Heather to arrange a time.** This is the phone call Catalyst had been chasing — Rupert handling it as joint policyholder.
- [2026-06-08_catalyst-engineer-visit-15-jun.md](insurance/2026-06-08_catalyst-engineer-visit-15-jun.md) 🔒H — **Site engineer visit proposed: Monday 15 June.** Catalyst (Seren Rowley) emailed Heather to book — engineers can attend Mon 15 Jun, time TBC, **must phone to confirm** (0333 004 8008 ext 314). To Heather only, but Rupert can ring Catalyst himself to confirm/coordinate (named joint contact). Heather on site, so access less of an issue than the trees. **SUPERSEDED — see 11 Jun (now 3 Jul).**
- [2026-06-11_catalyst-engineer-visit-3-jul.md](insurance/2026-06-11_catalyst-engineer-visit-3-jul.md) 🔒H — **Engineer visit re-offered: 3 July AM** (the 15 Jun date didn't go ahead). Catalyst (Oliver Mason, ext 355) emailed Heather — **must phone to book** (0333 004 8008). To Heather only; Rupert can ring himself as named joint contact. Catalyst job ref 139425; Ageas claim 6866220H.
- [2026-07-20_drain-claim-covered-repairs-scheduled.md](insurance/2026-07-20_drain-claim-covered-repairs-scheduled.md) — ✅ **DRAIN CLAIM CONFIRMED COVERED, REPAIRS BOOKED.** Catalyst (Vicky Russell) confirms investigation complete, claim covered under policy T&Cs. **Repairs scheduled Tue 28 Jul AM**, contractor calls 30 min ahead. **£400 excess** collected by contractor on the day. Rupert CC'd — own mail, safe to act on. Net recovery ~£8,960 as previously modelled.
- [2026-08-12_catalyst-drainage-report-scope-mismatch.md](insurance/2026-08-12_catalyst-drainage-report-scope-mismatch.md) — ⚠️ **COMPLETION REPORT RECEIVED, SCOPE DOESN'T RECONCILE.** Catalyst's own report (their own 3 Jul CCTV survey) lists only 4 defect locations vs DW Solutions' original 8-run/10-section £9,360.63 quote, using non-comparable MH numbering, with **no cost breakdown anywhere**. Can't confirm £9,360.63 worth of work was actually done. Reply to Vicky Russell suggested.
- [2026-08-13_rupert-reply-scope-query.md](insurance/2026-08-13_rupert-reply-scope-query.md) — ✅ **SENT.** Rupert's reply to Vicky Russell, itemising both DW Solutions' (£9,360.63, 8 runs + 2 gullies) and Catalyst's (4 MH-referenced defects) scopes side by side, asking whether Catalyst's work covers the same ground and what value it came to. Naive/questioning tone, no mention of the £400 excess.
- [2026-08-13_catalyst-reply-scope-query.md](insurance/2026-08-13_catalyst-reply-scope-query.md) — ✅ **REPLY RECEIVED same day** (Seren Rowley). Claims "7 repairs" on both the third-party quote and Catalyst's own work — doesn't cleanly reconcile against DW Solutions' 8 costed line items or Catalyst's own 4-location report. **Refuses to disclose cost/value** ("not at liberty"), asserts DW Solutions' quote "was inflated." £9,360.63/£8,960-net figures remain Rupert's own unconfirmed modelling. £400 excess not addressed. Practical read: probably as far as Catalyst goes voluntarily.
- [2026-08-14_rupert-thankyou-close.md](insurance/2026-08-14_rupert-thankyou-close.md) — Rupert's short courteous close on the thread, no new substance. Same day.
- 2026-08-14 — Rupert sent a short thank-you reply to Seren on the same thread (139425/6866220H), closing the loop courteously. No new substance; drain claim effectively closed pending any decision to escalate to Ageas directly.
- Policy docs (downloaded 12 May 2026): `PO-PolicySummary-2026.pdf`, `PO-PolicyBooklet-2026.pdf`, `PO-IPID-SilverPlus-2026.pdf`, `Ageas-TermsAndConditions-2026.pdf`, `ARAG-TermsAndConditions-2026.pdf`, `PO-ArrangementAndAdmin-TermsAndConditions-2026.pdf`

### [pensions/](pensions/)

- [2026-07-28_aegon-autoreply.md](pensions/2026-07-28_aegon-autoreply.md) — Automated ack from Aegon
  (`my.pension@aegon.co.uk`) for the Speedware/Infocentre trace enquiry sent same day. General
  enquiries quoted at 5 working days — expect substantive reply by ~4 Aug. Footer confirms "Aegon is
  a brand name of Scottish Equitable plc" — corroborates the WhatsApp-thread lead.
- [2026-07-28_rothesay-no-record.md](pensions/2026-07-28_rothesay-no-record.md) — ✅ **Rothesay
  substantively replied same day: no policy held in Rupert's name.** Rules out the buy-out-insurer
  fallback for Speedware — only the Aegon lead remains live (reply expected ~4 Aug). If Aegon also
  draws a blank, next step is the Pension Tracing Service directly.
- [2026-07-29_aegon-no-record.md](pensions/2026-07-29_aegon-no-record.md) — ⚠️ **Aegon also
  replied: no record on their Targetplan platform** — a day earlier than the ~4 Aug estimate. Both
  direct leads (Aegon + Rothesay) from the ex-colleague WhatsApp thread are now exhausted. Aegon
  flags they run multiple independent platforms, so worth a targeted follow-up before escalating to
  the Pension Tracing Service.

### [rbs/](rbs/)

- [2026-07-30_rbs-voicemail-callback-request.md](rbs/2026-07-30_rbs-voicemail-callback-request.md) — RBS voicemail requesting a callback (screenshot + note).
- [2026-07-31_rbs-callback-transcript.md](rbs/2026-07-31_rbs-callback-transcript.md) — Transcript of the 31 Jul RBS callback (recording also kept: `2026-07-31_rbs-callback-recording.mp3`).

### [solicitors/](solicitors/)

- [2026-08-03_alan-d81-vs-form-e-answer.md](solicitors/2026-08-03_alan-d81-vs-form-e-answer.md) —
  ✅ **Alan Caldwell answers the D81 vs Form E question** (asked 30 Jul): **D81 confirmed**, not
  Form E. Needs CETVs from both parties' pension providers (total figure only on the form), a
  signed **Record of Terms Agreed** between Rupert and Heather, and draft D81 figures from each.
  Blank D81 form attached — saved to `solicitors/2026-08-03_blank-d81-form.pdf`.

## Key contacts

### GHG Solutions (subsidence loss adjusters)

| Name | Role | Phone | Email |
|------|------|-------|-------|
| Matthew Turner | Chief Operating Officer | 02380 622622 / 07818 035054 | matthew.turner@ghgsolutions.co.uk |
| Kim Salter | Subsidence Technician (Cert CILA) | 02380 622622 | kim.salter@ghgsolutions.co.uk |
| Vicky Salter | Operations Manager - Subsidence (Cert CII, Cert CILA) | 02380 622622 / 02382 356529 | correspondence@agatha.app.ghgsolutions.co.uk |

GHG Solutions Limited | Threefield House | Threefield Lane | Southampton | SO14 3LP
FCA firm reference: 913965

### Ellisons Solicitors (front-runner)

| Name | Role | Phone | Email |
|------|------|-------|-------|
| Francesca Easter | Partner, Family Department | 01473 945614 | francesca.easter@ellisons.com |
| Francesca Tatum | Apprentice Solicitor, Family Dept (booking contact) | 01206 699406 | Francesca.Tatum@ellisons.com |
| Amy Allston | Client Support Assistant, Risk & Compliance | — | Amy.Allston@ellisons.com |

Ellisons Legal LLP | The Bath House | Le Cateau Rd | Colchester | Essex | CO2 7NA
SRA Number: 8001031 | LLP Registration: OC441111
Appointment location: Bury St Edmunds office

### Atkins Dellow (solicitor — consultation 2 Jun)

| Name | Role | Phone | Email |
|------|------|-------|-------|
| Alan Caldwell | Solicitor | 07796 145542 | alan.caldwell@atkinsdellow.com |
| Suzanne Corder | Front of House / Client Care | 0330 912 8338 | suzanne.corder@atkinsdellow.com |

Atkins Dellow LLP | 2 Friars Street, Sudbury, Suffolk CO10 2AA
SRA Number: 667838 | LLP Registration: OC430143

### Greene & Greene (solicitor — contacted 26 May)

| Name | Role | Phone | Email |
|------|------|-------|-------|
| Stuart Hughes | Managing Partner | 01284 717493 | stuarthughes@greene-greene.com |

### Estate agents (Pebmarsh valuations)

| Agent | Contact | Phone |
|-------|---------|-------|
| Michaels Property Consultants, Halstead | Aaron Wilcock | 01787 322799 |
| St George Property Group | Sam Fox | 07485 498850 |

### RBS Mortgage

- Mortgage number: 11177343
- Contact: 0345 300 4013

## Search criteria

- From: heather.heather.thomas@gmail.com, heather@pebmarsh.com
- From: ghgsolutions.co.uk
- From: greeneandgreene.co.uk (solicitor — contacted 26 May 2026)
- From: ellisons.com (solicitor — contacted 26 May 2026, auto-reply received)
- From: atkinsdellow.com (solicitor — contacted 26 May 2026)
- Keywords: subsidence, insurance, claim, pebmarsh
- Searched all mail (not just inbox) for full coverage
- Excluded: Urban Jungle, Ensleigh, CTickets, Interactive Investor, Feedspot, comparethemarket
