---
name: id-brainstorm
description: >-
  Turn a raw course brief or vague request into a structured instructional
  design concepts brief. Uses multi-turn clarification and parallel Goldfish
  review. Output: concepts_brief.md ready for id-draft.
---

# ID Brainstorm

Turn a raw brief — a paragraph, an email, a vague request — into a structured course design concepts brief via iterative clarification and Goldfish review.

This is the upstream step before `/id-draft`.

---

## Execution Constraints (CRITICAL)

1. **Artifact-First**: Write everything to `concepts_brief.md`. Never dump large content into chat.
2. **Multi-Turn Clarification**: Do NOT rush to spawn Goldfish. Ask one open-ended question per turn until the problem is clear.
3. **Parallel Goldfish**: When review is triggered, spawn all reviewers simultaneously.
4. **Critique First**: Lead with what is weak, missing, or risky before anything positive.
5. **No Glazing**: Do not call ideas "great," "brilliant," or "good." Compliments without substance are noise.
6. **Stress-Test by Default**: Find the weakest points before affirming anything.
7. **One Question Per Turn**: Never ask more than one question at a time.

---

## Step 1: Deep Clarification

Ask open-ended questions across multiple turns until these are clear:

- What specific performance gap or business problem does this course address?
- Who are the learners — role, experience level, what they already know?
- What should learners be able to DO after the course that they cannot do now?
- What are the hard constraints: duration, delivery tool, timeline, team?
- How will success be measured — on the job, not in the course?
- What is currently done to address this need, and why isn't it working?

Do NOT provide multiple-choice options during this phase. Ask open-ended questions in plain chat only.

---

## Step 2: Readiness Gate

Once the problem is clearly defined, write a 2–3 sentence working hypothesis summarizing:
- The performance gap
- The audience
- The proposed approach

Then ask in chat:

> "Working hypothesis: [your summary]. Ready to run Goldfish review, or do you want to refine further?"

Only proceed to Step 3 when the user confirms readiness.

---

## Step 3: Goldfish Review

Spawn two Goldfish reviewers in parallel (fresh subagent contexts):

**Reviewer 1 — Zoom Out:**
Prompt: "You are a fresh reviewer. Read the following course design brief and evaluate: (1) Does the stated problem justify a course? Could a job aid, checklist, or process change solve this instead? (2) Is the scope appropriate — not too broad, not too narrow? (3) What is the strongest counter-argument to this design approach? Brief: [paste concepts_brief.md content]"

**Reviewer 2 — Learner Advocate:**
Prompt: "You are a fresh reviewer representing the learners described in this brief. Read the following course design brief and evaluate: (1) Is the audience description specific enough to design for? (2) Are prerequisites stated and realistic? (3) Would the described learner care about this course? Brief: [paste concepts_brief.md content]"

Collect both reports. Deduplicate overlapping findings.

---

## Step 4: Write concepts_brief.md

Write the synthesized brief to `concepts_brief.md` using this structure:

```markdown
# [Course / Project Name]

- **Author:** [from git config or ask]
- **Date:** [YYYY-MM-DD]

## The Problem

[What performance gap or business need drives this course?
Specific, concrete. Not "employees need training on X."]

## Audience

[Role, experience level, prior knowledge, context of use, motivation factors]

## Terminal Objective

[The one measurable behavior learners will be able to perform after the course
that they cannot perform reliably now]

## Scope

- **In scope:** [What this course will address]
- **Out of scope:** [What this course will NOT address]
- **Estimated duration:** [X minutes]
- **Delivery tool:** [Rise 360 / Storyline / other]

## Constraints

[Timeline, team, resources, platform, accessibility requirements]

## Theory Candidates

[2–3 theories worth considering for this design, with one-line rationale each.
Reference resources/theory-pool.md]

## Goldfish Findings

### Zoom Out Review
[Key findings from Reviewer 1]

### Learner Advocate Review
[Key findings from Reviewer 2]

## Open Questions

- [ ] [Questions requiring SME or stakeholder input before drafting]

## Alternatives Weighed

[Design approaches considered and rejected during this brainstorm, with reason]

## Key Decisions for id-draft

[Decisions made here that id-draft should carry forward]
```

---

## Step 5: Notify and Iterate

Notify the user: "`concepts_brief.md` updated at [path]. Key findings from review: [highlight 2–3 issues]."

Ask: "How would you like to address these? Pivot approach, narrow scope, or proceed to `/id-draft`?"

Iterate until the brief has survived scrutiny and the user is satisfied.

---

## Step 6: Handoff

When approved, ask:

> "Brief finalized. Next step: run `/id-draft` to build the full course design spec from this brief."

Confirm `concepts_brief.md` is saved in the working directory.
