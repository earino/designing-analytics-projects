---
marp: true
theme: default
paginate: true
header: 'ECBS5228A: Designing Analytics Projects'
footer: 'Block 1: The Analytics Project Brief'
---

<!-- _class: lead -->
<!-- _paginate: false -->
<!-- _header: '' -->
<!-- _footer: '' -->

# Designing Analytics Projects

## Block 1: The Analytics Project Brief

**Eduardo Arino de la Rubia**
January 8, 2026

---

<!-- _class: lead -->

# Part 1: Course Overview
### *(15 minutes)*

---

## Welcome

Before we dive in:

- Grab coffee if you need it
- Phones away (you'll want to focus)
- We'll take breaks — this is a marathon, not a sprint

<!--
INSTRUCTOR NOTE:
Take 2-3 minutes for informal welcomes.
Ask: "Who's excited? Who's terrified? Both is the right answer."
-->

---

## A Question to Start

> **Think for 30 seconds:**
>
> What percentage of data science projects actually deliver business value?

<!--
INSTRUCTOR NOTE:
Pause. Let them think. Cold call 2-3 students for guesses.
Reveal: Studies suggest 60-85% fail to deliver intended value.
The problem usually isn't technical.
-->

---

## Why Most Analytics Projects Fail

It's rarely the model. It's usually:

- **Wrong problem** — solved something nobody needed
- **Wrong metric** — optimized the wrong thing
- **Wrong stakeholders** — built it, nobody used it
- **Wrong scope** — took too long, world moved on

This course is about avoiding those failures.

---

## What This Course Is NOT

❌ How to build models
❌ How to write Python/SQL
❌ Statistical methods
❌ Machine learning techniques

You have other courses for those.

---

## What This Course IS

✅ The work that happens **before** you write code
✅ How to scope projects that actually matter
✅ How to navigate organizational dynamics
✅ How to avoid the most common failure modes

**One framework. Applied repeatedly.**

---

## The Throughline

Your job — as a data scientist, analyst, or anyone working with data — is simple:

# Drive better decisions with data.

That's it. Everything else is in service of this.

---

## Why Projects Fail (Revisited)

Every common failure maps to a missing piece:

| Failure | What Was Skipped |
|---------|------------------|
| "Solved something nobody needed" | No clear decision to drive |
| "Optimized the wrong thing" | No counter-metrics |
| "Built it, nobody used it" | No stakeholder mapping |
| "Didn't see the disaster coming" | No pre-mortem |

The Brief prevents all four.

---

## The Single Artifact

Everything in this course revolves around one thing:

# The Analytics Project Brief

A structured framework that forces clarity **before** you start analyzing.

---

## Learning Outcomes

By the end of this course, you will be able to:

1. **Use the Analytics Project Brief** to scope projects
2. **Identify counter-metrics** and stakeholder dynamics
3. **Recognize which analyses** apply to different problems
4. **Apply influence strategies** to gain buy-in

---

## Assessment Overview

| Component | Weight | When |
|-----------|--------|------|
| Scenario → Brief | 30% | Jan 16 |
| Pen & Paper Exam | 30% | Jan 27 |
| Weekly Write-ups | 30% | Feb 10 – Mar 17 |
| Participation | 10% | During class |

Each of you gets a **unique scenario** for the Brief assignment.
No two students have the same one.

---

## Today's Roadmap (Day 1)

| Block | Time | Topic |
|-------|------|-------|
| **1** | 10:50–12:30 | The Analytics Project Brief *(you are here)* |
| | | *Lunch break* |
| **2** | 13:30–15:10 | Acquisition Analyses |
| | | *Break* |
| **3** | 15:40–17:20 | Retention & Growth Analyses |

By end of day: You'll know the Brief framework and all 9 foundational analyses.

---

## Questions Before We Dive In?

<!--
INSTRUCTOR NOTE:
Take 2-3 questions max.
"Big picture questions only — details will become clear as we go."
-->

---

<!-- _class: lead -->

# Part 2: The Analytics Project Brief
### *(45 minutes)*

---

## Why a Structured Framework?

Without structure, scoping conversations go like this:

> **Exec:** "Can you look at why revenue is down?"
> **You:** "Sure!"
> *(3 weeks later)*
> **Exec:** "This isn't what I wanted at all."

The Brief forces the hard conversations **upfront**.

---

## The Analytics Project Brief

10 sections. Each answers a critical question.

| # | Section | Key Question |
|---|---------|--------------|
| 1 | Problem & Decision | What decision will this inform? |
| 2 | Metrics | What are we optimizing? What breaks? |
| 3 | Stakeholders | Who has power? Who might block? |
| 4 | Methodology | What analyses? What data? |
| 5 | Scope | What's in? What's out? |

---

## The Analytics Project Brief (cont.)

| # | Section | Key Question |
|---|---------|--------------|
| 6 | Success Criteria | How will we know this worked? |
| 7 | Timeline | Key milestones? |
| 8 | Risks & Assumptions | What could go wrong? |
| 9 | Ethics & Privacy | PII? Bias risks? |
| 10 | Pre-Mortem | It failed. What happened? |

---

## Section 1: Problem & Decision

The most important section. Everything flows from here.

**Three questions to answer:**
1. What business question will this analysis inform?
2. Who is asking, and why now?
3. Who is the ultimate decision maker?

<!--
INSTRUCTOR NOTE:
Emphasize: "If you can't answer these, STOP. You're not ready to start."
-->

---

## Section 1: The Hypothesis

Also include a hypothesis:

> *We believe [X] because [Y], and this analysis will confirm or refute that.*

**Why?** Forces you to be specific about what you expect to find.

If you don't have a hypothesis, that's okay — mark it as **exploratory**.

---

## Check for Understanding

> **Quick check:**
> Why is "Who is asking and why now?" important?

<!--
INSTRUCTOR NOTE:
Cold call. Looking for answers like:
- Urgency/timeline implications
- Political context
- Whether this is a real priority or someone's pet project
-->

---

## Section 2: Metrics

Two parts:

### Primary Metric
What are you optimizing? **Be precise.**

❌ "Conversion rate"
✅ "Users who complete checkout / Users who reach cart page, excluding guest checkout, trailing 7 days"

---

## Section 2: Metric Definitions

A complete metric definition includes:

| Component | Example |
|-----------|---------|
| **Event/table** | `checkout_completed` events |
| **Numerator** | Users who completed checkout |
| **Denominator** | Users who viewed cart |
| **Filters** | Excluding guest checkout |
| **Time window** | Trailing 7 days |

If you can't write the SQL, you haven't defined it.

---

## Section 2: Counter-Metrics

We'll go deep on this in Part 3, but the key idea:

> **Counter-metrics** are what breaks if your primary metric succeeds.

You optimize checkout completion → Revenue per order drops (people buying cheaper stuff)

Always identify 2-3 counter-metrics.

---

## Discussion: Metric Precision

> **Think-Pair-Share (2 min):**
>
> Someone says their metric is "user engagement."
> What questions would you ask to make this precise?

<!--
INSTRUCTOR NOTE:
Give 30 sec to think, 1 min to discuss with neighbor, then share out.
Looking for: What counts as engagement? DAU? Time spent? Actions?
Which users? New? All? Time window?
-->

---

## Section 3: Stakeholders

Use the **Power-Interest Grid**:

|   | High Interest | Low Interest |
|---|---------------|--------------|
| **High Power** | Manage Closely | Keep Satisfied |
| **Low Power** | Keep Informed | Monitor |

---

## Section 3: Champions & Blockers

Beyond the grid, identify:

**Champions** — Who actively wants this to succeed?
**Blockers** — Who might resist? *Why* do they resist?

The "why" matters. People block for reasons:
- Threatens their budget
- Makes their past work look bad
- Creates work for their team

---

## Section 4: Methodology

Two parts:

### Which Analyses?
Select from the foundational analyses (we'll cover these in Blocks 2-3)

### Data Availability
| Data needed | Available? | If no, fallback? |
|-------------|------------|------------------|
| User clicks | Yes | — |
| Purchase history | Partial | Use last 6 months only |

---

## Section 4: Data Validity Checks — Stop/Go Gates

**Before you analyze, verify your data is trustworthy:**

| Check | How to Validate | Stop If... |
|-------|-----------------|------------|
| Events fire on iOS | Compare iOS vs Android event counts | >10% discrepancy |
| No duplicate users | `SELECT COUNT(*) vs COUNT(DISTINCT user_id)` | >1% duplicates |
| Attribution window consistent | Check `first_touch` vs `last_touch` logic | Multiple conflicting windows |
| Historical data complete | Count events by month | Any month <80% of expected |

**Grading note:** Your Brief must include 2+ specific checks with validation method AND stop condition.

If data is broken, **stop**. Don't draw conclusions from bad data.

<!--
INSTRUCTOR NOTE:
Emphasize this is a grading criterion. Students who write generic "we'll check data quality"
without specific checks, validation methods, and stop conditions will lose points.
-->

---

<!-- _class: lead -->

## ☕ Stretch Break
### 5 minutes

Stand up. Move around. Refill coffee.

<!--
INSTRUCTOR NOTE:
Enforce this. Attention spans need it.
Resume at exactly 5 minutes.
-->

---

## Section 5: Scope & Deliverables

Be explicit about what's **in** and **out**:

**In Scope:**
- US market only
- Last 6 months of data
- Desktop and mobile web

**Out of Scope:**
- Native app (separate project)
- International markets
- Real-time implementation

---

## Section 6: Success & Decision Criteria

**Analytical success:** What makes the analysis itself good?
- Metric defined with <20% confidence interval
- 3+ statistically significant drivers identified

**Business success:** What makes it valuable?
- Product team changes roadmap based on findings
- Clear A/B test hypotheses generated

---

## Section 6: Decision Criteria Table

Pre-commit to decisions:

| If we find... | We will... |
|---------------|------------|
| Checkout friction is #1 driver | Prioritize UX redesign |
| Price sensitivity is #1 driver | Test promotional strategy |
| No clear driver found | Run qualitative user research |

**Including the null result.** What if you find nothing?

---

## Section 6: Action Thresholds

Be specific about magnitude:

> "We will only recommend action if effect size ≥5 percentage points AND p<0.05"

> "We will not act if sample size <1000 users per variant"

This prevents "statistically significant but meaningless" results driving decisions.

---

## Sections 7-9: Quick Overview

**Timeline:** Key milestones and dates. Keep it simple.

**Risks & Assumptions:** What are you assuming is true? What could invalidate the analysis?

**Ethics & Privacy:** Does this require PII? Any bias risks? GDPR considerations?

---

## Section 10: Pre-Mortem

The most valuable section.

> **Prompt:** It's 3 months from now. This project failed spectacularly. What happened?

Write it as a story. Be specific. Be pessimistic.

This surfaces risks you wouldn't otherwise consider.

---

## Example Pre-Mortem

> We found that mobile users converted 40% less than desktop. Product redesigned the mobile checkout flow.
>
> Three months later, mobile conversion was flat. Turns out mobile users were just *browsing* — they always completed purchases on desktop. We solved the wrong problem because we didn't segment by user journey, just by device.

---

## The Brief in Practice

Key principle:

> **Fill out the Brief before you start analyzing.**

Not after. Not during. Before.

It will feel slow at first. It saves time overall.

---

## Questions on the Framework?

<!--
INSTRUCTOR NOTE:
Take 3-4 questions.
Common Q: "How long does this take?"
A: 30-60 min once you're practiced. First few times, longer.
-->

---

<!-- _class: lead -->

# Part 3: Counter-Metrics & Adversarial Thinking
### *(35 minutes)*

---

## Goodhart's Law

> "When a measure becomes a target, it ceases to be a good measure."
> — Charles Goodhart

Or more bluntly:

> "Tell me how you measure me, and I'll tell you how I'll behave."

---

## Goodhart's Law in Action

**Healthcare:** Hospitals measured on "length of stay"
→ Discharged patients early
→ Readmission rates spiked

**Education:** Schools measured on "test scores"
→ Taught to the test
→ Critical thinking declined

**Tech:** Social media measured on "engagement"
→ Optimized for outrage
→ Mental health crisis

---

## The Problem for Data Scientists

You're often asked to optimize a metric.

If you succeed, **something else gets worse**.

Your job is to figure out what that is **before** you start.

---

## Counter-Metrics Defined

> **Counter-metric:** A metric that could worsen if you optimize the primary metric.

Two types:

| Type | Definition | Example |
|------|------------|---------|
| **Guardrail** | Must not worsen | Data quality, fraud rate |
| **Tradeoff** | May worsen within bounds | Short-term revenue for LTV |

---

## The "What Breaks" Framework

Five questions to find counter-metrics:

1. **Direct negative:** What directly worsens when X improves?
2. **Quality degradation:** What quality suffers?
3. **User segments:** Which users are harmed?
4. **Temporal tradeoffs:** What long-term metrics suffer?
5. **Cross-functional:** Whose goals are threatened?

---

## Example: Checkout Optimization

**Primary metric:** Checkout completion rate

**What breaks?**
1. Revenue per order (people buy cheaper stuff to "just finish")
2. Return rate (impulse purchases get returned)
3. Customer service load (confused customers)
4. Fraud rate (less friction = more fraud)

---

## Example: Notification Optimization

**Primary metric:** Click-through rate on notifications

**What breaks?**
1. Notification opt-out rate (annoy people → they disable)
2. App uninstalls (too many notifications → rage quit)
3. Session quality (clicked but didn't engage)
4. User trust (feels spammy → brand damage)

---

## Discussion: Find the Counter-Metrics

> **Think-Pair-Share (3 min):**
>
> Primary metric: "Increase free-to-paid conversion rate"
>
> What could break if you succeed?

<!--
INSTRUCTOR NOTE:
Give 1 min to think, 2 min to discuss.
Looking for: Premature conversions → churn, free user satisfaction drops,
brand perception as "pushy," support load from confused upgrades
-->

---

## How Many Counter-Metrics?

**2-3 is right.**

Too few: You're not thinking hard enough
Too many: Analysis paralysis, false positive problem

Every additional guardrail at p<0.05 adds ~5% false alarm rate.

---

## Guardrails vs. Tradeoffs

**Guardrail:** Hard stop. If this worsens, kill the project.
- Fraud rate
- Data quality
- Legal compliance

**Tradeoff:** Acceptable within bounds. Monitor but don't stop.
- Short-term revenue (if LTV improves)
- Complexity (if value justifies it)

Label each counter-metric as one or the other.

---

## The Pre-Mortem Exercise

Now let's practice.

> **Scenario:** You're tasked with increasing user signups by 50% in Q1.

**Exercise (5 min):**
1. Individually, write a pre-mortem (2-3 sentences)
2. What went wrong? Be specific.
3. What counter-metric would have caught this?

<!--
INSTRUCTOR NOTE:
Give them 5 minutes to write. Silence is okay.
Then cold-call 3-4 students to share.
-->

---

## Pre-Mortem Sharing

Let's hear some failure stories.

<!--
INSTRUCTOR NOTE:
Cold call 3-4 students. After each one, ask:
"What counter-metric would have caught this?"

Common pre-mortems:
- Signup quality dropped (counter: D7 retention)
- Fraud increased (counter: fraud rate)
- Support overwhelmed (counter: tickets per signup)
- Brand damaged (counter: NPS)
-->

---

## Why Pre-Mortems Work

Psychology research shows:

- **Prospective hindsight** increases ability to identify reasons for outcomes by 30%
- Easier to generate specific failures than abstract risks
- Creates psychological safety to name concerns

It's not pessimism. It's **preparation**.

---

## Key Takeaways: Counter-Metrics

1. **Every metric optimization breaks something else**
2. **Use the "What Breaks" framework** to find counter-metrics
3. **Identify 2-3** — not zero, not twenty
4. **Label as Guardrail or Tradeoff**
5. **Pre-mortem** surfaces risks you'd otherwise miss

---

<!-- _class: lead -->

# Block 1 Recap

---

## Block 1 Recap

| Part | Key Takeaway |
|------|--------------|
| **Course Overview** | One framework (the Brief), applied repeatedly |
| **The Brief** | 10 sections — fill it out *before* you analyze |
| **Counter-Metrics** | What breaks if you succeed? Always ask. |

---

## Before Next Block

We'll cover the **9 foundational analyses** in Blocks 2-3.

Each one will be introduced through a completed Brief example.

**After lunch:** Funnel, Channel Attribution, Campaign Effectiveness, CAC/LTV

---

## Questions?

<!--
INSTRUCTOR NOTE:
Take 2-3 final questions.
End on time — lunch break matters.
-->

---

<!-- _class: lead -->
<!-- _paginate: false -->

# See you after lunch!

**Block 2 starts at 13:30**

Acquisition Analyses: Funnel → Attribution → Campaign → CAC/LTV
