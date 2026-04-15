---
related-concepts:
  - "[[The Four Types of Work ⭐]]"
  - "[[Work in Process (WIP) ⭐]]"
  - "[[The Brent Problem ⭐]]"
  - "[[The Three Ways ⭐]]"
  - "[[Goldratt's Five Focusing Steps]]"
sources:
  - "[[20-Chapter_15_•_Wednesday,_September_17|Chapter 15 — Wednesday, September 17]]"
---

# Chapter 15

## What Happens

Bill takes Paige to breakfast on Wednesday morning — the first real time off in three weeks. She observes that he's changed: jaw-clenching, absent, preoccupied. The conversation surfaces the reason he stays: financial obligation, a pay raise that makes a real difference, and a genuine belief that he can prevent the outsourcing of two hundred people's jobs. He drives back to work.

At his desk, an upbeat email from Wes is waiting. A DBA named Robert has forwarded a message to the engineering group: the change process saved a near-collision that morning. Two teams had been simultaneously planning changes to the same materials management database; Rajiv spotted the overlap on the change wall before either was implemented. The engineers worked it out themselves. Robert's sign-off: *"Keep those change cards coming, guys!"* Bill notes what makes it significant — the validation came from an engineer, not a manager.

Patty calls him to the Change Coordination Room. She points at the board. From Monday through Thursday of the previous week, the changes are densely populated and marked completed. Then: nothing. An empty stretch through the end of the week, with hundreds of cards piled in a basket labeled "Changes To Be Rescheduled."

Bill stares at the void. Phoenix happened, and every scheduled change was displaced. He knows Phoenix isn't the fourth category of work — it's a business project. But something about the void tells him what he's looking for. He turns it over: what displaced the planned work? Unplanned work. Firefighting. Not work in the normal sense — it's the thing that prevents all other work from happening. Matter and antimatter: *"In the presence of unplanned work, all planned work ignites with incandescent fury."*

He laughs out loud, pumps his arms, and calls Erik from a bench in the parking lot.

Erik confirms the fourth type: unplanned work, or "anti-work" — recovery work that almost always takes you away from your goals, distinct from the other three types precisely because it isn't chosen. He then runs through the progress Bill has made: stabilizing the environment, visualizing WIP on what Erik calls a kanban board, protecting the constraint. He names the change board explicitly as a kanban and references David Anderson's adaptation of Goldratt's work to software development.

Erik then delivers the Five Focusing Steps from Goldratt's *The Goal*:

1. **Identify the constraint.** Bill has done this — Brent.
2. **Exploit the constraint.** Never let it waste time. Brent should always be working the highest-priority commitment. Bill has made progress here.
3. **Subordinate the constraint.** Set the tempo of all work release to the constraint's capacity — the Drum-Buffer-Rope mechanism. This is Bill's next homework: figure out how to throttle work release to Brent's actual rate.

Erik also raises what he calls the unaddressed piece of the First Way: the distinction between work that matters to business outcomes and work that doesn't. Jimmy (John) can't make that distinction with the auditors. Outcomes matter — not process, not controls, not work completed. Taking needless work out of the system is more important than putting more in.

Finally, Erik names the core structural problem: Brent is the person who knows the most about the technical debt and how to design code for operational use. But Brent can never attend the planning and architecture meetings where that knowledge is needed, because unplanned work keeps him away. Solving the Brent problem is the prerequisite to solving the design-for-operations problem.

---

## Finding the Fourth Type

The void on the change board is the book's most elegant pedagogical device. Every concept in the Four Types of Work framework is observable — business projects are in the PMO, IT projects are on someone's backlog, changes are on the board. Unplanned work is defined by its absence: you can only see it by what it displaces.

Bill couldn't identify unplanned work by cataloguing work in progress. He identified it by watching planned work disappear and asking what erased it. This is why Erik called it "the most destructive type" rather than simply "the most important type." It is destructive specifically because it is invisible in planning — it doesn't appear on any list before it arrives — and then takes absolute priority when it does.

The kanban connection Erik draws is the chapter's other structural step forward. The change board was invented by Patty as an improvised solution to the volume problem. Erik names it as an instance of a known discipline and points Bill toward Goldratt's Five Focusing Steps as the theoretical framework that connects constraint management to WIP control to flow. The novel is now explicitly in conversation with *The Goal*.

---

## Management Observations

- **Robert's email is a more reliable signal than Bill's own assessment.** A change process that engineers voluntarily praise — "keep those change cards coming, guys!" — has passed the adoption test. A process that managers mandate but engineers route around is theater; a process that engineers recommend to each other is real. The distinction matters when evaluating whether any governance mechanism is working.
- **The void is the diagnostic, not the board.** Patty brought Bill in expecting concern about 100% non-completion; Bill's actual response is elation, because the void shows him something he had been searching for. The change board's value isn't just tracking what's scheduled — it's making the displacement of planned work by unplanned work observable. You can manage what you can see. You can't manage the void if you can't see the void.
- **Erik's Five Focusing Steps reframe Brent from a people problem to a systems problem.** The language changes in this chapter: Brent is not an overloaded engineer, he is the organizational constraint. The steps don't say "fix Brent" — they say identify, exploit, and subordinate the constraint. The constraint is a property of the system, not the person. Replacing Brent with someone equally skilled would not remove the constraint; it would just relocate it to the new person.
- **"Taking needless work out of the system is more important than putting more work in."** This is Erik's sharpest formulation in the chapter. The instinct in most organizations is to find more capacity — more headcount, more hours, faster tools. Erik is pointing in the opposite direction: most of the work in the system shouldn't be in the system at all. Until you can distinguish work that serves business outcomes from work that doesn't, adding capacity just accelerates the production of low-value work.
- **Nonfunctional requirements — operability, security, scalability, continuity — must be designed in.** Erik's critique of Chris's organization is that it spends all cycles on features and none on what he calls "the beautiful 'ities'." The result is systems that function but cannot be operated, secured, or maintained — which then generates the unplanned work that consumes Brent. The correction requires Brent in design and architecture meetings. The correction is blocked by unplanned work. The loop is complete.
