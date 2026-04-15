---
concept-type: "[[Framework]]"
description: The worst of TPS's seven wastes — producing more than is needed, or earlier than needed, which generates all other wastes downstream.
related-concepts:
  - "[[Just-in-Time ⭐]]"
  - "[[Pull System and Kanban ⭐]]"
  - "[[Production Leveling (Heijunka)]]"
  - "[[Autonomation (Jidoka) ⭐]]"
sources:
  - "[[05-Chapter_1__Starting_from_Need|Chapter 1 — Starting from Need]]"
---

# Overproduction

Ohno's hierarchy of waste places overproduction at the top — not because it is the most obvious, but because it is the most generative. Overproduction creates and conceals every other waste.

> *"There is no waste in business more terrible than overproduction."*

## Why It Is the Worst Waste

Most waste is visible: a defective part, an idle worker, a long transport route. Overproduction is different — it looks like productivity. A machine running at full speed producing parts that aren't needed appears efficient. The inventory it creates is recorded as an asset. The labor consumed is counted as output.

The damage is downstream and delayed:
- **Excess inventory** ties up cash and space, and hides quality problems until the parts are needed (when it's too late to fix them cheaply)
- **Defective inventory** is a particularly severe form — parts made before defects were discovered; an entire batch may be worthless
- **Obscured problems** — inventory buffers absorb disruptions, so the root causes of those disruptions are never felt urgently enough to fix
- **Misallocated labor** — workers making unneeded parts are not available to make needed ones

## The Psychological Root

Ohno traces the instinct to overproduce to a deep human tendency: hoarding against scarcity. Farmers stored rice against disaster; modern workers and managers build inventory against disruption. The instinct is not irrational given the history, but it is destructive in an industrial context.

The oil crisis revealed this: companies that had built inventory against a slowdown found themselves holding liabilities, not assets. The inventory didn't save them; it burdened them.

## The Revolution in Consciousness

Eliminating overproduction requires accepting a counterintuitive posture: *run machines less*. A machine sitting idle because downstream doesn't need parts is not wasting capacity — it is obeying the system. A machine running to produce unneeded parts is wasting everything.

Ohno calls this shift a "revolution in consciousness." Managers trained in utilization metrics resist it fiercely. An idle machine feels wrong; a running machine feels right. This intuition is exactly backward in a pull system.

## How TPS Prevents It

- **[[Pull System and Kanban ⭐]]** — nothing is produced without a downstream signal; no authorization to produce = no production
- **[[Just-in-Time ⭐]]** — the system is designed around consuming exactly what is needed
- **[[Autonomation (Jidoka) ⭐]]** — stops the line when defects occur, preventing the specific worst case: mass production of defective parts
