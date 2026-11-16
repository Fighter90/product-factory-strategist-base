---
id: M-evidence-design
lang: en
title: Evidence design — how much and which data a decision needs
course: pm
sources: ["EN mirror of the RU methodology card M-evidence-design (knowledge/methods/evidence-design.md); original sources are listed in the RU card"]
stages: [research, validation, review]
tags: [evidence, evidence-design, triangulation, evidence-strength, decisions, research, confidence]
related: [M-hypothesis-testing, M-source-criticism, M-brief-hypotheses, M-ab-testing, M-quant-methods, M-in-depth-interviews, M-b2b-validation, M-six-pager]
---

# Evidence design — how much and which data a decision needs

## When to use
Before an expensive or irreversible decision: decide in advance what evidence it will rest on, how much is enough, and of what quality. Also — when a research result is "on the edge" and you need to know whether you can decide on it. This card answers "how much data is enough", not "how to collect data" (methods — [[M-hypothesis-testing]]).

## Core idea
**Evidence is data capable of changing the decision.** Evidence design means projecting a set of evidence against the decision: define in advance what will count as sufficient grounds, from which sources and methods to collect, and which combinations make the conclusion robust.

**Three questions of evidence design:**
1. **Sufficiency:** which minimal set of data lets the decision be made? Under-collecting — deciding on faith; over-collecting — lost weeks and "analysis paralysis".
2. **Quality (strength):** how much the data can be trusted. Strength scale: direct measurement of behavior (payments, logs, A/B) > structured self-report (surveys, diaries) > interviews and observation > expert opinion > analogy/anecdote. For sources there is a separate A–D scale ([[M-source-criticism]]). A conclusion is no stronger than its weakest critical input.
3. **Independence (triangulation):** evidence from different methods, different data, different samples. Triangulation raises confidence only if the inputs are independent: two surveys of the same base are one input, not two.

### Types of evidence relative to the hypothesis
| Type | What it is | Example | Risk |
|---|---|---|---|
| Direct | data on the very behavior/effect | A/B test of conversion, payments, logs | expensive, needs test conditions |
| Indirect | a proxy metric linked to the effect | clicks on a "fake door", prototype engagement | the proxy can drift away from the target metric |
| Testimonial | users' words | interviews, surveys, support complaints | the gap between "say" and "do" |
| Contextual | external data on the market/analogues | reports, competitor benchmarks, industry history | someone else's context ≠ ours |

**Assembling the set:** the costlier and more irreversible the decision, the more direct evidence it must contain; testimonial and indirect inputs serve to find the mechanism and early signals, not to give the final "yes".

### Sufficiency: the "stop" criterion
Fix in advance: the metric threshold (what counts as success), sample size/MDE ([[M-ab-testing]]), the number of independent inputs (usually ≥ 2 for irreversible decisions), and who declares the set sufficient. Sufficiency reached → decide, even if "we'd like to check more"; not reached → no decision or a deferred decision, not "a decision made grudgingly".

**Confidence vs proven.** The goal is not absolute truth but confidence sufficient for action: reversible decisions have a lower bar (act and learn), irreversible ones a higher bar (a strong set first). Name the confidence level explicitly in the decision document: "confirmed by A/B and payments" ≠ "confirmed by three interviews".

**Negative evidence beats confirming evidence:** look for data that would refute, not reassure. A set that in principle cannot show "no" is not evidence — it is a presentation.

## Procedure
1. **Name the decision and its cost of error** (reversible/irreversible, cost of a month on the wrong path).
2. **Write the hypothesis in testable form** and what exactly should happen to the metric ([[M-brief-hypotheses]]).
3. **Define which data could change the decision:** by type (direct/indirect/testimonial/contextual) — what would prove, what would refute.
4. **Assemble the minimal set:** start with the cheapest independent inputs; for irreversible decisions, include at least one direct input.
5. **Check input independence:** different methods, different data, different samples. Remove duplicates (two methods on the same base = one input).
6. **Fix the sufficiency criterion before collection:** thresholds, sample sizes, number of inputs, decision owner.
7. **Collect and summarize the set in a table:** input → strength → what it shows → contradictions between inputs.
8. **Resolve contradictions:** a stronger input outranks a weaker one; if two strong inputs contradict — that is a new research task (dissect the mechanism), not a reason to pick the convenient one.
9. **Write the conclusion with a confidence level:** "the decision is based on …, confidence high/medium, remaining risks …" — into the decision document ([[M-six-pager]]).
10. **Reserve a review:** on which new data the conclusion is revisited (date, trigger).

## Template / checklist
| Field | Fill in |
|---|---|
| Decision and cost of error | |
| Hypothesis (testable form) | |
| Direct evidence | what we measure, where to get it |
| Indirect/testimonial/contextual | input, strength, what it shows |
| Sufficiency criterion (before collection) | thresholds, samples, number of independent inputs |
| Contradictions between inputs | how resolved |
| Confidence level and its limits | |
| Conditions for revisiting the conclusion | new data, date, trigger |

## Typical mistakes
- A set of interviews alone for an irreversible decision (all inputs testimonial and dependent).
- Triangulation with duplicates: "three surveys" on the same base of loyal customers.
- Sufficiency criterion set after the fact: "we already have enough data to agree with my opinion".
- A proxy metric detached from the target: growth in clicks counted as success without growth in payments.
- Confirmatory search: the study design cannot produce a refutation.
- Confidence not named: the decision document does not show what the conclusion rests on and how much to trust it.

## Questions that can change the decision
- What is the single cheapest observation that could refute the hypothesis — and has it been made?
- If the strongest input in the set turned out to be wrong, would the decision change? If yes — the set is insufficient.
- Which inputs are truly independent (data, samples, methods)?
- What is our confidence level, and what does this decision require?
- What would have to happen in the world for us to revisit the conclusion?

## Related maps
[[M-hypothesis-testing]], [[M-source-criticism]], [[M-brief-hypotheses]], [[M-ab-testing]], [[M-quant-methods]], [[M-in-depth-interviews]], [[M-b2b-validation]], [[M-six-pager]]
