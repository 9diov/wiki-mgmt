Process one or more source chapters from the High Output Management wiki into summaries, concepts, and examples.

The user will tell you which chapters to process — either by number ("chapters 4 and 5"), by filename, or by range ("the next 3 chapters"). If unclear, ask.

---

## Paths

| Content | Location |
|---|---|
| Source chapters | `sources/hom/` |
| Summaries | `content/summaries/hom/` |
| Concepts | `content/concepts/` |
| Examples | `content/examples/` |

---

## Step 1 — Read source chapters

Read each specified chapter file from `sources/hom/`. Note the filename prefix (e.g. `09-`, `14-`) — summaries mirror this naming.

---

## Step 2 — Create summary

Create `content/summaries/hom/<prefix>-<Simplified Title>.md` for each chapter.

**Structure:**
```
# Chapter N: [Title]

## Core Idea
1–2 sentence distillation of the chapter's thesis.

## Key Concepts

**[Concept Name]**
2–5 sentence explanation. Include a concrete example if it clarifies.

...repeat for each major concept...

## Illustrative Examples  ← only if an example is prominent enough to call out
Brief description + what it illustrates.
```

Keep sections tight. Prefer one clear sentence over two vague ones.

---

## Step 3 — Extract concepts

For each distinct concept in the chapter, check whether a file already exists in `content/concepts/`. If it does, skip. If not, create it.

**Filename:** Normal casing with spaces, no dashes. E.g. `Limiting Step.md`, `Task Relevant Maturity.md`.

**Structure:**
```markdown
---
concept-type: "[[Framework]]"
description: "One sentence summary of the concept."
related-concepts:
  - "[[Other Concept]]"
sources:
  - "[[NN-Chapter N Title]]"
---

# [Concept Name]

One-line definition.

## Principle / [Relevant subheading]
Explanation.

## Why It Matters
...

```

For `related-concepts`, link to other concept files that are meaningfully connected.

For `concept-type`, use "[[Framework]]" for mental models that help diagnose situations (e.g. Leverage, Limiting Step, Managers Output), or "[[Practice]]" for actionable methods a manager implements (e.g. One-on-One, Delegation, Indicators).
  
For `description`, write a single sentence that captures the essence of the concept.
  
For `sources`, use the exact source filename with a display alias, e.g.: `[[13-Chapter_4__Meetings—The_Medium_of_Managerial_Work|Chapter 4 — Meetings]]`. Find the exact filename in `sources/hom/` before writing the link.

---

## Step 4 — Extract examples

For each concrete example, case study, or named scenario in the chapter, check whether a file already exists in `content/examples/`. If it does, skip. If not, create it.

**Filename:** Normal casing with spaces, no dashes. E.g. `Intel College Recruiting.md`, `Depressed Manager.md`.

**Structure:**
```markdown
---
description: "One sentence summary of the example."
related-concepts:
  - "[[Concept Name]]"
sources:
  - "[[NN-Chapter N Title]]"
---

# [Example Name]

Brief situation setup (1–3 sentences).

## [Relevant subheadings as needed]
Details.

## What It Illustrates
Which concepts this example demonstrates and why.

*Concepts: [[Concept A]], [[Concept B]]*
*Source: Chapter N*
```

---

## Step 5 — Link examples to concepts

For each concept file created in Step 3, add an ## Examples section, linking to the relevant example files extracted in Step 4.

How to identify relevant examples:
- Check the related-concepts frontmatter of each example file you just created
- Also consider thematic relevance — which examples best illustrate this concept?

Format:
```markdown 
## Examples 
- **[[Example Name]]** — one-line description of what this example illustrates about the concept 
- ... 
```

If no relevant examples exist for a concept, omit the section entirely.

---

## Step 6 — Link inline mentions in summaries
Re-read each summary you just created. Replace inline mentions of concept and example names with Obsidian wiki links.

**Rules:**
- Bold concept section headers: `**Limiting Step**` → `**[[Limiting Step]]**`
- Headers where display text differs from filename: `**Three Types of Production Operations**` → `**[[Production Operations|Three Types of Production Operations]]**`
- Inline concept terms: `lowest-value stage` → `[[Lowest Value Stage|lowest-value stage]]`
- Named examples: `the criminal justice system` → `[[Criminal Justice System|the criminal justice system]]`

Use `[[File Name|display text]]` alias syntax whenever the display text differs from the exact filename. Do not force links on vague or ambiguous mentions — only link where the reference is clear.

---

## Conventions

- **File names:** Normal casing, spaces, no dashes (`Managerial Activities.md` not `managerial-activities.md`)
- **Frontmatter links:** Obsidian `[[wiki link]]` format throughout
- **No duplicates:** Always check existing files before creating new ones
- **Parallelise reads** where possible to work efficiently
