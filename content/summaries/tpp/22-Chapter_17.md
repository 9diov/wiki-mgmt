---
related-concepts:
  - "[[The Brent Problem ⭐]]"
  - "[[Uncontrolled Change ⭐]]"
sources:
  - "[[22-Chapter_17_•_Monday,_September_22|Chapter 17 — Monday, September 22]]"
---

# Chapter 17

## What Happens

Four days after his resignation, Bill takes his three-year-old son Grant to the train station — a promise he'd been unable to keep since starting the VP role. He is sleeping better than he has in weeks.

Wes and Patty reach him by phone. Steve had done exactly what Bill predicted: brought in all the engineers including Brent, demanded "hands on keyboards," and called for a general sense of urgency. The result: the teams didn't coordinate well enough. The inventory management systems are now down too. Finance cannot get the data needed to close the books for the quarter — cost of goods sold, gross margins, net margin are all unavailable. The CFO's staff are "about to jump from window ledges."

Bill is not surprised. He tells Wes and Patty he's proud of what they built together, advises them not to let anyone call the shots on their behalf, and hangs up to get back to Grant.

Steve calls three times on the drive home. Bill doesn't pick up. When he gets home, Paige tells him Steve called her too — apparently after a significant conversation with Erik — and wants to apologize and make a proposition.

Steve's voicemail and subsequent call are markedly different in tone. He acknowledges he hasn't been fair, that delegating IT issues to Sarah was a mistake, and that Bill has done everything right. He says Erik held his feet to the fire until he understood something important. He asks Bill to return for ninety days as VP of IT Operations, with the explicit framing that they need to work together "as the two sides of a dysfunctional marriage." If Bill still wants to leave at the end of the ninety days, he can go with a one-year severance package.

Paige extracts a promise from Bill to listen with an open mind. Bill calls Steve back. The conversation lasts forty-five minutes.

---

## The Cost of "All Hands on Deck"

Bill's prediction from Chapter 16 is now confirmed in its most specific form. The invoicing failure was a bounded, diagnosable problem. Steve's override — uncoordinated mass action, everyone on keyboards — introduced enough uncontrolled change into an already-fragile system that inventory management went down alongside it.

The second failure is not caused by bad intentions or incompetent engineers. It is caused by the same property that made the payroll failure worse in Chapter 2: multiple people making multiple changes to an interdependent system without anyone tracking what was changing, what was being touched, and what interactions might exist. The incident command protocol Bill had designed was precisely to prevent this. The protocol was overruled.

The chapter also marks the first significant change in Steve. His prior stance — "drawers open on my side of the desk," "I'm Captain Kirk" — has shifted. Erik has reached him in a way that Bill couldn't, which is itself a structural observation: sometimes the person with the most to lose from the problem cannot be the one who explains the problem to the decision-maker. A third party without a stake in the outcome can carry the same message further.

---

## Management Observations

- **The inventory collapse is a textbook case of incident response making things worse.** A focused failure (invoicing system) became a systemic failure (invoicing + inventory + quarterly close) not because the original problem was complex, but because the response was uncoordinated. Adding more hands to a system in an unknown failure state without coordination is adding more uncontrolled changes — each one a potential interaction with the failure or with someone else's simultaneous action.
- **Wes and Patty's call is the clearest evidence yet that the team has internalized what Bill built.** They call because they know what went wrong and why. They're not confused about the cause; they're reporting the exact failure mode Bill predicted. A team that can diagnose the cause of its own failures is a team that has learned. The process is resident in them, not just in Bill.
- **Erik coaching Steve is a structural necessity, not a redundancy.** Bill had told Steve the same things, repeatedly, and been overruled. Erik told Steve the same things once and produced an apology and a proposition. The content was the same; the relationship was different. Bill had stakes in the outcome (his job, his team, his decisions). Erik had none. The advice was received differently because the messenger's credibility came from a different source.
- **Steve's framing — "two sides of a dysfunctional marriage" — is the novel's first acknowledgment of a shared IT-business problem.** Every prior framing put IT as the party that failed. This framing puts both IT and the business as parties to a relationship that isn't working — and both as parties who need to change. Whether this reflects genuine understanding or diplomatic language will become clear in subsequent chapters.
