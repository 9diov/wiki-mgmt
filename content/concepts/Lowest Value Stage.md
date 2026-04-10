---
concept-type: "[[Framework]]"
description: The principle that defects should be caught and fixed as early in a process as possible, before further value has been added.
related-concepts:
  - "[[Limiting Step ⭐]]"
  - "[[Quality Assurance]]"
  - "[[Production Tradeoffs]]"
sources:
  - "[[09-Chapter_1__The_Basics_of_Production__Delivering_a_Breakfast_(or_a_College_Graduate,_or_a_Compiler,_or_a_Convicted_Criminal…)|Chapter 1 — The Basics of Production]]"
  - "[[10-Chapter_2__Managing_the_Breakfast_Factory|Chapter 2 — Managing the Breakfast Factory]]"
---

# Lowest-Value Stage

Detect and fix problems at the point in a production process where the defective material has accumulated the least value.

## Principle
Material becomes more valuable as it moves through production. A rotten egg caught at delivery costs almost nothing to reject. The same problem discovered after cooking, plating, and serving wastes every step in between—and damages the customer relationship.

> Reject before investing further value.

## Applications
- **Manufacturing**: Reject bad eggs on receipt (incoming inspection), not after boiling them
- **Recruiting**: Screen out weak candidates by phone before paying for a plant visit
- **Software**: Catch bugs in unit tests, not in final system test after full integration
- **Criminal justice**: Screening at earlier stages (campus interview, phone screen) is cheaper than discovering problems after heavy investment

## Inspection Types by Value Stage
| Stage | Name |
|---|---|
| Raw material, on receipt | Incoming / receiving inspection |
| Mid-process | In-process inspection |
| Finished, before shipment | Final / outgoing quality inspection |

## Reliability Exception
Never accept substandard material if the defect could cause a *reliability failure* for the customer—one that cannot be corrected after delivery. The financial and human cost of a failure (e.g., a pacemaker component) far exceeds any short-term savings from accepting marginal material.

## Examples
- **[[Three Minute Breakfast ⭐]]** — reject bad eggs at delivery (incoming inspection), not after boiling and plating
- **[[Intel College Recruiting]]** — phone screen before plant visit; reject weak candidates at the cheapest stage, not after a costly on-site
- **[[Compiler Development]]** — catch bugs in unit tests, not in final system test after full integration
- **[[Capital Equipment Approval]]** — reviewing capital requests at an early rough stage, before detailed engineering work has been done

*Source: Chapters 1 & 2*
