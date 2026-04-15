---
books-compared:
  - "[[The Goal (TGL)]]"
  - "[[Toyota Production System (TPS)]]"
  - "[[High Output Management (HOM)]]"
concepts:
  - "[[The Constraint ⭐]]"
  - "[[Five Focusing Steps ⭐]]"
  - "[[Subordinate and Elevate ⭐]]"
  - "[[Drum-Buffer-Rope]]"
  - "[[Dependent Events and Statistical Fluctuations]]"
  - "[[Takt Time ⭐]]"
  - "[[Just-in-Time ⭐]]"
  - "[[Production Leveling (Heijunka)]]"
  - "[[Limiting Step ⭐]]"
  - "[[Production Tradeoffs]]"
---

# The Limiting Step — Across Three Books

All three books share a foundational claim about how systems work: **one step determines the output of the entire sequence**. Everything else is secondary. Improving any other step doesn't improve overall output. The step that limits the system deserves all the attention that other steps don't deserve.

They call it different things — constraint, bottleneck, takt-pace step, limiting step. They find it through different methods, treat it with different strategies, and hold fundamentally different views on what to do with it once found. These differences are as instructive as the shared insight.

---

## The Goal: Find the Constraint, Then Govern Everything Else Through It

Goldratt's argument begins with mathematics. [[Dependent Events and Statistical Fluctuations|Dependent events combined with statistical fluctuations]] create an asymmetry in any production sequence: slowness propagates forward through the chain, but speed does not. When step 3 runs slow, step 4 waits; when step 3 runs fast, it merely builds a queue in front of step 4. Averaged over time, systems drift toward longer cycle times and higher inventory — even when every step's average capacity matches demand. This is the mathematical proof that a balanced plant cannot exist in practice.

The consequence: every system of dependent operations has a **[[The Constraint ⭐|constraint]]** — the one step whose capacity is equal to or less than the demand placed on it. All other steps have capacity to spare. The constraint's throughput rate is the system's throughput rate, regardless of how fast every other step can go.

An hour lost at the constraint is an hour lost for the entire system — there is no way to recover it downstream. An hour saved at a non-constraint saves nothing — the non-constraint wasn't limiting throughput anyway.

The [[Five Focusing Steps ⭐]] operationalize this:
1. **Identify** — find the constraint (follow the inventory; ask expeditors; find the most-praised "efficient" machine)
2. **Exploit** — get the maximum from the constraint as it exists today: eliminate idle time, stop feeding it defective parts, remove non-bottleneck work from it
3. **Subordinate** — arrange everything else to serve the constraint's needs, not their own utilization targets
4. **Elevate** — if exploitation isn't enough, add capacity to the constraint
5. **Repeat** — when the constraint breaks, a new one will emerge somewhere else

**[[Drum-Buffer-Rope]]** is the operational implementation of subordination. The bottleneck (drum) sets the pace for the entire plant. A protective buffer of work-in-process sits in front of the bottleneck to shield it from upstream fluctuations. The rope ties material release at the start of production to the bottleneck's consumption rate — nothing enters the system faster than the bottleneck can absorb it. Non-bottlenecks will have idle time; that is correct, not wasteful.

**[[Subordinate and Elevate ⭐|Moving Herbie to the front of the line]]** is the physical demonstration of this principle. In the boy scout hike, Herbie at the back causes the column to accordion: fast boys sprint ahead, creating a gap; the column bunches when they slow down; inventory accumulates as trail between Ron at the front and the constraint in the middle. Moving Herbie to the front makes the constraint visible and the system governable. Redistributing his pack (elevation) then directly increases the column's effective speed.

TGL is explicit on one uncomfortable truth: **a constraint will always exist**. Breaking one only moves it. The Five Focusing Steps are a cycle, not a completion. The last step's warning — *do not let inertia cause a system's constraint* — is a reminder that solutions built around one constraint can become constraints themselves when the bottleneck moves.

---

## TPS: Takt Time as the Designed-In Constraint — Real Constraints Are Waste

TPS does not name "the constraint" as a central concept, but the idea is present in a different form. **[[Takt Time ⭐]]** — available operating time divided by required daily quantity — is the pace the entire production system is designed to match. Every process is tuned to produce one unit per takt period. Takt is, in effect, a designed-in limiting step: the one rate that governs everything else.

The critical difference from TGL: in TPS, the limiting step is *external demand*, not an internal resource. The drum is the customer's required rate, not the plant's slowest machine. Ohno's ideal is that every process in the plant runs *exactly at takt* — no process is faster (overproduction), no process is slower (a problem requiring elimination). The goal is not to identify which internal step is limiting and exploit it; the goal is to eliminate every internal obstacle so that **demand, expressed as takt, is the only constraint**.

When an internal process *does* limit the flow — running slower than takt, creating a bottleneck — TPS treats this as **waste to be eliminated**, not a resource to be managed. Standard work is rewritten to eliminate non-value-added steps. [[Five Whys ⭐|Root-cause analysis]] surfaces why the step is slow. [[Just-in-Time ⭐|JIT]] removes the inventory buffers that were absorbing the slowness and hiding it. The constraint is exposed and then eliminated, not exploited and buffered.

**[[Production Leveling (Heijunka)]]** addresses the upstream source of constraint pressure before it reaches the production floor. Irregular demand (dekansho production — all the month's work bunching at month-end) makes any internal step a variable constraint depending on the moment. Leveling demand into a steady daily rate makes the system's pace stable and predictable. The pull system then works from this stable base: downstream withdraws at a steady rate; upstream produces to replace only what was withdrawn; each step runs at takt.

TPS's approach to variability is also different from TGL's. Goldratt responds to statistical fluctuations with a buffer (the bottleneck buffer in DBR). Ohno responds to variability by eliminating it at source — through level scheduling, standard work, and [[Preventive Maintenance|preventive maintenance]]. The buffer is not a feature; it is a concession TPS works to make unnecessary.

Where TGL asks "what is the constraint, and how do we manage around it?" TPS asks "why does any step run slower than takt, and how do we eliminate that waste?" The endpoint is different: TGL accepts that a constraint will always exist and builds a management method around that reality. TPS aims for a system where takt is the only pace-setter and every process flows at the rate the customer requires.

---

## HOM: Design the Entire Process Around the Limiting Step

Grove's treatment is the most practical and design-oriented of the three. The **[[Limiting Step ⭐]]** is not discovered through crisis or exposed by removing buffers — it is *designed around from the start*. The principle: identify the slowest, most expensive, or hardest-to-redo step in any production process and design the entire flow backward from it.

The **[[Three Minute Breakfast ⭐|three-minute breakfast]]** is the simplest illustration. The egg takes 3 minutes; toast takes 1 minute; coffee is already brewed. The egg is the limiting step. The entire production plan is organized around it: start coffee immediately, start toast at minute 2, deliver everything simultaneously at minute 3. Running toast or coffee first and letting them wait for the egg is not wrong in any dramatic sense — but it is the wrong design. The limiting step governs the schedule.

The **[[Intel College Recruiting]]** example shows the limiting step principle applied to a knowledge process. The plant visit — expensive in manager time and travel cost — is the limiting step in the hiring process. Every candidate who visits without receiving an offer is a wasted use of the limiting step. The solution: insert phone screens *before* issuing plant visit invitations. The phone screen is cheap; it filters out weak candidates before they consume the expensive step. The limiting step is protected by upstream gates, not buffered against failure downstream.

The **[[Criminal Justice System]]** case makes the same point through a system-design failure. The limiting step in the justice system is conviction — the most expensive, hardest-to-achieve output of the entire chain. Society invests over $1M per conviction through police, prosecution, and courts. But the system is then constrained by jail-cell availability, a far cheaper resource. Convicted criminals serve shortened sentences or none at all because cells are scarce. The wrong step is limiting the process: a $20,000/year cell is determining whether a $1M conviction is used. This is what misidentifying the limiting step costs.

Two distinctive contributions from HOM not present in the other books:

**Time offsets.** The limiting step determines not just what to optimize but *when* to start every other step. Each upstream step should be started at the offset that brings it to completion exactly when the limiting step needs its input. In the breakfast: start toast at t=2 because it takes 1 minute and the egg finishes at t=3. In recruiting: work backward from graduation (June) through offer deadlines, plant visits, phone screens, and on-campus interviews to determine when each step must begin.

**The limiting step can shift.** If the toaster queue becomes congested (multiple waiters competing for one toaster), the toaster becomes the new limiting step even though the egg still determines quality. The entire production plan must be reworked around the new constraint. This is the same insight as TGL's inertia warning — when a constraint breaks or changes, the system's architecture must change with it.

---

## Comparison

| | The Goal | TPS | HOM |
|---|---|---|---|
| **Name** | Constraint / Bottleneck | (Implicit) — process slower than takt | Limiting Step |
| **Where it comes from** | Emerges from system dynamics (dependent events + variability) | Internal process slower than takt = waste symptom | Identified by cost, time, or irreversibility |
| **Primary response** | Exploit, then subordinate everything else, then elevate | Eliminate the waste causing the slowness | Design the entire process around it; protect it with upstream gates |
| **Role of variability** | Buffer the constraint against fluctuations (DBR) | Level demand (heijunka) to remove variability before it reaches the floor | Protect limiting step with upstream filters |
| **Is a constraint permanent?** | Always one constraint; breaking it moves it | No — constraints are waste to eliminate | The limiting step changes when system conditions change |
| **The pacemaker** | The bottleneck (internal resource) | Takt time (external demand) | The limiting step (internal design choice) |
| **Non-limiting steps** | Should run below maximum; idle time is correct | Should run at takt — no more | Should start at the time-offset that feeds the limiting step |

---

## The Key Divergence: Manage or Eliminate?

The most instructive difference between TGL and TPS is their attitude toward the constraint once found.

**TGL manages around it.** DBR puts a buffer in front of the bottleneck. Scheduling is built around the bottleneck's capacity. Non-bottlenecks are subordinated to feed it. The bottleneck is the most important resource in the plant; it receives disproportionate attention and protection. This is the right response when constraints are structural — a machine with finite capacity, a specialist with unique skills, a regulatory approval process with fixed throughput.

**TPS eliminates it.** The bottleneck is evidence of waste: a step with non-value-added work that can be removed, a layout that creates unnecessary transportation, a changeover time that hasn't been reduced, a defect rate that consumes capacity. The buffer DBR places in front of the bottleneck is, in TPS terms, inventory waste — useful perhaps as a transition measure, but not a permanent solution. The correct response is to remove the waste that makes the step slow until it runs at takt with everything else.

Both responses are correct in different circumstances. TGL's approach is faster: you don't need to eliminate the constraint to improve throughput dramatically; you just need to exploit it better and stop non-bottlenecks from flooding it. TPS's approach is more durable: a system where every process flows at takt has no internal constraint to buffer, no bottleneck to protect, no point of fragility when demand patterns shift.

A practical synthesis: use TGL's constraint logic to quickly identify where improvement will have system-level impact; use TPS's waste-elimination approach to actually improve the constraint and eventually move it. DBR as a transitional tool, takt-flow as the endpoint.

**HOM's design-first approach** complements both: for processes being *built or redesigned*, identify the limiting step before allocating resources. Don't invest in making non-limiting steps faster; invest in making the limiting step more reliable, more efficient, and better protected by upstream quality gates. This is the planning-time equivalent of TGL's exploitation step — the question is the same, just asked before the system exists rather than after it's failing.

---

## What Happens When the Constraint Moves

All three books, in different ways, address what happens when the limiting step changes — and all three treat this as a critical management moment.

**TGL**: The Five Focusing Steps end with an explicit warning: *do not allow inertia to cause a system's constraint*. When the bottleneck is broken, a new one will emerge. The scheduling rules, buffer sizes, and subordination decisions built around the old constraint may now harm the new one. The entire analysis must restart. Organizations that don't notice the shift continue subordinating to a step that is no longer limiting — and accumulate waste and inventory around the new, unmanaged constraint.

**TPS**: When a process is improved past takt — when waste is eliminated until a formerly slow step now runs faster than demand requires — the improvement work moves to the next slowest process. There is always another waste to eliminate. The continuous improvement cycle (kaizen) is structured around this: takt time as the reference, every process measured against it, improvement work focused on the largest gap from takt.

**HOM**: When the toaster queue becomes congested, the entire breakfast production plan must be reworked around the new constraint. Time offsets change. The scheduling model that worked before now produces cold toast waiting for hot eggs. The practical lesson: a production plan is valid only for the system configuration it was designed around. Changes to any step's capacity, especially one near the limiting step, may invalidate the whole plan.
