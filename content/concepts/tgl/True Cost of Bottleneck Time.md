---
concept-type: "[[Framework]]"
description: The actual cost of one idle bottleneck hour is the total operating expense of the entire plant divided by available bottleneck hours — not the machine's local operating cost.
related-concepts:
  - "[[The Constraint ⭐]]"
  - "[[Exploit the Bottleneck ⭐]]"
  - "[[Throughput, Inventory, and Operating Expense ⭐]]"
  - "[[content/concepts/tgl/Local Optimization Trap]]"
sources:
  - "[[25-Chapter_19|Chapter 19 — Jonah's Plant Visit]]"
---

# True Cost of Bottleneck Time

## The Formula

> **True cost of one bottleneck hour = Total plant operating expense ÷ Bottleneck hours available per month**

**Example from Rogo's plant:**
- Total operating expense: $1,600,000/month
- NCX-10 available hours: 585/month
- Standard accounting cost: $32.50/hour
- True cost: $1,600,000 ÷ 585 = **$2,735/hour**

The numbers are not wrong arithmetically. The assumption is wrong: standard costs are calculated *as if the bottleneck existed in isolation*. It does not. The capacity of the plant equals the capacity of its bottleneck. When the bottleneck is idle, the entire plant is effectively idle — no throughput is being produced.

## Why the Assumption Fails

Standard cost accounting allocates overhead across all work centers based on direct labor or machine hours. This produces a "cost per hour" that reflects the machine's share of total expense. But it ignores the system relationship: the bottleneck's output is the system's output.

An hour lost at a non-bottleneck costs the non-bottleneck's allocated share. An hour lost at the bottleneck costs the entire system's operating expense for that hour, because no other resource can recover what was not produced.

Jonah's diagnosis: *"The numbers were almost always right. If I checked the assumptions, they were almost always wrong."*

## Practical Implication

At $2,735/hour, decisions near the bottleneck look completely different:

- A 30-minute break costs ~$1,368 in lost throughput potential
- A rejected batch of 100 bottleneck parts is not a quality cost — it is 100 × whatever the bottleneck spends per part, multiplied by $2,735/hour
- Paying a vendor slightly more per part to offload work from the bottleneck may be obviously worth it at true bottleneck costs, even when it looks expensive at standard costs

The question is never "what does it cost to run the bottleneck?" but "what does it cost for the bottleneck not to run?"
