---
concept-type: "[[Practice]]"
description: The three-tier change categorization that makes the CAB sustainable — fragile changes requiring full CAB authorization, standard changes pre-approved for scheduling, and medium-risk changes owned by the submitter with the CAB verifying process integrity rather than technical content.
related-concepts:
  - "[[Change Advisory Board (CAB)]]"
  - "[[Uncontrolled Change ⭐]]"
  - "[[The Four Types of Work ⭐]]"
sources:
  - "[[13-Chapter_8_•_Monday,_September_8|Chapter 8 — Monday, September 8]]"
aliases:
  - Change Categorization
  - Change Triage
---

# Change Risk Tiers

Developed in Chapter 8 when 437 change cards arrive for a one-hour CAB review meeting. The previous ITIL-based process failed by applying identical overhead to every change regardless of risk. The three-tier model concentrates review effort where it matters and removes friction everywhere else.

The insight that produces the tiers: *"The 80/20 rule likely applies here. Twenty percent of the changes pose eighty percent of the risk."*

## Tier 1 — Fragile (CAB-Mandatory)

Changes to systems where the risk of failure is high and the consequences are severe. At Parts Unlimited, this includes:
- PUCCAR (Parts Unlimited Check Clearing and Reconciliation) — a legacy billing system running an out-of-maintenance OS, whose vendor went out of business during the dot-com boom. Changes to it fail with significant frequency.
- Rainbow, Saturn, and Taser applications
- Shared network infrastructure
- Core databases affecting multiple systems

These changes require full CAB authorization before scheduling. The CAB reviews the change, assesses risk, and sets implementation timing. Critically, the business is given a voice: Patty generates historical success rates and downtime data for these systems, and the affected business owners are consulted on timing. A business owner who sees that PUCCAR changes fail 30% of the time may defer — a decision IT should not be making unilaterally.

Supporting resources (engineers, vendors) are identified in advance and put on standby for the implementation window — Patty's "firefighters and ambulances on the runway" formulation.

## Tier 2 — Standard (Pre-Approved)

Changes done successfully many times before, following a well-understood procedure with predictable outcomes. Examples: monthly tax table uploads to POS systems, established patching sequences for stable systems, routine backups and rotations.

Standard changes must still be submitted — visibility is non-negotiable — but they can be scheduled without waiting for CAB review. The submission creates the audit trail and keeps the change visible to anyone who might be affected; it does not create an approval bottleneck.

This tier is what the previous ITIL process should have had. Requiring 20 minutes of form-filling for a routine monthly upload destroyed engineer goodwill and made the process unworkable. Pre-approval of standard changes removes that friction while preserving the visibility that makes coordination possible.

## Tier 3 — Messy Middle (Submitter-Owned)

Medium-risk changes where the CAB cannot evaluate technical context — and shouldn't try. Wes's formulation: *"I don't want to be like a seagull, flying in, crapping on people, and then flying away."* The people closest to the work understand the risk better than a review committee.

For these changes, the submitter is accountable for:
1. Identifying everyone who could be affected
2. Consulting them and getting explicit sign-off
3. Submitting the card with confirmation that this work has been done

The CAB's role is process verification, not technical review: did the submitter do the necessary coordination? If yes, the change is approved for scheduling. If no, it goes back.

Bill's reference case is the tokenization deployment from Chapter 3. Under this model, John would have been required to get sign-off from the application owner, the database owner, and the business before the card reached the CAB. That coordination would likely have surfaced the conflict with the payroll run before the deployment — not after.

## Why Previous Processes Failed

Both prior CAB attempts at Parts Unlimited applied a single process to all three tiers. The first attempt used ITIL tooling that required 20-minute forms for five-minute changes (Tier 2 and 3 work treated as Tier 1). Engineers rebelled; the process died. The second attempt had no tiers at all — changes were effectively self-authorized.

The three-tier model succeeds by matching process overhead to actual risk level. Tier 1 changes get more scrutiny than before. Tier 2 and 3 changes get less — and less that is actually appropriate to their risk profile, not less because nobody cared.
