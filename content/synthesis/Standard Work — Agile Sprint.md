---
builds-on:
  - "[[Manufacturing vs IT]]"
  - "[[Agentic AI and the Manufacturing-IT Gap]]"
frameworks:
  - "[[Kanban]]"
  - "[[Work in Process (WIP) ⭐]]"
  - "[[Goldratt's Five Focusing Steps]]"
  - "[[Wait Time and Utilization]]"
  - "[[The Three Ways ⭐]]"
  - "[[The Four Types of Work ⭐]]"
  - "[[Technical Debt]]"
---

# Standard Work — Agile Sprint

A two-week sprint described as a manufacturing production cycle. Each phase is a work center with defined inputs, outputs, method, and quality checks — the same structure Erik describes on the MRP-8 plant floor: **machine, man, method, measure.**

This is not a process manual. It is a [[Kanban|standard]] against which deviations become visible and every deviation becomes a learning opportunity.

---

## Production Parameters

| Parameter                   | Value                                                                  |                         |
| --------------------------- | ---------------------------------------------------------------------- | ----------------------- |
| Cycle time                  | 2 weeks (10 working days)                                              |                         |
| Takt time                   | 1 user story per 2–3 days (team-dependent)                             |                         |
| WIP limit (In Development)  | 2 stories per developer pair                                           |                         |
| WIP limit (In Review)       | 3 stories                                                              |                         |
| WIP limit (In QA)           | 3 stories                                                              |                         |
| Planned capacity allocation | 70% feature work / 10% [[Technical Debt                                | tech debt]] / 20% slack |
| Constraint resource         | Identify per sprint — often QA, senior reviewer, or environment access |                         |

The 20% slack is not waste. It is the margin that prevents [[Wait Time and Utilization|queue time from exploding]] when utilization approaches 100%. A team at 100% planned allocation has zero capacity to absorb any [[The Four Types of Work ⭐|unplanned work]] without blowing every commitment.

---

## Work Centers

### 1. Backlog Refinement (Input Preparation)

**When:** Continuous; formal session midweek (Wed or Thu), 1 hour max.

| Element | Detail |
|---|---|
| **Machine** | Backlog tool (Jira, Linear, etc.), estimation framework |
| **Man** | Product owner, tech lead, 1–2 engineers on rotation |
| **Method** | For each candidate story: clarify acceptance criteria, identify dependencies, estimate size, flag constraint-resource needs. Stories exit refinement "Ready" — meaning any engineer could pick them up and start without asking questions. |
| **Measure** | % of stories entering sprint that were refined ≥ 3 days prior. Target: 100%. |

**Quality check:** A story that enters the sprint unrefined is the equivalent of releasing raw materials onto the plant floor without a routing. It will block, generate rework, and consume the constraint.

**Constraint awareness:** Flag stories that require the sprint's constraint resource (e.g., "needs senior backend review," "needs staging environment access"). These are the [[The Brent Problem ⭐|Brent-dependent changes]] — they must be sequenced against the constraint's available capacity, not scheduled freely.

---

### 2. Sprint Planning (Job Release)

**When:** Day 1 of sprint, 1–2 hours.

| Element | Detail |
|---|---|
| **Machine** | Sprint board (physical or digital kanban), capacity calculator |
| **Man** | Full team, product owner, scrum master |
| **Method** | (1) Review sprint goal — one sentence, business-outcome-framed. (2) Pull stories from the top of the refined backlog until capacity is filled. Do not exceed capacity. (3) Identify the sprint's constraint resource and sequence constraint-dependent stories first. (4) Commit. |
| **Measure** | Stories committed vs. team capacity (velocity ± 10%). Over-commitment rate tracked sprint-over-sprint. |

**The [[Allie the MRP Coordinator|Allie]] check:** Before committing, verify: do we have capacity at every work center this story will pass through? If QA is at 90% utilization from carryover work, pulling four QA-heavy stories is pulling work the constraint can't absorb. The commitment will fail — not from lack of effort but from [[Work in Process (WIP) ⭐|releasing work against capacity that doesn't exist]].

**The [[The Project Freeze ⭐|freeze]] rule:** Once planning is complete, the sprint scope is locked. New work enters the next sprint, not this one. This is not rigidity — it is WIP control. A sprint that accepts mid-flight scope changes is a sprint where every existing commitment becomes unreliable.

---

### 3. Development (Processing)

**When:** Days 1–8 (primary), with deployable increments emerging from Day 3.

| Element | Detail |
|---|---|
| **Machine** | IDE, CI pipeline, dev/staging environments, version control |
| **Man** | Engineers (paired or solo per team norm) |
| **Method** | Pull the top story from "Ready." Move card to "In Dev." Implement. Write tests. Push to branch. Move card to "In Review." Do not start a new story while your current story is in review — instead, review someone else's. |
| **Measure** | Cycle time per story (first commit → merged). Track and trend. |

**WIP limit enforcement:** No engineer should have more than one story in "In Dev" at a time. If blocked, swarm on the blocker or pull review/QA work — do not start a new story. Starting new stories while blocked is how [[Work in Process (WIP) ⭐|WIP]] compounds: each new start increases context-switching cost and decreases throughput even though it looks like productivity.

**[[Uncontrolled Change ⭐|Change discipline]]:** All changes go through version control. No direct production edits. No "quick fixes" that bypass the pipeline. The CI pipeline is the [[Change Advisory Board (CAB)|CAB]] — it enforces that every change is visible, tested, and traceable.

---

### 4. Code Review (In-Process Inspection)

**When:** Continuous; target < 4 hours from PR opened to review started.

| Element | Detail |
|---|---|
| **Machine** | PR tool (GitHub, GitLab, etc.), CI checks |
| **Man** | A peer engineer not involved in the implementation |
| **Method** | Review for correctness, clarity, test coverage, and operational concerns (logging, error handling, config). Approve, request changes, or flag for architectural discussion. |
| **Measure** | Review turnaround time (PR opened → first review). Target: < 4 hours. Track review rejection rate. |

**Why this is a work center, not a checkbox:** Review is where the [[Throwing the Pig Over the Wall|handoff gap]] is smallest. The reviewer catches what the author missed — missing error handling, implicit dependencies, configuration that works locally but won't in production. A review that takes three days is a story sitting in queue; at high utilization, it's [[Wait Time and Utilization|9x or 99x the wait]] of a review done in hours.

**Constraint protection:** If the senior reviewer is the sprint's constraint, review requests to them must be prioritized over their own development work. The constraint must never wait.

---

### 5. QA / Testing (Quality Gate)

**When:** Continuous; stories move to QA as they pass review.

| Element | Detail |
|---|---|
| **Machine** | Test environment, automated test suite, manual test plans |
| **Man** | QA engineer or engineer performing QA rotation |
| **Method** | Execute acceptance criteria. Run automated regression. Perform exploratory testing for edge cases. Pass → move to "Done." Fail → return to "In Dev" with specific failure description. |
| **Measure** | Pass-through rate (% of stories that pass QA on first attempt). Defect escape rate (bugs found in production that QA should have caught). |

**The inspection principle:** QA is not the place where quality is *created* — quality was created (or not) during development and review. QA is the place where quality is *verified*. A high QA rejection rate means the upstream work centers have a method problem, not that QA needs to test harder.

**Environment as constraint:** If the test environment is shared and at capacity, QA becomes a bottleneck regardless of QA staffing. The "machine" in this work center matters as much as the "man." Track environment availability as a constraint metric.

---

### 6. Deployment (Shipping)

**When:** Continuous (if CI/CD is mature) or batched at end of sprint.

| Element | Detail |
|---|---|
| **Machine** | CI/CD pipeline, deployment tooling, production environment |
| **Man** | Engineer on deploy rotation or automated pipeline |
| **Method** | Merge to main. Pipeline runs full test suite. Deploy to staging. Smoke test. Deploy to production. Verify monitoring. Roll back if anomalies detected within observation window. |
| **Measure** | Deployment frequency. Deployment failure rate. Mean time to recovery (MTTR) from failed deploy. |

**The [[The Point of No Return|point of no return]]:** Know where it is. For database migrations, schema changes, or data transformations — identify which steps are irreversible before starting. Verify those steps in staging at production data volume. The Phoenix database conversion failed because nobody verified the irreversible step under production conditions before crossing the threshold.

**Agentic AI application:** This work center is the most natural fit for AI automation. An agent can run the full deployment sequence, verify each step, monitor for anomalies, and roll back autonomously — producing a complete log at every stage. This is the [[The Brent Problem ⭐|no-keyboard rule]] implemented perfectly: every action is executed, observed, and documented.

---

### 7. Sprint Review / Demo (Output Verification)

**When:** Day 10 (last day), 1 hour.

| Element | Detail |
|---|---|
| **Machine** | Production or staging environment, demo script |
| **Man** | Full team, product owner, stakeholders |
| **Method** | Demo each completed story against its acceptance criteria. Stakeholders provide feedback. Incomplete stories return to the backlog — they do not carry implicit priority into the next sprint. Record stakeholder feedback as input to next refinement. |
| **Measure** | Stories committed vs. stories completed (sprint completion rate). Stakeholder satisfaction (qualitative). |

**The success metric problem:** "Technically, we hit the date" — Chris's defense of the Phoenix launch. A story that is "done" in development but broken in production is not done. The demo must be against the *production* system or a faithful replica. The definition of done is: the user can use it, not the engineer has finished coding it.

---

### 8. Retrospective (Improvement Kata)

**When:** Day 10, 1 hour, after the review.

| Element | Detail |
|---|---|
| **Machine** | Whiteboard or retro tool, sprint metrics |
| **Man** | Full team (no stakeholders — safe space) |
| **Method** | (1) Review metrics: cycle time, WIP trends, completion rate, defect escape rate, deployment frequency. (2) Identify one thing that went well (reinforce). (3) Identify one thing to improve (select, don't brainstorm a list of ten). (4) Define the experiment: what will we change, how will we measure it, when will we evaluate. (5) Review last sprint's experiment: did it work? Keep or revert? |
| **Measure** | Experiments run per sprint (target: 1). Experiments that produced measurable improvement (track over time). |

**This is the [[The Three Ways ⭐|Third Way]].** The retrospective is not a venting session or a blame exercise. It is the two-week Plan-Do-Check-Act cycle that Rother calls the Improvement Kata. One experiment per sprint. Small. Measurable. The point is not the magnitude of any single improvement — it is the *habit* of improving. Five minutes of daily practice beats three hours once a month.

**What to watch for:** If the same issue appears in three consecutive retros without improvement, the experiment design is wrong, the constraint hasn't been correctly identified, or the team lacks authority to make the change. Escalate — don't keep running the same failed experiment.

---

## The Kanban Board

```
┌──────────┬──────────┬───────────┬──────────┬──────────┬──────────┐
│ Refined  │  To Do   │  In Dev   │In Review │   In QA  │   Done   │
│ (Ready)  │ (Sprint) │  WIP: 2   │  WIP: 3  │  WIP: 3  │          │
├──────────┼──────────┼───────────┼──────────┼──────────┼──────────┤
│          │          │           │          │          │          │
│  story   │  story   │  story    │  story   │  story   │  story   │
│  story   │  story   │  story    │          │  story   │  story   │
│  story   │          │           │          │          │  story   │
│          │          │           │          │          │  story   │
└──────────┴──────────┴───────────┴──────────┴──────────┴──────────┘

Card colors:
  🟣 Purple — sprint goal stories (highest priority)
  🟡 Yellow — other committed stories
  🟢 Green  — tech debt / improvement work (protect the 10% allocation)
  🔴 Red    — blocked (reviewed twice daily)
```

If there are no green cards in progress at any point during the sprint, tech debt work is being crowded out. The color makes this visible at a glance — the same mechanism Patty built for the Parts Unlimited change board.

---

## Anti-Patterns (Mapped to TPP Failures)

| Anti-pattern | What it looks like | TPP equivalent |
|---|---|---|
| Mid-sprint scope injection | PO adds "just one more story" on Day 6 | Sarah's "WE MUST GO!" — commitment overriding capacity analysis |
| WIP explosion | Every engineer has 3 stories in progress | 942 pending change cards — WIP compounding at the constraint |
| Review queue backup | PRs sit for 2+ days | Inventory piling at the heat treat oven |
| Skipping retro | "We're too busy to improve" | Urgency defeating importance — the cycle that created the Brent problem |
| Definition-of-done drift | "It works on staging" counted as done | [[Works on My Laptop\|"Works on my laptop"]] — success defined at the wrong boundary |
| Hero deploys | One person does all deploys with no docs | Brent in the trance — tacit knowledge that evaporates |
| No capacity slack | Sprint planned to 100% | [[Wait Time and Utilization\|99% utilization]] = 99x wait time for any unplanned work |

---

## Where Agentic AI Slots In

| Work center | AI role | Human role |
|---|---|---|
| Refinement | Draft acceptance criteria, flag dependencies, estimate based on historical data | Judgment on priority, scope, business value |
| Planning | Capacity modeling, constraint identification, load analysis | Commitment decision, sprint goal |
| Development | Pair programming, boilerplate generation, test writing | Architecture, design decisions, novel problem-solving |
| Review | Automated style/correctness checks, security scanning, test coverage verification | Architectural judgment, readability, mentoring through review |
| QA | Automated regression, environment provisioning, exploratory test suggestion | Edge case judgment, UX evaluation, acceptance criteria interpretation |
| Deployment | Full pipeline automation, monitoring, auto-rollback | Go/no-go decision for high-risk deploys, incident command if rollback fails |
| Review/Demo | Metrics compilation, change summary generation | Stakeholder communication, feedback interpretation |
| Retrospective | Pattern detection across sprints, metrics trending, experiment suggestions | Judgment on what to change, culture of psychological safety |

The pattern: AI handles the [[The Three Ways ⭐|First and Second Way]] work (flow and feedback). Humans own the [[The Three Ways ⭐|Third Way]] (learning, judgment, culture).
