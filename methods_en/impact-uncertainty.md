---
id: M-impact-uncertainty
lang: en
title: Impact × uncertainty matrix — prioritizing trends and investment in future analysis
course: strategy
sources: ["EN mirror of the RU methodology card M-impact-uncertainty (knowledge/methods/impact-uncertainty.md); original sources are listed in the RU card"]
stages: [research, options, strategy]
tags: [impact, uncertainty, matrix, trends, analysis-prioritization, scenarios, signals, horizon, no-regret, option-bets]
related: [M-trends-scenarios, M-external-environment, M-forecasting-product, M-scenario-modeling, M-market-sizing, M-source-criticism, M-risks, M-strategy-growth, M-weighted-scoring]
---

# Impact × uncertainty matrix: what to analyze, what to plan for, what to ignore

## When to use
A trend map has been assembled while the budget for future analysis is limited: what to research
deeper, what to put into strategy and the model right away, and what to ignore; defending the
strategy against a "what if…" question for every factor; a regular review of the trend map. The
method sits between horizon scanning ([[M-trends-scenarios]]) and scenario planning: it decides
which trends deserve a scenario and which deserve a registry line.

## Core idea
Two questions for every trend/factor:
1. **Impact** — how strongly it will change the product: revenue, metrics, the model, costs.
   The scale is quantitative where possible: "% of revenue in N years", "a change of the key
   metric by X%". Impact is computed **for your product**, not for the industry at large.
2. **Uncertainty** — how widely plausible outcomes scatter: the range of expert estimates, the
   width of the scenario fork, technology maturity. Uncertainty ≠ "I don't get it": it is a
   property of the future, not of one person's ignorance ([[M-source-criticism]]).

| | Low uncertainty | High uncertainty |
|---|---|---|
| **High impact** | Account for in plans now: put into the model and roadmap (no-regret moves) | Scenarios and bets: 2–4 outcomes, option bets, signals, a monitoring owner |
| **Low impact** | Background: into base assumptions, no analysis budget | Ignore: a registry with a review date |

The method closes the two extremes of dealing with the future: paralyzing analysis of everything
and ignoring everything new. The analysis budget goes only to the top-right quadrant — where the
decision depends on the outcome and the outcome is not point-predictable.

Links to other methods: trends from the top-right quadrant flow into scenario analysis and the
2×2 matrix ([[M-trends-scenarios]], [[M-scenario-modeling]]); impact is converted into model money
([[M-forecasting-product]], [[M-market-sizing]]); bets on outcomes go into the risk register
([[M-risks]]).

## Procedure

### A. Build the factor list
1. Sources: horizon scanning, a PESTEL breakdown ([[M-external-environment]]), analytical reports
   (critically checked — [[M-source-criticism]]), internal observations.
2. Each factor is one row: name, type (technology/regulation/behavior/economics), source.
3. Fix the horizon (e.g., 3 years) — impact and uncertainty depend on it; separate matrices are
   built for different horizons.

### B. Score every row
1. Impact: in product quantities (%, money, metric change); a rough estimate with a source or an
   "assumption" mark.
2. Uncertainty: the width of the plausible outcome range (e.g., "growth of 10% or a fall of 40%"
   — high; "growth of 15–20%" — low). It helps to ask 2–3 experts independently: the spread of
   their estimates is itself a measure of uncertainty.
3. Check the classic substitution separately: "uncertain to me" ≠ "uncertain in general"; if the
   market has a consensus — uncertainty is low, even if you did not know it.

### C. Place rows and handle disagreement
1. Place the rows on the matrix (a board/table). Do it as a team, not alone: different roles see
   different factors.
2. On a scoring disagreement — record both points and the arguing arguments; a persistent
   disagreement about impact is itself an uncertainty signal (raise it on the Y axis).
3. The criterion for the top-right quadrant: if the outcome turns out different, the plan/model
   changes.

### D. Actions per quadrant
1. High impact × low uncertainty → into the base model and plans; the analysis is done here.
2. High impact × high uncertainty → per row: 2–4 plausible outcomes; signals telling which one is
   unfolding; no-regret steps and option bets; a review date and an owner.
3. Low impact × low uncertainty → background in the assumptions.
4. Low impact × high uncertainty → a registry with a review date; a return rule: what must happen
   for the factor to rise to "high impact".

### E. Operating the matrix
1. Monitoring owners for the top-right quadrant; signals go into a dashboard or a regular review
   ([[M-dashboards-visualization]] for observable metrics).
2. Review quarterly/semi-annually or upon a signal firing: a factor moving between quadrants
   updates the actions.
3. Matrix conclusions feed the strategy and the growth model ([[M-strategy-growth]]) and the
   verification plan ([[M-forecasting-product]]).

## Template / checklist

**A matrix row:**
`Factor | Type | Horizon | Impact (magnitude, source/assumption) | Uncertainty (outcome range) |
Quadrant | Action (model/scenario/background/registry) | Signals | Owner | Review date`

**Matrix readiness:**
- The horizon is fixed; factors come from ≥2 types of sources.
- Impact is expressed in product quantities, not a gut "strong/weak".
- Uncertainty is a spread of outcomes, not personal ignorance.
- The top-right quadrant has: outcomes, signals, no-regret/option bets, an owner, a date.
- The ignored ones have a condition for returning into analysis.
- The next review date is scheduled.

## Common mistakes
| Mistake | Outcome | Right move |
|---|---|---|
| Gut-scored estimates without sources | The matrix is one person's opinion | Magnitudes, sources, "assumption" marks |
| Industry impact instead of your product | Analysis drifts to foreign trends | Recompute: "how much for us in money/metrics" |
| "I don't understand" taken for "uncertain" | Important factors go into ignore | The market's outcome spread, not personal clarity ([[M-source-criticism]]) |
| Built and forgotten | The matrix stales, decisions never change | Owners, signals, a review date |
| Everything lands in "high impact, high uncertainty" | Too much analysis again | The hard criterion: does the plan change with the outcome |
| No actions per quadrant | A pretty picture without decisions | Every row gets an action |
| One horizon for all factors | Tactics and breakthroughs are mixed | Separate matrices per horizon |

## Questions that can change the decision
- What is the matrix horizon, and does it match the horizon of the decision it must support?
- By which scale is impact scored, and who confirmed the magnitudes?
- How did you separate "uncertain in general" from "unknown to me"? Are there independent estimates?
- Which signals move a factor between quadrants, and who watches them?
- What share of the analysis budget went to the top-right quadrant? If little — the matrix is
  not working.

## Related maps
[[M-trends-scenarios]], [[M-external-environment]], [[M-forecasting-product]], [[M-scenario-modeling]], [[M-market-sizing]], [[M-source-criticism]], [[M-risks]], [[M-strategy-growth]], [[M-weighted-scoring]]
