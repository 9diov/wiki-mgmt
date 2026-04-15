---
related-concepts:
  - "[[Work in Process (WIP) ⭐]]"
  - "[[Goldratt's Five Focusing Steps]]"
  - "[[Technical Debt]]"
sources:
  - "[[24-Chapter_19_•_Tuesday,_September_23|Chapter 19 — Tuesday, September 23]]"
---

# The Project Freeze

## The Setup

The off-site leadership team has just established that IT is carrying 35 business projects, 75 IT operations projects, thousands of pending changes, growing unplanned work, and a technical debt backlog that no one has measured. No one has been allowed to say no. Work keeps entering the system without capacity analysis.

Bill proposes something that sounds absurd: stop all non-Phoenix work. IT Operations freezes everything except Phoenix. Development freezes all deployments to Operations except Phoenix. Two weeks. No new work accepted.

Steve's first response: *"You must be out of your goddamned mind. Who do you think we are? Subsidized potato farmers paid not to grow crops?"*

Erik validates it by walking Steve through the manufacturing analogy directly. He asks Steve — who was once a plant manager — what happens when you freeze job releases at a plant with inventory piled to the ceiling:

*"The amount of WIP in the plant goes down, because work will start leaving the plant as finished goods."*

*"And what will likely happen to due-date performance?"*

*"Due-date performance goes up, because WIP went down."*

Steve arrives at the conclusion himself. He agrees to a one-week trial.

The freeze has two components: (1) halt new work intake and deployment flow; (2) have Development identify the top technical debt areas and actively pay them down during the freeze — reducing the source of future unplanned work while the current WIP drains.

Steve commits to sending a company-wide email making the freeze official, with explicit consequences for managers who try to strong-arm IT engineers into unauthorized work.

## What It Illustrates

**[[Work in Process (WIP) ⭐]]** — The freeze is the direct implementation of the manufacturing WIP reduction principle in IT. The logic is precise: work in process accumulates when work enters the system faster than the constraint can process it. Stopping new work entry allows the existing queue to drain. Due-date performance on the work that remains improves because it has undivided attention from resources no longer competing across forty projects simultaneously.

**[[Goldratt's Five Focusing Steps]]** — The freeze is Step 3 (subordinate) applied at the project level. Just as Brent's time was protected from unplanned interruptions at the resource level, the freeze protects the delivery system from new work injection at the project level. The constraint — both Brent and IT Operations' collective capacity — is given the space to work through the highest-priority commitment without new demand being thrown at it.

**[[Technical Debt]]** — The freeze's second component — paying down technical debt during the quiet period — is what separates a freeze from a pause. A pause reduces WIP temporarily; a debt paydown reduces the rate at which unplanned work is generated going forward. Without it, the freeze just defers the spiral rather than breaking it.
