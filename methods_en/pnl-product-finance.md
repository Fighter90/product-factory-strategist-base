---
id: M-pnl-product-finance
lang: en
title: Product finance for a PM — P&L, Cash Flow, EBITDA, and expense classification
course: skills
sources: ["EN mirror of the RU methodology card M-pnl-product-finance (knowledge/methods/pnl-product-finance.md); original sources are listed in the RU card"]
stages: [strategy, options, decision, after-decision]
tags: [pnl, ebitda, cashflow, opex, capex, expenses, financial-model, investment, business-case, headcount]
related: [M-unit-economics, M-business-models, M-monetization, M-traction-model, M-model-validation, M-cannibalization, M-market-sizing]
---

# Product finance for a PM — P&L, Cash Flow, EBITDA, and expense classification

## When to use
You need to explain to management and finance how a product decision shows up in the company's money: defend a development budget, build the business case for a direction, plan team headcount, or evaluate an investment case (spending now against payoff later). Unit economics answers "does the model converge per client" ([[M-unit-economics]]); this card answers "what the product model looks like in the company's reporting".

## Core idea
**Three statements a PM must understand:**
- **P&L (profit and loss statement)** — per period: revenue − expenses = profit. Shows *whether the model works*. The key line for a product is **EBITDA**: profit before interest, taxes, and depreciation; a rough operating profitability of the business, free of financing choices and asset accounting.
- **Cash Flow (statement of cash flows)** — when money actually arrives and leaves. Profit ≠ money: revenue recognized but the client has not paid; a subscription paid in advance. Shows *whether the business survives over time* — cash gaps kill profitable models too.
- **Balance sheet** — the state at a date: assets/liabilities; where CAPEX and receivables sit. A PM needs it at the concept level.

**Expense classification is the PM's main tool:**
| Dimension | Pairs | Why the PM needs it |
|---|---|---|
| Reaction to volume | fixed ↔ variable | fixed costs are the scale lever and the risk when revenue falls; variable ones are predictability |
| Attribution to the product | direct ↔ indirect | honest product unit economics: do not split infrastructure "equally for everyone" without logic |
| Accounting treatment | OPEX ↔ CAPEX | a service subscription is OPEX; own development/equipment is CAPEX (depreciated); it affects EBITDA and how the project looks in reporting |
| Link to the decision | controllable ↔ uncontrollable | what the PM can actually change via the roadmap |

**Where unit economics sits in the system:** unit economics is the "micro" (one client/order); P&L is the "macro" (the whole product per period). The link: `P&L revenue ≈ Σ (unit metrics × volumes)`; a mismatch means either indirect expenses/discounts are missing from the model, or the wrong period is used. A mandatory check when defending a business case: scaled unit economics must reproduce the P&L lines ([[M-unit-economics]]).

**Order of work on a product P&L case (a 12+ month model):**
1. Revenue from the growth model ([[M-traction-model]]): volumes × price/ARPU by segments, with seasonality.
2. Variable expenses: cost of turnover (acquiring, volume-based hosting, support per ticket).
3. Fixed: payroll — by role and workload (how many people the volume of work requires, not "as before"), fixed contracts, marketing budget split into acquisition/retention.
4. EBITDA = revenue − operating expenses; product gross margin; break-even point.
5. Sensitivity check: what happens to EBITDA at −20% revenue, +30% CAC, a quarter's launch delay ([[M-model-validation]]).

**Investment case (comparing a spend against alternatives):** a 3–5 year horizon; cash flows by year (−investment in year 0, effects from year 1+); discounting future money (the rate is the company's required return); NPV > 0 and a payback period within an acceptable horizon are the basic criteria; base/optimistic/pessimistic scenarios are mandatory. For product decisions, the "NPV/payback + sensitivity" pair is usually enough — no complex formulas required.

## Procedure
1. **State the decision question in money terms:** a development budget? a direction business case? an investment case? headcount planning? The question sets the model's depth.
2. **Assemble the factual base:** the product's current P&L lines (or the nearest analogue), current rates and contracts, headcount by role.
3. **Build revenue** from the growth model by segments ([[M-traction-model]]), not "grows 20% a month".
4. **Classify expenses:** fixed/variable, direct/indirect, OPEX/CAPEX; each block gets an owner and a controllability mark.
5. **Assemble the EBITDA model for the horizon** with monthly detail in year one: see the break-even point and cash gaps (Cash Flow separately: revenue recognition ≠ cash receipt).
6. **Reconcile unit economics with P&L:** scaled unit metrics must approach the report lines; a gap above 15–20% — find and explain the cause.
7. **Run sensitivity:** 3–5 scenarios of key assumption changes; which lines move EBITDA the most — that is where accuracy matters most.
8. **Package the case:** assumptions → model → EBITDA/break-even → sensitivity → the decision and review conditions; for an investment case — NPV and payback by scenario.
9. **Set control after the decision:** actuals vs the model monthly; a gap — recompute the model and the conclusions ([[M-model-validation]]).

## Template / checklist
| Field | Fill in |
|---|---|
| Decision question | budget / business case / investment case / headcount |
| Model horizon, detail step | |
| Revenue: segments, price/ARPU, seasonality | |
| Variable expenses (per unit) | |
| Fixed (payroll by role, contracts) | |
| OPEX/CAPEX split of key items | |
| EBITDA, gross margin, break-even point | |
| Cash Flow: cash gaps | |
| Reconciliation with unit economics | gap and cause |
| Sensitivity scenarios (3–5) | |
| NPV/payback (for an investment case) | |
| Actuals-vs-model control | |

## Quality criteria
- The model answers a specific decision question (budget / business case / investment case / headcount), not "finances in general".
- Revenue is built from the growth model by segments with seasonality; costs are split across all four classification axes.
- Unit economics is reconciled with P&L: the gap is computed and explained, not ignored.
- Cash Flow is shown separately from profit: cash gaps are visible month by month.
- Sensitivity covers 3–5 scenarios; assumption precision is higher for the lines that move EBITDA the most.
- For an investment case, NPV and payback are computed in the pessimistic scenario, not only the base one.
- Fact-vs-model control is scheduled with a date; the conditions for revisiting the case are written down.

## Typical mistakes
- Confusing profit and money: the model is profitable, the cash gap in the rollout month is unnoticed.
- All expenses "split equally across the product": indirect ones distributed without logic, unit economics profitably fake.
- A CAPEX project looks free in the expense month (depreciation spread out) — the PM enjoys the margin, finance does not.
- Revenue growth without seasonality and without a link to the growth model funnel.
- One optimistic scenario instead of sensitivity: EBITDA "converges" only under the base assumption.
- Headcount grows with revenue without a workload check: fixed expenses eat the margin when growth lags.
- The forgotten break-even point: unclear at what volume the direction starts paying off.

## Questions that can change the decision
- Which model lines move EBITDA the most, and how accurate are the assumptions on them?
- At what volume is the break-even point — and is it reachable within the model horizon?
- What happens to cash (Cash Flow) if a major client pays a quarter late?
- How many fixed expenses does the decision add, and what happens to them if revenue drops 20%?
- What are the NPV and payback in the pessimistic scenario — acceptable for the company?
- Does scaled unit economics reconcile with P&L (the gap explained)?

## Related maps
[[M-unit-economics]], [[M-business-models]], [[M-monetization]], [[M-traction-model]], [[M-model-validation]], [[M-cannibalization]], [[M-market-sizing]]
