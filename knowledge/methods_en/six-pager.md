---
id: M-six-pager
lang: en
title: Six-pager — a six-page strategic report with Excel appendices
course: pm-approaches-en
sources: ["EN mirror of the RU card; original sources listed there"]
stages: [options, strategy, validation, review]
tags: [six-pager, report, committee, excel-appendices, strategy-review, decision-support]
related: [M-market-sizing, M-traction-model, M-unit-economics, M-outcome-roadmap, M-success-metrics]
---

# Six-pager

## When to apply
When a recommendation is defended before a committee/leadership: a compact (~6 meaningful pages)
document in a fixed structure, where each section answers a known question and the numbers are
computed in Excel appendices, not "in thin air". In the agent it is a three-step chain:
`pfs export --six-pager` → the `six-pager-writer` subagent → `pfs check --six-pager` until 0 errors.

## Core idea
The tool never pastes documents 02/03/04/06 into the six-pager — the work is split:

| Step | What happens | What you get |
|---|---|---|
| 1. `pfs export --six-pager` | the tool builds the **data pack** and the **skeleton** | `outputs/six_pager_pack.json` (+ .md): claims with evidence strength (kind/grade), situation from 02, options and choice from 03, decisions, KPIs from 06, calcs.json calculations, sources; `outputs/SIX_PAGER.md` — the FAQ-1…6 skeleton with `[СЛОТ …]` slots and computed blocks (unit economics, tactics matrix, KPI table, footnotes, appendices) |
| 2. the `six-pager-writer` subagent (deep) | writes the text into the slots per the reference spec, **from the pack only** | the committee document: numbers with [C###]/[S###] tags, a "Conclusion (inference)" in every block, ≤ 3500 words of main text |
| 3. `pfs check --six-pager` | the mandatory cycle until 0 errors | gates: slots closed, reference structure (1.1–2.2, 3.1–3.3), contribution 100%, matrix, KPI planes, no service IDs or pasted documents |

Six FAQ sections, each answering a decision-maker's question (what feeds it — the data pack):

| Section | The reader's question | What fills it (the data pack, not pasted files) |
|---|---|---|
| FAQ-1 | What is happening in the market, who are the competitors, what is the challenge? | pack → situation + claims: size and dynamics as ranges, 5–7 trends with "what this means for the product", the competitor table with risks; "what nobody has yet" = the strategy window |
| FAQ-2 | Who are the users and their pains across the journey? | pack → situation + claims: segments by entry barrier, barriers by journey stage, "what holds back signup" |
| FAQ-3 | Which initiatives do we propose and why these? | pack → options + choice + claims: intro on the chosen direction (with the red team) and 3–4 driver initiatives, one per sub-point 3.1–3.3+, effect calculation (formula → substitution → result) |
| FAQ-4 | What exactly does each initiative consist of? | pack → options + choice: the "Initiative, Focus, Needs, Solutions (tactics)" matrix, 2–4 rows per initiative |
| FAQ-5 | How do we implement it and know it worked? | pack → kpi + decisions: contribution split in % (sum 100) with weight rationale, tactic order, season timing, parallel tracks, the decision with a stop trigger |
| FAQ-6 | Which metrics define success? | pack → kpi + calculations: business and product KPIs, baseline → target by deadline → action threshold, counter-metrics per red-team hit |

Structure rules: the contribution split sums to 100%; every initiative has strong objections;
"keep as is" and "shut the direction down" are full-fledged alternatives; the competitor table maps
"advantage → risk for us"; tactics are tied to needs, not features. The good/bad breakdown per FAQ —
the `M-six-pager-etalon` map.

## Procedure (agent)
1. Wait until `02_situation.md`, `03_options.md`, `04_product_strategy.md`, `06_validation_plan.md`
   exist — they feed the data pack but are not the document's structure (see the `six-pager` skill).
2. Collect calculation parameters from the claim registry into `projects/<slug>/calcs.json`
   (every value → C###).
3. Via a background subagent: `pfs calc all` → `outputs/attachments/*.xlsx` (unit economics, growth
   model, cohorts, market sizing; an editable "Input" sheet, formula-driven calculations).
4. `pfs export --six-pager` → data pack + skeleton; run the `six-pager-writer` subagent — text into
   the slots from the pack, never pasting 02–07. The EN version — per `SIX_PAGER_PROMPT_EN.md`.
5. `pfs check --six-pager` until 0 errors; `pfs check --strict`; show the leader the appendices list
   and what to edit in them.

## Template / checklist
- [ ] every section answers its own question instead of recapping a neighbour;
- [ ] numbers only with [C###]/[S###]; values in the text match Excel;
- [ ] every initiative has objections and a contribution share (sum = 100%);
- [ ] metrics with formulas, units, period and target value;
- [ ] validation plan: comparison baseline, deadline, counter-metrics, proceed/change/stop criteria;
- [ ] `pfs check --six-pager` — 0 errors.

## Typical mistakes
- "Nice text without calculations": numbers without a model and a source cannot be checked.
- Tactics without needs: a feature list instead of "pain → mechanic → expected effect".
- Gluing instead of writing: pasted 02/03/04/06 text instead of slots per the reference — the
  document does not answer the committee's questions in their order (the `pfs check --six-pager`
  gate catches verbatim lines).
- An overloaded FAQ-1: market history instead of "what this changes for the decision".
- Metrics without a comparison baseline and a deadline — "we will grow loyalty" is not checkable.
- Excel with "dead" numbers instead of formulas: an assumption cannot be probed.

## Questions that can change the decision
- What is each initiative's contribution to the target metric, and what is it based on?
- What should happen for us to abandon the initiative (the stop criterion)?
- Which number in the model is the most fragile, and what confirms it cheapest?

## Related maps
[[M-market-sizing]], [[M-traction-model]], [[M-unit-economics]], [[M-outcome-roadmap]], [[M-success-metrics]]
