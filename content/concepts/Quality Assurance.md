---
concept-type: "[[Practice]]"
description: A set of inspection strategies that balance catching defects against the cost and flow disruption of the inspection itself.
related-concepts:
  - "[[Lowest Value Stage]]"
  - "[[Production Operations]]"
  - "[[Work Simplification]]"
  - "[[Delegation ⭐]]"
sources:
  - "[[09-Chapter_1__The_Basics_of_Production__Delivering_a_Breakfast_(or_a_College_Graduate,_or_a_Compiler,_or_a_Convicted_Criminal…)|Chapter 1 — The Basics of Production]]"
  - "[[10-Chapter_2__Managing_the_Breakfast_Factory|Chapter 2 — Managing the Breakfast Factory]]"
---

# Quality Assurance

A set of inspection strategies that balance catching defects against the cost and disruption of the inspection itself.

## Gate Inspection vs. Monitoring

**Gate inspection**
All material is held until the test completes. Pass → move forward. Fail → rework or scrap. No bad material escapes, but throughput slows and cycle time grows.

**Monitoring (sampling)**
A sample is taken; the bulk of material continues moving. If successive samples fail, stop the line. Maintains flow smoothness but may let some defective material pass before the signal triggers action.

The trade-off: for the same cost, you can monitor far more frequently than you can gate-inspect. Higher frequency monitoring can contribute more to overall quality than less-frequent gate checks.

## Variable Inspection
Adjust inspection frequency based on observed quality:
- Consistent high quality → inspect less often
- Problems emerging → increase frequency until quality stabilizes

This reduces cost and production interference without materially increasing risk. Applied to management: a manager who reviews everything is meddling; a manager who never checks is abdicating. Strategic, variable spot-checks thread the needle.

## The Rule on Reliability
Economic trade-offs govern most quality decisions. The one exception: **never** accept substandard material if the defect could cause a reliability failure—a complete failure that the customer cannot recover from. A component in a cardiac pacemaker is the extreme case. When the cost of a post-delivery failure is incalculable, no compromise is acceptable.

## Application Beyond Manufacturing
The same principles apply to administrative inspection:
- A U.S. embassy processing 1 million visa applications/year approves 98% without issue. A sampling approach (as the IRS uses with tax returns) would process the same volume with far less friction—without materially increasing risk.
- A manager reviewing subordinates' work should do so at variable frequency, increasing scrutiny for new or unfamiliar tasks and relaxing it as the subordinate demonstrates reliability.

## Examples
- **[[Three Minute Breakfast ⭐]]** — visual check of coffee and toast before serving as a final gate inspection
- **[[US Embassy Visa Processing]]** — processing 100% of applicants was an unreflective default; sampling (as the IRS uses) would achieve the same quality standard with far less friction

*Source: Chapters 1 & 2*
