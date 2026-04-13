---
concept-type: "[[Framework]]"
description: Lead time is dominated by queue and wait, not setup and process — and both are proportional to batch size, so halving batch size roughly halves lead time.
related-concepts:
  - "[[The Constraint ⭐]]"
  - "[[Activation vs Utilization]]"
  - "[[Drum-Buffer-Rope]]"
  - "[[Throughput, Inventory, and Operating Expense ⭐]]"
sources:
  - "[[34-Chapter_28|Chapter 28 — Batch Sizes and Lead Time]]"
---

# Lead Time and Batch Size

## The Four Elements of Parts Flow Time

Every part that moves through a plant spends its total elapsed time in four states:

| Element | Definition |
|---|---|
| **Setup time** | Waiting for a resource to prepare itself to work on this part |
| **Process time** | Time being modified into a more valuable form |
| **Queue time** | Waiting in line for a resource that is busy on something else |
| **Wait time** | Waiting for another part so they can be assembled together |

**Setup and process are a small fraction of total elapsed time.** A part that takes 10 minutes to machine and 5 minutes to set up may spend 3 weeks sitting in a queue. Queue and wait dominate — often comprising 95% or more of total lead time.

## Where Queue and Wait Come From

- **Queue** is driven by bottleneck congestion. Parts bound for the bottleneck pile up waiting their turn. The longer the batch ahead, the longer the queue for the next batch.
- **Wait** is driven by assembly dependencies. Non-bottleneck parts arrive at final assembly and sit waiting for the bottleneck part that hasn't arrived yet. The bottleneck's queue time becomes the non-bottleneck part's wait time.

In both cases, the bottleneck dictates the dominant time element. This is why the bottleneck determines not just throughput and inventory, but also lead time.

## The Batch Size Lever

Halving batch size halves process time per batch. Since queue forms behind batches (a batch in queue = one batch worth of time before the next batch is touched), halving batch size roughly halves queue time. Wait time, which is bounded by bottleneck processing time, also shrinks proportionally.

Because queue and wait dominate total elapsed time, halving batch size roughly halves total lead time.

**Effect chain:**
- Halve batch size → halve queue and wait → halve lead time
- Halve lead time → halve WIP inventory (parts spend half as long in the plant)
- Halve WIP → reduce cash tied up in inventory
- Shorter lead time → faster response to orders → competitive advantage

## The Setup Cost Objection

Conventional batch-size optimization (Economic Batch Quantity / EBQ formulas) minimizes setup cost by spreading it over larger batches. This logic assumes setup time is the primary cost being managed.

But in a plant with idle non-bottleneck capacity (as in a DBR-managed plant), the workers and machines needed for setups already exist on the payroll. The marginal cost of an additional setup is close to zero — the time was going to be idle anyway. Meanwhile, the cost of large batches includes extended lead time, delayed throughput, and competitive disadvantage. EBQ optimizes the wrong variable.

**Jonah's symmetric rule:** *"An hour saved at a non-bottleneck is a mirage."* Saving setup time at a non-bottleneck preserves idle time. It does not increase throughput. The lead time benefit from smaller batches is real; the setup cost savings from larger batches are not.
