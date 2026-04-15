---
concept-type: "[[Framework]]"
description: The operational pace of production — available time divided by required quantity — setting the rate at which every process must produce to meet demand exactly.
related-concepts:
  - "[[Standard Work]]"
  - "[[Production Leveling (Heijunka)]]"
  - "[[Just-in-Time ⭐]]"
  - "[[Seven Wastes (Muda) ⭐]]"
sources:
  - "[[07-Chapter_3__Further_Development|Chapter 3 — Further Development]]"
aliases:
  - Tact time
---

# Takt Time

Takt time is the heartbeat of a production system. It is the rate at which products must be completed to exactly meet customer demand — no faster (which creates inventory), no slower (which creates shortfall).

**Formula:** Takt time = available operating time ÷ required daily quantity

For example: 480 minutes of operating time, 240 units required → takt time = 2 minutes per unit. Every process in the production system is designed to complete one unit every 2 minutes.

## Why It Governs Standard Work

Takt time is the yardstick for standard work. Every standard work sequence is designed to fit within one takt period. If a worker cannot complete the defined sequence within takt time, the process has an unresolved problem — insufficient manpower, excessive motion, or a wasteful step that needs elimination.

Improving a process means reducing the work content until it fits comfortably within takt. When multiple workers share a line, each worker's cycle time is tuned so that the combined output exactly matches takt.

## Operating Rate vs. Operable Rate

Ohno draws a sharp distinction between two measures of machine utilization:

**Operating rate** — the percentage of time a machine actually runs (production output ÷ full-capacity output). This is often optimized in traditional manufacturing: keep machines running to spread fixed costs across more units.

**Operable rate** — the reliability of a machine to run when it is needed. A machine that is always available when required has a 100% operable rate, regardless of how often it runs.

In TPS, the targets are:
- Operable rate → 100% (through maintenance and setup reduction)
- Operating rate → determined by takt time (run only as fast as needed)

Running a machine at 100% operating rate regardless of demand produces overproduction. A machine that runs at 60% operating rate but is always ready when needed (100% operable rate) is a better asset. This is the tortoise vs. the hare: slow and consistent beats fast and intermittent.

## Takt Time and Manpower

Takt time directly determines required headcount. If takt time is 2 minutes and one worker's cycle time (after waste elimination) is 2 minutes, one worker is needed. If improvements reduce the worker's cycle time to 1.5 minutes, the worker has 30 seconds of idle time — which is the signal to re-balance the line, not to produce faster.

When demand drops (takt time increases), fewer workers are needed. When demand rises (takt time decreases), more workers are needed. The line flexes to match demand — this is "using fewer workers" rather than "labor saving."

## Takt Time Is Not a Speed Target

A common misapplication: treating takt time as a minimum speed and trying to run faster. Running faster than takt time produces inventory, not throughput. The goal is to run exactly at takt time, consistently, with every process synchronized.

This is the tortoise: not the fastest runner, but the one that finishes on time every time.
