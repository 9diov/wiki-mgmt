---
related-concepts:
  - "[[Exploit the Bottleneck ⭐]]"
  - "[[Subordinate and Elevate ⭐]]"
  - "[[Local Optimization Trap (synth)]]"
  - "[[The Constraint]]"
---

# Chapter 23

## What Happens

Julie and Rogo have been dating for a week — movies, dinner, drives. No talk of divorce or marriage. Strange limbo, but easy.

**Heat-treat is losing hours no one was tracking.** Ralph, investigating why his throughput projections were 50% off (should have shipped 18–20 orders, only shipped 12), stakes out the heat-treat furnaces. He finds a batch sitting 2.5 hours past completion before anyone unloads it — workers were loaned out to other areas and nobody called them back. Hourly people confirm this is routine. Five hours of furnace time, in effect, wasted.

**NCX-10 similarly idle.** Bob's own investigation finds the machine sitting 20–40 minutes between jobs — not during breaks (those are now covered), but because setup people are assigned across multiple machines and don't return to the NCX-10 immediately when it stops.

**Fix: dedicated bottleneck crews.** Bob brings four recommendations to the staff meeting:
1. Dedicated machinist + helper on the NCX-10, all three shifts
2. Dedicated foreman + two workers at heat-treat furnaces, all three shifts — ready to load/unload immediately when a cycle completes
3. Activate the Zmegma and two other old machines for one shift per day → +18% capacity on NCX-10-type parts
4. Send surplus heat-treat parts to an outside vendor

People are pulled from non-bottleneck work centers, which by definition have excess capacity. Lou approves: the cost is justified if it increases throughput.

**Mike Haley, heat-treat foreman on third shift**, has been pushing 10% more parts through than other shifts. Rogo goes to see what he's doing. Mike pre-sorts incoming parts by temperature cycle before loading, combines compatible batches to fill the furnace completely, and has a proposal for interchangeable furnace tables (loaded via forklift) that would cut load-change time from an hour to minutes. Rogo pulls him to day shift to work with an industrial engineer to formalize the procedures for all shifts.

**The self-inflicted heat-treat load.** Bob discovers that three classes of parts currently requiring heat-treat only need it because of an internal decision made five years ago: engineers "improved" several non-bottleneck machining centers by increasing cutting speed (deeper bite per pass). The faster cutting made the metal brittle, which required heat-treating. Those non-bottleneck machines have excess capacity — they can run slower and still meet demand. Reverting to the original slower process removes the brittleness and eliminates heat-treat on ~20% of current volume. No engineering change order required because the original slow-process specification is still on the books.

Rogo's reflection: *"We're going to reduce the efficiency of some operations and make the entire plant more productive. They'd never believe it on the fifteenth floor."*

## Management Observations

- **Untracked idle time at the bottleneck is as expensive as tracked idle time.** Break coverage was implemented and counted; post-cycle delays were invisible. Ralph's field observation found what the data system missed.
- **Dedicated bottleneck resources look inefficient on paper.** Workers standing by at a furnace between cycles appear idle. At $2,188/hour true bottleneck cost, they are the cheapest insurance in the plant.
- **Improving non-bottleneck speed can increase bottleneck load.** The machining "efficiency" improvement created metal brittleness that required heat-treat. Local optimization on a non-constraint created extra work at the constraint. The fix — deliberately slowing the non-bottleneck — increases system throughput.
- **Frontline knowledge of the constraint is the fastest source of improvement.** Mike Haley developed batch pre-sorting and furnace-table ideas independently. Rogo's job is to find him, free him from third shift, and institutionalize what he knows.
