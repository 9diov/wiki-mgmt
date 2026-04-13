---
related-concepts:
  - "[[The Constraint ⭐]]"
  - "[[Activation vs Utilization]]"
  - "[[Balance Flow Not Capacity]]"
  - "[[Local Optimization Trap]]"
  - "[[Balanced Plant Fallacy]]"
---

# Chapter 25

## What Happens

Jonah's second plant visit. They find the milling machines: a foreman named Jake explains that 75–80% of his work is red-tagged (bottleneck-bound) parts. He's been following the rules — red before green. The green-tagged parts needed at final assembly have been sitting untouched for two to three weeks. Meanwhile, inventory in front of the NCX-10 has grown into a mountain reaching forklift height.

Jonah diagnoses the root cause on the plant floor with chalk diagrams. He draws four fundamental combinations of bottleneck (X) and non-bottleneck (Y):

**Case 1: Y → X** (Y feeds X)
Y needs 450 of its 600 available hours to satisfy demand. If Y is kept fully activated, it produces parts faster than X can process them. The excess piles up in front of X.

**Case 2: X → Y** (X feeds Y)
Y can only work as fast as X delivers. Y will be idle — starved. This is *acceptable*. Idle Y is not a problem.

**Case 3: Y and X both feed Assembly** (parts from both needed for the same product)
Keeping Y fully activated produces parts that sit at assembly waiting for the X parts that haven't arrived yet. Inventory builds at assembly instead of in front of X.

**Case 4: Y → Product A, X → Product B** (independent products)
Y can't sell more than market demand for Product A. Running Y to maximum produces excess finished goods — the constraint has moved to marketing's ability to sell.

**Common pattern across all four cases:** In no case does Y determine throughput. Activating Y above the level justified by demand always results in excess inventory — not more throughput.

**Two rules Jonah derives:**

> **Rule 1:** The level of utilization of a non-bottleneck is not determined by its own potential, but by some other constraint in the system.

> **Rule 2:** Activating a resource and utilizing a resource are not synonymous.

"Utilizing" means making use of a resource in a way that moves the system toward the goal. "Activating" is pressing the ON switch — the machine runs whether or not the work it produces will ever become throughput. Activating a non-bottleneck beyond what the system can absorb is not efficiency; it is the manufacturing of inventory.

**The actual diagnosis at the milling machines:** Not a genuine new bottleneck. The plant kept releasing materials to keep workers busy even as throughput increased. The volume of red-tagged work overwhelmed the millers' available time, preventing green parts from moving. Jonah: *"The milling machines are not intrinsically a bottleneck. You have turned them into one."*

The chapter ends with Jonah directing them back to the conference room to discuss the solution.

## Management Observations

- **A plant where everyone is always busy is maximally inefficient.** Keeping non-bottlenecks fully activated floods the system with inventory the bottleneck can't process. The busyness is real; the throughput contribution is not.
- **Idle non-bottleneck time is not waste — it is the correct outcome.** A non-bottleneck that is idle after satisfying the system's needs is working exactly as it should. Forcing it to produce more is what creates the problem.
- **The inventory mountain is a management decision, not a production outcome.** The parts in front of the NCX-10 were put there by the policy of activating workers to keep utilization high. The machine didn't accumulate that inventory; the scheduling system did.
- **Efficiency targets for non-bottlenecks are meaningless or destructive.** At 90% utilization, a non-bottleneck feeding a bottleneck is producing inventory at 90% of maximum speed. The correct question is never "how busy is this machine?" but "is what this machine is producing moving the system toward its goal?"
