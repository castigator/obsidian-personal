---
tags:
  - divorce
  - house
  - mortgage
  - draft
---

# RBS Mortgage Notification — draft (in progress)

**Status:** DRAFT — not yet sent. Working document, come back and iterate.

## Goal

Tell RBS (mortgage #11177343) about two things at once:
1. Divorce/separation — Rupert and Heather running two households.
2. The subsidence claim — active, affecting the property and the timeline to sell.

And explore, without over-promising, whether RBS can offer any support (payment flexibility /
holiday) given the combined financial pressure of dual housing costs + a sale that's sensibly
delayed until the subsidence works complete (~spring 2027).

**Decided 7 Jul (WhatsApp with Heather):** notify RBS about **both** — primarily the divorce/separation,
but subsidence too, so RBS is fully in the loop on both. See
`correspondence/heather/2026-07-06_whatsapp-trees-catalyst-valuation-rbs.md`.

## Open question: which channel?

RBS publishes **no general inbound email address** for mortgage/financial-difficulty queries (checked
8 Jul 2026). The actual options:

- **Secure messaging via RBS Digital Banking / mobile app** — closest equivalent to email: written,
  timestamped, sits in the account. RBS's own "Struggling Financially" flow (chat to "Cora") routes here.
  **This is the likely best channel for a paper trail**, but need to confirm Rupert has app/online access
  to the mortgage under his own login (joint mortgage — may only be visible via Heather's login, TBC).
- **Phone: mortgage team 0345 300 4013.** If this ends up being the only practical route, ask on the call
  for written confirmation of anything discussed (payment flexibility, notes on file) — request they email
  or secure-message a summary afterwards.
- No dedicated divorce/hardship team or email found — RBS's "Separation and Divorce" guidance page just
  points back to the same two channels.

## Research findings so far (running log — don't lose these)

### The product is a One Account, not a conventional mortgage (8 Jul 2026 — from monthly statement)
Rupert shared the May 2026 monthly statement (photo). Key facts:
- The mortgage is a **Royal Bank One Account** — a current-account mortgage / flexible borrowing
  facility, not a conventional repayment or interest-only mortgage. There is **no fixed monthly payment
  being "demanded"**: interest is simply calculated and collected from the account each month.
- Balance at 29/05/2026: **−£310,158.25**. Interest rate May 2026: **7.10%**; May interest
  **£1,871.42**, collected 23/06/2026. Credit interest rate 0.40% (nil earned).
- **RBS's last valuation on file: £390,000** — notably below Michaels' £550k-rectified figure and even
  their £400–425k as-is figure. RBS sees equity of £79,841.75 on its own numbers.
- **Repayment guide:** planned repayment date **11/12/2031**. Planned balance £136,560.83 vs actual
  £310,158.25 → **£173,597.42 BEHIND the repayment guide**. RBS suggests budgeting £3,514.22/mo to hold
  position (£1,871.42 interest + £1,642.80 principal).
- **Implication for "up to date on all payments":** technically true (nothing demanded is unpaid — the
  guide is explicitly "simply a guide") but misleading in spirit — the account is massively behind the
  repayment plan RBS tracks, and saying "up to date" invites them to look and see the opposite. Rupert
  flagged this himself. Accurate framing: **within the facility limit, interest met in full each month**.
- **Implication for the support ask:** payment-holiday/term-extension concepts (from the earlier
  credit-file research) map poorly onto a One Account — flexibility is built into the product. The real
  levers are the **facility limit** (any step-downs scheduled before 2031?) and the **planned repayment
  date/guide**. The credit-file question stands, but the options RBS can offer will be One
  Account-specific.
- Statement photo filed in the git repo: `incoming/WhatsApp Image 2026-06-09 at 17.54.57.jpeg`.

### Redemption statement + the £390k valuation (discussed 8 Jul 2026)

**Why the redemption statement matters (beyond the routine to-do):**
- The **ERC is an unresolved unknown**: RBS confirmed to Heather (Aug 2025, phone) that a penalty
  exists, but the amount/mechanics were never captured — her relayed version was garbled. An ERC on a
  One Account is slightly unusual (flexible product; ERCs normally attach to fixed-rate deals, and 7.10%
  looks variable). The written statement should clarify what this penalty actually is.
- **ERCs usually expire.** If the ERC period ends before a 2027 sale, selling as-is early incurs it and
  waiting avoids it — a real input to the sell-now vs wait model alongside the £125–150k price gap and
  ~£4k/mo dual-housing carry. Ask for: ERC amount, how calculated, and **the date it stops applying**,
  plus all discharge/admin fees.
- Settlement maths runs on **redemption cost**, not balance — needed for consent-order accuracy.
- The statement is a ~24h snapshot; the goal now is the ERC structure/expiry, not the precise figure
  (solicitors get a fresh one at completion).

**The £390k "last valuation" on RBS's file:**
- Almost certainly an indexed/desktop figure (origination valuation rolled forward by HPI), not an
  appraisal. Nobody has inspected the house.
- Only "way out" vs the £550k-rectified figure — vs Michaels' £400–425k as-is it's accidentally close.
- **Why it matters:** on RBS's numbers LTV ≈ 80% (£310k/£390k, equity £80k) — the lens they'll use when
  assessing any support ask; makes the account look more marginal than reality.
- **Tactical option for the message:** one line quoting the professional valuation of **~£550k on
  completion of the remedial works** (Michaels, 13 Jun 2026, in writing — must be quoted as "subject to
  works completed," not current value). True, favourable, and reinforces the reassurance framing
  ("security is fine, insurer making good, sale to follow"). The thing kept OUT of the message is the
  pessimistic as-is analysis; the optimistic rectified figure works in Rupert's favour. **Not yet added
  to the draft — Rupert to decide.**
- Lender file value is irrelevant to the divorce settlement itself (that uses market valuations).

**Loose end spotted (8 Jul):** CLAUDE.md's "est. equity ~£139,000" implies a ~£450k sale price, not the
£550k Michaels figure (550 − 310 = 240). May predate Michaels or be deliberately conservative (sale
costs, ERC?) — confirm which, since it changes the "≈£56k each" headline.

### RBS "Separation and Divorce" guidance page (checked 8 Jul 2026)
- Generic guidance only — no dedicated divorce/hardship team, no special process for separating couples.
- **Changing names on the mortgage:** max 2 people on a mortgage; RBS charges an admin fee; requires own
  solicitor to do the legal work; everyone being added/removed must agree + sign. RBS's own advice:
  **wait until court proceedings/financial order are finished before applying** — consistent with the
  existing plan to hold Final Order until the consent order is sealed ([[project_final_order_timing]] in
  memory). No new action needed here, just confirms current approach.
- General joint-account advice (not mortgage-specific): can ask bank to freeze joint accounts if needed,
  but must keep shared bills/direct debits running. Possibly relevant later for the joint credit cards,
  not the mortgage.

### Credit rating impact of contacting RBS / any support arranged (checked 8 Jul 2026)
This was flagged as something Rupert wants to be very clear on before acting. Key facts:
- **Simply contacting the lender and discussing options does NOT affect the credit file.** This is
  protected under current FCA-driven forbearance rules. No downside to raising this at all, given
  payments are currently up to date.
- **If RBS agrees a formal payment holiday**, whether it's reported to credit reference agencies is
  **lender-discretion** — post-COVID rules allow (but don't require) lenders to report a payment holiday
  as arrears. RBS hasn't said either way for this mortgage; must ask explicitly before agreeing to
  anything.
- **Two options carry an explicit no-credit-file-impact guarantee** (while up to date on payments, no
  affordability assessment needed): switching to **interest-only for up to 6 months**, and **extending
  the mortgage term**.
- **CORRECTION (8 Jul 2026 — Rupert flagged):** the mortgage is **already interest-only** (RBS offset
  mortgage #11177343 — see CLAUDE.md). So the "switch to interest-only" lever is **not available** —
  already used/not applicable.
- **SECOND CORRECTION (8 Jul 2026 — on reflection):** term extension was initially proposed as "the
  protected option left," but that reasoning doesn't actually hold for this mortgage. Term extension
  reduces monthly payments on a **repayment** mortgage by spreading the *capital* portion over more years.
  On an **interest-only** mortgage the monthly payment is just interest on the outstanding balance —
  extending the term (pushing back the date the capital must be repaid) doesn't change that calculation.
  So term extension would likely be **protected from a credit-file view but close to useless financially**
  for the actual problem (monthly cost of running two households). Dropped as the headline ask.
- **Net position:** the generic "protected no-credit-impact options" list (interest-only switch, term
  extension) doesn't have a good answer for an interest-only offset mortgage. Rather than prescribing a
  specific lever we're not sure applies, **the message should ask RBS directly** what (if anything) they
  can do that would actually reduce monthly outgoings without affecting the credit file — including asking
  about anything specific to the offset structure (e.g. using the linked savings/offset balance
  differently). This wasn't covered by the general web research, which was written for standard repayment
  mortgages, not offset ones.
- **If payments are already missed**, any help given at that point DOES get recorded — another reason to
  raise this proactively now while payments are current, not to wait.
- Sources: checkmyfile.com, MoneyHelper, Financial Ombudsman Service guidance (via web search 8 Jul 2026).

**Implication for the draft message:** don't prescribe a specific lever (interest-only and term extension
both ruled out/questionable). Ask RBS open-endedly what support is available that wouldn't affect the
credit file, flag the offset structure as a specific thing to ask about, and keep the explicit ask for RBS
to confirm in writing whether any option discussed would be reported to credit reference agencies.

**Action needed before sending:** confirm whether Rupert can log into RBS Digital Banking for the joint
mortgage under his own credentials. If yes → draft below goes in as a secure message. If no → call
0345 300 4013, use the drafted content as a script, and ask for written confirmation afterwards.

## Draft message

> Subject: Mortgage 11177343 — change of circumstances (separation + subsidence claim)
>
> Hello,
>
> I'm writing regarding mortgage account 11177343 (Maple Tree House, 1 Kingsmead, Pebmarsh, Essex, CO9 2NA), held jointly with Heather Thomas. Two updates for your records, and a couple of requests.
>
> First, Heather and I have separated and are in the process of divorcing. We are currently running two households — Heather remains at the property; I am in rented accommodation — and the house will be sold as part of the financial settlement.
>
> Second, the property has an active subsidence claim with our home insurer. Liability has been accepted and the claim is progressing — mitigation works are under way, and remedial works are currently expected to complete around spring 2027. The timing of the sale is not yet decided: we may market the property once the works are complete, or sooner.
>
> The account is within its facility limit and the monthly interest is being met in full. Given the cost of running two households, please set out what, if any, support options are available to us on this account that would not affect our credit files — for example regarding the facility limit or the planned repayment date. For any option, please confirm whether it would be reported to credit reference agencies.
>
> Please also send a current redemption statement, including a breakdown of any early repayment charge — how it is calculated and the date until which it applies — and any discharge or administration fees.
>
> Happy to provide further detail if needed.
>
> Regards,
> [Rupert's name / contact details]

**Notes on the draft:**
- **Tone (8 Jul — Rupert's direction):** polite but perfunctory/businesslike. No "I wanted to update
  you" / "I wanted to ask" framing — state the facts, make the requests directly ("please could you set
  out…", "please confirm…", "please also send…"). Keep this register in any future revision.
- **Sale timing kept OPEN (8 Jul — Rupert's correction):** an earlier draft said "we plan to market the
  property once the claim and repairs are concluded." That decision has NOT been made — waiting for
  repairs is the likely outcome (per Michaels' steer) but Rupert still considers selling as-is a live
  option (cash settlement could shorten the wait). The message now says timing is "not yet decided: once
  works are complete, or sooner." Don't present the wait-for-repairs path to anyone as settled.
- **Subsidence paragraph deliberately reframed (8 Jul review — Rupert flagged the original as an
  overstretch):** the first draft told RBS "lenders won't lend against a property with an active claim,
  so realistically we're looking at cash buyers only." Cut for three reasons: (1) it's Aaron Wilcock's
  estate-agent opinion generalized into a flat fact — Michaels said "extremely difficult," not
  impossible, and lendability on an accepted claim with scheduled works varies by lender; (2) **wrong
  audience** — it tells RBS, who hold this property as security against £309.7k, that their security is
  currently near-unsellable at £400–425k. Handing the mortgagee our worst-case internal analysis while
  asking for a favour invites them to reassess their own risk position (audience-awareness rule).
  (3) unnecessary — all RBS needs is: claim accepted, progressing, works done ~spring 2027, sale timing
  under review. The reframe also leads with "claim progressing" — reassurance framing, since the insurer
  making good the damage *protects* RBS's security. Keep the Michaels £400–425k analysis internal.
- Doesn't prescribe interest-only switch or term extension — both ruled out/questionable for this
  product (see corrections above, and the One Account findings — flexibility is built in; the real levers
  are the facility limit and the planned repayment date, which is what the draft now asks about).
- Explicitly asks RBS to confirm credit-file impact **before** anything is agreed — this was Rupert's
  specific ask (8 Jul 2026) to be clear-eyed about this before acting.
- **"Up to date on all payments" replaced (8 Jul — Rupert flagged):** the One Account has no demanded
  monthly payment — interest is auto-collected and the account is £173.6k behind RBS's repayment guide,
  so "up to date" was technically true but misleading in spirit and easily contradicted by their own
  records. Now says: "within its facility limit and the monthly interest is being met in full" —
  accurate, verifiable, and still establishes the not-in-arrears position that matters for forbearance.
- Includes the redemption-statement request from the existing to-do (fresh RBS redemption figure) so it
  rides along with this contact rather than needing a separate one.
- Keep tone factual/neutral — this is Rupert's own communication with a shared lender, not adversarial to
  Heather.

## Still to decide / do

- Confirm channel (Digital Banking secure message vs phone) — check Rupert's online banking access.
- Check the One Account T&Cs: (1) do they **require** notifying RBS of material damage to the property
  (subsidence)? If so, this notification is an obligation being met proactively, not just courtesy.
  (2) Does the **facility limit step down** between now and the planned repayment date (11/12/2031)? A
  scheduled step-down is the one thing that could turn "behind the guide" into a real problem — worth
  knowing before the conversation.
- Decide how much subsidence detail to include (claim ref? insurer name?) vs keeping it high-level.
- Decide whether to explicitly ask about payment holiday/flexibility by name, or leave it open as above.
- Send, then log RBS's response here and update `Divorce.md` to-do list.

## Related
- [[House Sale]]
- [[Subsidence Claim]]
