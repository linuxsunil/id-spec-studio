---
name: id-review
description: >-
  Run the four Goldfish reviewers on a course design spec in parallel.
  Produces four review reports and a consolidated findings report.
  You resolve findings and approve the final spec.
---

# ID Review

Run four specialized Goldfish reviewers against a course design spec simultaneously.

Each reviewer reads the document cold — no prior conversation context — giving you adversarial feedback from four distinct lenses.

---

## Execution Constraints (CRITICAL)

1. **Artifact-First**: All reports written to files. Never dump reports into chat.
2. **Parallel Review**: Spawn all four Goldfish simultaneously, not sequentially.
3. **Critique First**: Findings lead with what is broken.
4. **No Glazing**: Do not soften findings.
5. **You Resolve**: After review, the author (you) classifies each finding as CONTEST or ACCEPT and decides the fix.
6. **Max 2 Review Rounds**: If open Blockers remain after round 2, document them as accepted risk and proceed.

---

## Inputs

- **TargetFile**: Path to the course design spec (e.g., `docs/designs/<course-name>.md`)
- **GoldfishContext** (optional): Additional files to give reviewers as background (source materials, brief, stakeholder notes)

---

## Step 1: Intake

Verify `TargetFile` is provided and exists. If not, ask for the path.

Ask: "Any additional context files for reviewers? (e.g., the original brief, stakeholder notes) Or proceed with the spec alone?"

---

## Step 2: Select Review Mode

Ask:

> "Select review mode:
> 1. Interactive — check in after each reviewer's report
> 2. Consolidated — run all four, deliver one combined report"

---

## Step 3: Run the Four Goldfish in Parallel

Spawn four subagents simultaneously, each with fresh context. Pass the spec content and GoldfishContext to each.

**Reviewer 1 — Alignment Reviewer**
- Persona file: `agents/alignment-reviewer.md`
- Rubric: Standards 1, 2, 5 from `resources/id-review-standard.md`
- Output: `alignment_review_report.md`
- Prompt: "Read your persona at `agents/alignment-reviewer.md`. Then audit `[TargetFile]` against Standards 1, 2, and 5 in `resources/id-review-standard.md`. Context files: [GoldfishContext]. Write findings to `alignment_review_report.md`."

**Reviewer 2 — Learner Reviewer**
- Persona file: `agents/learner-reviewer.md`
- Rubric: Standards 3, 7 from `resources/id-review-standard.md`
- Output: `learner_review_report.md`
- Prompt: "Read your persona at `agents/learner-reviewer.md`. Then audit `[TargetFile]` against Standards 3 and 7 in `resources/id-review-standard.md`. Context files: [GoldfishContext]. Write findings to `learner_review_report.md`."

**Reviewer 3 — Practicality Reviewer**
- Persona file: `agents/practicality-reviewer.md`
- Rubric: Standard 8 from `resources/id-review-standard.md`
- Output: `practicality_review_report.md`
- Prompt: "Read your persona at `agents/practicality-reviewer.md`. Then audit `[TargetFile]` against Standard 8 in `resources/id-review-standard.md`. Context files: [GoldfishContext]. Write findings to `practicality_review_report.md`."

**Reviewer 4 — Theory Reviewer**
- Persona file: `agents/theory-reviewer.md`
- Rubric: Standard 4 from `resources/id-review-standard.md`, `resources/theory-pool.md`
- Output: `theory_review_report.md`
- Prompt: "Read your persona at `agents/theory-reviewer.md`. Then audit `[TargetFile]` against Standard 4 in `resources/id-review-standard.md` and against `resources/theory-pool.md`. Context files: [GoldfishContext]. Write findings to `theory_review_report.md`."

---

## Step 4: Consolidate Findings

After all four reports are written:

1. Read all four reports
2. Deduplicate overlapping findings (same issue raised by multiple reviewers → merge into one finding, credit all reviewers)
3. Assign stable IDs: `<reviewer>-1-<n>`
4. Sort by severity: 🔴 Blockers first, then 🟡 Major, then 🟢 Nits

Write `consolidated_review_report.md`:

```markdown
# Consolidated Review Report

**Spec reviewed:** [filename]
**Date:** [date]
**Reviewers:** Alignment, Learner, Practicality, Theory

## 🔴 Blockers

| ID | Reviewer | Section | Finding | Recommendation |
|---|---|---|---|---|

## 🟡 Major

| ID | Reviewer | Section | Finding | Recommendation |
|---|---|---|---|---|

## 🟢 Nits

| ID | Reviewer | Section | Finding | Recommendation |
|---|---|---|---|---|

## Traceability

| Finding ID | Source Report | Status |
|---|---|---|
```

Notify: "Review complete. `consolidated_review_report.md` written to [path]. [N] blockers, [N] major, [N] nits."

---

## Step 5: Resolution

For each Blocker and Major finding, ask the author:

> "Finding [ID]: [one-line summary]. CONTEST (explain why this finding is wrong) or ACCEPT (I will fix)?"

For contested findings: record the contest rationale. Do not re-open.
For accepted findings: apply the fix to `TargetFile` using file editing tools.

After fixes: re-read `TargetFile` and run a second review pass (Steps 3–4) if any Blockers were accepted.

---

## Step 6: Final Approval Gate

When no open Blockers remain (or remaining Blockers are documented as accepted risk):

Update spec header: `**Status:** Approved`

Ask:
> "Review complete. [N] findings resolved. Spec status set to Approved. Ready to hand to build pipeline."

---

## Convergence Rules

- **Clean round**: No open Blockers or Majors after fixes
- **Cap**: 2 review rounds maximum
- After cap: document remaining open findings as accepted risk in Section 10 of the spec. Set status to Approved with known risks.
