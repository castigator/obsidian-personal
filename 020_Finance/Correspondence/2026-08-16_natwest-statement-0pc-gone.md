# 2026-08-16 — NatWest statement: the 0% balance is gone, whole balance at 26.436%

**Statement:** [[2026-08-16_natwest-0354-statement.pdf]] (card ending 0354,
period 17 July – 16 August 2026) · **Discovered:** 17 September 2026 during
`/refresh`, after a £52.55 interest charge appeared in Banktivity

## What the statement says

**SUMMARY OF BALANCES** — the decisive section:

| Balance | Monthly rate | Annual rate | Outstanding |
|---|---|---|---|
| Purchases | 2.203% | **26.436%** | **£1,502.56** |
| Money Advances | 2.203% | 26.436% | £0.00 |

There is **no 0% promotional row at all**. The entire balance is classified
as *Purchases* at the full 26.436%.

The statement also warned, in plain text on page 1: *"If you make the minimum
payment of £15.03 and it reaches us on the due date of 10 September 2026 your
estimated interest payment next month is **£53.99**."* Banktivity duly shows
**-£52.55 INTEREST** posted 15 Sept 2026 (slightly under the estimate because
£300 was paid, not the £15.03 minimum).

## Why it happened — read directly off the transaction list

The statement's own ledger for the period shows the sequence:

```
BALANCE FROM PREVIOUS STATEMENT              £1,420.56   (the 0% BT balance)
28 JUL  FASTER PAYMENT RECEIVED           -  £1,900.00   (the M&S transfer)
        Sub-Total                            £479.44 CR
28 JUL  ATKINS DELLOW BURY ST EDMUN        + £1,982.00   (solicitor fee)
NEW BALANCE                                  £1,502.56
```

The £1,900 transferred from M&S **paid off the protected 0% balance
outright**, taking the account £479.44 into credit. The £1,982 solicitor
charge then landed as **entirely new purchase debt** at the standard rate.

So the [[Solicitor Payment 0% Plan]] did not go as recorded. That note says
the result was "£1,420.56 0% BT + £82.00 unprotected", with the £82 expected
to clear itself "at the cost of roughly £1–2 in interest". In reality
**100% of the balance is unprotected**, and the cost is **~£52–54 per
month**, not £1–2. The plan moved the money in the wrong direction: it used
the M&S 0% capacity to repay a balance that was *already* at 0%, while the
genuinely expensive new borrowing stayed on NatWest.

## This was visible a month earlier and was missed

The statement was issued 16 Aug and downloaded to `~/Downloads` on 17 Aug.
The 17 Aug `/refresh` saw only NatWest's *email* — "statement ready", no
figures — and logged it as "not worth its own entry". The figures were in the
attached PDF, not the email. **Lesson: a "statement ready" notice with no
figures is not the same as a statement with no news** — for any card with an
active plan or promotional balance riding on it, the statement itself needs
opening. See [[Correspondence Log]].

## What it costs and the way out

Balance is **-£1,255.11** (15 Sept, after the interest). At £300/month it
clears in roughly five payments, but accrues interest at ~26.4% throughout.

**The Tesco Clubcard 0% balance-transfer offer fits this almost exactly** —
0% until the Dec 2027 statement, 4.99% fee, ~£1,500 available credit, and a
**transfer window closing 9 October 2026**. Moving ~£1,255 across would cost
roughly **£63 in fee** against a standard rate of 26.436%. See
[[0% Offers Tracker]] and [[Tesco Clubcard Credit Card]]. Rupert's decision —
flagged, not actioned.
