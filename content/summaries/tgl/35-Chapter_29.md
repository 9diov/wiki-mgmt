---
related-concepts:
  - "[[Lead Time and Batch Size]]"
  - "[[Activation vs Utilization]]"
  - "[[The Constraint ⭐]]"
  - "[[Throughput, Inventory, and Operating Expense ⭐]]"
---

# Chapter 29

## What Happens

**4 AM, Rogo's house.** Julie is back. A nightmare about Peach chasing him in a Mercedes has woken Rogo up. He sits in the dark cataloguing the results so far: new contracts from marketing, efficiencies holding steady (excess inventory was consumed, then work resumed), batch sizes cut in half, WIP at historic lows. The bad news: smaller batches mean more setups, which raises the per-part direct labor cost in the accounting system — even though actual operating expense hasn't changed.

**The cost accounting problem.** He explains it to Julie: batch of 100 parts, 2-hour setup, 5 min/part → 6.2 min direct labor per part. Batch of 50, same 2-hour setup → 7.4 min per part. Burden (overhead allocated as a multiple of direct labor) goes up proportionally. On paper, part costs have risen. In reality, no new people were hired, no new costs incurred. Operating expense is actually lower per unit because it's spread over more product. The measurement assumes 100% worker utilization; since that assumption is wrong, the cost signal is wrong.

Lou's solution: change the cost base from last 12 months to last 2 months (high-throughput period), which makes part costs look better. Technically against policy, but defensible given the plant's transformation. Rogo approves; they'll use it and hope Frost doesn't look too closely.

**The Burnside order.** Johnny Jons calls: a customer (Burnside) needs 1,000 Model 12 units in two weeks. The order had been with a competitor for five months; the competitor failed to deliver. Burnside is desperate and heard about Bearington's fast turnaround. Preferred-supplier status on the line. Problem: only 50 units in stock; need 950 manufactured; bottleneck rate is 100/day.

Rogo's moves:
1. Cut batch sizes in half *again* — further compressing lead time and freeing bottleneck capacity
2. Reschedule orders currently being shipped early (ahead of due dates) back to their actual due dates — reclaims bottleneck time without hurting anyone
3. Electronic control modules (a vendor-only component): instead of ordering 1,000 at once (4–6 week delivery), order in weekly installments shipped air freight

Result: 250 units per week for 4 weeks, first shipment in 2 weeks. Jons calls back that night: Burnside took the deal — and prefers the staggered shipments.

## Management Observations

- **Cost accounting punishes the right decision.** Smaller batches reduce inventory, lead time, and total operating expense per unit. The accounting system reports a cost increase. This is the same distortion Jonah identified at the plant tour: the numbers are arithmetically correct; the assumptions are wrong.
- **Smaller shipments can be better for customers.** Burnside preferred 250/week over a single delivery of 1,000. Smaller batches don't just help the plant — they align with how customers actually manage their own inventory and production.
- **Rescheduling early-ship orders is recoverable capacity.** Shipping ahead of promise dates builds goodwill but consumes bottleneck time. When a large order needs that capacity, releasing early-ship orders back to their due dates is a zero-cost lever.
- **Air freight on a critical component is often worth it.** The cost of air-freighting small electronic modules is trivial compared to a million-dollar order and preferred-supplier status. The instinct to minimize shipping cost is the wrong optimization.
