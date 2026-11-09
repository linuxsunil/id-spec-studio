# Theory Review Report

**Reviewer:** Theory Reviewer
**Document reviewed:** docs/designs/pricing-objection-handling.md (v0.1, Draft)
**Rubric:** resources/id-review-standard.md, Standard 4; cross-checked against resources/theory-pool.md
**Context files:** None (spec alone)
**Date:** 2026-11-09

## Theory Selection Assessment

| Theory | Selected/Rejected | Justified? | Applied in Design? |
|--------|------------------|------------|-------------------|
| 4C/ID (Four-Component ID) | Selected (primary, advanced) | Yes (Sec 4, lines 60-61) | Yes: whole-task exchange (M5), supportive info (M1), procedural info (reference card), part-task drills (Sec 5, line 113) |
| Worked Example Effect | Selected (supporting) | Yes (lines 68-69) | Yes: worked, partly completed, independent fading per objection (lines 108-111) |
| Self-Efficacy Theory | Selected (supporting) | Yes (lines 75-76) | Yes: escalating objections across modules; feedback names strengths before gaps (lines 78-79, 115) |
| Transfer-Appropriate Processing | Rejected (line 84-85) | Yes | N/A. Diagnosis respected via live role-play and observed calls (Sec 6) |
| Social Learning Theory | Rejected (line 87-88) | Partly. Rejection reason is sound, but the text then says the role-play "uses this theory" | Conflict: rejected theory is named as the basis of a blended design element (line 88, Sec 6 line 132) |
| Desirable Difficulties (timer) | Rejected (line 90-91) | Yes | N/A. Timer excluded; no timer appears in the design |
| Retrieval Practice Effect | "Considered but not selected" (line 93) | Weak. Not selected as primary, with no supporting rationale | Yes, despite not being selected: matching items with "retrieval practice" as rationale (Sec 5, line 103; Sec 4, line 93 "quiz blocks will use retrieval-style items") |
| Spacing Effect | "Considered but not selected" (line 93) | Deferred to Sec 12 | No. Spaced follow-up is undesigned (line 226) |
| Goal-Based Scenarios | "Considered but not selected" (line 93) | Deferred to Sec 12 | Partly. Branching scenarios are the core practice format (Sec 5, line 104) |
| Cognitive Load Theory (Sweller) | Not evaluated, not selected, not rejected | No | Load is managed implicitly (chunking, fading, reference card) but never named, analyzed, or checked against timing |
| ARCS (Keller) | Applied in Sec 8; not in the Theory Consideration Report | Partly | Yes: attention (line 163), relevance (line 164), confidence (line 165), satisfaction (line 166) |
| Merrill's First Principles | Applied in part; not in the report | No | Demonstration and application present. Activation absent (see theory-1-5). Integration present (M5, role-play) |
| Gagné's Events of Instruction | Applied in part; not in the report | No | Attention, present stimulus, guidance, performance, feedback, and assessment present. State objective, recall prior, and retention are missing or undesigned |
| Clark's Evidence-Based Principles | Applied | Yes (worked examples, practice, feedback) | Yes (Sec 5, lines 104-115) |

**Report presence:** The Theory Consideration Report exists (Sec 4, line 52). No Blocker is raised for a missing report.
**Rejection count:** Three theories are explicitly rejected with reasons, and three more are set aside. The minimum of two rejections is met.
**Advanced theory:** 4C/ID is present. Met.

## Overlooked Theories Worth Considering

1. **Cognitive Load Theory (Sweller).** Pool use case: "complex content; novice learners." The spec's learners are experienced sellers but novices at this skill, and the skill has three parts across five objections. Design decision it would improve: the Module 4 structure (three hard objections in 8 minutes, lines 126 and 223). CLT would set an explicit intrinsic-load limit per module and justify splitting or extending it.
2. **Spaced Retrieval (Ebbinghaus).** Pool use case: "long-term retention programs." Design decision it would improve: the undesigned post-course follow-up (line 226). It would give the retention event a concrete form, such as a short spaced recall set after the course, and would replace the open question with a decision.
3. **Expectancy-Value Theory.** Pool use case: "learner buy-in; relevance framing." Design decision it would improve: the Module 1 deal-math comparison (line 123), which is the design answer to the named commission-based resistance (line 168). The theory explains why the deal math must show expected payoff, not only value.

## Findings

### 🔴 Blockers
None. The Theory Consideration Report is present, rejections are documented, and the primary theory is applied. The Major findings below should be resolved before build, but none stops the spec from proceeding.

### 🟡 Major
[Finding ID: theory-1-1] Line 93 (Sec 4) and line 103 (Sec 5): Retrieval Practice Effect is listed as "considered but not selected," but Sec 5 uses it as the stated rationale for the matching items, and Sec 4 line 93 says "quiz blocks will use retrieval-style items." Theory-pool Step 4 says rejected theories must never appear in design decisions. A theory that is used but not selected is either a missing selection or an unexplained use. This matters because the spec's retention case depends on it. Recommendation: move Retrieval Practice Effect into the selected list as supporting, with its own "why selected" and application lines (matching items, Module 2 recall, Module 5 retrieval), or remove it from the Sec 5 rationale.

[Finding ID: theory-1-2] Lines 87-88 (Sec 4) and line 132 (Sec 6): Social Learning Theory is rejected ("not a course element"), but line 88 states that the manager role-play "uses this theory," and Sec 6 makes the role-play a required blended element. The spec both rejects the theory and applies it, which the pool rules prohibit. Recommendation: either reselect Social Learning Theory as a supporting theory for the blended element, with a stated application (for example, the manager models one exchange before the rep practices), or rewrite line 88 so the role-play is justified under 4C/ID (whole-task practice and feedback) and not under Social Learning Theory.

[Finding ID: theory-1-3] Sec 4 (Theory Consideration Report, lines 56-93) and Sec 6 (lines 121-127): Cognitive Load Theory is not evaluated, selected, or rejected, even though the learners are novices in a three-part, five-objection skill. Standard 4 requires intrinsic load to be matched to the audience and extraneous load minimized, and the persona requires explicit load management. The spec manages load implicitly (module chunking, fading, reference card) but cannot show it. Recommendation: add Cognitive Load Theory to the report. Name the intrinsic load per module (objections per module), the extraneous-load controls (one differentiator per screen, no split attention between the prospect line and the reference card, the fading sequence), and the germane-load goal. Reject or select it with reasons.

[Finding ID: theory-1-4] Line 126 (Module 4, 8 min, three hard objections), line 125 (Module 3, 6 min, two mild objections), Sec 5 lines 108-113, and Sec 12 line 223: Each objection in Modules 3 and 4 requires a worked example, a partly completed example, an independent branch with feedback, and a part-task drill (lines 66 and 113). Module 4 contains three objections, each with the full sequence, in 8 minutes. That is roughly 2.5 minutes per objection for four steps, including reading the feedback. This is the highest intrinsic-load point in the course, and the spec defers it to a pilot. The fading sequence is therefore not supported by the stated timing. Recommendation: rebalance the modules (for example, two objections in Module 4 and one in Module 3, or extend Module 4 and shorten Module 1), or reduce the third objection in Module 4 to worked plus independent. Update the duration table to match the practice design.

[Finding ID: theory-1-5] Sec 2 line 24 and Sec 6 (lines 121-127): Section 2 states that some reps have a discount habit and their own pitch, and that "the course must address rather than ignore" it. No module asks learners to surface their current response, compare it with the three-part structure, or recall their own discount reflex. Merrill's activation principle (activate prior knowledge) and Gagné's "recall prior" event are therefore absent, and the audience constraint is not carried into the design. Recommendation: add an activation step at the start of Module 1 or Module 2 in which the learner writes or selects their usual response to "Your price is 40% higher," then compares it with the value-first response. Name the theory (Merrill activation, Gagné recall prior) and the design decision it drives.

[Finding ID: theory-1-6] Sec 6 (lines 121-127) and Sec 8 line 163: The learner-facing statement of objectives is not designed. Section 3 defines objectives for the design team, and Sec 6 lists "Objectives Covered" per module, but no module opens by telling learners what they will be able to do. Gagné's "state objective" event is therefore not addressed, and Standard 4 requires it. Recommendation: add a one-line learner-facing objective statement at the top of each module, drawn from Section 3 objectives, and record it as a Gagné event in Sec 5 or Sec 6.

[Finding ID: theory-1-7] Sec 4 line 93, Sec 10 (lines 185-194), and Sec 12 line 226: Gagné's "enhance retention and transfer" is partly addressed. Transfer is handled by the live role-play and observed calls, which is sound. Retention depends on one matching item in Module 2 and a spaced follow-up that is marked as an open question. Section 10 names no decay risk, yet Sec 4 line 93 refers to "the one-session decay risk." The retention event is therefore not designed. Recommendation: decide now whether a spaced follow-up exists (Spaced Retrieval is the pool candidate), state its schedule and owner, and add the decay risk to Section 10 with its mitigation.

### 🟢 Nits
[Finding ID: theory-1-8] Line 125 (Module 3 covers objectives 3 and 4) and line 144 (objective 4 assessed only as a summative item in Module 5): Section 6 says Module 3 covers objective 4, but Section 7 assesses objective 4 only in Module 5, and the formative checkpoints list (lines 149-153) does not include Module 3 for objective 4. Recommendation: either add a Module 3 formative item for objective 4 or change Module 3's objective coverage to 3 only.

[Finding ID: theory-1-9] Lines 93 and 215: "Considered but not selected" entries give no rejection reason beyond "not selected as primary." The pool requires a reason for each rejection. Recommendation: for Spacing Effect and Goal-Based Scenarios, add one line each stating why they are excluded or deferred, so the record shows a decision rather than an omission.

## Summary
The design is grounded in a deliberate primary theory (4C/ID) with worked examples, Clark's practice and feedback principles, ARCS, and a documented rejection of three theories, so the Theory Consideration Report requirement is met. The weaknesses are in how the theory is applied: Cognitive Load Theory is never evaluated despite a novice learner and a heavy Module 4, Retrieval Practice and Social Learning are used after being rejected or set aside, and activation, objective statement, and retention events are missing or undesigned. These should be fixed before build, and the Module 4 timing needs the pilot test the spec already proposes.
