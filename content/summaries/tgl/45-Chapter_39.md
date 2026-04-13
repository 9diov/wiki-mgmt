---
related-concepts:
  - "[[Drum-Buffer-Rope]]"
  - "[[The Constraint ⭐]]"
  - "[[Activation vs Utilization]]"
---

# Chapter 39

## What Happens

**The plant breaks down.** The French deal generated a surge of additional orders. Within weeks: 12 work centers on unplanned overtime, orders starting to miss due dates, Ralph projecting 20% late shipments and over a million dollars in delayed throughput by month end. Stacey and Bob have been expediting for days with no improvement.

**Root cause.** The bottlenecks are not overloaded — but they're being **starved**. Work arrives in waves. When upstream resources hit a problem, the bottleneck's buffer depletes. When the problem clears, upstream resources must simultaneously supply current demand AND rebuild the buffer. This requires more capacity than the bottleneck itself.

Bob names the principle: *"Non-bottlenecks must have more capacity than the bottleneck."* Not because they're poorly designed — it's a structural requirement. If upstream non-bottlenecks have no spare capacity, they can't recover from Murphy without starving the constraint.

The new orders didn't create new bottlenecks — they reduced the spare capacity of non-bottlenecks to a point where recovery from statistical fluctuations was no longer possible. And the buffer in front of the bottleneck wasn't increased to compensate. The inventory-capacity trade-off: more buffer → less spare capacity needed upstream; less buffer → more spare capacity required.

**Bob's fix.** He directs Ralph to identify orders with short-delivery promises and keep them at one-week material release; extend all others to two weeks. He puts the entire plant on a weekend shift to rebuild buffers. He notifies sales to stop promising anything under four weeks for now.

**The consequence.** All three TOC measurements move in the wrong direction simultaneously: throughput down (delayed sales campaign), operating expense up (weekend overtime), inventory up (larger buffers). Rogo is frustrated — the plant is moving backward and it was his decision to accept the French order that triggered it.

His conclusion: *"I'm driving looking only in the rear-view mirror, and then, when it's almost too late, we make last-minute corrections. It's not good enough."*

## Management Observations

- **Non-bottleneck spare capacity is not waste — it's shock absorption.** The plant learned this once (Chapter 20: idle non-bottleneck time is correct). The lesson reappears in a more complex form: when you add orders, you implicitly reduce non-bottleneck spare capacity. The buffer must be increased to compensate, or instability follows.
- **The inventory-capacity trade-off is explicit.** More inventory in front of the bottleneck means upstream resources have more time to recover from disruptions — so they need less excess capacity. This is a design choice, not an accident. Failing to make it consciously creates the conditions for wandering bottlenecks.
- **All three TOC measurements deteriorating simultaneously is a diagnostic signal.** When T is down, I is up, and OE is up at the same time, the system is not just inefficient — it's in crisis. The five-step process should have flagged the capacity-inventory trade-off before this happened, not after.
