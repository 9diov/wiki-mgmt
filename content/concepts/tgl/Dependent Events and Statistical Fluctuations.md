---
concept-type: "[[Framework]]"
description: The two phenomena present in every production system whose combination — not either alone — explains why balanced plants fail and inventory accumulates.
related-concepts:
  - "[[Balanced Plant Fallacy]]"
  - "[[Local Optimization Trap]]"
  - "[[Throughput, Inventory, and Operating Expense ⭐]]"
sources:
  - "[[17-Chapter_11|Chapter 11 — New York Breakfast]]"
  - "[[19-Chapter_13|Chapter 13 — The Boy Scout Hike]]"
---

# Dependent Events and Statistical Fluctuations

Two phenomena found in every plant. Neither causes problems alone. Together, they guarantee that a balanced plant will produce falling throughput and rising inventory.

## Dependent Events

A dependent event is one that cannot begin until prior events are complete. In any production sequence — cut, drill, assemble, test, ship — each step depends on the one before it. This is not unusual; it describes virtually every manufacturing and service process.

The consequence: **variations at one step cannot be recovered downstream.** If step 3 runs slow, step 4 cannot "make up" for it by running fast — step 4 can only run as fast as step 3 delivers work to it. Slowness propagates forward; speed does not.

## Statistical Fluctuations

Most production variables cannot be determined precisely in advance. How long will a setup take? How many parts will be scrapped? When will a machine go down? These vary from one instance to the next — they are statistically distributed around an average, not fixed.

This is normal and unavoidable. The average might be reliable, but any individual instance can be faster or slower than average.

## Why Their Combination Is Destructive

Individually:
- Dependent events alone, with zero fluctuation, would flow perfectly — every step always takes exactly the same time, queues never form
- Statistical fluctuations alone, without dependency, would average out — some steps run fast, some slow, but nothing is waiting on anything else

Together, they interact asymmetrically:

> **Slow runs accumulate. Fast runs don't.**

When one step runs slow (below average), the next step must wait — it cannot start until work arrives. The delay is real and passed forward. When one step runs fast (above average), it simply builds a small queue ahead of the next step — the speed is not "banked" to compensate for future slowness. It is absorbed into inventory.

Over time, in a balanced system with no slack, every statistical dip propagates as a delay while every statistical spike builds inventory. The system drifts toward longer cycle times and higher work-in-process, even though the average speed of each step is exactly at capacity.

## The Demonstrations

**The Boy Scout hike (Chapter 13):** scouts walking single file, each with variable pace, dependent on the scout ahead. The gap between first and last grows continuously — not because anyone is slow on average, but because slowness travels backward while speed does not.

**The dice game (Chapter 14):** a controlled proof. Five bowls (dependent events), one die per station (fluctuations, average 3.5), capacity perfectly balanced to demand. Expected throughput after 20 turns: 70 matches. Actual: ~40. Inventory accumulates in waves at the back of the chain — worst at the final station, the one that produces throughput. The deviation grows over time and does not self-correct. This is not bad luck; it is the mathematical structure of the system.

## The Implication

The only way to prevent this accumulation is to place **protective capacity** (slack) ahead of the constraint — the one step that limits the whole system. This is the setup for the Theory of Constraints: rather than balancing all capacity to demand, identify the constraint and manage the system around it.

*Source: Chapter 11*
