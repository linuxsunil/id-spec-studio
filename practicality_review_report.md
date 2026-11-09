# Practicality Review Report

**Reviewer:** Practicality Reviewer
**Document reviewed:** docs/designs/pricing-objection-handling.md (v0.1, Draft, 2026-11-09)
**Date:** 2026-11-09
**Rubric:** resources/id-review-standard.md, Standard 8 (Practicality and Buildability)
**Context files:** None (spec alone)

## Constraint Summary

**Stated constraints:**
- Authoring tool: Rise 360 only. Storyline is out of scope (Section 9, line 174).
- Seat time: about 30 minutes, self-paced, SCORM (Section 2, line 27; Section 6, line 129).
- Media: text, static graphics, Rise interactive blocks. No video, no voiceover (Section 9, line 176).
- Build window: three weeks, one instructional designer (Section 10, line 187).
- Learners: about 50 reps in the first cohort (Section 2, line 22).
- SME: sales director owns differentiators and objection scripts. Sign-off has no date (Section 10, line 188; Section 12, line 228).
- Manager: 15-minute role-play per rep, plus two observed live calls per rep (Section 6, lines 131-133; Section 10, line 191).
- Pilot, accessibility checks, SCORM upload, and LMS testing are named as work that must fit in the build (Section 10, lines 187 and 194).

**Unstated or unconfirmed constraints:**
- LMS: not named. SCORM version not confirmed (Section 9, line 179; Section 12, line 225).
- Accessibility standard: WCAG 2.1 AA is proposed, not confirmed (Section 9, line 178).
- Manager capacity: not committed (Section 10, line 191).
- Observation mechanism for live calls (recording or listening tool, consent, rep access): not stated.
- Deal-math figures and the cost of the gap: not quantified (Section 1, line 16; Section 12, line 217).
- Differentiators and objection scripts: not in the spec and not yet approved.
- Build-hour estimate: 20-25 hours, with no per-module breakdown (Section 10, line 187).
- Calendar dates for the three-week build: not set.

## Findings

### 🔴 Blockers

[Finding ID: practicality-1-1] Lines 46, 101-102, 108-111, 147-153, 188, 228, 232-237: The content the build depends on does not exist yet. The five approved differentiators, the five objection scripts, and the prospect lines for Modules 2-5 are not in the spec. The SME who owns them (the sales director) has no review window and no sign-off date (Section 12, line 228). The spec itself says "No approved content means no drafting of Modules 2-5" (line 188). Section 13 has "Ready for build" unchecked. Modules 2-5 carry about 25 of the 30 minutes and every formative and summative item. A three-week build cannot start on those modules until the sign-off arrives, and the spec does not say when that will be. Recommendation: Add an approved content inventory (five differentiators, five scripts, five prospect lines with tone notes) as an appendix or a named input. Set a dated sign-off gate before build starts, and name a backup reviewer if the sales director is unavailable. Re-anchor the three-week schedule to that gate date.

[Finding ID: practicality-1-2] Lines 101, 164, 12-16 (Section 1), 217: Module 1 requires a "worked numeric example" of the deal math, using "their own numbers" (line 164). The cost of the gap is "not yet quantified" and discount amounts are missing (line 16; Section 12, line 217). Nothing stated in the spec or the brief makes these figures available to the designer. Module 1, objective 2, and the scenario-choice item at the end of Module 1 (line 142) all depend on them. Without the figures, Module 1 cannot be authored. Recommendation: Obtain the sales ops figures (average deal size, discount depth, win-rate delta, sample rep data) before build. Confirm who supplies them and by what date. If the figures are not available, state a labelled illustrative example that the SME approves, and remove the claim that the example uses the reps' own numbers.

[Finding ID: practicality-1-3] Lines 131-133, 145, 157, 191: The terminal objective (line 46) is assessed only by two observed live calls per rep, scored by the manager, plus a 15-minute role-play per rep (about 100 observed calls and 50 role-plays for the cohort). Manager time is "not yet committed" (line 191). The course itself cannot assess the terminal behavior (line 157). If the manager capacity is not there, the terminal objective has no assessment path. The spec has no fallback. Manager observation time is not stated, but a live call observation takes the manager's full call length, and that is not in any estimate. Recommendation: Confirm in writing how many managers will observe, how many calls each can cover, and the observation time per call. Set the launch date only after that confirmation. If capacity is short, state which reps or cohorts are exempt from the observed-call pass rule, or narrow the terminal objective to what the course can assess.

### 🟡 Major

[Finding ID: practicality-1-4] Line 187: The 20-25 build-hour estimate covers only "one review cycle" of content. The spec states that SME review, accessibility checks, SCORM upload, LMS testing, and the pilot are excluded from that figure, and it adds that accessibility and LMS testing are "not counted in the estimate" (line 194). Those excluded tasks are part of the three-week plan. The figure is also at the low end of the range for new Rise 360 self-paced work (40-60 development hours per seat-time hour, which gives 20-30 hours for 30 minutes), and branching scenarios push the work toward the upper end. No per-module breakdown supports the figure. Recommendation: Produce a per-module hour breakdown that covers authoring, SME review, accessibility, SCORM and LMS testing, the pilot, and the manager materials. Set the total against the three-week calendar and show the margin. State the estimate as a range.

[Finding ID: practicality-1-5] Lines 109-113, 115, 141-145: The branching design is the largest build cost, and its size is not bounded. Each of the five objections has a three-step branch: acknowledge, pivot, and qualify. Each step has multiple choices, and each wrong choice has its own feedback. Each choice also shows the prospect's response (line 143). That is at least 45 choice points with feedback, before counting the prospect response screens, the worked and partly-completed versions, the part-task drills (line 113), and the Module 5 whole-task exchange. The branch cap per objection is still an open question (line 221). Rise 360's scenario block authors each branch by hand. Recommendation: Set a branch cap (for example, three options per step with one feedback screen per wrong choice) and write it into Section 5. Count the authored screens per module and add that count to the build estimate. If the cap cannot be met in three weeks, cut the number of objections in the independent branch rather than the depth of feedback.

[Finding ID: practicality-1-6] Lines 123-127, 153, 155: Seat time does not match the content in Modules 4 and 5. Module 4 covers three hard objections in 8 minutes (line 126). That includes three worked examples, three partly-completed items, three independent branches with feedback, and the part-task drills before each branch: about 9 interactions and 3 drills in 8 minutes. Module 5 covers a whole-task exchange across all five objections, the discount-first error-spotting item, a summary, and the summative items, in 7 minutes (line 127). The summative items carry the 80% pass threshold (line 155). Retakes of up to two times are allowed (line 155), and retake time is not counted in seat time. The spec's own open question on this (line 223) confirms the risk. Recommendation: Either lengthen Modules 4 and 5 and re-state the seat time as 35-40 minutes, or cut content. The cut should be one objection from Module 4 or the drills. Run a timed pilot of Module 4 before build, and state the retake time separately from seat time.

[Finding ID: practicality-1-7] Lines 38, 144, 147: Objective 4 requires the learner to find the discount line in a transcript and name the skipped step, using "Rise quiz block." Rise 360's quiz blocks are built on standard item types (for example, multiple choice, matching, sequence, fill-in). The spec does not show that any of them lets a learner click or select one line within a transcript. The persona's standard is that every stated interaction type is achievable in the stated tool. This item is not verified. If the block does not support it, the item becomes multiple choice, and objective 4 is then assessed at a lower level than its Analyze verb. Recommendation: Verify in Rise 360 that the chosen block can do line-level selection in a transcript. If not, define the fallback (for example, a multiple-choice item that asks which line is the discount, or a multiple-response item) and state the Bloom's-level effect in Section 7.

[Finding ID: practicality-1-8] Lines 46, 187, 209: The cut line in Section 10 (line 187) contradicts the terminal objective. The cut line says that if the SME review slips, one Module 4 objection moves to a later release. The terminal objective (line 46) requires a response to "any of the five pricing objections." Dropping one objection means the course does not meet the terminal objective it is built to meet, and the live observation pass rule still counts all five. The spec does not say what changes in the pass rule or the observed-call checklist. Recommendation: Define the release-1 terminal objective for the four objections that will ship. State explicitly how the fifth objection is handled in the observed-call checklist (for example, held back until release 2). Alternatively, set the cut line to remove scope from Module 5 instead, and say which summative items are affected.

[Finding ID: practicality-1-9] Lines 179, 178, 225, 194: The LMS is not named, the SCORM version is not confirmed, and the accessibility standard is proposed but not confirmed. A SCORM upload and LMS test cannot be planned without the LMS and version. Accessibility checks depend on the confirmed standard. Recommendation: Name the LMS, its SCORM version, and the test environment (sandbox or production). Confirm WCAG 2.1 AA with the LMS owner. Add the LMS test and accessibility check to the build schedule as named tasks with durations.

[Finding ID: practicality-1-10] Lines 133, 145, 191: The observed-call measure depends on a mechanism the spec does not name. The manager scores "two observed live calls per rep." The spec does not say whether observation is live listening, call recording, or a call-coaching tool. It also does not address consent for recording, rep access to recordings, or where the scored checklist is stored. Those choices affect whether the measure can run at all. Recommendation: Name the observation method and the tool used to store scores. Confirm the company's call-recording policy and consent process. Confirm that managers can access the call recordings or listen live. Put this in Section 6 with an owner.

[Finding ID: practicality-1-11] Lines 102, 108-111, 133, 144, 191: Several deliverables that the build must produce are not listed in the scope or the estimate. These are the procedural reference card (line 102), the one-page observation checklist (lines 133 and 145), the manager role-play guide (line 132), five prospect lines with tone notes (line 190), the deal-math one-pager, and the part-task drill items. Each needs authoring, SME review, and accessibility checks. Recommendation: Add an inventory of all deliverables, with an estimate for each, to the Section 10 estimate. Include the reference card, checklist, role-play guide, and drill items.

### 🟢 Nits

[Finding ID: practicality-1-12] Line 155: The Module 5 retake rule reshuffles answer order. The spec does not confirm that Rise 360 can randomize answer order on retake, and it does not say how SCORM reports retake scores (first attempt, best attempt, or last attempt). Recommendation: Confirm the Rise randomization setting and the SCORM reporting rule with the LMS owner. Write both into Section 9.

[Finding ID: practicality-1-13] Lines 93, 226: Spaced follow-up and a retrieval schedule are named as relevant to the one-session decay risk, but they are not designed or prioritized (line 226). The spec should record whether this is in scope for release 1. Recommendation: Mark spaced follow-up as release 2 (or as out of scope) in Section 11 or 12, so the build does not absorb it by default.

## Summary

The design as written cannot go to build. Its content (differentiators, scripts, and deal-math figures) is not yet in hand, and the sign-off dates and manager capacity that the terminal objective depends on are not committed. The build-hour estimate excludes the work the spec itself lists as necessary, and the branching and Module 4-5 seat time are not sized to the content. Resolving the three Blockers, and re-scoping the branch count and seat time, would make the spec buildable within a three-week window.
