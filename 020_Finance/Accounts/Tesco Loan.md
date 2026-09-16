# Tesco Loan

**Source document:** [[2025-08-19_tesco-loan-agreement-pack.pdf]] — the full
origination pack (approval letter 13 Aug 2025, welcome letter 19 Aug 2025,
"Understanding Your Loan", Pre-contract Credit Information, and the signed
Fixed Sum Loan Agreement customer copy). Everything below is taken from that
document, not inferred. Filed 16 Sept 2026.

- **Type:** Fixed sum loan, regulated by the Consumer Credit Act 1974
- **Creditor:** **Barclays Bank UK PLC** — "Tesco Bank" is a trading name
  (FCA Financial Services Register no. 759676)
- **Loan account no.:** 30519631 · **Sort code:** 406412
- **Application ref:** 886380636
- **Applied:** 13 August 2025 · **Opened:** 19 August 2025
- **Amount borrowed:** £3,000.00
- **Interest rate:** 9.3855% per annum (nominal, **fixed** for the term) ·
  **APR:** 9.8%
- **Length:** 26 months · **Repayments:** 24 (two-month payment break at the
  start — that's why 26 months carries only 24 payments)
- **Monthly payment:** £139.74
- **Total interest due:** £353.76 · **Total to repay:** £3,353.76
- **First payment:** 2 December 2025
- **Repaid from:** sort code 60-83-71, account 29495288 — shows as
  "Tesco Bank Loan" on the statement

## ⚠️ How the interest actually works — precomputed, not amortising

**There are no monthly interest charges on this loan, and never will be.**
The agreement (customer copy) is explicit:

> "At the beginning of the loan we work out the interest you will pay over
> the whole length of your loan and add this to your loan amount. We
> calculate your interest charge by applying interest at a monthly rate based
> on the APR to the balance of your loan, as reduced by your monthly
> repayments. We add this to the loan amount and then divide this total by
> the number of monthly repayments."

So the £353.76 was calculated **once, up front**, added to the £3,000, and
the £3,353.76 total divided by 24 to give £139.74. Each payment is simply
1/24th of the total — it is **not** split into an interest portion and a
principal portion that varies month to month.

This matters because it invalidates the obvious-looking approach: you cannot
derive a monthly interest/principal split for this loan from the APR, and any
such table would be a fabrication. (One was produced in the 16 Sept 2026
session before this document was read, and was wrong — it described a
reducing-balance amortising loan, which this is not.) **If a genuine
breakdown is ever needed, request it — see below.**

**📄 Free amortisation table on request.** Per the agreement's General Terms:
"You can get a free statement of your account (Amortisation Table) at any
time. This will tell you how many repayments you still have to make, the due
date and amount of each repayment, the amount of interest and capital in each
repayment and any conditions relating to future repayments." This is the only
legitimate source for a per-payment breakdown — call 0345 600 6016.

## Seeing the loan online / in the app

**The loan won't appear in the Tesco Bank app until it's linked in Online
Banking — and the linking can only be done in Online Banking, not in the
app.** Tesco Bank accounts aren't automatically joined up: the app only
displays products already attached to your Online Banking profile, which is
why the card shows and the loan doesn't no matter how long you hunt through
the app. Researched 16 Sept 2026 after Rupert couldn't find it.

**Fix — in Online Banking (web), not the app:**
1. Log in to Tesco Bank Online Banking.
2. Select **"Add your other Tesco Bank accounts"**.
3. Enter the loan's account details when prompted.

(The app has a signpost to the same place — settings → *Account* →
*Add Tesco Bank accounts* → *Continue to Online Banking* — but it hands you
off to the web to actually do it. Exact menu wording varies by app version.)

**The details it will ask for** — from
[[2025-08-19_tesco-loan-agreement-pack.pdf]]:
**Loan account no. 30519631**, **sort code 406412**.

Once linked, the app home screen shows the balance, remaining term and next
payment date, with payment history back to account opening and statements
for the last 5 years. Online Banking additionally shows the annual interest
rate and a document store, and both can produce an early settlement figure.

**Note:** neither the app nor Online Banking advertises the **Amortisation
Table** — that remains a phone request (0345 600 6016), per the agreement's
General Terms.

**Early settlement fee — the website and the agreement reconcile.** Tesco's
current pages quote "a fee of up to 2 months' interest", whereas the 2025
agreement says 28 days' interest and a settlement figure that includes
30 days' interest. Those are the same thing: 30 + 28 = 58 days ≈ "up to
2 months". No contradiction, no change in terms.

**Why the app is Barclays-operated:** Tesco Bank's banking business
transferred to **Barclays Bank UK PLC** on 1 Nov 2024 — products stay
Tesco-branded but are run by Barclays, which is why the PCCI in the pack
names Barclays as the creditor.

## Payment dates

- **Contractual date:** the **2nd of each month**, "or the next working day".
- **Observed in practice:** lands on the 1st or 2nd, occasionally the 5th —
  always at the **beginning** of the month, never the end. Ledger dates that
  look like month-end (31 Mar, 31 May, 30 Jun, 31 Aug) are the *following*
  month's payment landing a day or two early, not late payments.
- The repayment date can be **changed once a year**; doing so may extend the
  agreement by up to one month but won't change the interest or the number of
  repayments.

## Balance — three different numbers, don't conflate them

| Figure | Amount | What it is |
|---|---:|---|
| Banktivity ledger balance | **-£1,956.36** (as of 2026-08-31) | ✅ Corrected 16 Sept 2026 — opening balance restated to the total owed (£3,353.76). Now **agrees exactly** with the remaining contractual liability below, so these are no longer two different numbers. |
| Remaining contractual liability | **£1,956.36** | 14 remaining payments × £139.74. What it actually costs to run to term. |
| Early settlement figure | **only Tesco can say** | Must be requested. Includes a statutory CCA rebate of future interest, but also 28 days' interest (see below). |

### ✅ Ledger seeding — found and fixed, 16 Sept 2026

Because interest is added up front, the liability from day one is
**£3,353.76**, not £3,000. Banktivity had been seeded with the **advance**
(£3,000 — a manual "STARTING BALANCE / BALANCE ADJUSTMENT" row dated
15 Oct 2025) while still deducting the **full £139.74** per payment. Those
two don't belong together: 24 × £139.74 = £3,353.76, so a £3,000 opening
runs out early — the ledger would have reached £0 around payment 21½ and
finished showing **£353.76 in credit**, a loan that appears overpaid by
exactly the interest.

Two conventions would each have been self-consistent:
**(a) precomputed** — open at £3,353.76, subtract £139.74, landing exactly
on £0.00 at payment 24 (what the agreement describes); or
**(b) flat-rate split** — open at £3,000 and subtract £125.00 principal
(£3,000 ÷ 24), treating £14.74 of each payment as interest, since
£125.00 + £14.74 = £139.74 exactly. Banktivity was mixing (a)'s payments
with (b)'s opening balance.

**Resolved:** Rupert restated the opening balance to **-£3,353.76**
(convention (a)). Verified the same day from a fresh copy of the live file:
opening -£3,353.76, ten £139.74 payments, running balance **-£1,956.36**,
and the independent SUM-of-all-line-items check agrees to the penny. The
remaining 14 payments × £139.74 = £1,956.36 now lands precisely on £0.00 at
payment 24. **No caveat needed on this account any more** — the Banktivity
balance is the real outstanding liability, and `/refresh` can treat it like
any other row.

**Progress:** 10 of 24 payments posted (2 Dec 2025 → 31 Aug 2026, all on
time, none missed — the 10 payments reconcile exactly to the ledger balance:
£3,000 − (10 × £139.74) = £1,602.60). September 2026's payment was taken
early, on 31 Aug 2026. Next due ~2 Oct 2026. Final payment falls around
November 2027.

## Overpayments and early settlement

- **Overpayments:** allowed, with no charge for making them. By default Tesco
  uses an overpayment to **reduce the term**, leaving the £139.74/month
  unchanged. **Alternatively** you can have it reduce the monthly payment and
  keep the term the same — but you must **call 0345 600 6016 before making
  the overpayment** to choose this.
- **Early settlement in full:** allowed at any time. You must call for a
  settlement figure; it is valid for 30 days and automatically includes 30
  days' interest. The agreement also states that settling early attracts a
  charge of **28 days' interest**. A statutory CCA rebate of future interest
  is applied.
- If the account were ever in arrears, any extra payment is applied to clear
  the arrears first.

## Fees and charges

- **£12** each time a payment is missed
- **£12** each time a default notice is sent
- Tesco's "reasonable costs" if they have to take steps to secure repayment —
  explicitly including **the cost of tracing a new address if not notified**

## ⚠️ Address on file

The pack is addressed to **Mapletree House, 1 Kings Mead, Pebmarsh, Halstead,
CO9 2NA** — the Pebmarsh house. Rupert now lives at the Westgate address with
Mandy (see [[Accounts]]). Given the agreement charges for tracing an
un-notified address change, **worth confirming whether Tesco has been told**.
Not actioned — flagged 16 Sept 2026.
