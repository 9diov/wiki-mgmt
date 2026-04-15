---
related-concepts:
  - "[[Change Advisory Board (CAB)]]"
  - "[[Uncontrolled Change ⭐]]"
  - "[[The Brent Problem ⭐]]"
sources:
  - "[[21-Chapter_16_•_Thursday,_September_18|Chapter 16 — Thursday, September 18]]"
---

# The Apollo 13 Incident Command

## The Setup

The customer invoicing system has failed silently for three days — no invoices sent, $50 million in receivables stuck, the CFO on the "window ledge." Bill assembles the team in the NOC conference room.

Patty opens by presenting all changes from the last 72 hours. Bill then addresses the room:

*"Do not touch anything without getting approval from me. This is not an outage we're dealing with here. We're in a situation where we could accidentally lose order entry or accounts receivable data. This is our Apollo 13 moment, and I'm Gene Kranz in Houston Mission Control. I don't want guesswork. I want hypotheses backed up with facts. Failure is not an option."*

By 6 p.m., twenty potential failure causes have been documented and narrowed to eight, each with an assigned owner. They reconvene at 10 p.m. Bill goes home for dinner.

His reasoning for the approach: during the payroll outage, someone started "screwing with the SAN" without understanding it was in the failure's causal chain. That action added six hours to the outage and nearly lost payroll data. More people doing more things faster is not a mitigation strategy in a system state you don't understand.

## What It Illustrates

**[[Uncontrolled Change ⭐]]** — The incident command approach applies the same logic as change management to the response itself. An uncoordinated "all hands on keyboards" response during an active failure is, functionally, a set of simultaneous uncontrolled changes to a production system in an unknown state. Each engineer doing their best guess in parallel creates new variables, new interactions, new potential failure modes. The CAB controls change entry before incidents; the incident command structure controls change entry during them.

**[[Change Advisory Board (CAB)]]** — Patty's opening move — presenting the 72-hour change timeline before any diagnosis begins — is the CAB's Sev 1 protocol functioning exactly as designed. The change board converts "what changed recently?" from a memory exercise into a lookup. This is the first diagnostic step every time, not because it always reveals the cause, but because it narrows the hypothesis space before anyone touches anything.

**[[The Brent Problem ⭐]]** — Steve's counter-pressure — "get Brent in, all hands on deck" — is the structural threat to this approach. Brent is individually faster at diagnosis than any process. But every time Brent is pulled in to fix something that others couldn't fix, the team learns nothing, documents nothing, and the next incident requires Brent again. The methodical approach is slower in the short term and faster in the long term; the escalate-to-Brent approach is the opposite.
