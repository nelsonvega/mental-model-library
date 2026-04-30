---
noteId: "72a992103d1111f181025368d1677d72"
tags: []

---

<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# top mental model to do reserach using reserach method, using first principle with aplicabliity and lateral thinking

Here’s a compact “stack” of mental models you can use as a research method that combines first‑principles, applicability, and lateral thinking. I’ll lay it out as a repeatable loop you can drop into any research project.

***

## 1. Define the Game: Problem Framing + Circle of Competence

**Goal:** Make sure you’re solving the *right* research problem and know where your knowledge is strong vs. weak.

1. Write the problem as a precise question:
    - “What is the *smallest* set of facts I must know to make a good decision about X?”
2. Clarify scope using **Circle of Competence**:
    - List: “What do I already understand well here?” vs. “What is fuzzy / unknown?”[^1_1][^1_2]
3. Decide the “job” of your research: decision, strategy, or general understanding.

This stops you from boiling the ocean and sets up where to go deep vs. where to default to experts.

***

## 2. First Principles Decomposition (the Core Engine)

**Mental model:** First Principles Thinking.[^1_3][^1_4][^1_5][^1_1]

**Goal:** Strip the topic down to non‑negotiable truths, then rebuild.

Process:

1. **State assumptions explicitly.**
    - List everything you *think* is true about the topic.
2. **Interrogate each one with “Why?” and “How do we know?”**
    - Ask “Why is this true?” repeatedly until you hit something that would be very hard to dispute without new evidence (physics, math, identities, hard constraints, definitions, regulatory facts, etc.).[^1_4][^1_5][^1_1]
3. **Separate:**
    - First principles (hard constraints, laws, fundamental mechanisms).
    - Heuristics (rules of thumb, averages).
    - Conventions / legacy (done this way because of history or tooling).

Output: a short “first principles spec” of the domain—e.g., for an algorithmic strategy, that might be:

- Price is a function of order flow + information + constraints.
- My edge can only come from information, speed, risk-transfer, or structural constraints others can’t use.

***

## 3. Applicability Filter: Pareto + Constraints

**Mental models:** Pareto Principle (80/20), Inversion, Via Negativa.[^1_6][^1_7][^1_8]

**Goal:** Decide what’s worth researching *deeply*.

1. **80/20 Scan:**
    - Which 20% of variables explain 80% of outcomes? (e.g., in an options strategy: IV surface behavior, liquidity, margin rules).[^1_6]
2. **Inversion:**
    - Ask “If this project completely failed, what were the 3 most likely reasons?”[^1_8]
    - Research those failure modes early (regulation, liquidity, data quality, model risk).
3. **Via Negativa (removal instead of addition):**[^1_7]
    - Ask: “What can I *safely ignore* at this stage?”
    - Drop nice‑to‑knows that don’t change decisions.

Result: a tight list of high‑leverage questions and constraints that guides where you dig for detail.

***

## 4. Lateral Thinking Layer: Analogy + Map–Territory

**Mental models:** Reasoning by analogy (deliberate), Map vs. Territory, Second‑Order Thinking.[^1_2][^1_1][^1_8]

**Goal:** Generate non‑obvious ideas without abandoning rigor.

1. **Analogy harvesting:**
    - “Where else does a system like this exist?”
    - E.g., order books ↔ queuing systems; membership churn ↔ survival analysis; construction workflows ↔ manufacturing pipelines.[^1_2]
2. **Borrow and adapt:**
    - For each analog domain, list 2–3 techniques that might port over.
    - Explicitly write: “Same?” / “Different?” so you don’t over‑fit the analogy.[^1_1][^1_2]
3. **Map vs. Territory check:**
    - Ask: “Is this idea based on a *model* or on *observed data*?”[^1_1][^1_2]
    - Force yourself to distinguish theory vs. reality.
4. **Second‑order thinking:**
    - For each candidate idea, ask “And then what?” two steps out—impact on incentives, edge decay, operational load, etc.[^1_8]

This gives you generative breadth while staying anchored to first principles.

***

## 5. Experimentation \& Feedback Loops

**Mental models:** Feedback loops, Testing, Backcasting / Premortem.[^1_9][^1_10][^1_1]

**Goal:** Close the loop so research doesn’t stay abstract.

1. **Backcast from success:**
    - Define: “If this research were wildly successful in 12 months, what would exist? What metrics would be true?”[^1_9]
    - Work backward to identify the experiments or prototypes that must exist 1–3 months from now.
2. **Design the smallest experiments:**
    - A/B tests, paper trading, small pilot with one association, etc.[^1_10]
3. **Premortem:**
    - Imagine your experiment failed; list reasons, then adjust design to guard against them.[^1_9]
4. **Install feedback metrics:**
    - Decide what you’ll measure to update or kill your hypothesis quickly.[^1_10][^1_1]

This turns your mental‑model stack into a genuine research *method*, not just better thinking on paper.

***

## 6. Compact Checklist You Can Reuse

When you start a new research thread, run this short script:

1. **Frame:**
    - What precise decision or capability is this research supposed to support?
    - What’s inside vs. outside my circle of competence here?[^1_2][^1_1]
2. **Decompose (First Principles):**
    - List assumptions → ask “Why?” until you hit fundamentals → capture 5–10 first principles.[^1_5][^1_4][^1_1]
3. **Filter (Applicability):**
    - Identify the 20% of factors that drive 80% of the outcome.
    - Invert: how could this fail? Research those points first.[^1_7][^1_6][^1_8]
4. **Expand (Lateral Thinking):**
    - Collect 2–3 analog domains; harvest candidate techniques.
    - Use map–territory and second‑order thinking to keep ideas grounded.[^1_8][^1_1][^1_2]
5. **Test (Feedback Loops):**
    - Backcast from success → design smallest meaningful experiment.
    - Run a premortem, instrument feedback signals, iterate.[^1_10][^1_1][^1_9]

If you tell me a specific domain you’re researching right now (e.g., a new trading strategy, association engagement model, or construction workflow), I can walk this stack through that case step‑by‑step so you get a concrete template.
<span style="display:none">[^1_11]</span>

<div align="center">⁂</div>

[^1_1]: https://fs.blog/mental-models/

[^1_2]: https://jamesclear.com/feynman-mental-models

[^1_3]: https://www.mindlabpro.com/blogs/nootropics/5-mental-models-top-decision-makers-swear-by

[^1_4]: https://www.extern.com/post/mental-models-for-smarter-thinking-the-first-principles-approach

[^1_5]: https://www.reddit.com/r/mentalmodels/comments/p0qt2l/mental_model_fundamentals_first_principles/

[^1_6]: https://www.diygenius.com/powerful-mental-models/

[^1_7]: https://www.42courses.com/blog/home/2022/4/15/10-more-mental-models-worth-knowing

[^1_8]: https://www.linkedin.com/posts/vinay-gurram_here-are-5-mental-models-that-changed-how-activity-7417994066690314241-F0Sp

[^1_9]: https://www.hustleescape.com/mental-models/

[^1_10]: https://www.convert.com/blog/a-b-testing/mental-models-in-experimentation/

[^1_11]: https://www.youtube.com/shorts/3rewPpcB1hw

