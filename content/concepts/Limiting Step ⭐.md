---
concept-type: "[[Framework]]"
description: "The single step in a production flow that determines the pace of everything else, around which all other steps must be planned."
related-concepts:
  - "[[Production Operations]]"
  - "[[Production Tradeoffs]]"
  - "[[Lowest Value Stage]]"
sources:
  - "[[09-Chapter_1__The_Basics_of_Production__Delivering_a_Breakfast_(or_a_College_Graduate,_or_a_Compiler,_or_a_Convicted_Criminal…)|Chapter 1 — The Basics of Production]]"
aliases:
  - Bottleneck
---

# Limiting Step

The single step in a production flow that determines the pace of everything else—typically the longest, most expensive, most sensitive, or hardest-to-redo step.

## Principle
Design the entire production flow around the limiting step. Time all other steps backward from it (see: [Time Offsets](#)). Do not let a cheaper or easier step become the bottleneck if the actual limiting step is sitting idle.

## Why It Matters
If you ignore the limiting step, you optimize the wrong thing. You waste resources upstream while the real constraint goes underutilized. The shape of the whole operation follows from this one choice.

## Examples
- **[[Three Minute Breakfast ⭐]]** — the egg (3 min) is the limiting step; the entire flow is designed around it
- **[[Intel College Recruiting]]** — the plant visit (expensive, time-intensive) is the limiting step; phone screens protect it by raising the acceptance-per-visit ratio
- **[[Criminal Justice System]]** — conviction, not jail-cell availability, is the true limiting step; constraining on cells wastes the million-dollar investment already made per conviction

## Implication
When a bottleneck shifts (e.g., the toaster line becomes congested), the limiting step changes and the entire production plan must be reworked around the new constraint.

*Source: Chapter 1*
