# Six-pager reference: structure outline (Goods Marketplace case)

> A STRUCTURE outline of the reference document "Strategy Example" (Goods Marketplace case,
> the course "Growth Strategies for Business and Product," HSE): sections, order, mandatory
> tables, and the signs of "good." Not a copy of the reference text — the scheme the
> six-pager-writer follows. The full rules spec is `SIX_PAGER_PROMPT.md` (RU) /
> `SIX_PAGER_PROMPT_EN.md`; the good/bad breakdown per FAQ is the `M-six-pager-etalon` map.

## Document shape

- ≈6 meaningful pages of main text (appendices excluded); the main text is ≤ 3500 words
  (tables and footnotes do not count) — beyond that the committee stops reading.
- Six FAQ sections with numbered sub-points (1.1, 1.2, 2.1 …); every meaningful block ends
  with a "**Conclusion (inference)**: therefore / this means …" line.
- No screenshots or images: the committee's evidence format is tables, formulas, calculations,
  and source footnotes. A number without a provenance tag is not a number.
- At the bottom — numbered source footnotes; in the text — [C###]/[S###] tags.

## Section skeleton

| Section | Length | Mandatory elements |
|---|---|---|
| FAQ-1. Current state analysis | ~1 page | 1.1 market overview: size and dynamics as ranges, a bullet forecast by year, 5–7 trends as bullets (bold headline + "what this means for the product" + an implication-opportunity); 1.2 competitor table (columns — competitor groups; rows — "Key advantages", "Growth strategy and promo mechanics", "Risks for the company" rated High/Medium/Low) + a "what nobody has yet" paragraph = the strategy window; a conclusion with the opportunity window and its timeframe |
| FAQ-2. User Persona | ~1 page | 2.1 segments table (columns — user types by entry barrier; rows — "Who are they?", "What do they use today and why?", "What difficulties do they face?", "Common difficulties") + a prioritization rationale (capacity/CAC/competition); 2.2 a "Journey stage → Barrier today → What the product does" table (acquisition → choice → payment → post-payment experience) + "what holds back signup or renewal" per segment; conclusion: segment by the barrier, the tier ladder serves all barriers |
| FAQ-3. Strategic initiatives | ~1 page | intro: which options the direction was chosen from (referencing the red team) and why; 3–4 driver initiatives — one per numbered sub-point (3.1, 3.2, 3.3…), each: "driver → Key directions (bullets) → effect calculation (formula → substitution → result)"; conclusion: the initiatives close the FAQ-2 barriers and build on existing assets |
| FAQ-4. Tactics | ~0.5–1 page | the "Strategic initiative, Focus, User needs and expectations, Solutions (tactics)" matrix: 2–4 rows per initiative; tactics are executable ("what exactly is built/changed"), not slogans |
| FAQ-5. High-level plan | ~0.5 page | the initiatives' contribution to the outcome in % — summing to 100%, each weight justified; tactic order (high → medium → base); timing to market seasons; parallel tracks (community/partnerships); a decision with commitment, deadline, review date, and a stop trigger |
| FAQ-6. Success metrics | ~0.5 page | KPIs in two planes: business (revenue/MRR, paying users, payment conversion, plan mix, LTV/CAC) and product (activation, time to first value, actions to result, churn, CSAT/NPS); every KPI: baseline → target by deadline → action threshold; counter-metrics — one per red-team hit |
| Source footnotes | ~0.5 page | a numbered list: source — title — link; every number in the document traces back to a footnote |

## Signs of "good" (why the reference works)

- The document answers the committee's questions in their order instead of recapping working
  documents: each section is a self-contained "data → grounds → calculation → conclusion" answer.
- Every trend leads to a product implication; every competitor to a risk; every barrier to the
  mechanic that removes it; every tactic to a need.
- Effects are computed, not declared: formula → substitution → result; the contribution split
  sums to 100% and explains why the weights are what they are.
- Metrics are checkable: baseline, deadline, action threshold ("at which value we change the plan").
- Ranges instead of false precision where sources disagree; the conservative bound in calculations.

## Signs of "bad" (what `pfs check --six-pager` catches)

- Pasting working documents instead of writing per the reference (verbatim lines from 02–07).
- Service references without decoding: file names, Q#, H#, WBS, "milestone M", bare D### IDs.
- Trends without "what this means for us"; competitors listed without risks; slogan tactics.
- Contribution split "roughly equal" or not summing to 100%.
- Metrics without baseline, deadline, and action threshold; conclusions not separated from data.
- Main text above 3500 words — the committee stops reading.
