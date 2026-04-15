---
concept-type: "[[Framework]]"
description: "The three organizing principles of DevOps and IT Operations: flow of work from Development to Operations to the customer (First Way), feedback loops that amplify problems back upstream (Second Way), and a culture of experimentation and continuous learning (Third Way)."
related-concepts:
  - "[[The Four Types of Work]]"
  - "[[Throwing the Pig Over the Wall]]"
  - "[[Uncontrolled Change ⭐]]"
  - "[[Change Advisory Board (CAB)]]"
sources:
  - "[[12-Chapter_7_•_Friday,_September_5|Chapter 7 — Friday, September 5]]"
aliases:
  - First Way
  - Second Way
  - Third Way
---

# The Three Ways

Introduced by Erik Reid in Chapter 7 during the manufacturing plant visit. Erik presents them as the destination — the organizing principles Bill needs to work toward — without yet fully explaining how to get there. The Three Ways structure the arc of the entire novel.

## First Way: Flow

> *"The First Way helps us understand how to create fast flow of work as it moves from Development into IT Operations, because that's what's between the business and the customer."*

The First Way is about the left-to-right flow of work through the system: from business need → Development → IT Operations → customer. Anything that slows this flow — handoff gaps, unplanned work consuming planned capacity, bottlenecks, rework — degrades the system's ability to deliver value.

The manufacturing analogy from the plant visit makes this concrete: work in process accumulates when jobs are released faster than the bottleneck can consume them. The same dynamic applies to IT — features piling up waiting for deployment, incidents piling up waiting for Brent, change cards piling up waiting for CAB review. Fast flow requires controlling work release, protecting the constraint, and removing the friction between Dev and Ops.

The First Way also implies that local optimizations that don't improve overall flow are illusory. Goldratt's formulation: improvements made anywhere other than the bottleneck don't improve system throughput. A Development team that ships faster than Operations can absorb is not going faster — it is building WIP.

## Second Way: Feedback

> *"The Second Way shows us how to shorten and amplify feedback loops, so we can fix quality at the source and avoid rework."*

The Second Way is about the right-to-left flow of information: from the customer and production back upstream to Development and the business. Fast, amplified feedback loops allow problems to be caught close to their source, before they propagate downstream and become expensive.

Without feedback, problems discovered in production get fixed in production — after customers have been affected, after the original developer has moved on, after the context has been lost. With fast feedback, a deployment problem surfaces within minutes rather than days, the team still has context, and the fix is applied at the source rather than downstream.

This is structurally related to TPS's jidoka principle: stop at the point of abnormality, surface the problem, fix the root cause. The Second Way applies the same logic to software systems: detect problems as early as possible, make them visible immediately, prevent them from propagating.

## Third Way: Continuous Learning

> *"The Third Way shows us how to create a culture that simultaneously fosters experimentation, learning from failure, and understanding that repetition and practice are the prerequisites to mastery."*

The Third Way is about the organizational conditions that sustain the first two. Flow and feedback are mechanisms; the Third Way is the culture that makes continuous improvement possible rather than a one-time event.

Key elements: experimentation is encouraged, not penalized. Failure is diagnostic data, not a disciplinary event. Practice and repetition build the muscle memory that makes good practices automatic. The organization gets better over time because it systematically learns from what happens rather than repeating the same mistakes under a different crisis name.

## Relation to the Book's Structure

The Three Ways map onto the novel's arc:
- **Chapters 1–10:** The First Way problem — work is not flowing; planned work is swamped by unplanned work; the Dev/Ops handoff is broken
- **Chapters 11–25:** Moving toward the Second Way — building feedback mechanisms, making problems visible fast
- **Chapters 26–38:** The Third Way conditions — cultural change, trust, learning cycles that sustain improvement
