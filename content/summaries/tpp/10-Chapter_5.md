---
related-concepts:
  - "[[The Brent Problem ⭐]]"
  - "[[Uncontrolled Change ⭐]]"
  - "[[Change Advisory Board (CAB)]]"
sources:
  - "[[10-Chapter_5_•_Thursday,_September_4|Chapter 5 — Thursday, September 4]]"
---

# Chapter 5

## What Happens

Bill wakes to an urgent email from Steve: the Chief Audit Executive, Nancy Mailer, has called an 8 AM meeting about SOX-404 IT audit findings. He arrives to find Nancy, John, Wes, and an IT auditor named Tim assembled in silence.

Tim presents a 952-item audit report — 189 pages of eight-point type, compiled over eight weeks by a four-person team. Sixteen findings are significant deficiencies; two are potential material weaknesses. Many are repeat findings, now in their third year. The external auditors arrive in three weeks; Nancy needs a management response letter in six working days.

The two material weaknesses are the most damaging:
1. **No change management controls** — an unauthorized or untested change to a financial system could enter production without detection. The CAB meeting minutes required by policy don't exist because nobody attends the CAB.
2. **Developers have administrative access to production** — the segregation-of-duties control that would prevent fraudulent modifications to financial systems is absent. John's developer Max, who caused the payroll failure, is exhibit A.

Wes erupts at several findings he considers absurd (a MAX\_SYN\_COOKIE Windows setting), then escalates into a confrontation with John over patching fragile 20-year-old manufacturing ERP systems. Bill defuses it. John — who spent his political capital rushing the PCI tokenization deployment that caused the payroll failure — learns from Nancy that the SSN tokenization wasn't even in scope for the SOX-404 audit.

After the meeting, Bill asks Wes to stay behind. The conversation quickly circles back to Brent. When Bill points out that the audit remediation work will also require Brent, he erupts: *"Can't we do anything without him? If our organization can't do anything without one guy, we've got a big problem."*

Wes explains the full scope: Brent knows how every application talks to every other application at the enterprise level. Previous attempts to hire more senior engineers failed — half quit within a year, and Brent spent the rest of his time training them, leaving him stretched thinner than before.

Bill then asks what should have been his first question: what is the full list of IT's commitments? Wes and Patty can't answer. Business projects exist in Kirsten's PMO list. IT infrastructure projects have no central list. Work that arrives through personal relationships with IT staff is completely off the books. Nobody has ever aggregated the total demand against the total available capacity.

Bill directs Patty to build the list: one-liner per person, what they're working on, how long it will take. Start with Phoenix and audit resources. Identify who is most overloaded. The goal is a data-backed ask to Steve for more resources by Monday.

---

## The Situation Compounds

Three new structural problems surface:

- **952 audit findings, six days to respond.** The audit backlog is the direct result of years of deferred IT controls work — the same pattern as the SAN firmware and the test environment: legitimate requests denied or deferred, compounding silently until they become a crisis. The audit is now on the same timeline as Phoenix, competing for the same people.
- **No total work inventory exists.** IT has been operating without any aggregate view of demand vs. capacity. Commitments are made verbally, through email, via personal relationships with staff. Nobody — not Wes, not Patty, not Bill — knows what the organization has promised to do or when. Work gets bumped invisibly; the only signal that something slipped is when someone screams.
- **Hiring more Brents doesn't work.** Wes tried. The new engineers quit or underperformed, and Brent spent his remaining time training them. The knowledge concentration problem doesn't dissolve when you add headcount alongside the constraint — it gets worse, because the constraint absorbs the onboarding burden.

---

## Management Observations

- **The audit findings are the CAB problem made legal.** The material weakness finding — that an unauthorized change to a financial system could enter production undetected — is exactly what happened with John's tokenization deployment two days earlier. The audit finding is not theoretical; Parts Unlimited has already lived it. Bill's reboot of the CAB is now both an operational necessity and an audit remediation requirement.
- **John's tokenization deployment was wasted.** The urgent change that caused the payroll failure, bricked the SAN, and cost a day of recovery was fixing an audit finding that was never in scope for the SOX-404 audit. The damage was real; the compliance benefit was zero. This is what happens when security and compliance work bypasses the coordination process that would surface such misalignments.
- **Bill's question — "what is our total work inventory?" — is the chapter's turning point.** Until this moment, IT has been managed by assigning smart people to areas of responsibility and trusting them to handle what comes in. That model works when demand is predictable and capacity is sufficient. It fails exactly as Parts Unlimited is failing: silently, invisibly, until deadlines collide and the organization discovers it has promised the same people to five simultaneous priorities. The work inventory Patty is building is the first step toward managing IT as a system rather than a collection of individuals.
- **Wes's prediction about budget requests is important context.** He expects Steve to say no and cut 5% further. Every management ask has been denied for five years. The deferred SAN firmware, the missing test environment, the unfilled engineering positions — all are artifacts of a business that treats IT as a cost center to minimize rather than a capability to invest in. The audit findings are the compounded interest on that decision.
