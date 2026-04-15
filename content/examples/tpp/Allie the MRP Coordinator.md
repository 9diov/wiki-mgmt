---
related-concepts:
  - "[[Work in Process (WIP) ⭐]]"
  - "[[Goldratt's Five Focusing Steps]]"
  - "[[The Four Types of Work ⭐]]"
sources:
  - "[[24-Chapter_19_•_Tuesday,_September_23|Chapter 19 — Tuesday, September 23]]"
---

# Allie the MRP Coordinator

## The Setup

During the IT leadership off-site, Bill describes a previous visit to the MRP-8 plant where Erik introduced him to Allie, the Manufacturing Resource Planning Coordinator. Her job is to decide whether the plant can accept a new production order.

Her process: when an order arrives, she looks at its bill of materials — the list of components and operations required to fulfill it. She identifies which work centers those operations pass through. She checks the current loading on each relevant work center. Based on that analysis, she decides whether accepting the new order would jeopardize any existing commitments.

If the heat treat oven is already at capacity for the next two weeks and the new order requires heat treating, she doesn't accept it — not without renegotiating something else.

Erik then asks Bill: how does IT make this same decision?

Bill's answer: IT doesn't. Work enters IT because someone in the business asked for it, or because Steve approved it, or because it appeared on a project list. There is no bill of materials, no work center loading check, no systematic answer to "can we actually do this without jeopardizing what we've already committed to?"

## What It Illustrates

**[[Work in Process (WIP) ⭐]]** — The absence of Allie's function in IT is the structural cause of WIP accumulation. When work is accepted without checking capacity, the only possible outcome is more WIP. Every project that enters the system against unavailable capacity either fails (generating unplanned recovery work) or succeeds by cannibalizing capacity from something else (jeopardizing prior commitments). Neither outcome is visible at the point of acceptance because there is no Allie to surface it.

**[[Goldratt's Five Focusing Steps]]** — Allie's process is Step 2 and Step 3 of the Five Focusing Steps in practice. She exploits the constraint (never wastes it on orders it can't absorb) and subordinates everything else to the constraint's tempo (new orders are accepted based on what the bottleneck work centers can handle, not on what the first station has available). Manufacturing has formalized this. IT, as of Chapter 19, has not.

**[[The Four Types of Work ⭐]]** — Without a capacity analysis at the point of acceptance, IT cannot distinguish between projects that are achievable given current WIP and projects that will compress the schedule for everything else. The result is over-commitment across all four work types simultaneously, with unplanned work ultimately consuming the margin that was supposed to be available for Types 1, 2, and 3.
