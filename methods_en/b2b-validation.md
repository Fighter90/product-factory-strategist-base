---
id: M-b2b-validation
lang: en
title: Validating product hypotheses in B2B — specifics, risks, techniques
course: pm
sources: ["EN mirror of the RU methodology card M-b2b-validation (knowledge/methods/b2b-validation.md); original sources are listed in the RU card"]
stages: [research, discovery, validation]
tags: [b2b, hypotheses, validation, decision-makers, pilots, sampling, sales-cycle]
related: [M-hypothesis-testing, M-evidence-design, M-in-depth-interviews, M-customers, M-jtbd, M-ab-testing, M-quant-methods, M-guerrilla-research, M-pmf-scaling]
---

# Validating product hypotheses in B2B — specifics, risks, techniques

## When to use
The product is sold to companies rather than individuals, and a problem, value, or monetization hypothesis needs validation. Standard B2C techniques (A/B on heavy traffic, mass surveys) often do not apply: the base is small, access to clients goes through people, purchases are decided by several roles. This card covers what changes in validation and how not to deceive yourself.

## Core idea
**B2B differs from B2C in data scale, not in validation logic.** The logic is the same: hypothesis → data able to refute it → decision ([[M-hypothesis-testing]]). What changes are the conditions: the population is tens–hundreds of companies instead of millions of users; each respondent is a value in itself; access goes through contacts and negotiations; the purchase decision is collective and slow.

### Four structural specifics of B2B
1. **Small population.** A market of 200 companies cannot deliver classical statistical significance. Compensation: deep qualitative study of each company, expert estimates, quantitative checks on within-company data (one client has many users), sequential pilots instead of parallel A/B.
2. **A chain of roles.** The user (who works with the product) ≠ the buyer (who pays) ≠ the decision-maker (who decides) ≠ the blocker (who can forbid it). The user's pain is real, but the purchase hypothesis is tested with the buyer and decision-maker: each has their own job ("work faster" for the user; "cut costs/risk, justify it to management" for the buyer).
3. **A long, lumpy sales cycle.** The decision takes months and depends on the budget season and relationship history. "Keen interest" in an interview often never becomes a contract: wait for the fact of payment, not enthusiasm.
4. **Deal personalization.** Every client asks for "a small customization": it is easy to take a client's wish for market demand. One happy anchor client with an individual configuration is not proof of the value hypothesis for the segment.

### Specific risks of validation
| Risk | How it looks | Countermeasure |
|---|---|---|
| Sampling bias | interviews with friendly clients you already know | a sampling plan by segments, including "cold" and churned clients |
| Voice of the wrong roles | the user's pain taken as willingness to pay | a deal-role map; separate questions for user/buyer/decision-maker |
| Politeness instead of truth | "interesting, send the deck" read as demand | count only resources as evidence: time, data, money, people |
| Wish ≠ demand | "add this little feature — we'll buy" (they won't) | test willingness to pay on the current version, not on promises |
| False generalization | one anchor client = "the whole segment behaves like this" | a minimal threshold: 3–5 companies from different segments before a segment-level conclusion |
| Scope leakage | the pilot drags on with client-specific work; the hypothesis is no longer tested | pilot boundaries fixed before the start: scope, deadline, success criterion |

**Evidence that can be trusted in B2B (strongest first):** the fact of payment/signed contract; usage of the product in the working process after the pilot (activity logs); readiness to provide data/people for integration; a detailed description of "how we solve the task now" with numbers; a stated willingness to pay (the weakest).

## Procedure
1. **Decompose the hypothesis by roles:** user/buyer/decision-maker/blocker — what each role must confirm for success; a map of interests and deal risks.
2. **Build a sampling plan by segments:** which company types are mandatory (size, industry, process maturity), how many companies per segment (at least 3–5 for qualitative conclusions), including hard-to-reach and churned ones.
3. **Run problem interviews by role:** with the user — the current process, frequency, cost of error; with the buyer — the budget process, who decides and how, what internal approval requires ([[M-in-depth-interviews]]). Look for process facts and money, not opinions about the product.
4. **Test value on the approach to payment:** a demo on the client's data; a proposal letter with price and scope; a pre-pilot agreement: the client gives data and time, you give a result. The evidence is the resources the client commits.
5. **Design the pilot with boundaries fixed before the start:** scope (what is in/out), deadline, success criterion (a specific metric on the client's data), who signs off the result. A pilot without a success criterion = endless customization.
6. **Record signals per company identically** (template: segment, roles, pain with frequency, current process, reaction to the offer, committed resources, decision) — for comparison, not scattered anecdotes.
7. **Summarize by segments:** did the hypothesis hold in each; where are the limits of the conclusion; is the anchor client an exception or the rule.
8. **Decide accounting for the sales cycle:** forecast revenue through a funnel with stage durations, not by "warm" contacts; book budget seasonality.

## Template / checklist
| Field | Fill in |
|---|---|
| Hypothesis and roles (who must confirm) | user / buyer / decision-maker / blocker |
| Segments and sampling plan | company types, at least 3–5 per segment |
| The client's decision process | who, how, which budget cycle |
| Evidence criteria | payments / resources / pilot logs / words |
| Pilot boundaries | scope, deadline, success criterion, owner |
| Signals per company | one template, comparison by segments |
| Deal forecast | funnel, stage durations, seasonality |

## Typical mistakes
- Testing the purchase hypothesis with the user instead of the buyer/decision-maker.
- Counting "interesting, send a deck" as demand evidence; evidence is client resources (money, time, data, people).
- Drawing segment conclusions from one anchor client with an individual configuration.
- Surveying only friendly companies; excluding churned and "cold" ones.
- A pilot without a success criterion fixed in advance — it becomes free outsourcing.
- Transferring B2C logic: waiting for statistical significance that a population of 200 companies cannot produce.

## Questions that can change the decision
- Who signs the contract, and what does every link in the chain need to sign?
- How many companies in the segment have confirmed the pain with process facts (not words)?
- Is even one client ready to pay for the current, imperfect version?
- What is the real budget cycle: will the pilot land in the procurement window?
- What if the anchor client is an exception: who is "average" in the segment, and have they been tested?

## Related maps
[[M-hypothesis-testing]], [[M-evidence-design]], [[M-in-depth-interviews]], [[M-customers]], [[M-jtbd]], [[M-ab-testing]], [[M-quant-methods]], [[M-guerrilla-research]], [[M-pmf-scaling]]
