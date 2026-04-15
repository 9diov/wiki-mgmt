---
related-concepts:
  - "[[Wait Time and Utilization]]"
  - "[[Work in Process (WIP) ⭐]]"
  - "[[The Brent Problem ⭐]]"
sources:
  - "[[25-Chapter_20_•_Friday,_September_26|Chapter 20 — Friday, September 26]]"
---

# The Wait Time Formula

## The Setup

On the MRP-8 plant floor, Erik directs Bill's attention away from the work centers and toward the space *between* them — the queues where parts sit waiting to move to the next operation.

He introduces the formula:

> *"The wait time for a given resource is the percentage that resource is busy, divided by the percentage that resource is idle."*

He walks through the numbers:

- At **50% utilization**: wait time = 50/50 = 1 unit
- At **90% utilization**: wait time = 90/10 = 9 units
- At **99% utilization**: wait time = 99/1 = 99 units

*"When a resource is ninety-nine percent utilized, you have to wait ninety-nine times as long as if that resource is fifty percent utilized."*

Erik tells Bill that a historical investigation at MRP-8 revealed that for most parts, the "touch time" — time actually being worked on — was a tiny fraction of total process time. The rest was queue time, sitting in front of busy work centers.

## What It Illustrates

**[[Wait Time and Utilization]]** — The formula makes the cost of high utilization concrete and quantitative. A resource that looks 80% more productive than a 50%-utilized resource (90% vs. 50%) is actually producing wait times 9 times longer. Organizations that optimize for utilization are optimizing for the wrong variable — they're maximizing local efficiency while creating system-level delays.

**[[The Brent Problem ⭐]]** — Brent is the canonical example of a resource at near-100% utilization. He is never idle. He is always working something. And the consequence — visible in the 942 pending change cards and the 60% change incompletion rate — is that work waiting for Brent waits an order of magnitude longer than work routed around him. The formula explains why adding Brent to more things doesn't help: at full utilization, adding more demand increases wait times exponentially without increasing throughput.

**[[Work in Process (WIP) ⭐]]** — WIP accumulates precisely at high-utilization resources. The queue in front of a 99%-utilized work center grows faster than the work center can drain it. Making those queues visible — showing how long work sits at each handoff — is the diagnostic that reveals where flow is actually breaking down. The impressive number on a utilization dashboard is often the exact location where work is piling up and dying.
