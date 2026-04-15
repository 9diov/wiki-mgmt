---
related-concepts:
  - "[[Change Advisory Board (CAB)]]"
  - "[[Uncontrolled Change ⭐]]"
  - "[[The Brent Problem ⭐]]"
sources:
  - "[[11-Chapter_6_•_Friday,_September_5|Chapter 6 — Friday, September 5]]"
---

# Chapter 6

## What Happens

In a Phoenix status meeting, Bill learns that developers are deferring almost all testing to after deployment — which means the production environment will be the test environment.

Patty and Wes present the work inventory analysis commissioned in Chapter 5. The numbers are worse than feared:

- **35 major business projects** tracked by the PMO, each with IT commitments
- **70+ internal IT projects** with no central list — the number keeps growing as interviews continue
- At roughly 150 IT Operations staff, that's already approaching one project per person
- **Compliance remediation** would consume all key resources for an **entire year** if worked exclusively
- **Break-fix and incident work** currently absorbs **75% of staff time** and automatically takes priority over project work

During the interview process itself, Brent was pulled away twice by a SAN outage — a drive running without redundancy for months after a prior failure, blocked in Procurement for replacement parts. Bill erupts: preventive maintenance should have caught this. He demands daily SAN log checks from a junior engineer and schedules a dedicated meeting to reduce break-fix volume.

At the Friday CAB meeting, fourteen technical leads show up — a full room. But it opens with Wes and Patty in a shouting match over a past engineer termination, with John sitting uninvited in the back, inflaming things. Bill defuses it with his broken antique laptop (battery falls off on impact) and refocuses the room.

The tool-based process collapses immediately: too many mandatory fields, dropdown boxes that don't match reality, a 64-character text field for hundreds of server names. Wes's team marks everything "urgent" to get attention; Patty's team creates three-week approval backlogs in response.

Bill scraps the tool entirely. He brings index cards — one change per card, three fields only: who, what system, one-sentence summary. A whiteboard calendar for scheduling. After 30 minutes the group can't agree on the definition of a "change." After 90 minutes they have a working definition on the whiteboard. After two hours: five changes reviewed and approved.

Nobody except Bill is frustrated by the pace. Engineers are vigorously debating risks and discover one change that wasn't even necessary. People leave saying it was a great meeting. Patty stays behind, upset that years of policy work is being discarded. Bill acknowledges the effort and asks her to write the new simplified process herself.

That afternoon Patty calls: 243 change cards already submitted, more arriving over the weekend, expecting over 400 total for the following week. Bill declines to freeze changes — that would kill the momentum. Decision: submit by Monday, Monday's changes don't need pre-authorization, everything after requires approval.

---

## What the Chapter Reveals

The resourcing analysis lands the full scope of the capacity problem in a single spreadsheet:

- **Phoenix + compliance + break-fix already exceeds 100% of available capacity.** These three demands alone outrun supply, before the 70+ internal projects or 35 business projects are even counted. The organization has been making commitments against capacity that doesn't exist.
- **Break-fix consuming 75% of time is the core constraint.** Project work — Phoenix, audit remediation, infrastructure upgrades — cannot reliably happen because unplanned work continuously preempts it. IT is operating in permanent reactive mode, with only 25% of capacity available for anything planned.
- **400 unreviewed changes per week is the baseline state.** The index card exercise reveals something important: the change volume was always this high — it was just invisible. Nobody knew what was changing in production week to week because nothing was written down. The CAB exercise didn't create the problem; it made the existing problem visible for the first time.

---

## Management Observations

- **Scrapping the tool was the right call, but Patty's reaction names the real cost.** Years of legitimate process design work was abandoned because it was too cumbersome to use. A process nobody uses provides zero value; a process everyone uses imperfectly provides more value than a perfect process nobody follows. Starting with index cards and a whiteboard is the minimum viable version of change visibility.
- **The definition problem is not trivial.** Thirty minutes to define "change" is not a sign the meeting is failing — it is exactly the right conversation. Without a shared definition, every engineer applies their own judgment about what warrants review. The whiteboard definition is the first organizational agreement about what change management is actually for.
- **Bill's instinct not to freeze changes is correct.** Halting all changes while the backlog gets reviewed would demonstrate that the process is an obstacle to work. The early momentum — people voluntarily submitting cards, engaging in risk discussions, saying the meeting was useful — is more valuable than procedural completeness. Goodwill is the prerequisite for a functional process.
- **The 75% break-fix figure points to the book's central argument.** If unplanned work consumes three-quarters of capacity, the primary management challenge is not planning better — it is reducing the volume of unplanned work. That requires understanding what generates it: fragile systems, missing preventive maintenance, uncoordinated changes. The Brent Problem and the change management problem are both symptoms of the same underlying condition.
