---
related-concepts:
  - "[[The Four Types of Work ⭐]]"
  - "[[Change Risk Tiers]]"
  - "[[Change Advisory Board (CAB)]]"
  - "[[The Brent Problem ⭐]]"
sources:
  - "[[14-Chapter_9_•_Tuesday,_September_9|Chapter 9 — Tuesday, September 9]]"
---

# Chapter 9

## What Happens

Bill is in a budget meeting when a Severity 1 alert fires: all credit card processing and order entry systems are down, affecting every store. He leaves the meeting and joins the incident call in the NOC.

The call immediately degenerates into finger-pointing. Each team — developers, database, networking, OS — denies making any relevant changes and deflects blame to the next group. Nobody can produce a timeline of what changed before the outage. Then a voice on the speakerphone quietly makes a change without announcing it — and the systems come back up. The voice is Brent. He likely caused the outage, silently undid it, and said nothing until someone on the call asked who just did that.

Bill pulls Wes and Patty aside. He issues two directives: Patty will begin every Severity 1 call with a timeline of all relevant changes, drawn from the change process she now controls — not from polling the room. And she will run practice incident calls and fire drills every two weeks so the discipline exists before the next emergency. For Wes: impress on Brent immediately that no changes happen during an outage without being announced and discussed first.

Two days later, Wednesday's CAB meeting runs with notable efficiency. The 437 change cards have been sorted, categorized, and scheduled. High-risk changes are reviewed in under 30 seconds each. Medium-risk changes — 90 of 147 ready to schedule — are reviewed by sampling. The process that took two hours to approve five changes in its first meeting now handles the week's full change inventory in a single session.

The problem Patty flags: 173 of the week's changes are scheduled for Friday — the same day as the Phoenix deployment. When she puts it on the board, engineers immediately start voluntarily moving their changes earlier in the week to avoid the collision. Within fifteen minutes the schedule is redistributed.

After the meeting clears, Bill stays behind staring at the change board. Something Erik said keeps surfacing. He works through it: the project inventory Patty built was one manual collection of work. The change cards on the board are another. He realizes: changes are the third type of work. Business projects are one type. IT infrastructure projects are another. Changes are a third.

He counts three. He wonders what the fourth is — and the chapter ends.

---

## What the Chapter Reveals

The chapter operates on two levels simultaneously.

At the operational level, two things mature: the incident response process gets its first structural fix (timeline-first, no silent changes), and the CAB reaches functional efficiency in its second real meeting — a process that was paralyzed by 437 cards one week earlier now runs smoothly because the triage design is working.

At the conceptual level, Bill makes his first independent discovery toward answering Erik's question. Watching Patty's staff physically move change cards around the whiteboard, he realizes he is looking at work being scheduled — discrete units of work, just like project tasks, but a different kind. The change cards are not projects. They are changes. A third type.

The fourth type — unplanned work — is not yet named. But its presence has been visible since Chapter 2: incidents, break-fix, firefighting. The four-type framework is one step from complete.

---

## Management Observations

- **The incident call finger-pointing is what happens without a timeline.** Every team's first move is self-defense because there is no shared, authoritative record of what changed. The CAB process Bill is building is not just an audit requirement — it is the mechanism that makes incident diagnosis possible without convening a blame committee. Patty owning the timeline at the start of every Sev 1 call converts the change process from a scheduling tool into a diagnostic tool.
- **Brent making an unauthorized change during an outage and not disclosing it is the Brent Problem at its most dangerous.** He acted alone, without coordination, during a live incident. He likely fixed it — but nobody knows what he did, which means nobody can verify it won't cause a worse failure later, document the root cause, or prevent a recurrence. The fix that leaves no trace is not a fix; it is a deferred mystery.
- **Practice drills are the right response to the incident call chaos.** Bill's instinct — biweekly fire drills before a real emergency, not after — mirrors the military logic he carries from the Marines. Discipline under pressure requires rehearsal. A team that has never run a structured incident call will not spontaneously become disciplined when the business is down.
- **The change board making collisions visible is the CAB's first proactive contribution.** Until this week, 173 changes colliding with a major deployment on the same day would have been invisible — each engineer would have proceeded independently, unaware of the others. Seeing the Friday column on the whiteboard crowded with cards, and watching engineers voluntarily move their work earlier, is the first evidence that the change process is producing the situational awareness it was designed for.
- **Bill's insight about changes as a third work type is the chapter's quiet turning point.** He arrives at it not from Erik's lecture but from watching a physical process — cards moving on a board. The taxonomy is emerging from observation, not instruction. This mirrors how the book builds its argument: the framework is validated by what Bill sees, not just by what Erik tells him.
