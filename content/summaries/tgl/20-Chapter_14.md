---
related-concepts:
  - "[[Dependent Events and Statistical Fluctuations]]"
  - "[[Balanced Plant Fallacy]]"
  - "[[The Constraint ⭐]]"
  - "[[Goal Formulation]]"
---

# Chapter 14

## What Happens

Lunch at the picnic area. Rogo is still wrestling with whether the hike analogy actually proves anything — maybe a truly balanced system, with capacity set exactly equal to demand, would behave differently.

He borrows a die from a Scout, finds some matchsticks and bowls, and runs a controlled experiment: the **dice game**.

**Setup:**
- Five bowls in a line → five dependent events (stations in a production sequence)
- One die → statistical fluctuations per station (range 1–6, average 3.5)
- Market demand = 3.5 per turn (perfectly balanced — capacity equals demand)
- Each turn: roll the die, move up to that many matches from your bowl to the next; you can't move more than you have
- Expected throughput after 20 turns: 70 matches (3.5 × 20)

Five boys play: Andy, Ben, Chuck, Dave, Evan — first to last in the chain.

**What actually happens:**

The front of the chain (Andy, Ben) performs near average. But downstream, the bowl inventories accumulate in waves. When the front rolls low, nothing reaches the back. When the front finally rolls high, the back may roll low and can't pass it on. The delays compound through the chain, station by station.

After 10 rounds, actual throughput: **20 matches**. Expected: 35. The system shipped roughly half of what a balanced system "should" have delivered. Inventory at Dave and Evan's bowls has ballooned — by turns 8–10, Dave's bowl alone holds 11, 14, and 17 matches respectively.

The further from the front, the worse the deviation. Andy stays near average; Evan falls into a hole he can never climb out of. The problem is worst at exactly the point that matters most — the final step, the one that produces throughput.

Rogo stares at the chart:

> *"I still can hardly believe it. It was a balanced system. And yet throughput went down. Inventory went up. And operational expense? If there had been carrying costs on the matches, operational expense would have gone up too."*

Expected to ship 35, shipped 20. If real customers were waiting, more than half of all orders would be late. "All of that sounds familiar, doesn't it?"

The boys want to keep playing. Rogo runs out of paper tracking Dave and Evan's scores.

## What the Dice Game Proves

The hike was an observation — real but uncontrolled. The dice game is a proof. With exactly balanced capacity (average output = average demand), no variability in the average rate, and no external disruptions:

- **Throughput reliably falls below the expected average**
- **Inventory reliably accumulates, especially late in the chain**
- **The deviation grows over time — it does not correct itself**

This is the mathematical proof Jonah referenced in Chapter 11. The result is not a run of bad luck; it is the structural consequence of [[Dependent Events and Statistical Fluctuations|dependent events combined with statistical fluctuations]]. Every manager who has ever wondered why the plant is "always behind" despite "good average efficiency" has been living inside this chart.

## Management Observations

- **The damage accumulates downstream.** Andy looks fine — he's hitting average. The disaster is at Evan's bowl, the last step before shipping. A plant can *feel* busy and productive throughout while a backlog silently accumulates at the exit.
- **Averages are not additive in dependent systems.** You cannot take five stations each averaging 3.5 and assume the system averages 3.5. The dependency means the system average is always lower than any individual station average.
- **The chart looks like the Grand Canyon, not a sine wave.** Inventory doesn't oscillate around a mean — it drifts downward in staircase patterns as delays compound. The natural expectation (it will average out) is mathematically wrong.
