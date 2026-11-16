# Validation plan: <project>

> The experiment card is filled in BEFORE the launch. Decision criteria are fixed in advance.

## Hypothesis 1: <statement>

### Expected change
- Metric, direction, magnitude (range), unit, period; why we expect it [C###].

### Comparison baseline
- Design: A/B / control region / before-after adjusted for seasonality. Base value [C###] or how to get it.
- Minimum detectable effect (MDE) and sample size.

### Observation window
- … weeks: usage/payment/renewal cycle + sample recruitment.

### Counter-metrics
| Counter-metric | Stop threshold |
|---|---|

### KPI of two planes
| Plane | Metric | Formula |
|---|---|---|
| Business | Revenue/MRR | payments × average check (per period) |
| Business | Payers | unique payers per period |
| Business | Conversion to payment | payers / registered |
| Business | LTV/CAC | (average check × margin × repeat purchases) / CAC |
| Product | <key feature metric> | <formula from 04> |
| Product | <counter-metric> | <formula from 06 "Undesired consequences"> |

Filled in before launch: "Product" rows come from 04, "Business" rows are ready formulas;
six-pager FAQ-6 assembles two planes (Business/Product) from this table.

### Decision criteria
- Continue if …; change if …; stop if …

### Test type, cost, owner
- …
