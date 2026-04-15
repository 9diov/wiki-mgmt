---
related-concepts:
  - "[[The Brent Problem ⭐]]"
  - "[[Work in Process (WIP) ⭐]]"
  - "[[Goldratt's Five Focusing Steps]]"
  - "[[Technical Debt]]"
  - "[[The Three Ways ⭐]]"
sources:
  - "[[25-Chapter_20_•_Friday,_September_26|Chapter 20 — Friday, September 26]]"
---

# Chapter 20

## What Happens

Three days into the project freeze, Kirsten's email confirms it is working: more progress in seven days than a typical month. Sarah is already arguing her projects are exempt. Bill shares the news with Wes and Patty.

The question Patty raises — what happens when the freeze is lifted? — exposes a deeper problem. Bill asks how the team currently decides what to work on when multiple projects are competing. Wes: "We trust smart people to make the right call." Patty: "Priority one is whoever yells loudest. Tiebreaker: who can escalate to the most senior executive. Some engineers just prioritize whichever manager takes them to lunch." There is no principled prioritization mechanism.

Bill calls Erik, then meets him at MRP-8.

Erik asks Bill to describe what he sees on the plant floor. When Bill answers "Brent is the constraint," Erik challenges him: Brent is a *worker*, not a work center. The work center is the combination of machine, man, method, and measures. A work center requires all four. Brent is a worker associated with too many work centers — *"Imagine if twenty-five percent of all the work centers down there could only be operated by one person named Brent."* That's the actual problem statement. The implication: the solution is to catalog which work centers depend on Brent, document those methods, and enable others to operate them.

Erik then introduces the concept of a bill of resources — the IT equivalent of a manufacturing bill of materials combined with routings. For each piece of work, it specifies all prerequisites: hardware specifications, software and license information, configurations, security requirements, capacity and continuity needs. This enables, for the first time, a real capacity-demand analysis before accepting work.

On lifting the freeze: release projects that don't require Brent first. Projects that do require Brent can only be released at Brent's available tempo. The monitoring project — which prevents outages and reduces future Brent dependencies — doesn't require Brent and actively elevates the constraint. Erik names this as Step 4 of the Five Focusing Steps. He connects it to Total Productive Maintenance: *"Improving daily work is even more important than doing daily work."* He cites Mike Rother's Improvement Kata — continuous improvement as deliberate habit-building through repetition. The Third Way.

Erik introduces the wait time formula from queueing theory: wait time = utilization% / idle%. At 50% utilization, wait time is 1 unit. At 90%, it's 9 units. At 99%, it's 99 units. The critical insight: a resource running at 99% utilization produces wait times 99 times longer than a resource at 50% utilization. Managing queues and handoffs between work centers is as important as managing work within them.

Finally, Erik runs Bill through a test of John's audit projects against five questions: Do they increase throughput? Do they increase stability or reduce recovery time? Do they increase Brent's capacity? Do they reduce WIP? Bill answers no to all five. Erik's conclusion: whatever their compliance rationale, projects that fail all five questions are not improving the system.

---

## The Work Center Frame

Chapter 20 delivers the clearest statement of what it means to manage flow in IT. The correction about Brent is the sharpest moment: Bill has been thinking of Brent as a scarce resource to be protected. Erik reframes this — Brent is a worker, and his overload is a symptom of how many work centers in IT depend on a single person to operate them.

The work center model (machine, man, method, measure) makes the diagnosis precise. The problem is not that Brent is indispensable — it is that there are documented steps only Brent knows how to execute, running on systems only Brent understands, with outcomes only Brent can verify. Fix that, and the constraint disperses naturally. Hiring more Brents without fixing it produces the same result Wes described: everyone standing around waiting.

The bill of resources concept is the operational mechanism that makes all of this real. Without knowing which work centers a given project requires, and which of those work centers depend on Brent, there is no way to know whether releasing a project will hit the constraint or flow around it. The bill of resources is what turns constraint-aware scheduling from an intention into a practice.

The wait time formula is the chapter's sharpest quantitative contribution. Organizations obsess over utilization — 90%+ utilization looks like efficiency. The formula shows it's the opposite: high utilization creates exponentially longer queues. A resource running at 99% doesn't do 1% more work than a resource at 90%; it creates wait times nine times longer. The slack that looks wasteful is the slack that makes flow possible.

---

## Management Observations

- **"Whoever yells loudest" is not a prioritization system — it's an absence of one.** Patty's description is not unusual; it is the default state of any IT organization without an explicit prioritization mechanism. The consequence is not just unfairness — it's that the loudest projects get resources regardless of whether they serve business outcomes, while quiet-but-important work (monitoring, documentation, technical debt reduction) waits indefinitely.
- **The work center model implies that the Brent problem is solvable through documentation, not headcount.** If the issue were headcount, hiring more engineers would help. It doesn't help, because the new engineers can't operate Brent-dependent work centers — those methods are undocumented. The solution is to document the methods, which is what the level-3 pool and no-keyboard rule were designed to force.
- **The bill of resources is the mechanism that enables "saying no" to be data-driven.** Steve told Bill to say no with data. The bill of resources is that data: it shows which work centers each project requires, which of those are at capacity, and whether accepting the project jeopardizes existing commitments. Without it, no is just a gut feeling.
- **Erik's five-question test for John's audit projects is not an argument against compliance.** It is a filter for distinguishing compliance work that improves the system from compliance work that adds process without improving outcomes. The distinction is not "do the audit findings matter?" but "does this specific remediation action increase flow, stability, or constraint capacity?" If yes, it's real work. If no, it's waste wearing a compliance label.
- **The Improvement Kata's core claim is a management commitment, not a technical insight.** "Improving daily work is even more important than doing daily work" requires that organizations protect time for improvement work from the urgency of daily operations. This is structurally identical to the Brent problem: important work is always preempted by urgent work unless there is a deliberate mechanism to prevent it.
