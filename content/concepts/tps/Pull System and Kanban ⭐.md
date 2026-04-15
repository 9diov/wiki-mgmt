---
concept-type: "[[Practice]]"
description: The physical mechanism of just-in-time — later processes withdraw from earlier ones using kanban (signal cards) as the only authorization to produce.
related-concepts:
  - "[[Just-in-Time ⭐]]"
  - "[[Production Leveling (Heijunka)]]"
  - "[[Overproduction]]"
sources:
  - "[[05-Chapter_1__Starting_from_Need|Chapter 1 — Starting from Need]]"
aliases:
  - Kanban
  - Pull production
---

# Pull System and Kanban

The pull system is the operational mechanism by which just-in-time is realized. Kanban (看板, "sign board" or "signal card") is the information carrier that authorizes production and movement within the pull system.

## The Logic of Pull

In a push system, each process produces according to a schedule and forwards output to the next process. The schedule is built from a forecast of what will be needed. Wherever forecast deviates from reality — which is always — inventory accumulates or shortages occur.

In a pull system, nothing is produced until the downstream process signals that it needs something. The later process goes to the earlier process and withdraws exactly what it needs. The earlier process then produces only to replenish what was taken. The production signal travels backward through the chain; actual consumption is the trigger.

Ohno's formulation: *"A later process goes to an earlier process to pick up only the right part in the quantity needed at the exact time needed. In this case, wouldn't it be logical for the earlier process to make only the number of parts withdrawn?"*

## What Kanban Is

Kanban is the physical signal — originally a card, ticket, or container — that travels with parts through the system. It carries:
- What part is needed
- How many are needed
- Where they come from and where they go

When a process consumes a part, the kanban attached to that part is released and travels back to the supplying process as a production or withdrawal authorization. No kanban, no production. The kanban is both the permission slip and the information system.

## Why It Controls Inventory

Because production only occurs in response to a kanban signal, and kanbans are issued in fixed quantities, the total number of kanbans in the system caps the total inventory. Reducing the number of kanbans reduces inventory and increases the pressure to eliminate the problems that made large buffers feel necessary.

Ohno: *"Kanban accelerates improvements."* A system with large inventory tolerates large problems. A system with tight kanban counts cannot — each problem that causes a stoppage is immediately visible and painful.

## The Supermarket Insight

Ohno explicitly credits the American supermarket as the inspiration. In a supermarket, customers take what they need from the shelf; the shelf is restocked only to replace what was taken. The store doesn't push goods onto customers — customers pull goods from shelves. Ohno visited the United States in 1956 and returned with this model in mind.

## Kanban Is Not a Scheduling System

Kanban is often mistaken for a production scheduling tool. It is not. It is a constraint on production — a mechanism for preventing overproduction by ensuring nothing moves without a signal from downstream. The planning question ("what should we make this month?") is answered by production leveling. Kanban answers the execution question: "make this part now, because it was just consumed."
