---
related-concepts:
  - "[[Change Advisory Board (CAB)]]"
  - "[[Uncontrolled Change ⭐]]"
  - "[[The Four Types of Work ⭐]]"
sources:
  - "[[14-Chapter_9_•_Tuesday,_September_9|Chapter 9 — Tuesday, September 9]]"
---

# The 173 Changes on Friday

## The Setup

At the second functioning CAB meeting, Patty puts up the week's change calendar on the whiteboard — a visual display of all submitted changes plotted by day.

The pattern is immediately visible: 173 of the week's changes are clustered on Friday. Friday is also the scheduled day for the Phoenix deployment — the most critical and risky IT event of the quarter.

No individual team had known this. Each team submitting a Friday change was aware of their own change and the Phoenix deployment on their calendar. None of them had visibility into what the other 172 teams were planning.

Presented with the collision, engineers in the room voluntarily begin rescheduling. They move changes earlier in the week, redistribute the load, and clear Friday's concentration without being told to. The calendar makes the problem visible; the engineers fix it themselves.

## What It Illustrates

**[[Change Advisory Board (CAB)]]** — The 173-changes discovery is the CAB's clearest demonstration of value. Without the change calendar, each team would have proceeded with its Friday change independently, with no awareness that their change was one of 173 landing simultaneously on the highest-risk day of the quarter. The collision detection happened because every team's changes were visible in one place — the whiteboard — before any of them were implemented. The CAB's function here is not approval but awareness: making the aggregate visible so each team can make an informed decision.

**[[Uncontrolled Change ⭐]]** — The 173 changes aren't uncontrolled in the sense of being unauthorized — they've all been submitted. The risk is the uncoordinated concentration: 173 simultaneous changes on Phoenix deployment day creates compounding diagnostic difficulty for any incident that follows. If something breaks Friday night, the question "what changed?" has 173 answers. The change calendar converts a coordination failure into a coordination opportunity.
