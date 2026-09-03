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
| Starling - Main | £1,641.87 | 2026-09-01 |
| Starling - Joint | £65.44 | 2026-09-01 |
| Barclays - Current | £540.17 | 2026-09-02 |

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
| Starling - Savings Buffer | £0.50 | 2026-08-30 |
| Starling - Stash | £0.00 | 2026-02-17 |
| Gainsborough - Joint (unrelated to closed "Groceries - Joint" — see note above) | £130.00 | 2026-09-01 |
| Starling - Spare Funds (was "Lucy Rent") | £633.00 | 2026-09-01 |
| Starling - Westgate Rent | £1,000.00 | 2026-09-01 |
| Starling - Broadband | £32.99 | 2026-09-01 |
| Starling - Home Insurance | £5.30 | 2026-09-01 |
| Starling - Water | £0.00 | 2026-06-17 |
| Starling - Council Tax | £152.00 | 2026-09-01 |
| Starling - TV Licence | £15.53 | 2026-09-01 |
| Starling - Tesco Credit Card | £0.00 | 2026-07-02 |
| Starling - NatWest Credit Card | £600.00 | 2026-08-31 |

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
| Tesco Mastercard (Clubcard) | -£25.97 | 2026-08-19 | [[Tesco Clubcard Credit Card]] |
| NatWest Mastercard | -£1,502.56 | 2026-07-28 | [[NatWest Mastercard]] |
| Capital One | £0.00 | 2026-05-01 | [[Capital One]] |
| M&S Mastercard | -£1,966.31 | 2026-07-27 | [[M&S Credit Card]] |

**Atkins Dellow solicitor payment (28 Jul 2026) executed as planned on both  
cards.** M&S shows -£1,966.31 (£1,900 transfer + £66.31 fee); NatWest shows  
-£1,502.56 (£1,420.56 existing 0% BT + £82 stranded). Banktivity briefly had  
a data-entry error on the NatWest side (the transfer-out mis-recorded as a  
second Charge instead of a Payment), fixed by Rupert 29 Jul 2026 — both  
figures above are now confirmed correct. See [[Solicitor Payment 0% Plan]]  
and the individual card notes.

### Personal Loans (Rupert's Own Liabilities, not shared/Anne)

| Account | Balance | As of | Detail |
|---|---:|---|---|
| Tesco Loan | -£1,602.60 | 2026-08-31 | [[Tesco Loan]] — £3,000 @ 9.8% APR, £139.74/month, opened Aug 2025 |

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
| Heather - Barclaycard | -£7,819.16 | 2025-11-04 (stale) | -£7,274.24 (2026-07-20, from actual statement — supersedes spreadsheet) |
| Heather - Halifax | -£6,884.86 | 2025-11-04 (stale) | -£6,282.94 (2026-07-10, from spreadsheet) |
| Ann - Barclaycard | -£2,809.00 | 2025-11-04 (stale) | -£1,409.00 (2026-07-10, from spreadsheet) |

[[Shared Debt]] is being kept up to date from a spreadsheet, so it's the  
more trustworthy figure for the three accounts above — Banktivity just  
hasn't had transactions entered since Nov 2025.

**Heather - Next Directory:** closed and settled, deleted from Banktivity —  
nothing to track.
