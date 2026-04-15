---
concept-type: "[[Framework]]"
description: The queueing theory principle that wait time grows exponentially with utilization — a resource at 99% utilization produces wait times 99x longer than one at 50% — making high utilization the enemy of flow rather than a measure of efficiency.
related-concepts:
  - "[[Work in Process (WIP) ⭐]]"
  - "[[The Brent Problem ⭐]]"
  - "[[Goldratt's Five Focusing Steps]]"
  - "[[The Three Ways ⭐]]"
sources:
  - "[[25-Chapter_20_•_Friday,_September_26|Chapter 20 — Friday, September 26]]"
---

# Wait Time and Utilization

Erik introduces the wait time formula during the second MRP-8 plant floor visit in Chapter 20, as the quantitative basis for managing handoffs between work centers.

## The Formula

> Wait time = % busy / % idle

| Utilization | Wait time (relative) |
|---|---|
| 50% | 50/50 = 1 unit |
| 90% | 90/10 = 9 units |
| 99% | 99/1 = 99 units |

A resource running at 90% utilization does not produce 80% more work than one at 50% — it produces wait times nine times longer. A resource at 99% utilization produces wait times 99 times longer than the same resource at 50%.

## What This Means for IT Management

The universal instinct in resource management is to maximize utilization — idle engineers look wasteful; a server running at 30% capacity looks overprovisioned. The formula inverts this: high utilization is not efficiency, it is latency. Work queued behind a 99%-utilized resource waits nearly 100 times longer than work queued behind a 50%-utilized resource, regardless of how fast the resource processes each individual task.

This is why:
- Brent at 99% utilization creates waiting times that cascade through every project in his path
- A change management system at 100% throughput capacity creates a single denied change that delays an entire release
- A deployment pipeline that is "always busy" is slower in total cycle time than one with deliberate slack

The practical implication: the slack that looks wasteful at the resource level is the slack that makes flow possible at the system level. Organizations that measure efficiency by utilization will always sub-optimize flow, because they will remove the margins that prevent queuing from compounding.

## Application to Handoffs

Erik introduces the formula specifically in the context of handoffs between work centers. Parts at MRP-8 were spending a tiny fraction of their total process time being actively worked on; the rest was queue time — waiting for access to the next work center. The expediters had to physically search through inventory to find parts and push them forward.

In IT, the equivalent is work sitting in someone's queue: a change card waiting for Brent's availability, a deployment waiting for the test environment to free up, a code review request sitting unacknowledged. Each handoff point is a potential queue. At high utilization, each queue grows exponentially. Making wait times visible — showing engineers and managers how long work is sitting at each handoff — is the diagnostic that reveals where the real delays are.

## Relation to WIP

The wait time formula and WIP accumulation are two descriptions of the same phenomenon. High WIP is the symptom; high utilization at one or more resources is usually the cause. Reducing WIP at the constraint — by either reducing work input or increasing constraint capacity — reduces utilization, which reduces wait times, which improves flow across the entire system.
