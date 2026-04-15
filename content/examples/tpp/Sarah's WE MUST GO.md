---
related-concepts:
  - "[[The Point of No Return]]"
  - "[[Throwing the Pig Over the Wall]]"
sources:
  - "[[17-Chapter_12_•_Friday,_September_12|Chapter 12 — Friday, September 12]]"
---

# Sarah's "WE MUST GO!"

## The Setup

At 7:45 p.m. on Phoenix deployment night, with the code still not running in the test environment, Bill sends an urgent email to Steve, Sarah, and Chris recommending a one-week delay. He describes the situation as a "near-certain disaster" comparable to the 1999 Toys R Us Thanksgiving outage. He sends it marked highest priority and calls Steve immediately after.

Steve's response: the marketing ads have been printed and distributed to homes across the country. The partners are lined up. *"If you can convince Sarah to postpone the rollout, let's talk. Otherwise, keep pushing."*

Bill finds Sarah in the Phoenix war room and makes the case in person — the same case he made to Steve. Her response: *"Everyone is ready but you. Perfection is the enemy of good. We've got to keep going."*

Her email reply arrives minutes later:

> *Everyone is ready but you. Marketing, Dev, Project Management all have given this project their all. Now it's your turn.*
>
> **WE MUST GO!**

Bill resists the urge to reply.

## What It Illustrates

**[[The Point of No Return]]** — Sarah's email is the organizational point of no return, and it arrived before the technical one. The marketing ads, the partner commitments, the public announcements — these were upstream decisions that made reversal feel politically impossible by deployment night. When Bill asked Steve to delay, Steve redirected him to Sarah. When Bill asked Sarah, she had already defined the situation as IT's problem to solve. The window for a decision about whether to proceed had, in practice, already closed before the deployment started.

The three-line email also captures the accountability asymmetry precisely. Sarah's framing — "everyone is ready but you" — treats the deployment's readiness as binary: either IT delivers or IT fails. The risks Bill had named (multiday outages, data integrity, customer transactions) are not addressed in the reply, only dismissed. If the deployment succeeds, the credit belongs to the teams that were "ready." If it fails, the failure belongs to IT Operations, which was the last team to say it wasn't ready.

**[[Throwing the Pig Over the Wall]]** — The email is the moment when the pig lands. Sarah has declared that the pig is over the wall and it is now IT's turn. Whether the pig can survive the landing is a question that will be answered over the next 36 hours.
