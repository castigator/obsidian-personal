## How to File for Divorce — One-Pager

*England & Wales, no-fault. Plain summary for discussion. Not legal advice. Compiled 5 Jun 2026.*

### What "filing" Actually is

Filing the divorce application is the **opening move** — and it's almost a press-button. It needs **no financial  
detail, no agreement, and no reason** (no-fault). Filing **starts a 20-week clock**; the money side (gathering  
figures → mediation → drafting the consent order) all happens **during** those 20 weeks. So filing early just  
gets the clock ticking — it commits us to nothing about the finances.

### What We Need to File

- ✅ **Both full names** (as on the marriage certificate) + **both addresses**
- ✅ **Marriage date** — 22 Aug 1998
- ✅ **Marriage certificate** — a clean certified copy (ordering a fresh one, ~£11)
- ✅ **£612 court fee** (one fee, whoever applies)
- ✅ Tick the box to **keep financial claims open** (no figures needed — just a placeholder for the consent order later)

### What We Do NOT Need to File

- ❌ Any financial information — asset values, pensions, house valuation, debts
- ❌ The consent order (that comes later, inside the 20 weeks)
- ❌ Any reason, grounds, or blame

### Sole Vs Joint (same Cost, Same Timeline, Same outcome)

- **Joint** — we apply together on one form; both confirm. Collaborative, but moves at the pace we both act.
- **Sole** — one of us applies; the other simply acknowledges receipt later. Faster to start; still entirely no-fault, no blame.

### The Shape of the Process

> Two tracks run **in parallel** over the same period: **the divorce** (fixed, can't be contested) and **the  
> finances** (where the actual work is). They meet at two gates. Timeline is **illustrative** — some labels/durations  
> still being refined.

```mermaid
gantt
    title Divorce Timeline — both tracks run in parallel
    dateFormat YYYY-MM-DD
    axisFormat %b
    tickInterval 1month
    todayMarker off

    section DIVORCE
    File application            :a1, 2026-06-15, 1w
    Application issued          :milestone, am1, after a1, 0d
    20-week statutory wait      :a3, after am1, 20w
    Apply for Conditional Order :milestone, ac1, after a3, 0d
    Court lists CO (5–7 wks)    :ac2, after ac1, 6w
    GATE 1 · Conditional Order  :milestone, g1, after ac2, 0d
    6 wks + 1 day               :a4, after g1, 6w
    28d pension-order wait      :b6, after bm2, 4w
    Apply for Final Order       :milestone, af1, after b6, 0d
    Court processes             :af2, after af1, 2w
    GATE 2 · Final Order        :milestone, g2, after af2, 0d

    section FINANCES
    Gather the numbers          :b0, 2026-06-15, 8w
    Mediation (optional)        :b1, after b0, 6w
    Draft consent order + D81   :b2, after b1, 7w
    Lodge consent order         :milestone, b4, after g1, 0d
    Court reviews fairness      :b5, after b4, 6w
    Consent order sealed        :milestone, bm2, after b5, 0d
    Pension share implements    :pi1, after g2, 16w

    section COSTS
    £612 court fee              :milestone, k1, 2026-06-15, 0d
    Mediation (≈⅓ of lawyers)   :k2, after b0, 6w
    Consent order £1,600+VAT    :milestone, k3, after b1, 0d
    Filing fee ~£53             :milestone, k4, after g1, 0d
```

**Reading it:** filing the application (far left) starts everything. We gather numbers and mediate **during** the  
20-week wait. **Gate 1 (Conditional Order)** unlocks lodging the financial agreement. **Gate 2 (Final Order)** —  
the marriage ends — is deliberately held until the financial/pension side is sealed and safe.

### Costs to Budget for (most Are shared)

- **£612** — court fee to file (one-off)
- **Pensions expert (PODE) — ~£2,500–3,500, shared.** An actuary works out a *fair* pension split (a defined-  
  benefit pension's headline value is misleading, and Heather has one). One jointly-instructed expert, cost  
  split. Lands during the "gathering the numbers" phase.
- **Mediation — budget ~£2,000 total (~£1,000 each):**
    - *Does what:* turns "50/50 in principle" into concrete terms — offsetting, timing of realisation, clean break vs maintenance → produces the MoU the consent order is drafted from
    - *Cost:* MIAM each (~£100pp) + ~3 sessions + MoU; ~⅓ of the solicitor route
    - *Provider:* National Family Mediation (independent / charity — not a government service); mediator is neutral, advises neither side
    - *Action:* contact early, as advised
- **Consent order** — ~£1,600 + VAT to draft it (fixed-fee solicitor), + ~£53 to file
- *(Staying cooperative is what keeps all of these at the low end — a contested route multiplies every one.)*

---

*Notes still to firm up: exact mediation cost (per person vs joint), the ~£53 consent-order filing fee, and a few  
diagram labels. Statutory minimum ~26 weeks; real-world average ~44 weeks.*

## Related analysis

- [[2026-06-05_how-to-file-divorce-application]] — step-by-step filing guide
- [[2026-06-02_divorce-process-flow-validated]] — validated end-to-end process flow + nomenclature
- [[2026-06-03_sole-vs-joint-and-solicitor-models]] — sole vs joint application + solicitor models
