---
related-concepts:
  - "[[Uncontrolled Change ⭐]]"
  - "[[Throwing the Pig Over the Wall]]"
  - "[[Change Advisory Board (CAB)]]"
sources:
  - "[[08-Chapter_3_•_Tuesday,_September_2|Chapter 3 — Tuesday, September 2]]"
---

# The Tokenization Incident

## The Setup

The payroll failure that greets Bill on his first day as VP of IT Operations is traced, after a full day of investigation, to a single unannounced change.

John Pesche, the CISO, had directed a developer to tokenize the Social Security Number fields in the timekeeping database — a security improvement required for compliance. The change was made without notifying anyone, without a change ticket, and without a test environment. The developer used a production database as the de facto test environment. The timekeeping system appeared to work correctly afterward, so he considered it complete.

What John's team had not known: Payroll's database queries read those SSN fields in a specific format. The tokenization changed the format. When payroll ran the next morning, the queries failed. The payroll system had been working correctly for years; it had never been told anything about its dependency on timekeeping's SSN format.

Bill's investigation team reconstructs the timeline by combing through system logs, because no change ticket exists to consult.

## What It Illustrates

**[[Uncontrolled Change ⭐]]** — The tokenization change was well-intentioned, technically correct within its own scope, and completely invisible to the systems it affected. There was no mechanism to ask: *does anyone else need to know about this?* The payroll system's dependency on the SSN format was real and exploitable; it simply wasn't documented anywhere that John's team could see. The incident is the book's canonical example of how a change that is "done" from one team's perspective can be a failure from another team's perspective — not because anyone was negligent, but because the left hand didn't know what the right hand was doing.

**[[Throwing the Pig Over the Wall]]** — John's team considered the change complete when the timekeeping system kept functioning. What "complete" means was implicitly defined as "our tests pass" — not "downstream consumers continue to function." This is the handoff gap: the team making the change had no obligation to verify that changes were safe for systems they hadn't written or operated.

**[[Change Advisory Board (CAB)]]** — The tokenization incident is one of the two incidents (alongside the SAN firmware failure) that motivates Bill to reboot the CAB. The goal of the CAB is precisely to answer the question John's change skipped: before this change goes in, does anyone else need to know?
