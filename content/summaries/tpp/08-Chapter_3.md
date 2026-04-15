---
related-concepts:
  - "[[Uncontrolled Change ⭐]]"
  - "[[Change Advisory Board (CAB)]]"
  - "[[The Brent Problem ⭐]]"
sources:
  - "[[08-Chapter_3_•_Tuesday,_September_2|Chapter 3 — Tuesday, September 2]]"
---

# Chapter 3

## What Happens

Bill, Patty, and Wes go to Brent's workstation — a six-cubicle-wide setup with four monitors and stacks of servers — to reconstruct the timeline. Brent explains: he was helping a SAN engineer run a firmware upgrade the previous evening. It ran long and got difficult, finishing around 7 PM. When the SAN rebooted, the self-tests started failing. Fifteen minutes into troubleshooting, alerts about the payroll run failure came in. Brent concluded the two events were connected and recommended rolling back. The rollback bricked the SAN entirely.

While they're talking, Ann calls with a new detail: the corrupted payroll data isn't a global failure — it's specifically the Social Security Number field for hourly employees, now full of garbled characters. Brent recognizes the pattern immediately: a developer named Max called him the previous day asking a quick question about database table structure. He gave Max a fast answer and moved on.

The NOC conference line surfaces Max's manager, who confirms: Max was helping deploy something for John Pesche, the CISO, and went on vacation that morning.

Bill and Patty call John. He confirms: his team deployed a tokenization application to fix a PCI audit finding, replacing stored Social Security numbers with tokens to comply with data privacy regulations. The auditors are on-site the following week, the work had been delayed for a year, and John bypassed the change management process because the official process would have scheduled the deployment four months out.

Critically: the change was deployed directly into production. There is no test environment — IT requested budget for one years ago and never got it.

Back on the timeline, Patty reveals the full scope: no functional change management process exists. Nobody logs changes in a central system. The change advisory board (CAB) has been tried before and fizzled each time. Getting a change inventory means emailing all of IT and asking what they did.

Bill mandates the next CAB meeting — tomorrow — as non-optional and attends as the new VP.

The chapter ends in three beats: at 2 PM Patty confirms 27 changes in the past three days, two of which are plausible causes; at 3 PM Bill tells Dick and Ann plan B is the only option; at 7 PM the timekeeping app is restored; at 11 PM the SAN comes back online. Bill comes home after midnight, missing the celebration his wife organized. He reads a news article — the Herald Times has the story, the union is calling the failure "unconscionable," and the company is on the front page.

---

## The Root Cause

The chapter peels back two layers of failure:

- **The direct cause** was John's tokenization deployment corrupting the SSN field in the timekeeping database. A security compliance change, rushed to meet an audit deadline, was deployed without testing, without coordination, and without anyone in Operations being informed.
- **The enabling cause** is the absence of any functional change management process. Twenty-seven changes were made in three days and only two are even traceable. The change advisory board exists on paper; in practice, everyone bypasses it. No test environment exists because the budget request was denied years ago.

The SAN failure was a separate, compounding incident: a long-deferred firmware upgrade attempted without an adequate maintenance window, which Brent's rollback then turned into a full outage.

---

## Management Observations

- **Uncoordinated changes are the primary source of IT instability.** The payroll failure was not caused by neglect or incompetence — it was caused by a security engineer deploying a well-intentioned change that nobody else knew about. The SAN failure was caused by a deferred maintenance upgrade nobody else coordinated around. Both failures share the same root: changes entering production without visibility or review.
- **Security operating outside the process is a structural problem, not a personnel problem.** John's decision to bypass change management is rational from his perspective: the process would have taken four months, the auditors arrive next week. The problem is that the process is too slow to be usable, so people route around it. The solution is not to discipline John — it is to make the process fast enough to actually use.
- **Brent is already the single point of failure.** In one day, Brent was the engineer running the SAN upgrade, the person Max called for database advice, and the person now fixing the bricked SAN — all simultaneously. He is the invisible load-bearing wall. When he makes a quick, distracted answer to Max's question, the consequences compound across systems he isn't even directly working on.
- **The no-test-environment problem is a leadership failure, not an engineering failure.** The budget request was made and denied. John's team deployed to production because there was nowhere else to deploy to. The technical debt isn't on the engineers who worked around the constraint — it is on the decision to deny the budget.
- **Bill's first day ends on the front page.** Steve's framing in Chapter 1 — "never let the toilets flood the building" — has been violated immediately and publicly. The newspaper story is not just bad press; it is the first concrete demonstration of what unmanaged IT change costs at the organizational level.
