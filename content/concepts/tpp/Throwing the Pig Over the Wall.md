---
concept-type: "[[Framework]]"
description: The pattern where Development declares work complete at code-done and hands off to Operations without specifications, production requirements, or shared ownership of deployment — leaving Ops to absorb all risk and late-stage work under an immovable deadline.
related-concepts:
  - "[[The Brent Problem ⭐]]"
  - "[[Uncontrolled Change ⭐]]"
  - "[[Change Advisory Board (CAB)]]"
  - "[[The Point of No Return]]"
sources:
  - "[[09-Chapter_4_•_Wednesday,_September_3|Chapter 4 — Wednesday, September 3]]"
  - "[[17-Chapter_12_•_Friday,_September_12|Chapter 12 — Friday, September 12]]"
aliases:
  - Dev/Ops Handoff Gap
---

# Throwing the Pig Over the Wall

Bill names the pattern in Chapter 4 after Chris Allers volunteers a Phoenix go-live date of September 12 without consulting Operations:

> *"You can't just throw the pig over the wall to us, and then high-five each other in the parking lot, congratulating yourselves on how you made the deadline. Wes is telling us that the pig will probably break its leg, and it'll be my guys who work all-nighters and weekends to keep that pig alive."*

The "pig" is the application. Development finishes building it, declares victory, and transfers ownership to Operations — at which point the pig must somehow run in production, under real load, with real data, on infrastructure that was never specified during development.

## What Gets Left Out of the Handoff

By the time of the Chapter 4 meeting, Operations still does not have:

- A hardware specification (what servers, how many, what configuration)
- Performance requirements validated against actual code behavior (the code runs at 4 TPS; the target is 250 TPS)
- A production environment design
- A test environment to validate deployment procedures
- Monitoring and backup requirements
- Any documented runbook for operating the system once live

Wes: *"Newborn babies dropped off at church doorsteps have more operating instructions than what they're giving us."*

## Why It Persists

The handoff gap is structural, not personal. Development and Operations are measured on different things:

- **Development** is measured on feature delivery and deployment dates. Once code ships, the job is done.
- **Operations** is measured on uptime and stability. They own whatever breaks after deployment.

When there is no shared accountability for what happens between "code done" and "running in production," that gap belongs to no one — until something breaks, at which point it belongs entirely to Operations.

The pattern is reinforced by schedule pressure. As deadlines compress, the time available for joint planning, environment specification, and testing is cut first — these are seen as optional polish, not required work. Operations is expected to compensate for whatever was cut.

## The Consequence

A rushed deployment to an underspecified production environment produces instability after launch. Operations then provides heroic support — all-nighters, reboots, patches — to keep the system alive. This heroism is invisible to everyone who declared success at the handoff, which removes any feedback signal that the handoff process needs to change.

The book's argument: the gap between Development and Operations is not a people problem. It is a process and organizational design problem. Closing it requires joint ownership of the deployment pipeline — both teams responsible for the outcome, not just their respective pieces.

## The Pattern at Full Scale (Chapter 12)

The Phoenix deployment on September 12 is the complete illustration of the pig-over-the-wall pattern. Every category of missing information from Chapter 4 is still missing on deployment night:

- **No deployment runbook**: Operations had to discover the production environment requirements — including a required firewall port — through failed attempts during the deployment itself, not from documentation provided in advance.
- **No version control discipline**: Development continued sending individual changed files rather than full packages during the deployment window. QA lead William: *"Even if by some miracle Phoenix does pass the smoke test, I'm pretty sure we wouldn't be able to replicate it, because there are too many moving parts."*
- **No load testing of the database conversion**: The conversion script had never been run at production data volume. On the night, it ran a thousand times slower than expected. By the time the failure was discovered, the point of no return had already been crossed.
- **No POS fallback playbook**: When 120 stores opened with systems offline, no one in Operations or Retail had a prepared communication for store managers. Maggie improvised an email with stores already opening on the East Coast.
- **No performance testing at scale**: The application required server reboots every few hours to manage a memory leak. This behavior was unknown until live customer load was present.
- **A session bug that exposed credit card numbers** — discoverable in testing — was instead discovered by customers on Twitter.

Development had been making changes during the deployment itself, continuing to send releases while Operations was still trying to get the test environment stable. The handoff was not a handoff — it was a concurrent development and deployment happening simultaneously, with Operations absorbing all operational risk for code that was still being written.
