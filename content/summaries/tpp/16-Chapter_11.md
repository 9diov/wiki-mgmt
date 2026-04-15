---
related-concepts:
  - "[[The Brent Problem ⭐]]"
  - "[[The Four Types of Work ⭐]]"
  - "[[Change Advisory Board (CAB)]]"
  - "[[The Three Ways ⭐]]"
sources:
  - "[[16-Chapter_11_•_Thursday,_September_11|Chapter 11 — Thursday, September 11]]"
---

# Chapter 11

## What Happens

Patty calls Bill into the Change Coordination Room with alarming news: 60% of the scheduled changes from Monday and Tuesday were never completed. Her team has been closing out change cards at the end of each day, tracking completions and incidents — and the majority of authorised changes aren't getting done.

The reasons she's collected from change requesters are varied: dependencies that weren't in place, an outage in progress blocking the window, a storage expansion that wasn't finished in time. But the most common reason is Brent — either his involvement was planned and he wasn't available, or engineers discovered mid-change that they needed him and had to abort.

The arithmetic is alarming. 240 incomplete changes from this week, plus 400+ incoming next week, equals 640 changes on the schedule. At 60% incompletion, that number compounds: within weeks they'll be carrying thousands of incomplete changes. Patty is already tracking 942. The change cards are physically running out of space on the whiteboards.

Bill pulls Wes in. Wes's first instinct is to let Brent help with changes again. Bill rejects it — that would mean the blocked changes are more important than Phoenix, and they aren't.

Standing at the change board, staring at the pile-up, Bill makes the connection to Erik's plant visit. The cards piling up in front of Brent's invisible dependency are the same as inventory piling up in front of the heat treat oven. Brent is the constraint. The CAB is Mark — the job release desk authorising work into the system faster than the constraint can consume it.

The critical realisation: the CAB has been authorising changes without ever asking whether Brent was in the path of those changes. Work has been released into the system against a constraint nobody was tracking.

Bill doesn't reverse the policy. Instead he makes the constraint visible: Patty will flag every change card that has a Brent dependency, inventory them, triage them with the level 3 engineers, and report back. For the first time, the system will know how much work is queued against the bottleneck before that work is released.

Bill's formulation: *"It's because of this process that, for the first time, we're even aware of how much scheduled work isn't getting done. Getting rid of the process would just kill our situational awareness."*

The chapter ends with Bill wondering aloud to Wes — if Erik was right about WIP in IT, what else was he right about?

---

## The Conceptual Turn

Chapter 11 is where the manufacturing analogy stops being an analogy and becomes a diagnosis. The specific parallel Bill draws:

- **Heat treat oven = Brent** — the constraint that everything must pass through
- **Mark at the job release desk = the CAB** — releasing work into the system based on first availability, not bottleneck capacity
- **Inventory piled in front of the oven = 942 pending change cards** — WIP accumulating because the constraint can't absorb the release rate

The insight is not just that Brent is overloaded — that has been visible since Chapter 2. The insight is that the CAB, by authorising changes without tracking Brent dependencies, has been making the problem worse. The job release mechanism has been running blind to the constraint it feeds.

The solution is not to release less work or to ignore the constraint — it is to make the constraint visible at the point of release, so work can be sequenced against actual bottleneck capacity.

---

## Management Observations

- **The 60% incompletion rate is not a process failure — it is the process revealing a previously invisible problem.** Before the change process existed, these changes were attempted and failed silently, with no tracking and no data. The CAB didn't create the incompletion rate; it made it measurable for the first time. Patty's instinct to question whether the process is worth running is understandable but precisely backwards.
- **Protecting Brent from break-fix while releasing Brent-dependent changes is internally inconsistent.** Both policies were correct individually. Together, they created a new failure mode: changes scheduled against a constraint that had been removed from the pool. The system optimised one part without updating the other. This is the local optimisation trap in practice.
- **Flagging Brent-dependent changes on cards is constraint-aware scheduling.** It is the IT equivalent of Goldratt's directive: don't release work into the system faster than the constraint can consume it. The specific mechanism — a coloured card or an extra field — is less important than the principle: make the bottleneck dependency visible before authorising the work, not after discovering it mid-change.
- **The compounding arithmetic of incomplete WIP is the chapter's sharpest warning.** 240 incomplete changes plus 400 new ones equals 640 next week. At a sustained 60% incompletion rate, the number crosses 1,000 within days, then grows faster as the incomplete backlog itself generates dependencies and conflicts. WIP is not a linear problem — it compounds, exactly as Erik described inventory compounding on the plant floor.
- **Bill's Post-it note on the docking station is the chapter's quiet mirror.** He writes "DO NOT INSERT LAPTOP UNTIL POWERED ON" to prevent his own repeated mistake — a self-imposed countermeasure against a known failure mode. The same logic applied to the change process: make the constraint visible at the point of action, before the mistake is made.
