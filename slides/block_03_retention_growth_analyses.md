---
marp: true
theme: default
paginate: true
header: 'ECBS5228A: Designing Analytics Projects'
footer: 'Block 3: Retention & Growth Analyses'
---

<!-- _class: lead -->
<!-- _paginate: false -->
<!-- _header: '' -->
<!-- _footer: '' -->

# Designing Analytics Projects

## Block 3: Retention & Growth Analyses

**Eduardo Arino de la Rubia**
January 8, 2026

---

## Block 3 Overview

| Section | Time |
|---------|------|
| Retention Analysis | 20 min |
| Power User Analysis | 13 min |
| Mini-Case Exercise | 10 min |
| Failure Analysis | 13 min |
| Expansion & Monetization | 10 min |
| Ecosystem Analysis | 12 min |
| Day 1 Wrap-up | 8 min |

---

## The Retention & Growth Questions

Block 2 was about **getting** customers.
Block 3 is about **keeping** and **growing** them.

> Acquisition without retention is a leaky bucket.

The analyses in this block answer:
- Why do they leave? (Retention)

- Who matters most? (Power User)

- What's broken? (Failure)

- How do they grow? (Expansion)

<!--
INSTRUCTOR NOTE:

**Background:** This slide frames Block 3 as the natural continuation of Block 2. Block 2 was acquisition — getting customers in the door. Block 3 is retention and growth — keeping them and making them more valuable. The "leaky bucket" metaphor is powerful and should be emphasized.

**Key point:** Acquisition without retention is unsustainable. Block 3 addresses the other half of the customer journey.

**Say something like:**
"Block 2 was about getting customers. Funnel analysis, attribution, campaign effectiveness, CAC/LTV — all about acquisition.

Block 3 is about keeping and growing them.

Here's the metaphor: acquisition without retention is a leaky bucket. You can pour water in as fast as you want, but if it's leaking out the bottom, you'll never fill it.

The four analyses in this block address different questions:

Retention: Why do they leave? Understanding churn.
Power User: Who matters most? Finding your best customers.
Failure: What's broken? Root cause analysis.
Expansion: How do they grow? Upsells, upgrades, monetization.

Notice these follow the customer journey. First you acquire them (Block 2). Then you retain them. Then you identify the best ones. Then you grow them.

The meta-lesson will be the same as Block 2: selection bias. We'll see it everywhere in retention and growth analytics."

**If asked:** "Which analysis is most important?"
A: Depends on your business stage. Early stage: retention is critical — validate product-market fit. Growth stage: power user and expansion become important for scaling profitably. Mature: all of them, but failure analysis helps maintain quality.

**Transition:** "Let's start with retention analysis..."
-->

---

<!-- _class: lead -->

# Part 1: Retention Analysis
### *(22 minutes)*

---

## What is Retention Analysis?

**Measuring whether users come back after their first interaction.**

The fundamental question:

> Of the users who signed up on Day 0, what percentage are still active on Day N?

This tells you if your product has lasting value — or if people try it and leave.

<!--
INSTRUCTOR NOTE:

**Background:** Retention is often called "the silent killer" — companies can grow quickly with poor retention by pouring money into acquisition, but it's not sustainable. The D7 and D30 retention benchmarks vary dramatically by industry: gaming apps often have 20% D30, productivity apps 40%+, social apps in between.

**Key point:** Retention tells you if your product has lasting value.

**Say something like:**
"Retention analysis answers a simple but crucial question: do people come back?

Of the users who signed up on a given day — call it Day 0 — what percentage are still active on Day 7? Day 30? Day 90?

This is the single best indicator of whether your product has lasting value. If people try it and never return, it doesn't matter how many you acquire — you're filling a leaky bucket.

I like to think of retention as the truth-teller. Marketing can get people in the door. A clever onboarding flow can get them to complete signup. But if they don't come back the next week? The product didn't deliver value. Retention is the metric you can't fake."

**If asked:** "What's a good retention rate?"
A: It depends on the product category. Gaming apps: 20-30% D30 is solid. Productivity SaaS: 40%+ D30. Social apps: 30-40% D30. The trend matters as much as the absolute number — is it improving or declining?

**Transition:** "Let me show you why retention matters more than most people realize..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_03_retention_vs_acquisition.png)

---

## Why Retention Matters More Than Acquisition

**Acquisition is expensive. Retention compounds.**

- Improving acquisition 20% → 20% more users

- Improving retention 20% → 20% more users **every cohort, forever**

Small retention improvements have massive long-term impact.

<!--
INSTRUCTOR NOTE:

**Background:** This is one of the most important slides for students to internalize. Companies often over-invest in acquisition and under-invest in retention. The math is simple but powerful: acquisition improvements are additive (one-time gain), retention improvements are multiplicative (compound over every future cohort).

**Key point:** Retention improvements compound. Acquisition improvements don't.

**Say something like:**
"I want you to understand the math of retention vs. acquisition.

If you improve acquisition 20%, you get 20% more users this period. Great. But that's a one-time gain.

If you improve retention 20%, you get 20% more users retained from this cohort. And 20% more from next month's cohort. And 20% more from every cohort forever.

Retention compounds. Acquisition doesn't.

A 5 percentage point improvement in D30 retention might sound small. But apply it to every cohort over 3 years and you've potentially doubled your active user base compared to where you'd be otherwise.

This is why smart companies obsess about retention. It's not as glamorous as growth — nobody writes headlines about 'retention improved 3 percentage points' — but the long-term math is overwhelmingly in favor of retention investment."

**If asked:** "Then why do companies focus so much on acquisition?"
A: Several reasons. Acquisition is more visible. Executives can see ads running. Growth numbers look good in board decks. Retention is quiet — you're preventing something bad, not creating something visible. Also, many companies have short time horizons.

**Transition:** "Let me show you what data you need for retention analysis..."
-->

---

## The Data You Need

| Field | Example | Why |
|-------|---------|-----|
| `user_id` | `u_12345` | Track individual users |
| `signup_date` | `2026-01-01` | Define cohort (Day 0) |
| `activity_date` | `2026-01-08` | When they came back |
| `activity_type` | `app_open` | What counts as "active" |

**Critical decision:** What counts as "active"?
- App open? (low bar)

- Core action? (higher bar, more meaningful)

- Purchase? (highest bar)

<!--
INSTRUCTOR NOTE:

**Background:** The data structure for retention is straightforward, but the definition of "active" is the critical decision. Different definitions give wildly different retention rates. App open is easy to track but might not reflect value. Core action is harder to define but more meaningful. This decision should involve product and business stakeholders.

**Key point:** What counts as "active" is the critical decision. Get alignment from product and business stakeholders before running retention analysis.

**Say something like:**
"The data you need for retention is straightforward: user_id, signup_date, activity dates, and activity types.

But here's where the critical decision comes in: what counts as 'active'?

App open is the lowest bar. Did they open the app at all? Easy to track, but opening an app doesn't mean they got value. Maybe they opened it by accident. Maybe they opened it, saw nothing interesting, and left.

Core action is a higher bar. Did they complete the main thing your product is for? For Spotify, that might be 'played a song.' For Slack, 'sent a message.' For a food delivery app, 'placed an order.' This is harder to define but more meaningful.

Purchase is the highest bar. Only count users who paid. For subscription businesses, this might mean 'still subscribed.'

Here's the trap: different definitions give wildly different retention rates. The same product might show 40% D30 retention with 'app open' and 15% D30 retention with 'purchase.' Both are true. Neither is wrong. But they tell different stories.

Get alignment from product and business stakeholders before running retention analysis. Ask: 'What do we mean by active?' Document the definition. Use it consistently."

**If asked:** "Which definition should we use?"
A: Depends on what you're trying to understand. For product-market fit, core action is usually best. For revenue forecasting, purchase. For growth modeling, app open might be appropriate. The key is to be explicit and consistent.

**Transition:** "Once you've defined active, there are different ways to measure retention..."
-->

---

## Defining Retention: DN vs. Rolling

**DN retention** — Active on Day N specifically?
`Active Day N / Signups Day 0`

**Rolling D7** — Active at any point in days 1-7?
`Active any day 1-7 / Signups Day 0`

**Example:** 1,000 signups Jan 1 → 420 active Jan 8 → D7 = 42%

**DN is stricter.** Rolling is more forgiving. Be explicit.

<!--
INSTRUCTOR NOTE:

**Background:** DN (Day-N) and rolling retention measure different things. DN asks "were they active on exactly Day N?" while rolling asks "were they active at any point in the first N days?" DN is stricter and more volatile (depends on which day falls on a weekend). Rolling is more forgiving and smoother but may hide patterns.

**Key point:** DN is stricter than rolling. Know which you're using and be consistent.

**Say something like:**
"There are two ways to measure retention: DN and rolling. They measure different things.

DN retention asks: were they active on exactly Day N? D7 means: of the users who signed up on January 1st, what percentage were active on exactly January 8th — seven days later?

Rolling D7 asks: were they active at any point in days 1-7? This is more forgiving. If they were active on day 3 but not day 7, rolling counts them, DN doesn't.

Here's an example: 1,000 signups on January 1st. On January 8th — exactly Day 7 — 420 were active. D7 retention is 42%.

But what if 580 were active at some point during days 1-7? Rolling D7 would be 58%.

Same data, different definitions, different numbers.

DN is stricter and more volatile — it depends on what day of the week Day N falls on. If Day 7 is a Sunday and your product is work-related, D7 looks worse than it 'really' is.

Rolling is smoother but may hide patterns. A user who was active once and never again still counts as 'retained' under rolling.

The key is to pick one and be consistent. Document which definition you're using. Don't mix them."

**If asked:** "Which should I use for my capstone?"
A: DN is more common for quick comparisons. Rolling is better for understanding engagement over a period. Gaming often uses DN. SaaS often uses rolling or monthly active. Match industry norms if you can.

**Transition:** "Let me show you what this looks like visually..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_03_retention_curve.png)

---

## Reading the Retention Curve

**Shape matters:**
- **Steep early drop** = First-time experience problem

- **Continued decline** = No habit formation

- **Flattens** = Found product-market fit for those users

Where the curve flattens = your "true" retention rate.

<!--
INSTRUCTOR NOTE:

**Background:** The shape of the retention curve tells a story. Most products have steep early drops (Day 1-7) as users who signed up but never engaged disappear. The curve then either continues declining (product doesn't form habits) or flattens (users who made it past the early drop have found value). The "true" retention rate is where the curve stabilizes.

**Key point:** A steep early drop is normal. What matters is whether the curve eventually flattens.

**Say something like:**
"When you look at a retention curve, the shape tells you a story.

A steep early drop — say, 50% by Day 7 — sounds bad, but it's actually normal. Many people sign up and never really try the product. They downloaded the app and forgot. They created an account and got distracted. That's expected.

What you care about is what happens after. If the curve keeps declining — 50% at D7, 30% at D30, 15% at D60, trending toward zero — you don't have habit formation. Users try it, use it a bit, and gradually drift away. Your product doesn't become part of their routine.

If the curve flattens — 50% at D7, 35% at D30, 30% at D60, stable around 28% — you have something. Those 28% found enough value to keep coming back. That's your 'true' retention rate.

The place where the curve flattens tells you what percentage of users you're really retaining long-term. Everything before that is the 'sorting' period."

**If asked:** "When does the curve typically flatten?"
A: Varies by product. Consumer apps often see stabilization by D30-D60. Enterprise software might take months. Gaming can stabilize in days.

**Transition:** "You shouldn't just look at one cohort though..."
-->

---

## Cohort Analysis: Comparing Over Time

Don't just look at one cohort. Compare them:

| Cohort | D1 | D7 | D30 |
|--------|----|----|-----|
| Jan 2025 | 65% | 42% | 28% |
| Apr 2025 | 62% | 38% | 24% |
| Jul 2025 | 58% | 35% | 22% |
| Oct 2025 | 55% | 35% | ??? |

**Trend is down.** Something changed — product? Acquisition source? Competition?

Cohort analysis reveals trends that aggregate metrics hide.

<!--
INSTRUCTOR NOTE:

**Background:** Cohort analysis is the core technique for understanding retention trends. Aggregate retention metrics blend together different cohorts, hiding whether things are improving or declining. By separating cohorts and comparing them, you can spot trends early and investigate causes.

**Key point:** Don't look at aggregate retention. Compare cohorts over time to spot trends early.

**Say something like:**
"Never look at retention in aggregate. Aggregate retention blends together users who signed up years ago with users who signed up yesterday. It hides whether things are getting better or worse.

Cohort analysis separates users by when they signed up and tracks each cohort's retention separately.

Look at this table. January cohort: D30 retention was 28%. April cohort: 24%. July cohort: 22%. October cohort: we don't have D30 data yet, but the early indicators are concerning.

The trend is down. Each cohort is retaining worse than the last.

This is a red flag. Something changed. Maybe the product got worse. Maybe acquisition shifted to lower-quality sources — remember from Block 2, different channels have different LTV. Maybe competition intensified. Maybe it's seasonal.

You can't tell from this table what caused the decline. But you can tell THAT it's declining. That's the first step. Then you investigate: what changed between January and April? What changed again between April and July?

Cohort analysis is your early warning system. Without it, you might not notice the decline until aggregate metrics finally catch up — months or years later."

**If asked:** "How many cohorts should we compare?"
A: At least 4-6 to see meaningful trends. Monthly cohorts for products with high frequency. Quarterly for B2B or slower products. Weekly if you're doing rapid product changes.

**Transition:** "Once you see the trend, the next question is why..."
-->

---

## Retention Driver Analysis

Beyond "what is retention?" → **"what drives retention?"**

**Method:** Compare users who retained vs. churned. What's different?

| Behavior in First Week | Retained D30 | Churned D30 |
|-----------------------|--------------|-------------|
| Added ≥3 friends | 52% | 18% |
| Completed profile | 45% | 22% |
| Posted content | 48% | 15% |
| Only browsed | 12% | 68% |

**Insight:** Friend-adding is the strongest predictor.

<!--
INSTRUCTOR NOTE:

**Background:** Retention driver analysis compares users who retained against users who churned to find behavioral differences. This is useful for identifying what actions correlate with retention. However, this sets up the next slide's critical lesson: correlation isn't causation.

**Key point:** Driver analysis identifies behaviors that correlate with retention. The method is simple: compare what retained users did vs. what churned users did.

**Say something like:**
"Driver analysis asks a different question. Not 'what is retention?' but 'what DRIVES retention?'

The method is simple. Take two groups: users who retained (still active at D30) and users who churned (not active at D30). Look at what they did in their first week. Compare.

Look at this table. Among users who added 3 or more friends in week one, 52% retained. Among users who didn't add friends, only 18% retained. That's a huge gap.

Profile completion: 45% vs 22% retained. Content posting: 48% vs 15% retained. Only browsing: 12% vs 68% retained — wait, that's the other way. Users who only browsed were much more likely to churn.

The insight: friend-adding is the strongest predictor of retention.

This is valuable! It suggests that friend-adding might be an 'activation' behavior — something that unlocks the value of the product.

But here's where I want you to pause..."

**If asked:** "How do you pick which behaviors to analyze?"
A: Start with product intuition. What do you think the 'aha moment' is? Test that first. Then explore other behaviors in the first day, first week, first month. Look for big gaps between retained and churned.

**Transition:** "Because there's a trap here..."
-->

---

## The Driver Analysis Trap

**Correlation ≠ causation.**

Users who add 3+ friends retain better. But:
- Did friend-adding **cause** retention?

- Or do **naturally engaged users** both add friends AND retain?

If you force friend-adding on disengaged users, they might still churn.

**Always recommend A/B tests** before mandating changes based on driver analysis.

<!--
INSTRUCTOR NOTE:

**Background:** This is one of the most important cautions in the entire course. Every company does retention driver analysis and finds correlations like "users who do X retain better." The temptation is to force everyone to do X. This rarely works because it confuses correlation with causation. The Facebook "7 friends in 10 days" story is the canonical example — it's often misunderstood as "make everyone add 7 friends" when the insight was about identifying engaged users early.

**Key point:** Correlation is not causation. Recommend A/B tests before mandating changes.

**Say something like:**
"This slide is so important I want you to write it down. The driver analysis trap.

You do the analysis. You find that users who add 3+ friends in the first week retain at 2x the rate. The product team says: 'Great! Let's make everyone add 3 friends before they can use the app.'

Stop. Think about what you're assuming.

You're assuming that adding friends CAUSES retention. But what if engaged users — people who were always going to retain — naturally add friends because they're engaged? The adding didn't cause the engagement; they were both caused by underlying engagement.

If that's true, forcing friend-adding on disengaged users won't help. They'll add friends to get past the gate and then churn anyway. Or worse, they'll abandon during onboarding because you made it harder.

This is why your recommendation should always be: 'We found a correlation. We recommend an A/B test to establish causation before mandating the change.' That's what separates good analysts from dangerous ones."

**If asked:** "How do you run the A/B test?"
A: Test group gets prompted/encouraged to add friends but not forced. Control group gets normal experience. Measure D30 retention for both. If test retains better, there's likely a causal effect. If they're the same, the correlation was selection bias.

**Transition:** "Let me show you some common data quality issues to watch for..."
-->

---

## Common Retention Data Issues

**Inconsistent "active" definition** — Different teams use different events → metrics don't match

**Bot/fraud signups** — Unusual signup patterns → inflates D0, deflates retention

**Reactivation confusion** — Churned user returns after 90 days → is this D1 or new user?

**Platform differences** — iOS vs. Android tracking gaps → retention looks different

**Standardize your "active" event** across the company.

---

## The SnapGram Scenario

**Company:** SnapGram (photo sharing app)
**Problem:** D7 retention dropped from 42% to 35% over 6 months
**Stakes:** "Sugar diet growth" — high acquisition masking retention crisis

**Hypothesis:** Users who add ≥3 friends in first 48 hours retain at 2x the rate. Onboarding doesn't push friend-adding hard enough.

<!--
INSTRUCTOR NOTE:

**Background:** This scenario illustrates the driver analysis trap. "Sugar diet growth" refers to a company that looks healthy on total user counts but has declining retention — the acquisition sugar high masks the retention crisis. This is extremely common in VC-funded startups where growth at all costs is prioritized.

**Key point:** High acquisition can mask declining retention. This scenario sets up the lesson about correlation vs. causation in driver analysis.

**Say something like:**
"Let's apply what we've learned to a scenario.

SnapGram is a photo sharing app. D7 retention has dropped from 42% to 35% over six months. That's a significant decline — nearly 20% relative drop.

But here's the thing: their user count is still growing. Why? High acquisition is masking the retention problem. They're adding users faster than they're losing them — for now. This is what I call 'sugar diet growth.' It looks healthy, but it's not sustainable.

The analytics team did driver analysis. They found that users who add 3+ friends in the first 48 hours retain at 2x the rate. Their hypothesis: onboarding doesn't push friend-adding hard enough.

What do you think will happen if they act on this?"

**If asked:** "How do you detect 'sugar diet growth'?"
A: Compare cohort retention over time. If each new cohort retains worse than the last, you have a retention crisis even if total users are growing. The growth is buying time, but the underlying health is deteriorating.

**Transition:** "Before they act, let's think about counter-metrics..."
-->

---

## SnapGram: Counter-Metrics

**Signup completion** (Guardrail) — Aggressive onboarding increases abandonment

**Engagement depth** (Guardrail) — "Zombie retention" = they return but don't engage

**Notification opt-out** (Tradeoff) — Pushy re-engagement causes fatigue

<!--
INSTRUCTOR NOTE:

**Background:** This slide introduces the counter-metrics for retention optimization. The "zombie retention" concept is particularly important — users who return but don't engage are not valuable, but they inflate retention metrics. This connects to the "activity definition" discussion earlier.

**Key point:** Counter-metrics for retention optimization protect against gaming the metric without improving the user experience.

**Say something like:**
"Before SnapGram acts on the driver analysis, what could break?

Signup completion: If they make onboarding more aggressive — 'you must add 5 friends to continue' — some users will abandon. They came to try the app, not to invite friends. This is a guardrail. If signup completion drops more than X%, the intervention failed.

Engagement depth: This is 'zombie retention.' Users might return to the app — technically retained — but do nothing. They open, see nothing relevant, close. That's not real retention. That's gaming the metric. If engagement per session drops, you have zombies.

Notification opt-out: If they try to boost retention with notifications — 'your friend posted!' — users might opt out of notifications entirely. Or worse, uninstall. Pushy re-engagement has diminishing returns.

These counter-metrics force the team to think about second-order effects. 'Will this actually improve the experience, or just move numbers?'"

**If asked:** "How do you set thresholds for counter-metrics?"
A: Use historical variation as a baseline. If signup completion normally varies ±3%, a guardrail might be 'don't let it drop more than 5%.' There's no universal answer — it depends on how critical each metric is.

**Transition:** "Now let's see what happened..."
-->

---

## SnapGram: Pre-Mortem

> We found friend-adding was the #1 predictor. Product added a mandatory "add 5 friends" step.
>
> Signup completion dropped 30%.
>
> The correlation was selection bias — engaged users organically add friends, but forcing it didn't make disengaged users engaged.
>
> **Lesson:** Recommend A/B tests, not mandates. Correlation ≠ causation.

<!--
INSTRUCTOR NOTE:

**Background:** This pre-mortem illustrates the driver analysis trap in action. The 30% drop in signup completion is realistic — aggressive onboarding gates often cause similar drops. The key lesson is that the analyst should have recommended testing, not mandating. This is a professional responsibility issue, not just a technical one.

**Key point:** The analyst's job is to recommend testing hypotheses, not to present correlations as proven causation. This mistake happens constantly.

**Say something like:**
"Here's what went wrong.

The analytics team presented their finding: 'Friend-adding predicts retention at 2x.' Product heard: 'Make everyone add friends.' They added a mandatory step — add 5 friends before you can use the app.

Signup completion dropped 30%. For every 100 users who started signup before, now only 70 finish.

Why? The correlation was selection bias. Engaged users add friends because they're engaged. They want to share their photos with people they know. That's why they retained — they were engaged from the start.

Disengaged users don't have that motivation. They came to try the app, saw a wall of 'invite your friends,' and left.

The lesson for you as analysts: recommend A/B tests, not mandates. Your finding is: 'We observed a correlation. We recommend testing whether encouraging friend-adding improves retention before making it mandatory.' That's the professional way to present correlational analysis."

**If asked:** "What should the analyst have done differently?"
A: Recommend a test: Show friend-adding prompts to 50% of users, suppress for 50%. Measure retention for both. If prompted users retain better AND complete signup at similar rates, there's evidence the prompt helps. Then — and only then — consider mandating.

**Transition:** "Let's summarize the key takeaways from retention analysis..."
-->

---

## Retention Analysis: Key Takeaways

1. **Define "active" precisely** — same event across all analysis

2. **DN vs. rolling retention** — be explicit about which you're using

3. **Cohort comparisons reveal trends** — aggregates hide insights

4. **Driver analysis is correlational** — A/B test before mandating

5. **Counter-metrics matter** — don't break signup to fix D7

<!--
INSTRUCTOR NOTE:

**Background:** This summary slide reinforces the five key points from retention analysis. Point 4 (driver analysis is correlational) connects to the meta-lesson of Block 3 — selection bias.

**Key point:** End on the correlation/causation distinction. It's the most important takeaway and sets up the rest of Block 3.

**Say something like:**
"Let's recap retention analysis with these five takeaways.

First: define 'active' precisely. If different teams use different definitions, your metrics won't align. Pick one event and standardize.

Second: DN vs. rolling retention. Know which you're using and be explicit. They answer different questions.

Third: cohort comparisons. Never look at aggregate retention. Compare cohorts to spot trends early.

Fourth — and this is the most important: driver analysis is correlational. Just because users who add friends retain better doesn't mean adding friends causes retention. A/B test before mandating changes.

Fifth: counter-metrics. Don't break signup to fix D7. Think about what could go wrong.

Point four is the setup for the rest of today. We'll see the same correlation vs. causation trap in power users, expansion, and ecosystem analysis."

**Transition:** "Now let's move to Power User Analysis..."
-->

---

<!-- _class: lead -->

# Part 2: Power User Analysis
### *(13 minutes)*

---

## What is Power User Analysis?

**Understanding who your best users are and what they do differently.**

Most products have highly skewed engagement:

> A small percentage of users drive most of the value.

Power user analysis asks:
- How concentrated is engagement?

- Who are these users?

- What do they do differently?

- Should we optimize for them or broaden engagement?

<!--
INSTRUCTOR NOTE:

**Background:** Most products have highly skewed engagement — a small percentage of users drive a disproportionate share of value. This is the Pareto principle applied to user engagement. Power user analysis helps companies understand who these users are and decide whether to double down on them or try to create more of them.

**Key point:** Engagement is usually skewed. Understanding power users informs strategy.

**Say something like:**
"Most products have a dirty secret: a small percentage of users drive most of the value.

Think about any app you use. Some people check it 20 times a day. Most people open it once a week — if that. The daily users might be 10% of your base but 60% of your engagement.

Power user analysis asks four questions.

First: how concentrated is engagement? Is it 80/20? 90/10? 95/5?

Second: who are these power users? What do they have in common?

Third: what do they do differently? Features, behaviors, patterns?

Fourth — and this is the strategic question: should we optimize for power users, or try to create more of them?

This last question doesn't have a right answer. It's a strategy decision. Your job as an analyst is to provide the data that informs the decision."

**If asked:** "Shouldn't we always try to create more power users?"
A: Not necessarily. If your power users have fundamentally different needs or circumstances than casual users, trying to convert casual users may dilute the product for everyone. Sometimes serving power users better is the right call.

**Transition:** "Let me show you what data you need..."
-->

---

## The Data You Need

| Field | Example | Why |
|-------|---------|-----|
| `user_id` | `u_12345` | Identify individuals |
| `engagement_metric` | `viewing_hours` | What defines "power" |
| `time_period` | `Jan 2026` | Consistent measurement window |
| `user_attributes` | Tenure, source, demographics | Describe power users |
| `behaviors` | Features used, content consumed | What they do differently |

**Critical decision:** What metric defines "power"?
- Time spent? Actions taken? Revenue generated?

<!--
INSTRUCTOR NOTE:

**Background:** Like retention analysis, the critical decision is definitional. What makes someone a "power user"? Different metrics give different answers. Time spent might identify binge-watchers. Revenue might identify spenders. Actions might identify engaged users. Each definition leads to different strategic conclusions.

**Key point:** Define "power" carefully. Different metrics identify different user segments with different strategic implications.

**Say something like:**
"The data structure is similar to retention, but with engagement metrics added. User ID to identify individuals, time period for consistent measurement, attributes to describe users, and behaviors to understand what they do.

The critical decision is: what metric defines 'power'?

Time spent: identifies users who spend the most hours with your product. For a streaming service, these are binge-watchers.

Actions taken: identifies users who do the most things. For an e-commerce site, this might be searches, wishlist adds, reviews written.

Revenue generated: identifies users who spend the most money. For a subscription service with tiers, this is premium subscribers.

These might overlap, but they might not. A power user by time might be someone who falls asleep with the TV on. A power user by revenue might be a corporate account that barely uses the product but pays a lot.

The choice depends on what you're trying to understand. If you're optimizing for engagement, use time or actions. If you're optimizing for revenue, use revenue. Be explicit about your definition."

**If asked:** "Can we combine multiple metrics?"
A: Yes, you can create composite scores or use multiple definitions in parallel. But it gets complex. Start simple, with one definition, and expand if needed.

**Transition:** "Let me show you the pattern that almost always emerges..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_03_pareto_curve.png)

---

## The 80/20 Rule (Pareto)

Often, engagement follows a power law:
- Top 10% of users → 50%+ of engagement

- Top 20% of users → 80%+ of engagement

The exact numbers vary, but skew is almost universal.

<!--
INSTRUCTOR NOTE:

**Background:** The Pareto principle (80/20 rule) originated with economist Vilfredo Pareto's observation that 80% of Italy's land was owned by 20% of the population. It appears across many domains: wealth distribution, software bugs, customer value. In digital products, engagement skew is often even more extreme than 80/20.

**Key point:** Engagement skew is nearly universal in digital products. Understanding the degree of skew is the first step in power user analysis.

**Say something like:**
"This is the Pareto principle, or 80/20 rule. In many digital products, engagement is highly skewed — a small percentage of users drive the majority of activity.

The exact numbers vary by product. Gaming might be more extreme — top 5% driving 70% of play time. B2B SaaS might be more distributed.

The key insight is: you almost certainly have this pattern. The question is how extreme it is and what to do about it.

Some companies celebrate their power users. Others worry about over-dependence on a small group. Both perspectives are valid."

**If asked:** "Is extreme skew good or bad?"
A: Neither inherently. It depends on your business model. Subscription services want some skew (power users are retained) but not too much (revenue shouldn't depend on a tiny group). Advertising models often want high skew because heavy users see more ads. The goal is to understand your skew, not necessarily change it.

**Transition:** "Let me show you how to measure concentration precisely..."
-->

---

## Calculating Concentration

**Gini coefficient** or simple percentile analysis:

| User Percentile | % of Total Viewing Hours |
|-----------------|-------------------------|
| Top 1% | 15% |
| Top 5% | 35% |
| Top 10% | 52% |
| Top 20% | 72% |
| Bottom 50% | 8% |

**High concentration** = Small group matters a lot
**Low concentration** = Engagement is distributed

<!--
INSTRUCTOR NOTE:

**Background:** Gini coefficient is borrowed from economics (income inequality measurement). Range is 0 to 1: 0 means perfect equality (everyone uses equally), 1 means perfect concentration (one user does everything). For most products, Gini falls between 0.4 and 0.8. Percentile tables are often more intuitive for stakeholders than the Gini number itself.

**Key point:** Measuring concentration quantifies your skew. The percentile table is the clearest output for stakeholder communication.

**Say something like:**
"There are two ways to measure concentration. The Gini coefficient gives you a single number — higher means more concentrated. But I find percentile tables more useful for communication.

Look at this example: top 10% of users drive 52% of viewing hours. That's meaningful concentration. Bottom 50% contribute only 8%. That tells a story.

When you present this to stakeholders, the percentile table sparks conversation. 'Should we worry that half our users barely use the product?' 'Is our top 1% at risk of churning?'

These are strategic questions. Your job is to surface them with clear data."

**If asked:** "What's a 'normal' Gini for digital products?"
A: Typically 0.5-0.7 for consumer products. Gaming and social media tend higher (0.6-0.8). B2B SaaS tends lower (0.4-0.6) because enterprise users have more consistent usage patterns. There's no 'right' answer — it depends on your product and business model.

**Transition:** "Once you've quantified concentration, the next step is profiling who your power users are..."
-->

---

## Power User Behavioral Profile

Once you identify power users, describe them:

| Dimension | Power Users | Casual |
|-----------|------------|--------|
| Tenure | 18 mo avg | 4 mo |
| Sessions/week | 12 | 2 |
| Features used | 8 of 10 | 2 of 10 |
| Content type | Series | Movies |
| Time of day | Evening | Weekend |

**Insight:** Power users have formed a habit. Casual users haven't.

---

## Path to Power: How Users Become Power Users

Track user journeys over time:

| Months Active | % Became Power User |
|--------------|---------------------|
| 1 | 2% |
| 3 | 8% |
| 6 | 15% |
| 12 | 22% |

**Questions:** What triggers the transition? Can we accelerate it?

---

## The Strategic Question

**Two options:**

1. **Optimize for power users**

   - They drive most engagement

   - High retention, high value

   - Risk: Alienate casual users

2. **Broaden engagement**

   - More users become power users

   - Larger addressable base

   - Risk: Dilute product for core users

**This is a strategy decision, not an analytics one.** Your job is to inform it.

<!--
INSTRUCTOR NOTE:

**Background:** This is one of the most important strategic decisions a product team can make, and it's a recurring tension in most companies. Amazon famously optimizes for everyone (low prices, fast shipping). Apple historically optimized for power users (professional tools). Netflix tries to serve both with personalization. There's no universally right answer.

**Key point:** Power user analysis culminates in a strategic fork. Analysts provide the data to inform this decision; they don't make it.

**Say something like:**
"This is the strategic fork that power user analysis leads to. Do you double down on your best customers, or try to broaden the base?

Option 1: Optimize for power users. Build features they want, prioritize their retention, accept that casual users might churn. This is the 'serve your best customers' strategy.

Option 2: Broaden engagement. Make the product more accessible, lower barriers, try to convert casuals into power users. This is the 'grow the pie' strategy.

Both have risks. Optimizing for power users can create a product that's intimidating to newcomers. Broadening can dilute the product for people who love it.

Here's the key insight: this is a strategy decision, not an analytics one. Your job as an analyst is to present clear data on who your power users are, how concentrated engagement is, and what the path to power looks like. Leadership decides which direction to go."

**If asked:** "Can you do both?"
A: Companies try, usually through personalization or product tiers. But there are real tradeoffs. Engineering resources spent on power user features aren't spent on onboarding. It's tempting to say 'both' but that often means 'neither well.'

**Transition:** "Let's see how this plays out in the Streamflix scenario..."
-->

---

## The Streamflix Scenario

**Company:** Streamflix (streaming service, 45M subscribers)
**Problem:** Engagement is highly skewed. Small % drives most viewing.
**Question:** Optimize for power users or broaden engagement?

**Hypothesis:** Top 10% of users account for >50% of viewing hours and have distinct content preferences we're not explicitly designing for.

<!--
INSTRUCTOR NOTE:

**Background:** This scenario illustrates the power user strategic fork. Streamflix faces a common situation: a small group drives most engagement. The strategic question — optimize for them or broaden — has real consequences. Netflix famously tried to serve everyone; HBO traditionally served a more curated, power-user audience.

**Key point:** This scenario forces the strategic question: do you optimize for your best users or try to grow the middle?

**Say something like:**
"Streamflix is a streaming service with 45 million subscribers. They've done the concentration analysis and found their top 10% drive over 50% of viewing hours.

These power users have distinct preferences — they watch long-form series, they watch in the evenings, they finish what they start.

The strategic question: should Streamflix optimize for these users? Build features for binge-watchers — 'skip intro,' autoplay, viewing marathons? Or should they try to turn casual users into power users — better discovery, easier onboarding, more accessible content?

This is the fork. And there's no objectively right answer. It depends on Streamflix's strategy.

The analyst's job is to present the data clearly: here's how concentrated engagement is, here's who the power users are, here's what they do. Leadership decides which direction to go."

**If asked:** "What would you recommend?"
A: It depends on more context. If growth is the priority, broaden. If retention and engagement are the priority, deepen. Both are valid strategies. The analyst's job is to illuminate the tradeoff, not make the call.

**Transition:** "But before Streamflix decides, what could break?"
-->

---

## Streamflix: Counter-Metrics

**Casual user satisfaction** (Guardrail) — Power user features may confuse casual users

**Content diversity** (Tradeoff) — Optimizing for power users may narrow content

**New user activation** (Guardrail) — Power user UX may overwhelm newcomers

<!--
INSTRUCTOR NOTE:

**Background:** These counter-metrics apply specifically to the "optimize for power users" strategy. If Streamflix goes the other direction (broaden engagement), they'd need different counter-metrics (power user satisfaction, engagement depth). The counter-metrics depend on which direction you're moving.

**Key point:** Counter-metrics for power user optimization focus on protecting the casual majority who might be alienated.

**Say something like:**
"If Streamflix decides to optimize for power users, what could break?

Casual user satisfaction: Power user features might confuse casual users. If the homepage is optimized for binge-watchers with complex 'continue watching' logic, a casual user who watches one movie a month might feel lost. This is a guardrail — track casual user satisfaction separately.

Content diversity: This is a tradeoff metric. If the algorithm optimizes for what power users watch — long series, specific genres — content diversity might narrow. New shows outside that mold don't get promoted. Content creators get frustrated. The catalog becomes less diverse.

New user activation: Power user UX can overwhelm newcomers. If everything assumes you've watched 50 shows and have a profile, a brand-new user sees a confusing wall of recommendations. First-session experience suffers.

Note that these counter-metrics are specific to the 'optimize for power users' strategy. If they went the other direction, they'd track different things."

**If asked:** "How do you measure 'casual user satisfaction'?"
A: Segment your satisfaction surveys or NPS by engagement level. Track it separately for power users vs. casual users. If the gap widens after a power user optimization, you're alienating casuals.

**Transition:** "Now here's what went wrong..."
-->

---

## Streamflix: Pre-Mortem

> We redesigned homepage for power users (binge-watchers). Casual users saw engagement drop 20%, churn increased. We optimized for power users at the expense of everyone else.

**Lesson:** Serve both segments. Present a balanced strategy.

<!--
INSTRUCTOR NOTE:

**Background:** This pre-mortem illustrates the danger of choosing one segment and ignoring the other. The 20% engagement drop among casuals is realistic — UI changes that make sense for experts often confuse newcomers and casual users. The lesson connects to the "can you do both?" question from earlier.

**Key point:** The pre-mortem lesson is balance. Extreme optimization for one segment often damages the other.

**Say something like:**
"Here's the pre-mortem failure.

Streamflix analyzed their power users. They redesigned the homepage for binge-watchers — personalized queues, quick resume, series-focused recommendations.

Power users loved it. Their engagement went up.

But casual users — 60% of the subscriber base — saw engagement drop 20%. The new homepage was confusing. 'Why is it showing me episode 7 of a show I watched once? Where are the movies?'

Churn increased among casuals. And here's the thing: casual users might not watch much, but they still pay the subscription. Losing them hits revenue directly.

The lesson: serve both segments. This doesn't mean ignore power users. It means design with segments in mind. Maybe power users see one homepage, casual users see another. Maybe there's a 'simplified view' option.

The analyst's role is to present a balanced strategy: 'Here's what power users want, here's the risk to casuals, here's how we might serve both.' Not just 'optimize for power users.'"

**If asked:** "How do you serve both segments?"
A: Personalization. Different users see different experiences based on their usage patterns. Power users get power features surfaced; casual users get simpler, more approachable interfaces. A/B test segment-specific experiences.

**Transition:** "Let's summarize the key takeaways from power user analysis..."
-->

---

## Power User Analysis: Key Takeaways

1. **Engagement is usually skewed** — measure how much

2. **Define "power" with a clear metric** — time, actions, or revenue

3. **Profile power users behaviorally** — what do they do differently?

4. **Counter-metric: casual user health** — don't alienate the majority

5. **This informs strategy** — analysts provide data, leadership decides

<!--
INSTRUCTOR NOTE:

**Background:** This summary reinforces the five key points from power user analysis. Point 5 is crucial — the analyst's role is to provide clear data, not to make the strategic decision. That's leadership's job.

**Key point:** Power user analysis informs strategy but doesn't dictate it. Present the data clearly and let leadership decide.

**Say something like:**
"Five takeaways from power user analysis.

First: engagement is usually skewed. Most products have a Pareto distribution. Measure how skewed yours is.

Second: define 'power' explicitly. Time spent, actions taken, revenue generated — these identify different users. Be clear about your definition.

Third: profile behaviorally. What do power users do that casual users don't? This reveals potential paths to power.

Fourth: counter-metric is casual user health. Power user optimization can alienate casuals. Track both segments.

Fifth — and this is the professional practice point: this informs strategy, it doesn't make it. Your job as an analyst is to present clear data on concentration, profiles, and tradeoffs. Leadership decides whether to optimize for power users or broaden engagement. That's a business decision, not an analytical one."

**Transition:** "We have a mini-case exercise next to synthesize retention and power user concepts..."
-->

---

<!-- _class: lead -->

# Mini-Case Exercise: Retention
### *(10 minutes)*

---

## Mini-Case: SocialApp Retention Drop

> **Situation:** SocialApp's D7 retention dropped from 42% to 34% after a major UI redesign.
>
> **Additional data:**
> - Power users (top 10%) seem unaffected — their D7 is still 68%
> - Casual users (bottom 50%) dropped from 28% to 18%
> - The new UI emphasizes "stories" over the feed

**Think (2 min):** What does this pattern tell you? Which foundational analysis would you use first?

---

## Mini-Case: Discussion

**Questions to consider:**

1. Why might power users be unaffected while casual users suffer?

2. Is this a Retention Analysis problem or a Power User Analysis problem?

3. What counter-metric should have been tracked during the redesign?

4. What's your hypothesis for the root cause?

<!--
INSTRUCTOR NOTE:

**Background:** This mini-case synthesizes retention and power user analysis concepts. The pattern — power users unaffected while casual users suffer — is common in redesigns. It often indicates that the redesign optimized for the most vocal users (power users) while ignoring the silent majority (casual users).

**Key point:** Segment-level analysis reveals what aggregate metrics hide. A product change that looks neutral in aggregate might be hurting one segment and helping another.

**Say something like:**
"Cold call time. I'm going to call on 2-3 people. Take a moment to think about the data.

[Cold call student 1]: Why might power users be unaffected while casual users suffer?

Looking for: Power users have formed habits. They know where things are, they've customized their experience, they're invested. A UI change is an inconvenience, but they'll adapt. Casual users haven't formed those habits. They were still figuring out the product. A UI change resets their learning curve. They give up.

[Cold call student 2]: Is this a Retention Analysis problem or a Power User Analysis problem?

Looking for: It's both. Retention analysis identified the problem — D7 dropped. Power User analysis revealed the PATTERN — it's segment-specific. You need both.

[Cold call student 3]: What counter-metric should have been tracked during the redesign?

Looking for: Casual user engagement. Feature adoption by segment. First-session completion for new users. Any metric that tracks whether the change works for ALL users, not just the vocal power users.

Hypothesis: Stories are a power user feature. Power users love creating and viewing stories — it's more engagement for them. Casual users wanted simple scrolling through a feed. The redesign prioritized stories, pushing casual users out."

**If asked:** "How do you prevent this in redesigns?"
A: Segment every metric. Don't just track overall retention — track retention by engagement level. Set guardrails for casual users specifically. A/B test with segment-level success criteria, not just aggregate.

**Transition:** "Great discussion. Let's take a stretch break before we move to Failure Analysis..."
-->

---

<!-- _class: lead -->

## ☕ Stretch Break
### 5 minutes

Stand up. Walk around. The last 30 minutes cover Failure and Expansion analyses.

---

<!-- _class: lead -->

# Part 3: Failure Analysis
### *(13 minutes)*

---

## What is Failure Analysis?

**Systematically investigating why something isn't working.**

Different from other analyses:
- **Funnel analysis** tells you *where* users drop off

- **Failure analysis** tells you *why*

Often **exploratory** — you don't have a hypothesis yet. You're categorizing problems.

<!--
INSTRUCTOR NOTE:

**Background:** Failure analysis is different from other analyses because it's explicitly exploratory. You don't start with a hypothesis — you start with a symptom ("searches are failing") and build a taxonomy of causes. This is qualitative work disguised as quantitative analysis. The manual sampling step is crucial and often skipped by analysts who want to stay in SQL.

**Key point:** Failure analysis is exploratory. You're categorizing problems, not testing hypotheses.

**Say something like:**
"Failure analysis is different from everything else we've covered. It's explicitly exploratory.

Here's the difference. Funnel analysis tells you WHERE users drop off — 40% abandon at the payment step. But it doesn't tell you WHY. Is the page slow? Confusing form? Missing payment method? You don't know.

Failure analysis answers the 'why' question. And here's the key: you usually don't have a hypothesis when you start. You have a symptom — searches are returning zero results, support tickets are spiking, error rates are up. Your job is to categorize the failures and size each category.

This is qualitative work. You can't stay in SQL for this. You have to look at actual examples — actual search queries that failed, actual error messages, actual support tickets. And then you build a taxonomy: 'These failures are spelling errors. These are inventory gaps. These are junk queries.' That taxonomy is the analytical output."

**If asked:** "Can't we automate this with machine learning?"
A: Eventually, maybe. But you need the taxonomy first. And ML classification is only as good as its training labels — which means a human had to categorize examples first. Start manual, automate later.

**Transition:** "Here's when you'd use failure analysis..."
-->

---

## When to Use Failure Analysis

| Symptom | Failure Analysis Approach |
|---------|--------------------------|
| Zero search results | Sample queries, categorize why they failed |
| High error rates | Sample errors, identify root causes |
| Support tickets | Categorize complaints, size each category |
| Abandonment | Review session recordings, identify patterns |

**Common thread:** Something is broken, but you don't know the mix of causes.

<!--
INSTRUCTOR NOTE:

**Background:** Students often ask "when would I use this?" This table gives concrete examples. The key pattern is: you have a symptom (something's failing) but you don't know the distribution of causes. You might suspect spelling errors cause zero-results, but is it 10% or 80%? Failure analysis answers that question.

**Key point:** Use failure analysis when you have a symptom but don't know the mix of underlying causes.

**Say something like:**
"Here are the classic use cases for failure analysis.

Zero-result searches: You know 12% of searches return nothing. But why? Is it spelling? Inventory gaps? Bad data? You don't know until you look.

Error rates: Your checkout has a 3% error rate. Is that mostly payment declines? Address validation? System bugs? Each requires a different fix.

Support tickets: Volume is up 30%. What are people complaining about? You need to categorize before you can prioritize.

Session recordings: Users abandon at step 3. What are they struggling with? Watch actual sessions and build a taxonomy.

The common thread is: something is broken, you have a number that says it's broken, but you don't know the MIX of causes. And the mix matters — if 80% of failures are spelling errors, that's where you invest. If failures are evenly split across ten causes, you need a different strategy."

**If asked:** "How is this different from root cause analysis?"
A: Root cause analysis typically focuses on a single incident — "why did the server go down?" Failure analysis is about categorizing a population of failures — "what types of failures are we seeing, and how common is each type?" They're related but different scopes.

**Transition:** "Let me walk you through the method..."
-->

---

## The Method: Manual Sampling

**Step 1:** Pull a random sample (100-500 instances of failure)

**Step 2:** Manually review and categorize each one

**Step 3:** Develop a taxonomy (3-7 categories)

**Step 4:** Validate taxonomy at scale (can you apply it programmatically?)

**Step 5:** Size each category (volume and impact)

This is qualitative-first, quantitative-second.

<!--
INSTRUCTOR NOTE:

**Background:** This is where many analysts struggle. They want to stay in SQL and skip the manual work. But you can't build a good taxonomy without looking at actual examples. The sample size (100-500) is a balance: enough to see the major categories, small enough to review manually. 3-7 categories is a practical limit — fewer than 3 means you're not discriminating, more than 7 becomes unwieldy.

**Key point:** The manual sampling step is non-negotiable. You have to look at actual failures before you can categorize them.

**Say something like:**
"This is the five-step method. Let me walk through each step.

Step 1: Pull a random sample. 100-500 instances is the sweet spot. Less than 100, you might miss rare categories. More than 500, you're wasting time — you'll see the same patterns over and over.

Step 2: Manually review each one. This is the part analysts want to skip. 'Can't I just cluster them with ML?' No. Not yet. You need to understand what you're looking at. Read the search queries. Watch the session recordings. Read the error logs.

Step 3: Develop a taxonomy. As you review, patterns emerge. 'This is a spelling error. This is an inventory gap. This is a junk query.' Build categories. Aim for 3-7 — fewer than 3 means you're not discriminating, more than 7 becomes hard to manage.

Step 4: Validate. Can you apply these categories programmatically? If 'spelling error' is a category, can you build a rule that detects spelling errors? If not, refine the taxonomy.

Step 5: Size each category. Once you have clean categories, measure volume and impact. This is where you finally get quantitative.

The key insight: this is qualitative-first, quantitative-second. You have to understand the failures before you can count them."

**If asked:** "What if I don't have time for 200+ manual reviews?"
A: Start with 50. You'll see the major categories quickly. Then validate with another 50. It's still better than guessing.

**Transition:** "Let me show you what this looks like with a concrete example..."
-->

---

## Example: Zero-Results Search

Sample 200 zero-result queries. Manually categorize:

| Category | Example | Count | % |
|----------|---------|-------|---|
| **Spelling error** | "ipone case" | 86 | 43% |
| **Synonym gap** | "sneakers" (we index "trainers") | 42 | 21% |
| **Inventory gap** | "vintage camera" (we don't sell) | 34 | 17% |
| **Junk/nonsense** | "asdfgh" | 24 | 12% |
| **Ambiguous** | "gift" (too broad) | 14 | 7% |

**Insight:** 43% is spelling. That's a clear priority.

<!--
INSTRUCTOR NOTE:

**Background:** This is a real example from e-commerce search analysis. The numbers are typical — spelling errors are usually the largest category (30-50%), followed by synonym/vocabulary gaps. The "junk/nonsense" category is important because it sets expectations: not all failures are fixable. Some users type gibberish or test the search.

**Key point:** The taxonomy table is the key deliverable of failure analysis. It shows what's broken and how much of each category exists.

**Say something like:**
"Here's what the output looks like. This is a real analysis pattern from e-commerce search.

We sampled 200 zero-result queries. Manually reviewed each one. Built five categories.

Spelling errors: 43%. People type 'ipone case' instead of 'iPhone case.' Fixable with spell-correction.

Synonym gaps: 21%. We index 'trainers,' user searches 'sneakers.' Same product, different words. Fixable with synonym mapping.

Inventory gaps: 17%. User searches 'vintage camera.' We don't sell it. Not fixable without expanding inventory.

Junk: 12%. 'asdfgh.' Random keyboard mashing. Bots. Tests. Not fixable and probably not worth trying.

Ambiguous: 7%. 'gift.' Too broad. Could show everything or nothing. Partially fixable with better handling.

Now look at the insight: 43% is spelling. That's a clear priority. If you can fix spelling errors, you eliminate nearly half of zero-result searches. That's a high-impact recommendation.

This table is the deliverable. When you present failure analysis to stakeholders, this is what you show."

**If asked:** "What if categories overlap? What if 'ipone case' is both a spelling error AND could be a synonym gap?"
A: Categories should be mutually exclusive. Pick the primary cause. In this case, it's a spelling error first — the word is misspelled. Force yourself to pick one.

**Transition:** "But volume isn't everything. Let me show you how to size by impact..."
-->

---

## Opportunity Sizing

Not all failures are equal. Size by impact:

| Category | % | Value | Opportunity |
|----------|---|-------|-------------|
| Spelling | 43% | $50 | $5.4M/yr |
| Synonym | 21% | $75 | $3.9M/yr |
| Inventory | 17% | $120 | $5.1M/yr |
| Junk | 12% | $0 | $0 |

**Insight:** Spelling is highest volume, but inventory has high-value queries.

<!--
INSTRUCTOR NOTE:

**Background:** This is where failure analysis connects to business impact. Volume alone is misleading — a category can be 43% of failures but only 20% of value. The "Value" column represents average expected revenue per query (if successfully converted). Inventory gaps often have high value because they're specific, high-intent queries.

**Key point:** Size failures by impact (revenue, cost), not just volume. This changes prioritization decisions.

**Say something like:**
"Here's where failure analysis gets strategic. We have the taxonomy. Now we need to size by IMPACT, not just volume.

Look at this table. Spelling is 43% of failures — highest volume. But the average value of a spelling-error query is $50. Maybe these are common items, low-priced goods.

Inventory gaps are only 17% of failures. But the average value is $120. People searching for 'vintage camera' or specific brand names — these are high-intent, high-value queries.

When you multiply volume times value, the picture shifts. Spelling is $5.4M opportunity. Inventory is $5.1M. Nearly tied. If you only looked at volume, you'd say 'fix spelling first.' But impact says 'both matter equally.'

And look at junk — 12% of volume but $0 opportunity. Don't waste engineering resources on junk queries. Some failures aren't worth fixing.

This is the analysis that drives roadmap decisions. Engineering asks 'what should we build?' You answer with a prioritized table based on impact, not volume."

**If asked:** "How do you estimate the 'Value' column?"
A: It varies. For e-commerce, you can use average order value by product category. For SaaS, you might use conversion probability times contract value. The key is having some estimate — even rough — rather than treating all failures as equal.

**Transition:** "One more piece before we're done with the method: validation..."
-->

---

## Validation: Inter-Rater Reliability

Manual classification is subjective. Validate it:

**Method:** Have 2 people independently classify the same 50 samples.

| Agreement Level | Interpretation |
|-----------------|----------------|
| >80% | Taxonomy is clear, can proceed |
| 60-80% | Refine category definitions |
| <60% | Taxonomy is too subjective, rethink |

If classifiers disagree, the categories aren't crisp enough.

<!--
INSTRUCTOR NOTE:

**Background:** Inter-rater reliability is a concept from qualitative research. It's how you validate that your categories are objective enough to be useful. If two people can't agree on how to classify examples, then the categories are too fuzzy. The 80% threshold is standard in qualitative research — it means your taxonomy is operational.

**Key point:** Validate your taxonomy before trusting it. Inter-rater reliability ensures your categories are crisp enough to be actionable.

**Say something like:**
"Here's the quality control step that most analysts skip. And skipping it is a mistake.

You've built a taxonomy. You've classified 200 examples. But it's all been YOU doing the classification. How do you know your categories are clear? Maybe 'synonym gap' and 'inventory gap' are obvious to you, but confusing to someone else.

The validation method: take 50 samples. Have someone else classify them independently. Don't show them your answers. Then compare.

If you agree on 80% or more, your taxonomy is clear. Proceed with confidence.

If you agree 60-80%, there's ambiguity. Go back and tighten the category definitions. What distinguishes 'synonym gap' from 'inventory gap'? Write clearer rules.

If you agree less than 60%, your taxonomy is too subjective. You're essentially guessing. Step back and rethink.

This matters because the whole point of failure analysis is to guide decisions. If your categories are fuzzy, your recommendations will be fuzzy. 'Fix spelling errors' is actionable. 'Fix stuff that seems related to spelling but also maybe synonyms' is not."

**If asked:** "What if I'm the only analyst? No one else to compare with?"
A: Ask a product manager or engineer to classify 30 samples. They don't need to be an analyst — they just need to understand the categories. If they can't apply your taxonomy, it's not clear enough.

**Transition:** "Let's see how this plays out in the FindIt scenario..."
-->

---

## The FindIt Scenario

**Company:** FindIt (e-commerce search engine)
**Problem:** 12% of searches return zero results (up from 9%)
**Stakes:** Each percentage point = ~$2M lost GMV

**Framing:** This is **exploratory**. We don't know why searches fail. Goal is to categorize and size before picking a solution.

<!--
INSTRUCTOR NOTE:

**Background:** FindIt represents a classic failure analysis use case: search engines with zero-result problems. The $2M per percentage point sizing is realistic for large e-commerce platforms. Note the explicit framing: this is exploratory. Unlike driver analysis where you start with a hypothesis, failure analysis starts with a symptom.

**Key point:** This scenario explicitly frames failure analysis as exploratory. The goal is to categorize and size before choosing solutions.

**Say something like:**
"FindIt is an e-commerce search engine. Their zero-result rate has crept up from 9% to 12%. Each percentage point is about $2 million in lost GMV — users who search, find nothing, and leave.

The framing here is critical: this is EXPLORATORY. We don't know why searches fail. Maybe it's spelling. Maybe it's inventory gaps. Maybe it's a bug. We're not testing a hypothesis; we're building a taxonomy.

The goal of failure analysis is to categorize the failures and size each category. Only then do you pick solutions.

This is different from driver analysis where you start with 'we think friend-adding drives retention.' Here you start with 'searches are failing and we don't know why.'"

**If asked:** "How do you size the opportunity at $2M per percentage point?"
A: Calculate: total searches per year × zero-result rate × conversion rate × average order value. If you get 100M searches and 12% zero-result at $20 AOV with 10% conversion, that's $240M lost. Each percentage point is about $2M.

**Transition:** "Before we fix anything, what counter-metrics should we track?"
-->

---

## FindIt: Counter-Metrics

| Counter-metric | Type | Why it could break |
|----------------|------|-------------------|
| **Search relevance** | Guardrail | Returning bad results is worse than no results |
| **Query latency** | Guardrail | Complex spelling logic may slow search |
| **Inventory trust** | Tradeoff | Showing "similar" items may frustrate users |

**Key insight:** Aggressive spell-correction can break things. "Febreeze" → "Freeze" is wrong.

<!--
INSTRUCTOR NOTE:

**Background:** These counter-metrics are specific to search fixes. The "relevance vs. zero results" tradeoff is particularly important: returning irrelevant results can be worse than returning nothing because it wastes user time and damages trust. The Febreeze → Freeze example illustrates over-aggressive spell-correction.

**Key point:** Fixing failures can create new problems. Returning bad results is worse than returning no results.

**Say something like:**
"Before we fix anything, let's think about what could break.

Search relevance: This is the most important counter-metric. Returning BAD results is worse than returning NO results. Why? Because zero results give a clear signal — 'we don't have that.' Bad results waste user time. They click, see irrelevant products, bounce. Trust in the search degrades.

Query latency: Complex spelling correction algorithms take time. If you add a neural net spell-checker, queries might slow from 100ms to 500ms. Users notice. If zero-results drop by 3% but latency increases by 300%, you might have made things worse.

Inventory trust: If you start showing 'similar' items when exact matches don't exist, users might lose trust. They searched for a specific brand, you showed a competitor. That's frustrating.

The example at the bottom: someone searches 'Febreeze' — that's a brand name. Aggressive spell-correction might 'fix' it to 'Freeze' and show... ice products? That's worse than nothing."

**If asked:** "How do you balance reducing zero-results vs. maintaining relevance?"
A: Test carefully. Track clicks and conversions, not just zero-result rate. If you reduce zero-results by showing results, but those results don't convert, you haven't helped users — you've just moved a metric.

**Transition:** "Now let's see what happened..."
-->

---

## FindIt: Pre-Mortem

> We found spelling errors were 45% of failures and recommended a spelling correction system.
>
> Engineering built it, but the speller was too aggressive — it "corrected" valid brand names and niche terms. Search relevance dropped 15%.
>
> **Lesson:** Exploratory work was valuable, but we skipped validation. Test edge cases before launch.

<!--
INSTRUCTOR NOTE:

**Background:** This pre-mortem illustrates a common failure mode: the analysis was good (correctly identified spelling as the biggest category), but the solution was implemented without adequate testing. Over-aggressive spell-correction is a real problem — brand names, technical terms, and niche products often look like spelling errors to automated systems.

**Key point:** Good analysis can still lead to bad outcomes if implementation isn't validated. Test edge cases before full launch.

**Say something like:**
"Here's what went wrong.

The failure analysis was solid. They sampled queries, built a taxonomy, found spelling errors were 45% of failures. Good work.

They recommended a spelling correction system. Engineering built it. Makes sense.

But the speller was too aggressive. It 'corrected' valid brand names — 'Febreeze' becomes 'Freeze.' It 'corrected' niche terms — 'sourdough' becomes 'sour dough.' It 'corrected' product codes that looked like typos.

Search relevance dropped 15%. Users were now getting results — but wrong results. Trust in search declined.

The lesson: the exploratory analysis was valuable. The taxonomy was right. But they skipped validation. A spell-checker needs edge case testing: brand names, product codes, technical terms, foreign words. Before full launch, A/B test with a subset. Measure relevance, not just zero-result rate.

Good analysis plus bad implementation equals bad outcome."

**If asked:** "How do you test spell-correction safely?"
A: Build a whitelist of valid brand names and product terms. A/B test with a small percentage of traffic. Track relevance metrics, not just zero-result rate. Move slowly.

**Transition:** "Let's summarize failure analysis..."
-->

---

## Failure Analysis: Key Takeaways

1. **Start with manual sampling** — you need to see the failures

2. **Build a taxonomy** — 3-7 categories, mutually exclusive

3. **Validate with inter-rater reliability** — if classifiers disagree, refine

4. **Size by impact, not just volume** — small category can have big $$$

5. **This is exploratory** — you're building hypotheses, not testing them

6. **Counter-metrics prevent over-correction** — fixing one thing can break another

<!--
INSTRUCTOR NOTE:

**Background:** This summary has six takeaways because failure analysis has more distinct methodological steps than other analyses. Point 5 is key — failure analysis is explicitly exploratory, which distinguishes it from driver analysis where you start with a hypothesis.

**Key point:** Failure analysis is qualitative-first, quantitative-second. You have to look at actual failures before you can count them.

**Say something like:**
"Six takeaways for failure analysis.

First: start with manual sampling. There's no shortcut. You have to look at actual failures — read the search queries, watch the session recordings, read the error logs.

Second: build a taxonomy. 3-7 categories that are mutually exclusive. If you can't decide which category a failure belongs to, your taxonomy isn't crisp enough.

Third: validate with inter-rater reliability. Have someone else classify the same samples. If you don't agree at least 80%, refine your categories.

Fourth: size by impact, not just volume. A small category can have big dollar value. Don't assume the biggest category is the biggest opportunity.

Fifth — and this distinguishes failure analysis from everything else today: this is exploratory. You're building hypotheses, not testing them. You don't start with 'we think it's spelling errors.' You start with 'searches are failing and we don't know why.'

Sixth: counter-metrics prevent over-correction. Fixing zero-results might break relevance. Always think about what could go wrong with your solution."

**Transition:** "Let's move on to Expansion Analysis..."
-->

---

<!-- _class: lead -->

# Part 4: Expansion & Monetization Analysis
### *(13 minutes)*

---

## What is Expansion Analysis?

**Understanding how customers grow their relationship with you.**

Questions:
- Why do free users upgrade to paid?

- Why do basic subscribers upgrade to premium?

- What triggers expansion (more seats, higher tier)?

This is about **extracting more value from existing customers** — often cheaper than acquisition.

<!--
INSTRUCTOR NOTE:

**Background:** Expansion analysis is where retention and monetization intersect. It's often called "land and expand" in SaaS — you land a customer (acquisition) then expand their value over time. This is the fifth analysis in Block 3 and connects directly to CAC/LTV from Block 2: expansion revenue is a key driver of LTV, and it's typically much cheaper than acquiring new customers.

**Key point:** Expansion revenue from existing customers is usually cheaper than acquiring new customers. Understanding what triggers upgrades is a core analytical question.

**Say something like:**
"We've covered retention — keeping customers. Now we move to expansion — growing customer value.

The questions are different. Retention asks: 'Why do customers stay or leave?' Expansion asks: 'Why do customers pay more?'

In freemium products: Why do free users upgrade to paid?
In tiered products: Why do basic subscribers upgrade to premium?
In B2B: Why do companies add more seats or move to enterprise tier?

This matters because expansion revenue is usually cheaper than acquisition. If you already have a customer using your product, converting them to a higher tier has low acquisition cost — they already know you. The marketing spend is minimal. The sales cycle is short.

So 'expand existing customers' is often a better investment than 'acquire new customers.' Understanding what triggers expansion is a core analytical capability."

**If asked:** "How does this relate to CAC/LTV from Block 2?"
A: Expansion directly drives LTV. A customer who upgrades has higher lifetime value than one who doesn't. And expansion revenue has lower acquisition cost (often near zero), which improves the CAC/LTV ratio dramatically.

**Transition:** "Let's look at the freemium model as a lens for expansion..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_03_freemium_funnel.png)

---

## The Freemium Model

**Freemium math:**
- Free users: Large base, low/no revenue

- Paid users: Smaller base, meaningful revenue

- Premium: Smallest base, highest revenue

**The question:** What makes someone convert?

---

## The Data You Need

| Field | Example | Why |
|-------|---------|-----|
| `user_id` | `u_12345` | Track individual journeys |
| `subscription_status` | `free`, `basic`, `premium` | Current state |
| `status_change_date` | `2026-01-15` | When they upgraded |
| `usage_metrics` | Storage used, features used | What might trigger upgrade |
| `limit_hit_events` | `storage_limit_reached` | Friction points |

<!--
INSTRUCTOR NOTE:

**Background:** Expansion analysis requires tracking user state over time AND the events that might trigger state changes. The key addition here is `limit_hit_events` — tracking when users encounter limits is crucial for understanding conversion triggers. Many companies don't log these events, which makes expansion analysis much harder.

**Key point:** Log limit events and upgrade triggers. This data is often missing and difficult to backfill.

**Say something like:**
"The data structure for expansion analysis is similar to retention, but with a crucial addition.

User ID and subscription status are obvious — you need to know who has which tier.

Status change date tells you WHEN someone upgraded. This lets you do cohort analysis of upgrades.

Usage metrics — storage used, features used, sessions, actions — these are the behaviors that MIGHT trigger upgrades.

And here's the key addition: limit_hit_events. When did someone hit the storage limit? When did they try to invite a fourth team member and get blocked? When did they see the 'upgrade to unlock' modal?

This is the data that tells you what triggered the upgrade consideration. And many companies don't log it well. They know someone upgraded on January 15th, but they don't know that they hit the storage limit on January 12th and saw the upgrade prompt three times.

If you're designing a data pipeline: log limit events. Log upgrade prompt views. This data is essential for expansion analysis and hard to backfill."

**If asked:** "What if we don't have limit_hit_events logged?"
A: You can sometimes reconstruct them from usage metrics — if someone's storage was 4.9GB on Monday and 5.1GB on Tuesday, they probably hit the 5GB limit. But it's imperfect. Advocate for proper event logging going forward.

**Transition:** "With this data, we can do conversion driver analysis..."
-->

---

## Conversion Driver Analysis

Compare users who upgraded vs. stayed free:

| Behavior (Week Before Upgrade) | Upgraded | Stayed Free |
|-------------------------------|----------|-------------|
| Hit storage limit | 78% | 12% |
| Used premium feature (trial) | 65% | 8% |
| Invited team member | 45% | 5% |
| Heavy daily usage | 52% | 15% |

**Insight:** Hitting limits and trying premium features are strong triggers.

<!--
INSTRUCTOR NOTE:

**Background:** This is the same driver analysis pattern from retention, now applied to conversion. Compare those who converted vs. those who didn't. Look at behaviors in the period before conversion. The table shows classic patterns: limits and feature trials are strong triggers. Heavy usage alone is weaker — you can be a heavy user without needing to pay.

**Key point:** Limits and feature trials are usually the strongest conversion triggers. Heavy usage alone doesn't trigger upgrades — need + discovery does.

**Say something like:**
"This is the driver analysis pattern we saw in retention, now applied to conversion.

We compare two groups: users who upgraded last month vs. users who stayed free. What did they do in the week before upgrading?

Look at these numbers.

78% of upgraders hit the storage limit the week before. Only 12% of non-upgraders did. That's a 6x difference. Storage limits are a powerful trigger.

65% of upgraders used a premium feature during a trial. Only 8% of non-upgraders did. They tried it, liked it, paid for it.

45% of upgraders invited a team member. Only 5% of non-upgraders. Collaboration drives conversion.

Heavy daily usage: 52% vs 15%. Still a gap, but smaller. Heavy usage alone isn't enough — you can be a power user on the free tier forever.

The insight: limits and feature trials are the strongest triggers. This tells you where to focus. If you want more conversions, help users discover premium features. If limits are the biggest trigger, analyze whether limits are set correctly."

**If asked:** "But couldn't heavy users just be ABOUT to hit limits?"
A: Maybe. That's why multivariate analysis helps — you can control for usage level and still see that hitting a limit has an independent effect. The raw comparison is a starting point, not the final answer.

**Transition:** "Let's dig deeper into limits..."
-->

---

## Limit Analysis: The Conversion Trigger

Many freemium products use **limits** to drive conversion:

| Limit Type | % Who Hit It | Conversion Rate If Hit |
|-----------|--------------|------------------------|
| Storage (5GB) | 15% | 35% |
| Team members (3) | 8% | 52% |
| Projects (10) | 12% | 28% |
| API calls | 3% | 65% |

**Insight:** Few users hit limits, but those who do convert at high rates.

**Question:** Should we lower limits to force more conversions?

<!--
INSTRUCTOR NOTE:

**Background:** This table is the heart of limit analysis. Notice the tension: limits with highest conversion rates (API calls at 65%, team members at 52%) have the lowest hit rates. Limits with highest hit rates (storage at 15%) have lower conversion rates. This reflects a fundamental tension — aggressive limits feel punitive, so fewer people hit them, but those who do really need to upgrade.

**Key point:** High conversion rates on limits can be misleading. The question isn't just "who converts when hitting a limit" but "how many users hit the limit at all?"

**Say something like:**
"This table is the key output of limit analysis. Let me walk through it.

We track four types of limits. For each, we ask: what percentage of users ever hit this limit? And if they hit it, what's their conversion rate?

Storage limit: 15% of users hit it. Of those, 35% convert. That's 15% × 35% = 5.25% of all users converting due to storage limits.

Team members: Only 8% hit it, but 52% of those convert. That's 4.16% of all users.

API calls: Only 3% hit it, but 65% convert. That's 1.95% of all users.

See the pattern? Limits with highest conversion rates have lowest hit rates. Why? Because aggressive limits feel punitive. If only 3% of users hit the API limit, it's probably a high limit that only power users encounter. They really need it, so they convert.

This raises the tempting question at the bottom: should we lower limits? If we lower the storage limit from 5GB to 2GB, more users will hit it. More will convert. Right?

Maybe. But that's where the trap is. Let's discuss..."

**If asked:** "How do you calculate the overall impact?"
A: Hit rate × conversion rate = percentage of users who convert due to that limit. Then multiply by user base size to get absolute numbers. Storage contributes most conversions overall (5.25% of all users) even though its conversion rate is lower.

**Transition:** "The question is: should we lower limits? This leads to a dilemma..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_03_limit_tradeoff.png)

---

## The Limit Dilemma

Lowering limits increases conversion, but:

- **Too high:** Few hit the limit, low conversion

- **Too low:** Users feel nickeled-and-dimed, churn

**Finding the sweet spot requires experimentation.**

<!--
INSTRUCTOR NOTE:

**Background:** The limit dilemma is central to freemium strategy. Limits are the most powerful conversion lever — when users hit a limit, conversion rates spike. But limits that are too aggressive damage user trust and drive free users away. This is a classic tradeoff with no universal right answer.

**Key point:** Limits convert, but aggressive limits damage trust. Finding the right balance requires experimentation.

**Say something like:**
"This is the central tension in freemium: the limit dilemma.

Limits are incredibly powerful for conversion. When someone hits a storage limit or project limit, their conversion rate might be 10x higher than someone who hasn't hit a limit. They have an immediate need.

So there's a temptation: lower the limits. Make people hit them earlier. Convert more users.

But here's the problem. If limits feel too aggressive, users feel nickeled-and-dimed. They came for a 'free product' and immediately hit a paywall. They churn — often angrily, with bad reviews.

If limits are too generous, almost nobody hits them. You have millions of free users happily using your product forever, never converting.

The sweet spot is somewhere in the middle: limits that let users get genuine value from the free tier, encounter the limit naturally as they grow, and feel that paying is worth it.

Finding that sweet spot requires experimentation. There's no formula. You have to test different limits and measure both conversion AND free user retention."

**If asked:** "How do you test limit changes safely?"
A: Gradually and with holdbacks. Lower the limit for 10% of new users first. Measure conversion and churn for that cohort. If both metrics improve (or conversion goes up without killing churn), expand.

**Transition:** "Let's look at a real scenario..."
-->

---

## The NoteSpace Scenario

**Company:** NoteSpace (productivity SaaS)
**Problem:** 2M free users, 180K paid (9% conversion)
**Question:** Where should Product invest to drive upgrades — limits, feature discovery, or targeting?

**Hypothesis:** Users who hit the 5GB storage limit convert at 3x, but only 15% ever hit it.

<!--
INSTRUCTOR NOTE:

**Background:** NoteSpace represents a classic freemium SaaS company with a conversion rate optimization problem. 9% conversion is decent for freemium (typical is 2-5% for B2C, 5-15% for B2B). The question — limits vs. feature discovery vs. targeting — presents three strategic options for improving conversion.

**Key point:** This scenario presents three strategic options for improving freemium conversion. Each has different tradeoffs and risks.

**Say something like:**
"NoteSpace is a productivity SaaS with a freemium model. 2 million free users, 180,000 paying — that's a 9% conversion rate.

They want to improve conversion. They're considering three approaches:

Option 1: Limits. Lower the storage limit from 5GB to 3GB. More users hit it, more convert.

Option 2: Feature discovery. Better expose premium features to free users. Trial periods, in-app prompts, feature highlights.

Option 3: Targeting. Identify 'high-value' free users and target them specifically with upgrade prompts.

The hypothesis focuses on limits: users who hit the 5GB limit convert at 3x the rate of those who don't. But only 15% ever hit it. The temptation is: lower the limit, more people hit it, more conversions.

What do you think the risks are?"

**If asked:** "Which option is best?"
A: Depends on the product and users. Limits are powerful but risky. Feature discovery is gentler but slower. Targeting sounds smart but has selection bias risks. The right answer is probably 'test all three carefully.'

**Transition:** "Let's think about what could break..."
-->

---

## NoteSpace: Counter-Metrics

| Counter-metric | Type | Why it could break |
|----------------|------|-------------------|
| **Free user retention** | Guardrail | Aggressive prompts drive free users away |
| **Upgrade satisfaction** | Guardrail | Premature upgrades → regret → churn |
| **Brand perception** | Tradeoff | "Pushy" monetization damages trust |

<!--
INSTRUCTOR NOTE:

**Background:** These counter-metrics apply to all three conversion strategies (limits, discovery, targeting). The "upgrade satisfaction" metric is particularly important — users who convert before they're ready often churn quickly, making the conversion worthless. Premature conversions waste LTV.

**Key point:** Conversion is only valuable if the converted user retains. Premature upgrades hurt more than they help.

**Say something like:**
"Before NoteSpace acts on any strategy, what could break?

Free user retention: This is the big one. If you're too aggressive — lower limits, constant prompts, targeted messages — free users leave. They might not convert, but they're your top-of-funnel. They recommend the product. Some will convert later. Driving them away destroys future value.

Upgrade satisfaction: This is subtle. If someone converts before they're ready — maybe you pushed them hard — they might regret it. 'Why am I paying for features I don't use?' They churn within a month. The conversion was worthless. Worse, they feel tricked.

Brand perception: 'Pushy monetization' is how users describe products that constantly ask for upgrades. It damages trust and word-of-mouth. Some products are known for this — users warn each other to avoid them.

The insight: conversion is only valuable if the converted user retains and is happy. Gaming conversion at the expense of these counter-metrics backfires."

**If asked:** "How do you measure upgrade satisfaction?"
A: Survey new paid users at 30 days. 'Are you getting value from your subscription?' Or track paid user churn rate by cohort — if conversion rate goes up but paid churn also goes up, you're converting the wrong users.

**Transition:** "Now here's what went wrong..."
-->

---

## NoteSpace: Pre-Mortem

> We identified "high-value" free users (heavy usage, hit limits, tried premium features) and aggressively targeted them with upgrade prompts.
>
> Conversion increased 40%, but free user DAU dropped 25% as annoyed users left.
>
> Many "high-value" users were power free users who loved the free tier — they felt betrayed, not persuaded.
>
> **Lesson:** Looking valuable ≠ ready to convert. Use holdout tests. Monitor free retention as a hard guardrail.

<!--
INSTRUCTOR NOTE:

**Background:** This pre-mortem illustrates the selection bias trap in targeting. "High-value" free users — heavy usage, hitting limits, trying premium features — sound like great conversion targets. But many are power FREE users who chose the free tier deliberately. They're valuable to the ecosystem but not conversion candidates. Targeting them aggressively backfires.

**Key point:** High engagement doesn't mean conversion readiness. Power free users are a real segment that adds value (network effects, word-of-mouth) without converting.

**Say something like:**
"Here's the pre-mortem failure.

NoteSpace chose the targeting approach. They identified 'high-value' free users: heavy usage, hit limits, tried premium features. These users look like conversion candidates. Let's target them.

They sent aggressive upgrade prompts to this segment. Pop-ups. Emails. In-app notifications.

Conversion increased 40%. Success!

But free user DAU dropped 25%. The high-value free users — the ones they targeted — left. Not upgraded. Left.

Why? Selection bias again. These users were high-value, but they weren't conversion-ready. Many were power FREE users — people who love the product, use it heavily, but chose the free tier deliberately. Maybe they're price-sensitive. Maybe they're students. Maybe they're just principled about not paying for software.

These users add value: they generate content, they invite friends, they recommend the product. But they're not going to convert. Targeting them with aggressive prompts felt like betrayal. 'I'm your best free user and you're harassing me to pay?'

The lesson: looking valuable ≠ ready to convert. Use holdout tests. If you target 10% of 'high-value' users with prompts and 90% without, you can measure whether the prompts actually increase conversion OR just annoy people."

**If asked:** "How do you identify conversion-ready users vs. power free users?"
A: Look at behavior patterns. Users who've almost hit limits and expressed frustration (support tickets, feature requests) might be conversion-ready. Users who've optimized their workflow to stay under limits are power free users. But honestly, the best approach is holdout testing — let behavior reveal intent.

**Transition:** "Let's summarize expansion analysis..."
-->

---

## Expansion Analysis: Key Takeaways

1. **Conversion drivers are behavioral** — what triggers the upgrade moment?

2. **Limits are powerful but dangerous** — too aggressive alienates users

3. **Targeting requires validation** — holdout tests before aggressive prompts

4. **Counter-metric: free user health** — don't kill the funnel to boost conversion

5. **Selection bias is real** — engaged users ≠ incremental conversions

<!--
INSTRUCTOR NOTE:

**Background:** This summary reinforces five key points from expansion analysis. Point 5 connects back to the Block 3 meta-lesson — selection bias. "Engaged users ≠ incremental conversions" means that identifying engaged free users doesn't mean they're ready to convert.

**Key point:** Conversion optimization has the same selection bias trap as retention driver analysis. High-engagement free users may be power free users, not conversion candidates.

**Say something like:**
"Five takeaways from expansion analysis.

First: conversion drivers are behavioral. Understand what triggers the upgrade moment — hitting limits, discovering premium features, inviting teammates. These are the levers.

Second: limits are powerful but dangerous. They work, but too aggressive limits damage trust and drive free users away.

Third: targeting requires validation. Holdout tests before aggressive prompts. Don't assume that 'high-value' free users want to be sold to.

Fourth: counter-metric is free user health. Free users are your top-of-funnel. Driving them away damages future conversion potential. Don't kill the funnel to boost this month's conversions.

Fifth — and this connects to everything today: selection bias is real. Engaged users don't equal incremental conversions. A power free user looks valuable but may never convert. Targeting them based on engagement metrics is a trap.

This is the same pattern we saw in retention driver analysis. Correlation-based targeting without causal validation fails."

**Transition:** "Now let's move to Ecosystem Analysis — how products interact..."
-->

---

<!-- _class: lead -->

# Part 5: Ecosystem Analysis
### *(12 minutes)*

---

## What is Ecosystem Analysis?

**Understanding how multiple products or features interact.**

Questions:
- Do our products complement each other (1+1=3)?

- Or cannibalize each other (1+1=1.5)?

- Should we invest in cross-product features?

Relevant for: Multi-product companies, platform businesses, feature suites.

<!--
INSTRUCTOR NOTE:

**Background:** As companies grow, they often launch multiple products or features. The strategic question is whether these complement each other (using one increases value of another) or cannibalize each other (using one reduces need for another). This analysis is particularly relevant for platform businesses, multi-product companies, and feature-rich applications.

**Key point:** Products/features can complement (1+1=3) or cannibalize (1+1=1.5). Understanding which is crucial for strategy.

**Say something like:**
"Ecosystem analysis becomes important as companies grow and launch multiple products.

The core question: when users adopt multiple products, is the total value greater than the sum of parts — or less?

Complements: Think Slack and Google Drive. Using one makes the other more valuable. Integrations deepen engagement. 1+1=3.

Substitutes: Think iMessage and WhatsApp. Using one reduces need for the other. They compete for the same use case. 1+1=1.5.

If your products are complements, you want to encourage multi-product adoption — build bridges, promote cross-selling, reward multi-product users.

If your products are substitutes, you might be cannibalizing yourself. New product success comes at the expense of the old product. That might be okay strategically, but you need to know it's happening.

The analysis tells you which scenario you're in — and the strategy depends on the answer."

**If asked:** "How do I know if products are complements or substitutes?"
A: Look at user behavior. If users of Product A have higher engagement with Product B than non-users of A, they might be complements. If users of A rarely use B, they might be substitutes. But beware of selection bias — test causally.

**Transition:** "Let me define complements and substitutes more precisely..."
-->

---

## Complements vs. Substitutes

| Relationship | Definition | Example |
|-------------|------------|---------|
| **Complement** | Using A increases value of B | Slack + Google Drive |
| **Substitute** | Using A reduces need for B | iMessage vs. WhatsApp |
| **Independent** | No relationship | Spotify + banking app |

**Multi-product companies want complements.** Substitutes mean internal competition.

<!--
INSTRUCTOR NOTE:

**Background:** These terms come from economics — complement goods and substitute goods. In digital products, understanding the relationship between products in your portfolio determines whether cross-product investment is valuable. Complements benefit from integration; substitutes compete for the same use case. Sometimes the relationship is unexpected or changes over time.

**Key point:** The complement/substitute distinction determines your cross-product strategy. Complements = invest in bridges. Substitutes = manage cannibalization.

**Say something like:**
"Let me define these terms precisely.

Complements: Using Product A increases the value of Product B. Classic example: Slack and Google Drive. The more you use Slack for communication, the more valuable Drive integration becomes for sharing files. They enhance each other.

Substitutes: Using Product A reduces your need for Product B. Classic example: iMessage and WhatsApp. They serve the same purpose — messaging. If you're heavily using one, you probably don't need the other.

Independent: No relationship. Spotify and your banking app. They don't affect each other at all.

The strategic implication: Multi-product companies want complements. If your products are complements, invest in integration — shared logins, data sharing, cross-product workflows. Every product strengthens the others.

If your products are substitutes, you're competing with yourself. New product growth might come at the expense of old products. That can be strategic — maybe you want to transition users — but you need to know it's happening."

**If asked:** "Can products be both complements and substitutes?"
A: Yes, for different user segments. A professional might use both Photoshop and Lightroom as complements (different tasks). A hobbyist might see them as substitutes (both edit photos). This is why you segment the analysis.

**Transition:** "The challenge is that simply observing multi-product usage doesn't tell you if products are complements. Let me show you why..."
-->

---

## The Selection Bias Problem

You observe: Users of both Product A and B retain 40% better than single-product users.

**But:** Is that because:
1. Using both products **causes** higher retention? (Complement)

2. Highly engaged users **naturally** use more products? (Selection bias)

If it's selection bias, pushing cross-product adoption won't help — and may annoy users.

<!--
INSTRUCTOR NOTE:

**Background:** This is the same selection bias problem we discussed in retention driver analysis, applied to ecosystem analysis. Multi-product users often look better on every metric — but that's often because engaged users naturally adopt more products, not because multi-product adoption causes engagement. This mistake leads to expensive "cross-product" investments that don't work.

**Key point:** Multi-product correlation almost always has selection bias. Engaged users do everything.

**Say something like:**
"This is the same trap we saw in retention driver analysis, applied to ecosystem analysis.

You look at the data. Users who use both Product A and Product B retain 40% better than single-product users. The product team says: 'Great! Let's invest in cross-product features to get more people using both!'

Stop. Same question as before. Is it that using both products CAUSES higher retention? Or is it that highly engaged users — the people who would have retained anyway — naturally explore and adopt more products?

If it's the second — and it usually is — pushing cross-product adoption on single-product users won't help. You're not creating engagement. You're just annoying people who were perfectly happy with one product.

This is why you can't just observe correlations. You need to test causally. Did the INTERVENTION of promoting cross-product adoption increase retention? Or did you just select for already-engaged users?"

**If asked:** "How can you tell the difference?"
A: A/B test. Show cross-product prompts to a treatment group, suppress them for a control group. Measure retention for both. If treatment retains better, there's a causal effect. If not, it was selection bias.

**Transition:** "Let me show you some methods to untangle this..."
-->

---

## Methods to Untangle Causation

| Method | How It Works | Strength |
|--------|-------------|----------|
| **Propensity matching** | Compare multi-product users to similar single-product users | Controls for observables |
| **Natural experiments** | When one product has outage, does the other suffer? | Reveals dependence |
| **Holdout tests** | Suppress cross-product prompts in some markets | Gold standard |

**Key insight:** Observational analysis alone cannot establish causation.

<!--
INSTRUCTOR NOTE:

**Background:** This table introduces three causal inference methods, building on what students learned in Block 2. Propensity matching is observational. Natural experiments leverage random variation (like outages). Holdout tests are true experiments. Each has tradeoffs, but the key insight is that correlation alone isn't enough — you need causal identification.

**Key point:** Three methods to get at causation in ecosystem analysis. Holdout tests are gold standard, but natural experiments can be powerful when available.

**Say something like:**
"These are three methods to move beyond correlation in ecosystem analysis.

Propensity matching: Find single-product users who LOOK like multi-product users — same tenure, same engagement, same demographics. Compare their retention. If matched single-product users retain worse than multi-product users, you have some evidence of complementarity. Weakness: only controls for what you can observe.

Natural experiments: This is clever. When Product A has an outage, what happens to Product B usage? If they're complements, Product B usage should drop — people use them together. If they're substitutes, Product B usage might spike — people switch over. Outages are random, so this reveals true dependence.

Holdout tests: Suppress cross-product promotions for a random subset of users. If promoted users have higher multi-product adoption AND higher retention, you've demonstrated causation. This is the gold standard but requires planning.

The key insight at the bottom: observational analysis alone cannot establish causation. You saw this in Block 2 with campaign effectiveness. Same principle applies here. You need one of these methods to claim that cross-product usage CAUSES better outcomes."

**If asked:** "What if we can't run holdout tests?"
A: Natural experiments are underutilized. Every outage, every feature rollout, every market-specific launch is a potential natural experiment. Look for variation you can exploit.

**Transition:** "Let's see how this plays out with SocialSuite..."
-->

---

## The SocialSuite Scenario

**Company:** SocialSuite (FriendFeed, QuickChat, PicShare)
**Problem:** Products are siloed. Each PM optimizes their own metrics.
**Question:** Are products complements? Should we invest in "bridges"?

**Hypothesis:** Multi-product users retain 30% better, and cross-product features will increase stickiness.

<!--
INSTRUCTOR NOTE:

**Background:** SocialSuite represents a multi-product company facing a classic platform question: should we integrate or keep products separate? The three products (FriendFeed, QuickChat, PicShare) could be complements or substitutes — we don't know without analysis. The hypothesis sounds compelling but is exactly the kind of correlation that invites selection bias.

**Key point:** This scenario sets up the ecosystem analysis trap: observing that multi-product users retain better, but not knowing if that's causation or selection.

**Say something like:**
"SocialSuite has three products: FriendFeed for social updates, QuickChat for messaging, PicShare for photos.

Each product has its own PM, its own metrics, its own roadmap. They're siloed. The question from leadership: should we integrate them? Build bridges between products? Shared identity, cross-product features, unified experience?

The analytics team did the analysis. Multi-product users — people who use two or three products — retain 30% better than single-product users. The hypothesis: cross-product features will increase stickiness.

But wait. What's the question we should ask?

Is the 30% better retention CAUSED by multi-product usage? Or are engaged users just more likely to adopt multiple products?

This is the ecosystem analysis trap. The correlation is real. The causation is unclear."

**If asked:** "How common is this situation?"
A: Very common. Almost every multi-product company I've seen has done this analysis and found multi-product users retain better. The question is whether investing in cross-product features actually helps or whether you're just observing engaged users being engaged.

**Transition:** "Let's see what the counter-metrics are and what went wrong..."
-->

---

## SocialSuite: Counter-Metrics & Pre-Mortem

**Counter-metrics:**
- Individual product focus (dilution risk)

- User overwhelm (too many cross-promos)

- Cannibalization (one product grows at another's expense)

**Pre-mortem:** We found 40% better retention for multi-product users and invested heavily in cross-product features. But it was selection bias — engaged users adopt everything naturally. Cross-product prompts annoyed single-product users, and FriendFeed DAU dropped 10%.

<!--
INSTRUCTOR NOTE:

**Background:** This combined slide shows both counter-metrics and pre-mortem for efficiency. The pre-mortem illustrates the selection bias trap in ecosystem analysis — the most common failure mode. The 40% better retention for multi-product users is realistic, as is the FriendFeed DAU drop when cross-product prompts annoyed single-product users.

**Key point:** The pre-mortem crystallizes the Block 3 meta-lesson: correlation-based investment decisions fail when selection bias is present.

**Say something like:**
"Let's look at what could break and what did break.

Counter-metrics first:

Individual product focus: If engineering is building bridges between products, they're not improving individual products. Each product might stagnate. This is dilution risk.

User overwhelm: Cross-product promotions — 'Hey, have you tried QuickChat?' — can be annoying. Users came for one product. Constant prompts for other products feel like spam.

Cannibalization: What if the products ARE substitutes? Pushing users from FriendFeed to QuickChat might help QuickChat but hurt FriendFeed. Net effect might be zero.

Now the pre-mortem:

They observed 40% better retention for multi-product users. They invested heavily in cross-product features. Shared login, cross-posting, 'discover our other apps' prompts.

What happened? It was selection bias. Engaged users naturally adopt multiple products — they were always going to retain. The cross-product investment didn't CREATE engagement; it just measured it.

Worse, the cross-product prompts annoyed single-product users — people who were happy with just FriendFeed. They saw constant 'try QuickChat' messages and got frustrated. FriendFeed DAU dropped 10%.

The investment backfired. They didn't test causation before committing resources."

**If asked:** "How should they have tested this?"
A: Holdout test. Suppress cross-product prompts for 20% of users. If prompted users retain better AND adopt more products, there's a causal effect. If not, the correlation was selection bias. Test before investing millions in integration.

**Transition:** "Let's summarize ecosystem analysis..."
-->

---

## Ecosystem Analysis: Key Takeaways

1. **Multi-product correlation ≠ causation** — selection bias is likely

2. **Use natural experiments** — outages reveal true dependence

3. **Holdout test before investing** — don't assume cross-product features help

4. **Watch for cannibalization** — products may compete internally

5. **This informs platform strategy** — big investment decisions

<!--
INSTRUCTOR NOTE:

**Background:** This summary concludes the five analyses in Block 3. Point 1 restates the Block 3 meta-lesson one more time: multi-product correlation doesn't mean causation. Engaged users adopt multiple products because they're engaged, not because multi-product usage causes engagement.

**Key point:** Ecosystem analysis completes the selection bias story. The same trap appears again — multi-product users look better, but that's correlation, not causation.

**Say something like:**
"Five takeaways from ecosystem analysis.

First — and you've heard this before: multi-product correlation doesn't equal causation. Multi-product users retain better, but that's probably because engaged users use everything, not because using multiple products causes engagement.

Second: natural experiments are underutilized. When one product has an outage, watch what happens to the other. This reveals true dependence without needing a designed experiment.

Third: holdout test before investing. Cross-product features sound strategic, but test first. Suppress cross-product prompts for a subset and see if it matters.

Fourth: watch for cannibalization. Your products might be substitutes, not complements. One product's growth might come at another's expense.

Fifth: this informs platform strategy. Multi-product investment decisions are big decisions. Get the analysis right before committing resources.

That's ecosystem analysis. It shares the selection bias lesson with retention, power users, and expansion. Let's wrap up Block 3 with the common thread."

**Transition:** "Let's summarize what we learned today..."
-->

---

<!-- _class: lead -->

# Day 1 Summary & Wrap-up
### *(8 minutes)*

---

## The Retention & Growth Analyses

| Analysis | Question | Pitfall |
|----------|----------|---------|
| **Retention** | Do they come back? | Zombie retention |
| **Power User** | Who matters most? | Alienating casual users |
| **Failure** | What's broken? | Over-aggressive fixes |
| **Expansion** | How do they grow? | Annoying free users |
| **Ecosystem** | Products complement? | Selection bias |

---

## Common Thread: Selection Bias

**Multiple analyses today shared this trap:**

- Retention drivers: Engaged users do everything

- Power users: They were always going to be power users

- Expansion: High-propensity users would convert anyway

**Solution:** A/B test before major investments. Correlation ≠ causation.

<!--
INSTRUCTOR NOTE:

**Background:** This is the meta-lesson for Block 3, just as "interaction effects" was for Block 2. Selection bias is the single most common mistake in retention and growth analytics. It's related to the causal inference problem we introduced in Block 2, but here we're seeing it specifically in user-level analysis.

**Key point:** Selection bias causes most analytics failures in retention and growth work. Always ask: "Are we finding causation, or just selecting for engaged users?"

**Say something like:**
"I want you to notice a pattern that ran through every analysis we covered today.

Retention drivers: Users who add friends retain better. But maybe engaged users both add friends AND retain — selection bias.

Power users: Multi-product users have higher LTV. But maybe engaged users naturally adopt more products — selection bias.

Expansion: Users who hit limits convert. But maybe power users hit limits AND would have converted anyway — selection bias.

Do you see the pattern? In every case, we're observing a correlation and tempted to assume causation. But there's a hidden variable: underlying user engagement.

Here's the rule: whenever you find a behavioral correlation in user data, ask yourself: 'Would an A/B test validate this?' If you're not sure, recommend the test before the investment. The difference between correlation and causation can be millions of dollars of wasted effort.

Block 2's lesson was 'things interact.' Block 3's lesson is 'correlation isn't causation.' Both are the same underlying problem — observational data lies to you in predictable ways."

**If asked:** "Is there ever a case where we don't need to A/B test?"
A: If the intervention is cheap and reversible, sometimes you just try it. But for major investments — redesigns, forced onboarding changes, budget reallocation — always test.

**Transition:** "That wraps up Day 1..."
-->

---

## Day 1 Complete

You now know:
- **The Analytics Project Brief framework** (10 sections)

- **Counter-metrics and adversarial thinking**

- **9 foundational analyses** (4 acquisition + 5 retention/growth)

**Day 2:** Stakeholders & Influence, then Application & Capstone Preparation.

---

<!-- _class: lead -->
<!-- _paginate: false -->

# See you Monday!

**Day 2 starts at 10:50**

- Block 4: Application & Practice

- Block 5: Stakeholders & Influence

**Before then:** Review the Brief template. Questions: rubiae@ceu.edu
