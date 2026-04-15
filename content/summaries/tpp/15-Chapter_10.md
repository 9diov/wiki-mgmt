---
related-concepts:
  - "[[The Brent Problem ⭐]]"
  - "[[The Four Types of Work ⭐]]"
  - "[[Change Advisory Board (CAB)]]"
sources:
  - "[[15-Chapter_10_•_Thursday,_September_11|Chapter 10 — Thursday, September 11]]"
---

# Chapter 10

## What Happens

In the daily Phoenix stand-up, Kirsten calls Brent's name three times for overdue tasks. QA reports that broken features are being discovered twice as fast as they're being fixed. Sarah publicly questions whether Wes has personnel issues to address.

Bill goes directly to Brent's desk to observe rather than interrogate. He watches Brent work for several minutes without interrupting: one call about a database sync problem, another call about a downed service — both from IT colleagues who need help resolving incidents. When someone mentions the VP of Logistics is threatening stock-outs in stores, Brent drops what he's doing and spends thirty minutes on that too. He has three Post-it notes on his monitor tracking open problems.

Bill sits down with Brent and lays out the situation: five Phoenix tasks are late, all assigned to him. Brent says he's already half done with them and just needs two hours of uninterrupted time. He acknowledges the calls come from colleagues who can't solve things without him and confirms he logs nothing in the ticketing system because opening a ticket takes longer than fixing the problem.

Bill issues the directive: Brent works Phoenix only. Anyone calling about anything else gets redirected to Wes. Bill will have his assistant change Brent's voicemail greeting immediately.

Back with Wes and Patty, Bill proposes a structured solution to the Brent problem:

- A **level 3 engineer pool** of three engineers handles all escalations — Brent is excluded from this pool
- Access to Brent requires approval from Wes or Bill first
- When Brent is brought in, he **cannot touch the keyboard** — he tells the level 3s what to type
- Every session with Brent must be documented; the fix goes into the knowledge base
- Brent cannot work the same problem twice — if he does, the level 3 engineer responsible is accountable
- Daily timesheets from Brent; every escalation logged in the ticketing system
- Carrot: Brent gets a full week off, completely free of escalation duties — the first time in three years

Wes tells a story that explains why documentation is so hard: during a three-hour Sev 1 outage, the team finally brought Brent in as a last resort. He sat down, went into what Wes describes as a trance, and fixed the problem in ten minutes. When someone asked how he did it, Brent said: *"I have no idea. I just did it."* Patty raises the possibility that Brent's knowledge concentration might be partly self-protective — consciously or not.

Bill's formulation: *"Every time that we let Brent fix something that none of us can replicate, Brent gets a little smarter, and the entire system gets dumber."*

---

## What the Chapter Reveals

Chapter 10 is the Brent Problem's first structured response. Every previous chapter named the problem; this one builds the operational design to contain it.

The "no keyboard" rule is the sharpest insight. Brent's fixes are invisible when he works alone — he produces outcomes without producing knowledge. Forcing him into a coaching role, where a level 3 engineer executes every step under his direction, converts his tacit knowledge into documented procedure. The fix that was previously a mystery becomes a repeatable runbook entry.

The level 3 pool design also addresses the second dimension of the problem: the organization's learned helplessness. Every time Brent fixes something nobody else can, the incentive to develop that capability elsewhere decreases. The pool structure forces the skill-building to happen, because Brent is no longer available as the fallback.

---

## Management Observations

- **Observing before acting is the right first move.** Bill watches Brent's desk for several minutes without announcing himself. He sees the actual pattern — colleagues calling directly, no ticket logging, problems solved but knowledge not transferred — rather than relying on secondhand accounts. His conversation with Brent is calibrated by what he actually witnessed, not by Kirsten's list of late tasks.
- **"Every time Brent fixes something we can't replicate, Brent gets smarter and the system gets dumber."** This is the chapter's central formulation. The knowledge is not lost — it is just trapped in one person. The organization's collective capability does not grow when Brent solves problems alone. It only grows when the fix is understood, documented, and reproducible by others.
- **The "no keyboard" rule converts a constraint into a training mechanism.** Brent as coach rather than operator is not a demotion — it is the design that simultaneously protects his time, transfers his knowledge, and builds the level 3 pool's capability. The constraint is being exploited in the Theory of Constraints sense: making the bottleneck produce organizational value rather than individual heroics.
- **Patty's observation about knowledge as power is important but secondary.** Whether or not Brent is consciously protecting his position, the structural incentives produce the same behavior either way. The fix is not to change Brent's motivations but to change the system so that knowledge transfer is the only path through the constraint.
- **Logging Brent's time and escalations serves two purposes.** First, it makes the demand on Brent visible — the same visibility function that the change cards served. Second, it creates accountability: anyone consuming Brent's time must justify it, which will reduce casual escalations that currently arrive without friction or consequence.
