# Strategy: managing personal cards + Tesco Loan to avoid interest

Covers Rupert's own four cards and the Tesco Loan — not the shared debt
with Heather/Ann (see [[Paying Off 50% Shared Debt]] for that). As of
2026-07-20.

## Snapshot

| | Balance | Limit | Standard APR | Current promo | DD in place? | Next key date |
|---|---:|---:|---:|---|---|---|
| NatWest Mastercard (…0354) | -£1,420.56 | £10,000 | 26.436% | 0% intro BT, whole balance, expires **16 Feb 2027** | Yes, £300/month | Balance projected clear ~Dec 2026 |
| Tesco Clubcard (…2484) | -£74.43 | £1,500 | ~39.94% (2.840%/mo) | 0% BT available, transfer window closes 7 Aug 2026 | Yes, £150/month fixed | Payment due 9 Aug 2026 |
| M&S Mastercard (…0265) | £0.00 | £2,000 | 24.9% purchases / 29.9% cash | 0% BT for 12mo, window closes **31 Jul 2026** | Yes | Offer window closes 31 Jul 2026 |
| Capital One (…7498) | £0.00 | £1,800 | 30.340% (all types) | none current | Yes | — |
| Tesco Loan | -£2,021.82 | n/a (fixed sum) | 9.8% fixed, £139.74/mo | n/a | Yes (repayment schedule) | Matures ~Aug 2027 |

## Current interest being paid: effectively none

- NatWest: 0% (whole balance on the intro promo)
- Tesco Clubcard: £0 this cycle — balance tiny and within interest-free window
- M&S / Capital One: £0 balance, nothing to charge interest on
- Tesco Loan: 9.8% fixed is baked into the amortising schedule — not a
  "risk", just the known cost of that loan

So there's no live interest bleed to fix. The job is **defensive**: don't
let any of this drift into a state where interest starts.

## Risk calendar

1. **31 Jul 2026** — M&S 0% BT offer window closes. Recurring monthly
   (last three notices: Jul, Mar, and earlier — see [[Correspondence Log]]), so
   likely to reappear, but don't assume it will on the same terms.
2. **7 Aug 2026** — Tesco 0% BT transfer window closes (also recurring monthly).
3. **9 Aug 2026** — Tesco Clubcard payment due. Covered automatically by
   the £150 fixed DD against a £74.43 balance — no action needed unless
   spending on the card increases materially before then.
4. **16 Feb 2027** — NatWest 0% intro promo expires. At the current
   £300/month DD, the £1,420.56 balance clears in 5 payments (~Dec 2026),
   leaving a ~2 month buffer. **This is the one deadline worth actively
   monitoring** — if new spending gets added to this card, or the DD ever
   gets missed/reduced, that buffer shrinks fast and the balance would
   revert to 26.436%.

## Priorities, ranked

1. **Keep the NatWest £300/month DD running untouched** and re-check the
   balance each `/refresh` — it's the only account with real debt and a
   hard deadline. Don't add new spending to this card while the promo
   balance is being cleared.
2. **Tesco Clubcard, M&S, and Capital One — no action.** Balances are
   effectively zero and DDs are confirmed in place on all three. Capital
   One carries this project's highest standard rate (30.34%), so if a
   balance ever does land there, it's the one to clear fastest.
3. **Tesco Loan — leave as scheduled, don't rush to overpay.** At 9.8%
   fixed it's the cheapest debt by far (cheaper than every card's standard
   rate). Overpaying it wouldn't reduce risk, since the rate can't change
   — it's only worth doing if you just want the loan gone sooner for its
   own sake (freeing up the £139.74/month), not to dodge interest.
   Confirmed: overpayments are allowed and Tesco shortens the **term**
   rather than reducing the monthly payment. Early settlement is also
   allowed but requires requesting a settlement estimate from Tesco first
   (no fixed self-serve payoff figure) — consistent with the CCA 1974
   statutory right to early settlement with an interest rebate. See
   [[Tesco Loan]].

## On acquiring new finance

Right now there's no personal-card debt that actually needs restructuring
— everything's either 0% or £0. The two live 0% balance-transfer windows
(M&S, closing 31 Jul; Tesco, closing 7 Aug) are otherwise-idle capacity:
if a need for cash or debt consolidation comes up before those dates
(e.g. absorbing some of the shared debt, per
[[Paying Off 50% Shared Debt]]), they're sitting there ready to use —
but there's no standing reason to draw on them pre-emptively for these
four accounts as they are today. Re-evaluate this each `/refresh` since
the picture (balances, offer windows) changes monthly.

## How the balance transfer windows actually work

The "window closes" date on each offer (31 Jul for M&S, 7 Aug for Tesco)
is the deadline to **request** the transfer — it is not when the 0% period
itself ends, and transferring right up against the deadline does not tip
you straight into interest. What happens after that depends on how each
offer is structured, and the two currently on offer work differently:

- **M&S — duration-based:** "0% for 12 months" counts from the date of
  the transfer, not from the window closing. Transfer on the last day of
  the window (30/31 Jul) and you still get the full 12 months, running to
  roughly the same date in 2027.
- **Tesco — fixed-end-date based:** "0% until your October 2027 statement"
  is a fixed calendar cutoff, not a rolling period from the transfer date.
  Per the current notice, transferring on day 1 of the window or on the
  last day (7 Aug) lands on the same October 2027 cutoff either way.

So in neither case does hitting the deadline day create a sudden jump to
interest — the fee (see below) is charged regardless of timing, but the
0% clock is governed by the offer's own terms, not the request deadline.
Two caveats: (1) transfers aren't instant, so leave a few working days'
buffer before a deadline rather than submitting on the day itself, and
(2) offer structures can change between notices — re-check the wording
each time before relying on this.

## 0% balance transfer capacity available before 31 Jul 2026

Both current offers (M&S and Tesco) are open before 31 Jul, so this is
the combined headroom across both cards, capped so that transfer + fee
doesn't exceed available credit:

| Card | Available credit | Fee | Max transfer (fee included in limit) | Fee cost at max |
|---|---:|---:|---:|---:|
| M&S (…0265) | £2,000.00 | 3.49% | **£1,932.55** | £67.45 |
| Tesco Clubcard (…2484) | £1,425.57 | 4.99% | **£1,357.82** | £67.75 |
| **Combined** | | | **£3,290.37** | £135.20 |

That's the ceiling — maxing out both cards would use their full available
credit and leave no room in either for the transfer fee itself, let alone
any headroom for spending. A more comfortable working figure would leave
some buffer on each card rather than transferring right up to the limit.
