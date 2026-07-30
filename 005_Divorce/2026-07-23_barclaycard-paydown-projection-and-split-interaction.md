---
tags: [divorce]
---

# Barclaycard minimum-payment projection, and why faster paydown ≠ free headroom

Captured per [[feedback_capture_analysis]] — worked through in the sibling
`finance` project, but the substance (card-split dynamics) belongs here.

## The projection

Assuming minimum-only payments and zero new spending, using the disclosed
20.68% simple rate (1.7233%/month) and Barclaycard's own minimum formula
(interest for the period + 1% of the remaining balance):

| Statement (approx.) | Balance | Minimum payment |
|---|---:|---:|
| 20 Jul 2026 (actual) | £7,274.24 | £203.83 |
| ~20 Aug 2026 | £7,192.26 | £192.55 |
| ~20 Sep 2026 | £7,120.34 | £190.63 |
| ~20 Oct 2026 | £7,049.13 | £188.72 |
| ~20 Nov 2026 | £6,978.64 | £186.83 |
| ~20 Dec 2026 | £6,908.86 | £184.97 |

Over ~6 months: balance falls ~£434 (to ~£6,839.77), against ~£1,147.53
paid in, of which ~£713 (>60%) is interest. Confirmed the balance is
already trending down on its own (last actual cycle: £7,482.70 →
£7,274.24, a £208.46 fall), so no urgent need to intervene just to stop
it climbing.

Mechanics for overpaying if ever wanted: bank transfer, sort code
20-04-15, account 38290008, card number as payment reference — works
without being the named account holder.

## The correction that matters more than the numbers

Initial framing (wrong): "if this card's balance falls faster before the
loan/split executes, that's free headroom — you'd need to borrow less to
clear it."

**Rupert's correction (23 Jul 2026):** that's naive in isolation. The
actual goal of the proposed split is an even 50/50 of the *whole* debt
pool (Barclaycard to Rupert, Halifax + Ann's card to Heather — see
[[Debts]]). If the Barclaycard shrinks faster than Heather's side, that
doesn't hand Rupert spare headroom — it just distorts the split, and
could mean he ends up needing to absorb *more* overall to keep the
allocation genuinely even, not less. The only scenario where extra
paydown genuinely benefits Rupert is if it's **matched pound-for-pound by
Heather** on her side — otherwise it's a wash or worse for him.

**Explicit condition, not yet decided:** Rupert will not put his own extra
money into this card unless it's matched by equivalent extra payment from
Heather. That's a live, separate decision — not something to assume has
happened or will happen.

## Don't lose sight of, going forward

Rupert's own framing of the actual goals underneath all of this (stated
directly, 23 Jul 2026) — keep these as the test for any future
card-split/loan/paydown reasoning:

1. **Find a sensible way to separate himself from Heather financially** —
   gain control, get out from under joint liabilities.
2. **Minimise the total cost of doing so** — not just "pay down debt
   faster" as a goal in itself, disconnected from whether it actually
   serves (1) or reduces overall cost.

## Related
- [[Debts]]
- [[2026-07-22_card-split-loan-affordability-and-heather-risk]]
- [[2026-07-23_message-to-heather-review-cards-and-drains]]
