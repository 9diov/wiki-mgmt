---
related-concepts:
  - "[[Throwing the Pig Over the Wall]]"
  - "[[The Brent Problem ⭐]]"
  - "[[Change Advisory Board (CAB)]]"
  - "[[Uncontrolled Change ⭐]]"
sources:
  - "[[09-Chapter_4_•_Wednesday,_September_3|Chapter 4 — Wednesday, September 3]]"
---

# Chapter 4

## What Happens

Bill arrives at his desk to find 526 unread emails and 62 voicemails. The first crisis of the morning is an email from Sarah Moulton (SVP Retail Operations), cc'd to Steve, accusing Bill's team of holding up Phoenix and demanding he explain the delays at a 10 AM meeting.

Bill calls Wes, who explains: Brent was supposed to configure virtual machine environments for the Phoenix development team two weeks ago. He never finished because he got pulled onto the payroll/SAN crisis. The specification from Development is still incomplete anyway — every time Ops delivers something, Dev says it's wrong.

At the 10 AM meeting, attended by Sarah, Chris Allers (VP App Dev), Kirsten Fingle (PMO), and — unexpectedly — Steve Masters, Kirsten opens with the assessment that Phoenix is red and the deadline is in grave jeopardy: last week, only 3 of 12 critical-path tasks were completed. Steve turns and looks directly at Bill.

Bill explains Brent was absorbed by the payroll emergency. Sarah dismisses this and attacks Bill's team's sense of urgency. Bill deflects cleanly by asking Sarah which she would have prioritized — paying factory workers or Phoenix tasks — and attributing the priority to Steve. Sarah backs down.

Chris then volunteers a go-live date of one week from Friday (September 12), apparently to stop the bleeding in the room. Wes erupts: Development never provided a hardware specification, the code is performing at 4 transactions per second against a 250 TPS target, the required gear has a three-week vendor lead time, and no real performance testing has been done. Bill adds that deploying an untested system risks driving customers to competitors. Steve overrules all objections. The launch date is set: September 12, 5 PM.

After the meeting, Bill learns from Wes that Brent couldn't attend the Phoenix architecture planning meetings because he was always fighting fires — the same fires that are now blocking the Phoenix deployment. The cycle is self-reinforcing.

Back at his desk, Bill's laptop crashes — a Patch Tuesday security rollout from John's team has bricked over 200 laptops company-wide. His replacement is a ten-year-old machine with taped-on battery and worn keys.

Bill attends the rebooted CAB meeting. Only Patty is there. She explains the previous attempt: two years of ITIL consulting, a new tool, a formal process — and it collapsed because engineers spent 20 minutes filling out forms for 5-minute changes, managers stopped attending, and John eventually stopped enforcing it too. Bill sends a mandatory attendance email for Friday's CAB.

Wes calls immediately, furious about the change management mandate, recounting the previous CAB collapse in detail. Bill holds firm but asks Wes to help build the solution rather than fight it.

---

## The Situation Compounds

Chapter 4 introduces three new systemic problems layered on top of the ones already established:

- **Development and Operations have no handoff process for Phoenix.** Dev has been making promises to the business about deployment dates without involving Ops in the planning. The specification for the production environment is still incomplete. Neither side has formal ownership of the gap between "code is done" and "code runs in production."
- **Brent's absence from planning meetings is caused by the same fires that make his absence catastrophic.** He can't attend Phoenix architecture meetings because he's fixing broken things. Those broken things compound into Phoenix delays. The constraint is not just Brent's time — it is the lack of any mechanism to protect planning work from reactive work.
- **Change management has failed twice and is being attempted a third time.** The first attempt died from bureaucratic overhead; nobody used the tool because it was too slow. The second was killed when the team staged a rebellion. The third attempt (Bill's mandate) starts from the same position: a process nobody believes in, a tool nobody uses, and two managers openly at war over it.

---

## Management Observations

- **Sarah's political move and its limits.** Cc'ing Steve on an attack email is a classic escalation tactic — it forces the target to perform accountability in public rather than resolve the issue privately. Bill neutralizes it by redirecting the priority question back to Steve, making Sarah's attack land on the person she was appealing to. It works once, but the underlying dynamic — Sarah using Phoenix urgency as a weapon — is not resolved.
- **Chris's arbitrary date is the book's first explicit "throwing the pig over the wall."** He names September 12 to end the political pressure in the room without consulting Operations on feasibility. Bill's "pig over the wall" framing captures the structural pattern: Development treats deployment as someone else's problem once code is complete, leaving Ops to absorb all the risk and late-stage work under an immovable deadline.
- **The Patch Tuesday laptop failure is the book's second demonstration that uncoordinated change causes damage.** John's security team pushed patches that bricked over 200 machines without warning or staging. It is structurally identical to the tokenization deployment in Chapter 3: a legitimate compliance action, executed without change coordination, creating a production failure. The pattern is now established — it is not a one-off.
- **Wes's CAB history is a real warning, not just resistance.** His description of the previous process collapse is accurate and specific: 20-minute forms for 5-minute changes, mandatory meetings that consumed half the engineering week. A change management process that imposes more friction than it prevents will always be routed around. Bill's mandate is necessary but not sufficient — the process itself has to be designed to be fast enough to use.
- **IT Operations is fighting a three-front war.** Bill's closing observation names it: his team is under pressure from Development (Phoenix delays), Information Security (Patch Tuesday, tokenization), and Audit (SOX, PCI) — and his own two primary managers are in open conflict with each other. Every organization around IT treats it as a shared resource to be consumed on demand, with no one accountable for the total load.
