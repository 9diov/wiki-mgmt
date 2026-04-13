---
related-concepts:
  - "[[The Constraint ⭐]]"
  - "[[Exploit the Bottleneck ⭐]]"
  - "[[True Cost of Bottleneck Time]]"
  - "[[Balance Flow Not Capacity]]"
  - "[[Throughput, Inventory, and Operating Expense ⭐]]"
---

# Chapter 19

## What Happens

Rogo picks up Jonah at the airport. On the drive in, Jonah makes a remark that reframes everything: most plants do not have bottlenecks — they have enormous excess capacity. But they *should* have a bottleneck. *"One on every part they make."* Having a bottleneck is not a symptom of failure; it is a useful control point. The problem is not the bottleneck's existence but how it is being managed.

At the plant, Jonah leads the team on a tour. His first question at the NCX-10: *"Why isn't it running?"* It's a break. The setup people are off the machine for thirty minutes while the bottleneck sits idle.

Jonah's response establishes the logic that governs everything that follows:

> "On any non-bottleneck machine — no problem. Some percentage of a non-bottleneck's time should be idle. But on a bottleneck? Every hour you lose is gone forever. Your throughput for the entire plant will be lower by whatever amount the bottleneck produces in that time."

At heat-treat, Jonah reframes the pile of waiting parts. The team estimates $15–20K in material costs. Jonah corrects them: the pile contains ~1,000 parts, each enabling a $1,000 product shipment. That pile represents **$1 million in potential throughput** — delayed until the parts clear heat-treat and reach customers who haven't yet left for a competitor.

At QC, Jonah finds rejected bottleneck parts waiting to be scrapped. His point: a defect caught after the bottleneck wastes irreplaceable bottleneck time. The right place for quality inspection is *before* the bottleneck — ensure the bottleneck only ever processes good parts.

Back in the conference room, Jonah corrects the cost numbers.

**True cost of bottleneck time:**
- Standard accounting says NCX-10 costs $32.50/hour; heat-treat costs $21/hour
- Jonah's formula: total plant operating expense ÷ bottleneck hours available = true cost per bottleneck hour
- $1,600,000/month ÷ 585 hours = **$2,735 per bottleneck hour**

The numbers were not wrong arithmetically. The assumption was wrong: they calculated bottleneck costs *as if the bottleneck existed in isolation*. But the capacity of the plant equals the capacity of its bottleneck. One idle bottleneck hour = one hour the entire plant is not producing throughput.

**Three ways bottleneck time is wasted:**
1. Sitting idle (breaks, waiting for materials, waiting for setups)
2. Processing defective parts — which then get scrapped, wasting the bottleneck time spent on them
3. Making parts not needed now — building future inventory while current orders go unshipped

**Two ways to increase bottleneck capacity:**
1. Stop wasting bottleneck time (the three items above)
2. Offload work from the bottleneck to non-bottlenecks — check whether all parts *need* to go through the bottleneck; find vendors or alternate machines for those that don't

On the domestic front: Julie called again. Sharon heard classical music (violins) in the background. Rogo suspects she's at her parents'. He resolves to call them again.

## The Pivot

Chapter 19 shifts the team from diagnosis to action. The bottlenecks are found; now they are understood. The key reframe: hidden capacity already exists inside the bottleneck — it has been consumed by idle time, defective parts, and unnecessary work. No new equipment, no capital expenditure required for the first round of improvements.

## Management Observations

- **Bottlenecks are not inherently bad — unmanaged bottlenecks are.** A bottleneck is a control point. The failure is running it with the same assumptions as a non-bottleneck.
- **Standard cost accounting is wrong about bottlenecks.** The cost of a bottleneck hour is the cost of the whole system's hour, not just the machine's operating cost. This is not a rounding error — it changes $32 into $2,735. Every spending decision near the bottleneck looks different at that price.
- **Inventory in front of a bottleneck is not a cost — it is delayed throughput.** The heap of parts at heat-treat looks like $15K in materials. It is actually $1M in revenue waiting to ship. Managing the bottleneck is managing the release of that value.
- **QC placement is a system design decision.** Where inspection happens determines whether catching defects saves bottleneck time or wastes it. Post-bottleneck inspection punishes the entire system for each defect.
