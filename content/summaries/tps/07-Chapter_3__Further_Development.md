---
related-concepts:
  - "[[Takt Time ⭐]]"
  - "[[Value-Added Work]]"
  - "[[Overproduction]]"
  - "[[Seven Wastes (Muda) ⭐]]"
  - "[[Pull System and Kanban ⭐]]"
  - "[[Standard Work]]"
sources:
  - "[[07-Chapter_3__Further_Development|Chapter 3 — Further Development]]"
---

# Chapter 3: Further Development

## Core Argument

A production system built on waste elimination must eventually address how the organization *thinks*, not just how it operates. Chapter 3 develops TPS from a set of tools into an organizational philosophy: information should be just-in-time just as parts are; efficiency means matching output to demand, not maximizing output; machines are worth what they can produce, not what accounting says they cost; and management skill cannot be calculated — it must be trained.

## Key Ideas

**The autonomic nervous system — decentralized judgment**
Ohno opens with a biological analogy: the human body has motor nerves (controlled by the brain) and autonomic nerves (reflexive, local, no brain required). A business should work the same way. When kanban and JIT are internalized, workers can decide when to stop production, what sequence to follow, and whether overtime is needed — without consulting the production control department. The "brain" is freed for strategy; the plant handles its own reflexes.

Large organizations that require a brain command for every small plan change are like bodies with no autonomic nervous system — they get burned before the signal completes.

**Information just-in-time — suppress excess**
Ohno applies the JIT principle to information itself: provide only the information needed, exactly when it is needed, at the place it is needed.

Toyota's information architecture:
- Annual plan (rough quantity) → monthly schedule → daily level (quantity per product type per line)
- The **daily sequence schedule** is sent only to the **final assembly line** — not to every upstream process
- From there, kanbans carry the information backward, process by process, as parts are actually consumed

Sending Car #20's specifications to every process simultaneously — as computers naturally do — causes each process to start working on #20 immediately. But Process A may currently need #6's information, not #20's. Early information induces early production, which is overproduction.

**True efficiency vs. apparent efficiency**
A line of 10 workers producing 100 units/day gets improved and can now produce 120 units. If demand is still 100 units, running at 120 is waste — not efficiency. True efficiency = 8 workers producing the 100 units required. Apparent efficiency = 10 workers producing 120 units and building 20 units of unwanted inventory.

Ohno's formula: efficiency improvement only counts when it reduces cost. Increasing production beyond the required number increases cost, not efficiency. The required number — set by demand, not by the production department — is the only valid output target.

**[[Takt Time ⭐]] — the operational heartbeat**
Takt time is operating time ÷ required daily quantity. It is the pace at which each process must produce to meet demand exactly — no faster, no slower. Every improvement in standard work is measured against takt time: can the worker complete the sequence within takt? If yes, the process is in control. If no, the process has a problem to solve.

Ohno's distinction: **operating rate** (how much of the time a machine actually runs) vs. **operable rate** (how reliably a machine runs when needed). The ideal operating rate is not 100% — you should only run a machine when you need output from it. The ideal operable rate is 100% — when you need the machine, it must work. Keeping machines running to maximize their operating rate produces overproduction. Maintaining machines to maximize their operable rate enables JIT.

**[[Value-Added Work]] — the hierarchy of motion**
Every worker action falls into one of three categories:
1. **Value-added work** — physically changes the shape or character of a product (forging, welding, assembling, painting). This is the only category that a customer would pay for.
2. **Non-value-added but necessary work** — picking up parts, opening packages, pressing buttons. Required under current conditions but adds no value. Target for elimination through layout and tooling changes.
3. **Waste** — waiting, stacking subassemblies, overproduction. Eliminate immediately.

The ratio of value-added work in most plants is far lower than managers believe. "Moving is not necessarily working." Manpower reduction means raising the value-added ratio — ideally toward 100%.

**Waste generating waste — the secondary cascade**
Excess inventory triggers a chain of secondary wastes. One unit of overproduction:
→ needs storage → warehouse built → workers hired to carry goods → carts purchased → rust prevention staff needed → inventory management staff needed → computers purchased for inventory control → shortages discovered despite planned production → capacity expansion plan written → new equipment purchased → more inventory produced

Every link in this chain is a cost that appears in labor, depreciation, and overhead — with no corresponding value added. The cost of a single overproduction mistake can consume a year's profit margin.

**Machine value = earning power, not book value**
Accounting depreciation is a tax and reporting convenience. It has nothing to do with a machine's actual value to production. A 1920s machine maintained to near-100% operable rate is worth more than a last-year machine running at 50% operable rate. Replacing a well-maintained old machine with a new one is always more expensive than maintaining the old one — if the maintenance has been adequate. Poor maintenance followed by replacement is paying twice for the same problem.

## Key Quotes

> "Moving is not necessarily working. Working means actually advancing the process toward completing the job."

> "Speed is meaningless without continuity. Just remember the tortoise and the hare."

> "I frequently say management should be done not by arithmetic but by ninjutsu, the art of invisibility."

> "0.1 worker is still one worker." *(Fractional labor savings that don't eliminate a whole headcount save nothing.)*

## Management Observations

- **Send information just-in-time, not just-in-case.** Providing all processes with the full production schedule simultaneously induces exactly the early production you are trying to prevent. Information has the same inventory economics as parts.
- **Running a machine at 100% operating rate is not a goal.** It is a symptom of overproduction-oriented thinking. The goal is 100% operable rate (reliable when needed) at the operating rate set by takt time (no more).
- **Efficiency improvements that exceed required output are not improvements.** They are investments in future inventory problems. True cost reduction requires tying efficiency to demand, not to machine or worker capability.
- **Secondary waste is invisible until it isn't.** Warehouses, inventory management staff, and computer systems appear as legitimate organizational costs. Their root cause — overproduction — is never visible in the budget line that funds them.
