---
marp: true
theme: default
paginate: true
header: 'ECBS5228A: Designing Analytics Projects'
footer: 'Block 2: Acquisition Analyses'
---

<!-- _class: lead -->
<!-- _paginate: false -->
<!-- _header: '' -->
<!-- _footer: '' -->

# Designing Analytics Projects

## Block 2: Acquisition Analyses

**Eduardo Arino de la Rubia**
January 8, 2026

---

## Block 2 Overview

| Section | Time |
|---------|------|
| Funnel Analysis | 22 min |
| Channel Attribution | 22 min |
| Mini-Case Exercise | 10 min |
| Campaign Effectiveness | 22 min |
| CAC/LTV Analysis | 18 min |

All four analyses answer: **"How efficiently are we turning money into customers?"**

---

## How to Think About These Analyses

**This is a reference library, not a memorization exercise.**

Today we cover 9 foundational analyses. You won't memorize them all—and you shouldn't try.

**Your goal:**
1. Know what each analysis answers conceptually
2. Recognize which one applies to a given problem
3. Know where to find the detailed example when you need it

Each analysis has a complete Brief example in `templates/examples/`. Use them.

<!--
INSTRUCTOR NOTE:

**Background:** Students often panic when they see 9 analyses to cover in one day. This slide reframes expectations. The goal isn't memorization — it's pattern recognition. They need to know WHAT each analysis does, not HOW to execute it perfectly from memory.

**Key point:** Know what each analysis answers, not how to execute every detail.

**Say something like:**
"I want to set expectations for this block and the next one. We're going to cover 9 foundational analyses today. That sounds like a lot — and it is. But here's what I don't want you to do: don't try to memorize everything.

These analyses are a reference library. When you encounter a problem in the real world, you'll think: 'This looks like a funnel problem,' or 'This is a retention question.' Then you'll look up the details.

Your goal today is threefold. One: know what each analysis answers conceptually. Two: recognize which one applies when you see a business problem. Three: know where to find the detailed examples when you need them.

The template folder has complete Brief examples for each analysis. When you're working on your assignment, use them. Copy the structure. Adapt the content. That's how professionals work — nobody starts from a blank page."

**If asked:** "Will we need to memorize the formulas?"
A: For the exam, you'll need to know core concepts and when to use each analysis. The Brief template will be provided as reference.

**Transition:** "Let's dive into the first acquisition analysis — funnel analysis..."
-->

---

<!-- _class: lead -->

# Part 1: Funnel Analysis
### *(22 minutes)*

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_02_funnel_basic.png)

---

## Funnel Analysis: The Core Question

Every conversion process has steps. Most users don't finish.

Your job: **Find where they leave, and why.**

**The core question:** At which step are we losing the most users, and why?

<!--
INSTRUCTOR NOTE:

**Background:** Funnel analysis is usually the first analysis new analysts learn, but it's often done poorly. The common mistake is calculating overall conversion without understanding step-by-step drop-off. The "why" is crucial — you can identify WHERE users drop but understanding WHY requires segmentation and often qualitative research.

**Key point:** Funnel analysis tells you WHERE users drop. The "why" requires digging deeper.

**Say something like:**
"Funnel analysis is one of the most common analytics tasks you'll encounter. Every conversion process has steps, and most users don't make it to the end. Your job is to find where they leave — and more importantly, why.

I want to emphasize that second part. Funnel analysis is very good at telling you WHERE users drop off. It's much harder to tell you WHY. If you see a 40% drop at the payment step, you know there's a problem. But is it because the page is slow? The form is confusing? They're comparison shopping? They don't have their credit card handy? The funnel doesn't tell you that.

So when you do funnel analysis, you're usually generating hypotheses, not proving conclusions. You identify the biggest drops, then segment to narrow down causes, then often need qualitative research — user interviews, session recordings — to understand the 'why'."

**If asked:** "How do I know if a drop-off rate is bad?"
A: Compare to benchmarks (industry averages), your historical data, or segment by segment. A 60% checkout completion might be great for luxury goods and terrible for commodities.

**Transition:** "Let me show you just how universal funnel thinking is..."
-->

---

## Funnels Are Everywhere

| Business | Typical Stages |
|----------|---------------|
| **E-commerce** | Browse → Cart → Purchase |
| **SaaS** | Visit → Sign up → Subscribe |
| **B2B Sales** | Lead → SQL → Closed Won |
| **Mobile App** | Install → Register → First Action |
| **Content** | Impression → Click → Share |

The stages depend on your business. Define them explicitly.

<!--
INSTRUCTOR NOTE:

**Background:** Students sometimes think funnels only apply to e-commerce checkout. This table shows that funnel thinking is universal — any multi-step process can be analyzed as a funnel. The key insight is that YOUR business defines what the stages are; there's no universal template.

**Key point:** Funnels apply to any multi-step conversion process. Your business defines the stages.

**Say something like:**
"I want to show you that funnel thinking isn't just for e-commerce checkout. It's a universal framework.

E-commerce: Browse, Cart, Purchase — that's obvious. But look at SaaS: Visit, Sign up, Subscribe. Same structure. B2B sales: Lead, Sales Qualified Lead, Closed Won. Mobile app: Install, Register, First meaningful action.

Even content marketing is a funnel: Impression, Click, Share.

The point is: YOUR business defines what the stages are. There's no universal template. Your first job in any funnel analysis is to define the stages explicitly. What are the steps a user goes through? What events mark each transition?"

**If asked:** "How many stages should a funnel have?"
A: Typically 3-7. Too few and you miss important drops. Too many and you're just tracking every click. Focus on stages where users make meaningful decisions.

**Transition:** "Let me show you what data you need to do this analysis..."
-->

---

## The Data You Need

Funnel analysis requires **event-level data** with three things:

| Field | Example | Why |
|-------|---------|-----|
| `user_id` | `u_12345` | Track same user across steps |
| `timestamp` | `2026-01-08 14:32:07` | Sequence events in order |
| `event_type` | `checkout_started` | Identify which step occurred |

Optional but valuable: device, source, session_id, properties (like cart value)

<!--
INSTRUCTOR NOTE:

**Background:** Students often jump to analysis before understanding data requirements. The three required fields — user_id, timestamp, event_type — are non-negotiable for funnel analysis. Without user_id, you can't track the same person. Without timestamp, you can't sequence events. Without event_type, you can't define stages. Many analytics failures start with "we don't have that field."

**Key point:** Three fields are non-negotiable: user_id, timestamp, event_type. Check data availability BEFORE committing to the analysis.

**Say something like:**
"Before you do any funnel analysis, you need three things in your data.

User ID — some way to track the same person across steps. This could be a logged-in user ID, a device ID, a cookie. But you need something.

Timestamp — when did each event happen? You need this to sequence the journey. Did they add to cart before or after viewing shipping costs?

Event type — what happened? You need distinct events for each stage. 'checkout_started', 'payment_submitted', 'order_confirmed' — whatever your company calls them.

Without any one of these three, you cannot do funnel analysis. Full stop.

The optional fields — device, source, session_id — are what let you do the really valuable work: segmentation. But the core three are required.

Here's a tip: before you commit to a funnel analysis in your Brief, verify that these fields exist and are reliable. Many projects fail because someone assumed the data existed."

**If asked:** "What if we have page views but not events?"
A: Page views can work if URLs are unique per stage. But events are more reliable — page views can fire multiple times, have bot traffic, etc.

**Transition:** "Now let's talk about defining stages precisely..."
-->

---

## Defining Stages: Be Precise

**Vague:** "User started checkout"
**Precise:** "`checkout_start` event fired"

| Stage | Good Definition |
|-------|-----------------|
| Cart | `cart_page_loaded` event |
| Payment | `payment_form_submitted` event |
| Complete | `order_confirmation` event with `order_id` |

**Rule:** If you can't write the SQL WHERE clause, you haven't defined it.

<!--
INSTRUCTOR NOTE:

**Background:** Vague stage definitions are one of the most common sources of analytics confusion. When someone says "checkout started," five people might interpret it five different ways. The SQL test forces precision: if you can't write WHERE event_type = 'something', you haven't defined it. This connects directly to the Brief's metric precision requirements.

**Key point:** If you can't write the SQL WHERE clause, you haven't defined the stage.

**Say something like:**
"This is a rule I want you to internalize: if you can't write the SQL WHERE clause, you haven't defined it.

'User started checkout' — what does that mean? Did they click the checkout button? Did the checkout page load? Did they enter their email? Five people might interpret this five different ways.

'checkout_start event fired' — now I can write SQL. WHERE event_type = 'checkout_start'. No ambiguity.

[Point to table]

Look at these definitions. Cart: cart_page_loaded event. Payment: payment_form_submitted event. Complete: order_confirmation event with order_id.

Each one is precise enough to query. That's the standard.

When you write your Brief's metrics section, apply this test. Can you write the SQL? If not, keep refining until you can."

**If asked:** "What if my company doesn't have consistent event naming?"
A: That's a common problem. You'll need to figure out what events exist and what they mean. Check with engineering or look at the raw data. Document your definitions explicitly.

**Transition:** "Now let's calculate conversion rates..."
-->

---

## How to Calculate Conversion Rates

**Conversion Rate** = Users at Step N+1 / Users at Step N

**Example:**

| Stage | Users | Conv. Rate |
|-------|-------|------------|
| Cart | 10,000 | 85% → |
| Shipping | 7,820 | 88% → |
| Payment | 6,882 | 89% → |
| Confirm | 6,125 | — |

**Overall:** 61.3% cart-to-confirm

<!--
INSTRUCTOR NOTE:

**Background:** This is the fundamental calculation of funnel analysis. Students need to understand both the step-by-step rates AND the overall rate. The step-by-step view reveals WHERE drops happen; the overall rate gives the total picture. Note that the numbers compound: 0.85 × 0.88 × 0.89 ≈ 0.67, but we show 61.3% because of rounding at each step.

**Key point:** Calculate step-by-step rates, not just overall. The step-by-step view reveals where the problem is.

**Say something like:**
"Let me walk through the math. Conversion rate is users at step N+1 divided by users at step N. Simple division.

[Point to table]

10,000 users hit the cart. 8,500 made it to shipping — that's 85%. Of those 7,820 who saw shipping, 6,882 made it to payment — 88%. Of those, 6,125 confirmed — 89%.

Now, 85% sounds great. 88% sounds great. 89% sounds great. But multiply them together and you get 61.3% overall.

This is why step-by-step matters. If someone just told you 'checkout is 61%,' you might think 'okay, we're losing 39% somewhere.' But where? You don't know.

When you break it down by step, you see the biggest drop is cart to shipping — 15% lost. That's 1,500 people. Maybe shipping costs are scaring them off. The payment and confirm steps are actually pretty healthy."

**If asked:** "Should we count users or sessions?"
A: Usually users, to avoid double-counting the same person who abandons and returns. But depends on your business — some use sessions if repeat purchases in same session matter.

**Transition:** "Let me show you what this looks like visually..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_02_funnel_output.png)

---

## Reading Funnel Output

Two ways to view:
- **Percentage view:** Which step has the worst conversion rate?
- **Absolute view:** Which step loses the most users?

Sometimes they're different. A 5% drop from 100K users (5K lost) matters more than a 20% drop from 1K users (200 lost).

<!--
INSTRUCTOR NOTE:

**Background:** This distinction trips up many analysts. Percentage view finds the "leakiest" step; absolute view finds where the most opportunity is. For prioritization, you usually want absolute view — that's where fixing the problem has the biggest impact. But percentage view can reveal UX problems that affect smaller populations.

**Key point:** Percentage and absolute views tell different stories. For prioritization, use absolute — that's where the dollars are.

**Say something like:**
"Two ways to read a funnel, and they can tell different stories.

Percentage view asks: which step has the worst conversion rate? If step 3 converts at 60% and step 4 at 85%, step 3 is the 'leakiest.'

Absolute view asks: which step loses the most users in raw numbers? That depends on how many people reach each step.

[Point to the example]

5% drop from 100K users — you lose 5,000 people. 20% drop from 1K users — you lose 200 people. Percentage-wise, the 20% drop is worse. But for business impact? The 5% drop matters 25 times more.

When you're prioritizing what to fix, use absolute view. That's where the revenue is. A 10% improvement to a step that sees 100K users beats a 50% improvement to a step that sees 1K users.

Percentage view is still useful for diagnosis — a 50% drop-off is probably a broken UX, even if it's in a small segment."

**Transition:** "Now let me show you where the real insights come from — segmentation..."
-->

---

## Segmentation: The Real Power

Overall funnel hides important variation.

| Segment | Cart-to-Confirm |
|---------|-----------------|
| **Desktop** | 68% |
| **Mobile Web** | 54% |
| **iOS App** | 72% |
| **New Users** | 51% |
| **Returning Users** | 74% |

**Segment by:** Device, traffic source, new vs. returning, geography, time period.

The insight is usually in the segments, not the aggregate.

<!--
INSTRUCTOR NOTE:

**Background:** This is one of the most important slides in the funnel section. The aggregate funnel (say, 61% overall conversion) hides all the interesting variation. When you segment, you discover that mobile web is 54% while iOS app is 72% — that's an 18 percentage point gap! Segmentation is where insights live.

**Key point:** The insight is usually in the segments, not the aggregate.

**Say something like:**
"This is where funnel analysis gets interesting. The overall number — 61% checkout completion — is not that useful. It's an average that hides everything important.

Look at this table. Desktop is 68%. Mobile web is 54%. That's a 14 percentage point gap. iOS app is 72% — even better than desktop. New users are 51%, returning users are 74%.

Do you see the insights now? Mobile web has a problem. New users struggle more than returning users. These are actionable findings. 'Overall conversion is 61%' is not actionable.

This is why your first move after building the overall funnel should be: segment. By device, by traffic source, by new vs. returning, by geography, by time period.

The insight is almost never in the aggregate. It's in the segments."

**If asked:** "How many segments should I look at?"
A: Start with the obvious ones: device, new/returning, traffic source. Then let hypotheses guide you. Don't segment randomly — each segment should answer a question.

**Transition:** "Before we move on, let me warn you about common data issues..."
-->

---

## Common Funnel Data Issues

- **Missing events** — Event counts << page views → undercounts
- **Duplicate events** — Same user/timestamp → overcounts
- **Bot traffic** — Unusual patterns, data center IPs → inflates top
- **Cross-device** — User appears twice → undercounts
- **Session stitching** — Gaps in journey → breaks logic

**Always validate data before analyzing.**

<!--
INSTRUCTOR NOTE:

**Background:** Data quality issues are the most common source of funnel analysis failures. Students should understand that validating data comes BEFORE analysis. These five issues cover 90% of funnel data problems they'll encounter.

**Key point:** Never trust funnel data without validation. Each issue has a diagnostic pattern and affects the funnel differently.

**Say something like:**
"Before you analyze any funnel, you need to validate the data. Let me walk through the five most common issues.

Missing events — you look at your funnel and the numbers don't add up. More people complete checkout than start payment? That's impossible. Usually means the payment start event isn't firing. Compare event counts to page views as a sanity check.

Duplicate events — the opposite problem. Someone refreshes a page and you count them twice. Look for identical user/timestamp combinations and dedupe.

Bot traffic — inflates your top of funnel. You see tons of product views but nobody adds to cart. Check for patterns: same IP hitting hundreds of pages per second, data center IPs, no JavaScript execution.

Cross-device — Maria starts on her phone, completes on her laptop. If you can't stitch those sessions together, she looks like two users: one who abandoned and one who magically converted without starting. Undercounts your conversion rate.

Session stitching — related but different. Gaps in the journey that break your funnel logic. User goes from browse to purchase with nothing in between.

The diagnostic: always validate before you analyze. Check event counts against page views. Look for duplicates. Check for bot patterns. Otherwise you'll recommend a UI fix when the real problem is measurement."

**If asked:** "How do you catch these issues?"
A: Sanity checks. Compare event counts to page views. Look for impossible sequences (more completions than starts). Check for data center IPs. Look for identical timestamps.

**Transition:** "Now let's apply what we've learned to a real scenario..."
-->

---

## The Quickcart Scenario

**Company:** Quickcart (e-commerce)
**Problem:** Checkout completion dropped from 68% to 61%
**Stakes:** ~$4.2M in lost quarterly revenue

**Hypothesis:** Drop concentrated in payment step on mobile (new UI launched October)

<!--
INSTRUCTOR NOTE:

**Background:** This is the first complete scenario application in the course. Walk through how the Brief framework connects to funnel analysis. Note the specific elements: measurable problem (68% to 61%), quantified stakes ($4.2M), and a testable hypothesis (payment step, mobile, October launch). This is what "good scoping" looks like.

**Key point:** Notice how the hypothesis is specific and testable: payment step, mobile, October launch.

**Say something like:**
"Let me walk you through how funnel analysis connects to the Brief framework.

Quickcart is an e-commerce company. Their checkout completion dropped from 68% to 61%. That's 7 percentage points — and they've calculated it costs them about $4.2M per quarter.

Now look at the hypothesis: 'Drop concentrated in payment step on mobile, new UI launched October.'

This hypothesis is specific and testable. We can segment the funnel by device and look at the payment step. We can compare October and after to before October. If the hypothesis is right, we'll see mobile payment drop concentrated after the October launch.

That's what good scoping looks like. Not 'checkout is bad' — that's too vague. Not 'maybe the whole thing is slow' — that's not testable. A specific hypothesis about where, when, and what changed."

**If asked:** "What if the hypothesis is wrong?"
A: Great! That's a result. You eliminate one explanation and move to the next. Hypotheses are meant to be tested, not confirmed.

**Transition:** "Let's see how the Brief sections fill out for this scenario..."
-->

---

## Quickcart: The Brief Application

| Brief Section | Quickcart |
|--------------|-----------|
| **Primary metric** | `order_complete` / `checkout_start`, per session, US users |
| **Counter-metrics** | AOV (tradeoff), Fraud rate (guardrail), Support tickets (guardrail) |
| **Blocker** | Mobile team lead — defensive about October launch |

**Pre-mortem:** We identified payment step as problem, but events weren't firing on iOS 17. Recommended UI fix when real issue was measurement.

<!--
INSTRUCTOR NOTE:

**Background:** This slide connects the funnel analysis back to the Brief framework. The pre-mortem is crucial — it shows how data quality issues (the measurement problem from the previous slide) can lead to wrong recommendations. The blocker identification (mobile team lead) illustrates stakeholder management in a politically charged situation.

**Key point:** The pre-mortem reveals the trap: recommending a UI fix when the real problem was measurement. Always validate data first.

**Say something like:**
"Let me walk through how this connects to your Brief.

Primary metric is precisely defined: order_complete divided by checkout_start, measured per session, US users only. Notice the specificity — not just 'conversion rate' but exactly which events and which population.

Counter-metrics show you're thinking beyond the primary goal. AOV is a tradeoff counter-metric — you could boost conversion by showing only cheap products, but that tanks AOV. Fraud rate and support tickets are guardrails — if your 'fix' introduces more fraud or confuses customers, you've made things worse.

The blocker is the mobile team lead who owns the October UI launch. If your analysis points to their UI as the problem, they're going to push back hard. You need to anticipate that and have solid evidence.

But here's the lesson — look at the pre-mortem. You identified the payment step as the problem, recommended a UI fix, but the real issue was that events weren't firing on iOS 17. It was a measurement problem, not a UI problem.

This is why data validation comes first. This is why the pre-mortem exercise is so valuable — it forces you to imagine what could go wrong. If you had asked 'what if our event logging is broken?' you might have checked before recommending the wrong fix."

**If asked:** "How do you handle the blocker situation?"
A: Don't accuse their UI. Present the data objectively. If their UI is the problem, let the data speak. If it's a measurement issue, you've avoided a political fight entirely.

**Transition:** "Let's summarize the key takeaways from funnel analysis..."
-->

---

## Funnel Analysis: Key Takeaways

1. **Define stages with event names** — not page names, not intentions
2. **Calculate both % and absolute drops** — they tell different stories
3. **Segment immediately** — the insight is in the segments
4. **Validate data first** — logging gaps will mislead you
5. **Counter-metrics matter** — conversion isn't the only goal (AOV, fraud)

<!--
INSTRUCTOR NOTE:

**Background:** This is the summary slide for funnel analysis. Use it to reinforce the core lessons before moving to attribution. Students should remember these five points even if they forget the details.

**Key point:** These five points are the essential takeaways from funnel analysis.

**Say something like:**
"Let me summarize funnel analysis with five key takeaways.

One: Define stages with event names. Not 'checkout page' but 'checkout_start' event. Be precise.

Two: Calculate both percentage AND absolute drops. A 5% drop from 1 million users is 50,000 lost customers. That matters.

Three: Segment immediately. The overall funnel hides the story. Break it down by device, channel, user type.

Four: Validate your data first. Missing events, duplicates, bot traffic — check for all of these before drawing conclusions.

Five: Counter-metrics matter. Don't just optimize conversion. Watch AOV, fraud rate, support tickets.

These five principles will serve you in any funnel analysis. Now let's move to attribution."

**Transition:** "Now let's talk about a different problem: who gets credit for the sale?"
-->

---

<!-- _class: lead -->

# Part 2: Channel Attribution Analysis
### *(22 minutes)*

---

## What is Attribution?

**Assigning credit to marketing touchpoints for conversions.**

A user's journey: LinkedIn ad (day 1) → Google ad (day 5) → Direct purchase (day 8)

**Who gets credit for the sale?**

This is the attribution problem. There's no objectively "correct" answer.

<!--
INSTRUCTOR NOTE:

**Background:** Attribution is one of the most contentious topics in marketing analytics. Billions of dollars are allocated based on attribution models, yet there's no objectively "correct" answer — just different ways of assigning credit. This is fundamentally different from funnel analysis, where conversion rates are facts. Attribution is a modeling choice.

**Key point:** Attribution is about assigning credit, not measuring truth. There's no objectively correct answer.

**Say something like:**
"Let me be clear upfront: attribution is different from the other analyses we'll cover.

In funnel analysis, conversion rates are facts. 61% of users completed checkout — that's a number you can calculate precisely.

In attribution, we're making modeling choices. A user saw a LinkedIn ad on Monday, clicked a Google ad on Friday, and bought on Sunday. Who gets credit for the sale?

There's no objectively correct answer. LinkedIn introduced them. Google reminded them. The product convinced them. All three contributed.

Attribution models are different ways of assigning credit. Last-touch gives all credit to Google. First-touch gives all credit to LinkedIn. Linear splits it evenly.

None of these is 'right.' They're different lenses. The question is: which lens is most useful for the decision you're making?"

**If asked:** "So which model should we use?"
A: Depends on the decision. For budget allocation, I recommend comparing multiple models and looking for channels where they disagree dramatically. That's where investigation is needed.

**Transition:** "First, let's define what a touchpoint is..."
-->

---

## What is a Touchpoint?

A **touchpoint** is any recorded marketing interaction:

| Field | Example | Purpose |
|-------|---------|---------|
| `user_id` | `u_12345` | Link touchpoints to conversions |
| `timestamp` | `2026-01-05 09:14:22` | Sequence the journey |
| `channel` | `paid_search` | What marketing source |
| `campaign` | `winter_sale_2026` | Which specific effort |
| `action` | `click` or `impression` | What happened |

You need touchpoints joined to conversion events by user.

<!--
INSTRUCTOR NOTE:

**Background:** Students need to understand the data substrate for attribution analysis. A touchpoint is any recorded marketing interaction — not just clicks, but impressions too. The key insight is that you need to link touchpoints to conversions, which requires user_id matching across systems.

**Key point:** A touchpoint is any recorded marketing interaction. The challenge is linking touchpoints across platforms to the same user.

**Say something like:**
"A touchpoint is any marketing interaction we can record. Let me walk through the data you need.

User_id — this is how you link touchpoints to conversions. It's also the hardest part. Different platforms have different identifiers. Your ad platform has one ID, your website has another, your CRM has another. Matching these is an entire discipline called identity resolution.

Timestamp — you need to know when the touchpoint happened so you can sequence the journey. First touch, last touch, what happened in between.

Channel — what marketing source. Paid search, paid social, email, organic, referral. This is what you're trying to attribute credit to.

Campaign — more granular than channel. Within paid search, which campaign? Winter sale? Brand awareness? Retargeting?

Action — what happened. A click is active engagement. An impression means they saw it but didn't click. Different models weight these differently.

The key is joining this touchpoint table to your conversion table by user. That's how you answer 'what touchpoints did this customer see before converting?'"

**If asked:** "How do you handle cross-device tracking?"
A: It's hard. Probabilistic matching, login-based identity, device graphs. No perfect solution. This is why attribution data is always somewhat incomplete.

**Transition:** "Let me show you what this data structure looks like..."
-->

---

## The Data Structure

**Touchpoint Table:**

| user_id | timestamp | channel | action |
|---------|-----------|---------|--------|
| u_123 | Jan 1 | linkedin_ads | impression |
| u_123 | Jan 5 | paid_search | click |
| u_123 | Jan 8 | direct | click |

**Conversion Table:**

| user_id | timestamp | revenue |
|---------|-----------|---------|
| u_123 | Jan 8 | $150 |

**Join them** to see all touchpoints that preceded the conversion.

<!--
INSTRUCTOR NOTE:

**Background:** This slide shows the concrete data structure students will work with. The key operation is the JOIN — connecting touchpoints to conversions. Walk through the example: user u_123 saw a LinkedIn ad, clicked a Google ad, came back direct, and bought. The question becomes: which of these touchpoints gets credit?

**Key point:** Attribution analysis starts with joining touchpoints to conversions. The result is a journey per converted user.

**Say something like:**
"Here's what the data looks like in practice.

Top table is your touchpoint log. User u_123 saw a LinkedIn ad on January 1st — that's an impression, they saw it but didn't click. Then on January 5th they clicked a paid search ad. Then on January 8th they came back directly — maybe typed your URL, maybe had it bookmarked.

Bottom table is your conversions. User u_123 bought something worth $150 on January 8th.

Now you join these tables. For every conversion, you get all the touchpoints that preceded it. That's the journey: LinkedIn impression → paid search click → direct click → purchase.

Who gets credit for this $150 sale? That's what attribution models answer.

Note the complexity: the LinkedIn impression happened 7 days before purchase. Should that count? The direct visit was the last thing before buying — but did it really 'cause' the sale? These are the judgment calls that make attribution controversial."

**If asked:** "What if there are no touchpoints before conversion?"
A: That's 'organic' or 'unattributed.' Either they truly found you without marketing, or your tracking couldn't capture their journey. The latter is more common than you'd think.

**Transition:** "This brings us to a critical question: how far back should we look?..."
-->

---

## Attribution Windows

**How far back should you look?**

| Window | Use Case |
|--------|----------|
| **7-day click** | Standard for lower-funnel (search, retargeting) |
| **30-day click** | B2B, considered purchases |
| **1-day view** | Display, video (saw ad but didn't click) |
| **90-day** | Enterprise sales, long cycles |

**The window changes the answer.** A 7-day window ignores a LinkedIn ad from 3 weeks ago. A 90-day window includes it.

Be explicit about your window choice.

<!--
INSTRUCTOR NOTE:

**Background:** Attribution windows are a major source of disagreement between marketing teams. Google and Meta default to different windows, which makes cross-channel comparison misleading. The choice of window is a judgment call that should match purchase cycle length. B2B with 90-day sales cycles needs 90-day windows; impulse e-commerce might need 7-day.

**Key point:** The window changes the answer dramatically. Be explicit about your choice and why.

**Say something like:**
"Attribution windows are one of those technical details that have massive business implications.

The question is: how far back do you look for touchpoints that 'count' toward a conversion?

[Walk through table]

7-day click is the default for many ad platforms. If someone clicked an ad and converted within 7 days, that ad gets credit. But what if your sales cycle is 30 days? That first touch from 3 weeks ago gets zero credit.

For B2B with longer sales cycles, 30-day or even 90-day windows make more sense.

View-through windows — 1-day view — are for when someone saw an ad but didn't click. Did that awareness contribute? Maybe. But a 7-day view window would attribute tons of conversions to display ads people barely noticed.

Here's the key: the window changes the answer. If you use a 7-day window, awareness channels look terrible. If you use a 90-day window, awareness channels look much better. Neither is 'right' — but you need to choose consciously and document why.

When you compare channels, make sure they're using the same window. Google's default is different from Meta's default — comparing them head-to-head is apples to oranges."

**Transition:** "Let's look at the first attribution model..."
-->

---

## Attribution Model: First-Touch

**Rule:** 100% credit to the first touchpoint in the journey.

```
SELECT user_id, MIN(timestamp) as first_touch, channel
FROM touchpoints
WHERE timestamp <= conversion_time
  AND timestamp >= conversion_time - INTERVAL 30 DAY
GROUP BY user_id
```

**Bias:** Overvalues awareness channels (display, social, content)
**Undervalues:** Conversion channels (search, retargeting)

<!--
INSTRUCTOR NOTE:

**Background:** First-touch attribution is the mirror image of last-touch. It credits whoever introduced the customer, ignoring who closed the deal. It's useful for understanding which channels build awareness and start customer journeys. The SQL is simple — MIN(timestamp) instead of MAX. Use first-touch when evaluating brand-building campaigns.

**Key point:** First-touch answers "who started the journey?" It overvalues awareness and undervalues closers.

**Say something like:**
"First-touch is the opposite of last-touch. 100% credit to whoever first touched the customer within the attribution window.

The SQL is simple: MIN timestamp instead of MAX.

The bias is reversed. First-touch overvalues awareness channels — display ads, social, content marketing. These channels often start journeys but rarely close them. Under first-touch, they look great.

It undervalues conversion channels — search, retargeting, branded terms. These channels close deals but often weren't first.

When would you use first-touch? When you're evaluating brand-building campaigns. 'Is our podcast sponsorship starting new customer relationships?' First-touch would show you. Last-touch would show you nothing.

Neither first nor last-touch is 'right.' They answer different questions. First-touch: who starts journeys? Last-touch: who closes deals? Most mature companies run both and look for differences."

**Transition:** "Last-touch is more commonly used — let me show you why it's problematic..."
-->

---

## Attribution Model: Last-Touch

**Rule:** 100% credit to the final touchpoint before conversion.

```
SELECT user_id, MAX(timestamp) as last_touch, channel
FROM touchpoints
WHERE timestamp <= conversion_time
  AND timestamp >= conversion_time - INTERVAL 30 DAY
GROUP BY user_id
```

**Bias:** Overvalues closers (branded search, direct, retargeting)
**Undervalues:** Awareness channels that started the journey

**This is what most companies use by default.** It's convenient but misleading.

<!--
INSTRUCTOR NOTE:

**Background:** Last-touch is the default attribution model at most companies because it's simple to implement and explain. But it systematically overvalues "closer" channels (branded search, retargeting, direct) and undervalues awareness channels (display, social, content). This creates perverse incentives — cutting awareness channels looks good under last-touch but may hurt overall acquisition.

**Key point:** Last-touch is the default, but it systematically undervalues awareness channels. Be aware of the bias.

**Say something like:**
"Last-touch is what most companies use by default. It's simple: whoever touched the customer last before they converted gets 100% credit.

The SQL is straightforward — MAX timestamp grouped by user.

But here's the problem. Last-touch systematically overvalues closers. Who's typically the last touch? Branded search — someone types your company name into Google. Direct — they type your URL. Retargeting — they already visited, you reminded them.

These channels look amazing under last-touch. But think about it: if someone types your brand name into Google, they already knew about you. Who told them? Probably an awareness channel — a LinkedIn ad, a podcast mention, a friend's recommendation — that happened weeks earlier and doesn't get credit.

Last-touch tells you who closed the deal. It doesn't tell you who introduced the customer in the first place. If you cut all your awareness channels based on last-touch data, you might find that eventually nobody knows who you are and branded search volume drops."

**If asked:** "If it's so biased, why do companies use it?"
A: Convenience. It's easy to implement, easy to explain, and channels like Google Ads report last-touch by default. It takes deliberate effort to look at multi-touch.

**Transition:** "Let's look at a model that spreads credit more evenly..."
-->

---

## Attribution Model: Linear

**Rule:** Split credit equally among all touchpoints.

If user had 4 touchpoints before a $100 conversion:
- LinkedIn: $25
- Content: $25
- Email: $25
- Search: $25

**Bias:** Treats all touchpoints as equal, ignores timing
**Useful for:** Seeing full journey, identifying "assist" channels

<!--
INSTRUCTOR NOTE:

**Background:** Linear attribution is the simplest "multi-touch" model. It acknowledges that multiple touchpoints contributed to the conversion, unlike single-touch models. However, it treats all touches as equally important, which is its main weakness. A LinkedIn ad impression 30 days ago gets the same credit as the search click that happened right before purchase.

**Key point:** Linear is the simplest multi-touch model. It's egalitarian but ignores timing and engagement differences.

**Say something like:**
"Linear is the simplest way to spread credit across touchpoints. Everyone gets an equal share.

If a user had four touchpoints before a $100 conversion, each channel gets $25. Simple, fair, democratic.

The advantage? It acknowledges that multiple channels contributed. It surfaces 'assist' channels that never get credit under first or last touch.

The disadvantage? A LinkedIn impression from 30 days ago gets the same credit as the search click that happened 10 minutes before purchase. Intuitively, that feels wrong. The recent touchpoint probably mattered more for this specific conversion.

Linear is useful when you want to see the full picture — which channels are appearing in journeys at all? But for budget allocation, you probably want something that accounts for timing."

**If asked:** "Is linear ever the best choice?"
A: It's useful for discovery — seeing which channels appear in journeys. For budget allocation, time-decay or position-based are usually better because they account for recency.

**Transition:** "Time-decay tries to fix the timing problem..."
-->

---

## Attribution Model: Time-Decay

**Rule:** More credit to recent touchpoints, less to older ones.

Common approach: Half-life decay (e.g., 7-day half-life)

| Days Before Conversion | Weight |
|-----------------------|--------|
| 0 (same day) | 100% |
| 7 | 50% |
| 14 | 25% |
| 21 | 12.5% |

**Bias:** Still privileges closers, just less extremely than last-touch
**Useful for:** Compromise between first and last touch

<!--
INSTRUCTOR NOTE:

**Background:** Time-decay adds a recency dimension to multi-touch attribution. The half-life concept is from radioactive decay — the weight halves every N days. This addresses linear's main weakness (ignoring timing) while still giving some credit to earlier touchpoints. The 7-day half-life is common but arbitrary; adjust based on your sales cycle.

**Key point:** Time-decay gives more credit to recent touchpoints but doesn't ignore earlier ones entirely. The half-life should match your sales cycle.

**Say something like:**
"Time-decay fixes linear's main problem: ignoring timing.

The concept comes from radioactive decay — half-life. Every 7 days, the weight halves. A touchpoint on the day of conversion gets 100% weight. A touchpoint from 7 days ago gets 50%. 14 days ago gets 25%. And so on.

So if you had a $100 conversion with two touchpoints — one same-day and one from 7 days ago — the same-day gets about 67% credit ($67), the older one gets 33% ($33). Not equal, but both count.

The bias is clear: time-decay still privileges closers. It's softer than last-touch, but it's still saying 'recency matters.' That may or may not match your business reality.

The half-life is arbitrary. 7 days is common, but if your sales cycle is 90 days, you might use 30-day half-life. The point is to match the decay to how long consideration typically takes in your business."

**If asked:** "How do you pick the right half-life?"
A: Match it to your sales cycle. If typical time from first touch to purchase is 30 days, use a 7-10 day half-life. If it's 7 days, use 2-3 days. There's no universally 'correct' answer.

**Transition:** "The last model tries to capture both ends of the journey..."
-->

---

## Attribution Model: Position-Based (U-Shaped)

**Rule:** Heavy credit to first and last, less to middle.

Typical: **40% first / 20% middle (split) / 40% last**

Recognizes that:
- First touch introduced the user (awareness)
- Last touch closed the deal (conversion)
- Middle touches helped but were less decisive

**Popular because it feels intuitively fair.**

<!--
INSTRUCTOR NOTE:

**Background:** Position-based (also called U-shaped or bathtub) attribution tries to capture two important moments: awareness (first touch) and conversion (last touch). The 40/20/40 split is arbitrary but widely used. It satisfies both brand marketers (who value awareness) and performance marketers (who value conversion), which makes it politically viable.

**Key point:** Position-based credits both ends of the journey. It's popular because it's a political compromise between awareness and performance marketing teams.

**Say something like:**
"Position-based is my personal favorite for most use cases. Let me explain why.

It recognizes two critical moments in a customer journey. The first touch — who introduced this person to our brand? And the last touch — who closed the deal?

Both matter. The LinkedIn ad that introduced someone to you 30 days ago is valuable — without it, they'd never have heard of you. The search ad they clicked right before buying is also valuable — it converted the interest into revenue.

The middle touches? They helped nurture the relationship, but they're less decisive than the bookends.

The 40/20/40 split is arbitrary. Some companies use 30/40/30 or other variations. The exact numbers matter less than the principle: credit both ends.

Here's the real reason it's popular: it makes both brand marketers and performance marketers happy. Brand teams want credit for awareness. Performance teams want credit for conversions. Position-based says 'you're both important.' It's a political compromise that happens to be analytically reasonable."

**If asked:** "Why not 50/0/50 and ignore the middle entirely?"
A: Middle touches do matter — they keep the relationship warm. A user might have abandoned without that email reminder. 20% acknowledges their contribution without overweighting them.

**Transition:** "Let's compare the output from these models..."
-->

---

## Attribution Output: Touch-Based Models

| Channel | Last-Touch | First-Touch |
|---------|-----------|-------------|
| Paid Search | $450K | $180K |
| LinkedIn | $80K | $310K |
| Content/SEO | $120K | $260K |
| Direct | $150K | $200K |

Last-touch favors closers. First-touch favors awareness.

<!--
INSTRUCTOR NOTE:

**Background:** This table is the key "aha moment" for attribution. The same channels have wildly different attributed values depending on the model. LinkedIn: $80K last-touch vs $310K first-touch — that's a 4x difference! This is why attribution debates are so contentious: the model determines who looks good and who gets budget.

**Key point:** Same data, different models, 4x different answers. The model choice is political, not just technical.

**Say something like:**
"This table is the most important one in the attribution section. Look at the differences.

Paid Search: $450K under last-touch, $180K under first-touch. That's 2.5x difference.

LinkedIn: $80K last-touch, $310K first-touch. That's a 4x difference!

[Pause for effect]

Same conversions. Same revenue. Same data. Completely different credit allocation.

Now imagine you're the LinkedIn campaign manager and your performance review is based on attributed revenue. Under last-touch, you're at $80K — probably getting a budget cut. Under first-touch, you're at $310K — you're a hero.

This is why attribution is political. The model choice determines who looks good. When someone advocates for a particular attribution model, ask yourself: does that model happen to favor their channel?

The right answer is to present both. Look for the gaps. LinkedIn at $80K vs $310K is screaming 'investigate me!' That gap means LinkedIn is starting journeys but not closing them. Is that valuable? Depends on your strategy."

**Transition:** "Distributed models try to be more balanced..."
-->

---

## Attribution Output: Distributed Models

| Channel | Linear | Position-Based |
|---------|--------|----------------|
| Paid Search | $290K | $320K |
| LinkedIn | $220K | $195K |
| Content/SEO | $200K | $190K |
| Email | $140K | $145K |
| Direct | $150K | $150K |

Distributed models spread credit more evenly across the journey.

**Look for channels where models disagree dramatically.** LinkedIn: $80K (last-touch) vs. $310K (first-touch). That's worth investigating.

<!--
INSTRUCTOR NOTE:

**Background:** This table shows linear and position-based results. Notice how much more consistent the numbers are compared to the previous slide — distributed models spread credit more evenly, which reduces the extreme swings between first-touch and last-touch. The key teaching point is the methodology: look for channels where models disagree dramatically.

**Key point:** Distributed models are more stable than single-touch models. The action item is to investigate channels where models dramatically disagree.

**Say something like:**
"Now look at the distributed models. Much more consistent, right?

Paid Search: $290K linear, $320K position-based. That's close.
LinkedIn: $220K and $195K. Also pretty close.

Compare this to the previous slide where LinkedIn was $80K vs $310K depending on the model. Distributed models smooth out those extremes.

But here's the real insight — the action item isn't to pick one model and use it forever. The action item is to look for disagreement between models.

When you compare all four models, LinkedIn jumps out: $80K last-touch, $310K first-touch, $220K linear, $195K position-based. That's telling you something. LinkedIn is starting journeys but not closing them.

Is that valuable? If you're trying to grow awareness, absolutely. If you only care about immediate conversions, maybe not. But you need to know this pattern exists before you make budget decisions.

The methodology: run multiple models, look for disagreement, investigate the outliers."

**If asked:** "Which model should we report to leadership?"
A: Report multiple models with the caveat that they measure different things. Or if forced to pick one, position-based is often a good default because it balances awareness and conversion.

**Transition:** "Beyond credit allocation, let's look at actual paths customers take..."
-->

---

## Path Analysis: Common Journeys

Beyond credit allocation, look at **paths**:

| Path | Conversions | Avg Value |
|------|-------------|-----------|
| Search → Direct | 1,240 | $95 |
| LinkedIn → Content → Search | 890 | $180 |
| Direct only | 2,100 | $75 |

**Insight:** Multi-touch journeys have higher value. LinkedIn often starts valuable journeys.

<!--
INSTRUCTOR NOTE:

**Background:** Path analysis moves beyond credit allocation to understanding customer journeys holistically. The insight that multi-touch journeys have higher average value is common — customers who engage more are more valuable. This justifies investment in awareness channels even when last-touch doesn't credit them.

**Key point:** Multi-touch journeys are more valuable. Path analysis reveals the actual customer journey, not just credit allocation.

**Say something like:**
"Path analysis is different from attribution models. Instead of allocating credit, we're looking at actual customer journeys.

[Point to table]

Search → Direct: 1,240 conversions, $95 average value. These are people who searched, clicked, came back directly, and bought.

LinkedIn → Content → Search: fewer conversions — 890 — but $180 average value. Almost double!

Direct only: 2,100 conversions, but only $75 average value. These are people who just showed up and bought. Probably existing customers or word-of-mouth.

What's the insight? Multi-touch journeys are more valuable. Customers who engage with multiple channels before converting spend more. This makes sense — they're doing research, they're more intentional.

This has budget implications. If LinkedIn starts journeys that are worth 2x as much, cutting LinkedIn doesn't just reduce conversions — it reduces your highest-value conversions. The last-touch model completely misses this because it only credits who closed."

**If asked:** "How many paths should we analyze?"
A: Focus on the top 10-20 paths by volume or value. There's a long tail of rare paths that you can usually ignore.

**Transition:** "Before we move on, let me warn you about data quality..."
-->

---

## Data Quality Nightmares

- **Cross-device** — User on phone, converts on laptop → appears as two users
- **Cookie deletion** — Privacy browsers → touchpoints disappear
- **Walled gardens** — FB/Google limit data → can't see full journey
- **UTM inconsistency** — Different teams → channels miscategorized

Attribution is only as good as your tracking.

<!--
INSTRUCTOR NOTE:

**Background:** Data quality issues are often more impactful than model choice. You can run the most sophisticated attribution model, but if your data is broken, your results are wrong. These four issues affect virtually every attribution analysis — they're not edge cases, they're the norm.

**Key point:** Attribution accuracy is capped by data quality. These issues are pervasive and often invisible unless you look for them.

**Say something like:**
"Let me be honest: data quality issues will affect every attribution analysis you ever do. These aren't edge cases — they're the norm.

Cross-device: Someone researches on their phone during lunch, buys on their laptop that evening. If you can't link those sessions, you think a phone user abandoned and a laptop user converted with no prior touchpoints. Your journey data is just wrong.

Cookie deletion: Privacy browsers, incognito mode, cookie clearing — all break your tracking. You might see 5 touchpoints in your data but the user actually had 10. The ones you missed? Gone forever.

Walled gardens: Facebook and Google control their data. They'll tell you someone clicked an ad, but they won't give you the raw data to join with your other touchpoints. You're building a puzzle with missing pieces.

UTM inconsistency: This is entirely self-inflicted. Marketing team uses utm_source=facebook, sales team uses utm_source=Facebook, product team uses utm_source=fb. Same channel, three different labels. Your attribution is now wrong because your data hygiene is broken.

The implication: be humble about attribution results. They're directionally useful, not precisely accurate. And invest in data quality before investing in sophisticated models."

**If asked:** "How much of the journey do we typically miss?"
A: Varies, but 30-50% of touchpoints missing is common. Cross-device alone can cause 20%+ of users to appear as multiple people.

**Transition:** "Let's apply this to a B2B scenario..."
-->

---

## The DataDash Scenario

**Company:** DataDash (B2B analytics platform)
**Problem:** $2.4M/quarter across 6 channels, using last-touch only
**Suspicion:** Undervaluing awareness channels (LinkedIn, content)

**Hypothesis:** LinkedIn/content in >50% of deals as first-touch but <5% of last-touch credit.

<!--
INSTRUCTOR NOTE:

**Background:** This scenario illustrates a common B2B problem: long sales cycles where attribution is especially tricky. Someone reads a blog post in January, downloads a whitepaper in March, gets a sales call in May, and closes in June. Last-touch credits the sales call, but the content did the initial work.

**Key point:** B2B has long sales cycles where awareness channels contribute early and get no credit under last-touch.

**Say something like:**
"Let's look at a B2B scenario where attribution is especially tricky.

DataDash is a B2B analytics platform. They spend $2.4M per quarter across 6 channels. They use last-touch attribution — whatever most companies use by default.

The CMO suspects something's off. LinkedIn and content marketing don't get much credit, but qualitatively, customers keep saying 'I first heard about you from a blog post' or 'I saw you on LinkedIn.'

The hypothesis: LinkedIn and content are in more than 50% of deals as the first touch, but less than 5% of deals as the last touch. They're starting journeys that search and sales are closing.

This is classic B2B. Someone reads your blog post in January. Three months later, they search for your product category, click a branded search ad, and buy. Last-touch says 'Search gets all credit.' But search only worked because content built awareness months earlier."

**If asked:** "How long are typical B2B attribution windows?"
A: Often 90 days for enterprise sales, sometimes longer. The longer the window, the more you see awareness channels contributing.

**Transition:** "Let's look at the counter-metrics for this analysis..."
-->

---

## DataDash: Counter-Metrics

| Counter-metric | Type | Why it could break |
|----------------|------|-------------------|
| **Brand awareness** | Guardrail | Cutting awareness hurts long-term |
| **Lead quality** | Guardrail | Volume ≠ close rate |

**Blocker:** Paid Search manager — recently promoted based on "Search ROI" narrative. Reallocation = budget cut = career threat.

**Pre-mortem:** We cut Search to fund LinkedIn. Pipeline dropped 25%. Search was the "closer" for journeys LinkedIn started. We double-counted LinkedIn's influence.

<!--
INSTRUCTOR NOTE:

**Background:** This slide applies the Brief framework to the attribution scenario. Notice the counter-metrics are both guardrails — things that could break if you over-optimize on attributed revenue. The blocker is interesting: it's not about data or methodology, it's about a person's career being tied to a particular narrative.

**Key point:** The pre-mortem reveals a subtle trap: reallocating from "closers" to "starters" can break the whole system because they work together.

**Say something like:**
"Let's look at the counter-metrics and stakeholders.

Counter-metrics: Brand awareness is a guardrail — if you cut awareness channels, you might see immediate attribution look fine, but long-term you're killing the pipeline. Lead quality is another guardrail — you could get more leads that don't close.

The blocker is fascinating. The Paid Search manager was recently promoted based on the 'Search drives ROI' narrative. If your analysis says 'actually, Search is just closing deals that other channels started,' you're threatening their career story. They're going to fight you.

Now the pre-mortem: 'We cut Search to fund LinkedIn. Pipeline dropped 25%.'

What happened? Search was the closer. LinkedIn was the starter. They work together. You can't just take money from closers and give it to starters — you need both. The channels aren't independent.

This is the attribution trap: you see LinkedIn undervalued, so you fund more LinkedIn and cut Search. But LinkedIn starts journeys that Search closes. Cut Search, and those LinkedIn-started journeys have no closer. Pipeline drops.

The lesson: channels interact. Test causally before making major budget shifts."

**If asked:** "How do you handle the blocker?"
A: Acknowledge their contribution explicitly. Position it as 'Search is essential for closing' not 'Search is overstated.' Same data, different framing.

**Transition:** "Let's summarize attribution before moving to the next analysis..."
-->

---

## Attribution: Key Takeaways

1. **Touchpoint = user_id + timestamp + channel** — you need all three
2. **No model is "right"** — present multiple, look for disagreements
3. **Attribution windows matter** — be explicit about your choice
4. **Path analysis reveals interactions** — channels don't work alone
5. **Data quality limits everything** — cross-device and cookies kill accuracy
6. **Validate with holdouts** — before major budget shifts, test causally

<!--
INSTRUCTOR NOTE:

**Background:** This summary slide captures the essence of attribution analysis. Point 2 is the most important message — there's no objectively correct model, so the methodology is to compare models and investigate where they disagree.

**Key point:** No attribution model is "right" — the methodology is comparative, not absolute.

**Say something like:**
"Six key takeaways from attribution.

One: A touchpoint needs user_id, timestamp, and channel. All three. Without user_id you can't join to conversions. Without timestamp you can't sequence. Without channel you can't allocate.

Two: No model is right. First-touch, last-touch, linear, position-based — they're all wrong in different ways. Present multiple, look for where they disagree dramatically. That's where the insight is.

Three: Attribution windows matter. A 7-day window and a 30-day window give different answers. Be explicit about your choice and why.

Four: Path analysis reveals interactions. Channels work together. LinkedIn starts journeys that Search closes. Don't analyze them in isolation.

Five: Data quality limits everything. Cross-device, cookie deletion, walled gardens — all corrupt your data. Your attribution is only as good as your tracking.

Six: Before you make major budget shifts based on attribution, validate with holdouts. Attribution is correlation. Holdouts give you causation."

**Transition:** "Let's test your understanding with a quick exercise..."
-->

---

<!-- _class: lead -->

# Mini-Case Exercise: Acquisition
### *(10 minutes)*

---

## Mini-Case: TechStart E-commerce

> **Situation:** TechStart sees a 15% cart abandonment spike this month.
> At the same time, a new paid social campaign launched targeting first-time visitors.
>
> The VP of Marketing says: "The campaign is bringing in low-quality traffic."
> The VP of Product says: "The new checkout flow is broken on mobile."

**Think (3 min):** Which analysis would you use first — Funnel or Channel Attribution? Why?

<!--
INSTRUCTOR NOTE:

**Background:** This mini-case tests whether students can pick the right analysis for the situation. The two competing hypotheses (traffic quality vs. checkout bug) require different analyses to resolve. Funnel analysis with segmentation is the right first step — it can show whether the problem is concentrated in paid social traffic OR in mobile checkout across all channels.

**Key point:** Funnel first, segmented. This untangles whether it's a traffic problem or a checkout problem.

**Say something like:**
"Take 3 minutes to think about this. Work with your neighbor.

Two competing hypotheses. VP of Marketing blames traffic quality — the new campaign is bringing in people who were never going to convert. VP of Product blames the checkout — something's broken on mobile.

Your job: which analysis do you use first? Funnel or Channel Attribution? And how would you use it to decide who's right?

[Give them 3 minutes]

[After 3 minutes, cold call]

'[Name], what analysis would you start with?'"

**The right answer:**
Start with Funnel Analysis, segmented two ways:
1. Segment by traffic source (paid social vs. other)
2. Segment by device (mobile vs. desktop)

If paid social has worse conversion at EVERY step (not just checkout), it's probably traffic quality.
If mobile has worse conversion at the CHECKOUT step across ALL channels, it's probably a checkout bug.
If ONLY paid social on mobile has the problem, it might be both — or there's an interaction to investigate.

**Follow-up questions to ask:**
- "What data would you need?"
- "What if both VPs are partially right?"
-->

---

## Mini-Case: Discussion

**Key questions to consider:**

1. How would Funnel Analysis help you here?
2. How would Channel Attribution help you here?
3. What if both are right — how do you untangle the effects?
4. What data would you need to decide?

<!--
INSTRUCTOR NOTE:

**Background:** This is the discussion portion of the mini-case. Cold-call 2-3 students to get them thinking actively. The case tests whether they can apply both funnel analysis and attribution concepts, and more importantly, whether they can think about how analyses interact.

**Key point:** The answer depends on segmentation. You need to analyze the funnel BY traffic source to untangle whether it's a product problem or a traffic quality problem.

**Cold-call approach:**
Pick a student: "[Name], let's start with you. How would funnel analysis help here?"

**Looking for in answers:**
1. Funnel Analysis: "Build a funnel of the checkout flow, see WHERE the drop-off is concentrated"
2. Attribution: "Look at which channels are driving cart additions vs. which are abandoning"
3. Both right: "Segment the funnel BY traffic source — if mobile checkout drops for ALL channels, it's Product. If only paid social abandons, it's campaign quality."
4. Data needed: "user_id, timestamp, event_type (funnel events), source (channel), device"

**Say something like:**
"Let's discuss this. [Pick student] — how would funnel analysis help here?"

[After their answer]

"Good. Now here's the key question: what if BOTH the VP of Product AND VP of Marketing are partially right? How would you untangle that?"

[Looking for: segment the funnel by traffic source]

"Exactly. If you see mobile checkout drop-offs across ALL traffic sources, it's probably the checkout UX — a product problem. If you see high cart additions from paid social but then those specific users abandon at higher rates than other channels — it's traffic quality, a marketing problem.

The data you need: user_id to link events, timestamp for sequencing, event_type for the funnel steps, source to segment by channel, and device to test the mobile hypothesis."

**If no one gets it:**
"Let me give you a hint. What happens if you build TWO funnels — one for paid social traffic only, one for all other traffic? What would different patterns tell you?"

**Transition:** "Alright, let's take a quick break before we dive into some heavier statistical concepts..."
-->

---

## ☕ Quick Stretch
### 3 minutes

Stand up. Check your phone. Campaign Effectiveness is next — and it introduces some important statistical concepts.

---

<!-- _class: lead -->

# Part 3: Campaign Effectiveness Analysis
### *(22 minutes)*

---

## A Quick Prerequisite: The "What If" Problem

> You take medicine and your headache goes away. How do you know the medicine worked?

**The answer:** You can't — it might have gone away on its own.

This is the core challenge of **causal inference**.

<!--
INSTRUCTOR NOTE:

**Background:** This is the philosophical foundation for campaign effectiveness analysis. Many students (and professionals) conflate correlation with causation. The medicine example is intuitive and non-threatening — it's not about their work, so they can think clearly about the logic before applying it to marketing.

**Key point:** Correlation is not causation. To claim causation, you need a counterfactual.

**Say something like:**
"Before we talk about measuring campaign effectiveness, I need to introduce a concept that underpins everything: the 'What If' problem.

Here's a simple example. You have a headache. You take medicine. The headache goes away. Question: how do you know the medicine worked?

[Pause for answers]

The honest answer is: you don't. Maybe the medicine worked. Maybe the headache would have gone away on its own. Maybe you also drank water and that helped. Maybe you were stressed and then relaxed. You observed ONE outcome — headache gone — but you needed to compare it to a world where you didn't take the medicine. That world doesn't exist. You can't observe it.

This is the fundamental challenge of causal inference. In marketing: you ran a campaign and sales went up. Did the campaign cause the sales increase? Or would sales have gone up anyway? You can't directly observe the world where you didn't run the campaign."

**If asked:** "Can't we just compare to last year?"
A: That's one approach, but it assumes this year would have looked like last year without the campaign. New stores, economy, competitors — lots of things change. Year-over-year comparisons are a rough proxy, not a true counterfactual.

**Transition:** "Let me be more precise about what I mean by counterfactual..."
-->

---

## What is a Counterfactual?

A **counterfactual** is: *"What would have happened if we hadn't done X?"*

**The Twin Study Analogy:**
- Twin A takes drug → better in 3 days
- Twin B takes placebo → better in 5 days
- Difference (2 days) = **causal effect**

**The problem in marketing:** We don't have twins. We must *construct* a comparison group.

<!--
INSTRUCTOR NOTE:

**Background:** The counterfactual is the central concept in causal inference. The twin study analogy makes it concrete: if you had an identical twin who did everything the same except take the medicine, you could measure the true causal effect. In marketing, we don't have twins — we have to construct comparison groups that approximate what would have happened without the treatment.

**Key point:** A counterfactual is the hypothetical outcome if we hadn't intervened. We can't observe it directly — we have to estimate it.

**Say something like:**
"Let me give you a mental model for counterfactuals: the twin study.

Imagine you have an identical twin. Same genetics, same life, same everything. You both get a headache at the same moment. You take medicine, your twin takes a placebo. You feel better in 3 days, your twin in 5 days.

The difference — 2 days — is the causal effect of the medicine. You know it's causal because your twin controlled for everything else.

Now here's the problem in marketing: we don't have twins. We ran a campaign in all markets. We can't observe the parallel universe where we didn't run it.

So we have to construct a comparison group — a 'control twin' — that approximates what would have happened without the campaign. That's what the next few slides are about: different methods for building your control twin."

**If asked:** "Isn't year-over-year comparison good enough?"
A: It's a rough proxy, but assumes this year would look like last year. In reality, economy, competition, your own growth rate, seasonality — many things change. YoY is convenient but not a true counterfactual.

**Transition:** "Let me show you three ways to build a control twin..."
-->

---

## Three Ways to Build a "Control Twin"

**Randomized Holdout** — Randomly assign some markets to get no campaign
*Gold standard. Requires advance planning.*

**Geo-Matching** — Find naturally similar markets
*When randomization wasn't possible.*

**Synthetic Control** — Build weighted "twin" from multiple markets
*When no single market is a good match.*

**All three answer:** What would have happened without the campaign?

**Key insight:** The quality of your causal estimate depends entirely on how good your "control twin" is.

<!--
INSTRUCTOR NOTE:

**Background:** These three methods form a hierarchy of rigor. Randomized holdout is best but requires planning ahead. Geo-matching is common but risky — markets may differ in unobservable ways. Synthetic control is sophisticated but data-intensive. Students should understand when each is appropriate.

**Key point:** The quality of your causal estimate depends on how good your "control twin" is.

**Say something like:**
"There are three main ways to build a control twin, and they form a hierarchy of rigor.

Randomized holdout is the gold standard. Before the campaign, you randomly assign some markets to not receive it. Because assignment is random, any difference you see afterward is causal. But this requires advance planning — if the campaign already ran everywhere, it's too late.

Geo-matching is what you do when you didn't plan ahead. You find markets that look similar — maybe Phoenix and Tucson have similar demographics and growth trends — and use one as control. The risk: 'similar' on observables doesn't mean similar on unobservables.

Synthetic control is more sophisticated. When no single market is a good match, you create a weighted combination of multiple markets that together match your treated market's pre-campaign trajectory. It's powerful but requires more data and expertise.

All three answer the same question: what would have happened without the campaign? But they answer it with different levels of confidence.

The key insight: your causal estimate is only as good as your control twin. Garbage control = garbage estimate."

**If asked:** "Which method should I use?"
A: Randomized holdout if you can plan ahead. Geo-matching for quick analysis when holdout wasn't done. Synthetic control when you have data but no good single control market.

**Transition:** "Let me show you the fundamental question we're trying to answer..."
-->

---

## The Fundamental Question

> **Did the campaign cause the sales, or would they have happened anyway?**

Sales went up 12% during the campaign. But:
- Economy improved
- Competitor had a bad quarter
- It was holiday season
- New stores opened

**Correlation is easy. Causation is hard.**

<!--
INSTRUCTOR NOTE:

**Background:** This slide crystallizes the causal inference problem in a business context. Students often assume that if sales went up during a campaign, the campaign worked. The list of alternative explanations (economy, competitor, holiday, new stores) should make them uncomfortable — all of these could explain the sales increase without the campaign doing anything.

**Key point:** Many factors affect sales simultaneously. Without controlling for them, you cannot isolate the campaign's effect.

**Say something like:**
"Here's the fundamental question of campaign effectiveness: did the campaign cause the sales, or would they have happened anyway?

Sales went up 12% during the campaign. The marketing team is celebrating. But look at these confounders:

The economy improved — people have more money to spend. A competitor had a bad quarter — their loss was your gain. It was holiday season — people buy more during holidays anyway. New stores opened — more stores, more sales.

Any of these could explain the 12% increase. Maybe ALL of them together explain it, and the campaign contributed nothing. Or maybe the campaign drove an additional 8% on top of what would have happened naturally.

You cannot tell which is true just by looking at sales during vs. before the campaign. That comparison is correlation. To establish causation, you need to estimate what would have happened without the campaign and compare to that. That's hard."

**If asked:** "So we can never know if marketing works?"
A: You CAN know — with proper experimental design. Holdout tests, geo-experiments, synthetic controls. But you have to do the work. The naive 'sales went up' comparison tells you almost nothing.

**Transition:** "Let me show you a real scenario where this matters..."
-->

---

## Why This Matters

**Scenario:** You spent $18M on holiday marketing. Sales were up $45M vs. last year.

**CMO says:** "We drove $45M! That's 2.5x ROI!"

**CFO asks:** "Would sales have been up $30M anyway due to new stores and economy? So marketing only drove $15M — less than 1x ROI."

**Who's right?** You need to estimate the **counterfactual** — what would have happened without the campaign.

<!--
INSTRUCTOR NOTE:

**Background:** This CMO vs CFO scenario is a common real-world tension. CMOs often claim full credit for sales increases (correlation), while CFOs question how much was truly incremental (causation). The gap between $45M and $15M is the difference between a successful campaign and a budget cut. This frames why counterfactual estimation matters.

**Key point:** The difference between CMO's claim and CFO's skepticism is the counterfactual. This isn't an academic debate — it's budget on the line.

**Say something like:**
"Let me make this concrete with a scenario that happens in companies every quarter.

You're the analyst. The CMO shows you this slide at the year-end review. 'We spent $18M on holiday marketing. Sales were up $45M. That's 2.5x ROI! Marketing is killing it! Give me more budget!'

The CFO is skeptical. 'Hold on. We opened 50 new stores this year. The economy was strong. Competitors had supply chain issues. Would sales have been up anyway? If sales would have been up $30M without marketing, then marketing only drove $15M — and $15M from $18M spend is less than 1x ROI. We should cut the budget.'

[Pause]

Who's right? You literally cannot answer this question without estimating the counterfactual. What would sales have been if we hadn't run the campaign?

That's the fundamental question of campaign effectiveness. And it determines whether marketing gets more budget or gets cut. The stakes are real."

**If asked:** "Can't we just run without marketing for a quarter and see?"
A: That's actually the best answer — a holdout test. But it requires planning ahead, and CFOs are often reluctant to leave money on the table. We'll cover how to set these up.

**Transition:** "Let me visualize what a counterfactual looks like..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_02_counterfactual.png)

---

## The Counterfactual Problem

You can never directly observe what would have happened if you hadn't run the campaign.

You have to **estimate** the counterfactual using control groups or statistical models.

<!--
INSTRUCTOR NOTE:

**Background:** This is the philosophical core of the problem. The counterfactual is fundamentally unobservable — you cannot see what would have happened in a parallel universe. All of our methods (holdout tests, geo-matching, synthetic control) are ways of ESTIMATING the counterfactual, not observing it directly. This epistemological point matters because it means all causal estimates have uncertainty.

**Key point:** The counterfactual is unobservable. Every causal estimate is an approximation with uncertainty.

**Say something like:**
"Let me be philosophically precise for a moment. The counterfactual is fundamentally unobservable.

You ran the campaign in all markets. What would have happened if you hadn't? You can never directly observe that world — it doesn't exist. There's no way to rewind time, not run the campaign, and see what happens.

So every method we use — holdout tests, geo-matching, synthetic control — is trying to ESTIMATE what that unobservable counterfactual would have been. We're not measuring it. We're approximating it.

This matters because it means every causal estimate comes with uncertainty. Even the best randomized holdout test gives you an estimate plus or minus some confidence interval. The further you get from randomization, the more uncertainty you have.

When someone says 'the campaign drove $15M,' the honest way to say it is 'our best estimate of the incremental effect is $15M, with a 95% confidence interval of $10M to $20M.' That's less punchy in a presentation, but it's accurate."

**If asked:** "If we can never know for sure, why bother?"
A: Because imperfect estimates are infinitely better than no estimates. The alternative is claiming credit for everything (CMO) or nothing (CFO) — both are wrong. Causal inference gives you a principled middle ground.

**Transition:** "Let me show you the gold standard method..."
-->

---

## Method 1: Randomized Holdout Test

**Gold standard.** Randomly select some markets/users to NOT see the campaign.

| Group | What They See | Size |
|-------|--------------|------|
| **Treatment** | Full campaign | 90% of markets |
| **Control (Holdout)** | No campaign | 10% of markets |

**After campaign:**
```
Incremental Effect = Treatment Sales - Control Sales
```

**Why it works:** Random assignment ensures groups are comparable. Any difference is caused by the campaign.

<!--
INSTRUCTOR NOTE:

**Background:** Randomized holdout tests are the gold standard for causal inference in marketing. By randomly assigning some markets to receive no campaign, you create a true control group. Any difference between treatment and control is caused by the campaign — not confounders. The challenge is convincing stakeholders to "leave money on the table" by not marketing to 10% of markets.

**Key point:** Randomization is gold standard because it eliminates confounders. The cost is leaving some markets untreated.

**Say something like:**
"Randomized holdout is the gold standard. If you can do it, do it.

Before the campaign launches, randomly select some markets — say 10% — to NOT see any campaign ads. These are your 'holdout' or control markets. The other 90% get the full campaign.

After the campaign, compare sales. Treatment markets minus control markets equals your incremental effect. Simple.

Why does this work? Random assignment. Because you assigned randomly, any difference you see can't be explained by 'well, those markets are different.' They're not systematically different — you made sure of that by randomizing.

The challenge: you have to plan ahead. If the campaign already ran everywhere, it's too late. And stakeholders hate holdouts — 'You want me to NOT market to 10% of my customers? That's money on the table!'

Your job is to help them see that without a holdout, they'll never know if the campaign worked at all. Better to prove 90% of spend works than to spend 100% and hope."

**If asked:** "How many markets should we hold out?"
A: Depends on power calculations, but typically 10-20%. Larger holdout = more precision but more 'lost' revenue. Run a power analysis to size it properly.

**Transition:** "When you can't randomize, here's your next best option..."
-->

---

## Method 2: Geo-Matched Markets

When you can't randomize, find markets that **look similar** before the campaign.

| Market | Pre-Campaign Trend | Campaign Spend |
|--------|-------------------|----------------|
| Phoenix | +5% YoY | $2M (heavy) |
| Tucson | +4% YoY | $0 (control) |

**Compare post-campaign:** Did Phoenix outperform Tucson more than expected?

**Risk:** "Similar" markets may differ in unobserved ways.

<!--
INSTRUCTOR NOTE:

**Background:** Geo-matching is the most common approach when holdouts weren't planned. You find markets with similar pre-campaign trends and use one as control. The danger is that "similar on observables" doesn't guarantee "similar on unobservables." Phoenix and Tucson might have different economic conditions, competitive landscapes, or customer demographics that you can't see in the data.

**Key point:** Geo-matching assumes that markets similar on observables will behave similarly. This assumption can be wrong.

**Say something like:**
"When you didn't plan a holdout — and this is the common case — geo-matching is your next option.

The idea: find markets that looked similar before the campaign. Phoenix and Tucson both grew about 5% year-over-year. Phoenix got heavy campaign spend, Tucson got none. If Phoenix grows 15% during the campaign while Tucson grows 5%, maybe the campaign drove that extra 10%.

The logic is reasonable. But here's the risk: 'similar' on the things you can measure doesn't mean similar on things you can't measure.

Maybe Phoenix has a new tech company that just opened an office there — you don't know that, but it's driving growth. Maybe Tucson's main employer just announced layoffs. These unobserved factors will confound your estimate.

Geo-matching is better than nothing, but always acknowledge the assumption. Your estimate is valid IF similar pre-trends mean similar counterfactual trends. That's a big IF."

**If asked:** "How do I pick good matched markets?"
A: Match on as many observables as you can — growth rate, demographics, store count, competitive landscape. The more similar on observables, the more plausible that unobservables are also similar.

**Transition:** "When no single market is a good match, there's a more sophisticated option..."
-->

---

## Method 3: Synthetic Control

**Build a "fake" control from weighted combination of real controls.**

You're measuring Phoenix (treated). You have 10 other cities as potential controls.

Algorithm finds weights: Phoenix ≈ 0.4×Denver + 0.3×Austin + 0.2×Portland + 0.1×Salt Lake

The weighted combination matches Phoenix's pre-campaign trend.

**Post-campaign:** Compare Phoenix to the synthetic Phoenix.

<!--
INSTRUCTOR NOTE:

**Background:** Synthetic control is a sophisticated method from econometrics (Abadie, Diamond, Hainmueller 2010). When no single market is a good control, you create a weighted combination of markets that together replicate the treated market's pre-treatment trajectory. This is powerful but requires good pre-period data and statistical expertise.

**Key point:** When no single control works, create a weighted combination that matches pre-campaign trends. The method is powerful but requires expertise and good data.

**Say something like:**
"What if no single market is a good match for Phoenix? Tucson is smaller, Denver has different weather, Austin has different demographics. None of them alone are good controls.

Synthetic control solves this. Instead of picking one control market, you create a 'synthetic Phoenix' from a weighted combination of multiple markets.

The algorithm finds weights that make the synthetic Phoenix track real Phoenix as closely as possible BEFORE the campaign. Maybe 40% Denver, 30% Austin, 20% Portland, 10% Salt Lake together look like Phoenix.

If the synthetic Phoenix tracks real Phoenix well before the campaign, you have a credible counterfactual. After the campaign, the gap between real and synthetic Phoenix is your causal estimate.

This is more sophisticated than simple geo-matching. It's been used to estimate the effects of policies — California smoking regulations, German reunification, Brexit. But it requires solid pre-period data and statistical expertise to implement properly."

**If asked:** "What software implements this?"
A: Python's CausalPy or R's Synth package. Google also has open-source implementations. It's not plug-and-play — you need to understand the assumptions.

**Transition:** "Let me show you what the output looks like..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_02_synthetic_control.png)

---

## Reading Synthetic Control

The lines track together before the campaign.
The gap after = causal effect estimate.

---

## The Data You Need

| Data | Granularity | Why |
|------|-------------|-----|
| **Sales** | Market × Day/Week | Outcome variable |
| **Marketing spend** | Market × Day/Week | Treatment variable |
| **Pre-period trend** | 6-12 months before | Match controls |
| **Market characteristics** | Demographics, stores | Improve matching |

**Key requirement:** You need variation in spend across markets. If all markets got the same campaign, you can't estimate incrementality.

<!--
INSTRUCTOR NOTE:

**Background:** Students need to understand what data infrastructure is required for campaign effectiveness analysis. The key insight is variation — you need some markets to have been treated differently than others. If everyone got the same campaign, there's no control to compare to. This is why planning matters.

**Key point:** You need variation in spend across markets. Same campaign everywhere = no control = no causal estimate.

**Say something like:**
"Let me tell you what data you need to do this analysis properly.

Sales by market and time — this is your outcome. You need it at a granular level so you can see weekly or daily changes.

Marketing spend by market and time — this is your treatment variable. You need to know which markets got how much campaign exposure.

Pre-period trend — 6-12 months before the campaign. This is what you use to match markets or build synthetic controls. Without good pre-period data, you can't assess whether your controls are valid.

Market characteristics — demographics, store count, competitive landscape. These help you match more precisely and check for confounders.

But here's the critical requirement: you need VARIATION in spend. If all 50 markets got the exact same campaign with the same intensity, you have no control. Everyone was treated the same. You cannot estimate incrementality.

This is why the holdout matters. If you planned ahead and held out 10%, you have variation. If you ran the same campaign everywhere, you're stuck with year-over-year comparisons and their limitations."

**If asked:** "What if we always run the same campaign everywhere?"
A: Push for holdouts going forward. For past campaigns, you're limited to time-based comparisons (before/after, year-over-year) which have more confounders.

**Transition:** "Now let me show you how to interpret the results..."
-->

---

## Interpreting Results

Output looks like:

| Metric | Estimate | 95% CI |
|--------|----------|--------|
| Incremental Revenue | $42M | $28M - $56M |
| Campaign Spend | $18M | — |
| Incremental ROI | 2.3x | 1.6x - 3.1x |

**Critical:** Report confidence intervals, not just point estimates.

If CI includes 1x (or below), you can't confidently say campaign was profitable.

<!--
INSTRUCTOR NOTE:

**Background:** Confidence intervals are crucial for campaign effectiveness because they capture uncertainty. A point estimate of 2.3x ROI sounds great, but if the CI is 1.6x to 3.1x, you still might have lost money at the lower bound. Many executives only want to see the point estimate; your job is to insist on intervals.

**Key point:** Always report confidence intervals. A point estimate without uncertainty is a lie of omission.

**Say something like:**
"Let me show you how to read and present campaign effectiveness results.

[Point to table]

Point estimate: $42M incremental revenue, $18M spend, 2.3x ROI. Sounds great!

But look at the confidence interval: $28M to $56M. The 95% CI for ROI is 1.6x to 3.1x.

Why does this matter? At the lower bound — 1.6x — the campaign is still profitable but barely. At 2.3x it's clearly profitable. At 3.1x it's fantastic. You don't know which is true.

Here's the rule: if the CI includes 1x or below, you can't confidently say the campaign was profitable. The uncertainty is too large.

Many executives will want you to just show them the point estimate. 'Just tell me the ROI.' Your job is to push back. 'The ROI is 2.3x, but the uncertainty ranges from 1.6x to 3.1x. We're confident it was profitable, but the magnitude is uncertain.'

Point estimates without confidence intervals are a form of dishonesty. They make you look more certain than you are."

**If asked:** "How do I get tighter confidence intervals?"
A: More data (longer campaign, more markets) or better experimental design. The holdout size matters — bigger holdouts give more precision.

**Transition:** "Now let me warn you about common pitfalls..."
-->

---

## Common Pitfalls

- **Control contamination** — Control sees treatment ads → geographic buffers
- **Selection bias** — Best markets get campaign → randomize or match
- **Pull-forward** — Sales spike then drop → measure full period
- **Competitor confound** — Competitor enters control → validate matching

<!--
INSTRUCTOR NOTE:

**Background:** These four pitfalls represent the most common ways campaign effectiveness analyses go wrong. Each has a specific diagnostic and fix. Control contamination is especially common with digital advertising where targeting isn't perfectly geographic.

**Key point:** Each pitfall can invalidate your causal estimate. Know how to detect and prevent each one.

**Say something like:**
"Let me walk you through the four ways these analyses most commonly fail.

Control contamination: Your 'control' markets still saw the ads. This happens with digital advertising — someone from your control market visits a treatment market and sees the campaign on their phone. Now they're contaminated. The fix: use geographic buffers, analyze at larger regional levels, or use platform-level targeting that's more precise.

Selection bias: The best markets got the campaign, underperforming markets were 'held out.' Now your treated markets outperform for reasons that have nothing to do with the campaign — they were already better. The fix: randomize or match carefully on pre-period trends.

Pull-forward: The campaign spiked sales during the campaign period, but it was just pulling forward purchases that would have happened anyway. Post-campaign sales drop, and net effect is zero. The fix: measure the full period including post-campaign to see if gains persist.

Competitor confound: A competitor launches a big promotion in your control markets during the campaign period. Now your control looks worse, making your treatment look better. The fix: validate that nothing unusual happened in control markets during the test.

Each of these can completely invalidate your estimate if you don't catch them."

**If asked:** "How do I check for control contamination?"
A: Look at advertising platform data for reach in control markets. If it's not near zero, you have contamination. Also survey control market customers about brand awareness.

**Transition:** "Let me show you one of these pitfalls in detail..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_02_pull_forward.png)

---

## Pull-Forward: The Hidden Trap

**The question:** Did the campaign create NEW customers, or convince existing customers to buy earlier?

**Always check:** Compare campaign period + post-period to same timeframe last year.

<!--
INSTRUCTOR NOTE:

**Background:** Pull-forward is one of the most common traps in campaign analysis. A promotion causes a spike during the campaign period, but sales drop afterward as people who would have bought anyway already made their purchase. The "incremental" lift is actually just time-shifted demand, not new demand. Holiday campaigns and promotional periods are especially susceptible.

**Key point:** Measure beyond the campaign period. A spike followed by a drop is pull-forward, not true incrementality.

**Say something like:**
"Here's a trap that catches even experienced analysts: pull-forward.

You run a campaign. Sales spike 30% during the campaign period. Everyone celebrates. But then the next month, sales drop 20% below normal.

What happened? You didn't create new demand. You pulled forward demand that was going to happen anyway. People who would have bought next month bought this month instead because of the promotion.

From a campaign measurement perspective, your 'incremental' revenue is much smaller than it looked — maybe even negative once you factor in the discount you gave.

This is especially common with holiday promotions, sales, and limited-time offers.

The fix: always measure beyond the campaign period. Compare campaign period PLUS post-period to the same timeframe last year. If the total is the same but it shifted earlier, that's pull-forward."

**If asked:** "How long should the post-period be?"
A: Depends on purchase frequency. For consumer goods bought monthly, measure at least 2-3 months after. For annual purchases, you might need to wait a full year.

**Transition:** "Let me show you a realistic scenario..."
-->

---

## The BrightMart Scenario

**Company:** BrightMart (national retailer)
**Problem:** Spent $18M on holiday marketing. Sales up 12% YoY.
**Question:** How much was marketing vs. external factors?

**Stakeholder complexity:**
- CFO: Skeptical (burned by past campaign overspend)
- CMO: Advocate (budget depends on proving effectiveness)
- Agency: Worried (low ROI threatens $5M contract)

<!--
INSTRUCTOR NOTE:

**Background:** This scenario explicitly calls out the stakeholder dynamics that make campaign effectiveness politically charged. The CFO was burned before (distrust), the CMO's budget is on the line (high stakes), and the agency has a $5M contract at risk (external blocker). The analysis isn't just technical — it's navigating these competing interests.

**Key point:** Campaign effectiveness analysis exists in a politically charged environment. Every stakeholder has incentives that affect how they'll receive your findings.

**Say something like:**
"Notice the stakeholder complexity here. This isn't a clean analytical problem — it's a political minefield.

The CFO is skeptical. They've been burned before by marketing claiming credit for things that would have happened anyway. They're going to scrutinize your methodology.

The CMO is an advocate — but not objectively. Their budget for next year depends on proving this year's spend was effective. They WANT you to find high ROI.

And the agency has $5M at risk. If you find low ROI, their contract could get cut. They're going to push back on any analysis that makes them look bad.

So you're the analyst. Who do you please? The answer: none of them. You please the truth. But you need to anticipate these dynamics and have bulletproof methodology. When the CFO attacks your controls, you need to be ready. When the agency questions your data sources, you need to be ready.

This is why we spend so much time on methodology. In a politically charged environment, rigorous methods are your shield."

**If asked:** "How do you handle conflicting stakeholders?"
A: Be transparent about methodology, present uncertainty honestly, and let the data speak. Don't shade results for any stakeholder. Your credibility depends on being objective.

**Transition:** "Let's see what can go wrong in the pre-mortem..."
-->

---

## BrightMart: Pre-Mortem

> We proved 2.8x ROI and CMO was thrilled.
>
> But CFO's team found our "control" markets had a new competitor (ValueMart) enter during the campaign — artificially depressing their sales and inflating our incrementality.
>
> When re-run with proper controls, ROI dropped to 1.4x.
>
> **Lesson:** Validate control market selection rigorously before running analysis.

<!--
INSTRUCTOR NOTE:

**Background:** This pre-mortem illustrates the "competitor confound" pitfall in action. The control markets looked fine on historical data, but something changed during the test period. The entry of ValueMart into control markets depressed their sales, making the treatment markets look artificially good by comparison.

**Key point:** Control market validation isn't just about the past — you need to verify nothing changed during the test period itself.

**Say something like:**
"Let's walk through this pre-mortem. You proved 2.8x ROI — that's fantastic. The CMO is thrilled. Budget secured. Everyone's happy.

But the CFO's team does their own analysis. They discover something: ValueMart — a new competitor — entered your control markets during the campaign period.

What does that mean? Your control markets' sales dropped — not because they weren't getting your campaign, but because a new competitor was stealing market share. Your treatment markets look great by comparison, but it's not because your campaign was amazing. It's because your controls got worse for external reasons.

When you re-run the analysis excluding contaminated controls, ROI drops from 2.8x to 1.4x. Still positive, still justifiable, but a very different story.

The lesson: control market validation isn't just about historical similarity. You need to verify that nothing unusual happened to your controls DURING the test. New competitors, weather events, local economic shifts — any of these can confound your results.

Check during-period control validity, not just pre-period matching."

**If asked:** "How would you catch this before presenting?"
A: Monitor news, check for unusual sales patterns in control markets, look for explanatory variables beyond your campaign. Treat it like a scientific experiment where you're looking for confounds.

**Transition:** "Let's summarize what we've learned about campaign effectiveness..."
-->

---

## Campaign Effectiveness: Key Takeaways

1. **Correlation ≠ causation** — "sales went up" doesn't mean campaign worked
2. **You need a counterfactual** — what would have happened without campaign
3. **Randomized holdouts are gold standard** — plan them into future campaigns
4. **Synthetic control for observational** — when you can't randomize
5. **Check for pull-forward** — measure beyond campaign period
6. **Report confidence intervals** — point estimates alone are misleading

<!--
INSTRUCTOR NOTE:

**Background:** This summary captures the essence of campaign effectiveness analysis. The first point is the most important philosophical shift — students often conflate correlation with causation. The remaining points are practical guidance for doing the analysis correctly.

**Key point:** The fundamental lesson is that correlation isn't causation. Everything else follows from taking that seriously.

**Say something like:**
"Six takeaways from campaign effectiveness.

One: Correlation is not causation. This is the foundation. 'Sales went up during the campaign' tells you almost nothing about whether the campaign worked.

Two: You need a counterfactual. The question isn't 'what happened?' but 'what would have happened WITHOUT the campaign?' That's the comparison that matters.

Three: Randomized holdouts are gold standard. If you can plan ahead, hold out some markets. Random assignment eliminates confounders.

Four: When you can't randomize, synthetic control is your best observational method. Build a weighted control from multiple markets.

Five: Check for pull-forward. The campaign might spike sales during the campaign period, but those sales might have happened anyway in the next month. Measure beyond the campaign period.

Six: Report confidence intervals. A point estimate of 2.3x ROI sounds great. But if the CI is 0.8x to 3.8x, you don't actually know if the campaign was profitable. Uncertainty matters."

**Transition:** "Now let's talk about the fundamental question of unit economics..."
-->

---

<!-- _class: lead -->

# Part 4: CAC/LTV Analysis
### *(18 minutes)*

---

## The Unit Economics Question

> **"Does a customer generate more value than they cost to acquire?"**

This is the foundation of sustainable growth.

If LTV > CAC: You can scale profitably
If LTV < CAC: Growth makes you poorer
If LTV ≈ CAC: You're running on a treadmill

<!--
INSTRUCTOR NOTE:

**Background:** Unit economics became prominent during the 2010s tech boom when many startups grew at all costs, only to discover their customers weren't profitable. WeWork, Uber, and many others had terrible unit economics masked by growth. The 2022 market correction made CAC/LTV analysis suddenly important to investors and executives.

**Key point:** Growth without profitable unit economics is just burning money faster.

**Say something like:**
"This might be the most important question in business analytics: Does a customer generate more value than they cost to acquire?

If the answer is yes — LTV greater than CAC — you can scale profitably. Spend more on acquisition, get more customers, make more money. A virtuous cycle.

If the answer is no — LTV less than CAC — growth makes you poorer. Every new customer loses money. The more you grow, the more you lose.

And if they're roughly equal — you're on a treadmill. Running hard, going nowhere.

A lot of tech companies learned this the hard way in 2021-2022. They'd grown at all costs, raised funding based on growth rates, and then discovered their customers weren't actually profitable. [Pause] Some of those companies don't exist anymore.

Your job as an analyst is to answer this question honestly — even when the answer is uncomfortable."

**If asked:** "What's a good LTV:CAC ratio?"
A: Depends on the business. SaaS benchmarks are 3:1 or higher. E-commerce is often 2:1 to 3:1. The 'good' number depends on your cash flow needs and competitive dynamics.

**Transition:** "Let me define these terms precisely..."
-->

---

## Definitions

**CAC** = Total Acquisition Cost / Customers Acquired
*How much you pay per customer*

**LTV** = Revenue × Margin × Lifespan
*How much a customer is worth*

**LTV:CAC** = LTV / CAC → Profitability ratio

**Payback** = CAC / Monthly Revenue → Months to recover

**Benchmarks:** SaaS > 3:1, E-commerce > 2:1

<!--
INSTRUCTOR NOTE:

**Background:** These four definitions are the foundation of unit economics. CAC and LTV are the two core numbers; LTV:CAC ratio and payback period are derived metrics that investors and CFOs care about. The benchmarks (3:1 for SaaS, 2:1 for e-commerce) are rough guidelines — actual targets depend on business model, growth stage, and competition.

**Key point:** Four definitions to memorize. CAC and LTV are the inputs; LTV:CAC ratio and payback are the derived outputs.

**Say something like:**
"Let me give you four definitions you'll use for the rest of your career.

CAC — Customer Acquisition Cost. Total money spent acquiring customers divided by number of customers acquired. How much you pay per customer.

LTV — Lifetime Value. Revenue times margin times customer lifespan. How much a customer is worth to you.

LTV:CAC ratio — LTV divided by CAC. This is the profitability ratio. If it's above 1, you make money. Below 1, you lose money.

Payback — CAC divided by monthly revenue. How many months until you recover the cost of acquiring a customer.

[Point to benchmarks]

For SaaS, you want LTV:CAC above 3:1. For e-commerce, above 2:1 is often acceptable because transactions are more frequent.

Why is SaaS higher? Because SaaS has high upfront costs and subscription revenue comes in slowly. You need more cushion. E-commerce gets cash faster.

These are rough benchmarks. Your actual target depends on your competition, your growth stage, and your margin structure."

**If asked:** "What if we're a startup with no historical data for LTV?"
A: You'll need to project based on early cohort data or industry benchmarks. Be conservative and explicit about assumptions.

**Transition:** "Let me show you how to calculate CAC properly — most companies get it wrong..."
-->

---

## Calculating CAC: "Fully Loaded"

**Don't just count media spend.** Include everything:

| Cost Type | Example | Often Forgotten? |
|-----------|---------|-----------------|
| Media spend | $500K Google Ads | No |
| Creative production | $50K video shoot | Sometimes |
| Agency fees | $100K retainer | Sometimes |
| Team salaries | $200K (portion of 4 people) | **Often** |
| Tools & software | $30K attribution tool | **Often** |

**Fully loaded CAC = ($500K + $50K + $100K + $200K + $30K) / 1,000 customers = $880**
vs. just media: $500

<!--
INSTRUCTOR NOTE:

**Background:** Most companies understate CAC by only counting media spend. "Fully loaded" CAC includes all costs of acquiring customers: media, creative, agency fees, team salaries, tools. The difference can be dramatic — in this example, $880 fully loaded vs. $500 media-only. This matters for unit economics and profitability analysis.

**Key point:** Fully loaded CAC includes all costs, not just media spend. The difference can be 50%+ higher than naive calculations.

**Say something like:**
"When you calculate CAC, don't just count media spend. That's the most common mistake.

Look at this table. Media spend is $500K — that's what shows up in Google Ads or Meta's dashboard. But what else did you pay for?

Creative production: the video shoot cost $50K. Agency fees: you pay a retainer. Team salaries: you have 4 people working on paid acquisition — some portion of their salary is acquisition cost. Tools: that attribution software isn't free.

Add it all up: $880K total for 1,000 customers = $880 CAC.

If you only counted media spend: $500K / 1,000 = $500 CAC.

That's a 76% difference! If your LTV is $750, you think you're profitable at $500 CAC but you're actually underwater at $880.

When your Brief asks for CAC, specify 'fully loaded.' And when you read someone else's CAC claims, ask what's included."

**If asked:** "How do I allocate team salaries to acquisition?"
A: Estimate the percentage of time spent on acquisition activities. If 50% of the marketing team's time is acquisition, allocate 50% of salaries. It's imprecise but better than ignoring it.

**Transition:** "Let's break this down by channel..."
-->

---

## CAC by Channel

Break down by acquisition source:

| Channel | Spend | Customers | CAC |
|---------|-------|-----------|-----|
| Paid Social | $300K | 400 | $750 |
| Paid Search | $400K | 800 | $500 |
| Organic/SEO | $100K* | 600 | $167 |
| Referral | $50K | 300 | $167 |

*Content team salaries allocated

**Insight:** Organic and referral are 3-4x more efficient than paid.

<!--
INSTRUCTOR NOTE:

**Background:** Channel-level CAC is essential for budget allocation. This example shows the common pattern: organic and referral have much lower CAC than paid channels. However, the caveat matters — we're only seeing CAC, not LTV. Cheap customers aren't always valuable customers. And channels aren't independent, as we'll see.

**Key point:** Break down CAC by channel. The aggregate hides important variation. But don't optimize on CAC alone — LTV matters too.

**Say something like:**
"Now let's break CAC down by channel. This is where it gets interesting.

[Walk through the table]

Paid Social: $300K spent, 400 customers, $750 CAC. Expensive.

Paid Search: $400K spent, 800 customers, $500 CAC. Better.

Organic/SEO: $100K — and notice the asterisk, that's content team salaries — 600 customers, $167 CAC.

Referral: $50K program cost, 300 customers, $167 CAC.

[Pause]

The insight jumps out: organic and referral are 3-4x more efficient than paid. $167 vs $500-750.

Now here's where executives get into trouble. They see this table and say: 'Let's cut paid and put everything into organic and referral!'

That's naive for two reasons. One: CAC isn't the whole picture. What if paid social customers have higher LTV? We'll look at that next.

Two: channels aren't independent. What if paid social is how people first hear about you, and then they come back organically later? Cutting paid might kill organic.

For now, just note: break down CAC by channel. The aggregate lies to you."

**Transition:** "Let me show you how LTV changes this picture..."
-->

---

## Calculating LTV: The Projection Problem

LTV requires predicting the future:
- How long will they stay? (Retention)
- What will they spend? (Revenue)
- What's your margin? (Profitability)

**Simple formula:**
```
LTV = ARPU × Gross Margin × Customer Lifespan
```

**Example:** $50/month × 70% margin × 24 months = **$840**

<!--
INSTRUCTOR NOTE:

**Background:** LTV calculation is fundamentally a projection problem — you're predicting the future. The simple formula is useful for back-of-envelope calculations but hides significant uncertainty. The three components (retention, revenue, margin) all require predictions.

**Key point:** LTV is a prediction, not a measurement. Every component involves uncertainty.

**Say something like:**
"LTV requires predicting the future. Let me break down the three components.

How long will they stay? That's retention. You have to predict when they'll churn.

What will they spend? That's revenue over time. Will they upgrade? Downgrade? Buy add-ons?

What's your margin? That's profitability. Not just revenue, but what you keep after costs.

The simple formula multiplies these together: ARPU times gross margin times customer lifespan.

Let's work an example. $50 per month average revenue. 70% gross margin — meaning you keep $35 after direct costs. Customer stays for 24 months on average. 50 times 70% times 24 equals $840 LTV.

But here's the catch: every one of those numbers is a prediction. Maybe retention declines. Maybe pricing changes. Maybe costs increase. The $840 is a point estimate with uncertainty around it.

When you present LTV, always acknowledge the uncertainty. 'Our LTV estimate is $840, but it could range from $700 to $1000 depending on retention trends.'"

**If asked:** "Should we use simple formulas or cohort analysis?"
A: Cohort analysis is more accurate but requires more data and patience. Simple formulas are good for quick estimates and sanity checks. Use both.

**Transition:** "Let me show you a more accurate approach using cohorts..."
-->

---

## Cohort-Based LTV: More Accurate

Track actual cohorts over time:

| Months Since Signup | Cohort Jan 2025 | Cohort Apr 2025 |
|--------------------|-----------------|-----------------|
| Month 1 | $50 | $45 |
| Month 3 | $145 | $130 |
| Month 6 | $270 | $235 |
| Month 12 | $480 | ??? |

For newer cohorts, **extrapolate** based on older cohort curves.

**Warning:** Extrapolation is guessing. Be conservative.

<!--
INSTRUCTOR NOTE:

**Background:** Cohort-based LTV tracking is more accurate than simple formulas because it measures actual user behavior over time. But it requires patience — you can only observe data you have. For newer cohorts, you extrapolate based on older cohorts' trajectories. This extrapolation is the source of most LTV calculation errors.

**Key point:** Cohort tracking is more accurate, but extrapolation is guessing. Always be conservative when projecting future LTV.

**Say something like:**
"Cohort-based LTV tracking is more accurate than simple formulas because you're measuring what users actually do, not what a formula predicts.

Look at this table. The January 2025 cohort has been around for 12 months, so we know their 12-month LTV: $480. The April cohort has only been around 6 months — we can see $235, but month 12 is a question mark.

To fill in that question mark, we extrapolate. If January cohort went from $270 at month 6 to $480 at month 12, that's a 78% increase. We might assume April cohort follows a similar curve: $235 × 1.78 = ~$418.

But here's the danger: extrapolation is guessing. Maybe April cohort came from a different marketing channel. Maybe the product changed. Maybe the economy shifted. Any number of things could make the future different from the past.

Rule of thumb: when projecting LTV, be conservative. If your optimistic projection says 3:1 LTV:CAC and your conservative projection says 1.8:1, plan for 1.8:1."

**If asked:** "How far out can we reasonably project?"
A: Depends on how much historical data you have and how stable the business is. Projecting 12 months from 6 months of data is reasonable. Projecting 36 months from 6 months is dangerous.

**Transition:** "Let me show you what these curves look like visually..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_02_ltv_curve.png)

---

## Reading LTV Curves

Early months are observed. Later months are projected.

The further you project, the more uncertain the estimate.

---

## Channel Economics: The Winners

| Channel | CAC | LTV | LTV:CAC | Payback |
|---------|-----|-----|---------|---------|
| Organic | $167 | $840 | **5.0x** | 3 mo |
| Referral | $167 | $920 | **5.5x** | 2 mo |

These channels are highly profitable. Low cost, high retention.

<!--
INSTRUCTOR NOTE:

**Background:** This slide shows what "good" channel economics look like. These numbers are realistic for subscription businesses — organic and referral typically have the best unit economics because customer acquisition cost is minimal. Students should internalize what healthy LTV:CAC ratios look like (3x+ is typically the benchmark).

**Key point:** Organic and referral channels usually have the best economics because CAC is so low, not because LTV is exceptionally high.

**Say something like:**
"Look at these numbers. Organic and referral have LTV:CAC ratios of 5x and 5.5x. These are excellent — above the 3x benchmark we typically target.

But notice something interesting. Their LTV isn't dramatically higher — $840 and $920. What makes them 'winners' is the CAC is so low — just $167. That's because you're not paying for ads to acquire these customers.

Organic means they found you through search or word of mouth. Referral means existing customers brought them in. In both cases, your main cost is just the operational cost of processing the signup, maybe a small referral bonus.

The payback period is also short — 2-3 months. That means you recoup your acquisition cost quickly and the rest is profit.

Every company dreams of channels like this. But here's the catch — they're usually not scalable. You can't just 'buy more organic traffic.' You have to earn it through content, SEO, product quality. So while these are the best channels, they're often not the ones you can grow on demand."

**If asked:** "What's a good LTV:CAC benchmark?"
A: 3x is the common benchmark for healthy SaaS/subscription businesses. Below 3x and you're spending too much to acquire customers. Above 5x means you might be under-investing in growth.

**Transition:** "Now let's look at the other end of the spectrum..."
-->

---

## Channel Economics: The Losers

| Channel | CAC | LTV | LTV:CAC | Payback |
|---------|-----|-----|---------|---------|
| Paid Search | $500 | $780 | 1.6x | 8 mo |
| Paid Social | $750 | $650 | **0.9x** | 14 mo |

Paid social is underwater (LTV < CAC over 12 months).

**But wait...** Are channels independent?

<!--
INSTRUCTOR NOTE:

**Background:** This slide sets up the channel interaction problem that follows. On paper, these channels look like clear candidates for cutting — especially paid social with a 0.9x LTV:CAC (losing money on every customer). The payback periods are also concerning. But the slide ends with a provocative question that should make students pause.

**Key point:** Don't rush to judgment. Channels that look bad in isolation may be serving a purpose the attribution system can't see.

**Say something like:**
"Now look at paid channels. Paid search is at 1.6x — below our 3x benchmark but at least profitable. But paid social? 0.9x. For every dollar we spend, we get back 90 cents. We're literally losing money on every customer we acquire.

The payback period is 14 months — which means it takes over a year to recoup the acquisition cost. For a subscription business that's concerning. A lot can go wrong in 14 months.

If you showed this table to a CFO, what would they say? 'Cut paid social. It's destroying value.'

And that's exactly what many companies do. They run this analysis, see the bad unit economics, and cut the underperforming channels.

But here's where I want you to pause. Look at that last line: 'Are channels independent?'

What if paid social isn't really about direct conversions? What if it's building brand awareness that drives organic and referral? What if cutting it tanks your overall growth even though its direct economics look bad?

This is the trap. Let me show you what happens when companies fall into it..."

**If asked:** "At what point should you cut a channel?"
A: Only after you've tested whether cutting it affects OTHER channels. Run a holdout test first — turn it off in some markets and measure total outcomes, not just that channel's attributed conversions.

**Transition:** "Let me show you why those last two lines matter so much..."
-->

---

## The Channel Interaction Problem

Channels don't work in isolation.

**Scenario:** You cut paid social because LTV:CAC is 0.9x.

What happens?
- Brand awareness drops
- Organic search volume decreases
- Referral slows (fewer people know about you)
- Overall growth drops 40%

**Paid social was feeding the other channels.**

<!--
INSTRUCTOR NOTE:

**Background:** This is one of the most common mistakes in channel analysis — treating channels as independent when they're interconnected. It's the same causal inference problem we discussed earlier, but applied to channel relationships. The "halo effect" of awareness channels is real but hard to measure directly.

**Key point:** Channels interact. Cutting one may hurt others in ways that attribution doesn't capture.

**Say something like:**
"This is crucial. Channels don't work in isolation.

Let me give you a scenario. You analyze your channel economics and find paid social has a 0.9x LTV:CAC ratio — every dollar you spend, you lose 10 cents. Seems like an easy call: cut paid social.

So you cut it. What happens?

Brand awareness drops — fewer people see your ads, fewer people know you exist. Organic search volume decreases — people search for brands they've heard of. Referral slows — people don't recommend products they haven't heard of. Overall growth drops 40%.

What happened? Paid social wasn't just acquiring customers directly. It was building awareness that fed your other channels. The attribution system couldn't see this because it only measured direct conversions.

This is why the pre-mortem for MindfulApp is so important. They cut paid social based on channel economics and killed their growth. The analysis was correct — paid social's direct LTV:CAC was low — but it missed the indirect effects.

Before you make major channel cuts, run holdout tests. Turn off the channel in some markets and see what happens to OVERALL growth, not just that channel's attributed conversions."

**If asked:** "How do you measure the 'halo effect'?"
A: Holdout tests or market experiments. Turn off a channel in some geos and measure total outcome, not just attributed outcome. It's more work but it's the only way to know for sure.

**Transition:** "Let me show you a real scenario where this goes wrong..."
-->

---

## The MindfulApp Scenario

**Company:** MindfulApp (meditation app)
**Problem:** 40% YoY growth, burning $8M/quarter
**Question:** Are we acquiring customers profitably?

**Hypothesis:** Organic/referral >5x LTV:CAC; paid social ~1.2x

**Blocker:** Paid acquisition team — if paid social looks bad, team of 4 becomes team of 2. Jobs literally on the line.

<!--
INSTRUCTOR NOTE:

**Background:** This scenario explicitly names the human stakes — a team of 4 becoming a team of 2 means layoffs. This is the most politically charged blocker we've discussed. The analysis isn't just about data; it's about people's jobs.

**Key point:** When your analysis threatens jobs, expect fierce resistance. This doesn't mean you change your analysis — it means you anticipate the pushback and have solid methodology.

**Say something like:**
"Look at the blocker here. If paid social looks bad, a team of 4 becomes a team of 2. That's not abstract — that's layoffs. Jobs on the line.

When you're the analyst presenting this, expect resistance. The paid acquisition team will question your methodology. They'll find edge cases. They'll argue the data is incomplete.

Some of this is legitimate. Maybe your data IS incomplete. Maybe there ARE edge cases you haven't considered.

But some of it is motivated reasoning. They don't want to lose their jobs. That's human and understandable.

Your job is to be rigorous AND empathetic. Rigorous: make sure your methodology is bulletproof before you present. Empathetic: acknowledge the human stakes and present the data as 'here's what we found and what we recommend' not 'here's why you should be fired.'

The goal is to find the truth and make good decisions for the company — not to 'win' against a team."

**If asked:** "How do you handle it when your analysis threatens someone's job?"
A: Present facts, not accusations. Recommend decisions about channels, not people. Let leadership make personnel decisions. And make sure your analysis is solid — you owe that to everyone.

**Transition:** "Let's see what went wrong in the pre-mortem..."
-->

---

## MindfulApp: Pre-Mortem

> We showed paid social had 1.5x LTV:CAC and recommended cutting 60% of spend.
>
> Growth slowed from 40% to 15%.
>
> Turns out paid social drove awareness that boosted organic and referral — channels weren't independent.
>
> **Lesson:** Run holdout tests before major channel cuts to understand interactions.

<!--
INSTRUCTOR NOTE:

**Background:** This is the canonical "channel interaction" failure. The direct LTV:CAC for paid social was low (1.5x), so cutting seemed rational. But paid social was driving awareness that fed organic and referral. When awareness dropped, those "cheap" channels dried up.

**Key point:** Channels aren't independent. The "awareness tax" from paid channels can't be measured with attribution — you need experiments.

**Say something like:**
"This pre-mortem is the culmination of everything we've discussed about channel interactions.

The analysis was correct: paid social's direct LTV:CAC was 1.5x — below the 3x benchmark. The recommendation seemed obvious: cut 60% of spend.

Growth slowed from 40% to 15%.

What went wrong? Paid social wasn't just acquiring customers directly. It was building awareness. When people see your ads, they don't always click immediately. But later, when they're ready to meditate, they remember 'MindfulApp' and search for it — organic. Or they recommend it to a friend — referral.

Those organic and referral channels looked great on paper — 5x+ LTV:CAC! But they were being fed by paid social. Cut the awareness engine, and the 'cheap' channels dry up.

This is why I keep saying: run holdout tests before major channel cuts. Turn off paid social in some markets and measure TOTAL growth, not just paid social's attributed conversions. If overall growth drops, you know paid social is feeding other channels."

**If asked:** "How would you have avoided this?"
A: Run a geo-holdout test first. Cut paid social in 10-20% of markets and measure overall growth for a quarter. If growth tanks in those markets, you know paid social has spillover effects.

**Transition:** "Let me summarize CAC/LTV before we move on..."
-->

---

## CAC/LTV: Key Takeaways

1. **Use fully-loaded CAC** — include salaries, tools, creative
2. **Project LTV conservatively** — extrapolation is guessing
3. **Use cohort-based analysis** — track real behavior over time
4. **Calculate by channel** — aggregate hides important variation
5. **Channels interact** — cutting one may hurt others
6. **Payback matters** — not just ratio (cash flow implications)

<!--
INSTRUCTOR NOTE:

**Background:** These six takeaways capture the essential lessons of CAC/LTV analysis. Points 4-6 are often overlooked by analysts who focus only on the aggregate ratio.

**Key point:** CAC/LTV analysis is more nuanced than a simple ratio. Channel-level analysis, interaction effects, and payback period all matter.

**Say something like:**
"Six takeaways from CAC/LTV.

One: Use fully-loaded CAC. Don't just count ad spend — include salaries, tools, creative production. The true cost is higher than you think.

Two: Project LTV conservatively. Extrapolating from 6 months to 24 months is guessing. Be humble about your predictions.

Three: Use cohort-based analysis. Track actual customers over time. Simple formulas are shortcuts that hide important patterns.

Four: Calculate by channel. The aggregate LTV:CAC ratio hides huge variation. Organic at 5x and paid social at 0.9x average to 2x — but that masks a problem.

Five: Channels interact. This is the MindfulApp lesson. Cutting one channel may hurt others in ways you can't see in attribution.

Six: Payback matters. A 3x LTV:CAC ratio sounds great, but if payback is 18 months, your cash flow suffers. Time to recoup investment matters, not just the final ratio."

**Transition:** "Let me summarize what we've learned about all four acquisition analyses..."
-->

---

<!-- _class: lead -->

# Block 2 Summary

---

## The Four Acquisition Analyses

| Analysis | Core Question | Key Method |
|----------|--------------|------------|
| **Funnel** | Where do we lose them? | Step-by-step conversion rates |
| **Attribution** | Which channels brought them? | Multi-model comparison |
| **Campaign** | Did spend cause the lift? | Counterfactual estimation |
| **CAC/LTV** | Worth more than they cost? | Cohort-based unit economics |

<!--
INSTRUCTOR NOTE:

**Background:** This table summarizes the four acquisition analyses covered in Block 2. Each has a core question and a key method. Use this slide to help students see the bigger picture before moving to retention and growth.

**Key point:** Each analysis answers a different question about customer acquisition. Together, they form a complete picture.

**Say something like:**
"Let me summarize the four acquisition analyses we've covered.

Funnel analysis answers: Where do we lose them? You're looking at step-by-step conversion rates to find the biggest drops.

Attribution answers: Which channels brought them? You compare multiple models and look for disagreements to understand channel contributions.

Campaign effectiveness answers: Did the spend cause the lift? You estimate counterfactuals to separate correlation from causation.

CAC/LTV answers: Are they worth more than they cost? You track cohort-based unit economics to see if acquisition is profitable.

These four analyses give you a complete picture of the acquisition side of the customer journey. For your capstone, you'll pick 2-3 that are most relevant to your specific problem."

**Transition:** "Before we move on, let me highlight the common thread across all these analyses..."
-->

---

## Common Thread: Interactions

**Every pre-mortem in this block shares a theme:**

Things don't work in isolation.
- **Funnel:** Device handoffs (mobile browse, desktop buy)
- **Attribution:** Multi-touch journeys
- **Campaign:** Control market confounds
- **CAC/LTV:** Channel awareness spillover

**Before major decisions, test causally.** Attribution and correlation lie.

<!--
INSTRUCTOR NOTE:

**Background:** This summary slide ties together the meta-lesson of Block 2: interaction effects are everywhere, and they're the most common source of analytics mistakes. Each pre-mortem in this block illustrated a different version of the same problem.

**Key point:** The common failure mode in acquisition analytics is treating things as independent when they interact.

**Say something like:**
"Before we break, I want you to notice a pattern. Look at the pre-mortems from this block.

Funnel analysis: We saw mobile conversion drop and 'fixed' mobile checkout, but users were browsing on mobile and buying on desktop. The devices interacted.

Attribution: We credited last-touch and undervalued LinkedIn, but LinkedIn was starting journeys that search was closing. The channels interacted.

Campaign effectiveness: We found great ROI but our control markets had a competitor enter. Treatment and control interacted with external factors.

CAC/LTV: We cut paid social and growth collapsed because paid social was feeding awareness that drove other channels. The channels interacted.

Every single failure was about interaction effects. Things don't work in isolation. This is why I keep emphasizing causal testing. Run holdouts. Do experiments. Don't make major decisions based on attribution alone — attribution is correlation, not causation."

**If asked:** "Is there a way to model all these interactions?"
A: Marketing mix modeling (MMM) tries to. But it's complex and requires a lot of data. For most decisions, simpler holdout tests work better.

**Transition:** "After break, we'll cover retention and growth analyses. Same pattern — we'll look at how things interact."
-->

---

## Coming Up: Block 3

After break, we cover **Retention & Growth Analyses:**

| Analysis | Question |
|----------|----------|
| **Retention** | Why do they leave? |
| **Power User** | Who are our best customers? |
| **Failure** | What's broken? |
| **Expansion** | How do they grow? |
| **Ecosystem** | How do products interact? |

<!--
INSTRUCTOR NOTE:

**Background:** This is the preview for Block 3 (Day 2). Give students a sense of what's coming so they can connect the acquisition analyses to retention and growth during the weekend.

**Key point:** Block 3 covers the other side of the customer journey — keeping and growing customers you've acquired.

**Say something like:**
"After our break, we'll move to the other side of the customer journey: retention and growth.

Retention analysis: Why do they leave? Understanding churn patterns.

Power user analysis: Who are our best customers? Finding the users who generate the most value.

Failure analysis: What's broken? Root cause analysis when things go wrong.

Expansion analysis: How do they grow? Understanding upsells, upgrades, and expansion revenue.

Ecosystem analysis: How do products interact? Understanding how multiple products or features work together.

The same themes apply — interactions, counter-metrics, pre-mortems. But the questions are different. Acquisition is about getting customers in the door. Retention and growth are about keeping them and making them more valuable over time.

Your weekend assignment will touch on both. You'll think about which analyses are most relevant to your capstone scenario."

**Transition:** "Any quick questions before we break?"
-->

---

## Questions?

<!--
INSTRUCTOR NOTE:

**Background:** This is a brief Q&A to close Block 2 before transitioning to Day 2's content preview. Keep it to 2-3 questions maximum to stay on schedule. Students will have more time to ask questions during the weekend assignment.

**Key point:** Answer 2-3 questions concisely, then transition to the Day 2 preview.

**Common questions and answers:**

Q: "Which analysis should I start with for my capstone?"
A: Depends on the problem. Funnel if conversion is the issue, Attribution if budget allocation, CAC/LTV if unit economics are the question. The Brief's methodology section forces you to justify your choice. Start with the core business question and work backwards to the analysis.

Q: "Do I need to do all four analyses?"
A: No — you'll pick 2-3 that are most relevant to your capstone problem. The Brief template asks you to justify why those specific analyses answer your business question.

Q: "How deep do I need to go on causal inference?"
A: Understand the concepts well enough to know when your analysis can make causal claims and when it can only show correlation. You don't need to implement synthetic control from scratch, but you should know when to recommend it.

Q: "What tools should I use for these analyses?"
A: Python or SQL for most data work. The specific tools matter less than understanding the logic. For campaign effectiveness, Google has open-source libraries; for attribution, most ad platforms have built-in tools you'd use in practice.

Q: "What if my capstone company doesn't have good data?"
A: This is common. Part of your Brief should identify data gaps and what's achievable with available data. Sometimes the recommendation is 'instrument these events before running this analysis.'

**Say something like:**
"Before we preview Day 2, let me take 2-3 quick questions. We'll have more time for questions during office hours and the weekend assignment."

[After 2-3 questions]

"Great questions. Hold onto any others — you'll have plenty of time to dig deeper during the assignment. Let me give you a quick preview of what's coming on Day 2..."

**Transition:** "Let me give you a preview of Day 2..."
-->

---

<!-- _class: lead -->
<!-- _paginate: false -->

# Break Time!

**Block 3 starts at 15:40**

Retention & Growth Analyses

