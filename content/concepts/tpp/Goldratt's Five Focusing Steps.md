---
concept-type: "[[Framework]]"
description: Goldratt's five-step cycle for managing organizational constraints — identify, exploit, subordinate, elevate, and repeat — introduced by Erik as the theoretical basis for managing Brent and controlling work release in IT Operations.
related-concepts:
  - "[[The Brent Problem ⭐]]"
  - "[[Work in Process (WIP) ⭐]]"
  - "[[The Four Types of Work ⭐]]"
  - "[[The Three Ways ⭐]]"
sources:
  - "[[20-Chapter_15_•_Wednesday,_September_17|Chapter 15 — Wednesday, September 17]]"
  - "[[25-Chapter_20_•_Friday,_September_26|Chapter 20 — Friday, September 26]]"
aliases:
  - Five Focusing Steps
  - Theory of Constraints
  - TOC
---

# Goldratt's Five Focusing Steps

Erik introduces the Five Focusing Steps in Chapter 15 as the framework from Goldratt's *The Goal* that underlies constraint management. He walks Bill through the first three steps as applied to IT Operations, with Brent as the identified constraint.

## The Steps

**Step 1 — Identify the constraint.**
Determine the single resource that limits the throughput of the entire system. Every improvement not made at the constraint is an illusion — it adds capacity somewhere that isn't the bottleneck, which doesn't increase flow. The constraint must be correctly identified before any other step is meaningful. Erik challenges Bill to keep verifying that Brent is genuinely the organizational constraint, because being wrong about this makes everything else pointless.

**Step 2 — Exploit the constraint.**
The constraint must never wait. It should never be idle, never be blocked by a missing dependency, and always be working on the highest-priority commitment the organization has made. Waste at the constraint is doubly damaging: an hour lost at the constraint is an hour lost to the entire system, not just that workstation. Bill has made progress here — reducing Brent's exposure to unplanned work, protecting him from direct-call escalations, giving him a week off.

**Step 3 — Subordinate everything else to the constraint.**
All other resources must be managed to support the constraint's tempo, not their own. The Drum-Buffer-Rope mechanism implements this: the constraint sets the drum (the production rhythm); a buffer of work is kept in front of it so it never starves; the rope controls how fast new work enters the system (tied to the constraint's rate, not the first station's availability). Applied to IT: work should be released into the change process only at the rate Brent can absorb the Brent-dependent portion of it.

**Step 4 — Elevate the constraint.**
Once the constraint is fully exploited and everything is subordinated to it, if throughput is still insufficient, add capacity at the constraint. This is the step most organizations jump to first (hire more Brents, buy faster hardware) — and it is Step 4, not Step 1. Elevating the constraint before exploiting it wastes the investment, because the constraint was not yet being used at full capacity.

**Step 5 — Repeat.**
Once the original constraint is broken, a new one will emerge. Return to Step 1. The constraint shifts — if Brent's bottleneck is broken, the next constraint might be the CAB process, or the test environment, or something else entirely. The cycle doesn't end; it restarts at a higher performance level each time.

## Application in the Novel

Erik tells Bill he is ready for Step 3 in Chapter 15. Bill has done Step 1 (identified Brent as constraint) and made progress on Step 2 (reduced unplanned interruptions, protected Brent's time). His homework: figure out how to throttle work release to Brent's actual capacity — the IT equivalent of Alex Rogo moving Herbie to the front of the Boy Scout line and releasing work at the pace of the slowest scout.

The explicit reference to *The Goal* places the novel in direct conversation with Goldratt. Erik names Alex Rogo and Herbie by reference, connects Drum-Buffer-Rope to the change board as kanban, and cites David Anderson's adaptation of these principles to software development. The Five Focusing Steps are not a metaphor in the novel — they are the operating manual.

## Step 4 in Practice: The Monitoring Project (Chapter 20)

Erik identifies the monitoring project — which detects unauthorized changes and prevents outages — as a Step 4 action. It doesn't require Brent, and it actively reduces future demand on Brent by preventing the outages that currently consume him.

Erik connects Step 4 to Total Productive Maintenance (TPM): preventive maintenance work that increases machine availability. The IT equivalent is any project that reduces unplanned work generation — proactive monitoring, alerting, automated testing, runbook documentation. These projects look like overhead until you account for the unplanned work they prevent.

## The Work Center Model (Chapter 20)

Erik also corrects a conceptual error in Chapter 20: Brent is not a work center. A work center consists of four elements — machine, man, method, measure. Brent is the "man" component of multiple work centers that have no documented method. The constraint is not Brent himself; it is the number of work centers whose method exists only in Brent's head.

This reframing has a direct implication: the way to elevate the constraint is to document those methods (creating reproducible steps others can execute) and to build tooling that automates them (removing human dependency entirely). Hiring more Brents does nothing unless the methods are documented — new engineers will simply stand around unable to operate work centers they don't have procedures for.

## Why Step Order Matters

The steps are ordered deliberately. Organizations almost universally skip to Step 4 (elevate — add resources) when facing capacity problems, because adding people or machines is visible and satisfying. But if the constraint is not exploited first, the added resources flow into non-constraint work. If everything is not subordinated first, the constraint will be starved while non-constraint resources produce WIP that piles up in front of it — exactly what the CAB was doing before Brent-dependent changes were flagged.

Erik's formulation: *"Any improvement not made at the constraint is just an illusion."*
