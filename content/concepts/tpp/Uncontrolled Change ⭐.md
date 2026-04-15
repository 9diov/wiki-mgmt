---
concept-type: "[[Framework]]"
description: Changes entering production without visibility, coordination, or review are the primary cause of IT instability — not hardware failure, not developer incompetence, but untracked modifications to a system nobody has a complete picture of.
related-concepts:
  - "[[Change Advisory Board (CAB)]]"
  - "[[The Brent Problem ⭐]]"
  - "[[Throwing the Pig Over the Wall]]"
sources:
  - "[[08-Chapter_3_•_Tuesday,_September_2|Chapter 3 — Tuesday, September 2]]"
  - "[[09-Chapter_4_•_Wednesday,_September_3|Chapter 4 — Wednesday, September 3]]"
---

# Uncontrolled Change

Every incident in the opening chapters of The Phoenix Project traces back to a change that entered production without coordination:

- **Tokenization deployment (Ch. 3):** John's security team deployed a PCI compliance fix directly to the timekeeping database without going through the change process, without testing, and without telling Operations. The SSN field was corrupted; payroll failed for all hourly employees.
- **SAN firmware upgrade (Ch. 3):** A long-deferred firmware upgrade was attempted without an adequate maintenance window. When it went wrong, the rollback bricked the SAN entirely, taking down hundreds of dependent systems.
- **Patch Tuesday laptops (Ch. 4):** A routine security patch rollout crashed over 200 laptops company-wide. No staging, no warning, no coordination with the people whose machines would be affected.

None of these were acts of sabotage or negligence. Each was a legitimate, well-intentioned change made by competent people — for compliance, for performance, for security. The damage came from the absence of any system that would let the right people know what was changing, when, and what to watch for.

## Why Changes Go Uncoordinated

The root cause is not indiscipline — it is that the coordination mechanism is too slow to be usable. When the formal change process quotes a four-month deployment window and the auditors arrive next week, the rational actor bypasses the process. The process fails not because people are lazy but because it was designed without regard for the speed at which real work needs to move.

The result is a system where no one has a complete picture of what is running in production. When something breaks, the only way to reconstruct what changed is to email everyone in IT and ask. Patty describes this as the default state: "the left hand rarely knows what the right hand is doing."

## The Compound Effect

Uncontrolled changes compound in two directions:

1. **Direct:** A change breaks something. The fix requires taking a key engineer (Brent) off other work. That other work (Phoenix) slips. The slip creates deadline pressure. Deadline pressure produces more rushed, uncoordinated changes.

2. **Diagnostic:** Because changes aren't logged, reconstructing the cause of a failure requires investigation rather than lookup. Every incident takes longer to diagnose, which keeps key engineers absorbed in incidents longer, which causes more work to pile up unattended.

## The Change Management Response

The Change Advisory Board (CAB) is the institutional mechanism for making change visible. Its failure to take hold in previous attempts at Parts Unlimited illustrates the second half of the problem: a change coordination process that imposes too much overhead will be abandoned. The goal is not bureaucracy — it is a lightweight, fast mechanism that makes all production changes visible before they happen, so that conflicts and risks can be caught without slowing legitimate work to a halt.
