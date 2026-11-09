---
name: id-draft
description: >-
  Build a full course design spec section by section from concepts_brief.md
  or a raw brief. Uses the id-design-doc template and your theory pool.
  Output: course_design_spec.md approved section by section.
---

# ID Draft

Build a complete course design spec from `concepts_brief.md` (or a raw brief if no brainstorm was run).

This produces `design_draft.md` section by section, with your approval at each gate, then saves the final spec to `docs/designs/`.

---

## Execution Constraints (CRITICAL)

1. **Artifact-First**: Write everything to `design_draft.md`. Never dump the draft into chat.
2. **Section-by-Section with Gates**: Draft one section, notify the user, get approval before the next.
3. **Author Decides Architecture**: When a design decision has more than one defensible answer, present up to 3 options with trade-offs. Do not rank or recommend. Ask the author to choose.
4. **Theory Consideration Report is Mandatory**: Section 4 must include a full Theory Consideration Report — selected theories with justification, rejected theories with reason, at least 2 rejections, at least 1 advanced theory.
5. **Critique First**: When reviewing a section before writing the next, lead with weaknesses.
6. **No Glazing**: Do not validate choices reflexively.
7. **One Question Per Gate**: Each approval gate asks one question only.

---

## Step 1: Ingest Context

Check for `concepts_brief.md` in the working directory. If found, read and confirm with the user: "Found `concepts_brief.md`. Starting draft from this brief — confirm?"

If not found, prompt: "No concepts brief found. Paste your raw brief here, or run `/id-brainstorm` first."

Resolve author from `git config user.name` or ask in chat.

---

## Step 2: Draft — The Problem, Audience, Terminal Objective

Using `resources/id-design-doc.md` as the template:

1. Write Sections 1 (The Problem), 2 (Audience), and the Terminal Objective from the ingested context
2. Save to `design_draft.md`
3. Notify: "Drafted Problem, Audience, Terminal Objective in `design_draft.md` at [path]. Key decisions: [2–3 bullet highlights]."

**Gate:**
> "Sections 1–2 drafted. Approve and proceed to Learning Objectives, or request revisions?"

---

## Step 3: Draft — Learning Objectives

1. Write Section 3 (Learning Objectives) using Bloom's taxonomy
   - Verify each objective uses a measurable verb
   - Assign Bloom's level explicitly
   - Link each objective to an assessment type placeholder
2. Update `design_draft.md`
3. Notify with path and 2–3 highlights

**Gate:**
> "Learning Objectives drafted. Approve and proceed to Theory Selection, or request revisions?"

---

## Step 4: Draft — Theory Selection

This section is mandatory and non-negotiable.

1. Read `resources/theory-pool.md`
2. Analyze the content type (concept/procedure/principle/problem), audience, and domain complexity
3. Evaluate at least 4–6 candidate theories from the pool
4. Write Section 4 (Theory Consideration Report):
   - Select 2–3 theories with explicit justification
   - Reject at least 2 with specific reason
   - Include at least 1 advanced theory (not just ADDIE + Bloom's)
   - Show how each selected theory translates into a design decision
5. Update `design_draft.md`

**Gate:**
> "Theory Selection drafted. Approve and proceed to Instructional Strategy, or request revisions?"

---

## Step 5: Draft — Instructional Strategy and Course Structure

1. Write Section 5 (Instructional Strategy):
   - Map each content type to a strategy
   - Explain sequence logic
   - Describe practice design (what learners do before assessment)
2. Write Section 6 (Course Structure):
   - Build the module table
   - Link each module to objectives
   - Estimate duration per module and total
3. Update `design_draft.md`

**Gate:**
> "Instructional Strategy and Course Structure drafted. Approve and proceed to Assessment, or request revisions?"

---

## Step 6: Draft — Assessment Strategy

1. Write Section 7 (Assessment Strategy):
   - For each objective, specify assessment type, format, and feedback design
   - Ensure assessment level matches Bloom's level of objective
   - Add formative checkpoints
   - Define summative assessment and pass threshold
2. Update `design_draft.md`

**Gate:**
> "Assessment Strategy drafted. Approve and proceed to Motivation Design, or request revisions?"

---

## Step 7: Draft — Motivation, Delivery, Constraints, Alternatives

1. Write Section 8 (Motivation Design — ARCS)
2. Write Section 9 (Delivery Specification)
3. Write Section 10 (Constraints and Risks)
4. Write Section 11 (Alternatives Considered) — from `concepts_brief.md` Alternatives Weighed section
5. Write Section 12 (Open Questions)
6. Update `design_draft.md`

**Gate:**
> "Remaining sections drafted. Approve and finalize, or request revisions?"

---

## Step 8: Finalize and Save

1. Check `design_draft.md` against `concepts_brief.md` for contradictions:
   - Report any contradiction (brief decided X, draft decides Y differently)
   - Ask the author to resolve each one
   - Apply decisions before saving

2. Save to `docs/designs/<course-name>.md`

3. Update `docs/designs/SITEMAP.md` if it exists (add: title, date, author, objectives count, status)

4. Notify: "Spec saved to `docs/designs/<course-name>.md`. Run `/id-review <path>` for Goldfish review."
