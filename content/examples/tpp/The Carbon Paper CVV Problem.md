---
related-concepts:
  - "[[Throwing the Pig Over the Wall]]"
  - "[[Uncontrolled Change ⭐]]"
sources:
  - "[[18-Chapter_13_•_Monday,_September_15|Chapter 13 — Monday, September 15]]"
---

# The Carbon Paper CVV Problem

## The Setup

When the Phoenix database conversion failure takes all 120 store POS systems offline, the operational fallback is carbon paper credit card imprinters — the kind of manual swipe machines that predate electronic authorization. Store managers send employees to office supply stores to stock up on carbon paper slips. The fallback works: stores can transact.

On Monday, John walks into the Finance war room where Ann's team is processing problem orders from the stores. The faxes coming in from stores are scanned images of the carbon paper slips. John picks up a stack and goes pale. He pulls Bill into the hallway.

The carbon paper slips have captured CVV codes — the three-digit card verification values printed on the back of customers' cards. Under PCI DSS, storing or transmitting CVV codes is prohibited; even possessing them constitutes a cardholder data breach. The fines scale with the number of affected cardholders. Ann's team has been routing, faxing, and filing stacks of them for two days.

The PCI auditors are on-site today, in the building, doing scheduled interviews. They are supposed to use the conference room currently serving as the Phoenix recovery war room.

## What It Illustrates

**[[Throwing the Pig Over the Wall]]** — The carbon paper fallback was designed for operational continuity: if the electronic systems go down, stores can still process sales. What wasn't designed into the fallback was any of the compliance and security constraints that apply to customer payment data. The primary POS system had controls — no raw CVV storage, encrypted transmission, audit trails. The fallback had none of those controls and nobody had checked whether it needed them.

This is the same pattern as the handoff gap in deployments: a solution that works within its own scope (stores can transact) while inheriting obligations from the domain it's substituting for (cardholder data regulations still apply to a manual swipe just as they apply to an electronic one). "Fallback mode" does not mean "compliance-free mode."

**[[Uncontrolled Change ⭐]]** — The fallback became necessary because of the database conversion failure, which was itself a consequence of the deployment proceeding without adequate pre-verification. The CVV problem is two steps downstream from the original uncontrolled element — a reminder that the blast radius of a deployment failure extends not just into the systems that break, but into the contingency responses that the failure forces into use.
