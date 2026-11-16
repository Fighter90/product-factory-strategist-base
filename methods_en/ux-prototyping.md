---
id: M-ux-prototyping
lang: en
title: Prototyping for UX testing — fidelity levels and testing hypotheses on a prototype
course: ux
sources: ["EN mirror of the RU methodology card M-ux-prototyping (knowledge/methods/ux-prototyping.md); original sources are listed in the RU card"]
stages: [options, validation]
tags: [prototype, fidelity, sketch, wireframe, clickable-prototype, tasks, iteration, ux-test, interface-hypothesis]
related: [M-usability-testing, M-ux-frameworks, M-ux-heuristics, M-cjm, M-design-thinking, M-genai-prototyping, M-mvp-pilots, M-solution-design, M-guerrilla-research, M-ux-backlog, M-dogfooding]
---

# Prototyping for UX testing: fidelity levels and hypothesis checks

## When to use
When you need to check whether users understand the path and whether the interface solves their
task — before development: a design dispute is cheaper to settle with a prototype than with a
release; preparation for a usability test; verifying the to-be CJM ([[M-cjm]]; defending a
solution to stakeholders with a working mock-up instead of words. A prototype answers "is this
worth building?", not "how will it look".

## Core idea
**A prototype is a hypothesis carrier.** It exists so that something can be tested on it: is the
path clear, is the next step's logic visible, does the screen remove anxiety. Anything not being
tested is extra weight and risk: a polished mock-up invites trust the hypothesis has not earned.

Fidelity levels and what is testable on each:

| Level | What it is | Testable questions | Cost/speed |
|---|---|---|---|
| Sketch/paper | Hand-drawn screens, "screens" shuffled by hand | Concept: is the idea clear, is the step order logical | Minimal, hours |
| Wireframe | Black-and-white structure: blocks, fields, hierarchy | Screen structure: what users notice, what they skip | Low, days |
| Clickable prototype | Interactive navigation between screens | Path: does the user find the scenario, where does it break | Medium |
| Code prototype | A working build on real data, not the product | Details: wording, delays, real content | High |

The selection rule: **fidelity = the minimum at which the tested hypothesis is still testable.**
The hypothesis "the user understands the step sequence" is tested by paper; "the user finds the
right menu item" — by a clickable prototype; "the button wording does not scare them" — by a code
or high-fidelity mock-up. Higher fidelity raises the cost of changing edits — so iterations run
from low to high levels, never the other way around.

## Procedure

### A. Hypothesis and test plan
1. Formulate the interface hypothesis: "If [design decision], then the user [behavior], because
   [reason]" — and the test question the prototype will answer.
2. The test's success metric: % of users completing the task; time; error count; verbal comfort
   ("easy/got lost") ([[M-usability-testing]]).
3. User tasks: 3–5 realistic tasks ("send the March report"), not interface instructions ("open
   the menu").

### B. Choose the fidelity level
1. From the levels table, by hypothesis: the minimum sufficient one.
2. Limit the prototype's scenario to the exact path being tested; other branches get honest
   stubs saying "not implemented in the prototype".
3. Realistic content in critical places (titles, numbers, objects from the user's world) — on
   "lorem ipsum" users behave differently.

### C. Build and dry-run inside the team
1. Build the prototype; add date/version to compare iterations ([[M-ux-backlog]]).
2. Dogfooding: 1–2 passes by colleagues through the test tasks ([[M-dogfooding]]); fix obvious
   path breakers before user tests — do not spend their sessions on internal bugs.

### D. Test with users
1. 5–8 users of the target segment; the scenario uses the planned tasks; moderated or
   unmoderated format by budget ([[M-usability-testing]], [[M-guerrilla-research]]).
2. Record: where they hesitated, what they re-read, where they erred, what they said; behavior
   matters more than opinion.
3. After each session — a 2-minute findings note; a pattern = repetition by 2+ participants.

### E. Iteration and decision
1. Findings go to the UX backlog, split into: "fix the prototype", "change the hypothesis",
   "a question for the data" ([[M-ux-backlog]]).
2. Edits to critical steps → re-test only those steps (not the whole scenario).
3. Exit from the loop: tasks complete at the target user share within acceptable time — the
   hypothesis is confirmed; otherwise change the design solution ([[M-solution-design]]).
4. The build decision: the prototype became the path specification; into development with notes
   on what was a stub ([[M-mvp-pilots]] for a live-traffic check).

## Template / checklist

**Prototype readiness for the test:**
- Hypothesis and test question written; success metric defined.
- Fidelity level is minimally sufficient for the hypothesis.
- The scenario covers the tested path; non-working branches are honestly marked.
- Tasks are phrased in the user's terms, not the interface's.
- Dogfooding inside the team passed without path breakers.
- Users are the target segment; 5–8 participants planned.
- A findings format is ready (a note after each session).

## Quality criteria
- The interface hypothesis and the test question are written down; the success metric is defined before the build.
- Fidelity is minimally sufficient for the hypothesis; iterations go from lower to higher levels.
- Tasks are phrased in user terms; non-working branches are honestly stubbed.
- The prototype passed dogfooding before user sessions; content in critical places is realistic.
- The test runs on 5–8 users of the target segment; behavior is recorded, not opinions.
- The loop is closed: findings led to fixes and a re-test of the critical steps; exit by the target task-completion rate.

## Common mistakes
| Mistake | Outcome | Right move |
|---|---|---|
| Polishing the mock-up instead of testing | Time goes to beauty, the hypothesis is untested | Fidelity by hypothesis, not ambition |
| High fidelity for an early concept | Expensive to change; edits get skipped to protect the work | Sketch → wireframe → clickable, stepwise |
| Testing "like/dislike" | Opinion instead of behavior; false conclusions | Tasks and observation ([[M-usability-testing]]) |
| The prototype promises more than the release | Users get used to ghost features | Honest stubs, a clear release scope |
| Lorem ipsum in critical places | Users behave artificially | Realistic content where it matters |
| One test "for everyone", no iterations | Findings collected but never verified by edits | The loop: edit → re-test the critical steps |
| Skipping dogfooding | User sessions wasted on internal bugs | 1–2 colleague passes before the test |
| A prototype without version/date | Iterations incomparable, conclusions mixed | Version it like code ([[M-ux-backlog]]) |

## Questions that can change the decision
- Which hypothesis does this prototype test, and which user behavior measures it?
- What is the minimum sufficient fidelity — are we building clickable where paper would do?
- Who are the target test participants and how do they enter the sample?
- How many iterations are planned and what is the stopping criterion?
- What will actually ship from the prototype, and what is a stub?

## Related maps
[[M-usability-testing]], [[M-ux-frameworks]], [[M-ux-heuristics]], [[M-cjm]], [[M-design-thinking]], [[M-genai-prototyping]], [[M-mvp-pilots]], [[M-solution-design]], [[M-guerrilla-research]], [[M-ux-backlog]], [[M-dogfooding]]
