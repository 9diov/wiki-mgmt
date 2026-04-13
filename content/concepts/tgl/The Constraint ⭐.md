---
concept-type: "[[Framework]]"
description: The single resource or step that limits the throughput of the entire system — the slowest point in a dependent sequence.
related-concepts:
  - "[[Dependent Events and Statistical Fluctuations]]"
  - "[[Balanced Plant Fallacy]]"
  - "[[Goal Formulation]]"
  - "[[Throughput, Inventory, and Operating Expense ⭐]]"
  - "[[Subordinate and Elevate ⭐]]"
  - "[[Balance Flow Not Capacity]]"
sources:
  - "[[19-Chapter_13|Chapter 13 — The Boy Scout Hike]]"
  - "[[21-Chapter_15|Chapter 15 — The Boy Scout Hike Resolution]]"
  - "[[24-Chapter_18|Chapter 18 — Finding the Bottleneck]]"
aliases:
  - Bottleneck
  - Constraint
---

# The Constraint

In any system of dependent events, one step limits the output of the entire system. This is the constraint — also called the bottleneck. Its capacity sets the maximum throughput of the whole, regardless of how fast every other step can run.

## The Hike Demonstration

In Chapter 13, Herbie is the constraint. He is the slowest hiker in the column. Every boy behind him is backed up; every boy in front of him walks away into a growing gap. The column's effective speed — its throughput — is not Ron's pace at the front, not the average pace of all boys, but Herbie's pace at the slowest point.

No amount of effort by the faster boys can increase the column's throughput past Herbie's rate. They can sprint to close gaps, but they hit Herbie's back and slow down again. Their excess speed is wasted — absorbed as inventory (trail between Ron and me) rather than converted into throughput.

## The Plant Equivalent

Every production system has a constraint: the one machine, worker, or step that limits how much can be shipped. All other resources in the system have more capacity than the constraint — they are **non-constraints**.

The critical implication:

- **An hour lost at the constraint is an hour lost for the entire system.** There is no way to recover it downstream.
- **An hour saved at a non-constraint saves nothing.** The non-constraint wasn't limiting throughput anyway; saving time there just creates idle capacity or more inventory piling up in front of the constraint.

## What the Constraint Governs

The constraint determines:
- **System throughput** — you can never ship faster than the constraint processes
- **Required inventory** — work piles up in front of the constraint; how much depends on how protected it is
- **Effective operating expense** — if the constraint sits idle, operating expense produces zero throughput during that time

This is why maximizing utilization of *every* resource (the [[Balanced Plant Fallacy]]) is wrong: only maximizing utilization of the *constraint* matters. Non-constraints should be managed to *feed the constraint*, not to hit their own utilization targets.

## Formal Definition (Jonah, Chapter 18)

> A **bottleneck** is any resource whose capacity is equal to or less than the demand placed upon it. A **non-bottleneck** is any resource whose capacity is greater than the demand placed on it.

The distinction matters because bottlenecks and non-bottlenecks must be managed completely differently. Non-bottlenecks should *not* be maximized — their excess capacity is the buffer that protects the bottleneck from fluctuations.

## Finding the Constraint

Data systems are often unreliable guides — routings go stale, run-times go uncorrected, equipment gets sold without updating the records. Faster methods:

- **Ask the expeditors.** The parts they're always chasing pass through the bottleneck. The departments where they spend most of their time are the candidates.
- **Follow the inventory.** The bottleneck will have the largest pile of work-in-process in front of it — the plant equivalent of the gap behind the slowest hiker.
- **Check what efficiency reports praise.** The most "efficient" machine in the plant may be the bottleneck — if it replaced many older machines, its per-unit speed may be high while total throughput capacity is lower than what it replaced.

*Sources: Chapters 13, 15, 18*
