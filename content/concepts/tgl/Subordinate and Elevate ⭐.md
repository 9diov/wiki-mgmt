---
concept-type: "[[Framework]]"
description: The two actions that follow from identifying the constraint — arrange everything else to serve the constraint, then increase the constraint's capacity.
related-concepts:
  - "[[The Constraint ⭐]]"
  - "[[Dependent Events and Statistical Fluctuations]]"
  - "[[Balanced Plant Fallacy]]"
sources:
  - "[[21-Chapter_15|Chapter 15 — The Boy Scout Hike Resolution]]"
---

# Subordinate and Elevate

Once the constraint is identified, two actions determine whether the system improves.

## Subordinate Everything to the Constraint

Arrange all non-constraint resources to serve the constraint's needs — not their own utilization targets.

In the hike: move Herbie to the front. Now the fast boys behind him have spare capacity. When any fluctuation occurs, that spare capacity closes the gap. The system's pace is still Herbie's pace, but now it is the actual output rate — not the cause of accumulating inventory.

Before subordination, the fast boys at the front were running away from Herbie, maximizing their own efficiency while the column exploded behind them. After: everyone walks at Herbie's rate. Individual utilization drops for the fast boys. System throughput increases.

The critical implication: **non-constraints should run below their maximum capacity.** Idle time at a non-constraint is not waste — it is the slack that makes the system resilient to fluctuations.

## Elevate the Constraint

Once the system is subordinated to the constraint, increasing the constraint's capacity directly increases system throughput.

In [[Boy Scout Hike ⭐]]: redistribute Herbie's pack. He's been carrying a skillet, canned food, a shovel — weight that slowed him and, through him, slowed everyone. Taking the load off Herbie doubles the troop's effective speed.

Adding capacity to a non-constraint does nothing. Adding weight to Andy (the fastest boy) makes no difference to the troop's speed — Andy was not limiting the system. Only elevating the constraint — the actual limit — changes the system output.

Elevation can mean:
- Removing load from the constraint (as with Herbie's pack)
- Adding resources to the constraint step
- Reducing waste or downtime at the constraint
- Redesigning the work the constraint must perform

## The Sequence Matters

Subordination before elevation. If non-constraints are not subordinated first, elevating the constraint may not help — the constraint's increased output is still fed by an unmanaged, fluctuating system. The two moves work together.

## The Management Translation

| Hike | Plant |
|---|---|
| Herbie at the back | Constraint buried mid-process, fast steps piling inventory ahead of it |
| Fastest at front | High-utilization non-constraints racing ahead, building WIP |
| Move Herbie to front | Schedule to the constraint; release work at the constraint's rate |
| Redistribute Herbie's pack | Add hours, reduce setups, offload work at the bottleneck |
| Manager carries Herbie's heaviest items | Management absorbs the constraint's hardest burdens |
