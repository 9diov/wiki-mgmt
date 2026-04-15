---
concept-type: "[[Practice]]"
description: Smoothing production volume and mix over time so that each process runs at a steady, predictable rate — the pre-condition for just-in-time to work.
related-concepts:
  - "[[Just-in-Time ⭐]]"
  - "[[Pull System and Kanban ⭐]]"
  - "[[Overproduction]]"
sources:
  - "[[05-Chapter_1__Starting_from_Need|Chapter 1 — Starting from Need]]"
aliases:
  - Heijunka
  - Level production
---

# Production Leveling (Heijunka)

Production leveling — *heijunka* in Japanese — is the practice of smoothing both the volume and the mix of production over time. Instead of making all of one thing, then all of another, or doing all the month's work at month-end, production is spread into small, consistent increments throughout the day and month.

## The Problem It Solves: Dekansho Production

Early Toyota suffered from what Ohno called "dekansho production" — named after a folk song about sleeping half the year. Parts arrived from suppliers irregularly throughout the month; assembly could only happen when enough parts had accumulated. All the assembly work bunched at month-end.

The consequences were severe: workers idle early in the month, frantic at the end; suppliers receiving irregular orders and unable to plan; quality suffering under end-of-month pressure; no possibility of running a pull system when demand was random.

## The Arithmetic of Leveling

Ohno's formulation is simple: if 1,000 parts are needed per month, and there are 25 working days:
- Make **40 parts per day**
- In an 8-hour (480-minute) day: **one part every 12 minutes**

This target rate — one unit per unit of time — is called *takt time*. Every process in the system is then tuned to this rate. Faster processes have idle time; slower ones are the target for improvement.

## Why It Enables Just-in-Time

Pull systems depend on a steady withdrawal rate from downstream processes. If demand arrives in spikes — 0 parts needed for three weeks, then 500 needed in two days — upstream processes cannot respond without either building inventory in advance (overproduction) or failing to deliver (shortfall).

Leveled demand makes pull feasible. When downstream withdraws at a predictable rate, upstream can produce at a matching rate, kanban quantities can be sized correctly, and the entire system stabilizes.

## The Supplier Dimension

Leveling is not only an internal discipline. Ohno explicitly extends it to suppliers: Toyota must give suppliers leveled, predictable order patterns to make their cooperation in JIT feasible. A supplier receiving lumpy orders will rationally build inventory to protect themselves — which transfers the waste upstream rather than eliminating it.

## Leveling vs. Responsiveness

A common objection: leveling seems to reduce flexibility. If production is smoothed to a constant rate, how does the system respond to a sudden spike in demand?

The TPS answer: the spike should be absorbed by small adjustments to the leveled plan (adjusting takt time, adding overtime), not by abandoning level production and reverting to batch production. The discipline of level production is more valuable than the apparent flexibility of batch production — because batch production's "flexibility" always comes at the cost of the inventory and overproduction problems it creates.
