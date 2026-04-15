---
related-concepts:
  - "[[Change Advisory Board (CAB)]]"
  - "[[The Brent Problem ⭐]]"
  - "[[Uncontrolled Change ⭐]]"
sources:
  - "[[21-Chapter_16_•_Thursday,_September_18|Chapter 16 — Thursday, September 18]]"
---

# Chapter 16

## What Happens

Dick Landry sends an all-executive email flagging a major crisis: no customer invoices have been sent for three days. Approximately $50 million in receivables is stuck in the system. The company will miss its end-of-quarter cash targets by a material amount unless the invoicing system is restored immediately.

Bill assembles the team. Patty presents all changes from the past 72 hours before any diagnosis begins. Bill establishes the incident command structure: "Do not touch anything without my approval." He invokes the Apollo 13 analogy — he's Gene Kranz, and he wants hypotheses backed by facts, not guesswork. The risk is not just downtime; it's data loss. By 6 p.m., Patty's team has documented twenty potential failure causes, narrowed to eight with assigned owners. They agree to reconvene at 10 p.m. Bill goes home for dinner and his son's bedtime reading.

He notes the contrast with earlier incidents: the previous Sev 1 had been full of finger-pointing and wasted time. Since then, Patty has run blameless postmortems and rehearsed the new procedures through mock incident calls. The 10 p.m. email traffic shows organized work, timelines, hypotheses, and coordination — everything the payroll failure lacked.

At 9:15 p.m., Steve calls. He's spoken with Dick, who says Bill is "dragging his feet." Steve demands Bill return to the office and get "all eyeballs on screens, all hands on keyboards." Bill pushes back: the payroll outage got worse because someone started screwing with the SAN without knowing what had caused the failure. Uncoordinated action in a complex environment creates more problems. He's building situational awareness before acting.

Steve tells him he also called Brent directly. Brent has expressed skepticism about Bill's approach, suggesting it separates people from the work that needs doing. Steve says he wants Brent on the problem now.

Bill responds that calling Brent in is exactly wrong — Brent is one of the reasons the hull is punctured in the first place. Bringing Brent in perpetuates the reliance. Every escalation to Brent makes the system less capable of solving the next problem without him.

Steve doesn't yield. He invokes the CEO authority: "Drawers open on my side of the desk. DEFCON 1. All hands on deck. Status updates every two hours."

Bill's response is immediate: "I don't know why you need me to do that. You're talking directly to my people, and you're calling all shots on the ground. Do it yourself."

Then: "Expect my resignation in the morning."

Paige stares at him wide-eyed from across the hallway.

---

## The Incident Command Principle

Chapter 16 crystallizes a management idea that has been building since the payroll failure: the most dangerous thing a leader can do in a complex incident is send everyone into action before establishing situational awareness.

Bill's Apollo 13 framing is not rhetorical. The actual Gene Kranz protocol during the Apollo 13 emergency was to stop all action, establish what was actually known versus assumed, generate hypotheses, and then test them methodically. The instinct — all hands on deck, do something — is precisely what Kranz suppressed, because premature action in a system-state you don't understand creates new problems on top of the existing one.

The payroll outage is the proof case Bill cites. Someone screwed with the SAN without knowing it was in the failure's causal chain, added six hours to the outage, and nearly lost payroll data. "More people doing more things faster" is not a risk-reduction strategy in an environment of high uncertainty. It is a risk-multiplication strategy.

The chapter also surfaces a structural weakness in Bill's position: Steve can call Brent directly. Brent can give Steve his own read on the situation. Bill's authority over the incident management process does not extend to controlling the information channel between his engineers and the CEO. Brent, genuinely skeptical of Bill's process-oriented approach, tells Steve something that sounds reasonable to Steve — and the result is an executive override that dismantles exactly the discipline Bill has been building.

The resignation is a logical endpoint to that structural problem. If the CEO calls the plays directly, the VP of Operations is accountable for outcomes he doesn't control. Bill's argument is precise: you can't have both — either he has authority to run the incident, or Steve does. Bill is willing to abdicate. He is not willing to carry accountability without authority.

---

## Management Observations

- **"Do not touch anything without my approval" is the incident command equivalent of work release control.** Just as the CAB releases changes at a controlled rate before they enter production, incident management requires a controlled rate of intervention before engineers touch production during an active failure. Uncoordinated action during an incident is unplanned change — with all the same properties: invisible to others, potentially compounding, impossible to roll back.
- **Patty opening with the 72-hour change timeline is now the default first move.** This is the CAB's most operationally important secondary function: when something breaks, the first diagnostic question is always "what changed?" The change board converts that question from a memory exercise to a lookup. Bill notes the contrast with earlier incidents; the process is working.
- **Steve calling Brent directly is the organizational failure mode that Bill's containment design was trying to prevent.** The no-keyboard rule, the level-3 pool, the gated access — all of these were designed precisely because executives with urgency will go around the constraint protection to get the fastest answer. The containment design only works if people at the top enforce it, not just people in the middle.
- **Brent's skepticism of Bill's process is the constraint protecting itself.** Brent is not being malicious. From his vantage point, Bill's approach looks like bureaucracy that slows things down. Brent's entire career has been built on the "call me and I'll fix it" model. He is genuinely faster than the process in any individual incident. He is also the reason the system cannot fix incidents without him. His preference for direct action is structurally rational from his position and structurally damaging from the system's position.
- **The resignation is about authority-accountability parity.** Bill's logic is exact: if Steve is calling the plays, Steve is accountable for the outcomes. Carrying accountability for a process he no longer controls is not acceptable. The resignation is not impulsive — it is the logical terminus of "you can do it yourself" applied consistently. Whether it is wise is a different question; whether it is coherent is not in doubt.
