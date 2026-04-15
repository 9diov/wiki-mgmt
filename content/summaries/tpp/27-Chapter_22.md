---
related-concepts:
  - "[[Work in Process (WIP) ⭐]]"
  - "[[The Brent Problem ⭐]]"
  - "[[Goldratt's Five Focusing Steps]]"
  - "[[Kanban]]"
  - "[[Technical Debt]]"
sources:
  - "[[27-Chapter_22_•_Monday,_September_29|Chapter 22 — Monday, September 29]]"
---

# Chapter 22

## What Happens

John has disappeared after the audit meeting. Bill tells Wes to stop feeding the rumor mill.

Patty calls a meeting to share what she built over the weekend. On the back wall of the Change Coordination Room: a kanban board. Four rows — "Move worker office," "Add/change/delete account," "Provision new desktop/laptop," "Reset password" — each divided into three columns: "Ready," "Doing," "Done."

She visited MRP-8 herself, talked to a plant supervisor, and came back with a working system. She documented each of the most frequent service request types, mapped the steps and resources required, timed each operation, and built the board. Any activity going through these resources must go through the kanban — not email, not phone, not instant message. What's not on the board won't get done; what is on the board will get done quickly, because WIP is capped.

She has also published a laptop replacement schedule: every requester listed, the date they submitted, and the projected delivery date. Bill is fourteenth in line, four days out. She delivers his laptop two days early. Everyone ahead of him has already received theirs; the few with configuration errors early in the trial have already been corrected in the work instructions. Defects down from fifteen configuration turns to tracking toward three.

The existing change board has been upgraded with color-coding: purple cards for the top five business projects, yellow for other changes, green for internal IT improvement projects (allocated at 20% of cycles, as Erik recommended), and pink sticky notes for blocked cards — reviewed twice daily. Change IDs are written on each card and tracked in the change management tool.

Patty also plans a kanban specifically around Brent: formalizing how work reaches him, making upstream and downstream demand visible, and creating one more line of defense against direct drive-bys.

On the project sequencing question — how to lift the freeze without being overwhelmed — Bill proposes three lists:
1. Projects requiring Brent
2. Projects that *increase* Brent's throughput (most important list)
3. Everything else

The principle: improving the constraint is the highest-priority IT internal work. Projects that don't require Brent can be run without constraint impact. Projects that require Brent must be sequenced within his available capacity.

Patty names what they're building: a Manufacturing Production Control function. Manufacturing production control accepts orders based on available capacity at each work center, builds a master schedule, expedites as needed, and delivers against commitments. That's what IT Operations now needs.

Bill notes that managing the IT production schedule probably should have been in his job description from the start.

---

## The Kanban in Action

Chapter 22 is the first chapter where the manufacturing principles introduced by Erik are visibly working — not as theory, but as Patty's laptop delivery schedule arriving two days early.

The kanban board's mechanism is simple: separate the intake queue ("Ready") from the work in progress ("Doing") from the completion queue ("Done"). Cap the "Doing" column. When Doing is full, nothing new enters it until something completes. This forces single-tasking, which is what makes the lead time predictions reliable. A resource that is only working one thing at a time can be timed; a resource that is context-switching across seven things cannot.

The color-coding of the change board is the visual management complement. The question "are we working on the right things?" has a visible answer in the balance of purple, yellow, and green cards in the "Doing" state at any moment. If there are no green cards in Doing, improvement work is being deferred again. If there are too many purple cards, business projects are crowding out IT health work.

The production control analogy completes the chapter's arc. Parts Unlimited has now built, iteratively and under operational pressure, the equivalent of the function that manufacturing companies formalized decades ago: an explicit mechanism for accepting work based on known capacity, scheduling it against known constraints, and delivering against published commitments.

---

## Management Observations

- **Patty delivers the laptop ahead of schedule because she eliminated multitasking, not because she added resources.** The throughput improvement came entirely from process redesign: documenting steps, limiting WIP, routing all requests through a single visible queue. No new headcount. The kanban is a flow improvement, not a capacity addition.
- **The three-list project prioritization is a direct application of the Five Focusing Steps.** List 2 (projects that increase Brent's throughput) corresponds to Step 4: elevate the constraint. List 1 (projects requiring Brent) must be sequenced against Step 3: subordinate everything to the constraint. List 3 (everything else) can flow freely. This isn't a prioritization methodology — it's constraint-aware scheduling, applied to the project portfolio.
- **The 20% green card allocation is the operational guarantee for improvement work.** Without an explicit protected allocation, improvement work will always be crowded out by urgent project demand and unplanned work. The color-coding makes the allocation visible; the visual management makes violations of it visible. If there are no green cards in progress, the team has tacit permission to pull one from Ready.
- **"Managing the IT production schedule" as a job function is the organizational conclusion of the entire novel to this point.** The question that Erik has been circling since Chapter 7 — how does IT decide whether to accept new work? — has a structural answer: a production control function that maintains a bill of resources, tracks work center loading, and makes the accept/reject decision based on real capacity data. Bill's observation that this "probably should have been in his job description" is the book's understated acknowledgment that this function is almost universally missing from IT organizations.
