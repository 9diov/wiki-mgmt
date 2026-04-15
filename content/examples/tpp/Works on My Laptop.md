---
related-concepts:
  - "[[Throwing the Pig Over the Wall]]"
  - "[[Uncontrolled Change ⭐]]"
sources:
  - "[[17-Chapter_12_•_Friday,_September_12|Chapter 12 — Friday, September 12]]"
---

# "Works on My Laptop"

## The Setup

It's 7:30 p.m. on Phoenix deployment night. Operations and QA teams have been working since 4 p.m. trying to get the Phoenix code to run in the test environment. It won't come up cleanly. Critical tests are failing. Engineers are scouring server settings, database configurations, and OS versions trying to identify what the test environment is missing.

A developer walks into the room. He looks at the chaos, looks at the failed test results, and says:

*"Look, it's running on my laptop. How hard can it be?"*

Wes starts swearing. Two Operations engineers and three QA engineers immediately begin poring through the developer's laptop, trying to find what makes it different from the test environment.

It takes them over twenty minutes — while the deployment slips further — to identify and narrow down the discrepancy.

## What It Illustrates

**[[Throwing the Pig Over the Wall]]** — The developer's statement is offered helpfully. It is also the precise definition of the handoff gap: "running on my laptop" and "running in production" are treated as the same condition. The developer's environment has whatever it needs — specific library versions, open ports, local configuration, environment variables — that were never documented, never specified, and never communicated to the team responsible for running the code everywhere else.

This is the pig over the wall: code that works in the environment it was built in, handed to Operations to run in an environment no one fully specified. The developer is not being careless — he genuinely believes the problem should be simple, because for him it is. The gap between his mental model and the production environment is the gap that the handoff process was supposed to close and didn't.

The moment also captures the asymmetry of blame: when the deployment fails, Operations carries the incident. When the code "works on my laptop," Development considers its job done. Nothing in the process makes the environmental gap Development's problem to solve.
