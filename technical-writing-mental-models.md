---
noteId: "945da7203d1111f181025368d1677d72"
tags: []

---

<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# mental model, pattern, best practice, creative of the process to write a technical paper

Here’s a concrete way to think about (and repeatedly use) a **mental model / pattern** for writing a technical paper, with embedded best practices and room for creativity.

***

## 1. Core mental model: “Problem → Story → Contract → Proof”

Hold four questions in your head from start to finish:

1. **What problem do I solve?** (problem)
2. **What is the story of how we solve it?** (story)
3. **What do I promise the reader I’ll deliver?** (contract)
4. **How do I prove every promise, cleanly?** (proof)

A useful framing from robotics/CS folks is to see the paper as a **tree of problems and solutions**.[^1]

- Root: the big problem the paper tackles.
- Internal nodes: sub‑problems, each paired with a sub‑solution.
- Leaves: full technical detail, derivations, code-level specifics.[^1]

Your job is to **walk the reader down this tree**, always introducing the *problem first, then the solution*—never dumping math or architecture without a clear motivating problem.[^1]

***

## 2. Process pattern: from chaos → outline → draft → refine

### Step 1 – Capture: “Crappy first brain dump”

Goal: get everything out of your head with zero concern for quality.

- Brain‑dump **stream‑of‑consciousness notes** in bullets or fragments, not sentences.[^2]
- Don’t structure yet; just list ideas, results, sketches, known references.
- This lowers perfectionism and makes you more willing to delete / move things later.[^3][^2]

Mental model: **separate creation from refinement**. Creation is wild, refinement is ruthless.[^3]

***

### Step 2 – Cluster: form the “problem/solution tree”

Take your brain dump and **group items into problem/solution clusters**:

- For each cluster, name:
    - The **problem** (what’s confusing, inefficient, unknown?).
    - The **solution** (your method, model, algorithm, experiment, design).
- Arrange clusters from **root problem → sub‑problems → detailed techniques** (the tree).[^1]

This becomes your **section skeleton**:

- Introduction = root problem + big picture solution.
- Technical sections = sub‑problems + their solutions.
- Experiments / evaluation = proof that solutions work for stated problems.

***

### Step 3 – Define the contract (Abstract \& Intro)

Think of the **Abstract + Introduction as a contract with the reader**:

You promise to clearly specify:

1. **Context \& importance** – where in the world this problem lives.
2. **Gap** – what’s missing or broken in current approaches.
3. **Your contribution** – what you propose.
4. **Evidence** – how you back up the contribution (experiments, theorems, case studies).

Best‑practice pattern: the goal is to convince the reader your scheme is **interesting, different, and better enough to care about**, and raises legitimate questions worth further research.[^4]

When drafting this contract:

- Avoid narrative like “First we will…” and instead be precise about what the paper *does* and *shows*.[^2]
- Every strong claim in the intro must later be backed by **citation, quantitative data, or careful argument**.[^4]

***

### Step 4 – Design the reading paths (structure as UX)

Use a **UX mindset**: most readers will **skim**, not read linearly.

- Many readers will only read: title → abstract → intro → figures/tables → conclusion.[^1]
- Only a few will drill all the way down into proofs or algorithmic details (the leaves).[^1]

Design for:

- **Skimmers** – they should still understand the main problem, your idea, and why it matters.
- **Implementers** – they should find enough detail in later sections/appendix to reproduce.

Techniques:

- Use a **hierarchical structure** with clear headings, subheadings, bullets.[^5][^6]
- Each technical section starts with a **plain-language description of the problem it solves**.[^1]
- Keep navigation easy with consistent formatting, section titles that reflect the problem being solved, and visuals (diagrams, tables).[^7][^6]

***

### Step 5 – Write section by section using the “mini‑story” pattern

For each major section (methods, system design, experiments), repeat a **mini story**:

1. **Setting** – the local context: what sub‑problem are we in?[^7][^1]
2. **Conflict** – what makes this sub‑problem hard (limitations of existing things).
3. **Resolution** – your solution (equations, algorithms, architecture).
4. **Verification** – how you check that this part actually works (tests, metrics).

You can borrow **story structure** for technical writing without becoming fluffy: use it to organize context, not to embellish prose.[^7]

***

### Step 6 – Style: clarity, precision, and voice

Key best practices:

- **Know your audience** – define their level (e.g., roboticists, ML engineers, clinical researchers) and write to their background.[^6][^8][^5]
- **Be clear and precise** – avoid vague terms like “soon”, “a lot”, “often”; use quantitative descriptions instead.[^5][^6]
- Prefer **active voice and present tense** where possible for directness:
    - “We propose a method that…” instead of “A method is proposed that…”.[^5]
- Use first person “we” to describe what you did, not “we the paper / we the reader”.[^2]
- Keep jargon minimal and always define it on first use.[^6][^5]

Mental models to enforce this:

- **Occam’s Razor for writing** – simplest explanation that is correct usually wins; cut unnecessary complexity.[^3]
- **First principles** – every dense paragraph should answer: what is the minimum needed to understand this, and can I remove the rest?[^3]

***

### Step 7 – Make it readable: visuals, structure, and creativity

Technical ≠ dry. You can be **creative in design rather than in flowery language**:

- Use **figures, diagrams, tables, and examples** liberally to offload cognitive load.[^6][^7]
- Use layout and structure as creative tools: logical section ordering, helpful summaries, callout boxes, etc.[^7]
- Think of your visuals as part of the story: each figure answers a specific question (“What does the architecture look like?”, “How does performance scale?”).

Creativity principle: treat the paper like a **well‑designed product**—you’re designing a user experience for a busy, skeptical expert.[^6][^7]

***

### Step 8 – Revision loop: eliminate gaps and friction

Have a specific revision checklist:

1. **Contract check**: Does the body of the paper actually prove every claim in the abstract/introduction?[^4]
2. **Tree check**: For each technical detail, is the motivating problem clearly stated? If not, add one level of context.[^1]
3. **Audience check**: Would someone at your target level stop and say “wait, what?” anywhere? Simplify or explain.[^8][^5][^6]
4. **Style check**: passive voice, vague words, unnecessary jargon—tighten and clarify.[^8][^5]
5. **Accuracy check**: every factual statement can be backed by either data, citation, or explicit reasoning.[^8][^4]

Best practice: revise not just for grammar but for **technical accuracy, consistency, and accessibility**.[^8]

***

## 3. Compact “algorithm” you can reuse

When you sit to write your next technical paper, you can literally follow this checklist:

1. **Brain dump** bullets of everything you know (no sentences).[^2][^3]
2. Group bullets into **problem/solution clusters**; arrange as a tree from big problem to details.[^1]
3. Draft Abstract + Introduction as a **contract**: context, gap, contribution, evidence.[^4]
4. For each section, apply the **mini‑story**: setting → conflict → resolution → verification.[^7][^1]
5. Add visuals and structure so skimmers can still get the story.[^6][^7][^1]
6. Run the **revision loop** with contract, tree, audience, style, and accuracy checks.[^5][^4][^8][^6]

If you tell me what kind of technical paper you want to write next (e.g., “multi‑agent trading system architecture” or “evaluation of an AI-native SaaS migration framework”), I can help you instantiate this into a concrete section-by-section outline with example phrases.
<span style="display:none">[^10][^11][^12][^13][^14][^15][^9]</span>

<div align="center">⁂</div>

[^1]: https://h2r.cs.brown.edu/writing-a-technical-paper/

[^2]: https://homes.cs.washington.edu/~mernst/advice/write-technical-paper.html

[^3]: https://www.publicationcoach.com/mental-models/

[^4]: https://www.cs.utexas.edu/~dahlin/professional/paper-writing.pdf

[^5]: https://www.scilife.io/blog/best-practices-tips-technical-writing

[^6]: https://radcomservices.com/technical-writing-best-practices-the-key-to-clear-and-effective-communication/

[^7]: https://resources.ascented.com/ascent-blog/creativity-in-technical-writing-2

[^8]: https://proedit.com/technical-writing-best-practices/

[^9]: https://dl.acm.org/doi/10.1145/3690712.3690722

[^10]: https://www.reddit.com/r/cscareers/comments/1rmxrht/the_exact_mental_model_senior_developers_use_when/

[^11]: https://www.nngroup.com/articles/mental-models/

[^12]: https://mavmatrix.uta.edu/cgi/viewcontent.cgi?params=%2Fcontext%2Futalibraries_publications%2Farticle%2F1007%2Ftype%2Fnative%2F\&path_info=

[^13]: https://arxiv.org/pdf/2604.05166.pdf

[^14]: https://www.sciencedirect.com/science/article/pii/S0950584923001544

[^15]: https://eudl.eu/pdf/10.4108/eai.17-12-2022.2338687

