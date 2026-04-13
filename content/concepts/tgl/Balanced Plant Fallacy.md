---
concept-type: "[[Framework]]"
description: The near-universal management goal of matching capacity exactly to demand — which Goldratt shows leads to falling throughput and rising inventory.
related-concepts:
  - "[[Dependent Events and Statistical Fluctuations]]"
  - "[[Local Optimization Trap]]"
  - "[[Goal Formulation]]"
  - "[[Throughput, Inventory, and Operating Expense ⭐]]"
sources:
  - "[[17-Chapter_11|Chapter 11 — New York Breakfast]]"
---

# Balanced Plant Fallacy

The conventional manufacturing goal: match the capacity of every resource exactly to market demand. No resource sits idle; no capacity is wasted. Every manager strives for this. Goldratt argues it is a fatal error.

## The Logic of the Balanced Plant

The intuition is sound on the surface:
- Excess capacity = money wasted on idle resources (OE too high)
- Insufficient capacity = missed throughput (T too low)
- Therefore: balance capacity exactly to demand = optimal

Every efficiency drive, every headcount trim, every capacity-utilization target follows from this logic.

## Why It Fails

When capacity is trimmed to exactly match demand, two things happen simultaneously:

1. **Throughput goes down**
2. **Inventory goes through the roof**

And because inventory rises, carrying costs (part of OE) rise with it — often enough to wipe out the OE savings from trimming capacity in the first place.

This is not a management failure; it is a mathematical consequence of the combination of [[Dependent Events and Statistical Fluctuations|dependent events and statistical fluctuations]] that exist in every production system. There is no balanced plant anywhere in practice, and it's not because managers lack skill or discipline — it's because the goal itself is wrong.

## The Correct Implication

The solution is *not* to add slack everywhere. It is to identify *where* capacity matters:

- At the **constraint** (the bottleneck): capacity must be protected and maximized — every idle moment here directly reduces throughput for the whole system
- At **non-constraints**: some idle time is acceptable and even desirable — keeping non-constraints busy just to hit utilization targets produces inventory that clogs the constraint

Rogo's plant ran robots at high utilization to justify their cost. The result: piles of parts that couldn't be assembled because other components were missing. The balanced-plant logic made things worse.

## The Broader Principle

The fallacy is a special case of the [[Local Optimization Trap]]: optimizing each resource locally (maximize utilization) produces a globally suboptimal system. The goal is not to keep everyone busy — it is to move the system toward its goal.

*Source: Chapter 11*
