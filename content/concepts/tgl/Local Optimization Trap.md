---
concept-type: "[[Framework]]"
description: Improving a local metric (efficiency, utilization, cost per part) can harm overall system performance by generating inventory and obscuring real constraints.
related-concepts:
  - "[[Productivity]]"
  - "[[The Goal]]"
sources:
  - "[[12-Chapter_4|Chapter 4 — The O'Hare Encounter]]"
---

# Local Optimization Trap

When a plant optimizes individual workstations or departments in isolation, it can simultaneously *improve* local metrics and *worsen* system-level performance. The trap is that the metrics look good while the system deteriorates.

## The Mechanism

The logic of local optimization: to reduce cost per part, run every machine as much as possible. To maintain high efficiency, never let a resource sit idle. To justify capital investment in robots, maximize their utilization.

Each of these is locally rational. Together, they produce:
- Excess work-in-process inventory (everything upstream of a constraint piles up)
- Late shipments (the constraint is overwhelmed; everything waits)
- High reported efficiency alongside poor financial performance

## Jonah's Diagnostic

Jonah identifies the trap without seeing the plant by asking three questions:

| Question | If the answer is "no"... |
|---|---|
| Are you shipping more products per day? | Local improvement didn't increase throughput |
| Did you reduce headcount? | Local improvement didn't reduce operating expense |
| Did inventories go down? | Local improvement didn't free up working capital |

If all three answers are "no," the improvement was local only — it produced no system-level benefit regardless of how the efficiency numbers look.

## Why It Persists

Managers are measured on local metrics. A department head is rewarded for high utilization and low cost per part; they are not penalized when their output creates a bottleneck two steps downstream. The incentive structure reinforces the trap.

## Relationship to Constraints

The local optimization trap is the setup for the Theory of Constraints: once you understand that local efficiency is not the goal, the next question is what *does* govern system performance — which Goldratt answers with the concept of the constraint (bottleneck).

*Source: Chapter 4*
