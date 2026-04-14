<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# regenrate including references books, libraries

Here are the key mental models again, plus concrete books and libraries to go deeper into “habit-forming” (ethically) product design.[^1][^2][^3]

## Core mental models

1) **Jobs To Be Done (JTBD)**
Think in terms of the life “job” the user is hiring your product to do: situation → motivation → desired outcome → anxieties.[^2][^1]

- Use interviews and story-based surveys to capture real jobs (“never forget a task again,” “feel on top of my money”).[^1]
- Design first-session and daily flows so the job is completed with radically less friction than alternatives.[^2][^1]

2) **Causal / Feedback Loops**
Map your product as loops: trigger → action → variable reward → investment → stronger trigger.[^4][^1]

- Positive loops: more content → more value → more sharing → more content.[^1]
- Add visible compounding (streaks, levels, collections) that grows with each use.[^5][^1]

3) **Value Stream / Time‑to‑Aha**
Model: intent → sign‑up → first success (“aha”) → repeat usage → habit.[^2][^1]

- Instrument where people drop and eliminate steps between intent and first **reward**.[^1]
- Aim for a “one‑session aha” where new users feel clear value within minutes.[^1]

4) **Pareto \& Power Users**
Assume 20% of flows drive 80% of retention, and a small % of users drive most content/revenue.[^6][^1]

- Identify behaviors that correlate with 7‑, 30‑, 90‑day retention and over‑optimize those flows.[^1]
- Build pro features, automations, and APIs for power users who live in the product.[^6]

5) **Kano + Micro‑Delight**
Separate basics (must-work), performance (more = better), and delighters (unexpected joy).[^2]

- Basics: speed, reliability, clear feedback, undo everywhere.[^3][^2]
- Delighters: tiny, repeatable moments (smart defaults, context-aware suggestions, subtle animations) that show up daily.[^3][^2]

6) **PMF as “Pull Strength”**
Treat product–market fit as “how painful would it be to lose this tomorrow?”[^1]

- Measure with usage depth and qualitative “how disappointed would you be if…?” surveys.[^1]
- Tune your loops until a narrow core says they’d be “very disappointed.”[^1]

7) **Pioneers, Settlers, Town Planners**
Use different mental modes as the product matures.[^1]

- Pioneers: explore loops, hooks, and novel value.[^1]
- Settlers: clean up UX, pricing, metrics; make loops reliable.[^1]
- Town planners: scale infra, governance, reliability, ethics.[^5][^1]


### Quick reference table

| Model | What it drives |
| :-- | :-- |
| Jobs To Be Done | Clear core value and “can’t-live-without” use cases. [^1][^2] |
| Causal/feedback loops | Habit, daily/weekly active use, viral spread. [^1][^4] |
| Value stream / Time‑to‑Aha | Fast first win and better activation. [^1][^2] |
| Pareto \& power users | Deep engagement and revenue concentration. [^6][^1] |
| Kano + micro‑delight | Emotional attachment and word-of-mouth. [^2][^3] |
| PMF as pull strength | Strategic focus on retention over vanity metrics. [^1] |
| Pioneers/Settlers/Town | Right style of building at each stage. [^1] |

## Books to internalize these ideas

Core “hooking” and behavior-change texts (read with an ethical lens):

- **Hooked: How to Build Habit-Forming Products – Nir Eyal**
Lays out the Trigger → Action → Variable Reward → Investment loop, with many SaaS/app examples.[^4][^3]
- **Designing for Behavior Change – Stephen Wendel**
A step-by-step method for defining target behaviors, turning them into product flows, and measuring change.[^7][^8]
- **Engaged: Designing for Behavior Change – Amy Bucher**
Very practical playbook for engagement and motivation in digital products.[^8]

Foundational behavior and UX psychology:

- **Influence: The Psychology of Persuasion – Robert Cialdini** (principles like reciprocity, scarcity, social proof).[^9][^3]
- **Thinking, Fast and Slow – Daniel Kahneman** (System 1 vs 2, biases your UX will hit constantly).[^7][^9]
- **The Design of Everyday Things – Don Norman** (friction, affordances, feedback in interaction design).[^9][^7][^3]

Curated lists you can mine:

- “9 Behavioral Psychology Books for Persuasive UX Design” (UserTesting).[^3]
- “The Ultimate List of Books for Behavior Change and Design” (Aim for Behavior).[^8]


## Libraries / frameworks to implement addictive loops

Not “addiction” libraries per se, but tools that make it trivial to instrument and iterate on loops:

- **Product analytics**
    - Amplitude, Mixpanel, PostHog: cohort analysis, funnel drop-off, retention curves, and behavioral segments.[^1]
- **Experimentation \& growth**
    - Statsig, Optimizely, or LaunchDarkly for feature flags and A/B tests around hooks, notifications, rewards, and onboarding.[^1]
- **Gamification / engagement layers**
    - For web: use React or Vue component kits plus your own “points / levels / streaks” domain logic; follow gamification patterns like points, badges, leaderboards, quests, and rewards described in research on addictive digital patterns.[^5]
    - For mobile: Firebase (Remote Config, Messaging, Analytics) to tune notifications, remote configs for streak logic, referral prompts, etc.[^1]
- **Ethical guidelines**
    - “Defining, Classifying and Identifying Addictive Patterns in Digital Interfaces” (AEPD report) gives a taxonomy of patterns (gamification, infinite scroll, social validation) and guidance for using them responsibly.[^5]

If you tell me which stack you’re using (e.g., Next.js + PostHog + Firebase) I can sketch a concrete “addiction loop” architecture: events, tables, and services mapped to these mental models.
<span style="display:none">[^10][^11][^12][^13][^14][^15]</span>

<div align="center">⁂</div>

[^1]: https://amplitude.com/blog/mental-models

[^2]: https://www.simplethread.com/applying-mental-models-to-building-digital-products/

[^3]: https://www.usertesting.com/blog/9-behavioral-psychology-books-for-persuasive-ux-design

[^4]: https://uxdesign.cc/should-we-be-creating-addictive-products-exploring-the-paradox-of-hooked-61792bcd552b

[^5]: https://www.aepd.es/documento/defining-classifying-identifying-addictive-patterns.pdf

[^6]: https://www.adamwaselnuk.com/principles-and-mental-models

[^7]: https://www.linkedin.com/pulse/5-must-read-behavioral-science-books-product-managers-sofia-maradiaga-p38fe

[^8]: https://insights.aimforbehavior.com/p/the-ultimate-list-of-books-for-behavior

[^9]: https://trymata.com/blog/books-that-will-teach-you-how-to-crack-the-behavioral-and-ux-design-codes/

[^10]: https://www.paulmduvall.com/10-mental-models-i-rely-on-for-building-at-scale/

[^11]: https://www.linkedin.com/posts/sureshlb_10-mental-models-that-made-me-smarter-in-activity-7406362410120462336-29Z-

[^12]: https://www.reddit.com/r/ProductManagement/comments/1c314gp/what_are_some_mental_models_that_make_your_daily/

[^13]: https://betterprogramming.pub/5-mental-models-to-build-better-products-as-software-developers-34b8ede1d42b

[^14]: https://www.youtube.com/shorts/SFg3pD3afMg

[^15]: https://shopify.engineering/building-mental-models

