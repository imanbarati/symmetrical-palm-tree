# Preliminary Financial Model — Specification

## Status and limitations
This is a model design, not a valuation, appraisal, quantity-surveyor estimate, investment offer, or forecast. No site area, permitted area, local currency, market rents, costs, taxes, financing terms, or schedule have been verified. Therefore this document intentionally contains formulas and input fields rather than invented amounts.

## Model architecture
Build one workbook with the following tabs:
1. Read_Me — version, author, model date, currency, limitations, and change log.
2. Inputs — editable assumptions, units, low/base/high values, source IDs, confidence, and last-verified dates.
3. Site_Planning — land area, setbacks, coverage, floor-area ratio, permitted height, gross floor area (GFA), excluded areas, and net lettable/saleable area.
4. Program — use mix, area allocation, efficiency, rents/prices, occupancy, absorption, incentives, operating expenses.
5. Development_Cost — hard costs, soft costs, site works, basement, fees, taxes, contingency, escalation.
6. Schedule — planning, design, procurement, construction, lease-up, and stabilization dates.
7. Revenue — sales proceeds, rental income, parking/ancillary income where supported.
8. Funding — founder land contribution, partner equity, third-party equity, debt, deposits/presales only if lawful, and other eligible funding.
9. Cashflow — monthly or quarterly development cash flow and interest during construction.
10. Returns — project IRR, equity multiple, NPV, residual land value, development margin, debt metrics.
11. Sensitivity — scale, cost, revenue, rate, delay, occupancy, and contingency scenarios.
12. Sources — evidence register and source IDs for every material assumption.

## Core formulas (define sign conventions consistently)
- Buildable GFA = MIN(planning-permitted GFA, technically feasible GFA, market-supported GFA). The relevant planning method must be confirmed locally.
- Net lettable/saleable area = GFA × net-to-gross efficiency. Efficiency must be benchmarked against relevant local comparables and tested by the design team.
- Gross development value (GDV) = sum of supportable sales proceeds + capitalized stabilized income value + other evidenced income. Do not count the same asset as both sold and retained.
- Stabilized NOI = effective gross operating income − operating expenses, excluding financing and tax according to the selected valuation convention.
- Income value = stabilized NOI ÷ market-supported capitalization rate, only where an income valuation is appropriate and sourced.
- Total development cost (TDC) = land basis + hard costs + soft costs + site/infrastructure + statutory charges + taxes + financing costs + contingency + escalation + other owner costs. Avoid double-counting land where it is contributed.
- Development profit = GDV − TDC.
- Development margin = development profit ÷ GDV.
- Residual land value (simplified) = GDV − non-land development costs − required developer profit − financing and other costs, with timing and tax treated consistently. A discounted cash-flow residual may be more appropriate for complex/phased projects.
- Funding gap = peak cumulative cash requirement − available committed equity/debt/other eligible sources.
- Debt draw = MIN(eligible cost × lender advance rate, lender LTV limit, lender LTC limit, debt yield constraint, facility cap), subject to actual lender terms.
- Loan-to-cost = debt ÷ eligible project cost.
- Loan-to-value = debt ÷ lender-accepted collateral value.
- Equity multiple = cash distributions to equity ÷ total equity invested.
- Project IRR and equity IRR must be calculated from dated cash flows, not a single-period profit ratio.
- Interest during construction must be calculated from actual draw timing and loan terms; avoid a circular reference or document the iterative calculation method.
- Contingency = applicable cost base × independently recommended contingency percentage. The percentage must be set by a cost professional based on scope/design maturity and risk.

## Scenario design
Run separate cases for:
- 40 floors.
- 60 floors, only if lawful planning capacity is plausible.
- Reduced height / mid-rise.
- Phased or joint-venture alternative.
- Land sale or ground lease.
- No-build / hold.

Each case needs its own floor area, efficiency, use mix, program, schedule, cost plan, revenue, risk and capital stack. Do not derive a 60-floor estimate by simply multiplying a 40-floor estimate by 1.5.

## Required sensitivities
At minimum:
- Permitted GFA / height lower than target.
- Construction cost +10%, +20%, and +30% as analytical stress tests—not predictions.
- Revenue/rent/sales value −10%, −20%, and −30%.
- Construction and approval delay by 6, 12, and 24 months.
- Interest rate +1, +2, and +3 percentage points.
- Occupancy/absorption slower than base case.
- Basement omitted, reduced, or materially more expensive.
- Contingency and escalation increased.
- Equity diluted or lender advance reduced.
- Combined downside case.

These percentages are stress-test settings only; replace them where local market evidence and professional advice justify different ranges.

## Model integrity controls
- Every key input must have units, source ID, source date, confidence, and owner.
- Distinguish hard-coded assumptions from calculated outputs.
- No hard-coded project returns or valuation conclusions.
- Include explicit currency and measurement units; do not mix currencies or square-foot / square-metre assumptions.
- Add checks for GFA reconciliation, area allocation totals, funding balance, cashflow balance, and no negative unexplained cash.
- Add warnings when approvals, cost plans, leases, or financing are unverified.
- Show nominal vs real values and tax treatment.
- Maintain formula documentation and version history.
- Have an independent reviewer inspect formulas and assumptions before external circulation.

## Investment interpretation
Land ownership is not automatically cash equity, liquid collateral, or accepted lender security. Its contribution value depends on title, market valuation, legal transfer/lease structure, priority of claims, and lender/investor requirements. A land contribution may also create tax, stamp duty, transfer, or liability consequences. Obtain independent legal, valuation, tax, and financing advice.

## No fabricated outputs
Until verified inputs exist, label results “illustrative only / not calculated.” Never present template cells as a feasibility conclusion or investor return forecast.
