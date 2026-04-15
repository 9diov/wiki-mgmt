---
related-concepts:
  - "[[Throwing the Pig Over the Wall]]"
  - "[[The Four Types of Work ⭐]]"
sources:
  - "[[19-Chapter_14_•_Tuesday,_September_16|Chapter 14 — Tuesday, September 16]]"
---

# Chapter 14

## What Happens

Steve runs his post-mortem sessions with the leadership team, one at a time. Sarah comes out first, ashen and close to tears, after less than ten minutes. Bill and Chris go in together.

Steve directs the heaviest criticism at Chris — over $20 million invested, and the result was net damage to the company. He reminds them of the company's economics: a five percent net margin means every million dollars lost required twenty million in sales to earn. Then he delivers two announcements that weren't on the post-mortem agenda.

First, the board has decided to investigate splitting the company and selling it off in pieces. Steve is opposed but can't stop it — consultants are already engaged. Second, and more immediately: Steve has given Dick Landry, the CFO, the green light to evaluate full IT outsourcing. Dick has ninety days to select a vendor. If IT can pull off "some sort of miracle" in that window, Steve will consider keeping them in-house. Otherwise, everyone in IT — Bill included — may not have a job.

In the meeting, Bill pushes back on Steve's framing, pointing out that he had explicitly warned Steve about the deployment risk and been blown off. Steve acknowledges nothing. He tells Bill he's tired of Chicken Little predictions and wants solutions, not warnings after the fact.

After the meeting, Bill and Chris go to lunch. Over drinks they have the first honest conversation of their working relationship. Chris is depleted — he admits he used to love the work but finds it increasingly unsustainable. Technology changes faster than engineers can absorb. Product managers are arguing about feature backlogs three years out while the team can't reliably plan one year ahead. Development is hemorrhaging engineers to escalation support, which pulls them off feature work, which pushes deadlines, which lengthens deployment intervals, which causes them to batch more features into each deployment to justify the cycle time — which makes deployments harder and riskier.

Chris apologizes for his role in the Phoenix disaster. He explains that Sarah had asked him the earliest code-complete date without revealing she intended to present it to Steve as the go-live date. He should have listened to William's warnings. Bill accepts.

They agree to meet weekly and work together against the outsourcing threat. Chris promises to alert Bill if Sarah runs political interference again. Wes is notified of a post-Phoenix party in the Development building and immediately replies that his team is still fixing the transaction data from Development's code. Bill calls Wes and makes the case for going anyway: they need those relationships.

---

## The Common Death Sentence

Chapter 14 is where the novel's scope quietly expands. The Phoenix disaster is no longer just a deployment failure to be recovered from — it has triggered a board-level conversation about the company's future and a ninety-day countdown on IT's existence.

The outsourcing threat changes what "success" means for Bill. Before this meeting, success was stabilizing Phoenix and preventing the next crisis. After it, success requires demonstrating that IT can be a business asset within ninety days — not just a function that doesn't break things. The stakes have shifted from operational to existential.

The lunch conversation is structurally important for a different reason: it is the first time Bill and Chris talk as peers rather than as adversaries across a deployment boundary. What Chris describes from the Development side mirrors what Bill has been experiencing from the Operations side. Development is also overloaded. Development also has a fragmentation problem — engineers pulled to escalations, deadlines slipping, planning horizons collapsing. The deployment interval spiral Chris describes — deployments that used to take ten minutes now taking a week, compensated for by batching more features, which makes them longer still — is not a Development failure or an Operations failure. It is a system failure, and it is happening to both of them.

This is the chapter where the book begins reframing the Dev/Ops divide. The divide was visible in Chapters 3–4 as Development throwing problems over a wall. Chapter 14 shows that Development is also drowning, also operating without adequate process, also being damaged by the same absence of feedback and flow. The antagonism between Bill and Chris dissolves not because someone apologizes but because they recognize a common problem.

---

## Management Observations

- **Steve's outsourcing threat is a forcing function, not a punishment.** It sets a ninety-day window with a clear criterion: demonstrate that IT can deliver business value, or be replaced by someone who can. The threat is blunt but structurally useful — it converts a diffuse question ("is IT good?") into a concrete one ("can IT demonstrate enough value in ninety days to justify keeping?"). Bill's response — treat it as a "stay of execution" to work toward — is the correct one.
- **Bill's challenge to Steve in the meeting is right in content and risky in form.** Steve did dismiss Bill's warning email and redirect him to Sarah. That fact is accurate. But raising it in a post-mortem session in Steve's office, in front of Chris, produces no useful outcome — Steve is not going to accept responsibility in that setting — and burns credibility Bill will need later. The correct moment to establish accountability for that decision was in writing, at the time, which Bill did. The post-mortem is for analysis, not for winning the argument that he had already documented.
- **Chris's deployment interval spiral is the Development-side version of unplanned work accumulation.** Escalations pull engineers from features → deadlines slip → deployment intervals lengthen → more features get batched to justify the cycle → each deployment becomes larger and riskier → more escalations after each deployment. The spiral is self-reinforcing in the same way the Brent cycle is self-reinforcing. The mechanism is different; the structure is identical. Neither team can see the full loop because each team only sees its own half.
- **"The free puppy" captures the shadow IT problem precisely.** A summer intern builds a database reporting tool. Marketing adopts it for daily operations. IT inherits it without specifications, without security controls, without a support model — and then spends weeks building compliance scaffolding around something it didn't build and wasn't consulted about. The puppy was free; the operations and maintenance were not. This is the Type 2 and Type 4 work that accumulates off the books: IT projects and unplanned break-fix work created by business decisions that treated IT as a delivery mechanism, not a stakeholder.
- **Wes's reply about the party — "Mission Accomplished" — is operationally correct but strategically wrong.** His team is still bailing water while Development is celebrating. The frustration is legitimate. But the relationship between Development and Operations is the variable that determines whether the next deployment is better or worse than Phoenix. Bill's instinct — go to the party anyway, build the relationship — is correct at the strategic level even though it requires swallowing a real grievance.
