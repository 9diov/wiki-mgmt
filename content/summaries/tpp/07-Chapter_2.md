---
related-concepts:
  - "[[The Brent Problem ⭐]]"
  - "[[Uncontrolled Change ⭐]]"
sources:
  - "[[07-Chapter_2_•_Tuesday,_September_2|Chapter 2 — Tuesday, September 2]]"
---

# Chapter 2

## What Happens

Bill leaves Steve's office and immediately works the payroll crisis. He meets CFO Dick Landry and his Operations Manager Ann in Finance. Ann walks through the problem on a whiteboard: the payroll system receives hourly employee data from timekeeping systems in each division; yesterday's upload zeroed out all hourly worker records. Salaried employees are fine — only hourly staff are affected.

A troubling detail surfaces: IT previously gave Finance a manual correction tool so they could fix upload errors themselves, without having to involve IT. Ann used it, but can't fix what she can't see — the upstream data is simply missing.

The fallout if the 5 PM electronic payment window is missed: the only fallback is to reuse last pay period's data, which means paying people the wrong amounts, creating financial reporting errors, and triggering extended SOX-404 audit scrutiny. Dick gives Bill until 3 PM to fix it before they implement the messy plan B.

Bill then walks to Building 7 — IT's building, visibly the worst-maintained on campus — to find Wes Davis (Director of Distributed Technology Operations) and Patty McKee (Director of IT Service Support). Both are in the middle of a Severity 1 incident call around the speakerphone. Bill pulls them aside.

He delivers the news: Luke and Damon are gone. He's their new boss. Wes is hostile — he worked with Damon for years and questions whether Bill, whose career has been in midrange systems, is capable of running modern distributed infrastructure. Patty is calm and immediately supportive. Bill doesn't take the bait from Wes; he redirects to the payroll problem.

The technical picture is murkier than expected: a SAN firmware upgrade was in progress yesterday when the payroll run failed. Brent — a senior engineer everyone depends on — decided the SAN was corrupting data and tried to roll it back. The rollback bricked the SAN entirely; it won't boot and is now displaying error messages in what appears to be kanji. Hundreds of systems that depend on the SAN for storage are now down.

But Bill notes a problem with the SAN theory: if the SAN failed broadly, why aren't there much wider outages? The payroll failure may not be related to the SAN at all. The chapter ends with the three of them walking to Brent's desk to establish an accurate timeline.

---

## The Situation Set Up

Several structural problems become visible in this chapter:

- **IT gave Finance a workaround and called it a solution.** The manual correction tool exists because the payroll upload fails often enough that Finance needed a way to fix it without waiting for IT. The "solution" is a dangerous one — Finance personnel with direct access to payroll data outside the application, with no audit trail.
- **A key-person dependency is already visible.** Brent appears in Chapter 2 as the engineer everyone turns to when something serious breaks. He was the one who diagnosed the SAN, recommended the rollback, and is now the only person working the fix. He was also pulled off Phoenix work to do it. This single point of failure will recur throughout the book.
- **Simultaneous crises are already in conflict.** The SAN issue, the payroll failure, and the Phoenix virtual machine work for Sarah are all competing for the same people — specifically Brent — right now, on Bill's first day.
- **The IT building is a physical metaphor.** Building 7 has oil seeping through the carpet, peeling paint, and outdated infrastructure. The business has underinvested in IT for years, and the environment shows it.

---

## Management Observations

- **Bill's first move is to understand the problem from the business side before touching the technology.** He goes to Finance before going to the NOC. This sequence matters: he establishes what "fixed" looks like from the business perspective — pay correct amounts by 5 PM — before trying to diagnose the IT cause. He also buys time explicitly (3 PM decision point) rather than accepting the panic as the default operating mode.
- **The SAN theory is being chased because it's visible, not because it's correct.** The NOC team is deep into a SAN vendor call, coordinating a fifteen-person bridge, before anyone has established whether the SAN and the payroll failure are actually connected. Wes is doing what feels productive; it may not be what's useful.
- **Wes's hostility is organizational friction made personal.** His challenge to Bill isn't irrational — he watched a peer get promoted over him, and he has a legitimate grievance that he wasn't consulted. But the form it takes (attacking Bill's technical credentials mid-incident) is exactly the kind of behavior that makes outages worse. Bill's response — redirect to the work, offer to take it to Steve — is the right one.
- **"That doesn't work for solving crimes, and it definitely doesn't work for solving outages."** Patty's instinct to establish an evidence-based timeline before acting is the chapter's sharpest operational observation. The team has been running on hearsay since the failure started; going to Brent's desk to reconstruct what actually changed and when is the first move toward genuine diagnosis.
