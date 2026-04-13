---
related-concepts:
  - "[[Exploit the Bottleneck ⭐]]"
  - "[[Subordinate and Elevate ⭐]]"
  - "[[The Constraint ⭐]]"
  - "[[Local Optimization Trap]]"
---

# Chapter 21

## What Happens

Rogo calls Julie back late that night and asks her out on a date. She says yes — Saturday, 7:30.

**Priority system implementation:** Ralph and Stacey worked through the night. 67 overdue orders ranked by days late, worst at 58 days. 90% involve parts through one or both bottlenecks. Supervisors Ted (heat-treat) and Mario (NCX-10) are briefed: work down the list from most overdue, in sequence, nothing else.

By early afternoon the NCX-10 is sitting idle. Investigation reveals: operators finished the first two batches and couldn't find materials for the third, so they stopped entirely rather than skipping to the fourth. The missing parts were sitting at Otto's lathe area — held up because Otto was running a long, unimportant batch and had no idea the parts were urgent. He was staying busy. Nobody had told him those parts needed to reach the NCX-10.

Rogo's diagnosis:

> *"The non-bottleneck was blocking bottleneck-bound parts without knowing it — because we gave no system for people to tell the difference between an important batch and an unimportant one."*

**The red/green tag system:** Bob Donovan designs a plant-wide signaling mechanism announced at a 15-minute meeting with all three shifts:

- **Red tag** = parts destined for a bottleneck operation. First priority everywhere. If you receive red-tagged parts, drop what you're doing (within 30 minutes) and work on them. If you're mid-setup, break the setup immediately.
- **Green tag** = everything else. Work on green only when no red parts are in queue.
- **Numbers on each tag** = sequence within the same color. Always take the lowest number first.

The hourglass analogy is used to explain why the bottleneck governs everything. A plant newsletter will replace the old employee paper to track progress.

By end of week: the union agrees not to challenge the new break policy for bottleneck operators.

Saturday evening: Rogo shows up at the Barnett house with flowers and new clothes. Julie opens the door.

## The Implementation Gap

The chapter surfaces a problem that precedes all complex system changes: rules given to supervisors do not automatically translate into correct behavior throughout the plant. Mario followed instructions literally — work only what's on the list, in order — and the bottleneck went idle. Otto followed his normal incentive — stay busy, finish long runs — and blocked critical parts. Both were acting rationally within their local information.

The tag system solves this not by improving supervision but by making priority information visible at every workstation. A non-bottleneck operator doesn't need to understand bottleneck theory to act correctly — they just need to know whether the part in front of them is red or green.

## Management Observations

- **Subordinating non-bottlenecks requires a communication system, not just a policy.** Telling supervisors to prioritize bottleneck parts doesn't work unless every worker who handles those parts can identify them on sight.
- **Idle bottlenecks caused by non-bottleneck delays are the same problem as idle bottlenecks from breaks.** The mechanism is different but the cost is the same: $2,188/hour of lost throughput.
- **Breaking a setup on a non-bottleneck to serve red-tagged parts is always the right decision.** The setup cost at a non-bottleneck is zero in throughput terms; the cost of the bottleneck waiting is not.
- **Transparency about the crisis motivates rather than demoralizes.** Rogo holds meetings for all three shifts, explains the situation plainly, and asks for cooperation. The union, once given the full picture, agrees to the new break policy the same day.
