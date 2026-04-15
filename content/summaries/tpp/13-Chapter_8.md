---
related-concepts:
  - "[[Change Risk Tiers]]"
  - "[[Change Advisory Board (CAB)]]"
  - "[[Uncontrolled Change ⭐]]"
  - "[[The Brent Problem ⭐]]"
sources:
  - "[[13-Chapter_8_•_Monday,_September_8|Chapter 8 — Monday, September 8]]"
---

# Chapter 8

## What Happens

Bill spends the weekend preparing a PowerPoint presentation for his Monday meeting with Steve. He arrives to find Sarah already in the room, burning eleven of his thirty minutes recounting Phoenix analyst briefings. When she leaves, Bill has nineteen minutes.

He makes the case: demand far exceeds capacity, Phoenix and compliance work compete for the same people (specifically Brent), and the organization needs six additional hires to have any chance of delivering both. Steve refuses on every front: Phoenix is already $10M over budget, IT is benchmarked as overspending versus peers, adding $2M in labor is impossible, and if anything he may need to cut headcount. His counter-suggestion: make the case to peers and ask them to transfer budget.

Bill pushes back directly — *"If you really care about closing the gap with the competition by having Phoenix succeed, you sure aren't acting like it"* — but Steve doesn't move. Sarah walks in two minutes early for the next analyst call. Bill leaves, drops his weekend's work in the recycling bin, and walks to the CAB meeting.

He arrives to find the Change Coordination Room transformed: 437 index cards covering every whiteboard, stacked on the table in piles, some hanging ten-deep on hooks. Wes and Patty are equally stunned. A one-hour meeting to authorize 437 changes is obviously impossible.

Bill reframes the goal — situational awareness, not perfect authorization — and proposes the 80/20 rule: 20% of changes carry 80% of the risk. The team builds a triage system in real time:

**Three tiers emerge:**

1. **Fragile / High-risk** — changes to known brittle systems (PUCCAR, Rainbow, Saturn, Taser applications; shared network and databases). Must be CAB-authorized before scheduling. Patty will generate historical success rates and downtime data so the business can make informed scheduling decisions. Bill's insight: give the business a voice in timing — the responsibility shouldn't rest entirely with IT.

2. **Standard / Pre-approved** — routine changes done successfully many times before (monthly tax table uploads, established patching procedures). Submitted for visibility but scheduled without CAB review.

3. **Messy middle** — medium-risk changes where the CAB can't evaluate technical context. The submitter owns the preparation: consult everyone affected, get their sign-off, then submit the card. The CAB verifies process integrity, not technical correctness.

The team agrees on an amnesty window through Tuesday, with a full scheduling CAB on Wednesday. Wes proactively asks about next week's process — a first. Everyone leaves the meeting smiling, also a first.

---

## What the Chapter Reveals

Two things happen in parallel: Bill fails upward with Steve, and the CAB achieves its first real design breakthrough.

The Steve meeting establishes a hard constraint that will drive the rest of the book: **no new resources, no budget relief, no prioritization help from above.** Bill must fix the system with what he has. The only lever Steve offers is negotiating with peers for budget transfers — which is effectively no lever at all.

The CAB triage session is where actual progress happens. The three-tier design is what makes the process sustainable where previous attempts failed. The earlier ITIL-based process applied uniform overhead to every change regardless of risk — the same 20-minute form for a routine patching run and for a change to the company's most fragile billing system. Concentrating CAB attention on the fragile tier and removing friction everywhere else is the design principle that rescues the process.

---

## Management Observations

- **Steve's refusal to prioritize is itself a prioritization decision.** Declining to choose between Phoenix and compliance forces both to share the same constrained resources. The outcome is predictable: both will be done poorly and late. Bill naming this explicitly — even unsuccessfully — is still the right call. The constraint is now on the record.
- **The 80/20 triage is the design principle the CAB was missing.** A PUCCAR change and a monthly tax table upload are not the same risk. Previous processes failed by treating them identically. Identifying the fragile tier and concentrating review there is the minimum viable version of risk-based change management.
- **Pushing accountability to the submitter for medium-risk changes is correct.** Bill's tokenization example is precise: before reaching the CAB, John should have gotten sign-off from the application owner, the database owner, and the business. The CAB verifies that those conversations happened — it does not substitute its judgment for the people closest to the work. This distributes technical accountability to where the knowledge actually lives.
- **Giving the business a voice in fragile change scheduling matters.** Sharing historical success rates and downtime data before scheduling high-risk changes transfers some of the risk decision to the people who bear the consequences. A business owner who sees that PUCCAR fails 30% of the time during changes may choose to defer — reducing IT's unilateral burden and making risks visible before things go wrong rather than after.
- **"We all leave smiling" is the chapter's closing signal.** Every previous meeting ended with someone angry or defensive. The CAB triage session produced a workable design that Wes helped build and proactively extended to the following week. Process people participate in designing is process people follow.
