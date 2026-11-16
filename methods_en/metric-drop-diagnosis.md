---
id: M-metric-drop-diagnosis
lang: en
title: Metric movement diagnosis — when a drop is not a problem and how to find the cause
course: data
sources: ["EN mirror of the RU methodology card M-metric-drop-diagnosis (knowledge/methods/metric-drop-diagnosis.md); original sources are listed in the RU card"]
stages: [research, validation, after-decision]
tags: [metric-diagnosis, drop, seasonality, mix-shift, data-quality, cannibalization, noise, counter-metrics, alerts, decomposition]
related: [M-product-metrics, M-basic-statistics-pm, M-dashboards-visualization, M-ab-testing, M-cannibalization, M-event-taxonomy, M-success-metrics, M-traction-model, M-model-validation, M-loyalty-metrics, M-cjm]
---

# Metric movement diagnosis: when a drop is not a problem

## When to use
A metric dropped (or unexpectedly jumped) and you must decide whether to fix it or accept it as
normal: a dashboard alert, leadership asking "why did conversion fall", a backlog ticket "fix the
metric". The rule: diagnosis before treatment. The method answers two questions: (1) is there a
problem at all, (2) if yes — where exactly and why.

## Core idea
Metric movement is a signal, not a diagnosis. A drop can be normal or harmless:

| Cause of a "normal" drop | How to recognize it |
|---|---|
| Seasonality / day of week / calendar | The drop repeats every year/week at the same time |
| Mix shift in structure | The share of a low-metric segment grew; within each segment the metric holds |
| Data quality | Lost events, SDK migration, duplicates, a "jump" at the moment of a tracking release |
| Self-cannibalization | A new feature/channel took traffic from the old path; in total — growth ([[M-cannibalization]]) |
| External factors | Holidays, weather, news, competitor moves, regulation |
| Base effect | The previous period was abnormally high (a viral spike, a promo) |
| Noise / small sample | Volatility within the historical range; the confidence interval covers the baseline |

Diagnosis goes through decomposition: the metric is split into factors (e.g., conversion =
visits × depth × target action / visits) and into segments (channel, platform, new/returning
audience, geo). The drop is always located in a specific branch of the decomposition — that is
where the cause lives.

Two different questions that must not be mixed:
- **Mix or behavior?** The "hospital average" fell because the audience composition changed (mix)
  — then look at the metric inside segments.
- **Noise or shift?** The deviation is within the historical volatility (per a control chart or
  interval — [[M-basic-statistics-pm]]) — observe, don't fix.

## Procedure

### A. Check the data (first of all)
1. Is collection broken: do events arrive at all, SDK/tag versions, migrations, limits.
2. Is there a sharp step at the moment of a tracking/app release — a sign of a data problem,
   not a product one.
3. Cross-check with an independent source: payment system, server logs, CRM export.

### B. Compare periods correctly
1. Compare comparable windows: week over week, month over month in the same season; not "monthly
   average versus yesterday".
2. Align day of week and calendar (holidays, promos, month length).
3. The "normal" boundary: the metric's historical volatility (σ over past windows, intervals —
   [[M-basic-statistics-pm]]); deviation within it is noise.

### C. Decompose and find the branch
1. Split the metric into factors and segments ([[M-product-metrics]]: metric passport, tree).
2. Find the branch where the drop actually is: compare each segment with its own past period.
3. Separate the two mechanisms: traffic composition changed (mix) or behavior within the segment.

### D. Find the cause inside the branch
1. Your own changes: releases, experiments ([[M-ab-testing]]), price/plan changes, new channels,
   disabled integrations in the drop window — a change timeline against the metric timeline.
2. External factors: seasonality, news, competitor moves, regulation, weather.
3. Cannibalization: did traffic flow into another product path ([[M-cannibalization]])?
4. Counter-metrics and adjacent metrics: does the funnel one step earlier/later confirm the
   picture ([[M-loyalty-metrics]] for loyalty, events — [[M-event-taxonomy]])?

### E. Classify and decide
1. Verdict: noise → observe; normality (season/mix) → explain and update expectations in the
   model ([[M-model-validation]], [[M-traction-model]]); problem → a cause hypothesis.
2. For a problem: hypothesis + the cheapest verification (retro-analysis, A/B rollback of the
   feature, interviews with affected users) + owner + deadline.
3. Update alerts: thresholds accounting for volatility and seasonality so noise is not caught
   ([[M-dashboards-visualization]]).
4. Record the analysis: what happened, the cause, the action — a base for the next diagnosis.

## Template / checklist

**A diagnosis passport (one page):**
`Metric | Comparison window | Deviation (size, share of baseline) | Data verified (yes/no) |
Decomposition branch where the drop is | Mix or behavior | Cause hypothesis | Verification |
Verdict (noise/normal/problem) | Owner | Deadline`

**Criterion "the drop is not a problem":**
- The deviation is within the historical volatility of the comparison window.
- Season/day of week/calendar explain the movement; last year behaves the same.
- The metric within every segment holds; only the structure changed.
- The data is confirmed by an independent source.

## Common mistakes
| Mistake | Outcome | Right move |
|---|---|---|
| Fixing without decomposition | "Repairing" a healthy segment while the real one is not found | First decompose into factors and segments |
| Comparing incomparable windows | Panic from seasonality | Week over week, season over season |
| Ignoring data quality | Chasing a phantom, "fixing" tracking with product work | Collection check is always the first step |
| Taking mix for behavior | A working feature gets blamed | Compare a segment with its own past |
| Taking noise for a shift | A fire drill from a random fluctuation | Volatility and intervals before alerts ([[M-basic-statistics-pm]]) |
| "It fell — the last release is guilty" | Rolling back working code without verification | Change timeline against metric timeline |
| A one-off analysis with no consequences | The same drop next month — a new fire | Record the analysis, update alert thresholds |
| Hospital average instead of segments | The problem is smeared and invisible | A segment cut is mandatory ([[M-product-metrics]]) |

## Questions that can change the decision
- What volatility is normal for this metric, and who recorded it?
- What changed in the audience composition over the comparison window (mix)?
- Which events in and around the product coincided with the start of the drop?
- Does an adjacent metric or funnel step confirm the same picture?
- If it is mix or season — which expectations in the plan/model must be updated, instead of
  fixing the metric?

## Related maps
[[M-product-metrics]], [[M-basic-statistics-pm]], [[M-dashboards-visualization]], [[M-ab-testing]], [[M-cannibalization]], [[M-event-taxonomy]], [[M-success-metrics]], [[M-traction-model]], [[M-model-validation]], [[M-loyalty-metrics]], [[M-cjm]]
