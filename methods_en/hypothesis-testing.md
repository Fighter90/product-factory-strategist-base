---
id: M-hypothesis-testing
lang: en
title: Choosing a method for validating a product hypothesis
course: pm
sources: ["EN mirror of the RU methodology card M-hypothesis-testing (knowledge/methods/hypothesis-testing.md); original sources are listed in the RU card"]
stages: [research, validation]
tags: [hypotheses, methods, validation, research, decision-risk, evidence, experiment, b2b, method-choice]
related: [M-brief-hypotheses, M-research-types, M-evidence-design, M-ab-testing, M-in-depth-interviews, M-quant-methods, M-guerrilla-research, M-b2b-validation, M-usability-testing]
---

# Choosing a method for validating a product hypothesis

## When to use
A product hypothesis has been formulated and the question "how do we validate it?" arises: which research method or experiment to choose, what it costs in time and money, and which risks the choice of method itself carries. This card is a selection procedure: from the type of hypothesis and the cost of a wrong decision to the minimally sufficient method.

## Core idea
**A hypothesis is not a question but a testable statement.** A product hypothesis links an action to an expected metric change: "if we do X, then Y will change by Z for segment W, because …". Validation = collecting data that can refute the hypothesis and change the decision. If the data cannot change the decision, it is not research but a ritual.

**The method is chosen not "by convention" but against three things:**
1. **Type of hypothesis.** Problem ("the segment has a pain"), value ("the solution removes the pain"), usability ("the user can complete the scenario"), channel (the channel brings the right users), monetization ("they are ready to pay this much"), growth (the mechanic adds increment).
2. **Cost of a wrong decision.** How much we lose if we are wrong: a reversible decision (a button can be removed) allows a fast cheap method; an irreversible one (shutting down a direction, changing monetization) requires strong evidence.
3. **Access to data and respondents.** Is there a user base, an A/B option, access to decision-makers in B2B (see [[M-b2b-validation]]), willingness to pay for a sample.

### Map "hypothesis type → methods"
| Hypothesis type | Fast and cheap | Costlier but stronger |
|---|---|---|
| Problem | problem interviews, observation, guerrilla research ([[M-guerrilla-research]]) | quantitative survey on a representative sample ([[M-quant-methods]]), demand-search log analysis |
| Value | clickable prototype, "fake door" (a fake pricing option on a landing page) | A/B test of value, pilot with anchor clients |
| Usability | test with 5 respondents ([[M-usability-testing]]) | moderated test on target segments, comparison against a competitor |
| Channel | small paid channel tests, CPL measurement | large-scale test with traffic-quality control |
| Monetization | willingness-to-pay survey, Van Westendorp ([[M-van-westendorp]]) | price A/B, pre-orders, selling before building |
| Growth / increment | forecast and cannibalization in the model ([[M-traction-model]], [[M-cannibalization]]) | A/B test with MDE calculation ([[M-ab-testing]]) |

### Risks of the method itself
- **The method does not answer the question.** A "would you buy…?" survey does not validate a monetization hypothesis (stated intent ≠ paying behavior); a usability test does not validate demand.
- **A method with built-in bias.** A survey of loyal customers confirms anything; interviews with colleagues instead of users; an A/B on a segment the rollout will never touch.
- **A cheap method for an expensive decision.** Saving on research before an irreversible decision is the most expensive kind of saving.
- **An expensive method for a cheap decision.** A full-scale study before changing a button label.
- **Confirmatory design.** The study is designed so that it cannot refute the hypothesis (leading questions, a "friendly" sample, no control group).

**The minimally sufficient method** is the cheapest one that can change the decision under any outcome. Start with "cheap refuters" (interviews, prototypes, logs), then move to expensive ones (sampled surveys, A/B). Principle: **learning speed per ruble**, not "rigor for rigor's sake" (see [[M-evidence-design]]).

## Procedure
1. **Rewrite the hypothesis in testable form:** what we do, for whom, what we expect to see in a specific metric, within what period, why (the mechanism). Test: what data would force us to say "no"?
2. **Estimate the cost of error:** is the decision reversible, what does a month on the wrong path cost, what breaks with a wrong rollout. The cost of error sets the required strength of evidence, and that sets the method.
3. **List 2–3 candidate methods** from the "hypothesis type → methods" map; for each: what exactly it proves or refutes, time, cost, access to respondents.
4. **Check each candidate for method risk:** can it answer "no"? where is the sampling bias? what counts as success, fixed in advance (threshold, MDE)?
5. **Choose the minimally sufficient one:** the cheapest valid option. If torn between qualitative and quantitative — start qualitative (find and understand the mechanism), then quantitative (measure prevalence).
6. **Design the check before collecting:** questions/scenario/metrics, success and failure criteria, sample size, who decides and when based on the result. Fix it in writing ([[M-brief-hypotheses]]).
7. **Run it, keep raw data** (not only aggregates): quotes, answers, logs — for auditing the conclusions.
8. **Sum up:** confirmed / refuted / not tested (the method gave no answer); strength of evidence; what happens to the decision. A refuted hypothesis is an equally valuable result; "not tested" goes back to step 3.

## Template / checklist
| Field | Fill in |
|---|---|
| Hypothesis (testable form) | if … then … for … because … |
| Hypothesis type | problem / value / usability / channel / monetization / growth |
| Cost of a wrong decision | reversible / irreversible; cost of a month on the wrong path |
| Candidate methods (2–3) | what it proves/refutes, time, cost |
| Sampling bias of the chosen method | whom we will not hear |
| Success criterion fixed in advance | metric + threshold + period |
| Failure criterion fixed in advance | what counts as "no" |
| Who decides on the result | role, deadline |

## Typical mistakes
- Testing a monetization hypothesis with "would you pay?" instead of a payment test.
- Starting with an expensive method (a full survey, A/B on heavy traffic) when 5 interviews in a day can answer.
- Not fixing the success criterion before launch — "any result will find confirmation".
- Ignoring sampling bias: surveying whoever is available instead of the target users.
- Research without a decision at the end: data collected, but it is unclear what to change.
- Treating a single method as enough for an irreversible decision ([[M-evidence-design]] — triangulation).

## Questions that can change the decision
- What data would make us say "we were wrong"? If none — the hypothesis is untestable.
- How much does a month of moving in the wrong direction cost? Are we underspending on validation?
- Which respondents are unavailable to the chosen method, and how does that bias the conclusion?
- Can the hypothesis be tested with a "fake door" in a week instead of a full build?
- Do logs or reports already contain data that confirms or refutes the hypothesis before we collect new data?

## Related maps
[[M-brief-hypotheses]], [[M-research-types]], [[M-evidence-design]], [[M-ab-testing]], [[M-in-depth-interviews]], [[M-quant-methods]], [[M-guerrilla-research]], [[M-b2b-validation]], [[M-usability-testing]]
