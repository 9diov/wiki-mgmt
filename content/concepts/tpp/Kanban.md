---
concept-type: "[[Practice]]"
description: A visual work management system — originally from Toyota production — that makes demand and WIP visible, limits work in progress to available capacity, and enables work to be pulled through the system at a predictable, controllable rate.
related-concepts:
  - "[[Work in Process (WIP) ⭐]]"
  - "[[The Three Ways ⭐]]"
  - "[[Goldratt's Five Focusing Steps]]"
  - "[[The Brent Problem ⭐]]"
  - "[[Change Advisory Board (CAB)]]"
sources:
  - "[[20-Chapter_15_•_Wednesday,_September_17|Chapter 15 — Wednesday, September 17]]"
  - "[[27-Chapter_22_•_Monday,_September_29|Chapter 22 — Monday, September 29]]"
aliases:
  - Kanban Board
  - Visual Work Management
---

# Kanban

Erik first names the change board as a kanban in Chapter 15, connecting it to David Anderson's adaptation of Goldratt's manufacturing principles for software and IT operations. Patty builds a working kanban for IT service requests in Chapter 22 after visiting MRP-8 and speaking with a plant supervisor directly.

## The Mechanism

A kanban board visualizes the state of work across three basic columns:

- **Ready**: work that has been accepted and is waiting to begin
- **Doing**: work actively in progress
- **Done**: work completed

The critical constraint is the "Doing" column: the number of cards that can be in progress simultaneously is capped. When Doing is full, no new card can enter it until one completes. This is the WIP limit.

The WIP limit forces single-tasking. A resource working one thing at a time is measurable — the time from entering Doing to Done can be timed, averaged, and used to predict future lead times. A resource context-switching across seven things has no predictable lead time because the queue effects are compound and non-linear.

## What It Achieves

Patty's laptop replacement kanban in Chapter 22 demonstrates the outcomes:

- **Predictable lead times**: Once each step is timed and WIP is capped, delivery dates become calculable and publishable. Requesters can see when their laptop will arrive.
- **Higher accuracy**: Defect rate (configuration errors) dropped from ~15 errors per delivery to near zero, because work instructions are now checked at each handoff in the visible "Doing" state.
- **Earlier completion**: Bill's laptop arrives two days before the published date — not because resources were added, but because the elimination of multitasking removed the coordination overhead that previously slowed everything down.

None of this required additional staff. All gains came from making the flow visible and limiting the WIP.

## The Change Board as Kanban

The Parts Unlimited change board — Patty's index card system — is a kanban even before she calls it one. It makes the week's changes visible in a single view, separates upcoming work from in-progress from completed, enables collision detection, and provides a timeline for incident diagnosis. Erik validates this in Chapter 15 and connects it to Anderson's work.

In Chapter 22, Patty upgrades the change board with color-coding:
- **Purple** cards: changes supporting the top five business projects
- **Yellow** cards: other changes
- **Green** cards: internal IT improvement projects (allocated at 20% of capacity)
- **Pink sticky notes**: blocked cards — reviewed twice daily

The color allocation makes the "right balance" visible: a board dominated by purple with no green means improvement work is being crowded out. The visual makes this detectable at a glance without requiring a report.

## Kanban for the Constraint

Patty also plans a kanban specifically around Brent: formalizing how work reaches him, making the upstream queue and downstream dependencies visible, and preventing direct escalations that bypass the gating mechanism. A kanban for the constraint is the operational implementation of Step 3 (subordinate): all work release to Brent is governed by the board, so his capacity is visible and manageable rather than invisible and continuously exceeded.

## Relation to Pull Systems

Kanban is a pull system, not a push system. Work enters "Doing" when capacity becomes available — when something completes and a slot opens. In a push system, work is released when it is ready to be done; in a pull system, work is released when the downstream work center has capacity to absorb it. The distinction is the difference between Mark at the job release desk (push: releasing work whenever his station is free) and constraint-aware scheduling (pull: releasing work only at the rate the constraint can consume it).
