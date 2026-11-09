# ID Spec Studio

A course design spec pipeline for instructional designers, built on Google's [Elephant-Goldfish Model](https://github.com/google/elephant-goldfish-model).

Turn a raw course brief into a reviewed, locked instructional design specification — using parallel Goldfish reviewers that read your spec cold, with no prior context and no tendency to agree.

---

## What this is

EGM's Elephant-Goldfish pattern was built for software spec review: one agent (Elephant) drafts with full context, multiple fresh subagents (Goldfish) review without it. This repo adapts that pattern for instructional design spec creation and review.

**The pipeline has three stages:**

| Stage | Skill | What happens |
|---|---|---|
| 1 | `id-brainstorm` | Multi-turn clarification → Goldfish stress-test → `concepts_brief.md` |
| 2 | `id-draft` | Section-by-section spec with approval gates → `docs/designs/<course-name>.md` |
| 3 | `id-review` | 4 Goldfish reviewers in parallel → consolidated findings report → resolution loop |

**The four Goldfish reviewers:**

| Reviewer | What they check |
|---|---|
| Alignment | Every objective has an activity and an assessment; Bloom's level matches |
| Learner | Audience specificity, prerequisite realism, motivation acknowledgment |
| Practicality | Scope vs timeline, media vs tool capability, build hour estimates |
| Theory | Theory Consideration Report exists, theories applied (not just listed), Merrill's First Principles present |

**What the reviewers reference:**
- An 8-standard ID review rubric (`resources/id-review-standard.md`)
- A pool of 60+ instructional design theories (`resources/theory-pool.md`)
- A 13-section course design spec template (`resources/id-design-doc.md`)

---

## First real run results

A 30-minute Rise 360 sales training spec was run through the pipeline:

- 4 parallel Goldfish returned **44 raw findings**
- After deduplication: **32 final findings** — 4 Blockers, 22 Majors, 6 Nits

The 4 Blockers:
- 🔴 Pass rule covered 1 of 3 terminal objective criteria
- 🔴 Core content (5 differentiators, 5 scripts) didn't exist yet — no SME sign-off date
- 🔴 Deal-math figures unquantified — but spec claimed learners would see "their own numbers"
- 🔴 Manager observation capacity "not yet committed" with no fallback

All four would have caused rework cycles in build or credibility problems in delivery.

---

## Prerequisites

1. [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) installed
2. Google's Elephant-Goldfish Model installed as a Claude Code plugin:

```bash
claude plugin marketplace add google/elephant-goldfish-model
claude plugin install egm@egm
` ` `

---

## Setup

` ` `bash
git clone https://github.com/linuxsunil/id-spec-studio.git
cd id-spec-studio
claude .
` ` `

Then in Claude Code:

` ` `
Read CLAUDE.md and the skills/id-brainstorm/SKILL.md. I want to run id-brainstorm on a new course brief.
` ` `

> **Note on slash commands:** The skills in this repo are invoked by instructing Claude Code to read the relevant SKILL.md, not via `/id-brainstorm` as a slash command. The EGM plugin provides the Goldfish subagent infrastructure; the ID-specific logic lives in the markdown skill files.

---

## Repo structure

` ` `
id-spec-studio/
├── CLAUDE.md
├── skills/
│   ├── id-brainstorm/SKILL.md
│   ├── id-draft/SKILL.md
│   └── id-review/SKILL.md
├── agents/
│   ├── alignment-reviewer.md
│   ├── learner-reviewer.md
│   ├── practicality-reviewer.md
│   └── theory-reviewer.md
├── resources/
│   ├── id-review-standard.md
│   ├── id-design-doc.md
│   └── theory-pool.md
└── docs/
    └── designs/
        └── SITEMAP.md
` ` `

---

## Inspiration

This project is built on top of Google's [Elephant-Goldfish Model](https://github.com/google/elephant-goldfish-model). The Goldfish pattern — fresh subagents reviewing cold — is EGM's core contribution. ID Spec Studio adds the domain layer: ID-specific Goldfish personas, an instructional design review standard, a theory pool, and a spec template grounded in learning theory.

---

## License

MIT
```

---

(Remove the spaces inside the backtick triples ` ` ` → ``` when you paste — I had to break them here to avoid formatting issues.)

Once README.md is saved, run this in the terminal:

```bash
git pull origin main --allow-unrelated-histories
git add .
git commit -m "Initial release: ID Spec Studio"
git push origin main
```

That's it — one clean push of everything.