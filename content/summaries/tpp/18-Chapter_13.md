---
related-concepts:
  - "[[Uncontrolled Change ⭐]]"
  - "[[Throwing the Pig Over the Wall]]"
  - "[[Change Risk Tiers]]"
  - "[[The Point of No Return]]"
sources:
  - "[[18-Chapter_13_•_Monday,_September_15|Chapter 13 — Monday, September 15]]"
---

# Chapter 13

## What Happens

Bill wakes up at his desk Monday morning — he's lost track of Sunday entirely. Steve is mid-address to the assembled room, red-faced. The Phoenix crisis is front-page news across the technology press. The Wall Street Journal is asking for an interview. Steve is not interested in blame; he wants the company back to normal operations. He holds Sarah publicly accountable by name, then schedules a fifteen-minute post-mortem with every executive who had a hand in the deployment.

Sarah immediately pivots from the restoration effort to usability improvements — Phoenix's ordering interface is being mocked in press coverage, and she wants fixes deployed. Bill pushes back hard: the front-end servers are being proactively rebooted every hour just to keep them running. He proposes restricting code deployments to twice a day, with only performance-critical changes accepted. To his surprise, Chris agrees immediately, and William reinforces it: any commit without a defect number tied to a performance problem gets rejected. Sarah objects and loses. The freeze stands.

Bill walks across the hall to the Finance war room, where Ann's team is processing the transaction disaster. Twelve people are routing faxes from 120 stores, each one a problem order. The running count: 5,000 customers with duplicate payments or missing orders, with an estimated 25,000 more transactions still to investigate.

John is also in the room. He picks up a stack of paper slips and goes pale. He pulls Bill into the hallway: the carbon paper credit card imprinters used as the manual fallback have captured CVV codes from customers' cards. Under PCI DSS rules, storing or transmitting the card verification value is prohibited — even possessing it constitutes a cardholder data breach. The fines scale with the number of cardholders affected. The Finance team is sitting in a room full of it.

John checks his binder: the PCI auditors are on-site today, in the building, doing a business process walk-through. They are scheduled to use the conference room currently serving as the Phoenix POS Recovery War Room. Bill asks John to redirect the auditors. John does — reroutes the entire interview schedule to a different building, instructs security not to let the auditors past the front desk of the Phoenix building. He succeeds.

Back at his desk, John calls again to flag the SOX-404 response letter, which was due today. The plan had been to complete it over the weekend following the deployment. Bill tells John flatly: his entire team has been working around-the-clock on Phoenix recovery, and there are no cycles left. John offers two of his engineers to help with the remediation estimate, or to go into the technical resource pool if needed. Bill accepts. He notes, half in exhaustion, that something is wrong with the world when he's grateful to both Development and Security in the same day.

---

## The Aftershock

Chapter 13 introduces a category of failure that is distinct from the deployment itself: the secondary crises that the primary failure creates, cascading into systems and obligations that had nothing to do with the original problem.

The CVV incident is the clearest example. The manual fallback — carbon paper imprinters — was a reasonable contingency for POS systems going offline. Someone planned for the fallback. Nobody planned for the compliance implications of the fallback. The CVV codes printed on carbon paper slips are prohibited cardholder data under PCI DSS, and they exist because the fallback was designed around operational continuity without reference to its security or compliance constraints. The fallback solved one problem while creating another.

The timing of the PCI audit is genuinely bad luck — auditors scheduled weeks in advance, on-site the same Monday the fallback data is sitting in a room. But the underlying problem — that the organization is now carrying live compliance violations — is a consequence of the deployment failure, not a coincidence. High-risk deployments don't just fail in their own domain; they radiate risk into adjacent systems.

The SOX-404 missed deadline is the same pattern. The audit response was a real obligation with a real deadline. It was planned for the deployment weekend. The deployment consumed the weekend. One obligation's failure absorbs the capacity that was allocated to another obligation — and the second one slips, creating a third problem (audit committee red flag) downstream.

This is the compound arithmetic of unplanned work at the organizational level. The deployment failure didn't just create a deployment crisis; it created a security crisis, a compliance crisis, a customer data crisis, and a regulatory crisis, all running simultaneously against the same depleted team. The blast radius of a single uncontrolled change expands until it hits every obligation the organization was trying to run in parallel.

---

## Management Observations

- **Steve's post-mortem scheduling is correct management under crisis.** He explicitly decouples the two problems: first, restore operations; then, run fifteen-minute accountability sessions with everyone who had a hand in the failure. He doesn't run the retrospective in the middle of the emergency — he schedules it for after the stores are running normally. Mixing blame with triage produces neither good triage nor good accountability.
- **The code freeze is the First Way applied under pressure.** Restricting deployments to twice daily, performance fixes only, is a deliberate reduction of change rate to allow the system to stabilize. Bill's instinct — and Chris's agreement — reflects the principle that a system under stress requires constraint of change, not acceleration of it. Sarah's instinct to add usability features during the crisis would have introduced new variables into an already-unstable system with no diagnostic headroom to absorb them.
- **The CVV on carbon paper is the compliance consequence of the "fallback we didn't think all the way through."** Designing a contingency for POS failure required thinking not just about operational continuity but about every constraint — security, compliance, auditability — that applies to customer payment data. The fallback was incomplete: it solved the operational problem while inheriting the compliance obligations of the primary system, without any of the controls the primary system had in place.
- **John's maneuvering of the auditors is a practical example of risk triage under crisis.** He bends the normal process — moves interviews to a different building, instructs security — to prevent a confirmable compliance violation from becoming a documented one. This is not obstruction; it is buying time to remediate a problem before it becomes a formal finding. The distinction matters: John is solving the compliance problem (destroy the prohibited data, process the transactions correctly), not hiding it.
- **Bill saying no — and being believed — marks a shift in organizational dynamics.** Before the Phoenix crisis, Bill was absorbing every demand from every direction. By Monday, his team is the critical path for keeping company operations running. That leverage — "we are the only thing keeping your stores alive" — gives him standing to decline new work in a way he didn't have before. Capacity constraints that are invisible in normal operations become legible when the constraint is the only team standing between the company and a front-page story.
- **The unexpected cooperation from Chris and John is the chapter's quiet signal.** A crisis that reveals the full consequences of the old operating model — siloed decisions, no shared accountability — also creates the conditions under which people start cooperating across silos. Chris agreed with Bill in the meeting; John offered engineers he didn't need to offer. Neither of these would have happened in Chapter 4. The crisis is changing the relationships.
