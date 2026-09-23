## Account Catalogue

Master index of everything tracked, built from `data/rupert-copy.bank8`  
(Banktivity export, lives in the `finance` git repo, not Obsidian) cross-checked against the  
per-account notes below. Query it with the git repo's `scripts/query-balances.sh` (documents the  
schema gotchas — account names live on `ZACCOUNT.ZPNAME`, balances/amounts on `ZLINEITEM`, not  
`ZTRANSACTION`). Balances below are the latest running balance in Banktivity as of the date  
shown — where Rupert isn't the accountholder (Heather's and Ann's cards), Banktivity is only as  
current as the last time a transaction was entered by hand, so treat those as potentially stale  
and prefer the figure in [[Shared Debt]] / [[Loans from Anne]] if more recent.

### Current Accounts

| Account | Balance | As of |
|---|---:|---|
| Starling - Main | £162.97 | 2026-09-21 |
| Starling - Joint | £184.50 | 2026-09-21 |
| Barclays - Current | £32.65 ⚠️ | 2026-09-20 |

**Starling account identification (confirmed 17 Sept 2026).** Starling uses
a single sort code across its personal accounts, so the account *number* is
what distinguishes them — easy to get wrong:

| Account | Sort code | Account number | Confirmed by |
|---|---|---|---|
| `Starling - Main` | 60-83-71 | **29495288** | Two independent sources: the [[Tesco Loan]] agreement pack (repayments taken from 60-83-71 / 29495288) and Capital One's Direct Debit panel (60-83-71 / ****5288) |
| `Starling - Joint` | 60-83-71 | **13428283** | Stored on the account record in Banktivity |

`Starling - Main` is the workhorse: it funds the Tesco Loan (£139.74/mo),
the Capital One DD mandate (fixed £100/mo, dormant while that card sits at
£0), and the bill-pot Spaces. Don't assume a 60-83-71 reference means the
joint account — check the account number.

**✅ Daybreak Hotels £50 pending hold — resolved 12 Aug 2026.** Rupert paid  
£60 to Daybreak Hotels a while back; Daybreak also put a £50 provisional  
card authorisation (pending, not settled) on `Starling - Main` at the same  
time, which showed in the Starling app's live balance but never appeared  
in Banktivity (Banktivity only reflects settled transactions) — the gap  
had consistently read £50 for several refreshes. Confirmed by Rupert on  
12 Aug (the believed 30-day card-scheme cutoff) that the Starling app  
balance and Banktivity's `Starling - Main` figure now equate — the hold  
has dropped off. No further action; no £50 to chase.

**Starling - Main jump (26–27 Aug 2026):** £6,080.83 credit on 26 Aug  
labelled "P751 00111041" (looks like salary), plus two £100 transfers in  
from Starling - Spare Funds, against ordinary spending both days — accounts  
for the balance moving from £69.45 to £6,112.12. Starling - Joint and  
Barclays - Current moves over the same window are ordinary spending only.

**27–31 Aug 2026:** all three accounts moved on ordinary spending only —  
Starling - Main £6,112.12→£6,345.92, Starling - Joint £117.47→£65.44  
(includes a £114.90 BGC from Heather on the Barclays side too, see below),  
Barclays - Current £490.15→£425.05 (includes two Heather-labelled BGCs —  
"Heather Thomas DEBT" £114.90 on 27 Aug and "Heather Thomas BILLS" £57.50  
on 25 Aug — plus routine spending, no shared-debt/settlement significance  
flagged in the divorce project for these).

**1 Sept 2026 — month-rollover sweep, all identified/ordinary.** Starling -  
Main dropped £6,345.92→£1,744.95 on the usual 1st-of-month outflow: the  
recurring mortgage-labelled transfer to Heather (£1,592.62, "Heather  
Thomas" — this label/pattern recurs monthly, amount varies ~£1,350–1,600,  
consistent with the ~£1,497/month mortgage liability in  
[[Monthly Contributions]]), £200 to Lucy (food contribution), £1,000 to  
Starling - Westgate Rent, £333 to Starling - Spare Funds, and smaller  
sweeps into the bill-pot Spaces (Council Tax £152, Broadband £32.99, TV  
Licence £15.51, Home Insurance £5.30) — plus £459.58 and £230.02 moved to  
Barclays - Current (Rupert's own transfer between his accounts, accounts  
for that account's £425.05→£1,114.65 jump). Starling - Joint's balance is  
unchanged (£65.44) despite passing £130 through it — see the HealthSpa  
transfer-chain note below. Small further Starling - Main spend on 1 Sept
(Budgens, Journey official, Swan Long Melford) took it down to £1,641.87.

**2 Sept 2026 — Barclays - Current, routine monthly debt-servicing
payments.** £1,114.65→£540.17: two payments to "Barclaycard" (£200 +
£196.50) and one to "Halifax" (£177.98) — this is Rupert's recurring
monthly contribution toward Heather's Barclaycard/Halifax minimums (same
pattern every month since at least Mar 2026, see [[Shared Debt]] /
[[Monthly Contributions]] for the servicing-split context). Halifax's
£177.98 this month is higher than the usual ~£62–70 — worth a passing
flag, but nothing in the divorce cross-check suggests a change to the
servicing split, so treating as ordinary unless it recurs. Confirmed via
a routine Halifax "Payment received" notice, no new figures.

**2–3 Sept 2026 — all three accounts, ordinary spending/transfers only.**
Starling - Main £1,641.87→£1,455.14 (pub spending, a £100 transfer to
Mandy/Rupert shared costs, East of England Coop, plus several small
card-spend line items late on 3 Sept — £15.20/£13.60/£12.90/£4.90 —
picked up by this refresh, not yet posted when the prior refresh ran).
Starling - Joint £65.44→£196.55 (two £100 credits in — "Mandy Zimmer &
Rupert Thomas" and "Shopping" — against a £68.89 Tesco debit). Barclays -
Current £540.17→£473.22 (£66.95 Home Insurance direct debit, same
recurring amount as the 3 Aug DD). Nothing irregular.

**3–4 Sept 2026:** no further movement — all three current accounts
unchanged (Banktivity has no new line items since 3 Sept).

**3–6 Sept 2026 — Starling - Main, ordinary spending only.**
£1,455.14→£978.61: pubs/restaurants (Five Bells Cavendish, The Black
Lion, Swan Long Melford), East of England Coop, Amazon Marketplace ×2,
PayPal ×2, Audible and Anthropic subscriptions, a £100 transfer to Mandy
("Mandy Zimmer & Rupert Thomas"), and a £175 payment to "Hsbc Uk Bank T/a
M&s Bank" (the M&S card's usual fixed DD landing — confirms
[[M&S Credit Card]]'s balance moving -£1,966.31→-£1,791.31 same day) and
a £72.84 Fuse Energy payment (household energy supplier), plus further
small pub/grocery spend on 6 Sept (Budgens, Five Bells Cavendish ×2).
Nothing irregular, no shared-debt significance.

**6–7 Sept 2026 — Starling - Joint, ordinary spending.** £196.55→£166.05:
a single -£30.50 Tesco debit on 7 Sept. Nothing irregular.

**✅ £1,200 Barclays credit — explained 11 Sept 2026: it was the tree money,
passed straight through to Hamish.** £473.22→£1,673.22 on 6 Sept (an
unreferenced "FASTER PAYMENTS" credit), then £1,200 straight out again on
7 Sept — but the outgoing leg is **not** a reversal: it's a payment to
"HAMISH JOHN JENKIN" with the reference "HEATHER/PEBMARSH FT". So the
insurer's tree-removal funding reached Rupert's Barclays and Rupert paid
Hamish the same week. Supersedes the earlier reading in this note (an
erroneous credit that reversed itself out) — net effect on Rupert is still
zero, but the money is accounted for, not mysterious. **Cross-project:**
the sibling `divorce` project's open item "confirm Hamish has actually been
paid" is answered by this — paid 7 Sept 2026, £1,200, from Rupert's
Barclays.

**7 Sept 2026 — Starling - Main, ordinary spending.** £1,013.01→£894.93:
small pub/grocery card spend (£22.90/£44.99/£5.89/£6.75/£3.15). Nothing
irregular.

**8–10 Sept 2026 — Starling - Main, ordinary spending only.**
£894.93→£621.85: the £25.97 Tesco Clubcard DD (the retry that settled that
card), Budgens, several small Black Lion/Hare Inn/PayPal items, iD Mobile
£44.99 and two Tesco debits on 10 Sept (£15.20, £50.32). Nothing
irregular.

**10–13 Sept 2026 — both Starling accounts, ordinary spending only.**
Starling - Main £621.85→£479.50: RingGo, The Nutshell, Cook, Hare Inn,
Nethergate Brewery ×2, The Black Lion ×2, Amazon Marketplace, Netflix
£5.99, and a £50 transfer to Mandy ("Mandy Zimmer & Rupert Thomas").
Starling - Joint £166.05→£111.78: Jilani £69.90, Cineworld, Hare Inn and
Tesco £62.59 against two £50 credits in (the usual "Mandy Zimmer & Rupert
Thomas" / "shopping" pair — note the joint-account top-ups have halved
from £100 each on 3 Sept to £50 each on 12 Sept, worth a passing glance
but not obviously irregular). No debt-servicing or shared-debt movement in
this window.

**13–15 Sept 2026 — Starling - Main, ordinary spending plus a water-bill
round trip.** £479.50→£397.42: Netflix £5.99 (13 Sept), then on 14 Sept
Tesco £22.70, Colchester Arts Centre £11.00, MiPermit £2.45, The Centurion
£13.05, plus a £58.00 transfer out to the `Starling - Water` Space — which
came **straight back in on 15 Sept** (+£58.00, same "Water" label), after
which the actual **Anglian Water direct debit of £32.88 came off Starling -
Main directly**, not out of the Space. So the Water pot was filled at £58,
emptied again, and the real bill was paid from the main account: the Space
nets to £0.00 and its "as of" date moves from 17 Jun to 15 Sept without its
balance changing. Reads as Rupert (or Starling's own bill-pot automation)
correcting an over-estimated pot — the £58 pot figure was about £25 above
the actual £32.88 bill. Nothing irregular, nothing owed.

**✅ 14 Sept 2026 — £200 credit into Starling - Joint labelled "Django" is
dog-sitting money.** £111.78→£311.78 on a single inbound £200 line item.
Confirmed by Rupert 16 Sept 2026: **Django is a dog he and Mandy dog-sat
for**, and the £200 is the fee — nothing owed and nothing to chase.
**⚠️ Banktivity mis-pairs this with a Barclays debit — the pairing is wrong,
and it leaves a real £200 unexplained (17 Sept 2026).** Banktivity records
the Django money as a **single two-legged transfer** (transaction `7385`,
type 1): `Barclays - Current` -£200 → `Starling - Joint` +£200, both legs
titled "Django". A refresh note briefly repeated that as fact — **it is
wrong**. Rupert has confirmed the Django money was **cash paid in** to the
joint account and has **nothing to do with Barclays**.

The balances are unaffected either way (the Joint credit and the Barclays
debit both genuinely happened), but the *relationship* between them is a
Banktivity artefact — the same auto-matching failure mode as
`feedback_banktivity_unmatched_duplicate_transfers`, just joining two
unrelated items instead of duplicating one.

**The Barclays leg is separately explained — it is Heather's drain-excess
withdrawal.** The £200 that left `Barclays - Current` on 14 Sept is Heather
taking her half of the uncollected £400 drain insurance excess (see the
15–16 Sept entry below); Rupert took his half out on 16 Sept as "SURPLUS".
Nothing is unexplained. Banktivity has simply mis-titled Heather's
withdrawal "Django" by auto-pairing it with the unrelated cash deposit —
worth un-linking the two legs in Banktivity so each shows its own identity. Flagged on the day only because
the reference appears nowhere else in Banktivity's history, the vault, or
the sibling `divorce` project, and it's the largest single credit this
account has ever taken (every other is a £15–£130 shared-cost or
Gainsborough top-up). Not a duplicate-feed artefact — the
SUM-of-all-line-items check reconciles exactly to £311.78. Worth knowing
the pattern: **ad-hoc third-party income can arrive in the joint account
under a bare personal/pet-name reference**, so an unrecognised one-off
credit here isn't automatically suspicious.

**15–16 Sept 2026 — ordinary spending plus the drain-excess "SURPLUS".**
`Starling - Main` £397.42→£565.17: three £10.75 Five Bells Cavendish items
on 15 Sept, then **+£200 in on 16 Sept labelled "SURPLUS"** — a genuine
two-legged transfer (transaction `7391`) out of `Barclays - Current`.
**Explained by Rupert 17 Sept, from a WhatsApp exchange with Heather:** he
and Heather had each put £200 into an account to cover a **£400 drain
insurance excess** which the insurer "were meant to have collected when they
did the drains but they didn't & haven't asked for it, so it is surplus".
Heather withdrew her £200 ("am skint & need to pay oil – suggest you do the
same") and Rupert has taken his out the same way. So this is Rupert
recovering his own money, not new income and not a cost. Background to the
drains/insurance side sits in the sibling `divorce` project, not here.
`Starling - Broadband` swept £32.99→£0.00 on 16 Sept paying "Fibrely" (the
broadband bill leaving its pot as designed; refills on the 1st).

**⚠️ `Barclays - Current` is down to £73.22 and needs funding before
2 October.** It fell £473.22→£73.22 on **both halves of the uncollected £400
drain insurance excess coming back out** — Heather's £200 on 14 Sept
(mis-titled "Django" by Banktivity) and Rupert's £200 on 16 Sept
("SURPLUS"). £473.22 − £400 = £73.22 exactly, which matches Rupert's own
remark to Heather that the account holds "just enough to pay bills in there.
No more, no less". Fully explained; the only open point is whether it needs
topping up before the October servicing run, which he normally does at the
month rollover. Barclays is the account
the **monthly shared-debt servicing** runs from — roughly **£574.48** goes
out at the start of each month (£200 + £196.50 to Barclaycard, £177.98 to
Halifax; see [[Shared Debt]] / [[Monthly Contributions]]). At £73.22 it
cannot cover that. Rupert does normally top it up at the month rollover
(£459.58 + £230.02 went in on 1 Sept), so this is most likely just the
low point of the usual cycle rather than a problem — but it is a genuine
£500 shortfall against a known, dated commitment, so worth a glance before
the 2nd.

**⚠️ 17 Sept 2026 — the NatWest card's funding Space has been emptied into
Savings Buffer.** Two chained transfers the same day: `Starling - NatWest
Credit Card` **-£300 → `Starling - Main`** (txn 7400), then `Starling -
Main` **-£300 → `Starling - Savings Buffer`** (txn 7401), taking that Space
£0.50 → £300.50. Net effect on `Starling - Main` is nil; the £300 has simply
moved from the card-payment pot into savings.

**✅ Not a problem — confirmed by Rupert 18 Sept.** The Space empties and
refills by design: **on the 1st or 2nd of each month £300 moves
`Starling - Main` → `Starling - NatWest Credit Card` Space, and the card's
DD is then paid out of that Space.** So a £0.00 balance mid-month is the
normal resting state once the DD has gone, not a funding failure. The 17
Sept sweep to Savings Buffer was just surplus being tidied away after the
10 Sept payment. **No action needed before 11 Oct** — the Space will refill
at the month rollover. Recorded here because this funding mechanism wasn't
previously documented anywhere, and a £0.00 Space looks alarming without it.

**16–17 Sept 2026 — `Starling - Main` £565.17→£157.34, ordinary spending.**
Swan Long Melford ×3 and East of England Coop ×2 on 16 Sept; then on
17 Sept the two £300 transfers above (netting to zero), Harpers Haslemere
£158.40 and £132.60 (**both since cancelled — see the refund watch below**),
and Tesco £40.00 and £15.20. `Starling - Joint`
£311.78→£269.80 on a single £41.98 Tesco debit.

**⏳ WATCH — Harpers Haslemere £291.00 refund outstanding (revised 23 Sept
2026 — now BOTH bookings, was £158.40).** Both 17 Sept Harpers Haslemere
debits on `Starling - Main` are cancelled bookings, so the whole £291.00 is
owed back:

| Debit | Amount | Status |
|---|---:|---|
| Harpers Haslemere (10:35) | £158.40 | **Booking.com** (conf 6716612871), cancelled **18 Sept** — refund was due by ~25 Sept, **now overdue** |
| Harpers Haslemere (10:36) | £132.60 | **Direct** (ref 1a0b3dc33c3), cancelled **23 Sept** — refund window runs to ~7 Oct, not late yet |
| **Total owed** | **£291.00** | |

Both were bookings for **the same night, Fri 2 Oct 2026** — one through
Booking.com, one direct — and both were cancelled inside the free-cancellation
window, so there is no cancellation fee on either and the full £291.00 is
owed. Full detail, references and contact number in
[[2026-09-23_harpers-haslemere-both-bookings-cancelled]].

**The two legs are on different clocks:**
- **£158.40 (Booking.com), cancelled 18 Sept — this one is now overdue.**
  Booking.com's cancellation email promised a refund "in the next 7 days"
  (i.e. by ~25 Sept) and explicitly pointed at the hotel, not Booking.com,
  if it doesn't arrive. **This is the leg to chase**, on 01428 776 560,
  quoting conf **6716612871**.
- **£132.60 (direct), cancelled 23 Sept** — 5–10 working days runs to about
  **7 Oct 2026**. Not late yet; don't chase this one before then.

**Neither received as of 23 Sept 2026** (feed runs to 21 Sept, nothing in
email). Check every `/refresh` and close each leg off **separately** — a
partial refund is the likely failure mode, so one credit landing does not
clear the other. This is a material sum against a `Starling - Main` balance
that has been sitting under £200.

**17–20 Sept 2026 — ordinary spending, deeper into the pre-payday trough.**
`Starling - Main` £157.34→£30.46: pub/grocery spend (Black Lion, Hare Inn,
Perrywood, Amazon, Five Bells Cavendish, a £10 cash withdrawal). `Starling -
Joint` £269.80→£256.20: two small debits (Tesco £41.98, Hare Inn £13.60).
`Barclays - Current` £73.22→£32.65: a single £40.57 HomeServe direct debit
(household drain-cover policy, routine). Nothing irregular; no Harpers
Haslemere refund among these line items — still outstanding.

**Cash position is at its pre-payday trough, which is normal.**
`Starling - Main` £30.46 and `Barclays - Current` £32.65 are both very low,
but salary has landed around the 26th in recent months (£6,080.83 on
26 Aug), so the month-end commitments — the ~£574.48 servicing run from
Barclays, the Tesco Loan £139.74, the M&S £175, and the 1st-of-month sweeps
— fall after payday, not before it. Barclays is now well below the
~£574.48 it needs for the October servicing run if nothing lands before
the 2nd — worth a closer watch than usual given how thin both balances now
are.

**Starling - Joint is new** (first appeared in the 2026-07-20 refresh).  
Application approved by email 2026-07-19 — see  
[[2026-07-19_starling-joint-account-approved]]. Joint with Rupert's partner,  
Mandy Zimmer, for managing shared costs. Details on Mandy herself live in the  
sibling `divorce` project, not here.

**Groceries - Joint was closed by Rupert** (confirmed 4 Aug 2026) — no  
longer tracked. **Gainsborough - Joint is unrelated**, a separate new  
account that happens to have appeared around the same time (confirmed by  
Rupert, not a replacement) — where the Gainsborough HealthSpa membership  
direct debit comes out of.

**✅ HealthSpa transfer chain — both legs now confirmed live (1 Sept 2026).**  
On 31 Aug, £130 landed in Starling - Joint as two £65 credits ("Rupert  
Thomas" and "Gainsborough:Rup" — the latter presumably Mandy's side of the  
contribution, labelled differently from her earlier one-off "Transfer from  
Mandy" credits). On 1 Sept, the second leg fired for the first time: £130  
moved Starling - Joint → Gainsborough - Joint (label "Gainsborough" on both  
sides), leaving Gainsborough - Joint at £130.00 and Starling - Joint back  
at its pre-existing £65.44. So the actual monthly cost funding this  
membership is **£130, not £65** as originally assumed — worth Rupert  
confirming that matches what he expects the HealthSpa DD to actually be.  
Both legs of the chain are now operating automatically; nothing further to  
watch here unless the amount or timing looks wrong to him.

### Savings / Bill Pots (Starling Spaces)

**Starling - Lucy Rent has been renamed to Starling - Spare Funds** in  
Banktivity (same account, same balance) — noted here in case the old name  
is referenced elsewhere.

| Account | Balance | As of |
|---|---:|---|
| Starling - Savings Buffer | £300.50 | 2026-09-17 |
| Starling - Stash | £0.00 | 2026-02-17 |
| Gainsborough - Joint (unrelated to closed "Groceries - Joint" — see note above) | £130.00 | 2026-09-01 |
| Starling - Spare Funds (was "Lucy Rent") | £450.00 | 2026-09-21 |
| Starling - Westgate Rent | £0.00 | 2026-09-21 |
| Starling - Broadband | £0.00 | 2026-09-16 |
| Starling - Home Insurance | £5.30 | 2026-09-01 |
| Starling - Water | £0.00 | 2026-09-15 |
| Starling - Council Tax | £0.00 | 2026-09-06 |
| Starling - TV Licence | £0.08 | 2026-09-07 |
| Starling - Tesco Credit Card | £0.00 | 2026-09-08 |
| Starling - NatWest Credit Card | £0.00 ⚠️ | 2026-09-17 |

**Spare Funds → Main top-ups, 20–21 Sept 2026.** £33 (20 Sept) and £150
(21 Sept) moved from `Starling - Spare Funds` to `Starling - Main`, Spare
Funds £633 → £450. Rupert's own transfers, partly to cover the annual
Amazon Prime renewal (£95, due 22 Sept) against a thin Main balance. The
£95 charge itself hasn't appeared in the feed yet — see [[Reminders]].

**Planned: Starling - Amazon Prime Space (flagged 22 Sept 2026).** Not yet
created. Rupert intends to set up a Space funded monthly (~£8) to pay the
annual £95 Prime renewal (next due 22 Sept 2027) — see [[Reminders]]. Add it
to the table once it appears in Banktivity.

These read as budgeting sub-accounts (each a separate Starling "Space")  
rather than real savings — most sit at £0 because they're swept for bills.  
Worth confirming what these are actually for.

**Starling - Savings Buffer now syncing live (24 Aug 2026).** Starling  
previously didn't support open-banking sync on Savings Spaces; Rupert has  
now wired the connection up, so it's no longer a manually-entered figure —  
confirmed matching between feed and ledger (£0.49, last txn 1 Jan 2026).

**✅ Starling - Spare Funds sync fixed (24 Aug 2026, was broken since ~19  
Jul).** Root cause: the "Lucy Rent" → "Spare Funds" rename in Starling  
caused Salt Edge to spin up a second, separate connection to the same  
underlying Space (both showed the same account UID `60f09be44daf` on Salt  
Edge's dashboard) — Banktivity stayed bound to the old dead "Lucy Rent"  
connection (frozen at £470.08/45 transactions from 19 Jul) while the live  
"Spare Funds" connection (£450.00/50 transactions) went unused. Fixed by  
disconnecting just this one account in Banktivity's per-account Connection  
Status dialog and re-adding it under the existing Starling login, this time  
binding to the live "Spare Funds" connection. Banktivity now shows £450.00  
as of 23 Aug, matching Salt Edge/the live app exactly, including the  
transactions (-£50 21 Aug, -£150 23 Aug) that had been stuck. No longer  
flagged as stale.

**Starling - Tesco Credit Card space: settled back to £0.00** — the  
-£74.43 debit flagged 17 Aug posted through to `Tesco Mastercard` on 18 Aug  
(briefly £48.46 credit), then got clawed back again on 19 Aug, same as the  
9-10 Aug cycle. See [[Tesco Clubcard Credit Card]] — this now looks like a  
recurring collection/reversal pattern rather than a one-off, worth Rupert's  
awareness but not costing him anything net so far.

**Starling - Westgate Rent is real rent, not a bill-sweep pot.** Refilled to  
£1,000 on 1 Sept 2026 as expected (was £0 the day before, per the usual  
pay-out-then-refill cycle). £1,000/month is  
the actual rent for where Rupert now lives (with Mandy) —  
Rupert and Mandy split it 50/50, so Rupert's personal liability is £500/  
month. On top of that Rupert separately pays his mortgage liability  
(£1,497.14/month, per [[Monthly Contributions]]) for the  
Pebmarsh house he still jointly owns with Heather. Both together (~£2,000  
combined) is his total housing-cost liability — see  
[[Loan Application Answers]] for where this was used.

### Mortgage

**Not tracked here.** The RBS mortgage (outstanding ~£311k as of Aug 2025,  
early-redemption penalty applies, to be settled by solicitors on sale) is  
being handled in the sibling `divorce` project — see  
`divorce/correspondence/heather/2025-08-27_rbs-mortgage-early-redemption.md`.  
"RBS - Mortgage" in Banktivity (£19.76) is just a linked current/offset  
sub-account, not the mortgage balance — not worth tracking here.

### Personal Credit Cards (Rupert's own)

See individual notes for offer/APR detail.

| Account | Balance | As of | Detail |
|---|---:|---|---|
| Tesco Mastercard (Clubcard) | £0.00 | 2026-09-08 | [[Tesco Clubcard Credit Card]] — £25.97 minimum payment cleared, confirmed settled |
| NatWest Mastercard | -£1,255.11 🚨 | 2026-09-15 | [[NatWest Mastercard]] — **no longer 0%**; £52.55 interest charged 15 Sept, whole balance at 26.436% |
| Capital One | £0.00 | 2026-09-17 | [[Capital One]] — verified from the web portal; ⚠️ web access being withdrawn, app access unresolved |
| M&S Mastercard | -£1,791.31 | 2026-09-05 | [[M&S Credit Card]] |

**Atkins Dellow solicitor payment (28 Jul 2026) executed as planned on both  
cards.** M&S shows -£1,966.31 (£1,900 transfer + £66.31 fee); NatWest shows  
-£1,502.56 (£1,420.56 existing 0% BT + £82 stranded). Banktivity briefly had  
a data-entry error on the NatWest side (the transfer-out mis-recorded as a  
second Charge instead of a Payment), fixed by Rupert 29 Jul 2026 — both  
figures above are now confirmed correct. See [[Solicitor Payment 0% Plan]]  
and the individual card notes.

**✅ NatWest Mastercard duplicate £300 payment — resolved 11 Sept 2026.**
Banktivity had briefly shown -£902.56 off a second, single-sided £300
credit dated 9 Sept that the NatWest feed re-imported alongside the 8 Sept
two-legged transfer. Rupert cleared the duplicate the same day; the ledger
reconciles to **-£1,202.56** again. See [[NatWest Mastercard]].

**🚨 NatWest is no longer a 0% card — found 17 Sept 2026.** A **£52.55
interest charge** posted on 15 Sept, the first ever on this card, taking it
to **-£1,255.11**. The 16 Aug statement
([[2026-08-16_natwest-0354-statement.pdf]]) shows the whole balance under
*Purchases at 26.436%* with **no promotional row**. Cause, read off the
statement's own transaction list: the £1,900 transfer in from M&S on 28 Jul
**repaid the protected 0% balance in full**, and the £1,982 solicitor charge
then landed as fresh full-rate purchase debt. The 0% wasn't lost to an
expiry — it was repaid, and the costly borrowing was left behind. This makes
NatWest **the most expensive debt Rupert currently holds**, and it
invalidates the "£82 stranded at £1–2 interest" assumption in
[[Solicitor Payment 0% Plan]]. The Tesco Clubcard 0% BT offer could absorb
it for ~£63 of fee, but its window shuts **9 Oct 2026** — see
[[0% Offers Tracker]] and [[2026-08-16_natwest-statement-0pc-gone]].

### Personal Loans (Rupert's Own Liabilities, not shared/Anne)

| Account | Balance | As of | Detail |
|---|---:|---|---|
| Tesco Loan | -£1,956.36 | 2026-08-31 | [[Tesco Loan]] — £3,000 @ 9.8% APR, £139.74/month, opened Aug 2025 |

**✅ Tesco Loan ledger corrected by Rupert, 16 Sept 2026 — now reconciles.**
The account had been seeded with the **advance** (£3,000) instead of the
**total owed** (£3,353.76) while still deducting the full £139.74 per
payment, which would have finished £353.76 *in credit*. Rupert restated the
opening balance to **-£3,353.76**; verified the same day — 10 payments
posted, running balance **-£1,956.36**, SUM cross-check agrees exactly, and
the remaining 14 × £139.74 now lands precisely on £0.00. The figure above is
the real outstanding liability, so this row no longer needs a caveat. The loan is a **precomputed** fixed-sum loan (interest calculated
once at the outset and added to the advance, the £3,353.76 total divided by
24), confirmed from the signed agreement filed 16 Sept 2026 — so there are no
monthly interest postings for Banktivity to pick up, and none will ever
appear. Actual remaining liability is **£1,956.36** (14 × £139.74); a true
early-settlement figure is obtainable only from Tesco. Full detail, including
the free amortisation table available on request and the corrected
beginning-of-month payment pattern, is in [[Tesco Loan]] and
[[2025-08-19_tesco-loan-origination-pack]].

### Other Personal Credit Agreements

| Item | Detail |
|---|---|
| Car Insurance (Tesco) | See [[Car Insurance]] — switched from 1st Central 7 Aug 2026; 11×£20.76 monthly DDs, first due 4 Oct 2026 |

### Loans from Anne (owed back to Anne)

See [[Loans from Anne]].

| Account | Banktivity balance | As of |
|---|---:|---|
| Ann - Loan #1 | -£3,318.00 | 2025-07-19 |
| Ann - Loan #2 | -£5,522.66 | 2025-07-19 |

Banktivity itself has now been updated to the exact figures — matches  
[[Loans from Anne]] (£3,318 + £5,522.66 = £8,840.66, confirmed by Heather  
27 Jul 2026, superseding the old rounded £3,300 + £5,500).

### Other Personal Loan (not yet Documented Anywhere else)

| Account | Balance | As of |
|---|---:|---|
| Stuart Loan | -£3,000.00 | 2025-07-23 |

Loan from Rupert's dad, Stuart. Still owed, but not being actively repaid  
at the moment (no scheduled repayments).

### Shared Debt (Heather) — See [[Shared Debt]]

| Account | Banktivity balance | As of | Shared Debt.md figure |
|---|---:|---|---|
| Heather - Barclaycard | -£7,819.16 | 2025-11-04 (stale) | -£7,116.17 (2026-09-21, from Barclaycard's own persistent-debt notice — supersedes spreadsheet) |
| Heather - Halifax | -£6,884.86 | 2025-11-04 (stale) | -£6,330.58 (2026-09-07, from 16 Aug 2026 statement via WhatsApp) |
| Ann - Barclaycard | -£2,809.00 | 2025-11-04 (stale) | -£1,409.00 (2026-07-10, from spreadsheet) |

[[Shared Debt]] is being kept up to date from a spreadsheet, so it's the  
more trustworthy figure for the three accounts above — Banktivity just  
hasn't had transactions entered since Nov 2025.

**Heather - Next Directory:** closed and settled, deleted from Banktivity —  
nothing to track.
