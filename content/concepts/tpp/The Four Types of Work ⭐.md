---
concept-type: "[[Framework]]"
description: Erik's framework for categorizing all IT work into four types — business projects, IT projects, changes, and unplanned work — as a prerequisite to managing capacity, sequencing, and constraint protection. Only one type is named in Chapter 7; the full framework emerges as Bill works it out.
related-concepts:
  - "[[The Three Ways ⭐]]"
  - "[[The Brent Problem ⭐]]"
  - "[[Uncontrolled Change ⭐]]"
  - "[[Change Advisory Board (CAB)]]"
sources:
  - "[[12-Chapter_7_•_Friday,_September_5|Chapter 7 — Friday, September 5]]"
  - "[[10-Chapter_5_•_Thursday,_September_4|Chapter 5 — Thursday, September 4]]"
  - "[[14-Chapter_9_•_Tuesday,_September_9|Chapter 9 — Tuesday, September 9]]"
  - "[[20-Chapter_15_•_Wednesday,_September_17|Chapter 15 — Wednesday, September 17]]"
---

# The Four Types of Work

In Chapter 7, Erik tells Bill he has identified only one of four types of work that IT Operations is responsible for — business projects — and that without understanding all four, he cannot manage demand, protect the constraint, or have an intelligent conversation about capacity.

Erik gives Bill a phone number and a single task: identify the other three. When he has them, call.

## The Framework (as it emerges)

**Type 1 — Business Projects**
Work driven by business initiatives: features, new systems, market responses. The work most visible to executives and the board. Phoenix is the dominant example throughout the novel. Business projects are tracked by the PMO, have sponsors and deadlines, and compete with everything else for IT capacity.

**Type 2 — IT Projects**
Internal infrastructure and improvement work that IT owns: upgrading the SAN firmware, replacing end-of-life servers, consolidating databases, building a test environment. These projects are essential for keeping the platform stable and current, but they rarely have business sponsors or formal visibility. At Parts Unlimited, over 70 IT projects exist with no central list and no formal prioritization — they accumulate off the books.

**Type 3 — Changes**
Any modification to the production environment: deployments, patches, configuration changes, database scripts, network updates. Changes are the operational lifeblood of IT — necessary to deliver business projects and keep infrastructure current — but uncoordinated changes are also the primary source of incidents. The CAB exists specifically to make Type 3 work visible and sequenced. The 437 index cards in Chapter 8 represent one week of Type 3 work that was previously invisible.

**Type 4 — Unplanned Work**
Incidents, break-fix, firefighting, and recovery work. Unplanned work is the destroyer of planned work — it arrives without warning, immediately preempts everything else, and consumes the organization's most critical resources (Brent, first and foremost). At Parts Unlimited, unplanned work consumes approximately 75% of IT capacity, leaving only 25% for Types 1, 2, and 3 combined.

## Why the Taxonomy Matters

Without a shared vocabulary for the four types, IT cannot:
- Estimate capacity accurately (unplanned work is invisible until it hits)
- Protect the constraint (Brent gets pulled to Type 4 work before Type 1 work)
- Prioritize intelligently (business projects compete with IT projects with no common unit)
- Have honest conversations with the business (Steve cannot be shown why Phoenix and compliance are truly in conflict without a model that makes the conflict visible)

The four-type framework is the prerequisite to what Erik calls "controlling the release of work" — the equivalent of the job release desk on the plant floor. You cannot control what you cannot categorize. You cannot categorize what you have not named.

## The Type 4 Problem

Unplanned work is the most destructive type precisely because it is invisible in planning but always takes priority in execution. Type 1, 2, and 3 work can be estimated, sequenced, and committed to. Type 4 arrives at random and immediately preempts everything else by definition (incidents must be resolved).

The consequence: any commitment made against IT capacity is implicitly conditional on the volume of Type 4 work staying constant. When it spikes — as it does repeatedly in the novel — every planned commitment slips simultaneously, with no warning and no recourse. Reducing Type 4 volume is therefore not just a quality goal; it is the primary lever for increasing the reliability of all other commitments.

## How Bill Discovers the Fourth Type (Chapter 15)

Bill identifies unplanned work not by cataloguing work in progress but by observing what happened to planned work during the Phoenix disaster. Standing at the change board with Patty, he sees a dense record of completed changes on the left side and a void on the right — a week where nearly every scheduled change was abandoned or rescheduled.

The Phoenix recovery consumed every available person. The board didn't show that directly. It showed the absence of everything else. Bill's formulation: unplanned work is like dark matter — you can only see it by what it displaces.

Erik confirms the insight and names it: *"Unplanned work is recovery work, which almost always takes you away from your goals. That's why it's so important to know where your unplanned work is coming from."* He also suggests the term "anti-work" to emphasize that it is not merely one category among four — it is the category that destroys the other three.
