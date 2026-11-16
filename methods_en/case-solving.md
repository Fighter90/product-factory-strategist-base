---
id: M-case-solving
lang: en
title: Product case solving — from a raw problem to a testable solution under time pressure
course: pm
sources: ["EN mirror of the RU methodology card M-case-solving (knowledge/methods/case-solving.md); original sources are listed in the RU card"]
stages: [research, options, validation]
tags: [case, as-is, root-problem, solution-hypotheses, decomposition, effect-metrics, assessment-criteria, verdict, time-boxing]
related: [M-problem-design, M-solution-design, M-jtbd, M-cjm, M-prioritization-ricews, M-product-metrics, M-hypothesis-testing, M-evidence-design, M-mvp-pilots, M-competitors, M-product-frameworks]
---

# Product case solving: from a raw problem to a testable solution

## When to use
When a product task needs a structured answer within limited time: hiring rounds and case
championships, defending an initiative before a committee, a quick "what do we do with this
product" request from leadership, starting work on an unfamiliar problem. The method also serves
the agent: a case is a compressed formula of real product work — the same steps, condensed and
with explicit quality criteria.

## Core idea
A case is a packaged real problem: raw data, conflicting interests, unstated context. The solution
is judged not for a "guessed answer" but for the structure of reasoning and the discipline of
evidence: did you reframe the problem, ground it in data, reach the root cause, propose genuinely
different options, tie the effect to metrics, name risks and a way to verify.

The solution skeleton (expanded in "Procedure"):

| Stage | Question | Output |
|---|---|---|
| 1. Re-read and reframe | What is actually asked: problem, metric, or solution? | Your own one-two sentence task statement |
| 2. AS-IS | How does it work now, through the client's and the business's eyes? | Journey/scenario map ([[M-cjm]]), metric tree |
| 3. Root problem | Why does the metric/pain exist? Is it a symptom? | Problem statement ([[M-problem-design]]) |
| 4. Segments and jobs | Who hurts and which job do we serve? | 1–3 segments, JTBD ([[M-jtbd]]) |
| 5. Solution hypotheses | Which other ways could close the job? | ≥3 genuinely different options |
| 6. Prioritization | What do we do first and why? | Scoring ([[M-prioritization-ricews]]), trade-offs |
| 7. Effect and metrics | What changes and how do we measure it? | Baseline → target shift ([[M-product-metrics]]) |
| 8. Risks and verification | What can go wrong and how will we know? | Top risks, MVP/pilot ([[M-mvp-pilots]]) |
| 9. Verdict | What do we propose and what do we do tomorrow? | Explicit decision + first steps |

A rule common across case practices: a solution without metrics and verification is an "idea",
not a solution; a solution without the root problem is a decoration of the symptom.

## Procedure

### A. Preparation (5–10% of time)
1. Read the prompt twice. Write down: who the decision's customer is, what is explicitly asked,
   the constraints (time, resources, regulation, platform), and which data is given.
2. Reframe the task in your own words and check it against the prompt: "We solve… for…, because…,
   success looks like…". If the framing drifts — clarify with the "customer" (in a championship,
   ask the jury/organizers; in real work — the problem owner).
3. A time plan: allocate the minute budget across the skeleton stages upfront and watch the clock.

### B. AS-IS and the root problem (25–30% of time)
1. Assemble the "how it works now" picture: the client journey step by step (actions, barriers,
   emotions — [[M-cjm]]), segment economics/metrics, key players and competitors ([[M-competitors]]).
2. Mark the break points: where conversion drops, where support calls appear, where workarounds.
3. Reach the root problem ("5 whys" or a cause tree): symptom → mechanism → cause. Check: if this
   cause is fixed, does the symptom go away? If not — dig further.
4. Pick 1–3 segments with the highest pain × reach; for each — the client job ([[M-jtbd]]).

### C. Solution hypotheses and prioritization (25–30% of time)
1. Generate ≥3 genuinely different options (not variations of one): different mechanisms,
   different segments; "do nothing / change the process" is also an option. Ideas come from AS-IS
   barriers, market analogues, and removing the client job ([[M-solution-design]]).
2. Write each hypothesis as: "If [mechanism] for [segment], then [metric] shifts from X to Y,
   because [reason]" ([[M-hypothesis-testing]]).
3. Score the options by Impact/Reach/Confidence/Effort or cheaper: benefit × likelihood × cost.
4. Pick the main option and state explicitly what you rejected and why — assessors check exactly
   this awareness of rejection.

### D. Effect, risks, verification (20–25% of time)
1. Effect in metrics: baseline (where the number comes from), target shift (by how much and why it
   is realistic), counter-metrics (what must not degrade).
2. Economics: a rough unit estimate (ARPU / acquisition cost / unit margin) or P&L impact — at
   least the order of magnitude and the assumptions.
3. Risks: top-3 with type and mitigation; value/feasibility/business risks ([[M-solution-design]]).
4. Verification: the cheapest way to learn the hypothesis is true — prototype, pilot, A/B,
   dashboard ([[M-mvp-pilots]]); verification deadline and the "continue/pivot" criterion
   ([[M-evidence-design]]).

### E. Verdict and presentation (10–15% of time)
1. A one-paragraph verdict: problem → chosen solution → expected effect → first verification.
2. First steps: 2–3 actions with owners and deadlines.
3. Presentation: "problem → solution" structure, one thought per slide/paragraph, numbers with a
   source; pre-answer the jury's/customer's expected objection.

## Template / checklist

**Readiness of the case solution:**
- The task is reframed in your own words; constraints are named.
- AS-IS relies on the case data or its assumptions are marked.
- The root problem is named, not the symptom; the "cause → symptom" logic is checked.
- Segments chosen with a criterion (pain × reach); the client job is formulated.
- ≥3 genuinely different options; the choice and the rejections are explained.
- Effect in metrics: baseline → target; counter-metrics named.
- Risks and the verification method stated; the first check is cheap and dated.
- The verdict fits one paragraph and reads without context.

## Quality criteria
- The task is restated in your own words with constraints; it is clear what is actually asked: problem, metric, or solution.
- The root problem is reached: "if we remove it, the symptom goes away" is verified, not assumed.
- The AS-IS picture relies on the case data; missing data is marked as assumptions, not invented.
- There are at least three substantially different options; the choice and conscious rejections are explained.
- The effect is expressed in metrics with a baseline and a target shift; counter-metrics and the order of magnitude of the economics are named.
- The verdict fits one paragraph: problem → solution → effect → first validation; first steps have owners and deadlines.

## Common mistakes
| Mistake | Outcome | Right move |
|---|---|---|
| Jumping to the solution in the first minute | Solving the symptom; the jury sees no analysis | AS-IS and the root problem first |
| One option presented as the only possible one | No comparison — no grounded choice | ≥3 options + explicit rejection of the rest |
| Metrics like "conversion will grow" without a baseline | The effect is unverifiable | Where the number comes from, by how much, why realistic |
| Ignoring the case constraints (time, money, law) | Beautiful but unimplementable | Constraints go into the task reframing |
| Volume instead of structure | The assessor cannot find the thinking in the text | The 9-stage skeleton, one thought per block |
| The segment "all users" | For no one in particular | 1–3 segments with a selection criterion |
| No verdict ("next we need to study…") | There is no decision — only a study plan | An explicit decision + what we verify first |
| Invented numbers without a source | Trust drops for the whole solution | Case data, analogues, an "assumption" mark |

## Questions that can change the decision
- What is actually asked: problem diagnosis, metric choice, or a ready solution? The same case
  story may require any of the three.
- Which data is given and which is missing? Say plainly what the case data cannot tell you,
  instead of inventing it.
- Does the solution survive honest assumptions, not only optimistic ones?
- Who will verify the solution and when? Without verification it is belief, not a decision.
- What must the "customer" of the solution see to say "yes"?

## Related maps
[[M-problem-design]], [[M-solution-design]], [[M-jtbd]], [[M-cjm]], [[M-prioritization-ricews]], [[M-product-metrics]], [[M-hypothesis-testing]], [[M-evidence-design]], [[M-mvp-pilots]], [[M-competitors]], [[M-product-frameworks]]
