---
concept-type: "[[Practice]]"
description: A root-cause analysis technique — ask "why" five times in succession to move from symptom to underlying cause, then fix the cause rather than the symptom.
related-concepts:
  - "[[Seven Wastes (Muda) ⭐]]"
  - "[[Standard Work]]"
  - "[[Autonomation (Jidoka) ⭐]]"
sources:
  - "[[06-Chapter_2__Evolution_of_the_Toyota_Production_System|Chapter 2 — Evolution of the Toyota Production System]]"
aliases:
  - 5 Whys
  - Five Why Analysis
---

# Five Whys

A problem-solving discipline at the core of how TPS was built and how it is maintained. When a problem occurs, ask "why" and answer it. Then ask "why" again of that answer. Repeat five times. The fifth answer is typically the root cause — the one whose correction actually prevents recurrence.

## The Machine Stoppage Example

Ohno's canonical illustration:

1. Why did the machine stop? — The fuse blew due to overload.
2. Why was there an overload? — The bearing was not sufficiently lubricated.
3. Why was lubrication insufficient? — The lubrication pump was not pumping enough.
4. Why wasn't it pumping enough? — The pump shaft was worn and rattling.
5. Why was the shaft worn? — No strainer was attached; metal scrap got in.

**Countermeasure:** attach a strainer to the pump.

Stopping at the first why (replace the fuse) or even the second (replace the pump shaft) allows the problem to recur within months. Only reaching the fifth why produces a durable fix.

## Why Five?

Five is not a magic number — it is a minimum threshold for the discipline. Most symptoms have three to four levels of cause between them and the actual root. One or two whys almost always land on a proximate cause, not a root cause. The discipline of asking five forces the team to go deeper than is comfortable.

In practice, different chains have different depths. The point is the habit of not stopping at the first plausible answer.

## How TPS Was Derived From It

Ohno credits five-why thinking as the scientific foundation of the entire Toyota Production System:

- *Why can one Toyota operator run one machine while a Toyoda textile worker runs 40–50?* → machines don't stop themselves on completion → **autonomation**
- *Why can't we make this part just-in-time?* → earlier processes make at their own rate without knowing downstream need → **production leveling**
- *Why are we making too many parts?* → no mechanism exists to prevent overproduction → **visual control** → **kanban**

Each of these was not a design decision — it was a diagnosis followed by a countermeasure.

## Application Beyond Machines

Five Whys applies to any problem where a symptom is visible but a cause is not: defects, delays, cost overruns, customer complaints. The discipline is the same: each "why" must be answered with a specific, verifiable fact, not a general observation. *"The process is inefficient"* is not an answer. *"The operator waits 30 seconds between cycles for the upstream machine to complete"* is an answer.

## The Managerial Implication

Managers who accept the first answer to "why" will spend their careers replacing fuses. The instinct to fix the visible problem quickly is natural and often rewarded in the short term. Five Whys is a commitment to the slower, more uncomfortable process of finding what is actually wrong — and fixing it once.
