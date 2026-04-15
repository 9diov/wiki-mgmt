---
concept-type: "[[Practice]]"
description: The institutional mechanism for making all production changes visible before they happen — a scheduled review where technology teams log upcoming changes, surface conflicts, and get authorization, so the left hand knows what the right hand is doing.
related-concepts:
  - "[[Uncontrolled Change ⭐]]"
  - "[[The Brent Problem ⭐]]"
  - "[[Throwing the Pig Over the Wall]]"
  - "[[Change Risk Tiers]]"
  - "[[Work in Process (WIP) ⭐]]"
sources:
  - "[[08-Chapter_3_•_Tuesday,_September_2|Chapter 3 — Tuesday, September 2]]"
  - "[[09-Chapter_4_•_Wednesday,_September_3|Chapter 4 — Wednesday, September 3]]"
  - "[[13-Chapter_8_•_Monday,_September_8|Chapter 8 — Monday, September 8]]"
  - "[[14-Chapter_9_•_Tuesday,_September_9|Chapter 9 — Tuesday, September 9]]"
  - "[[16-Chapter_11_•_Thursday,_September_11|Chapter 11 — Thursday, September 11]]"
aliases:
  - Change Management
  - Change Control
---

# Change Advisory Board (CAB)

Patty McKee owns the CAB at Parts Unlimited. Its purpose is to collect all planned production changes from every technology team, review them for conflicts and risks, and authorize deployment. In principle, no change enters production without CAB review.

In practice, as of Chapters 3–4, the CAB is non-functional. When Bill arrives at the scheduled meeting in Chapter 4, only Patty is there.

## The Failure History

The CAB at Parts Unlimited has collapsed twice:

**First attempt:** After years of incidents, the company brought in ITIL consultants, replaced the ticketing system with an ITIL-compliant change management tool, and ran a formal rollout. Engineers were required to submit change requests through the tool, where they would be routed for approvals. Within two years, nobody used it. The tool required 20 minutes to fill out forms for a 5-minute change. Engineers staged an informal rebellion. John (CISO) eventually stopped attending and stopped enforcing.

**Second attempt:** After the first collapse, the process was quietly abandoned. No formal second attempt was made — the system returned to the default state: changes made whenever, by whoever, without central visibility.

**Third attempt (Bill's reboot):** Following the payroll failure and SAN outage in Chapters 3–4, Bill mandates CAB attendance as a condition of employment and schedules a Friday meeting. Wes immediately calls to object, accurately describing the prior failure: *"My guys were spending half their time doing paperwork and sitting in that damned CAB meeting."*

## What Makes It Fail

The CAB fails when the friction it imposes exceeds the value it provides. Three failure modes are visible:

1. **Process too slow for real work.** A four-month queue for a change needed next week means people bypass the process. This is rational behavior, not indiscipline.
2. **No top-level enforcement.** When managers don't attend, their teams don't attend. Bill's observation: *"Efforts like this must start and be continually maintained from the top."*
3. **No feedback loop to the bypasser.** John bypassed the process, triggered a $1M+ incident, and experienced no personal consequence from the CAB failure. The process has no mechanism to make the cost of bypassing visible to the person who bypassed it.

## What It Needs to Do

The goal is not bureaucracy — it is visibility. A functional CAB answers one question before every production change: *does anyone else need to know about this?*

If a security engineer is tokenizing SSN fields in a timekeeping database on Monday evening, the Operations team running payroll Tuesday morning needs to know. The CAB is the mechanism that surfaces that conflict before the change, not after the incident.

The design challenge — which the book will explore further — is building a process fast enough that compliance is the path of least resistance, not an obstacle to getting work done.

## When the CAB Works (Chapters 8–9)

By Chapter 8's second real meeting, the three-tier design is in place and the results are measurable. High-risk changes that previously took ninety minutes to approve five are now reviewed in under thirty seconds each. Medium-risk changes are handled by sampling. The full week's 437 change inventory is processed in a single session.

Chapter 9 adds the CAB's most valuable operational contribution: **collision detection**. When 173 of the week's changes appear clustered on Friday — the same day as the Phoenix deployment — it is visible on the whiteboard before any of those changes are implemented. Engineers voluntarily move their changes earlier in the week. Without the change calendar, each team would have proceeded independently, with no awareness that their change was one of 173 landing simultaneously on the most critical day of the quarter.

The CAB also becomes the diagnostic foundation for incident response. Patty's new Sev 1 protocol requires her to open every incident call with a timeline of all recent changes drawn from the change system — converting the CAB from a scheduling tool into a root-cause tool.

## The Constraint-Blindness Failure (Chapter 11)

The CAB's first serious design limitation surfaces in Chapter 11. Patty's team discovers that 60% of scheduled changes are failing to complete — many because engineers discovered mid-change that they needed Brent and he was unavailable.

The CAB had been authorizing changes without tracking whether Brent was in their path. When Bill directed Brent to work Phoenix only (correct), the CAB continued releasing Brent-dependent changes for scheduling (not updated). Two correct policies created a new failure mode because neither was aware of the other's effect on the same constraint.

Bill's diagnosis maps directly to the plant floor analogy: the CAB is Mark at the job release desk, releasing work based on first-station availability without checking whether the bottleneck downstream can absorb it. The result is 942 pending changes — WIP piling at the constraint exactly as inventory piled at the heat treat oven.

The fix: flag Brent-dependent changes at submission time. The CAB must know a change requires Brent before authorizing it, so it can triage against actual constraint capacity. **The job release desk must be constraint-aware.**
