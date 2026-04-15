---
concept-type: "[[Practice]]"
description: Designing production lines and machines to operate with a variable number of workers — so that headcount tracks volume rather than remaining fixed regardless of demand.
related-concepts:
  - "[[Takt Time ⭐]]"
  - "[[Standard Work]]"
  - "[[Just-in-Time ⭐]]"
  - "[[Autonomation (Jidoka) ⭐]]"
  - "[[Seven Wastes (Muda) ⭐]]"
sources:
  - "[[10-Chapter_6__Surviving_the_Low-Growth_Period|Chapter 6 — Surviving the Low-Growth Period]]"
aliases:
  - Shoninka
  - Flexible staffing
  - Variable manning
---

# Variable Workforce (Shoninka)

*Shoninka* (少人化) means "few-person-ization" — designing a line so it can be operated with fewer people when volume falls, and with more when volume rises. It is TPS's structural answer to the problem of fixed labor cost in a variable-demand environment.

## The Problem It Solves

Conventional lines are staffed for a target volume. When that volume is achieved, the staffing looks correct. When volume falls — a slow-selling model, a demand dip, a post-crisis production cut — the fixed headcount produces a worsening cost per unit. The labor cost that seemed reasonable at full production becomes a liability at 60%.

Ohno identified a specific version of this problem after the 1973 oil crisis: autonomated machines with two fixed operators (one at input, one at output) still required both operators at half production volume. The machines had been designed correctly for JIT purposes but with a rigid staffing assumption built in. The result: halving output did not halve the labor cost.

## The Design Principle

A variable-workforce line is designed from the outset so that:

1. The work content is organized into tasks that can be redistributed as headcount changes
2. Workers are multi-skilled — capable of covering adjacent processes
3. The physical layout (often U-shaped) allows one worker to reach and operate multiple machines in sequence
4. Standard work sequences exist for different staffing levels (5-worker version, 4-worker version, 3-worker version)

When takt time lengthens (volume falls), workers are removed from the line. The remaining workers cover a wider span of tasks, each completing more steps per unit. Output falls proportionally to headcount — unit cost stays roughly constant.

## The Takt Time Connection

Variable workforce is the complement of takt time. Takt time sets the required pace from demand. Headcount is then derived: if takt time is 4 minutes and one worker's full cycle takes 4 minutes, one worker is needed per unit of the line. If takt time widens to 6 minutes (demand falls), fewer workers are needed; each can handle more steps within the longer cycle.

The formula: required headcount = total work content per unit ÷ takt time. As takt time changes, the right number of workers changes. A variable-workforce line is one where this calculation can actually be implemented — not just calculated on paper.

## Multi-Skill Training as the Prerequisite

Variable workforce is impossible without multi-skilled workers. A worker who can only operate one type of machine cannot cover adjacent processes when colleagues are removed from the line. Toyota's investment in cross-training — rotating workers through different processes, training them to handle a span of operations — is what makes shoninka physically achievable.

This is why Ohno regards multi-skill training as infrastructure, not overhead. The line's flexibility to respond to volume changes depends entirely on the workers' flexibility.

## Labor-Saving vs. Worker-Saving

Ohno distinguishes carefully:

- **Labor-saving** (*shoryokuka*): reducing the effort per unit, typically by automating a step. The worker count may stay the same; the work is easier or faster per cycle.
- **Worker-saving** (*shoninka*): reducing the actual headcount while maintaining output proportional to volume.

Labor-saving is useful. Worker-saving is the cost-reduction goal. A machine that automates one step in a ten-step process while leaving the worker in place has achieved labor-saving. A line redesigned so that three workers can produce what four produced at the previous takt time has achieved worker-saving.

The distinction matters because in low-growth periods, the cost reduction that matters is reduction in bodies, not reduction in effort per body.
