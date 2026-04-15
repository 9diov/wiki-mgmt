---
concept-type: "[[Practice]]"
description: The discipline of maintaining machines to prevent breakdown before it occurs — the structural necessity created by eliminating inventory buffers in a JIT system.
related-concepts:
  - "[[Just-in-Time ⭐]]"
  - "[[Takt Time ⭐]]"
  - "[[Autonomation (Jidoka) ⭐]]"
  - "[[Standard Work]]"
sources:
  - "[[09-Chapter_5__The_True_Intention_of_the_Ford_System|Chapter 5 — The True Intention of the Ford System]]"
aliases:
  - TPM
  - Total Productive Maintenance
---

# Preventive Maintenance

In a traditional production system, inventory buffers absorb machine downtime. If a machine breaks down, work-in-process in front of it depletes slowly while repairs are made; downstream processes may not even notice for hours or days. The buffer absorbs the shock.

Just-in-time eliminates these buffers. When a machine breaks down in a JIT system, the downstream process runs out of parts almost immediately — the line stops. The same property that makes JIT efficient (no excess inventory) makes it acutely sensitive to machine reliability.

This creates a direct logical requirement: **if buffers are removed, machine reliability must be maintained at a level that makes buffers unnecessary**. Prevention replaces protection.

## Ohno's Formulation

*"If we think to keep inventory in anticipation of machine problems, why not consider preventing trouble before it occurs?"*

This is the same inversion logic that runs through TPS: rather than designing systems to tolerate problems, design systems that prevent them. Inventory-as-buffer tolerates breakdowns. Preventive maintenance eliminates them.

## What Preventive Maintenance Requires

**Regular inspection and servicing** — machines are serviced on a schedule based on expected wear, not in response to failure. Oil changes, filter replacements, bearing checks, and calibration happen before problems appear, not after.

**Operator ownership** — in TPS, the operator of a machine is responsible for its basic maintenance: cleaning, checking, detecting early signs of wear or abnormality. This is consistent with autonomation: the operator who monitors the machine also maintains it. Deterioration that operators can detect early is far cheaper to correct than deterioration discovered at breakdown.

**Mean-time-between-failures tracking** — recording when and why machines fail creates the data needed to improve the maintenance schedule. If a bearing consistently fails after 2,000 hours, replace it at 1,800.

## The Operable Rate Connection

Ohno's concept of **operable rate** (the percentage of time a machine is functional when needed) directly depends on preventive maintenance. A machine with 100% operable rate is available every time takt time calls for it. Achieving this requires the discipline of maintenance before failure, not after.

By contrast, **operating rate** (how much of the time the machine actually runs) is deliberately kept below 100% — the machine runs only at the rate demand requires. The goal is high operable rate at demand-appropriate operating rate: always ready, never running unnecessarily.

## Prevention vs. Repair Economics

The cost comparison is asymmetric. Preventive maintenance has a known, scheduled cost. Breakdown maintenance has an unpredictable cost that includes: repair labor, parts, lost production during downtime, expediting to recover lost output, and — in a JIT system — the cascading downstream stoppages caused by the absence of buffer inventory. In a high-volume JIT system, an hour of unplanned downtime costs far more than a day of scheduled maintenance.

## The Ford Parallel

Ford applied the same logic to human health: if perfect food maintains health, build the system around perfect food rather than better hospitals. Ohno draws this analogy explicitly — *"Toyota's strength does not come from its healing processes — it comes from preventive maintenance."* A strong constitution (machine reliability built in) is more valuable than excellent emergency response.
