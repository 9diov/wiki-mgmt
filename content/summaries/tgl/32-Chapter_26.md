---
related-concepts:
  - "[[Drum-Buffer-Rope]]"
  - "[[The Constraint ⭐]]"
  - "[[Activation vs Utilization]]"
  - "[[Throughput, Inventory, and Operating Expense ⭐]]"
---

# Chapter 26

## What Happens

At home that night, Rogo explains the hike problem to his kids — Herbie stuck in the middle, can't be moved, how do you keep the line together? Sharon's answer: a drummer, like a parade. Dave's answer: ropes, like mountain climbers. Rogo synthesizes: you don't need to tie everyone together, just link the front of the line to Herbie. When the front moves too fast, Herbie signals it to wait.

Back at the conference room earlier that day, the team had worked through the same logic. The solution Jonah confirmed:

**Release red-tag (bottleneck-bound) materials at the rate the bottleneck needs them — not whenever non-bottleneck machines run out of work.**

Ralph's contribution: he's been tracking the bottleneck queue and can calculate, within ±1 day, when material released now will reach the bottleneck. Travel time from first operations to the bottleneck averages two weeks. By knowing what's in the bottleneck queue and adding two weeks, he can predict when to release the next batch. A 3-day buffer of WIP in front of each bottleneck provides protection against fluctuations.

Jonah extends this further: once you know when bottleneck parts will reach final assembly, you can work backwards and calculate the release date for non-bottleneck (green-tag) materials too. The bottleneck schedule governs the release of *all* materials into the plant.

Jonah: *"That's going to produce the same effect as moving the bottlenecks to the head of production."*

**The efficiency problem.** Bob raises the political risk: non-bottleneck workers will have idle time; efficiency reports will look bad; Peach will see the numbers. Stacey's response:

> *"Once somebody is already on the payroll, it doesn't cost us any more to have them be idle. Whether somebody produces parts or waits a few minutes doesn't increase our operating expense. But excess inventory — that ties up a lot of money."*

Rogo decides: go ahead. Idle time is not the problem. Then, quietly, to Bob: *"If there is a lot of idle time out there, don't hassle anybody — just make damn sure it doesn't show up in the efficiency reports."*

## The Mechanism

The system the kids independently invented — drum and rope — is the scheduling logic that will govern the plant:

- **Drum:** the bottleneck sets the beat for the entire plant. Its processing schedule determines when material enters the system.
- **Buffer:** a small protective stock of WIP in front of the bottleneck (3 days) absorbs fluctuations without requiring overproduction upstream.
- **Rope:** the signal that ties material release at the start of production to the bottleneck's consumption rate. Non-bottlenecks don't release work when they run out of something to do; they release work when the bottleneck is ready for it.

## Management Observations

- **Idle workers cost nothing extra; excess inventory does.** Once headcount is fixed, an idle worker is a zero marginal cost. Inventory is a real carrying cost and a throughput delay. The efficiency metric has the signs backwards.
- **The bottleneck should govern material release, not worker availability.** The old system pushed material in whenever a non-bottleneck had capacity. The new system pulls material based on what the bottleneck needs and when.
- **Protecting efficiency numbers and improving plant performance are in direct conflict here.** Rogo chooses performance and asks Bob to manage the optics. This is a political concession, not a management principle — but it reflects the reality of operating inside a reporting system built on wrong assumptions.
