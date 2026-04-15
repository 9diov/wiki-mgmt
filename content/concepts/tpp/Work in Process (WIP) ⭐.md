---
concept-type: "[[Framework]]"
description: Work that has been started but not completed — the invisible accumulation of in-flight tasks, changes, and projects that degrades flow, creates dependencies, and compounds into chronic due-date failures. Erik's "silent killer," applied directly to IT Operations in Chapter 11.
related-concepts:
  - "[[The Four Types of Work ⭐]]"
  - "[[The Three Ways ⭐]]"
  - "[[The Brent Problem ⭐]]"
  - "[[Change Advisory Board (CAB)]]"
  - "[[Change Risk Tiers]]"
  - "[[Technical Debt]]"
  - "[[Goldratt's Five Focusing Steps]]"
sources:
  - "[[12-Chapter_7_•_Friday,_September_5|Chapter 7 — Friday, September 5]]"
  - "[[16-Chapter_11_•_Thursday,_September_11|Chapter 11 — Thursday, September 11]]"
  - "[[24-Chapter_19_•_Tuesday,_September_23|Chapter 19 — Tuesday, September 23]]"
aliases:
  - WIP
  - Work in Process
---

# Work in Process (WIP)

Erik introduces WIP in Chapter 7 from the catwalk of the MRP-8 plant: *"WIP is one of the root causes for chronic due-date problems, quality issues, and expediters having to rejuggle priorities every day."* In the plant's earlier era, inventory piled so high you couldn't see across the building. Every day was an emergency. The plant held a standing record as best customer of an air freight company from shipping thousands of pounds of finished goods overnight to angry customers.

In Chapter 11, Bill realizes this is not a historical anecdote — it is an exact description of his change process in the present tense.

## The IT Equivalent

On the manufacturing floor, WIP is physical: pallets of partially-processed parts stacked between work centers, waiting for the next operation. In IT, WIP is invisible — but it accumulates in the same way and produces the same damage:

- **Change cards** that have been authorized and scheduled but never completed
- **Tickets** opened but not resolved, cycling through queues
- **Projects** started but blocked, consuming planning and coordination overhead without producing output
- **Incidents** in progress simultaneously, each pulling the same engineers in different directions

At Parts Unlimited by Chapter 11: 942 pending change cards, growing at a rate that would cross 1,000 the following week. The cards are physically running out of space on the whiteboards. This is inventory piled to the ceiling — just in a different medium.

## Why WIP Accumulates

WIP accumulates when work is released into the system faster than the constraint can process it. In the plant, Mark at the job release desk released jobs whenever his station was free, without checking whether the bottleneck downstream could absorb them. The result: work piled at the bottleneck while the first station looked productive.

In IT, the equivalent is authorizing changes and starting projects without checking whether the constraint (Brent, or whatever the bottleneck resource is) has capacity to handle them. The CAB at Parts Unlimited was releasing 437 changes per week while Brent — who was in the path of many of them — was already reserved exclusively for Phoenix. Changes were authorized against capacity that didn't exist.

## The Compound Effect

WIP does not accumulate linearly — it compounds:

- Incomplete work carries forward into the next period, competing with new work
- Each piece of WIP creates dependencies: a change that was started but blocked may prevent other changes from proceeding
- Large WIP increases the time to diagnose problems (more things changed recently = harder to isolate cause)
- High WIP creates the illusion of productivity (many things in progress) while actual throughput falls

Bill's arithmetic in Chapter 11: 240 incomplete changes from the current week, plus 400+ incoming next week, equals 640 on the schedule. At a sustained 60% incompletion rate, the number compounds — thousands of incomplete changes within weeks, each one a potential dependency or conflict for future work.

## The Management Response

The manufacturing solution was to freeze job releases until the WIP drained to manageable levels, then reintroduce work based on the bottleneck's tempo — not the first station's availability.

The IT equivalent: make the constraint visible at the point of work release. At Parts Unlimited, this means flagging Brent-dependent changes on the card at submission time, before they are authorized, so the CAB can triage against actual constraint capacity rather than discovering the dependency mid-change.

The broader principle: **you cannot control WIP you cannot see.** The change process made WIP visible for the first time. The natural instinct — abandon the process because it revealed an alarming number — is precisely backwards. The process didn't create the WIP; it revealed WIP that was already there, invisible and unmanaged.

## The Project Freeze as WIP Reduction (Chapter 19)

In Chapter 19, Bill proposes freezing all non-Phoenix work across IT Operations and halting all Development-to-Operations deployments for two weeks. The logic is the manufacturing WIP freeze:

- Stop releasing new jobs into the plant
- Existing WIP drains as finished goods
- WIP falls → due-date performance rises
- Resume releasing work at the constraint's actual tempo

Erik validates the proposal explicitly using this analogy, walking Steve through the manufacturing version before connecting it to IT. Steve's initial resistance — "subsidized potato farmers paid not to grow crops" — dissolves when he follows the logic himself.

The freeze also includes a technical debt component: Development will tackle the top sources of unplanned work during the freeze period, paying down debt principal rather than just stopping new debt accumulation.

## The Capacity Analysis Gap

Erik introduces Allie, the MRP coordinator at the MRP-8 plant, as the model for how capacity decisions should work. When a new order arrives, Allie checks the bill of materials, identifies the relevant work centers, checks their loading, and determines whether the new order would jeopardize existing commitments. Only then does she accept or reject it.

Erik asks Bill how IT makes the equivalent decision. Bill's honest answer: it doesn't. Work enters IT because someone in the business requested it, or because Steve approved it, or because it appeared on a project list. There is no systematic check of whether IT has capacity to complete the work before committing to it.

This is the structural cause of WIP accumulation: work enters the system without analysis. The only possible outcome is more WIP, more shortcuts, and more unplanned work.

## Relation to the Three Ways

WIP accumulation is the primary enemy of the First Way (fast flow). Flow requires that work move through the system without piling up at any point. A system with high WIP has, by definition, slow flow — work spends more time waiting than being processed. Reducing WIP is not a secondary optimization; it is the prerequisite for achieving the flow that makes reliable delivery possible.
