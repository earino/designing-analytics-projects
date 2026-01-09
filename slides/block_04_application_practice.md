---
marp: true
theme: default
paginate: true
header: 'ECBS5228A: Designing Analytics Projects'
footer: 'Block 4: Application & Practice'
---

<!-- _class: lead -->
<!-- _paginate: false -->
<!-- _header: '' -->
<!-- _footer: '' -->

# Designing Analytics Projects

## Block 4: Application & Practice

**Eduardo Arino de la Rubia**
January 12, 2026

<!--
INSTRUCTOR NOTE:

**Background:** This is Day 2, Block 4 — the first teaching block after a 4-day break. Students have had time to process Day 1 but may have forgotten specifics. Today shifts from content delivery to application. The goal is for students to leave ready to complete their assignment.

**Key point:** Day 2 is practice-focused. Less new content, more application.

**Say something like:**
"Good morning! Welcome to Day 2. I hope the break gave you time to digest what we covered on Wednesday.

Today is different. Less lecture, more practice. By the end of today, you should feel ready to tackle your assignment."

**Transition:** "Let's see what we're covering this morning..."
-->

---

## Welcome Back

Day 2 Agenda:

| Block | Time | Topic |
|-------|------|-------|
| **4** | 10:50–12:30 | Application & Practice *(you are here)* |
| | | *Lunch break* |
| **5** | 13:30–15:10 | Influence for Data Scientists |
| | | *Break* |
| **6** | 15:40–17:20 | Capstone Preparation & Closing |

Today is about **applying** what you learned on Day 1.

<!--
INSTRUCTOR NOTE:

**Background:** Day 2 starts after a 4-day break. Students have had time to digest Day 1 concepts but may have forgotten details. The morning coffee break just ended, so energy should be reasonable. This block is the transition from "learning concepts" to "applying concepts."

**Key point:** Set the tone that today is hands-on. Less lecture, more practice.

**Say something like:**
"Welcome back! I hope the long weekend gave you time to let Day 1 sink in. Today is different from Day 1. Less lecture, more practice.

By the end of Day 1, you had all the vocabulary — Briefs, counter-metrics, stakeholder maps, the 9 analyses. Today we put it together. You'll work through complete scenarios, argue with each other about analysis choices, and practice under time pressure.

The goal is that by the end of today, you're ready for your assignment on Thursday."

**Energy management:** This is the first slide of Day 2. Take a moment to scan the room. How are energy levels? If people seem sluggish, consider a 30-second "stand up and stretch" before diving in.

**Transition:** "Let me show you what we'll cover this morning..."
-->

---

## Block 4 Overview

| Section | Time |
|---------|------|
| Q&A on Day 1 Content | 20 min |
| Deep Dive: A Complex Brief | 30 min |
| Group Exercise: Analysis Selection | 25 min |
| Timed Brief Practice | 10 min |
| Common Scoping Mistakes | 15 min |

<!--
INSTRUCTOR NOTE:

**Background:** This overview sets expectations for the block. The timing is tight but achievable. The sequence is deliberate: start with Q&A to surface confusion, then model excellence (deep dive), then practice as a group, then practice individually, then learn from common mistakes.

**Key point:** The block builds from passive to active: watch → discuss → practice. By the end, students have done real work.

**Say something like:**
"Here's what we'll cover this morning.

First, 20 minutes of Q&A. What confused you from Day 1? What questions came up over the weekend?

Then I'll walk through a complete, well-written Brief. You'll see how all the pieces connect.

Then YOU work — a group exercise where you debate analysis selection. Then a timed individual exercise to practice writing under pressure.

We'll close with the six most common mistakes I see in Briefs. Learn from others' errors.

Let's start with your questions from Day 1."

**Transition:** "First, let's clear up any confusion from Day 1..."
-->

---

<!-- _class: lead -->

# Part 1: Q&A on Day 1
### *(20 minutes)*

<!--
INSTRUCTOR NOTE:

**Background:** This section header transitions to the Q&A portion. After a 4-day break, students will have varying levels of recall. This Q&A serves both to surface confusion AND to get students talking early, which increases engagement for the rest of the block.

**Key point:** Q&A early in Day 2 prevents confusion from compounding.

**Say something like:**
"Let's start with questions. What came up as you reflected on Day 1 over the weekend?"

**Transition:** Wait for this slide for just a moment, then advance to show the recap framework as a memory aid.
-->

---

## Day 1 Recap: The Framework

**The Analytics Project Brief** — 10 sections:

| | |
|---|---|
| 1. Problem & Decision | 6. Success & Decision Criteria |
| 2. Metrics (Primary + Counter) | 7. Timeline |
| 3. Stakeholder Map | 8. Risks & Assumptions |
| 4. Methodology | 9. Ethics & Privacy |
| 5. Scope & Deliverables | 10. Pre-Mortem |

<!--
INSTRUCTOR NOTE:

**Background:** This table serves as a visual memory aid. Students learned these 10 sections on Day 1. Showing them helps trigger recall before asking questions. The two-column layout groups related sections: left column is "what are we doing," right column is "how will we know if it worked."

**Key point:** Use this as a reference while taking questions. Point to specific sections when answering.

**Say something like:**
"Here's the Analytics Project Brief framework from Day 1 — all 10 sections. Use this as a reference as we discuss.

The left column is about what you're doing: the problem, metrics, stakeholders, method, and scope.

The right column is about validation: success criteria, timeline, risks, ethics, and what could go wrong.

What questions do you have about any of these sections?"

**If asked:** "Do I need all 10 sections?"
A: For your assignment, yes. In industry, you adapt. But the thinking process is what matters — you should be able to answer questions about any section even if you don't write them all down.

**Transition:** "Let me also show you the analyses quick reference..."
-->

---

## Day 1 Recap: The Analyses

**Acquisition (Block 2):** Funnel (where lose them?) → Attribution (which channels?) → Campaign (did spend work?) → CAC/LTV (worth the cost?)

**Retention & Growth (Block 3):** Retention (come back?) → Power User (who matters?) → Failure (what's broken?) → Expansion (how grow?) → Ecosystem (products interact?)

<!--
INSTRUCTOR NOTE:

**Background:** This is the 9 analyses compressed into two lines. The one-word summaries in parentheses are the key questions each analysis answers. This structure follows the customer journey: acquire → retain → grow.

**Key point:** Students should be able to match a business question to an analysis type. This is the skill the group exercise will test.

**Say something like:**
"And here are the 9 analyses — 4 from Block 2 (Acquisition), 5 from Block 3 (Retention & Growth).

The parenthetical after each is the question that analysis answers. Funnel asks 'where do we lose them?' Attribution asks 'which channels work?' And so on.

Today's group exercise will test your ability to match business questions to the right analysis. If you're fuzzy on any of these, ask now.

What questions do you have about the analyses?"

**Common questions:**
- "What's the difference between Attribution and Campaign Effectiveness?" → Attribution tells you which channels get credit. Campaign Effectiveness tells you if the spend was worth it (causal).
- "When would I use Power User vs. Retention?" → Retention is about everyone. Power User is about the concentrated top — who drives most value.
- "What's Ecosystem Analysis?" → How multiple products or features interact. Relevant for multi-product companies.

**Transition:** "Any other questions from Day 1 before we move on?"
-->

---

## Questions from the Long Weekend?

> **Open floor (15 min):**
>
> What questions came up as you reflected on Day 1?

<!--
INSTRUCTOR NOTE:

**Background:** This Q&A serves two purposes: (1) surface confusion from Day 1 before we build on it, and (2) get students talking early in Day 2 to increase engagement. After a 4-day break, some concepts will have faded. Better to resurface confusion now than during the assignment.

**Key point:** Questions are signals — they reveal what stuck and what didn't.

**Facilitation approach:**
- Wait at least 10 seconds after asking. Silence is uncomfortable but productive.
- If no hands, cold-call: "What question did you have on Sunday when you were thinking about this?"
- Write questions on the board as they come — shows you're listening.
- Don't answer everything immediately. Some questions are better answered by other students.

**Common questions and quick answers:**
- "How do I choose between analyses?" → Depends on the question. We'll practice this in 30 minutes.
- "What if I don't have the data?" → That's what the Brief surfaces. Better to know now than after you've promised results.
- "How detailed should the Brief be?" → Detailed enough that someone else could take over. One page is typical.
- "Guardrail vs. tradeoff?" → Guardrail = must not cross. Tradeoff = acceptable cost. We'll see more examples.

**If no questions:** "What was most surprising about Day 1?" or "What's one thing you'd do differently on a past project after Day 1?"

**Transition:** "Let me quickly clarify a few things that often come up..."
-->

---

## Quick Clarifications

**Q: How long should a Brief take to complete?**
A: 30-60 minutes once practiced. First few times, longer.

**Q: What if I can't fill out a section?**
A: That's valuable information. "Unknown" or "To be determined" is honest. Blank is not.

**Q: Do I need all 9 analyses?**
A: No. Most projects use 2-3. The Brief's methodology section forces you to justify your choice.

<!--
INSTRUCTOR NOTE:

**Background:** These FAQs address the most common anxieties students have before their assignment. The "30-60 minutes" answer calibrates expectations. The "Unknown is honest" answer reduces perfectionism anxiety. The "2-3 analyses" answer prevents scope overload.

**Key point:** The Brief is a thinking tool, not a compliance exercise.

**Say something like:**
"These questions come up every time I teach this. Let me address them preemptively.

First: timing. Once you're practiced, a Brief takes 30-60 minutes. Your first few will take longer. That's expected.

Second: blank sections. 'I don't know' is useful information. It tells your sponsor what needs to be figured out before analysis begins. What's not acceptable is a blank section with no acknowledgment. If you don't know the answer, say so and explain what you'd need to find out.

Third: you don't need all 9 analyses. Most real projects use 2-3. The point of learning all 9 is so you can choose wisely, not so you use them all."

**If asked:** "What if my sponsor asks for an analysis I don't think is right?"
A: That's a conversation, not a conflict. Ask what decision they're trying to make. Often the 'wrong' analysis request reflects a real underlying question that a better analysis could answer.

**Transition:** "Now let's see how all the Brief sections work together in a real scenario..."
-->

---

<!-- _class: lead -->

# Part 2: Deep Dive — A Complex Brief
### *(35 minutes)*

<!--
INSTRUCTOR NOTE:

**Background:** This section transitions from Q&A (reactive, student-led) to the deep dive (proactive, instructor-led). The deep dive uses a complete, well-written Brief as a teaching example. Students see how all 10 sections work together. The scenario is MindfulApp — a meditation app considering premium feature expansion.

**Key point:** Model excellence before asking students to practice. Show them what "good" looks like.

**Say something like:**
"Now that we've cleared up questions from Day 1, let me show you what a complete, well-crafted Brief looks like.

On Day 1, I showed you each section in isolation. Now you'll see how they connect. This is a Brief I might write in my own work.

The scenario is MindfulApp — a meditation app thinking about premium features. As we walk through, pay attention to how each section builds on the previous one."

**Transition:** "Let me explain why this deep dive matters..."
-->

---

## Why Deep Dive?

Day 1 showed you Brief sections in isolation.

Now let's see how they **connect** in a complete, realistic example.

We'll walk through one Brief end-to-end and discuss:
- What makes it strong?
- What would you change?
- How do sections reference each other?

<!--
INSTRUCTOR NOTE:

**Background:** Day 1 taught each Brief section individually. But in practice, sections connect — the methodology must answer the problem, counter-metrics anticipate pre-mortem scenarios, stakeholder blockers shape how you present findings. This deep dive shows that coherence.

**Key point:** The Brief isn't 10 independent sections. They reference each other.

**Say something like:**
"Yesterday, we went through each Brief section one by one. Problem statement, metrics, stakeholders, methodology, and so on. That's the learning mode.

But in real life, you don't fill out sections in isolation. They connect. Your methodology has to actually answer the problem you stated. Your counter-metrics should anticipate the failure modes in your pre-mortem. Your stakeholder map shapes how you present findings.

This deep dive shows a complete, realistic Brief. We'll walk through it section by section and pay attention to how each section references the others. This is what coherence looks like — and it's where most points are lost in your assignment."

**If asked:** "Is this the format we should use for the assignment?"
A: The structure, yes. The exact formatting is flexible. What matters is that all sections are covered and they connect logically.

**Transition:** "Let's look at the scenario..."
-->

---

## The Scenario: MindfulApp

**Company:** MindfulApp (meditation & wellness app)
**Problem:** Growing 40% YoY but burning $8M/quarter
**Question:** Are we acquiring customers profitably? Should we scale or fix?

Let's walk through their CAC/LTV Brief section by section.

<!--
INSTRUCTOR NOTE:

**Background:** MindfulApp is a composite case based on real wellness apps (Calm, Headspace, etc.). The scenario captures a common startup tension: growth looks great, but unit economics may be broken. Series B companies often face this "grow or fix" decision. The $8M/quarter burn rate is realistic for a company at this stage.

**Key point:** This scenario is realistic — you'll see versions of it in your careers.

**Say something like:**
"Let me set the scene. MindfulApp is a meditation app — think Calm or Headspace. They're growing 40% year-over-year, which sounds great. But they're burning $8 million per quarter, which is not sustainable.

Their investors are asking a question that many growth-stage companies face: Are we acquiring customers profitably? Or are we buying growth that will never pay back?

This is the 'scale or fix' decision. If unit economics are good, pour on the gas. If they're broken, fix the leak before you scale the problem.

We're going to walk through their Brief section by section. As we go, notice how each section connects to the others."

**If asked:** "Is this a real company?"
A: It's a composite based on real companies. The specific numbers are illustrative but the dynamics are realistic.

**Transition:** "Let's start with Section 1: Problem & Decision..."
-->

---

## Section 1: Problem & Decision

| Element | MindfulApp |
|---------|------------|
| **Business question** | Are we acquiring customers profitably by channel? |
| **Who's asking** | Series B investors (path to profitability) |
| **Decision maker** | Board of Directors |
| **Hypothesis** | Organic/referral >5x LTV:CAC; paid social ~1.2x |

**Discussion:** Why does "who's asking" matter here?

<!--
INSTRUCTOR NOTE:

**Background:** This slide demonstrates what a complete Problem & Decision section looks like. Notice the specificity: not "are we acquiring profitably" but "by channel." The hypothesis is quantified (>5x, ~1.2x), which makes it testable.

**Key point:** "Who's asking" shapes everything — framing, benchmarks, timeline, politics.

**Discussion facilitation:**
Pause after the question. Wait 5-7 seconds. If no response, cold-call: "You — why does it matter that investors are asking?"

**Looking for in discussion:**
- Investors have specific expectations (industry benchmarks like 3:1 LTV:CAC)
- Board context = high stakes, career implications
- Timeline is probably tied to fundraising (Series C planning)
- Framing will need to be "investor-friendly" (unit economics language)

**Say something like:**
"Let's pause here. Why does it matter that investors are asking, rather than, say, the marketing team?

[Discussion]

The 'who' shapes everything. Investors think in LTV:CAC ratios because that's how they evaluate companies. They have benchmarks: a 3:1 ratio is healthy, below 1:1 is a red flag. If the marketing team asked, you might frame findings differently — 'how do we optimize spend?' vs. 'are we a good investment?'

Also notice the hypothesis is quantified. Not 'organic is better than paid' but '>5x vs. ~1.2x.' That's testable."

**Transition:** "Now let's look at how they defined their metrics..."
-->

---

## Section 2: Metrics

**Primary Metric:**
> LTV:CAC Ratio by Channel — (12-month projected LTV) / (Fully-loaded CAC), by acquisition source

**Counter-Metrics:**

- **Growth rate** (Tradeoff) — Cutting unprofitable channels slows growth
- **Engagement quality** (Guardrail) — Cheap users may not engage
- **Brand awareness** (Tradeoff) — Paid builds awareness even with low direct ROI

**Discussion:** Why is growth rate a "tradeoff" not a "guardrail"?

<!--
INSTRUCTOR NOTE:

**Background:** This slide shows a well-specified primary metric with appropriately labeled counter-metrics. The distinction between tradeoff and guardrail is critical — students often confuse them.

**Key point:** Tradeoffs are expected costs you accept; guardrails are lines you won't cross.

**Discussion facilitation:**
This is a concept-check question. If students struggle, it indicates Day 1 didn't land.

**Answer to surface:**
Growth rate is a tradeoff because we EXPECT cutting unprofitable channels to slow growth — that's the cost we're willing to pay for profitability. It's not a line we refuse to cross; it's a known consequence we accept.

Engagement quality is a guardrail because we DON'T want users who sign up but never engage. If a cheap acquisition channel produces non-engaging users, we'd stop using it regardless of the CAC — that's a line we won't cross.

**Say something like:**
"Why is growth rate labeled as a tradeoff rather than a guardrail?

[Wait for answers]

Growth rate is a tradeoff because cutting unprofitable channels WILL slow growth. We know this going in. If we decide unit economics matter more than growth rate right now, we accept slower growth as the cost of that decision. That's a tradeoff — an expected consequence we consciously accept.

Engagement quality is different. If we're acquiring users cheaply but they never meditate, that's not a cost we accept — that's a failure. That's a guardrail. If we cross it, we stop, regardless of how good the CAC looks."

**If asked:** "Can something switch from tradeoff to guardrail?"
A: Yes, if circumstances change. If the board says 'growth rate cannot drop below 30%', that becomes a guardrail.

**Transition:** "Now let's see who they identified as stakeholders..."
-->

---

## Section 3: Stakeholders

| | High Interest | Low Interest |
|---|---|---|
| **High Power** | CEO, CFO, Board | CTO |
| **Low Power** | Head of Growth, Paid team | Product, Engineering |

**Blocker:** Paid acquisition team — if paid social looks bad, their team shrinks from 4 to 2.

**Discussion:** How does knowing this blocker change how you present findings?

<!--
INSTRUCTOR NOTE:

**Background:** This is where the Brief shifts from technical to political. The stakeholder map reveals the landscape; the blocker analysis reveals the landmines. The paid team has existential stakes — half their team could be cut. This isn't a hypothetical; this happens.

**Key point:** Knowing blockers BEFORE you present lets you shape the message, not suppress it.

**Discussion facilitation:**
This is a politically sensitive topic. Some students may feel uncomfortable with "managing" stakeholders. Emphasize: you're not manipulating or lying. You're being strategic about HOW you communicate truth.

**Looking for:**
- Present scenarios, not verdicts ("If paid social is <2x, options include...")
- Private conversation before the big meeting (no ambushes)
- Frame as "tradeoffs leadership must decide" not "paid team failed"
- Acknowledge the work the paid team has done, even if results aren't great
- Give the paid team advance notice so they're not blindsided

**Say something like:**
"This is where things get real. The paid acquisition team — 4 people — could become 2 people if your analysis shows paid social isn't working. That's not hypothetical. That's jobs.

How does knowing this change how you present?

[Discussion]

First, you don't ambush them. Before the board meeting, you have a private conversation with the Head of Growth. 'Here's what I'm going to present. I wanted you to see it first.' This isn't political favor-trading; it's professional courtesy.

Second, you present scenarios, not verdicts. 'If paid social is below 2x, leadership has options: cut spend, change creative strategy, or accept the awareness value.' You're not saying 'fire the paid team.' You're laying out the decision space.

Third, you acknowledge what's worked. 'Paid social contributed to brand awareness growth even if direct attribution looks weak.' Don't be dishonest — but don't make people feel like failures unnecessarily."

**If asked:** "Isn't this manipulative?"
A: No. You're not hiding findings. You're being thoughtful about how truth lands. An analyst who drops a bomb in a meeting with no warning isn't being more honest — they're being careless.

**Transition:** "Let's look at the methodology they chose..."
-->

---

## Section 4: Methodology

**Cohort-based LTV modeling**
Predict lifetime value from early behavior. Needs: subscription history.

**Fully-loaded CAC by channel**
True acquisition cost. Needs: marketing spend, team allocation.

**Payback period analysis**
Months to recover CAC. Needs: monthly revenue by cohort.

**Discussion:** Why "fully-loaded" CAC? What gets missed if you just count media spend?

<!--
INSTRUCTOR NOTE:

**Background:** This slide shows how methodology connects to the problem. They're doing CAC/LTV analysis, so they need cohort-based LTV, fully-loaded CAC, and payback period. Notice each methodology line includes "Needs:" — this is the data requirements check.

**Key point:** "Fully-loaded" matters because media spend is only part of the true cost.

**Discussion facilitation:**
This is a technical concept-check. Push students to be specific about what gets missed.

**What gets missed with media-only CAC:**
- Salaries: The 4-person paid team's compensation
- Tools: Analytics platforms, creative tools, ad management software
- Agency fees: If they use external agencies for creative or buying
- Overhead: Office space, management time, etc.
- Creative production: Photo shoots, video production

**Say something like:**
"Why does the Brief specify 'fully-loaded' CAC rather than just CAC?

[Wait for answers]

If you only count media spend — the money you give to Facebook or Google — you're ignoring the salaries of the 4 people running the campaigns. You're ignoring the $50K/year you spend on analytics tools. You're ignoring the agency you hired to make the ads.

A channel might look profitable if you only count media spend but unprofitable when you load in the team cost. This matters especially for paid social, where creative production and campaign management are labor-intensive.

This is why the methodology says 'fully-loaded CAC by channel' — not just 'CAC.'"

**If asked:** "How do you allocate shared costs like office space?"
A: Common approach: proportional to headcount or time tracking. Perfect accuracy isn't possible; directional accuracy is the goal.

**Transition:** "Now let's see what they put in scope and out of scope..."
-->

---

## Section 5: Scope

**In Scope:**
- 5 channels (Paid Social, Paid Search, Organic, Referral, Influencer)
- Cohorts from last 18 months
- Monthly and annual subscribers

**Out of Scope:**
- Free tier users
- B2B partnerships
- Reactivated churned users

**Discussion:** Why exclude free tier users? Is that the right call?

<!--
INSTRUCTOR NOTE:

**Background:** This slide demonstrates good scoping — explicit in-scope AND out-of-scope lists. The discussion question is genuinely debatable; there's a reasonable argument for including free users.

**Key point:** Scoping is about making conscious choices, not just listing what you'll do.

**Discussion facilitation:**
This is a good "reasonable people disagree" moment. Let students argue both sides before providing synthesis.

**Arguments for excluding free tier:**
- Free users have different economics (zero LTV until conversion)
- Including them would muddy the paid subscriber CAC/LTV analysis
- The business question is about paying customer profitability
- Could be a separate analysis: "What's the CAC of free-to-paid conversion?"

**Arguments for including free tier:**
- Free tier is part of the acquisition funnel
- CAC should include cost of acquiring free users who never convert (that's real spend)
- Excluding them might make ratios look better than reality

**Say something like:**
"Should free tier users be in scope or out? Let me hear arguments on both sides.

[Discussion]

Both positions are defensible. The Brief chose to exclude them. Here's the logic: the investors' question is about PAYING customer profitability. Including free users who never convert would muddy that specific analysis.

But — and this is important — there's a legitimate counter-argument. The cost of acquiring free users who never convert IS a real cost. By excluding them, you might make LTV:CAC look better than the true picture.

This is a scoping choice, not a right answer. The Brief makes the choice explicit. That's what matters."

**Transition:** "Now let's see what decisions they'd make based on different findings..."
-->

---

## Section 6: Success & Decision Criteria

**Decision Criteria:**

| If we find... | We will... |
|---------------|------------|
| All channels >3x | Scale aggressively |
| Mixed (some >3x, some <2x) | Reallocate from low to high |
| Most channels <2x | Fix retention before scaling |
| Referral is 5x+ but tiny | Invest $500K in referral program |

**Discussion:** Why include the "inconclusive" outcome?

<!--
INSTRUCTOR NOTE:

**Background:** Decision criteria are often the weakest part of student Briefs. This example shows what good looks like: specific thresholds (3x, 2x, 5x), concrete actions (scale, reallocate, fix, invest $500K), and importantly — the null/mixed result case.

**Key point:** Pre-defining decisions prevents analysis paralysis and post-hoc rationalization.

**Discussion facilitation:**
The question is about why "inconclusive" matters. Many students skip this scenario.

**Why include inconclusive/mixed outcomes:**
- Most real analyses produce mixed results (not clean stories)
- Without pre-defined action, you waste weeks debating what to do
- Prevents cherry-picking: "Well, THIS channel is great..."
- Keeps you honest: if most channels are broken, don't hide behind the one that works

**Say something like:**
"Why include the 'most channels <2x' scenario? Couldn't you just figure out what to do if that happens?

[Wait for answers]

Here's what actually happens if you don't pre-define this. You finish your analysis. Most channels are mediocre. And then you spend three weeks debating what to do, with different stakeholders advocating for their favorite interpretation.

The paid team says 'but awareness!' The growth team says 'but the trend is improving!' The CFO says 'but the burn rate!' By pre-defining the decision — 'if most channels <2x, we fix retention before scaling' — you short-circuit that debate.

Also notice the last row: 'Referral is 5x+ but tiny.' This anticipates a specific finding that might get buried. Even if the answer is 'invest more,' you've pre-committed to noticing it."

**If asked:** "What if leadership overrides the pre-defined decision?"
A: That happens. The value of pre-defining isn't that it's binding — it's that overriding requires conscious choice. They have to say "I know we agreed to X, but I want Y instead." That's different from drifting into Y through analysis paralysis.

**Transition:** "Let's quickly cover timeline, risks, and ethics..."
-->

---

## Section 7-9: Timeline, Risks, Ethics

**Timeline:** 4 weeks (data → findings → board-ready)

**Key Risk:** LTV projections too optimistic
**Mitigation:** Use conservative retention curves, show sensitivity

**Ethics:** PII required (user-level data), no bias risk, GDPR compliant

**Discussion:** What could invalidate the LTV projections?

<!--
INSTRUCTOR NOTE:

**Background:** These sections are often rushed in student Briefs. Timeline, risks, and ethics feel like "administrative" sections. They're not — they're where assumptions get surfaced.

**Key point:** LTV projections are assumptions about the future. Assumptions can be wrong.

**Discussion facilitation:**
Push students to think about what makes projections fragile. This connects to the pre-mortem mindset.

**What could invalidate LTV projections:**
- Product changes: New features could improve (or worsen) retention
- Pricing changes: If they raise prices, historical LTV doesn't predict future
- Competitor entry: A new meditation app could shift the market
- Economic shifts: Recession = more churn on discretionary subscriptions
- Cohort composition: Early adopters vs. late majority have different behaviors
- Platform changes: Apple privacy updates affecting attribution and targeting

**Say something like:**
"What could make these LTV projections wrong?

[Discussion]

This is critical thinking. LTV projections assume the future looks like the past. That's often wrong.

If they launch a major new feature that improves retention, historical LTV underpredicts. If Apple changes privacy rules and targeting gets worse, historical LTV overpredicts. If a competitor launches and users churn faster, historical LTV overpredicts.

The Brief acknowledges this: 'Use conservative retention curves, show sensitivity.' That means: don't just show the happy path. Show what happens if retention is 20% worse."

**Transition:** "Now let's look at the pre-mortem — the most important section for adversarial thinking..."
-->

---

## Section 10: Pre-Mortem

> We showed paid social had 1.5x LTV:CAC and recommended cutting 60% of spend.
>
> Growth slowed from 40% to 15%.
>
> Turns out paid social drove awareness that boosted organic and referral — channels weren't independent.

**Discussion:** How could they have caught this before recommending the cut?

<!--
INSTRUCTOR NOTE:

**Background:** This pre-mortem is excellent because it tells a specific story with a causal insight. It's not "we failed because data quality" — it's a concrete failure scenario that reveals a methodological blind spot (channel interdependence).

**Key point:** Good pre-mortems reveal WHAT YOU HAVEN'T THOUGHT ABOUT yet.

**Discussion facilitation:**
Push students to think about detection mechanisms. This is how pre-mortems add value — they surface problems you can then look for.

**How they could have caught this:**
- Correlation analysis: Do organic/referral signups spike after paid campaigns?
- Geographic testing: Cut paid in one market, observe organic in that market
- Seasonal analysis: Does organic drop when paid is paused (holidays)?
- Customer surveys: "How did you hear about us?" with multi-touch option
- Time-lagged analysis: Is there a delay between paid spend and organic lift?

**Say something like:**
"This pre-mortem describes a specific failure: channels that looked independent weren't. Paid social was boosting organic in ways that didn't show up in direct attribution.

How could they have caught this before recommending the cut?

[Discussion]

The key insight is channel interdependence. If they'd looked at correlations — does organic spike after paid campaigns? — they might have noticed. Or they could have done a geographic test: cut paid in one city, see if organic drops in that city.

This is the value of pre-mortems. It's not about predicting the future. It's about asking 'what are we assuming?' The assumption here was 'channels are independent.' A good pre-mortem surfaces that assumption so you can test it."

**If asked:** "Isn't this hindsight bias?"
A: The pre-mortem is written BEFORE the analysis. The example shows what could go wrong. In practice, you write this to force yourself to think about interdependence, then you test for it.

**Transition:** "Let's step back and see how all these sections connect..."
-->

---

## How Sections Connect

The Brief isn't 10 independent sections. They reference each other:

- **Methodology** must answer the **Problem**
- **Counter-metrics** anticipate **Pre-mortem** scenarios
- **Stakeholder blockers** inform **how you present findings**
- **Decision criteria** prevent analysis-paralysis

<!--
INSTRUCTOR NOTE:

**Background:** This is the "coherence" message — the same thing that's worth 20 points in the grading rubric. Students often treat Brief sections as independent checkboxes. They're not. This slide makes the connections explicit.

**Key point:** Brief coherence is where most points are lost on the assignment.

**Say something like:**
"Let me make this explicit. The Brief isn't a checklist of 10 independent sections. They connect.

Your methodology has to actually answer the problem you stated. If your problem is 'are we acquiring profitably by channel?' and your methodology doesn't segment by channel, you have a coherence problem.

Your counter-metrics should anticipate your pre-mortem scenarios. MindfulApp's pre-mortem was about channels being interdependent. Their counter-metric 'brand awareness' connects to that — it's watching for the same failure mode.

Your stakeholder map informs how you present. If the paid team is a blocker, that shapes your presentation strategy.

On your assignment, this is where most points are lost. Sections that feel disconnected. A pre-mortem that describes a risk not mentioned in the risks section. A methodology that can't answer the problem. Look for these when you self-review."

**Transition:** "Let's look at what makes this Brief strong overall..."
-->

---

## What Makes This Brief Strong?

1. **Specific metric definition** — Not just "LTV:CAC" but fully specified
2. **Counter-metrics with types** — Guardrail vs. tradeoff is clear
3. **Named blocker with motivation** — "Jobs on the line" is concrete
4. **Decision criteria include null result** — What if we find nothing?
5. **Pre-mortem is specific** — Not generic "something went wrong"

<!--
INSTRUCTOR NOTE:

**Background:** This slide summarizes the quality markers from the grading rubric. Each point corresponds to something students often miss.

**Key point:** These five elements distinguish a strong Brief from a weak one.

**Say something like:**
"Let me summarize what makes this Brief strong. These are the things you should check in your own work.

First: specific metric definition. Not 'LTV:CAC' but '12-month projected LTV / fully-loaded CAC by acquisition source.' Could you write the query? If yes, it's specific enough.

Second: counter-metrics WITH TYPES. Growth rate is a tradeoff. Engagement quality is a guardrail. Not just 'here are some other things to watch.'

Third: a named blocker with motivation. Not 'the marketing team might resist' but 'the paid acquisition team could lose half their headcount — that's their motivation to resist.'

Fourth: decision criteria include the null result. What if you find nothing conclusive? Most analyses produce mixed results. Plan for it.

Fifth: the pre-mortem is specific. It tells a story with a causal insight. Not 'data quality was bad' but 'we assumed channels were independent and they weren't.'

Check your work against these five things."

**Transition:** "Now, what would you change about this Brief?"
-->

---

## What Would You Change?

> **Discussion (3 min):**
>
> Looking at this Brief, what's missing or could be stronger?

<!--
INSTRUCTOR NOTE:

**Background:** This is an important "critique" exercise. Students need practice identifying weaknesses, not just strengths. No Brief is perfect — developing critical eye helps students improve their own work.

**Key point:** Even good Briefs have room for improvement. The skill is seeing what's missing.

**Facilitation:**
Give students 30 seconds to think before opening discussion. If no one speaks, cold-call: "You — one thing you'd change."

**Possible answers:**
- No sensitivity analysis specified for LTV projections → How much does the answer change if retention is 20% worse?
- Doesn't address channel interaction explicitly in methodology → The pre-mortem assumes independent channels, but methodology doesn't test for it
- Timeline might be aggressive for board-quality work → 4 weeks is tight for cohort analysis, LTV modeling, AND board-ready presentation
- Could specify action thresholds more precisely → "Scale aggressively" is vague. How much? Which channels first?
- No contingency for data gaps → What if we can't get team allocation data for fully-loaded CAC?
- Ethics section is thin → "No bias risk" — really? What about different privacy expectations across user demographics?

**Say something like:**
"No Brief is perfect. What would you improve?

[Discussion]

Some things I'd push on: The pre-mortem worries about channel interaction, but the methodology doesn't explicitly test for it. That's a gap. The timeline — 4 weeks — is aggressive for cohort analysis AND LTV modeling AND board-ready presentation. And 'scale aggressively' — what does that mean? 2x? 5x? The more specific your decision criteria, the less room for post-hoc debate."

**Transition:** "Alright, now it's your turn. Let's do some group work..."
-->

---

<!-- _class: lead -->

# Part 3: Group Exercise — Analysis Selection
### *(30 minutes)*

---

## The Exercise

You'll see 3 business scenarios.

For each one:
1. **Which foundational analyses apply?** (Pick 2-3)
2. **Why those analyses?** (Justify your choice)
3. **What's the primary metric?** (Be specific)

Work in groups of 3-4. You'll present and defend your choices.

<!--
INSTRUCTOR NOTE:

**Background:** This is the most interactive part of Block 4. Students work in groups, argue about analysis selection, and then defend their choices publicly. This simulates real work — you'll always have to justify your methodology to stakeholders.

**Key point:** There are multiple reasonable answers. The skill is justifying your choice, not finding "the right" one.

**Group formation (1 min):**
- Count off: "1, 2, 3, 4, 1, 2, 3, 4..." to form groups
- Or let them self-select into groups of 3-4
- Mixed backgrounds are ideal (diverse perspectives)

**Timing:**
- 2 min to read Scenario A
- 5 min group work on A
- 5 min share-out and debate on A
- Repeat for B and C
- Total: ~25-30 min

**Facilitation approach:**
- Walk around during group work, listen but don't answer questions
- During share-out, push back on EVERY answer: "Why not [X] instead?"
- Highlight disagreements between groups: "Group 1 said Funnel, Group 2 said Attribution — let's hear why"
- Don't reveal a "correct" answer — there isn't one

**Say something like:**
"Here's how this works. You'll see a business scenario. In your groups, you have 5 minutes to decide: which 2-3 analyses would you do, why, and what's the primary metric?

Then you'll share out and defend your choices. I'll push back. Other groups will disagree. That's the point — you need to be able to justify your methodology.

Form groups of 3-4 now. [Pause for group formation] First scenario coming up..."

**Transition:** "Here's Scenario A..."
-->

---

## Scenario A: StreamBox

**Company:** StreamBox (music streaming service)
**Situation:** Premium subscriber growth is flat. Free tier is growing but not converting. Marketing spend is up 30% but results aren't scaling.

**The ask from the CMO:** "Help me understand what's working and what's not in our growth engine."

> **Your task:** Which 2-3 analyses? Why? What primary metric?

<!--
INSTRUCTOR NOTE:

**Background:** StreamBox is inspired by Spotify's freemium model. The scenario describes a classic growth-stage problem: lots of free users, marketing spend increasing, but paid conversion stalling. This is a multi-part problem — no single analysis will solve it.

**Key point:** The vague ask ("what's working and what's not") is intentional. Students must narrow it down.

**Give groups 5 minutes to work, then move to discussion slide.**

**Reasonable analysis choices:**
- Funnel Analysis: Where are free users dropping off before premium? What's the conversion rate at each stage?
- CAC/LTV: Is the marketing spend producing profitable customers? Which channels are efficient?
- Expansion/Monetization: What triggers free→paid conversion? Which behaviors predict upgrade?
- Attribution: Which channels are driving (or not driving) premium signups?

**Less appropriate (but discuss if raised):**
- Retention: Not directly answering "what's working" — unless they reframe as "are we losing converts?"
- Failure Analysis: Could apply if they want to understand why free users don't convert

**Transition:** After 5 min: "Time. Let's hear from groups..."
-->

---

## Scenario A: Discussion

> **Groups share (5 min):**
>
> What analyses did you choose? Why?

<!--
INSTRUCTOR NOTE:

**Background:** This is the debate portion. The goal isn't consensus — it's exposing different reasoning. Students learn as much from defending their choices as from hearing alternatives.

**Key point:** Push back on every answer. Make students justify.

**Facilitation approach:**
1. Call on one group: "What did you pick and why?"
2. Push back: "Why Funnel and not Attribution?"
3. Ask another group: "Did anyone pick something different?"
4. Highlight the tension: "So Group 1 would start with the funnel, Group 2 would start with channels. Both are defensible. What would make you choose one over the other?"

**Good pushback questions:**
- "If you had to pick ONLY ONE, which would it be?"
- "What data would you need for that analysis? Do they have it?"
- "If the CMO pushed back and said 'I don't care about funnel, I want to know if marketing is working,' what would you say?"

**Wrap-up synthesis:**
"Multiple approaches work here. The key is justifying your choice based on the business question. Funnel answers 'where do we lose people?' Attribution answers 'which channels work?' CAC/LTV answers 'is our spend efficient?' All are valid interpretations of 'what's working.'

In real life, you'd have a conversation with the CMO to narrow it down."

**Transition:** "Let's try another one. Scenario B is different — it's about diagnosis, not growth..."
-->

---

## Scenario B: QuickShip

**Company:** QuickShip (e-commerce logistics)
**Situation:** Customer complaints about delivery failures have tripled in 6 months. NPS dropped from 45 to 28. Operations says "it's not us, it's the carriers."

**The ask from the COO:** "Figure out what's actually going wrong and who's responsible."

> **Your task:** Which 2-3 analyses? Why? What primary metric?

<!--
INSTRUCTOR NOTE:

**Background:** QuickShip is a diagnostic scenario — something is broken, we don't know what. This is different from StreamBox (growth optimization). The "finger-pointing" dynamic (Operations blaming carriers) is common and politically charged.

**Key point:** This is exploratory. You don't know the root cause yet. Start with diagnosis.

**Give groups 5 minutes to work, then move to discussion slide.**

**Reasonable analysis choices:**
- Failure Analysis: Categorize why deliveries fail — carrier? address quality? inventory? This is the core analysis.
- Funnel Analysis: Where in the delivery process do failures occur? (Order → Pick → Pack → Ship → Deliver)
- Retention Analysis: Are affected customers churning? What's the downstream revenue impact?

**Less appropriate (but discuss if raised):**
- CAC/LTV: Not relevant — this is about operations, not acquisition
- Attribution: Wrong domain — this isn't about marketing channels

**Key insight to surface:**
This is exploratory — they don't know the root cause. You can't optimize something until you understand it. Failure Analysis is the natural starting point.

**Transition:** After 5 min: "Time. What's the right approach here?"
-->

---

## Scenario B: Discussion

> **Groups share (5 min):**
>
> What analyses did you choose? Why?

<!--
INSTRUCTOR NOTE:

**Background:** This discussion should surface the difference between diagnostic (exploratory) and optimization analyses. QuickShip doesn't know what's broken — they need to find out first.

**Key point:** Failure Analysis is the natural starting point. You diagnose before you optimize.

**Facilitation approach:**
1. Ask: "What did you pick?" Expect Failure Analysis as the top answer.
2. If someone says Funnel: "Good — how is that different from Failure Analysis here?"
3. If someone says Retention: "Why track retention? What does that tell you about root cause?"

**Good pushback questions:**
- "Operations says it's the carriers. How would you test that claim?"
- "What if you do Failure Analysis and find 47% is 'carrier fault'? Is that actionable?"
- "Who's the blocker here? How would you present findings that blame Operations?"

**Stakeholder angle:**
This is politically charged. Operations is blaming carriers. If you find Operations is at fault (bad address validation, inventory issues), you need to handle that carefully. This connects to Block 5 (Influence).

**Wrap-up synthesis:**
"This is diagnostic work. You don't know what's broken, so you start with Failure Analysis to categorize problems. Then you can decide what to fix.

Notice the political layer: someone's going to look bad. Your Brief should identify Operations as a potential blocker and plan for how to present findings diplomatically."

**Transition:** "Last scenario. This one is about product synergies..."
-->

---

## Scenario C: FinTrack

**Company:** FinTrack (personal finance app)
**Situation:** App has 3 products: Budgeting, Investing, and Credit Score. Each team optimizes independently. CEO suspects "we're leaving money on the table by not connecting these."

**The ask from the CEO:** "Should we invest in cross-product features? Is there synergy?"

> **Your task:** Which 2-3 analyses? Why? What primary metric?

<!--
INSTRUCTOR NOTE:

**Background:** FinTrack is inspired by apps like Mint/NerdWallet that have multiple product lines. The scenario surfaces a classic product strategy question: are our products complements or substitutes? Do multi-product users have higher LTV, or is it just selection bias?

**Key point:** Correlation vs. causation is the trap here. Multi-product users may look better without causation.

**Give groups 5 minutes to work, then move to discussion slide.**

**Reasonable analysis choices:**
- Ecosystem Analysis: Are products complements or substitutes? Do users who try Budgeting also try Investing?
- Power User Analysis: Who are the multi-product users? Are they more valuable? What behaviors define them?
- Retention Analysis: Do multi-product users retain better? Is that causal or selection?

**The selection bias trap:**
Students will likely observe: "Multi-product users have higher LTV!" The pushback is: Is that because using multiple products CAUSES higher value, or do inherently more engaged users just use more products?

This is the tutorial completion trap from Block 1 — correlation doesn't imply causation.

**Transition:** After 5 min: "Let's discuss — and watch out for a trap..."
-->

---

## Scenario C: Discussion

> **Groups share (5 min):**
>
> What analyses did you choose? Why?

<!--
INSTRUCTOR NOTE:

**Background:** This discussion MUST surface the selection bias trap. It's the most important learning moment in the exercise.

**Key point:** Multi-product correlation ≠ causation. Engaged users use more products; that doesn't mean more products CAUSE engagement.

**Facilitation approach:**
1. Let a group present: "We'd look at LTV of multi-product users vs. single-product users."
2. Trap sprung: "Great — and if you find multi-product users have 2x LTV, what do you recommend?"
3. If they say "invest in cross-product features": Push back hard.

**The pushback script:**
"Wait. If multi-product users have higher LTV, does that mean cross-product features will increase LTV? Or is it that inherently engaged users happen to use multiple products?

Remember the tutorial completion example from Day 1? Users who complete tutorials retain better. Does that mean forcing tutorials causes retention? No — engaged users complete tutorials AND retain. Same trap here."

**How to avoid the trap:**
- Look at users BEFORE they adopted second product. Were they already higher-value?
- Run an A/B test: promote cross-product features to some users, not others
- Use a quasi-experiment: cohorts before/after cross-product features launched

**Wrap-up synthesis:**
"Ecosystem Analysis tells you if there's correlation. It doesn't tell you if there's causation. Your Brief should acknowledge this — if you find correlation, the recommendation isn't 'build cross-product features' but 'test whether cross-product features improve outcomes.'"

**Transition:** "Let's debrief on what these three scenarios taught us..."
-->

---

## Debrief: Why Reasonable People Disagree

There's no single "right" answer to analysis selection.

It depends on:
- **What data is available**
- **What decisions need to be made**
- **What's the timeline**
- **What's been tried before**

The Brief framework forces you to **justify** your choice, not just make it.

<!--
INSTRUCTOR NOTE:

**Background:** This slide provides closure to the group exercise. The meta-lesson isn't "here are the right answers" — it's "multiple approaches are valid, but you must justify your choice."

**Key point:** The Brief forces justification. That's its power.

**Say something like:**
"Let me step back from the scenarios. What did we learn?

First: there's no single right answer. StreamBox could reasonably start with Funnel, Attribution, or CAC/LTV. QuickShip could start with Failure Analysis or Funnel. All are defensible.

Second: context matters. What data do you have? What decision needs to be made? What's the timeline? Two analysts with the same scenario might choose different approaches based on different constraints.

Third: the Brief forces you to justify your choice. That's the point. You can't just say 'we'll do Funnel Analysis.' You have to say WHY Funnel Analysis answers the business question better than Attribution or CAC/LTV for THIS situation.

That justification is what separates good analysts from order-takers. Anyone can run a query. Knowing which query to run, and why, is the skill."

**Energy check:** This is about 70 minutes into the block. If energy is flagging, consider a 1-minute "stand up and stretch" before moving to timed practice.

**Transition:** "Now let's practice under time pressure. This is what your assignment will feel like..."
-->

---

<!-- _class: lead -->

# Timed Brief Practice
### *(10 minutes)*

---

## Your Assignment Preview

On Thursday, you'll receive a unique 2-page scenario. You'll complete a full Brief.

Right now, you'll practice **under time pressure**. This is what Part C of the exam feels like.

**Ready?**

<!--
INSTRUCTOR NOTE:

**Background:** This timed exercise simulates exam conditions. Students often underestimate how long Brief sections take to write well. This exercise calibrates expectations and builds confidence.

**Key point:** Exam conditions are faster than you expect. Practice now.

**Say something like:**
"On Thursday, you'll get your assignment — a 2-page scenario, unique to you. You'll complete a full Brief.

Right now, we're going to practice under time pressure. This is 10 minutes. It's tight. That's intentional.

The goal isn't to produce perfect work. The goal is to experience how quickly 10 minutes goes when you're thinking carefully about metrics and blockers.

Ready?"

**Transition:** [Pause dramatically] "Here's the exercise..."
-->

---

## Timed Exercise (10 minutes)

**Use the StreamBox scenario from the previous exercise.**

Write these sections:
1. **Primary Metric** — Full operational definition (2 min)
2. **One Counter-Metric** — Label as Guardrail or Tradeoff, explain why it could break (3 min)
3. **One Blocker** — Name the role, their motivation to resist, and your mitigation (3 min)

**Work alone. Timer starts now.**

<!--
INSTRUCTOR NOTE:

**Background:** This is individual work under time pressure. The goal is for students to experience how quickly time goes when writing precise metrics and thinking through blockers. 10 minutes is intentionally tight.

**Key point:** Time pressure reveals gaps. If you struggle with metric precision, now you know what to practice.

**Facilitation:**
1. Set a visible 10-minute timer (phone timer, projected timer, whatever works)
2. Say: "Work alone. Timer starts... now."
3. Walk around the room silently. Don't answer questions. If someone asks something, say: "On the exam, I can't help. Figure it out."
4. At 5 minutes, announce: "Five minutes left."
5. At 10 minutes: "Pens down."

**What to look for while walking:**
- Are students writing immediately or staring at the page?
- Are metrics specific or vague?
- Are people getting stuck on counter-metrics?
- Is anyone visibly stressed? (Normal — this is calibration)

**After timer:**
"Pens down. How did that feel?"

Expect answers like:
- "Not enough time for the metric"
- "I couldn't think of a blocker"
- "I forgot what Guardrail vs Tradeoff means"

All of these are useful data for what students need to review.

**Transition:** "Let's debrief quickly..."
-->

---

## Timed Exercise Debrief

> **Quick share (2 min):**
>
> How did that feel? What was hardest under time pressure?

<!--
INSTRUCTOR NOTE:

**Background:** This debrief validates the struggle and motivates practice before Thursday. The key message: the discomfort is useful information.

**Key point:** Now you know what to practice before the assignment.

**Facilitation:**
Ask: "How did that feel? What was hardest?"
Let 2-3 students share. Don't fix their answers — just acknowledge.

**Common struggles and responses:**
- "Metric precision takes forever" → Yes. That's why we practice. On Thursday, budget more time for metrics.
- "I couldn't think of a counter-metric" → Review the "What Breaks" framework. 5 questions to generate counter-metrics.
- "Blocker motivation was hard" → You need to put yourself in their shoes. What do they care about? What threatens them?
- "I kept re-reading the scenario" → That's normal. On the assignment, you'll have more time. But efficient reading matters.

**Say something like:**
"I asked how that felt. Most of you probably felt rushed. That's intentional.

The point isn't to produce great work in 10 minutes. The point is to surface where you struggle. If you couldn't write a precise metric quickly, that's information — practice that before Thursday. If you blanked on counter-metrics, review the 'What Breaks' framework tonight.

Your assignment is Thursday. You now know what to work on."

**Transition:** "Before we wrap up, let me show you the most common mistakes I see in Briefs..."
-->

---

<!-- _class: lead -->

# Part 4: Common Scoping Mistakes
### *(15 minutes)*

---

## Mistake 1: Vague Metrics

❌ **Bad:** "Improve user engagement"

✅ **Good:** "Increase D7 retention (users with ≥1 `app_open` on day 7 / users who `signup_complete` on day 0) from 35% to 42%"

**The test:** Can you write the SQL? If not, it's not defined.

<!--
INSTRUCTOR NOTE:

**Background:** Vague metrics are the #1 mistake in student Briefs. "Engagement," "satisfaction," "growth" — all meaningless without operational definitions. This slide establishes the standard: SQL-level precision.

**Key point:** The SQL test is definitive. If you can't write the query, the metric isn't defined.

**Say something like:**
"This is the most common mistake I see. 'Improve user engagement.' What does that mean? App opens? Time spent? Features used? Sessions per week?

'Engagement' is not a metric. It's a category that contains dozens of possible metrics. Your Brief needs to pick one and define it precisely.

Here's the test: can you write the SQL query? If the answer is 'I'd need to figure out what tables to use and what to count,' the metric isn't defined yet.

Look at the good example: D7 retention, defined as users with at least one app_open event on calendar day 7 after signup_complete on day 0. That's queryable. You know exactly what to count."

**Transition:** "Second mistake: no counter-metrics..."
-->

---

## Mistake 2: Missing Counter-Metrics

❌ **Bad:** Only tracking the primary metric

✅ **Good:** Identifying 2-3 things that could break

**Example:** You optimize checkout conversion. AOV drops 15%, fraud triples. You "won" on conversion but lost overall.

**The test:** What could go wrong if you succeed? If you can't answer, you haven't thought hard enough.

<!--
INSTRUCTOR NOTE:

**Background:** Missing counter-metrics is the second most common mistake. Students optimize for the primary metric without asking what could break. This is Goodhart's Law in action.

**Key point:** Optimization without counter-metrics is dangerous. You WILL break something.

**Say something like:**
"Second mistake: no counter-metrics. You track conversion rate, you optimize conversion rate, conversion goes up. Victory, right?

Meanwhile, average order value dropped 15% because you added aggressive discount pop-ups. Fraud tripled because you removed friction from checkout. Customer satisfaction tanked because you're pushing too hard.

You 'won' on conversion but lost overall. That's what happens without counter-metrics.

Here's the test: what could go wrong if you succeed on your primary metric? If you can't answer, you haven't done the adversarial thinking."

**If asked:** "How do I know which counter-metrics to track?"
A: Use the 'What Breaks' framework: What directly worsens? What quality degrades? Which users are harmed? Which long-term metrics suffer? Which other teams' goals are threatened?

**Transition:** "Third mistake: ignoring stakeholders..."
-->

---

## Mistake 3: Stakeholder Blind Spots

❌ **Bad:** "We'll present to the leadership team"

✅ **Good:** Named stakeholders with power, interest, and motivation

**The killer:** The blocker you didn't identify who kills your project in a meeting you weren't invited to.

**The test:** Who has veto power? Who might resist? Why?

<!--
INSTRUCTOR NOTE:

**Background:** Stakeholder blind spots kill more projects than technical failure. The most dangerous blocker is the one you didn't identify — the person who torpedoes your recommendation in a meeting you weren't in.

**Key point:** "The leadership team" is not a stakeholder. Specific people are stakeholders.

**Say something like:**
"Third mistake: stakeholder blind spots. 'We'll present to the leadership team.' That tells me nothing.

Who specifically? The CEO? The CFO? The Head of Marketing? Each has different interests, different concerns, different power. 'Leadership' is not a stakeholder. Sarah the CFO is a stakeholder. Marcus the VP of Ops is a stakeholder.

Here's what happens when you don't map stakeholders: someone you didn't anticipate — someone whose budget, headcount, or reputation is threatened by your findings — raises objections in a meeting you weren't invited to. Your beautiful analysis dies in a room you've never entered.

The test: Who has veto power over acting on your findings? Who might resist? Why would they resist?"

**Transition:** "Fourth mistake: scope creep..."
-->

---

## Mistake 4: Scope Creep

❌ **Bad:** "We'll also look at [tangentially related thing]"

✅ **Good:** Explicit "Out of Scope" section

**Warning signs:**
- "While we're at it..."
- "It would be easy to also..."
- "Leadership asked if we could add..."

**The test:** Does adding this help the decision we're trying to inform? If not, it's out of scope.

<!--
INSTRUCTOR NOTE:

**Background:** Scope creep is death by a thousand additions. Each small addition seems harmless, but they compound. A 2-week analysis becomes 6 weeks, and the original decision window has passed.

**Key point:** "Out of Scope" is as important as "In Scope." Saying no is a skill.

**Say something like:**
"Fourth mistake: scope creep. 'While we're at it, we should also look at X.' 'It would be easy to add Y.' 'Leadership mentioned they'd love to see Z.'

Each addition seems small. But they compound. Suddenly your 2-week analysis is 6 weeks, the decision window has closed, and you've delivered a comprehensive report that nobody acts on because the moment passed.

The warning phrases: 'while we're at it,' 'it would be easy to also,' 'leadership mentioned.' These are scope creep triggers.

Here's the test: does this addition help the decision we're trying to inform? Not 'is it interesting' — is it decision-relevant? If not, it's out of scope.

An explicit 'Out of Scope' section in your Brief is your shield. When someone asks to add something, you point to the Brief: 'We agreed this is out of scope for this analysis. We can do a separate project if needed.'"

**Transition:** "Fifth mistake: no decision criteria..."
-->

---

## Mistake 5: No Decision Criteria

❌ **Bad:** "We'll analyze and see what we find"

✅ **Good:** "If we find X, we'll do Y. If we find Z, we'll do W."

**Including the null result:** What if you find nothing conclusive?

**The test:** Before you start, do you know what actions different findings would trigger?

<!--
INSTRUCTOR NOTE:

**Background:** "We'll analyze and see what we find" is analysis for its own sake. Without decision criteria, you'll produce insights that don't drive action. This is how analytics work becomes shelf-ware.

**Key point:** Define decisions BEFORE analysis. If you don't know what you'd do with different results, why are you analyzing?

**Say something like:**
"Fifth mistake: no decision criteria. 'We'll analyze and see what we find.' That's not a project — that's exploration.

Exploration has its place. But if someone is paying for your time, they usually want decisions, not insights. Before you start, you should know: if I find X, we do this. If I find Y, we do that. If I find nothing conclusive, here's what happens.

The null result is crucial. Most analyses produce mixed or inconclusive results. If you haven't planned for that, you'll waste weeks after delivery debating what the results 'really mean.'

Here's the test: before you start, do you know what actions different findings would trigger? If not, have that conversation with your sponsor. Force them to commit: 'If we find LTV:CAC below 2x, what will you do?' Get that answer before you start the work."

**Transition:** "Last mistake: the most dangerous one..."
-->

---

## Mistake 6: Correlation as Causation

❌ **Bad:** "Users who do X retain better, so we should make everyone do X"

✅ **Good:** "Users who do X retain better. We recommend A/B testing whether forcing X improves retention."

**The trap:** Engaged users do everything. Forcing behavior on disengaged users rarely works.

**The test:** Is this correlation or causation? How would we know?

<!--
INSTRUCTOR NOTE:

**Background:** This is the selection bias trap we've discussed throughout the course. It's mistake #6 but arguably the most dangerous. Recommendations based on correlation-causation confusion waste resources and damage analyst credibility.

**Key point:** Correlation identifies hypotheses. Experiments test causation.

**Say something like:**
"Last mistake, and the most dangerous: confusing correlation with causation.

'Users who complete the tutorial retain 2x better. Let's make the tutorial mandatory.'

What actually happens: signup drops 40%, and users who do complete the tutorial now retain at the same rate as everyone used to. The tutorial didn't cause retention — engaged users completed tutorials AND retained. You just filtered out the disengaged users at signup.

This is the tutorial completion example from Day 1. It shows up everywhere. Power users do X, so make everyone do X. Multi-product users are more valuable, so push everyone to multiple products. Tutorial completers retain better, so mandate tutorials.

The correlation is real. The causation is a hypothesis. An analyst who confuses them will make expensive recommendations that don't work.

Here's the test: is this correlation or causation? If I forced this behavior on users who wouldn't naturally do it, would the outcome change? If you're not sure, the honest recommendation is 'A/B test this hypothesis.'"

**Transition:** "These six mistakes share a common root cause..."
-->

---

## The Meta-Mistake

All these mistakes share a root cause:

> **Starting analysis before finishing the Brief.**

The Brief exists to surface these issues **before** you waste time.

30 minutes of scoping saves 30 hours of wrong analysis.

<!--
INSTRUCTOR NOTE:

**Background:** This is the core message of the entire course. Every mistake we've discussed — vague metrics, missing counter-metrics, blocker blind spots, scope creep, no decision criteria, confusing correlation with causation — stems from skipping the scoping work. The Brief is uncomfortable because it forces hard conversations. Students will be tempted to skip to "the real work" (analysis). This slide is the intervention.

**Key point:** 30 minutes of scoping saves 30 hours of wrong analysis. The Brief is the work.

**Say something like:**
"I want you to notice something about all the mistakes we just covered. They have a common root cause.

Vague metrics? That happens when you start analyzing before you've defined what you're measuring. Missing counter-metrics? That happens when you're excited to optimize something and don't pause to ask what could break. Blocker blind spots? That's from not mapping stakeholders before you present. Scope creep? That's from not drawing boundaries upfront.

All of these get caught if you fill out the Brief BEFORE you start analyzing.

I know the temptation. You get an exciting analysis request. You want to dive into the data. SQL is fun. Building models is fun. Scoping conversations are uncomfortable.

But here's the math: 30 minutes of scoping saves 30 hours of wrong analysis. The time you spend on the Brief is not overhead — it's the actual work of ensuring your analysis matters.

When you get your scenario Thursday, resist the urge to start analyzing. Fill out the Brief first. It will feel slow. It will save you."

**If asked:** "What if the Brief takes longer than 30 minutes?"
A: That's fine, especially at first. The time estimate is for someone practiced. Your first few Briefs will take longer. That's expected.

**Transition:** "Let me summarize what we covered..."
-->

---

## Block 4 Summary

| Section | Key Takeaway |
|---------|--------------|
| **Q&A** | Questions are valuable — gaps in understanding surface |
| **Deep Dive** | Brief sections connect; they're not independent |
| **Analysis Selection** | Reasonable people disagree; justify your choice |
| **Common Mistakes** | Brief prevents these; fill it out *before* you analyze |

<!--
INSTRUCTOR NOTE:

**Background:** This summary reinforces the four main lessons from Block 4. Students should leave with these takeaways firmly in mind before lunch.

**Key point:** Four things to remember: questions reveal gaps, sections connect, justify choices, Brief prevents mistakes.

**Say something like:**
"Let me summarize what we covered this morning.

Q&A: Questions aren't a sign of weakness. They're a sign of engagement. The gaps in understanding you surfaced this morning are gaps you can now fill before Thursday.

Deep Dive: The Brief isn't 10 independent sections. They reference each other. Your methodology must answer your problem. Your counter-metrics should anticipate your pre-mortem. Your stakeholder map shapes how you present.

Analysis Selection: Reasonable people disagree about which analyses to use. The skill isn't finding 'the right answer' — it's justifying your choice based on the business question and constraints.

Common Mistakes: Vague metrics, missing counter-metrics, stakeholder blind spots, scope creep, no decision criteria, correlation-causation confusion. The Brief prevents all of these — but only if you fill it out BEFORE you start analyzing."

**Transition:** "Any final questions before lunch?"
-->

---

## Questions Before Lunch?

<!--
INSTRUCTOR NOTE:

**Background:** This is the final Q&A before lunch. Keep it short — afternoon energy depends on a proper break.

**Key point:** End on time. Protect the lunch break.

**Facilitation:**
- Take 2-3 questions maximum
- If questions run long, say: "Great question — let's continue at 13:30"
- Don't let one student monopolize the remaining time

**Say something like:**
"Quick questions before lunch? [Take 2-3] Great — enjoy your break. Be back by 13:30 for Block 5: Influence for Data Scientists. That's where we learn how to get people to act on your analysis."

**Logistics reminder:**
- Lunch is approximately 1 hour
- Block 5 starts at 13:30
- Consider announcing where lunch is / recommending places if unfamiliar campus

**Transition:** Move to closing slide.
-->

---

<!-- _class: lead -->
<!-- _paginate: false -->

# Lunch Break!

**Block 5 starts at 13:30**

Influence for Data Scientists

