---
related-concepts:
  - "[[The Constraint ⭐]]"
  - "[[Local Optimization Trap (synth)]]"
  - "[[Balance Flow Not Capacity]]"
sources:
  - "[[24-Chapter_18|Chapter 18 — Finding the Bottleneck]]"
---

# NCX-10 Machine Purchase

## The Setup

Rogo's plant replaced three types of older machines with a single new CNC machine, the NCX-10. The economics looked compelling:

**Old process (10 machines total):**
- 2 machines of type A: 2 minutes per part
- 5 machines of type B: 8 minutes per part
- 3 machines of type C: 4 minutes per part
- Total: 14 minutes per part, across 10 machines, each requiring a dedicated machinist

**New process:**
- 1 NCX-10: 10 minutes per part
- Requires only 2 setup operators

The NCX-10 saved 4 minutes per part and eliminated the labor cost of 8 machinists. By every unit-cost and efficiency metric, it was a clear improvement. Division praised it as a productivity success.

Two years later, the NCX-10 is the plant's primary bottleneck — weeks of work-in-process stacked in front of it, expeditors permanently camped nearby, the entire plant's throughput constrained by a single machine.

## What It Illustrates

**[[The Constraint ⭐]]** — The NCX-10 became the bottleneck not despite being the plant's best machine, but partly because of it. The old configuration had 10 machines processing these parts in parallel; the new one had 1. Even though each part moves through faster, total throughput capacity collapsed. One machine running at 10 minutes per part cannot match the combined output of 10 machines running at 14 minutes per part. Efficiency reports showed the NCX-10 as a star performer. The inventory pile in front of it showed the truth.

**[[Local Optimization Trap (synth)]]** — The purchase decision was evaluated on unit cost and per-part processing time — local metrics. The system metric that mattered was total throughput capacity for this class of parts. Optimizing the wrong variable turned a cost-reduction initiative into a capacity crisis. The plant saved money on machinists and created a bottleneck that constrained the entire operation.

**[[Balance Flow Not Capacity]]** — The NCX-10 decision implicitly assumed that faster-per-part equals more flow. It doesn't — flow depends on total capacity relative to demand, not speed per unit. A single fast machine can produce less flow than multiple slower ones. The right question before the purchase was not "what is the cost per part?" but "will this change the rate at which we can ship?"
