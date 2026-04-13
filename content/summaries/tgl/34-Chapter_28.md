---
related-concepts:
  - "[[Lead Time and Batch Size]]"
  - "[[Activation vs Utilization]]"
  - "[[The Constraint ⭐]]"
  - "[[Drum-Buffer-Rope]]"
---

# Chapter 28

## What Happens

Jonah calls from Singapore — he won't be reachable for a few weeks but has time to talk now. Rogo describes the situation: production is strong, but Peach wants 15% more, and the backlog is gone. Jonah says they've "only just begun" and suggests the next step.

**Cut batch sizes in half on non-bottlenecks.**

Jonah explains the four elements of time a part spends inside the plant:

1. **Setup time** — waiting for a resource to prepare itself
2. **Process time** — time actually being modified into a more valuable form
3. **Queue time** — waiting in line for a resource that's busy on something else
4. **Wait time** — waiting for another part to arrive so they can be assembled together

Setup and process are a small fraction of total elapsed time. Queue and wait dominate — often the vast majority. For bottleneck-bound parts, queue is the dominant element (stuck waiting in front of the bottleneck). For non-bottleneck parts, wait is dominant (sitting at assembly waiting for the bottleneck part to arrive). Either way, the bottleneck dictates both elements.

**The batch size logic:** Halving the batch size halves the time it takes to process each batch. Queue and wait time are proportional to batch size. Therefore, halving batch size halves queue and wait — and since those dominate total elapsed time, it roughly halves total lead time.

Halved lead time means:
- Inventory drops (parts spend half as long in the plant)
- Cash flow improves (less money tied up)
- Response to market demand is twice as fast
- Competitive advantage: promise delivery in 4 weeks vs. competitors' months

**Bob's objection:** More setups = higher direct labor cost. Rogo's counter — Jonah's symmetric rule:

> *"An hour saved at a non-bottleneck is a mirage."*

Non-bottlenecks now have idle time (thanks to DBR restricting material releases). Adding setups eats into idle time, not productive capacity. Setup costs at non-bottlenecks are illusory because the time being "saved" was going to be idle anyway. Doubling setups won't even consume all the idle time.

**Marketing.** Rogo drives to headquarters to meet Johnny Jons. Current lead time: ~2 months (down from 4). With halved batch sizes: 3–4 weeks. Jons is skeptical — last winter they promised 4 months and took 6. Rogo bets a pair of Guccis. Jons agrees to promise customers 6-week delivery. Counter-bet: if any order ships in under 5 weeks, Jons buys Rogo shoes.

## Management Observations

- **Lead time is dominated by waiting, not working.** The part that takes 10 minutes to machine may spend 3 weeks in a queue. Attacking process time has marginal impact; attacking queue and wait time is where lead time compression lives.
- **Batch size is a lead time lever.** Conventional batch-size optimization (EBQ formulas) minimizes setup cost. It ignores the cost of extended lead time: inventory carrying costs, delayed throughput, competitive disadvantage. The tradeoff looks completely different once lead time value is included.
- **Non-bottleneck setup costs are already paid.** The labor is on the payroll. The machine exists. Spending that idle time on a setup costs nothing marginal — and produces the lead time reduction that can win new orders.
- **Faster delivery is a competitive differentiator.** The plant can now offer something the market wants and competitors can't match. Throughput can grow not just by processing faster, but by attracting business that was previously going elsewhere.
