## Overview

A wiki of important concepts and examples from notable management books.

## Goals
* Study on how to software engineering process
* esp. on how to applying agentic AI to the process

## Books

- High Output Management (HOM)
- The Goal (TGL)
- Toyota Production System (TPS)
- The Phoenix Project (TPP)
- Accelerate (ACC)
- The Toyota Way (TTW)

`book-id` convention: use short lowercase codes (for example: `hom`, `tgl`, `tps`, `tpp`, `acc`, `ttw`).

## Directory structure

```text
wiki-hom/
├── README.md
├── TODO.md
├── <book>.md                   # optional top-level book notes
├── content/
│   ├── concept-types/          # shared concept templates
│   ├── concepts/
│   │   ├── <book-id>/          # book-specific concepts
│   │   └── ...                 # shared concepts
│   ├── examples/
│   │   └── <book-id>/          # examples/cases by book
│   ├── summaries/
│   │   └── <book-id>/          # chapter-level summaries by book
│   └── synthesis/              # cross-book synthesis notes
├── demos/
│   └── <book-id>/              # demo artifacts
├── maps/
│   └── <book-id>/              # Obsidian canvas concept maps
└── sources/
    └── <book-id>/              # source text, epub, and extracted images
```

Note: hidden workspace/config folders such as `.obsidian/`, `.agents/`, and `.claude/` are omitted above.
