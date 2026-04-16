# Boy Scout Hike — Interactive Demo Design

## Purpose

A single-page HTML/JS simulation that lets the user **see** why dependent events + statistical fluctuations destroy throughput in a balanced system, and **feel** the difference when the constraint is managed.

The demo covers all three chapters (13, 14, 15) of the Boy Scout Hike arc.

## Core Mechanic

A line of **10 scouts** walks left-to-right across a trail. Each tick:

1. Each scout rolls a random pace (uniform integer 1–6, mean 3.5).
2. **Dependency rule:** a scout cannot advance past the scout ahead of him. If his roll would place him ahead, he stops at the back of the next scout. (Speed is absorbed locally; slowness propagates backward.)
3. The **last scout's cumulative distance** = system throughput.
4. The **sum of gaps** between consecutive scouts = inventory (WIP).

Herbie's base pace range is **1–4** (mean 2.5) — visibly slower but not dramatically so. All others roll 1–6.

## Three Scenarios (tabs or buttons)

| # | Label | Configuration | What it teaches |
|---|-------|--------------|-----------------|
| 1 | **Fastest First** | Ron (fastest) at front, Herbie at back. Natural/intuitive order. | Column explodes. Max inventory, throughput = Herbie's pace. Ch. 13 insight. |
| 2 | **Herbie Leads** | Herbie moved to front. No one passes. | Gaps stop forming. Spare capacity behind absorbs fluctuations. Subordinate step. |
| 3 | **Pack Redistributed** | Herbie at front, his range changes from 1–4 to 1–6 (pack weight shared). | Throughput jumps. Elevate step. Full solution. |

The user can switch scenarios at any time. Each scenario runs independently.

## Visual Layout

```
+---------------------------------------------------------------+
|  Boy Scout Hike Simulation                                     |
|                                                                |
|  [Fastest First]  [Herbie Leads]  [Pack Redistributed]         |
|                                                                |
|  Trail view (horizontal):                                      |
|  ............................................................  |
|  ^Ron   ^Scout2  ^Scout3 ... gap ...  ^Herbie   ^Rogo(you)    |
|  (colored dots on a horizontal track, spaced by actual pos)    |
|                                                                |
|  Metrics panel:                                                |
|  +------------------+-------------------+-------------------+  |
|  | Throughput       | Inventory (WIP)   | Ticks elapsed     |  |
|  | 47 / 70 expected | 23 trail-units    | 20                |  |
|  +------------------+-------------------+-------------------+  |
|                                                                |
|  Live chart (small, below):                                    |
|  - Line chart: throughput over time (actual vs. expected 3.5t) |
|  - Area chart: total inventory over time                       |
|                                                                |
|  Controls: [Play/Pause] [Step] [Reset] Speed: [slow|med|fast] |
|                                                                |
|  Explanation text (context-sensitive to current scenario)       |
+---------------------------------------------------------------+
```

### Trail View Details

- Horizontal track, ~800px wide, representing 0–100 trail units.
- Each scout is a **colored circle** (16px diameter) with a 1-letter label.
- **Herbie** is always visually distinct: orange fill + bold "H" label.
- **Rogo** (last in line) is a darker/outlined circle — his position = throughput.
- Gaps between scouts are visible as whitespace. When inventory is high, the column visibly stretches.
- A faint "expected position" marker (dashed vertical line) shows where the last scout *should* be if the system averaged 3.5/tick.

### Chart

Use plain Canvas 2D — no charting library. Two overlaid line charts:
- **Blue line:** cumulative throughput (last scout's distance).
- **Gray dashed line:** expected throughput (3.5 * tick).
- **Red area:** total inventory (sum of gaps) — plotted on a secondary y-axis or as a small separate chart below.

Keep it minimal. No axes labels needed beyond a legend.

## Interaction

- **Scenario tabs** at top. Clicking one resets and starts that scenario.
- **Play / Pause** toggle. Auto-advances one tick every 400ms (adjustable).
- **Step** button: advance exactly one tick (useful for studying the mechanic).
- **Speed slider** or three preset buttons (1x / 2x / 4x).
- **Reset** returns to tick 0 for the current scenario.
- Hovering a scout shows a tooltip: name, current pace roll, cumulative distance.

## Explanation Panel

A short paragraph below the simulation that changes per scenario:

**Scenario 1 — Fastest First:**
> "Ron sets the pace at the front. Each scout can walk as fast as they roll — unless blocked by the scout ahead. Watch Herbie: every time he rolls low, everyone behind him waits. But when he rolls high, he can only close the gap to the scout ahead — the speed is absorbed. Slowness propagates backward; speed does not. The column stretches inevitably."

**Scenario 2 — Herbie Leads:**
> "Herbie now sets the pace for the entire column. No one can pass him. The fast scouts behind have spare capacity — when anyone pauses, the scouts behind close the gap easily. The column stays together. Throughput hasn't increased (it's still Herbie's pace), but inventory has collapsed."

**Scenario 3 — Pack Redistributed:**
> "Herbie's pack has been shared across the group. His effective pace range is now the same as everyone else's. The column moves faster AND stays together. Throughput is up. Inventory is down. This is 'elevate the constraint' — the only action that actually increases system output."

## Technical Approach

### Single HTML file, no dependencies

- All CSS inline in `<style>`.
- All JS inline in `<script>`.
- Canvas element for the trail view and charts.
- No build step, no npm, no framework.

### Data Model

```js
// Scout object
{
  name: string,        // "Ron", "Herbie", "Rogo", etc.
  isHerbie: boolean,
  minPace: number,     // 1 for normal, 1 for Herbie
  maxPace: number,     // 6 for normal, 4 for Herbie (scenario 1-2), 6 (scenario 3)
  position: number,    // cumulative distance
  lastRoll: number,    // most recent dice roll
  color: string        // display color
}

// State
{
  tick: number,
  scouts: Scout[],          // ordered front-to-back
  throughputHistory: number[], // last scout's position each tick
  inventoryHistory: number[], // sum of gaps each tick
  scenario: 1 | 2 | 3,
  running: boolean,
  speed: number              // ms per tick
}
```

### Tick Logic (pseudocode)

```
for each scout from FRONT to BACK:
  roll = random(scout.minPace, scout.maxPace)
  scout.lastRoll = roll
  newPos = scout.position + roll
  if (prevScout exists):
    newPos = min(newPos, prevScout.position)  // can't pass the one ahead
  scout.position = newPos

throughput = scouts[last].position
inventory = sum of (scouts[i].position - scouts[i+1].position) for i in 0..n-2
```

### Scout Names & Order

**Scenario 1 (Fastest First):**
`[Ron, Andy, Ben, Chuck, Dave, Evan, Frank, Greg, Herbie, Rogo]`

Ron and the fast boys up front. Herbie near the end. Rogo last (observer).

**Scenario 2 & 3 (Herbie Leads):**
`[Herbie, Ron, Andy, Ben, Chuck, Dave, Evan, Frank, Greg, Rogo]`

Herbie at front. Everyone else behind. Rogo still last.

### Rendering

- **Trail:** Draw a horizontal line. Plot each scout as a circle at `x = (scout.position / maxPosition) * canvasWidth`. Scale dynamically so the frontmost scout is always near the right edge.
- **Charts:** Simple polyline on a second canvas. Throughput as blue line, expected as gray dashed, inventory as red filled area.
- **Metrics:** Update DOM text nodes each tick.

### Responsive

- Canvas resizes to container width.
- Minimum viable width: 600px.
- On narrow screens, stack chart below trail.

## Color Palette

| Element | Color |
|---------|-------|
| Normal scout | `#4a90d9` (blue) |
| Herbie | `#e67e22` (orange) |
| Rogo | `#2c3e50` (dark, outlined) |
| Trail line | `#ddd` |
| Expected line | `#999` dashed |
| Throughput line | `#3498db` |
| Inventory area | `rgba(231, 76, 60, 0.3)` |
| Background | `#fafafa` |

## Edge Cases

- If a scout's roll would make them pass the scout ahead, they stop at the same position (gap = 0). This is correct — it represents blocked capacity.
- Rogo has the same dice range as normal scouts. He is just the measurement point.
- At tick 0, all scouts start at position 0.

## What Success Looks Like

A user who has never read the book should be able to:

1. Run Scenario 1 and **see** the column stretch — feel confused about why the system falls behind when everyone averages 3.5.
2. Switch to Scenario 2 and **see** the column stay together — understand that putting the constraint first eliminates inventory accumulation.
3. Switch to Scenario 3 and **see** throughput jump — understand that only elevating the constraint speeds up the system.
4. Compare the throughput and inventory charts across scenarios and have the "aha" moment that the book's readers get from chapters 13–15.
