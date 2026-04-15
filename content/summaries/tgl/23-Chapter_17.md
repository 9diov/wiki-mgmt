---
related-concepts:
  - "[[Dependent Events and Statistical Fluctuations]]"
  - "[[Local Optimization Trap (synth)]]"
  - "[[The Constraint ⭐]]"
  - "[[Subordinate and Elevate ⭐]]"
---

# Chapter 17

## What Happens

Monday morning chaos: Dave burns pancakes, Sharon refuses to go to school, Rogo gets both kids out the door an hour late. He arrives at the plant past nine to find an urgent message from Hilton Smyth demanding 100 sub-assemblies by end of day — and a memo revealing that Smyth has just been promoted to division productivity manager, with dotted-line authority over all plant managers. Rogo sets up the expedite, then calls Smyth's secretary to say the shipment will arrive tomorrow regardless.

He spends the morning presenting the hike insights to his staff — Lou, Bob, Stacey, Ralph. Two hours of diagrams on an easel. Their reaction: unimpressed. Lou wants to know how Rogo can be sure these phenomena are actually happening in the plant. Bob pushes back on whether robots have statistical fluctuations at all.

Rogo turns the Smyth job into a live demonstration. Pete Schnell's department will fabricate parts (quota: 25/hour, noon to 4 PM). A robot will weld them (exactly 25/hour, 1 PM to 5 PM). Materials handlers will transfer parts from Pete to the robot every hour. Expected output: 100 sub-assemblies on the 5 o'clock truck. He bets Bob $10 they won't ship.

**What actually happens:**

Pete's log:

| Hour | Produced | Cumulative |
|---|---|---|
| 12–1 PM | 19 | 19 |
| 1–2 PM | 21 | 40 |
| 2–3 PM | 28 | 68 |
| 3–4 PM | 32 | 100 |

Pete's team finished all 100 parts. They cheered walking out. But the robot — which processes exactly 25 pieces per hour — could only work with what Pete delivered each hour. The early shortfalls constrained the robot's output even though Pete eventually caught up. By 4 PM, the robot still had backlogged pieces to work through. At 5:05, the robot is still running. The truck won't wait.

Rogo shows Bob the combined log. The maximum Pete was ever behind was 10 pieces. The shipment ends up exactly 10 short. The quote:

> *"The maximum deviation of a preceding operation will become the starting point of a subsequent operation."*

Bob pays up. Rogo redirects the $10 to Pete's team for coffee — and then flags the real problem:

> *"Pete and his people thought they were heroes. Ordinarily, we might have thought the same thing. That isn't right."*

Meanwhile: Rogo's mother moves in with two suitcases and four boxes of her own pots and pans to hold down the house until Julie returns.

## The Plant-Floor Proof

The chapter bridges abstraction and practice. The dice game (Chapter 14) was a controlled demonstration with matchsticks. This is the same mathematics playing out on the production floor with real parts, real equipment, and a real deadline.

Pete's fluctuations (−6, −4, +3, +7 from quota) were modest — no disaster, no equipment failure, no one shirking. His team actually rallied and finished strong. None of it mattered. The dependency between Pete's operation and the robot meant every shortfall below quota was passed forward as a deficit the robot could never recover, while every overage above quota was absorbed as inventory waiting in queue. The system's final output was governed by the accumulated negative deviation — not Pete's heroic finish.

## Management Observations

- **"We beat the quota" is the wrong victory.** Pete's department hit 100 pieces. The shipment still failed. Local completion does not equal system output. This is the incentive trap in concrete form: the people doing the work celebrated a performance that had no impact on the goal.
- **The robot's precision doesn't help.** The robot is exactly the kind of "efficient, consistent" equipment managers celebrate. But its precision only means it faithfully transmits the accumulated deficit. Consistency at a non-constraint doesn't rescue throughput when the upstream operation is fluctuating.
- **The maximum negative deviation propagates exactly.** Not approximately — exactly. Pete's worst cumulative shortfall was 10. The shipment was 10 short. The math is deterministic once the dependency is in place.
- **Staff skepticism is reasonable.** Lou's objection — "how do you know this is really happening in our plant?" — is a fair question. The live demonstration was the right response. Abstract principles need a concrete referent before they change behavior.
