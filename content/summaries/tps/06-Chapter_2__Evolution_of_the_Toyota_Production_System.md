---
related-concepts:
  - "[[Five Whys ⭐]]"
  - "[[Seven Wastes (Muda) ⭐]]"
  - "[[Standard Work]]"
  - "[[Pull System and Kanban ⭐]]"
  - "[[Production Leveling (Heijunka)]]"
sources:
  - "[[06-Chapter_2__Evolution_of_the_Toyota_Production_System|Chapter 2 — Evolution of the Toyota Production System]]"
---

# Chapter 2: Evolution of the Toyota Production System

## Core Argument

Every element of TPS was derived from asking "why" repeatedly until a real cause appeared, then building a countermeasure from necessity. This chapter traces that derivation: Five Whys as the scientific method behind TPS, the seven wastes as the taxonomy it produced, standard work as the discipline that holds it together, and kanban as the tool that makes it run — along with the candid account of how 10 years of resistance and expansion were required to make it work.

## Key Ideas

**[[Five Whys ⭐]] — the scientific foundation of TPS**
Ohno opens the chapter with a machine stoppage: why did it stop? Blown fuse. Why? Overloaded bearing. Why? Insufficient lubrication. Why? Pump shaft worn. Why? No strainer — metal scrap got in. Replace the fuse and the problem recurs in months. Replace the strainer and it is solved permanently. Ohno's claim: the entire Toyota production system was built by repeatedly applying this logic.

The same method derived TPS's core components:
- *"Why can one Toyota operator run one machine while a Toyoda textile worker runs 40–50 looms?"* → machines don't stop themselves → autonomation
- *"Why can't we make this part just-in-time?"* → earlier process makes them without knowing what's needed → production leveling
- *"Why are we making too many parts?"* → no mechanism to prevent overproduction → visual control → kanban

**[[Seven Wastes (Muda) ⭐]] — the complete taxonomy**
The preliminary step of TPS is identifying all waste. Ohno names seven categories:

1. Waste of overproduction
2. Waste of time on hand (waiting)
3. Waste in transportation
4. Waste of processing itself
5. Waste of stock on hand (inventory)
6. Waste of movement
7. Waste of making defective products

The key equation: *present capacity = work + waste*. True efficiency improvement means bringing waste to zero — not running faster, but eliminating non-work entirely. Reducing two workers from a ten-person line that produces 100 units/day doesn't reduce output; it reveals that the capacity to produce those 100 units existed with 8 people all along.

**[[Standard Work]] — the visible foundation**
Standard work sheets are posted at every workstation and define three elements:
1. **Cycle time** — time allotted per unit, derived from required quantity and available operating time (takt time in practice)
2. **Work sequence** — the order of operations a worker performs (not the order of the production flow)
3. **Standard inventory** — the minimum WIP needed to keep work flowing through the process

Standard work makes abnormalities visible: if a worker cannot complete the sequence within cycle time, something is wrong. It is the baseline from which all improvement is measured.

**[[Pull System and Kanban ⭐]] — rules and implementation**
Kanban has six rules:
1. The later process picks up only what is needed, when needed
2. The earlier process produces only the amount withdrawn
3. Nothing is produced or moved without a kanban
4. A kanban must accompany all goods
5. Defective products are never sent to the next process
6. The number of kanbans is reduced over time

Rule 6 is the improvement engine: reducing kanbans reduces authorized inventory, which reduces the tolerance for disruptions, which forces problems to be solved. *"Kanban accelerates improvements"* — a plant with large kanban counts tolerates large problems; a plant with small counts cannot.

**The 10-year rollout — implementation is not adoption**
Kanban was not decreed; it was expanded step by step within Ohno's growing sphere of authority. Machine shop (1949) → Motomachi plant (1959) → company-wide (1962) → first suppliers (1963). It took nearly 20 years from conception to full external deployment. Key reason for caution: *"If used for picking up parts ordered from outside without first changing the production method within the company, kanban immediately becomes a dangerous weapon."* Flow must be established before kanban is introduced — kanban manages flow, it does not create it.

**[[Production Leveling (Heijunka)]] — the pre-condition for kanban**
Leveling is not a scheduling preference; it is the physical pre-condition for pull systems. Without level withdrawal, earlier processes must hold large inventories of every item to avoid stockouts when the later process suddenly demands a surge. The Tsutsumi plant demonstrates this in practice: Corona and Carina interleaved on the same line, with mixed-model sequencing (sedan-hardtop-sedan-wagon) minimizing batch sizes at every upstream process. Die setup time fell from 2–3 hours in the 1940s to 3 minutes by the late 1960s — the consequence of needing small lots.

## Key Quotes

> "To tell the truth, the Toyota production system has been built on the practice and evolution of this scientific approach. By asking why five times and answering it each time, we can get to the real cause of the problem, which is often hidden behind more obvious symptoms."

> "Present capacity = work + waste."

> "A half-hearted introduction of kanban brings a hundred harms and not a single gain."

## Management Observations

- **Root cause analysis is not optional.** Fixing symptoms (replacing a fuse) costs time and recurs. Fixing root causes (installing a strainer) costs more once and eliminates the problem. The five-why discipline forces the deeper fix every time.
- **Efficiency improvements that don't reduce headcount or cost aren't improvements.** Running faster while maintaining the same manpower just produces more inventory. Real efficiency means making the same output with fewer inputs — or more output with the same inputs.
- **Transformation takes years and requires expanding authority.** Ohno could only implement kanban where he had direct control. He waited until his authority expanded before expanding the system. Attempting company-wide rollout from the beginning would have failed.
- **Kanban is a diagnostic tool, not just a scheduling system.** Each time a line stops because a kanban wasn't available, a problem is exposed. The correct response is to fix the problem, not add more kanbans.
