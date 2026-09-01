# Starling — scheduled payment to Tesco Credit Card space failed

**Date:** 2026-08-10
**From:** donotreply@starlingbank.com
**To:** rupert@pebmarsh.com
**Account:** Starling - Main → Starling - Tesco Credit Card (space)

Starling flagged that a scheduled internal payment of £74.43 from the main
personal account into the "Tesco Credit Card" Space failed on the morning
of 10 Aug 2026 due to insufficient funds in the main account — Starling
said it would keep retrying until 4pm that day.

**Explained by Rupert (11 Aug):** an unplanned purchase landed on the Tesco
Clubcard (cashflow-driven, not intentional use of the card). He made a
manual one-off payment of £90.13 — the *pending* balance shown to him at
the time — not realising Tesco's own automated collection would separately
try to take the *actual* statement balance too. That automated collection
is what generated this £74.43 Starling transfer; it failed in Starling
that morning (insufficient funds, having just been spent on the manual
payment), but a retry evidently succeeded later the same day, since the
£74.43 landed on the card on 9 Aug regardless. By then the card only
actually owed £25.97 (the new purchase), so the £74.43 collection overpaid
it by £48.46 — Tesco Mastercard now sits at **£48.46 in credit**, not a
clean £0 (see [[Tesco Clubcard Credit Card]] for the full
transaction-by-transaction reconciliation; an earlier read of this as
£25.97 in credit was wrong — mixed up the order of two same-day Banktivity
entries). Nothing further to chase; the "pickle" was a timing collision
between two payments for the same balance, not a missed payment.
