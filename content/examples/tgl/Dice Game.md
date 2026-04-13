---
related-concepts:
  - "[[Dependent Events and Statistical Fluctuations]]"
  - "[[Balanced Plant Fallacy]]"
  - "[[Throughput, Inventory, and Operating Expense ⭐]]"
sources:
  - "[[20-Chapter_14|Chapter 14 — The Dice Game]]"
---

# Dice Game

## The Setup

After the hike, Rogo runs a controlled experiment at the picnic area to prove that what he observed wasn't just bad luck or an uncontrolled field observation.

**Setup:**
- Five bowls in a line → five dependent events (stations in a production sequence)
- One die per station → statistical fluctuations (range 1–6, average 3.5)
- Market demand = 3.5 per turn — capacity is perfectly balanced to demand
- Each turn: roll the die, move up to that many matches from your bowl to the next; you can't move more matches than you currently have
- Five boys (Andy through Evan) each man one station
- Expected throughput after 20 turns: 70 matches (3.5 × 20)

Everything is designed to be fair. Average capacity equals average demand. No external shocks.

**What happens:**

After 10 rounds, actual throughput is 20 matches. Expected was 35. The system shipped roughly half of what the balanced capacity calculation predicted. Dave's bowl — station 4 — holds 11, 14, then 17 matches in successive turns. Andy at station 1 stays near average. Evan at station 5 (the exit, the one that produces throughput) falls into a deficit he can never recover from.

The further from the front, the worse the deviation. The problem is worst at exactly the station that matters most.

## What It Illustrates

**[[Dependent Events and Statistical Fluctuations]]** — The dice game is the mathematical proof that the Boy Scout Hike was not an anomaly. With perfectly average capacity, perfectly random fluctuations, and five dependent steps, throughput reliably falls below the mathematical expectation and inventory reliably accumulates downstream. The deviation grows over time; it does not self-correct. "Averages are not additive in dependent systems" — you cannot take five stations each averaging 3.5 and assume the system averages 3.5.

**[[Balanced Plant Fallacy]]** — The game was explicitly designed as a balanced plant: average output equals average demand at every station. The result is the proof that this design is not neutral — it is structurally guaranteed to underperform. The expected 70 matches is what a balanced-capacity model predicts. The actual ~40 is what the physics of the system produces.

**[[Throughput, Inventory, and Operating Expense ⭐]]** — The game tracks all three simultaneously. Throughput (matches shipped by Evan) falls below expectation. Inventory (matches in bowls, especially late in the chain) climbs continuously. If the matches carried holding costs, operating expense would rise too. All three measurements move in the wrong direction — in a system that looks perfectly designed on paper.
