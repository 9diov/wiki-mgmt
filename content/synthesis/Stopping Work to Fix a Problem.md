---
books-compared:
  - "[[The Goal (TGL)]]"
  - "[[Toyota Production System (TPS)]]"
  - "[[High Output Management (HOM)]]"
concepts:
  - "[[Autonomation (Jidoka) ⭐]]"
  - "[[Five Whys ⭐]]"
  - "[[Exploit the Bottleneck ⭐]]"
  - "[[True Cost of Bottleneck Time]]"
  - "[[Quality Assurance]]"
  - "[[Lowest Value Stage]]"
examples:
  - "[[Toyoda Sakichis Loom]]"
  - "[[NCX-10 Machine Purchase ⭐]]"
  - "[[Intel Ion Implanter Failure ⭐]]"
---

# Stopping Work to Fix a Problem — Across Three Books

The default instinct in any production system is to keep things moving. A stopped line produces nothing; a running line produces output. Stopping feels like loss; running feels like progress. All three books argue that this instinct, left uncorrected, is one of the most destructive forces in an organization — and they arrive at the same conclusion from different angles: running through a problem does not save time. It multiplies cost, buries the evidence, and makes the underlying cause harder to fix.

The books differ in *where* they say to stop, *what* triggers the stop, and *what to do once stopped*. Those differences are worth examining carefully.

---

## The Goal: Stop Before the Bottleneck

In Rogo's plant before the transformation, the working assumption was conventional: keep every resource running, catch quality problems downstream, do rework at the end. A defective part that passed through the NCX-10 and got caught at final inspection was a quality cost. Unfortunate, but manageable.

Jonah's plant visit produces a different accounting. The [[True Cost of Bottleneck Time|true cost of one idle bottleneck hour]] is not the machine's allocated share of overhead — it is the total plant operating expense divided by available bottleneck hours. In Rogo's plant: $1,600,000 ÷ 585 hours = **$2,735 per hour**. A defective part that reaches the NCX-10 and is processed before detection does not cost the price of a scrapped part. It costs the scrapped part *plus* whatever bottleneck time was consumed processing it — time that is permanently, unrecoverably gone.

This reframes the quality decision completely. The question is not "what is the cost of this defect?" but "where in the production sequence does this defect cost the most?" The answer is always: at the constraint. A defect that doesn't reach the bottleneck costs only the material and upstream labor that produced it. A defect that reaches the bottleneck costs all of that, plus irreplaceable bottleneck capacity, plus whatever downstream work gets applied to a part that will ultimately be scrapped.

Jonah's directive from [[Exploit the Bottleneck ⭐]]: move quality inspection to *before* the bottleneck. The bottleneck should only ever process good parts. Every scrap and rework decision involving a part that hasn't yet reached the bottleneck is a cheap decision. The same decision made after the bottleneck has touched the part is expensive in the one currency the system cannot recover — throughput capacity.

**The TGL insight is about location, not just timing.** Stopping the line anywhere is not the lesson. The lesson is that the value of catching a defect scales with how close it is to the constraint. Catching it upstream costs nothing extra. Letting it through the constraint costs everything.

The conventional plant didn't stop before the bottleneck — not because anyone decided that was the right policy, but because no one had calculated what running through defects actually costs at the constraint. The accounting system made bottleneck time look cheap. At $32.50/hour it was easy to let it absorb a defective part. At $2,735/hour the calculus is completely different.

---

## TPS: Stop Everywhere — Problems That Run Through Are Problems That Compound

TPS's approach to stopping is more radical and more general. The principle is not "stop before the bottleneck" — it is **stop at the point of abnormality, anywhere in the line, always**.

The origin is [[Toyoda Sakichis Loom|Toyoda Sakichi's loom]]. A conventional power loom runs continuously. If a thread breaks, the loom keeps weaving defective fabric until an operator notices — which may be meters of ruined cloth later. Sakichi built a loom that stopped the instant any thread broke. One defective piece, then a stop. The device that detected the abnormality and halted the machine was the invention; the loom itself was already well understood.

Ohno transplanted this principle from textiles to automobiles as **[[Autonomation (Jidoka) ⭐]]** — automation with a human touch. The extension to workers is the **andon cord**: any worker who detects an abnormality has both the authority and the responsibility to stop the line. This is not a safety valve — it is the primary mechanism by which TPS surfaces problems.

The cultural challenge is severe. Every management instinct runs against it. A stopped line produces nothing; managers are measured on production. The instinct is to let the line run and fix it downstream, or on the next shift, or at end-of-day rework. Ohno's counter-argument: *"An old Japanese saying mentions hiding an offensively smelly object by covering it up. If materials or machines are repaired without the managing supervisor's being made aware of it, improvement will never be achieved."* A line that runs through defects produces a mountain of defective parts and a management team that never learns what is causing them. A line that stops on the first defect produces one defective part and an urgent, visible problem that must be understood.

**Stopping is progress. Running through is stagnation.**

The connection to [[Five Whys ⭐]] is direct. Stopping the line is necessary but not sufficient — it surfaces the problem but does not solve it. The Five Whys discipline is what happens after the stop: ask why five times, reach the root cause, apply a countermeasure that prevents recurrence. A plant that stops on defects but only replaces fuses is doing half the work. The stop creates the opportunity; root-cause analysis converts the opportunity into improvement.

TPS's approach is also more aggressive than TGL's about where defects are accepted. TGL focuses quality inspection effort around the constraint because that is where defects cost the most. TPS objects to defects anywhere in the line — not because every location has equal cost, but because any defect allowed to pass is a problem that was hidden rather than solved. The inventory buffers that make downstream defect detection feel safe are themselves waste; removing them (through JIT) makes every defect immediately visible and immediately costly, which creates the urgency to fix root causes rather than manage symptoms.

---

## HOM: Catch Defects at the Lowest-Value Stage

Grove's treatment is the most economically precise of the three. The **[[Lowest Value Stage]]** principle states: catch defects as early in the process as possible, before further value has been added to the defective material. A rotten egg rejected at delivery costs almost nothing. The same problem discovered after boiling, plating, and serving wastes every step in between — and damages the customer relationship.

This is structurally the same argument as TGL's inspect-before-the-bottleneck principle, generalized: the cost of catching a defect increases with every additional step the defective material passes through. Stop as early as possible.

**[[Quality Assurance]]** adds the inspection strategy dimension. Two instruments: gate inspection (hold all material until the test completes — 100% defect prevention, but flow stops) and monitoring (sample continuously, stop the line if successive samples fail — flow continues, but some defective material may pass before the signal triggers). The trade-off is between defect containment and throughput. For the same inspection budget, monitoring can be done far more frequently than gate-checking, and higher-frequency monitoring often contributes more to overall quality than lower-frequency gates.

The reliability exception is Grove's sharpest quality principle: *never* accept substandard material if the defect could cause a reliability failure — a complete failure the customer cannot recover from. A pacemaker component is the extreme case. When the cost of post-delivery failure is incalculable, no economic trade-off is acceptable. The line must stop; the defect cannot pass. This is jidoka applied to the highest-stakes context: the stop is non-negotiable regardless of its production cost.

The [[Intel Ion Implanter Failure ⭐]] is HOM's illustration of running through a problem. An operator continued processing wafers through a machine that had drifted out of tune — not because she was negligent, but because she hadn't been trained to recognize the abnormality. The machine ran through the defect for nearly a full day. Over $1M of material was scrapped; delivery schedules slipped for weeks. The failure was not at the defect detection point — the defect was invisible to the untrained operator. The failure was upstream, in the training system that should have equipped her to stop the machine.

---

## Comparison

| | The Goal | TPS | HOM |
|---|---|---|---|
| **Where to stop** | Before the bottleneck — that is where defects cost most | At the point of abnormality, anywhere in the line | At the lowest-value stage — as early as possible |
| **What triggers the stop** | Quality inspection gate placed before the constraint | Machine self-detection (autonomation) or worker judgment (andon) | Gate inspection or monitoring thresholds |
| **Why running through costs more** | Defects consume irreplaceable bottleneck time ($2,735/hour) | Problems buried in running production compound; causes never get fixed | Each downstream step adds value to defective material that will eventually be scrapped |
| **What happens after the stop** | Fix defect; resume; protect bottleneck from recurrence | Five Whys — find root cause; update standard work | Variable inspection frequency; root cause if threshold triggered |
| **The cultural barrier** | Standard accounting makes bottleneck time look cheap | Managers penalize stoppages; running feels like progress | Economic trade-offs dominate; reliability exception is absolute |
| **Illustration** | NCX-10 — defects consuming $2,735/hour of constraint capacity | Toyoda's loom — one defective piece then a stop vs. meters of ruined fabric | Ion implanter — untrained operator runs through defect for a full day |

---

## The Core Disagreement: Local or Universal?

TGL and TPS differ in scope. Goldratt's recommendation — inspect before the bottleneck — is explicitly constraint-relative: defects that don't reach the bottleneck cost only their direct material and labor. There is no particular urgency to catch them earlier than the bottleneck gate; the savings from earlier detection don't justify restructuring the entire quality system. The constraint is the organizing principle.

TPS rejects this framing. Ohno's position is that any defect allowed to pass anywhere is a problem tolerated, not solved. The inventory buffers that make downstream detection feel safe — the safety stock that absorbs a defective batch before it causes a downstream stoppage — are themselves waste. The TPS answer is to remove the buffers, expose every defect immediately, and force root-cause resolution rather than symptom management. The bottleneck is not a special location; every step is a location where a problem should stop rather than propagate.

The practical difference: a plant implementing TGL's quality advice will have one high-value inspection gate before its bottleneck. A plant implementing TPS's quality discipline will have workers stopping the line at every station when something looks wrong, and managers treating those stops as diagnostic data rather than production failures. Both produce fewer defects at the constraint. TPS also produces a continuous improvement mechanism at every step; TGL does not require this.

**HOM's lowest-value-stage principle bridges the two.** Grove's framework says: inspect where the cost difference between early and late detection is largest. For a bottleneck-constrained plant, that is before the bottleneck — consistent with TGL. For a JIT system where every inventory buffer has been removed, it is everywhere — consistent with TPS. The principle is the same; the right application point depends on the system's current design.

---

## The Shared Principle: Visibility Is the Goal

Beneath the strategic differences, all three books make the same claim about what stopping for a problem accomplishes.

**A running line that buries a problem is not making progress.** The output it produces obscures the defect, delays the diagnosis, adds cost to material that will eventually be scrapped, and removes the urgency that forces root-cause resolution. The line looks productive; the problem compounds.

**A stopped line that reveals a problem is making progress.** Nothing is being produced, but the problem is visible, urgent, and available for diagnosis. If the stop is followed by genuine root-cause analysis, the problem will not recur. The pause in production now prevents repeated production of defects later.

This is the inversion both Goldratt and Ohno are forcing. The conventional frame is: a running line is a producing line; a stopped line is a failing line. The corrected frame is: a running line is only a producing line if it is producing good output; a line running through defects is producing cost, not throughput. Stopping to fix the problem is the production decision. Running through it is the failure.

Grove reaches the same conclusion from a different direction through the reliability exception: when a defect in delivered output cannot be corrected after the fact, the economic trade-off that normally governs inspection decisions does not apply. You stop. The framing is different — cost-of-failure vs. cost-of-inspection — but the conclusion is identical: some problems cannot be allowed to pass, and the decision to stop is the correct production decision, not a deviation from it.
