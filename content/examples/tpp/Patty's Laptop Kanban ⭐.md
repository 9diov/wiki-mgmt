---
related-concepts:
  - "[[Kanban]]"
  - "[[Work in Process (WIP) ⭐]]"
  - "[[Wait Time and Utilization]]"
sources:
  - "[[27-Chapter_22_•_Monday,_September_29|Chapter 22 — Monday, September 29]]"
---

# Patty's Laptop Kanban

## The Setup

Laptop replacements at Parts Unlimited have been a running embarrassment. Bill has been using a duct-taped machine for weeks; his replacement has been lost in the queue. Patty has seen this as an opportunity to test something.

She visits MRP-8, spends an hour with a plant supervisor, and comes back with a working system. She maps the four most common service request types (laptop/desktop replacement, account management, office moves, password resets), documents each step, times each operation, and builds a kanban board:

- Four rows, one per request type
- Three columns: **Ready / Doing / Done**
- Work must flow through the board — not email, phone, or Slack
- Doing column is capped; nothing new enters until something completes

She publishes a laptop replacement schedule: every requester listed with their submission date and projected delivery date. Bill is fourteenth in line, projected for Friday.

Two days later — Wednesday — his new laptop arrives. Fully configured. All data transferred. Every application present. He is delivered two days ahead of schedule. Every person ahead of him has also received theirs. Defect rate (configuration errors) has dropped from an average of fifteen corrections per system to near zero, because the work instructions are now checked at each step, and errors are corrected in the instructions rather than fixed case-by-case.

Patty's summary: *"Imagine what this will do to user satisfaction if we could tell them when they make the request how long the queue is, tell them to the day when they'll get it, and actually hit the date, because we're not letting our workers multitask or get interrupted!"*

## What It Illustrates

**[[Kanban]]** — The board's WIP limit is the mechanism that makes everything else work. When only one laptop at a time can be in the "Doing" state per worker, the work is observable, timeable, and correctable. When workers were handling requests ad hoc — via email, phone, and direct ask — the actual state of any request was invisible, lead times were unpredictable, and errors were discovered only when someone complained. The board converts invisible, multi-threaded work into visible, single-threaded flow.

**[[Work in Process (WIP) ⭐]]** — The previous state was high WIP: many laptops requested, all being "worked on" in some vague sense, none on a predictable timeline. The kanban collapses that into a visible queue with a defined throughput rate. The improvement in delivery time came not from adding resources but from reducing multitasking — which is WIP reduction at the individual worker level.

**[[Wait Time and Utilization]]** — The fifteen-errors-per-delivery figure reflects the cost of high utilization and constant context-switching: workers moving between requests without finishing, catching errors only at delivery, reworking under time pressure. Capping WIP reduces effective utilization of the request queue and, consistent with the wait time formula, reduces the time each request spends in the system.
