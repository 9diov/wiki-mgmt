---
concept-type: "[[Framework]]"
description: A scheduling method in which the bottleneck sets the pace for the entire plant, a protective buffer of inventory sits in front of the bottleneck, and material release is tied to the bottleneck's consumption rate.
related-concepts:
  - "[[The Constraint ⭐]]"
  - "[[Balance Flow Not Capacity]]"
  - "[[Activation vs Utilization]]"
  - "[[Subordinate and Elevate ⭐]]"
  - "[[Exploit the Bottleneck ⭐]]"
sources:
  - "[[32-Chapter_26|Chapter 26 — The Drum and the Rope]]"
aliases:
  - DBR
---

# Drum-Buffer-Rope

A scheduling method that operationalizes "balance flow, not capacity" — making the bottleneck govern the rate of the entire plant rather than letting non-bottlenecks run at their own capacity.

Introduced through Sharon's drummer analogy and Dave's rope analogy in Chapter 26.

## The Three Elements

### Drum
The bottleneck's processing schedule. Like a drummer in a parade, the bottleneck sets the beat that everyone else marches to. Its output rate determines the plant's throughput rate. The drum schedule specifies what the bottleneck works on and when.

### Buffer
A small protective stock of work-in-process kept in front of the bottleneck — typically a few days' worth. The buffer absorbs statistical fluctuations in upstream operations without requiring those operations to overproduce. If an upstream step runs slow for a day, the buffer covers the bottleneck; if it runs fast, the buffer grows slightly and then returns to normal. The buffer is sized to protect the bottleneck from starvation, not to maximize efficiency of upstream steps.

### Rope
The signal that ties material release at the start of production to the bottleneck's consumption rate. The rope replaces the push-scheduling logic (release materials when non-bottlenecks run out of work) with pull-scheduling logic (release materials when the bottleneck will be ready for them).

In practice: calculate the queue at the bottleneck, add the travel time from raw material release to bottleneck arrival, and release materials only when the math says the bottleneck will need them. Non-bottlenecks process materials when they arrive; the rate at which materials arrive is governed by the drum.

## Why It Solves the Inventory Problem

Without DBR: non-bottlenecks release or process work whenever they have capacity. Since non-bottlenecks have more capacity than the bottleneck, they generate parts faster than the bottleneck can absorb them. Inventory accumulates in front of the bottleneck and at assembly.

With DBR: material enters the system at the bottleneck's rate. Non-bottlenecks will have idle time (they have excess capacity by definition). But idle non-bottleneck time costs nothing extra; it does not increase operating expense. Excess inventory does.

## The Equivalence to Hike Reordering

Jonah observed that releasing materials according to the bottleneck's rate achieves the same practical effect as physically moving the bottleneck to the front of the production sequence — which is what Rogo did on the hike by moving Herbie to the front of the line. Material doesn't enter the system until the bottleneck is ready for it; everything upstream has the character of feeding the front of the line rather than racing ahead of it.

## Scope

DBR governs release of all materials — not just bottleneck-bound (red) parts. Once the bottleneck schedule determines when red-tag parts will reach final assembly, green-tag part releases can be calculated by working backwards from those assembly dates. The bottleneck schedule becomes the master schedule for the plant.
