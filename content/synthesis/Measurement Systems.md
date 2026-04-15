---
books-compared:
  - "[[The Goal (TGL)]]"
  - "[[Toyota Production System (TPS)]]"
  - "[[High Output Management (HOM)]]"
concepts:
  - "[[Throughput, Inventory, and Operating Expense ⭐]]"
  - "[[Financial Measurements]]"
  - "[[Productivity]]"
  - "[[Takt Time ⭐]]"
  - "[[Value-Added Work]]"
  - "[[Standard Work]]"
  - "[[Seven Wastes (Muda) ⭐]]"
  - "[[Managers Output ⭐]]"
  - "[[Leverage ⭐]]"
  - "[[Indicators ⭐]]"
  - "[[Management by Objectives ⭐]]"
---

# Measurement Systems — Across Three Books

All three books open with the same diagnosis: the measurements organizations use are wrong. Not inaccurate — wrong in kind. They measure the wrong things, reward the wrong behaviors, and systematically obscure what actually matters. Each book then proposes a replacement measurement system built on a different philosophical foundation.

The disagreement between them is real and instructive: they do not measure the same thing, they do not define "better" the same way, and they cannot be trivially unified. But they share a common critique — *activity is not output* — and the tensions between their frameworks reveal something important about what organizations are actually trying to do.

---

## The Goal: Measure the Flow of Money

Goldratt's central measurement insight is that conventional accounting actively generates bad decisions. Because labor is embedded in the cost of work-in-process inventory, a plant that produces and stockpiles goods *appears* more productive — the "asset" value grows. This accounting convention incentivizes overproduction directly.

His replacement is **[[Throughput, Inventory, and Operating Expense ⭐]]** (T/I/OE):

- **Throughput (T)** — the rate at which the system generates money *through sales*. The key word is *sales*: producing something that sits in a warehouse is not throughput. This one definition breaks the incentive to overproduce.
- **Inventory (I)** — all money invested in things the system intends to sell. Labor is explicitly excluded; it goes into Operating Expense. Inventory is just trapped capital, full stop.
- **Operating Expense (OE)** — all money spent turning inventory into throughput.

The goal becomes: increase T, decrease I, decrease OE — simultaneously. Any decision is evaluated by its effect on all three. A local cost reduction that suppresses throughput is wrong. An investment that increases throughput faster than it raises OE is right.

T/I/OE sits above the financial measurements (net profit, ROI, cash flow) as a bridge to operational decisions. [[Financial Measurements]] tell you whether the company is making money; T/I/OE tells you *why* and gives you actionable levers. The financial measurements can't tell a plant supervisor whether to run a particular batch. T/I/OE can.

The key distinction T/I/OE unlocks is **[[Activation vs Utilization]]**: a machine producing parts the constraint cannot absorb is *activated* but not *utilized*. It increases I without increasing T. By conventional accounting it looks productive — parts are being made, the machine is busy. By T/I/OE it is moving the plant away from its goal.

Goldratt's framework defines [[Productivity]] as goal-directed: an action is productive if and only if it moves the system toward its goal (more T, less I, less OE). This is the measurement analogue of the constraint insight — productivity cannot be local.

---

## TPS: Measure the Flow of Work

Ohno's measurement system operates in physical, not financial, terms. The primary instruments are **takt time**, **waste classification**, and the **value-added ratio** — none of which involve money directly. The premise is that if waste is eliminated and flow is achieved, the financial results will follow. The financial results are not the target; they are the consequence.

**[[Takt Time ⭐]]** is the system's heartbeat: available operating time divided by required daily quantity. It is simultaneously a production target (every process must complete one unit per takt period), a staffing calculator (required headcount = total work content ÷ takt time), and a diagnostic tool (if a worker cannot complete their sequence within takt, there is a problem requiring investigation).

Takt time also yields the sharpest distinction in TPS measurement: **operating rate vs. operable rate**. Operating rate measures how often a machine runs relative to full capacity — the metric conventional manufacturers maximize. Operable rate measures whether a machine is ready when needed. TPS targets 100% operable rate and whatever operating rate takt time requires — often well below 100%. A machine running at 60% operating rate but always available when needed is a better asset than one running at 95% but breaking down unpredictably. Maximizing operating rate produces overproduction; maximizing operable rate produces reliability.

**[[Seven Wastes (Muda) ⭐]]** is the classification system for everything that is not value-added: overproduction, waiting, transportation, over-processing, inventory, movement, defects. The key equation is: *present capacity = work + waste*. Improvement is not running processes faster — it is eliminating the waste portion so that more of capacity becomes real work.

**[[Value-Added Work]]** refines this further into three levels: work that transforms the product (true value-added), work required under current conditions but not customer-valued (necessary but wasteful), and waste to eliminate immediately. Ohno's method for measuring the ratio is direct observation — standing on the floor and classifying every worker action. The ratio cannot be seen from a report. This is not a concession to impracticality; it is a deliberate design choice that forces managers onto the production floor.

**[[Standard Work]]** locks in each measurement gain. Every improvement is a new standard cycle time, a new work sequence, a new standard inventory level. Without a documented standard, there is no baseline from which improvement can be measured and no mechanism to sustain improvement once found.

TPS's measurement system answers a different question from T/I/OE. Where Goldratt asks "is the system generating money?", Ohno asks "is the system generating value and nothing else?" The physical framing has a practical advantage: waste is visible and classifiable at the shop floor before it ever appears in a financial report. You can see overproduction; you cannot see throughput erosion until the month-end numbers arrive.

---

## HOM: Measure Organizational Output and Leverage

Grove's measurement framework operates at the level of managerial and organizational output rather than production flow. His diagnosis: managers measure their own *activities* (meetings attended, decisions made, hours worked) rather than their *output*, and this confusion corrupts how organizations assess performance and allocate effort.

**[[Managers Output ⭐]]** redefines the unit of measurement. A manager's output is not their individual work — it is the combined output of the organization they supervise and the neighboring organizations they influence. A manager who does brilliant individual work while their team underperforms has produced low output. A manager who enables others to work better — through a single well-run planning process, a well-timed decision, or a course that improves how 200 people think — has produced high output regardless of what they personally made.

**[[Leverage ⭐]]** is the multiplier: output generated per unit of managerial time invested. The managerial output formula is: Output = Σ(Leverage × Activity). High-leverage activities affect many people simultaneously, have durable effects, or apply unique knowledge that unlocks the work of others. Low-leverage activities consume time without propagating. The path to increasing output is not working more hours — it is shifting the mix toward higher-leverage activities.

**[[Indicators ⭐]]** are the practical measurement instrument. Grove's principles: focus each indicator on a specific operational goal, measure output not activity, use physical countable things where possible, and — critically — *pair every indicator*. Every metric pushes behavior in one direction; a paired counter-metric catches the side effect. Track inventory *and* shortage frequency. Track throughput *and* error rate. Track hiring pace *and* quality of hire. An unpaired metric is an invitation to game it.

The indicator types — leading, linearity, trend, stagger chart — reflect a time-sensitivity that T/I/OE and waste classification don't emphasize. A linearity indicator shows you early whether you are on track to hit a period goal, giving time for corrective action. A stagger chart reveals whether forecasts are improving or deteriorating over successive updates. Grove's measurement system is built for *anticipation*, not just diagnosis.

**[[Management by Objectives ⭐]]** makes the measurement system operational for individuals. Each person defines where they want to go (objective) and how they will pace progress (key results, dated). The nesting principle ensures that individual objectives accumulate into organizational objectives. The key warning: MBO is a pacing tool for the person doing the work, not a performance contract. Mechanically scoring someone on whether they completed key results misuses the system — the point is whether they advanced the objective, and sometimes the right path diverges from the one planned.

---

## Comparison

| | The Goal | TPS | HOM |
|---|---|---|---|
| **Primary unit** | Money flow (T/I/OE) | Work content and waste | Organizational output and leverage |
| **Goal of measurement** | Maximize T, minimize I and OE | Eliminate waste, achieve takt-pace flow | Maximize output per unit of managerial time |
| **Key instrument** | T/I/OE applied to every decision | Takt time + seven wastes + value-added ratio | Indicators (paired) + leverage analysis |
| **Time horizon** | Transaction to shipment | Cycle time to takt time | Quarter to year (MBO); day (leverage) |
| **What "busy" means** | Activated but not utilized | Operating rate without operable rate | Activity without output |
| **Where improvement appears** | T increases, I decreases | Waste category eliminated, ratio improved | Output-per-hour increases |
| **Anti-pattern being corrected** | Cost accounting inflating inventory | Operating-rate maximization causing overproduction | Activity metrics mistaken for performance |

---

## The Core Disagreement: What Is the Goal?

The three systems start from different definitions of what the organization is trying to do — and this is not a trivial difference.

**TGL defines the goal financially**: the company exists to make money (for private firms), and every operational measurement must ultimately be expressible in terms of net profit, ROI, and cash flow. T/I/OE is valuable because it bridges from financial goals to daily decisions. Goldratt is explicit: a company that improves waste but doesn't make more money has not improved.

**TPS defines the goal physically**: eliminate waste and create flow; financial results are consequences. Ohno never defines "success" in financial terms within the book. The test of improvement is whether waste has been removed, whether the value-added ratio has risen, whether the system flows at takt. A company that improves its financial metrics by accumulating inventory has not improved — regardless of what the books show.

**HOM defines the goal organizationally**: the manager's job is to increase the output of their organization and the organizations they influence. Grove is not indifferent to financial results, but the *measurement target* is the team's output — not the financial outcome of that output. A manager who maximizes T/I/OE in their division while destroying their team's capability or morale has not done their job.

These are not the same goal. They will sometimes agree and sometimes not. A decision that improves T while increasing waste (e.g., a temporary sprint that burns out the team) would be approved by TGL, rejected by HOM, and assessed by TPS as unsustainable. A decision that reduces waste but doesn't improve T (e.g., improving a non-bottleneck process) would be approved by TPS, neutral or negative by TGL, and evaluated by HOM based on whether it was a high-leverage activity.

---

## The Convergence: Activity Is Not Output

Despite the disagreement about what to measure, all three books converge on the same anti-pattern they are correcting.

Conventional management confuses *activity* with *output*:
- A machine running at high utilization appears productive (TGL: it is activated, not utilized)
- A production process running at high operating rate appears efficient (TPS: it may be producing overproduction)
- A manager attending many meetings appears engaged (HOM: they may be doing low-leverage work)

In each case, the visible activity is real — the machine is really running, the workers are really busy, the manager is really in meetings. The measurement is not falsified. The problem is that nobody asked whether the activity moves the system toward the goal.

All three books offer a sharper definition of productivity to replace the activity proxy:
- **TGL**: does this action increase T, decrease I, or decrease OE?
- **TPS**: does this action add value the customer pays for, or can it be classified as a waste to eliminate?
- **HOM**: does this activity produce high output for the organization relative to the time invested?

Used together, the three tests are more powerful than any one alone. A decision that passes all three — increases throughput, eliminates waste, and represents a high-leverage use of managerial time — is genuinely productive. A decision that fails any one of them deserves scrutiny even if it passes the other two.

---

## How to Use All Three

The measurement systems complement rather than replace each other when applied at different levels:

- **T/I/OE for system-level decisions**: when evaluating whether an investment, a process change, or a batch decision moves the organization toward its financial goal
- **Takt + waste classification for process-level improvement**: when standing on the floor identifying what to eliminate next; the physical visibility of waste provides diagnostic resolution that financial metrics cannot
- **Leverage + indicators for managerial allocation**: when deciding how to spend time, what to monitor, and how to build a measurement system that anticipates problems rather than just recording them

The deepest integration: Goldratt tells you *where to focus* (the constraint), Ohno tells you *what to improve* (the waste at and around the constraint), and Grove tells you *how to organize the work of improvement* (high-leverage activities, standard review cadences, paired indicators). None of the three answers the other two's question.
