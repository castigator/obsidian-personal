# Starling — scheduled payment out of Tesco Credit Card Space failed

**Date:** 2026-08-19
**From:** donotreply@starlingbank.com
**To:** rupert@pebmarsh.com
**Account:** Starling - Tesco Credit Card (space)

Starling flagged that a scheduled payment of £74.43 out of the "Tesco Credit
Card" Space failed on the morning of 19 Aug 2026 due to insufficient funds
in the Space — Starling said it would keep retrying until 4pm that day.

**Context:** this is a different incident from the 10 Aug failure
([[2026-08-10_starling-scheduled-payment-failed]]), which was resolved
same-day. Banktivity shows the Space itself went to **-£74.43 on 17 Aug**
(see [[Accounts]]) — i.e. it's already overdrawn by exactly this
amount, which is why the 19 Aug attempt to take another £74.43 out of it
had nothing to pull from. Two £74.43 debits in three days out of a Space
that's meant to sit at/near £0 between sweeps suggests either a duplicated
standing arrangement or the Space just isn't being topped up before its
scheduled payment date. Needs Rupert to check the Starling app for what's
actually configured on this Space (recurring transfer in from Starling -
Main, and the scheduled payment out to Tesco) — not something inferable
from Banktivity alone.
