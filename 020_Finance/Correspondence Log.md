# Correspondence Log

Finance-relevant emails (rate changes, offers, statements, loan documents),
found and filed by `/refresh`. Mortgage/divorce-related correspondence lives
in the sibling `divorce` project instead — not duplicated here. Individual
entries live in `Correspondence/`.

**2026-09-21.** Nothing new to file — the only hit since 18 Sept was a
routine Barclaycard "Your statement is here" notice (Heather's card, 19
Sept, no figures in the body), same not-worth-an-entry pattern as prior
statement-ready notices. All other sender and keyword searches since 18
Sept came back empty. ⏳ The Harpers Haslemere **£158.40 refund is still
outstanding** — no credit has reached `Starling - Main` (checked against
the 17–19 Sept line items).

**Last checked:** 2026-09-21.

**2026-09-18 (second run, same day).** Nothing new. All three hits (NatWest
statement notice, Capital One new-device alert, Halifax statement-ready) were
already assessed earlier today; every other sender and keyword search empty.
Banktivity unchanged too — not a single line item has posted since 17 Sept,
so no balance diffs to reconcile. Notable only as the **first clean sweep on
the migrated OAuth credentials** (project `rupert-personal-507609`), which
ran without a token error. ⏳ The Harpers Haslemere **£158.40 refund is still
outstanding** — no credit has reached `Starling - Main`.

**Last checked:** 2026-09-18. The Gmail token had expired
(`invalid_grant`) and blocked the first attempt; Rupert re-authorised via
`auth.py` and the sweep then completed. **Fourth token expiry** (11 Aug,
26 Aug, 3 Sept, 18 Sept) — the refresh token doesn't seem to survive much
beyond a fortnight, so expect this roughly every other week.

Four hits, **none needing its own entry**:
- **Halifax, 17 Sept** — "your new credit card statement is ready"
  (Heather's card ending 3123). No figures in the email, but it confirms a
  **September statement exists** and that the **next payment is due
  12 Oct**. ⏳ That statement is the best remaining chance to pin down the
  **new standard rate effective 19 Nov** — it's in Heather's digital inbox,
  not reachable via Gmail. Noted in [[Shared Debt]]; needs Rupert to ask her
  to open it.
- **NatWest, 17 Sept** — "your latest card statement is now available". This
  is the notice for the **16 Sept statement Rupert already supplied**, which
  is filed at [[2026-09-16_natwest-0354-statement.pdf]]. Nothing new — and
  this time the statement itself was read, not just the notice.
- **Capital One, 17 Sept** — "Did you log in on a new device?" (Android,
  17 Sept 11:52). **Explained: Rupert's own app registration that day** (see
  [[Capital One]]). Benign, no action.
- **Tesco, 16 Sept** — statement-ready notice, already assessed last run
  (routine, no figures, card settled at £0.00).

All other sender and keyword searches came back empty.

**2026-09-18.** NatWest's **16 Sept statement** supplied by Rupert
([[2026-09-16_natwest-0354-statement.pdf]], filed to `xx_media`) — it
**confirms** the previous day's finding rather than changing it: SUMMARY OF
BALANCES again shows Purchases only, **£1,255.11 at 26.436%**, interest
included £52.55, no promotional row. New forward figures now on record from
NatWest itself: minimum £106.10, next DD **£300 on 11 Oct**, and estimated
interest next month **£26.81** (replacing the project's own estimate).
Notably the next DD falls *after* the Tesco transfer window shuts on 9 Oct —
see [[NatWest Mastercard]].

**Last checked:** 2026-09-17. One new email, plus a **major finding from a
statement that was already on disk**:

- 🚨 **NatWest 0% is gone — whole balance at 26.436%.** A £52.55 interest
  charge in Banktivity (15 Sept) led back to the **16 Aug statement**, which
  shows no promotional balance at all and had warned "estimated interest
  payment next month is £53.99". Filed as
  [[2026-08-16_natwest-statement-0pc-gone]] with the PDF in `xx_media`.
  Updates [[NatWest Mastercard]], [[0% Offers Tracker]],
  [[Solicitor Payment 0% Plan]] and [[Accounts]].
  **⚠️ Process failure worth remembering:** the 17 Aug refresh saw NatWest's
  *email* ("statement ready", no figures) and logged it as "not worth its own
  entry" — but the figures were in the PDF, which had been sitting in
  `~/Downloads` since 17 Aug. A figure-free statement notice is not the same
  as a statement with no news; for any card carrying a plan or promotional
  balance, open the statement.
- **Capital One Direct Debit reissue** (16 Sept) — admin notice, no figures,
  but it predicts a **duplicate DD mandate 22 Sept – 5 Nov 2026**; don't
  cancel either. Filed as
  [[2026-09-16_capital-one-direct-debit-reissue]] because a stray mandate in
  that window would otherwise look like an anomaly. Balance is £0.00, so no
  collection should occur at all.

All other sender and keyword searches since 15 Sept came back empty. The
16 Sept Tesco "statement available" notice was already assessed last run
(routine, no figures, card settled at £0.00).

**Previously — last checked:** 2026-09-16. Nothing new to file. One hit since 15 Sept: a
Tesco Bank "view your latest statement online" notice (16 Sept, card ending
2484) — routine statement-ready notice with **no figures in the body** (it
points at Online Banking/the app), same not-worth-an-entry pattern as prior
statement-ready notices, so not filed and nothing changed in
[[Tesco Clubcard Credit Card]] — that card is at a settled £0.00, so there
should be no minimum due on this statement. Every other sender search
(NatWest, M&S, Capital One, Barclays, Starling, Barclaycard, Halifax) and
both keyword searches came back empty. Six quiet days now.

**Correction (16 Sept, same session):** the long-carried "next expected are
the M&S £175 DD and the Tesco Loan £139.74 **at month-end**" was wrong on
both counts, and has been carried forward unchecked for several refreshes.
Neither is a month-end item and neither is outstanding: the **Tesco Loan** is
a **beginning-of-month** payment (contractually the 2nd, or next working day)
and September's already came out on 31 Aug — next ~2 Oct. The **M&S £175 DD**
collects around the **7th** — it ran on 5 Sept, so next is ~5–7 Oct. See
[[Tesco Loan]] and [[M&S Credit Card]].

**2026-09-16 (same session) — Tesco loan origination pack filed.** Rupert
supplied the full 11-page pack directly; filed as
[[2025-08-19_tesco-loan-origination-pack]] with the PDF in `xx_media`. It
establishes that the loan is **precomputed, not amortising** — see the entry
and [[Tesco Loan]] for why that matters.

**2026-09-09.** One item worth its own entry since 8 Sept:
a Starling "problem with your scheduled payments" notice — the £25.97
Tesco Clubcard minimum-payment DD failed on the Starling-Space funding
side this morning, retrying until 4pm today, ⏳ needs Rupert to top up
(see [[2026-09-09_starling-tesco-space-payment-failed]] and
[[Tesco Clubcard Credit Card]]). Also: Tesco's recurring balance-transfer
offer rolled forward (window now 9 Oct, rate now to Dec 2027 statement —
updated in [[0% Offers Tracker]] and the account note, no separate entry)
and two Barclays admin/marketing notices (Click to Pay rollout, an email
address update confirmation) with no figures, not filed. All other sender
and keyword searches since 8 Sept came back empty.

**2026-09-08.** Nothing new — the only hit since 7 Sept
(Halifax "you have a new message from us") was the digital-inbox notice
already filed that same day (see below). All other sender and keyword
searches since 7 Sept came back empty.

**2026-09-07.** One new item since 5 Sept: a Halifax notice
that the standard interest rate on Heather's card (ending 3123) is going up
from 19 Nov 2026 — new rate not yet known, the actual figure sits in a
digital-inbox message not visible via Gmail (see
[[2026-09-07_halifax-rate-increase-notice]] and [[Shared Debt]]). All other
sender and keyword searches since 5 Sept came back empty.

**2026-09-05.** One new item since 4 Sept: a Halifax
"payment due" reminder (Heather's card, £177.98 minimum by 10 Sept) —
confirms the £177.98 debt-servicing payment flagged 2 Sept is the current
minimum, not a one-off (see [[2026-09-04_halifax-payment-due-reminder]] and
project status). The Barclaycard 0% offer and Halifax "Lloyds app"
invitation surfaced again but are the same items already logged below, not
new. All other sender and keyword searches since 4 Sept came back empty.

**2026-09-04.** Three hits since 3 Sept, none worth their own
entry: a Barclaycard 0% purchases-offer reminder (Heather's card ending
5002, rolled forward — updated in [[0% Offers Tracker]] and
[[Shared Debt]]), a Halifax "invitation to start using the Lloyds app"
(pure marketing, no figures), and Barclays' routine "statement is
available" notice (Rupert's own current account, no figures, sent twice
same-minute). All other sender and keyword searches since 3 Sept came
back empty.

**2026-09-03 (second run same day).** Nothing new
— the only hit (the 3 Sept Halifax "payment received" notice) was already
logged earlier this run's own predecessor, re-surfaced by the date filter.
All other sender and keyword searches since 3 Sept came back empty.
Banktivity also unchanged since the prior run — no balance diffs to
reconcile against.

**2026-09-03 (earlier run).** Gmail token expired/revoked this run —
re-authorized mid-refresh (Rupert approved via browser) before sweeping.
Nothing new to file — only hit since 2 Sept was a routine Halifax "payment
received" notice (Heather's card, confirms the £177.98 debt-servicing
payment already visible in Banktivity, no new figures). All other sender
and keyword searches since 2 Sept came back empty.

**2026-09-02.** Nothing new to file — only hit since 1 Sept
was Halifax's recurring 0% transfer offer to Heather (terms rolled forward,
window now 30 Sept, available capacity refreshed to £1,169 as at 24 Aug —
updated in [[0% Offers Tracker]] and [[Shared Debt]]). All other sender and
keyword searches since 1 Sept came back empty.

**2026-09-01.** Nothing new to file — only hits since 28 Aug
were app-login/marketing noise with no figures or terms (Barclays app
welcome + security-tips emails, a Starling login notification, an M&S
mobile-banking-app-setup confirmation) — none finance-relevant. All other
sender and keyword searches since 28 Aug came back empty.

**2026-08-28.** Nothing new to file — full sender and keyword
sweep since 27 Aug came back empty.

**2026-08-27:** Nothing new to file — full sender and keyword sweep since
26 Aug came back empty.

**2026-08-26.** Gmail token expired/revoked this run —
re-authorized mid-refresh (see project memory) before sweeping. Nothing new
to file — full sender and keyword sweep since 25 Aug came back empty.

**2026-08-25:** Two hits since 24 Aug, neither worth its own
entry: a Barclaycard 0% purchases-offer reminder (Heather's card ending
5002, new terms — updated in [[0% Offers Tracker]] and
[[Shared Debt]]) and a routine Halifax "statement is ready" notice
(Heather's card, no figures). All other sender and keyword searches since
24 Aug came back empty.

**2026-08-24:** Nothing new to file — the only hits since
21 Aug were the same Barclaycard "statement is here" notice already logged
last refresh (re-surfaced by the date filter due to its US timezone
offset) and a Capital One app-update marketing email, neither
finance-relevant. All other sender and keyword searches since 21 Aug came
back empty.

**2026-08-21.** Nothing new to file — only hit was a routine
Barclaycard "statement is here" notice (Heather's card, 20 Aug, no figures),
same pattern as prior statement-ready notices, not worth its own entry. All
other sender and keyword searches since 20 Aug came back empty.

**2026-08-20:** Nothing new — the only hit (Starling's 19 Aug
failed-payment notice) was already filed last refresh. All sender and
keyword searches since 19 Aug came back empty. Banktivity now shows that
episode resolved (see [[Accounts]] and [[Tesco Clubcard Credit Card]]).

**2026-08-18:** Nothing new to file — only hit was Halifax's
recurring 0% transfer offer to Heather (17 Aug, terms unchanged, available
capacity refreshed to £1,284 as at 11 Aug — updated in
[[0% Offers Tracker]] and [[Shared Debt]]). All other sender and
keyword searches since 17 Aug came back empty.

**2026-08-17.** Nothing new to file — only hit was a routine
NatWest "statement ready" notice (15 Aug, no figures), same pattern as prior
statement-ready notices, not worth its own entry. All other sender and
keyword searches since 15 Aug came back empty.

**2026-08-15:** Nothing new to file — only hit was a routine
Tesco "statement ready" notice (15 Aug, no figures), same pattern as prior
statement-ready notices, not worth its own entry. All other sender and
keyword searches since 14 Aug came back empty.

**2026-08-14:** Nothing new — full sweep across all sender and
keyword searches since 13 Aug came back empty.

**2026-08-12 sweep:** Nothing new to file: Tesco's recurring BT offer
rolled forward again (terms unchanged — 0% to Nov 2027 statement, 4.99% fee,
window to 4 Sept — capacity figure updated in the tracker to reflect the
Tesco Clubcard balance flipping back to -£25.97, see Banktivity refresh); a
Tesco "balance is less than £0" notification (11 Aug, timestamped for the
9 Aug credit dip) is just a low-value confirmation of an event already
tracked in [[Tesco Clubcard Credit Card]], not filed separately.

**2026-08-11:** Gmail token expired/revoked this run — re-authorized
mid-refresh (see project memory) before sweeping. One genuinely new item filed
(Starling scheduled-payment failure); Tesco's recurring BT offer rolled forward
(terms updated in tracker/account note, no new entry); a Barclays feedback
survey and a Barclaycard purchases-0% offer (both 7 Aug, already assessed in
the prior session) reappeared in this window's sweep but aren't new.

**12-month historical backfill run 2026-07-21** (2025-07-21 to 2026-07-21,
using the direct Gmail API tooling — the MCP connector was found to be
unreliable, see project memory). Swept by sender and by keyword subject
across the full window. Surfaced two previously-undocumented items (filed
below); everything else was either already covered by an existing account
note (Tesco Loan origination, M&S card origination) or routine
noise/marketing not worth filing as its own entry (recurring
Barclaycard/Halifax 0% offers to Heather, statement-ready notices with no
figures, scam-safety emails, Starling Easy Saver rate cuts on a
near-zero-balance space, household direct debits out of this project's
scope) — **note (5 Aug 2026): "not worth filing" still means not worth an
individual entry here, but any 0%/promotional-rate offer's
current terms now go into [[0% Offers Tracker]] regardless,
even the recurring ones. See that note and `/refresh`'s step 3.**

## Entries

- [[2026-09-16_capital-one-direct-debit-reissue|2026-09-16 — Capital One Direct Debit reissue]] — duplicate mandate expected 22 Sept–5 Nov 2026, do not cancel; balance £0.00 so no collection due
- [[2026-08-16_natwest-statement-0pc-gone|2026-08-16 — NatWest statement: 0% balance gone, whole balance at 26.436%]] — 🚨 found 17 Sept from a £52.55 interest charge; the M&S transfer repaid the 0% balance and the solicitor fee replaced it at full rate
- [[2025-08-19_tesco-loan-origination-pack|2025-08-19 — Tesco Bank loan origination pack]] — backfilled 16 Sept 2026 from the paper pack; the signed CCA agreement, establishes the loan is precomputed (no monthly interest charges), free amortisation table available on request
- [[2026-09-09_starling-tesco-space-payment-failed|2026-09-09 — Starling scheduled payment failed (Tesco Credit Card Space)]] — £25.97 minimum-payment DD failed on funding side, ⏳ Rupert needs to top up by 4pm today
- [[2026-09-07_halifax-rate-increase-notice|2026-09-07 — Halifax standard rate increase notice (Heather's card)]] — rate rising from 19 Nov 2026, new rate not yet known
- [[2026-09-04_halifax-payment-due-reminder|2026-09-04 — Halifax payment-due reminder (Heather's card)]] — confirms £177.98 minimum, due 10 Sept
- [[2026-08-19_starling-scheduled-payment-failed-tesco-space|2026-08-19 — Starling scheduled payment failed (Tesco Credit Card space)]] — £74.43 out of the Space failed on insufficient funds, second such debit in three days, needs Rupert to check the app
- [[2026-08-13_ms-statement-dd-confirmed|2026-08-13 — M&S statement confirms £175 fixed DD landed]] — resolves open item from the 28 Jul DD amendment; £1,966.31 balance, £2,000 limit, 0% holding
- [[2026-08-10_starling-scheduled-payment-failed|2026-08-10 — Starling scheduled payment failed]] — £74.43 internal transfer to Tesco Credit Card space bounced on insufficient funds, retry outcome unconfirmed
- [[2026-07-28_ms-balance-transfer-confirmation|2026-07-28 — M&S balance transfer confirmation]] — £1,900 transferred in, Atkins Dellow solicitor-payment plan executed, updates NatWest/M&S balances
- [[2026-07-20_barclaycard-statement-heather|2026-07-20 — Barclaycard statement (Heather's card)]] — balance £7,274.24, APR 20.68%/22.8% compound resolved, updates Shared Debt.md
- [[2026-07-19_starling-joint-account-approved|2026-07-19 — Starling Joint account approved]] — new account, joint with Mandy Zimmer (Rupert's partner)
- [[2026-07-20_tesco-balance-transfer-offer|2026-07-20 — Tesco balance transfer offer]] — recurring, terms unchanged
- [[2026-07-16_natwest-mastercard-statement|2026-07-16 — NatWest Mastercard statement]] — confirms balance £1,420.56, 0% promo unchanged
- [[2026-07-06_ms-balance-transfer-offer|2026-07-06 — M&S balance transfer offer]] — recurring, terms unchanged
- [[2026-02-16_natwest-balance-transfer-card-opened|2026-02-16 — NatWest Balance Transfer card opened]] — backfilled, origination of the NatWest Mastercard
- [[2025-09-15_capital-one-credit-limit-increase|2025-09-15 — Capital One credit limit increase]] — backfilled, £800 → £1,800
