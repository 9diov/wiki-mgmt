Scan summary files and turn inline mentions of concepts and examples into Obsidian wiki links.

Use this after adding new concept or example files, or any time summaries need their links refreshed.

---

## Step 1 — Build the reference list

List all files in `content/concepts/` and `content/examples/` (filenames without `.md`). These are the link targets.

---

## Step 2 — Scan summaries

Read all files in `content/summaries/` (recursively). For each file, identify mentions that correspond to a concept or example filename.

**What to link:**

| Pattern | Link as |
|---|---|
| Bold header matches concept name exactly | `**[[Concept Name]]**` |
| Bold header matches concept name with different wording | `**[[Concept Name\|Header Text]]**` |
| Inline term clearly refers to a concept | `[[Concept Name\|display text]]` |
| Named example or case study reference | `[[Example Name\|display text]]` |

**What not to link:**
- Vague or partial matches where the reference is ambiguous
- Mentions already linked
- Terms that appear in frontmatter or code blocks

---

## Step 3 — Apply edits

Update each summary file with the links identified. Use `[[File Name|display text]]` alias syntax whenever the display text differs from the exact filename.

Read each file before editing it.
