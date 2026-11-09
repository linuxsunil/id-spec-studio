# Learner Review Report

**Reviewer:** Learner Reviewer
**Document reviewed:** docs/designs/pricing-objection-handling.md (v0.1, Draft)
**Standards applied:** Standard 3 (Audience Specification), Standard 7 (Motivation Design, ARCS); Andragogy and Cognitive Load Theory from theory-pool.md
**Date:** 2026-11-09

## Audience Specification Assessment

The spec names the learner clearly: new B2B SaaS sales reps, about 50 in the first cohort, with 2–3 years of selling experience, no objection-handling training, and a stated discount habit (lines 22–24). Context of use is partly stated: live calls, under time pressure, when a price objection comes up (line 25). Motivation is acknowledged, including the risk that reps paid on closed deals will read a value-first rule as a cost (lines 26, 168). Specific gaps: the label "new" conflicts with the stated experience level; device and timing of the course are unset; the cost data that Module 1 depends on is not quantified; and the success criteria for the live element do not match the terminal objective. The strongest parts are the prerequisite statement, the named resistance, and the explicit limit of what the course can assess (line 157).

## Findings

### Blockers

**learner-1-1** | Section 6 (Module 1), Section 3 (Objective 2), Section 8 (Relevance) | Lines 123, 36, 164, 16, 217
Module 1 is the designed answer to the learner's main motivation problem: it shows "the deal math" and "what the discount costs them in their own numbers" (line 164). Objective 2 requires reps to cite "the cost of discounting in their own terms" (line 36). But the spec states that the cost of the gap is not quantified and that the discount-rate baseline by rep is not yet pulled (lines 16, 217). Module 1 cannot be written as specified, and the relevance design has no input data. Blocks build.
**Recommendation:** Before build, obtain the discount data from sales ops and specify its source, fields, and time window. If the data cannot be obtained in time, redesign Module 1 around a labelled illustrative deal with the numbers shown, and remove the claim that reps see their own numbers.

### Major

**learner-1-2** | Section 2 (Audience) | Lines 22–23, 54
The audience is labelled "New B2B SaaS sales reps" (line 22) but the experience level is "Intermediate in selling (2–3 years)" (line 23). Section 4 calls them "experienced sellers" (line 54). A reader cannot tell whether this is a new-hire cohort or an experienced cohort, and that changes the strategy (worked examples and novice framing in Sections 4–5).
**Recommendation:** Pick one definition. State the screening criterion (for example, hired within a stated window, or a minimum years of selling), and say whether reps who already handle price objections are in scope.

**learner-1-3** | Section 5 (Practice design), Section 4 (Worked Example Effect) | Lines 69–73, 111, 24
Every objective gets a worked example, then a partly completed example, then an independent branch. Line 24 says some reps already have a discount habit and their own pitch. Line 69 frames all learners as novices at objections. The spec has no diagnostic and no route for a rep who already handles an objection well to skip the worked steps. This runs against the Andragogy principle in the persona brief (experienced adults should not be treated as novices) and invites an expertise-reversal problem.
**Recommendation:** Add a diagnostic: one unworked branch per objection, or a short pre-check. Reps who pass the diagnostic can skip the worked and partly completed steps for that objection. Also state how the existing discount habit is addressed in the course, since line 24 names it as a thing the course "must address," but no module does so explicitly.

**learner-1-4** | Section 2 (Context of use), Section 9 (Delivery), Section 12 | Lines 25, 27, 218–219, 226
Standard 3 asks for delivery context (device, location, time). The spec gives time pressure for live calls but not the device the course is taken on, the location, or when it is taken relative to the first live call (line 25: "not yet set"). Quota-heavy weeks are an open question (line 219). Device affects Rise 360 layout, scenario readability, and the seat-time estimate.
**Recommendation:** State the supported devices (desktop only, or desktop and mobile), the completion window before first live call (for example, within 5 working days), and whether 30 minutes is a single sitting or can be split.

**learner-1-5** | Section 8 (Attention), Section 6 (Course Structure) | Lines 163, 123
Section 8 says the course opens with a real prospect line, "Your price is too high," in a short scenario, and that learners are "in the middle of the problem within the first 30 seconds." The Module 1 row in Section 6 lists only a "Deal-math comparison" as the key activity, with no scenario. As written, the first module starts with explanation, and the stated attention hook does not appear in the module structure.
**Recommendation:** Either add the opening scenario to the Module 1 key activity in Section 6, or move the hook to a stated pre-Module 1 screen. Make Sections 6 and 8 agree.

**learner-1-6** | Section 6 (Module 4), Section 5 (Sequence logic) | Lines 126, 113, 223
Module 4 covers three hard objections ("Competitor X is cheaper," "What do we get that justifies the premium?," "Can you match their price?") in 8 minutes. Each objection runs worked, partly completed, and independent steps, with drills before each independent branch (line 113). That is roughly 2.5 minutes per objection for a full fading sequence. The spec flags this as an open question (line 223), but Section 6 still presents the 8-minute timing as settled. The hardest objections sit in the module with the least time per objection, which weakens the confidence sequence in Section 8.
**Recommendation:** Budget minutes per objection, and recheck the total. Move one objection to Module 3, or lengthen Module 4. Decide before build, not at pilot.

**learner-1-7** | Section 6 (Module 2), Section 3 (Objective 1) | Lines 124, 35, 65
Module 2 asks learners to recall five differentiators (objective 1, line 35), learn the three-part structure, learn the 30-second rule (line 65), and use a reference card, all in 5 minutes, before any practice. That is high intrinsic load for a novice set of items, and the spec does not show how the load is spread. Cognitive Load Theory (persona brief) predicts that recall of five unrelated items plus a procedure in one short module will overload working memory.
**Recommendation:** Split differentiator recall from structure learning, or move the matching item (objective 1) to after the first objection in Module 3, when the differentiators are used in context.

**learner-1-8** | Section 7 (Terminal behavior), Section 6 (Blended element), Section 3 (Terminal Objective) | Lines 46, 133, 145
The terminal objective requires a three-part response (acknowledge, pivot, qualify) within 30 seconds, before any mention of price. The pass rule for the observed live calls is only "the rep attempts the three-part response before any discount" (line 133). A rep who makes one attempt in the right order passes, whatever the content and timing. Standard 7 asks for clear success criteria, and the learner has none that match the terminal objective.
**Recommendation:** Align the pass rule with the terminal objective: all three parts, in order, before any price or discount mention, and within the observed time limit. State the checklist criteria in the course so the learner sees the bar before the live call.

**learner-1-9** | Section 6 (Blended), Section 12 | Lines 25, 157, 226
The course is one session, and the live calls come after it with no set window (line 25). The spec names knowledge decay as a risk (line 93) but has no follow-up design (line 226: "not designed"). A rep may complete Module 5 and then face the first objection weeks later with nothing in place to hold the skill. Standard 7 asks that the course end with a sense of application, and this one does not reach it past the end of the course.
**Recommendation:** Decide the follow-up before build: for example, one short retrieval item sent at day 7, or a pre-call job aid the rep can open on the day of the call. Set the window between completion and the first observed call.

**learner-1-10** | Section 8 (Relevance and Resistance), Section 2 (Motivation), Section 10 | Lines 164, 168, 16
Line 164 says reps "see their own discount habit," which needs individual rep data. Line 168 says the discount-rate measure "is not used to judge individual reps in the course." The spec does not say which individual data is shown to each rep, who sees it, or how it is kept separate from manager judgment. For a commission-paid cohort, this is the point where resistance is most likely to turn into disengagement (line 26).
**Recommendation:** State exactly what individual data appears in the course, who can see it, and how it is protected. Reconcile line 164 with line 168, and decide whether the Module 1 comparison uses individual or cohort-level numbers.

**learner-1-11** | Section 2 (Prerequisites), Section 3 (Objective 1), Section 10 | Lines 24, 35, 188
Prerequisites are stated well ("Product training is complete," line 24). But Module 2 and objective 1 depend on approved differentiators, and line 188 says the sales director owns them and scripts can change after build. Learners would be asked to recall content that has not been approved and may change. The prerequisite statement does not cover this dependency.
**Recommendation:** Confirm the differentiators and scripts before Module 2 is built, and list which differentiators are prerequisite knowledge and which are taught in the course.

### Nits

**learner-1-12** | Section 2 (Constraints), Section 9 | Lines 27, 178
The audience spec does not mention learners with accessibility needs, and the accessibility target is still "proposed" (line 178). A text-and-click course with no audio is a reasonable start, but the audience description should record the target so the design decisions (contrast, keyboard use of scenario blocks, screen reader text for branching) can be checked against it.
**Recommendation:** Confirm WCAG 2.1 AA as the target in the audience section and note the accessibility requirements for the scenario blocks.

**learner-1-13** | Section 5 (Strategy), Section 6 (Course Structure) | Lines 120–127
The course is linear. Learners cannot choose which objection to start with, even though reps sell into different objections in different deals. Andragogy favours self-direction, and the spec does not use it.
**Recommendation:** Let learners choose the order of objections in Modules 3 and 4, or let them jump to the objection that matches their most recent lost deal.

**learner-1-14** | Section 8 (Satisfaction), Section 6 (Module 5) | Lines 127, 166
Module 5 ends with a summary (line 127), and the sense of accomplishment is placed in the manager role-play outside the course (line 166). Inside the course, the learner does not state a plan for their next real call. Standard 7 notes that a course should end with a sense of application.
**Recommendation:** Add a short "my next call" commitment in Module 5, which the learner writes in their own words and can carry into the role-play.

## Summary

This design serves its described learner in intent. The audience is named, the prerequisites are stated, and the resistance is acknowledged. It does not yet serve them in practice. Module 1 cannot be built without cost data the spec says it does not have, the audience label and experience level conflict, and Module 4 is timed for a fading sequence the spec itself questions. Resolve the blocker and the Major findings on audience, timing, and the pass rule before build.
