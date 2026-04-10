---
related-concepts:
  - "[[Limiting Step ⭐]]"
  - "[[Production Operations]]"
  - "[[Production Tradeoffs]]"
  - "[[Quality Assurance]]"
  - "[[Lowest Value Stage]]"
sources:
  - "[[09-Chapter_1__The_Basics_of_Production__Delivering_a_Breakfast_(or_a_College_Graduate,_or_a_Compiler,_or_a_Convicted_Criminal…)|Chapter 1 — The Basics of Production]]"
---

# The Three-Minute Breakfast

A waiter must serve a soft-boiled egg, buttered toast, and coffee—all fresh and hot—simultaneously.

## The Setup
- Egg: 3 minutes to boil (longest step, most important to the customer)
- Toast: ~1 minute
- Coffee: already brewed

## What It Illustrates

**Limiting step**: The egg governs the entire flow. Plan backwards from when the egg is done—offset toast and coffee starts accordingly.

**Time offsets**: Each component starts at a different time so they all finish together. The offset for each is calculated by working backward from delivery.

**Complications—the toaster queue**: If waiters must share a toaster, the toaster queue can become the new limiting step, even though the egg still determines quality. The entire production plan must be reworked around the new constraint.

**Trade-off resolution**: When toaster capacity is the bottleneck, options are: hire specialists (overhead), borrow a colleague's help (unpredictable), add a toaster (capital cost), or build a toast inventory (waste). Each costs money; find the most cost-effective combination.

**Continuous operations**: Scaling to a high-volume factory means buying a continuous egg-boiler and matching toaster. Cost drops and consistency improves, but flexibility is lost—you can no longer make a 4-minute egg on request.

**In-process inspection**: Insert a thermometer in the boiler water and attach an alarm. Non-destructive, continuous, immediate warning. Better than cracking open an egg to test it (destroys the product) or waiting for a customer complaint (too late).

**Incoming inspection + inventory**: Inspect eggs on receipt; reject cracked or rotten ones before they enter production. Keep one day's inventory to avoid a shutdown if the egg supplier delivers bad product.

*Concepts: [Limiting Step](../concepts/limiting-step.md), [Production Operations](../concepts/production-operations.md), [Production Trade-offs](../concepts/production-tradeoffs.md), [Quality Assurance](../concepts/quality-assurance.md)*
*Source: Chapter 1*
