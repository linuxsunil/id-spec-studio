# ID Spec Studio

A course design spec pipeline built on the Elephant-Goldfish Model (EGM).
Turn a raw brief into a reviewed, locked instructional design specification.

## What this does

Three skills run in sequence:

1. `/id-brainstorm` — drill a raw brief into a structured concepts brief
2. `/id-draft` — build the full course design spec section by section
3. `/id-review` — four Goldfish reviewers tear the spec apart in parallel

Output: a reviewed `course_design_spec.md` in `docs/designs/` ready to hand to any build pipeline.

## Skills

| Command | File | Purpose |
|---|---|---|
| `/id-brainstorm` | `skills/id-brainstorm/SKILL.md` | Brief → concepts_brief.md |
| `/id-draft` | `skills/id-draft/SKILL.md` | Brief → course_design_spec.md |
| `/id-review` | `skills/id-review/SKILL.md` | Spec → reviewed spec |

## Agents (Goldfish reviewers)

| Agent | File | Lens |
|---|---|---|
| Alignment Reviewer | `agents/alignment-reviewer.md` | Objectives ↔ activities ↔ assessment coherence |
| Learner Reviewer | `agents/learner-reviewer.md` | Audience realism, prerequisites, prior knowledge |
| Practicality Reviewer | `agents/practicality-reviewer.md` | Buildability within stated constraints |
| Theory Reviewer | `agents/theory-reviewer.md` | Evidence-based design — theory selection and application |

## Resources

- `resources/id-review-standard.md` — the rubric all Goldfish apply
- `resources/id-design-doc.md` — the course design spec template
- `resources/theory-pool.md` — 60+ ID theories with selection guidance

## Working files (created during a session)

- `concepts_brief.md` — output of id-brainstorm
- `design_draft.md` — working draft during id-draft
- `docs/designs/<course-name>.md` — final approved spec
- `*_report.md` — Goldfish review reports

## Usage

Open this folder in Claude Code and run:

```
/id-brainstorm  [paste your raw brief or describe the course need]
```

Then follow the gates.
