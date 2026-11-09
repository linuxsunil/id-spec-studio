# Consolidated Review Report

**Spec reviewed:** docs/designs/pricing-objection-handling.md (v0.1, Draft)
**Date:** 2026-11-09
**Reviewers:** Alignment, Learner, Practicality, Theory
**Context files:** None (spec alone)
**Source reports:** alignment_review_report.md, learner_review_report.md, practicality_review_report.md, theory_review_report.md

**Totals:** 4 Blockers, 22 Majors, 6 Nits (32 findings). Raw reviewer findings: 44 (Alignment 8, Learner 14, Practicality 13, Theory 9). Overlaps merged: 12. Merged findings take the highest severity raised and credit every reviewer.

## 🔴 Blockers

| ID | Reviewer | Section | Finding | Recommendation |
|---|---|---|---|---|
| B-1 | Alignment (alignment-1-1), Learner (learner-1-8) | 3, 6, 7 | The terminal objective has three measurable criteria: 30 seconds, value before price, three-part structure. The pass rule checks only order ("attempts the three-part response before any discount"). The checklist is not specified, and the 30-second limit has no timing method. | Specify the checklist criteria in the spec (one line each, including how time is measured). Set the pass rule to cover every terminal criterion, or narrow the terminal objective. Record the decision in Sections 3 and 7. |
| B-2 | Practicality (practicality-1-1), Alignment (alignment-1-2), Learner (learner-1-11) | 5, 6, 10, 13 | The content the build depends on does not exist: the five differentiators, five scripts, and five prospect lines. The sales director has no review window or sign-off date. Modules 2–5 carry about 25 of 30 minutes and every formative and summative item. | Add an approved content inventory as an appendix. Set a dated SME sign-off gate before build. Name a backup reviewer. Re-anchor the three-week schedule to that gate. |
| B-3 | Learner (learner-1-1), Practicality (practicality-1-2) | 1, 6, 8 | Module 1 depends on deal-math figures (average deal size, discount depth, win-rate delta) that the spec says are not quantified. Objective 2 and the Module 1 item also depend on them. The spec still claims reps see "their own numbers." | Get the sales ops figures and set a delivery date. If unavailable, use a labelled illustrative example the SME approves, and remove the "own numbers" claim. |
| B-4 | Practicality (practicality-1-3) | 6, 7, 10 | Terminal behavior is assessed only by about 100 observed live calls and 50 role-plays. Manager time is "not yet committed," and observation length is not estimated. No fallback exists if capacity is short. | Confirm in writing how many managers observe, how many calls each covers, and the minutes per call. Set the launch date after confirmation. If capacity is short, name the exempt cohorts or narrow the terminal objective. |

## 🟡 Major

| ID | Reviewer | Section | Finding | Recommendation |
|---|---|---|---|---|
| M-1 | Alignment (alignment-1-3) | 3, 5, 7, 8 | Objective 2 requires citing the cost of discounting "in their own terms." The assessment only recognizes an explanation. Section 8 claims reps see their own numbers. | Reword objective 2 to match the design, or add a learner-input calculation item. Remove the "own numbers" claim unless the design provides the data. |
| M-2 | Alignment (alignment-1-4), Theory (theory-1-8) | 6, 7 | Module 3 lists objective 4 as covered, but its activity has no error-spotting task. The only objective 4 assessment is in Module 5. | Add a formative error-spotting item in Module 3 or 4, or correct the Module 3 coverage entry. |
| M-3 | Alignment (alignment-1-5) | 6, 7 | The summative set (Module 5 items) covers objectives 3 and 4 only. Section 7 lists objective 1 as summative, and objective 2 has no summative item. The 80% threshold cannot be verified against objectives. | Add an objective-to-summative-item map. Fix the objective 1 label and state whether objective 2 is formative only. |
| M-4 | Alignment (alignment-1-6) | 3, 5, 6, 7 | Objective 1 says "without notes," but the reference card stays on screen. The matching item's condition is not stated. | State whether the matching item is closed-book. If it is open-book, remove "without notes." |
| M-5 | Learner (learner-1-2) | 2, 4 | The audience is labelled "New" but described as "Intermediate (2–3 years)" and "experienced sellers." The strategy depends on which one is true. | Pick one definition. State the screening criterion and whether reps who already handle objections are in scope. |
| M-6 | Learner (learner-1-3), Theory (theory-1-5) | 2, 4, 5, 6 | Every objective gets the full worked-example sequence. There is no diagnostic or activation step for reps with an existing discount habit, which Section 2 says the course must address. | Add a diagnostic or activation step (learner writes their usual response to "Your price is 40% higher," then compares it with the value-first response). Let reps who pass skip worked steps for that objection. Name the theory and the design decision it drives. |
| M-7 | Learner (learner-1-4) | 2, 9, 12 | Delivery context is missing: supported devices, completion window before the first live call, and single sitting or split. | State supported devices, a completion window, and whether 30 minutes can be split. |
| M-8 | Learner (learner-1-5) | 6, 8 | Section 8 says the course opens with a real prospect line in a short scenario. The Module 1 row lists only a deal-math comparison. | Add the opening scenario to the Module 1 activity, or add a pre-Module 1 screen. Make Sections 6 and 8 agree. |
| M-9 | Learner (learner-1-6), Theory (theory-1-4), Practicality (practicality-1-6) | 5, 6, 12 | Module 4 covers three hard objections, each with four steps and drills, in 8 minutes. Module 5 covers a full exchange, error spotting, a summary, and summative items in 7 minutes. Retake time is not counted. The spec flags this as open but presents the timing as settled. | Budget minutes per objection and recheck the total. Move one objection to Module 3, or lengthen Module 4 and Module 5 and restate seat time (35–40 min). Run a timed pilot before build. State retake time separately. |
| M-10 | Learner (learner-1-7), Theory (theory-1-3) | 4, 5, 6 | Cognitive load is not evaluated. Module 2 asks for five differentiator recalls, the three-part structure, the 30-second rule, and a reference card in 5 minutes, before any practice. Cognitive Load Theory is not in the Theory Consideration Report. | Add Cognitive Load Theory to Section 4 with a selection or rejection reason. Name intrinsic load per module, extraneous-load controls, and germane-load goals. Split Module 2 or move the recall item to Module 3. |
| M-11 | Learner (learner-1-9), Theory (theory-1-7) | 4, 6, 10, 12 | No follow-up design exists after the course. Live calls may come weeks later, and knowledge decay is named as a risk but not addressed. Retention is an undesigned Gagné event. | Decide the follow-up: a spaced retrieval item at day 7, or a pre-call job aid. Set the window between completion and the first observed call. Add the decay risk to Section 10. |
| M-12 | Learner (learner-1-10) | 2, 8, 10 | The spec does not say which individual rep data appears in the course, who sees it, or how it is kept from manager judgment. Section 8 says reps see their own discount habit, while Section 10 says discount rate is not used to judge individuals. | State the individual data shown, who sees it, and how it is protected. Reconcile Sections 8 and 10. |
| M-13 | Practicality (practicality-1-4) | 10 | The 20–25 build-hour estimate excludes SME review, accessibility, SCORM and LMS testing, and the pilot. No per-module breakdown supports it. | Produce a per-module hour breakdown covering all tasks. Compare it with the three-week calendar. State the estimate as a range. |
| M-14 | Practicality (practicality-1-5) | 5, 6 | Branching size is unbounded. About 45 or more choice points with feedback, plus worked and partly completed versions, drills, and the Module 5 exchange. The branch cap is open. | Set a branch cap in Section 5 (for example, three options per step, one feedback screen per wrong choice). Count authored screens per module and add them to the estimate. |
| M-15 | Practicality (practicality-1-7) | 7 | Objective 4 needs line-level selection in a transcript. The spec does not show that Rise 360's quiz blocks support it. | Verify the block in Rise 360. If unsupported, define a fallback and state its Bloom's-level effect. |
| M-16 | Practicality (practicality-1-8) | 10, 3 | The cut line removes one Module 4 objection if the SME slips. The terminal objective still requires all five objections, and the observed-call checklist counts all five. | Define a release-1 terminal objective for the four shipping objections, and state how the fifth is handled in the checklist. Or move the cut to Module 5 scope and name the affected summative items. |
| M-17 | Practicality (practicality-1-9) | 9, 12 | The LMS, SCORM version, and accessibility standard are not confirmed. SCORM upload and LMS testing cannot be scheduled without them. | Name the LMS, SCORM version, and test environment. Confirm WCAG 2.1 AA with the LMS owner. Add LMS and accessibility tasks to the schedule with durations. |
| M-18 | Practicality (practicality-1-10) | 6, 7 | The observation method is unnamed (live listening, recording, or coaching tool). Consent, rep access, and score storage are not addressed. | Name the observation method and score storage tool. Confirm the call-recording policy and consent process. Assign an owner in Section 6. |
| M-19 | Practicality (practicality-1-11) | 5, 6, 10 | Deliverables are not inventoried: reference card, one-page observation checklist, manager role-play guide, five prospect lines with tone notes, deal-math one-pager, and drill items. | Add a deliverables inventory with an estimate for each to the Section 10 estimate. |
| M-20 | Theory (theory-1-1) | 4, 5 | Retrieval Practice Effect is "considered but not selected," yet Section 5 uses it as the rationale for matching items. The pool forbids using rejected theories in design. | Move Retrieval Practice Effect into the selected list with its own rationale and application, or remove it from the Section 5 rationale. |
| M-21 | Theory (theory-1-2) | 4, 6 | Social Learning Theory is rejected, but the manager role-play is said to use it, and the role-play is a required blended element. | Reselect Social Learning Theory as supporting with a stated application (for example, the manager models one exchange). Or justify the role-play under 4C/ID only. |
| M-22 | Theory (theory-1-6) | 6 | No module states its learning objective to learners. Gagné's "state objective" event is missing. | Add a one-line learner-facing objective at the top of each module, and record it as a Gagné event. |

## 🟢 Nits

| ID | Reviewer | Section | Finding | Recommendation |
|---|---|---|---|---|
| N-1 | Alignment (alignment-1-7) | 3 | The terminal objective has no stated Bloom's level. | Add "Bloom's level: Apply (performance)." |
| N-2 | Alignment (alignment-1-8) | 3 | The Bloom's note says objective 3 "is the terminal behavior," but the terminal objective adds the 30-second and value-first conditions. | Describe objective 3 as the course-level component. List the terminal criteria it does not cover. |
| N-3 | Learner (learner-1-12) | 2, 9 | The audience section does not record the accessibility target or needs. | Confirm WCAG 2.1 AA in the audience section, and note the scenario-block requirements. |
| N-4 | Learner (learner-1-13) | 5, 6 | The course is linear. Learners cannot choose which objection to start with. | Let learners choose the order of objections in Modules 3 and 4. |
| N-5 | Learner (learner-1-14) | 6, 8 | Module 5 has no learner commitment to apply the skill on a real call. | Add a short "my next call" written commitment to Module 5. |
| N-6 | Practicality (practicality-1-12), Theory (theory-1-9) | 5, 7, 9 | The retake rule's answer-order randomization and SCORM reporting rule are unconfirmed. "Considered but not selected" entries give no rejection reason. | Confirm Rise randomization and the SCORM retake rule. Add one-line rejection reasons for Spacing Effect and Goal-Based Scenarios. |

## Traceability

| Finding ID | Source Report | Status |
|---|---|---|
| B-1 | alignment-1-1; learner-1-8 | Accepted, fixed in spec v0.2 (pass rule narrowed to observable criteria; timing coached, not scored) |
| B-2 | practicality-1-1; alignment-1-2; learner-1-11 | Accepted, fixed in spec v0.2 (dated SME gate 2026-11-13 proposed; Appendix A inventory added) |
| B-3 | learner-1-1; practicality-1-2 | Accepted, fixed in spec v0.2 ("own numbers" replaced by labelled illustrative example pending SME approval) |
| B-4 | practicality-1-3 | Accepted, fixed in spec v0.2 (manager capacity confirmation added as launch dependency) |
| M-1 | alignment-1-3 | Open |
| M-2 | alignment-1-4; theory-1-8 | Open |
| M-3 | alignment-1-5 | Open |
| M-4 | alignment-1-6 | Open |
| M-5 | learner-1-2 | Open |
| M-6 | learner-1-3; theory-1-5 | Open |
| M-7 | learner-1-4 | Open |
| M-8 | learner-1-5 | Open |
| M-9 | learner-1-6; theory-1-4; practicality-1-6 | Open |
| M-10 | learner-1-7; theory-1-3 | Open |
| M-11 | learner-1-9; theory-1-7 | Open |
| M-12 | learner-1-10 | Open |
| M-13 | practicality-1-4 | Open |
| M-14 | practicality-1-5 | Open |
| M-15 | practicality-1-7 | Open |
| M-16 | practicality-1-8 | Open |
| M-17 | practicality-1-9 | Open |
| M-18 | practicality-1-10 | Open |
| M-19 | practicality-1-11 | Open |
| M-20 | theory-1-1 | Open |
| M-21 | theory-1-2 | Open |
| M-22 | theory-1-6 | Open |
| N-1 | alignment-1-7 | Open |
| N-2 | alignment-1-8 | Open |
| N-3 | learner-1-12 | Open |
| N-4 | learner-1-13 | Open |
| N-5 | learner-1-14 | Open |
| N-6 | practicality-1-12; theory-1-9 | Open |
