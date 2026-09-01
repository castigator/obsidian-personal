# Tesco Clubcard Credit Card

- **Type:** Credit card (Tesco Bank, Mastercard)
- **Card number:** **** **** **** 2484
- **Credit limit:** £1,500.00
- **Balance:** **-£25.97** (as of 2026-08-19, Banktivity)
- **Available credit:** ~£1,474.03
- **Standard purchase rate:** 2.840% monthly (≈39.94% representative APR,
  compounded) — per statement dated 15 July 2026
  (`~/Downloads/CCStatements-260715.pdf`). £0 interest charged this cycle
  as the balance is within the interest-free purchase window.

**Brief detour into credit, now unwound (Aug 2026):** the prior -£90.13
balance was cleared by a manual payment of £90.13 on 8 Aug. A new,
unplanned purchase then put -£25.97 back on the card (9 Aug). Tesco's
automated Direct Debit then collected £74.43 anyway — the same collection
that generated the *failed* Starling transfer on 10 Aug (see
[[2026-08-10_starling-scheduled-payment-failed]];
Starling's side failed that morning but a retry evidently succeeded, since
the £74.43 landed on the card the same day). £74.43 against £25.97 actually
owed overpaid the card by £48.46, putting it briefly in credit (confirmed
£48.46, cross-checked against the sum of every transaction on the account
at that point). **Tesco then clawed the £74.43 back out on 10 Aug**
(a distinct dated transaction, not a same-day ordering ambiguity),
returning the balance to **-£25.97** — exactly what was actually owed from
the 9 Aug purchase. Net effect: the manual £90.13 payment and the automated
£74.43 DD collision resolved itself without any action needed — not a
missed payment, and not money actually "paid back" by Tesco so much as
Tesco correcting its own over-collection.

**Update (20 Aug refresh):** the £74.43 clawback described above wasn't
final — a fresh £74.43 landed on the card again on 18 Aug, putting it back
into **£48.46 credit**, this time via `Starling - Tesco Credit Card` (the
Space had gone to -£74.43 on 17 Aug, then cleared to £0 as this posted).
See [[2026-08-19_starling-scheduled-payment-failed-tesco-space]]
for the Starling-side failed-payment email that appears to be the same
episode settling out.

**Update (21 Aug refresh) — it happened again, exact same shape.** The
£74.43 was clawed back a second time on 19 Aug, returning the card to
**-£25.97**. That's now a *third* £74.43 in/out cycle on this card
(9 Aug in → 10 Aug clawed back; 18 Aug in → 19 Aug clawed back), each time
netting back to the same -£25.97. This looks less like a one-off timing
collision and more like a genuinely recurring collection/reversal pattern
(possibly Tesco's DD retrying against the Starling Space each time it's
topped up, then reversing when Tesco reconciles the actual balance owed).
Not costing Rupert anything net, but worth him being aware it may keep
recurring rather than being resolved.

## Money transfer option

Tesco Bank offers money transfers from this card to a UK current account:
- **Rate:** standard interest rates apply (no promo rate — rate not yet captured)
- **Fee:** 3.99% of amount transferred
- **Limit:** up to 95% of available credit (~£1,354 currently)
- Funds within 2 working days if approved; no credit-file footprint from the check

Note: at standard rates this is expensive borrowing — only relevant as an
emergency cash option, not part of any 0% strategy.

## Balance transfer offer (recurring)

- **Rate:** 0% interest on balance transfers until November 2027 statement
- **Fee:** 4.99% (min £5)
- **Transfer window:** until 4 September 2026 (per most recent notice)
- **Source:** recurring monthly email from Tesco Bank, most recently
  2026-08-11 (see [[2026-07-20_tesco-balance-transfer-offer]]
  for the prior instance — terms just roll forward monthly, no new entry filed)
- Moves debt *onto* this card from elsewhere — doesn't produce cash. See
  [[Paying Off 50% Shared Debt]] for why this isn't usable for
  the shared debt right now.
