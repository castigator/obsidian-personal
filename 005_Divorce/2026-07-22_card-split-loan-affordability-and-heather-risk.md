---
tags: [divorce]
---

# Card-split loan: affordability breakdown and risk if Heather doesn't confirm

Full working from a 22 Jul 2026 session run in the sibling `finance` project
(loan calculator walkthrough), captured here per [[feedback_capture_analysis]]
since it bears directly on [[Card Split Agreement]] and the consolidation
loan referenced in [[Debts]].

## Question

Rupert is comparing lenders/terms for the £7,500 loan intended to fund his
side of the proposed card split (taking on the Barclaycard, £7,283, in
exchange for Heather keeping Halifax + Ann's Barclaycard, £7,222 — see
[[Card Split Agreement]]). Two linked questions came up:

1. Which lender/term is actually the better choice, once you look past the
   headline "100% pre-approved" figures?
2. If the loan is drawn and the card split then falls through (Heather's
   buy-in is uncertain as of 22 Jul — she initially agreed but is "not 100%
   behind it anymore"), what does that actually cost/expose Rupert to?

## What was reviewed

- MoneySavingExpert Credit Club loan eligibility checker (TransUnion-powered
  soft search), run at both 2-year and 3-year terms
- MoneySavingExpert Credit Club full TransUnion credit report (borrowing
  summary + "All accounts" view, both Open and Closed) — pulled to check
  whether the existing Tesco Loan and RBS mortgage were visible to lenders
- Halifax's product detail panel (eligibility criteria, positive/negative
  product features)
- Finance project's own affordability figures (`monthly-contributions.md`,
  `personal-debt-interest-strategy.md`, `solicitor-payment-0pc-plan.md`)
- The existing precondition already on record in this project: **the loan
  must not be drawn until the Card Split Agreement is signed**, and must
  complete before the RBS mortgage notification letter is sent

## Key findings

### 1. Lender/term comparison

| Lender | Term | APR | Monthly | Total interest |
|---|---|---:|---:|---:|
| Tesco (Clubcard rate) | 2yr | 6% | £331.87 | £464.88 |
| Tesco (standard, no Clubcard) | 2yr | 6.4% | £333.15 | £495.60 |
| Halifax | 2yr | 6.4% | £333.15 | £495.60 |
| Tesco (Clubcard rate) | 3yr | 6% | £227.62 | £694.32 |
| Halifax | 3yr | 6.4% | £228.91 | £740.76 |
| NatWest (earlier quote, ~16 Jul) | 2yr | 6.9% | £334.74 | £533.76 |

Tesco's headline rate is only better than Halifax's **if** you enter a
Clubcard number to get the discounted rate — without it, Tesco's 2yr
figures are identical to Halifax's (6.4%, £333.15, £495.60). Entering the
Clubcard number ties the application directly to Rupert's existing Tesco
relationship at the point of applying.

### 2. Rupert already has an active Tesco Loan (£3,000, ~£2,021.82
outstanding, £139.74/mo) — but it does not appear on his TransUnion credit
file at all, open or closed. Neither does the RBS mortgage. Checked the
full "All accounts" view (not just the summary), both Open and Closed tabs
— genuinely absent, not a display/filtering artefact. Likely explanation:
Tesco Bank and RBS may simply not report to TransUnion specifically (UK
lenders don't always report to all three bureaus), rather than anything
being wrong with either account.

**Why this matters:** the "100% Pre-Approved" figure from the eligibility
tool is generated from this same (incomplete) TransUnion data. It does not
mean Tesco Bank's own internal underwriting — which absolutely does know
about its own existing loan to Rupert, regardless of what any credit
bureau shows — will reach the same conclusion. The tool's small print
("subject to ID, fraud and verification checks") plausibly covers exactly
this kind of internal exposure check. **Recommendation: Halifax is the
safer choice** specifically because there's no existing lending
relationship to complicate their internal decision — its rate is no worse
than Tesco's non-Clubcard rate, so there's no real cost to preferring it.

### 3. Halifax's early repayment fee

Product detail panel shows: **"An early repayment fee will apply if the
loan is paid off in full."** Overpayments (partial) are allowed free of
charge — it's specifically full early closure that costs. This matters
for two things:
- The general assumption that this loan could be cleared "for free" once
  the house sells (via the statutory right to early settlement with an
  interest rebate) isn't quite right — the rebate typically offsets most
  of the fee, but it isn't literally costless. Get the actual fee figure
  from Halifax's T&Cs before relying on this.
- If the card split falls through and Rupert wanted to simply unwind the
  loan (repay it immediately, having no further use for it), that undo
  also isn't free.

### 4. Combined monthly affordability, both scenarios

Baseline monthly costs common to both scenarios (net salary £6,109/mo):
Pebmarsh mortgage share £1,497.14, Pebmarsh scheduled transactions
£575.75, Lucy food £200, Westgate rent (Rupert's half) £500, NatWest card
DD £300, Tesco Clubcard DD £150, Tesco Loan £139.74. (Cats' £65/mo drops
end of Jul 2026 either way, excluded above.)

| | Split + solicitor plan both go ahead | Split falls through, loan already drawn |
|---|---:|---:|
| Shared debt servicing (existing, 80% share) | — (cleared by loan) | £363.72 (still running) |
| New Halifax loan (2yr) | £333.15 | £333.15 |
| M&S DD (solicitor 0% plan) | £175.00 | £175.00 |
| **Total monthly commitments** | **£3,870.78** | **£4,234.50** |
| **Headroom** | **~£2,238.22** | **~£1,874.50** |

Neither scenario is tight — even the worst case leaves ~£1,875/month
headroom. But the *shape* of the risk is real: if the loan is drawn and
the split doesn't happen, Rupert isn't saving the £363.72/month shared
debt servicing anymore, he's paying it **in addition to** the new loan —
effectively double-servicing, ~£697/month between the two, for as long as
it stays unresolved.

## The "what if Heather backs out" question, answered directly

The loan is a contract between Rupert and the lender — completely
independent of whatever he and Heather agree or don't agree on the card
split. If she pulls out, **Rupert still owes the full £7,500 + interest
regardless.** He'd have £7,500 in cash with no card left to apply it to
(the whole point was to pay off the Barclaycard, which requires her
cooperation/agreement to actually count for anything in the settlement).

Realistic fallback uses for stranded funds, if this happens:
- **Pay off the Tesco Loan early** — clears a genuinely-owned personal
  debt (9.8%, not shared), frees £139.74/month. Clean, no ambiguity.
- **Pay the Barclaycard down anyway, unilaterally**, even without
  Heather's sign-off — but this carries a **settlement risk, not just a
  cashflow one**: without a formally agreed recital, it's unclear whether
  this payment would count toward Rupert's 50% share when the consent
  order is eventually calculated, versus reading as a unilateral gift to
  the marital pot that Heather isn't obliged to reciprocate for. **This is
  a question for Alan (solicitor), not resolvable from the finance side.**
- Least good option: park it as an idle buffer, paying loan interest for
  no offsetting benefit.

## The existing precondition, and the tension with what Rupert is now
considering

This project's own prior notes already establish: **the loan must not be
drawn until the Card Split Agreement is signed**, and it must complete
before the RBS mortgage notification letter is sent (RBS = NatWest Group;
drawing new debt within the same banking group right before flagging
mortgage-side hardship is the risk being managed there).

As of this session, Rupert was leaning toward drawing the loan first
("get the loan sorted... then sort the solicitor") specifically because he
wants it in hand before the solicitor-fee balance-transfer plan proceeds.
**This does not conflict with the RBS-letter sequencing** — the
consolidation loan (Halifax/Tesco) and the solicitor-fee financing
(NatWest purchase + M&S balance transfer) are unrelated products, no
overlap there. But it **does directly reopen the risk the
sign-before-drawing precondition exists to avoid**, given Heather's
confirmed uncertainty about the split as of 22 Jul.

## Recommendation

1. **Lender: Halifax over Tesco**, given the existing Tesco relationship
   risk and Halifax offering an identical rate to Tesco's non-Clubcard
   tier anyway.
2. **Term: 3 years preferred over 2**, per Rupert's own stated preference
   for lower monthly pressure — reasonable given the house sale is
   unlikely to complete before either term ends anyway, so term length
   mostly sets the interim monthly commitment rather than the real payoff
   date.
3. **Timing: hold off drawing the loan until Heather actually confirms**
   the card split, consistent with the existing precondition — the
   downside of waiting is delay; the downside of not waiting is a real,
   quantified double-servicing cost (~£364/month) plus an early-repayment
   fee if Rupert wants to unwind it. Worth an explicit, current
   conversation with Heather (or via Alan) to get a real answer rather
   than proceeding on an assumption either way.

## Related analysis
- [[Card Split Agreement]]
- [[Debts]]
- [[Clean Break]]
