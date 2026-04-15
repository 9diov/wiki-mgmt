---
related-concepts:
  - "[[The Constraint ⭐]]"
  - "[[Balanced Plant Fallacy]]"
  - "[[Balance Flow Not Capacity]]"
  - "[[Dependent Events and Statistical Fluctuations]]"
  - "[[Local Optimization Trap (synth)]]"
---

# Chapter 18

## What Happens

Julie called while Rogo was at work — spoke to the kids, said she loved them, couldn't say when she'd be back, refused to leave a number. Tuesday morning his mother manages the house; the staff, now believers after watching the Pete/robot demonstration, regroup.

Rogo calls Jonah. With the staff on speaker phone, Jonah delivers the formal framework.

**Jonah's definitions:**

> A **bottleneck** is any resource whose capacity is equal to or less than the demand placed upon it. A **non-bottleneck** is any resource whose capacity is greater than the demand placed on it.

And his first rule:

> **Balance flow, not capacity.**

Don't try to match each resource's capacity to demand. Instead, make the *flow of product through the plant* match market demand — and the bottleneck is the resource that governs that flow. A tiny bit below demand is fine; equal is acceptable; above is waste.

Jonah hangs up. The team's next step: find out if the plant has a bottleneck.

**The search.** They attempt a systematic data-driven approach — calculating demand for every work center and comparing against available hours. It bogs down immediately. Bills of material don't match routings. Run-times are outdated. They spent two and a half hours calculating demand for machines that were sold a year ago.

Rogo cuts it short: *"We're not going to have time for perfect data. We've got ten weeks."* Two faster methods emerge:

1. **Ask the expeditors.** The parts they're always chasing are probably the ones that go through a bottleneck. The departments where expeditors spend most of their time are bottleneck candidates.
2. **Follow the inventory.** On the hike, the slow kids had the largest gaps in front of them. In the plant, the bottleneck will have the largest pile of work-in-process sitting in front of it.

The search narrows fast. They find two bottlenecks.

**Bottleneck 1: The NCX-10.** The plant's newest, most efficient machine — the one Peach sabotaged in Chapter 1. It replaced three older machines and processes parts faster per unit (10 minutes vs. 14 minutes on the old setup). But it replaced *ten* machines total, and there's only one of it. Net result: less total throughput capacity despite better per-unit efficiency. Weeks of WIP stacked in front of it. Setup personnel hard to train (six months) and hard to retain. Third-shift position only recently filled after Tony quit.

**Bottleneck 2: Heat-treat.** Two furnaces, each running 6–16 hours per batch. The problem: expeditors keep interrupting with small urgent runs — five pieces here, a dozen there — so the furnaces almost never run full. Half-empty furnaces doing the same number of heat cycles as full ones. A proposal for a third furnace was killed at division level for low efficiency.

**The plan fails before it starts.** Rogo's instinct is to do what he did on the hike — put the bottleneck at the front of production, with graduated capacity increases downstream. The staff shuts it down immediately: the sequence of operations is fixed by engineering and metallurgy. You can't move the NCX-10 or heat-treat ahead of steps that must logically precede them.

Alternative: add capacity to the bottlenecks and turn them into non-bottlenecks. Lou kills that too — no budget, worst year in company history, Peach would never approve it.

The chapter ends with the team staring at two confirmed bottlenecks and no obvious path forward.

## Management Observations

- **Data systems don't survive operational chaos.** The attempt to find bottlenecks through the database hits bad routings, missing machines, and outdated run-times almost immediately. Floor knowledge and expeditor behavior are faster and more reliable signals than stale records.
- **The most efficient machine can be the bottleneck.** The NCX-10 is the plant's best equipment — lowest cost, highest rate per part. It's also the constraint. Efficiency per unit and total throughput capacity are different measurements; buying one efficient machine to replace ten less efficient ones can reduce total capacity even while improving unit costs.
- **Expeditor behavior is a diagnostic signal.** Where expeditors spend their time maps the bottleneck. This is a cheap, fast, and accurate way to locate capacity constraints that no data system can match.
- **Half-empty furnaces are a symptom of system dysfunction, not operator failure.** The heat-treat furnaces look underutilized; the efficiency report reflects this. The cause is upstream expediting behavior driven by the wrong incentives. The "low efficiency" that killed the third furnace proposal was itself caused by the bottleneck dynamics the third furnace might have helped resolve.
