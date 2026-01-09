---
marp: true
theme: default
paginate: true
header: 'ECBS5228A: Designing Analytics Projects'
footer: 'Block 5: Stakeholders & Influence'
---

<!-- _class: lead -->
<!-- _paginate: false -->
<!-- _header: '' -->
<!-- _footer: '' -->

# Designing Analytics Projects

## Block 5: Stakeholders & Influence

**Eduardo Arino de la Rubia**
January 12, 2026

---

## Block 5 Overview

| Section | Time |
|---------|------|
| **Stakeholder Management** | **25 min** |
| Processing Fluency | 8 min |
| Message Theory Cheat-Sheet | 2 min |
| Four Influence Strategies | 30 min |
| Stakeholder-Strategy Integration | 12 min |
| Think-Pair-Share: Influence Planning | 15 min |

<!--
INSTRUCTOR NOTE:

**Background:** This is the "soft skills" block, which some students will initially dismiss. The key is establishing early that these aren't optional nice-to-haves — they're how analysis creates value. Many excellent analysts plateau in their careers because they refuse to engage with organizational dynamics.

**Key point:** This block is about making your technical work actually matter.

**Say something like:**
"Here's what we're covering in this block. Stakeholder management — who are the people involved in your analysis, and how do you work with them? Processing fluency — why simple communication beats complex. Message theory — how to structure your presentations. Four influence strategies — different approaches for different stakeholders. And then we'll integrate it all with an exercise.

I know some of you are thinking 'this isn't technical.' You're right. It's not. But it's how technical work creates value. Stick with me."

**Transition:** "Let me start by framing why Day 2 is different from Day 1..."
-->

---

## Day 2 Theme: The People

> **Day 1 was about "The Work"** — scoping, metrics, analyses.
>
> **Day 2 is about "The People"** — stakeholders, influence, communication.

The best analysis fails if:
- The wrong people see it
- The right people don't buy in
- A blocker kills it politically

**Technical correctness is necessary but not sufficient.**

<!--
INSTRUCTOR NOTE:

**Background:** This block often meets resistance from students who see themselves as "technical" and view organizational dynamics as "politics they shouldn't have to deal with." The key reframe is that stakeholder work IS the work — it's not optional overhead, it's how analysis creates value. Many excellent analysts plateau in their careers because they refuse to engage with this.

**Key point:** Technical correctness is necessary but not sufficient. The best analysis fails without stakeholder buy-in.

**Say something like:**
"I want to set the frame for Day 2. Yesterday was about The Work — how to scope projects, define metrics, conduct analyses. Important stuff.

Today is about The People. And I know some of you are thinking: 'I'm a data scientist. I just want to do good analysis. Why do I need to learn about politics?'

Here's why: because the best analysis in the world fails if the wrong people see it, or the right people don't buy in, or a single blocker kills it politically.

I've seen this dozens of times. Beautiful analysis. Correct methodology. Actionable findings. And it went nowhere. Because the analyst didn't understand who needed to be convinced, or they surprised the wrong person in a meeting, or they presented to an executive who'd already made up their mind.

Technical correctness is necessary — obviously — but it's not sufficient. The skills we cover today are how analysis creates value. They're not optional overhead. They're the job."

**If asked:** "Isn't this just 'office politics'?"
A: It's organizational awareness. Politics has a negative connotation — like manipulation. This is about understanding how decisions get made and communicating effectively. That's a professional skill, not a dark art.

**Transition:** "Let's start with stakeholder management..."
-->

---

<!-- _class: lead -->

# Part 1: Stakeholder Management
### *(25 minutes)*

---

## Why Stakeholders Matter

Your job includes navigating organizational dynamics.

| Without Stakeholder Awareness | With Stakeholder Awareness |
|------------------------------|---------------------------|
| Surprised by resistance | Anticipated and addressed |
| Analysis ignored | Analysis acted upon |
| "Why didn't anyone tell me?" | "I saw that coming" |

**Every analysis exists in a political context.** Ignoring it is a choice — usually a bad one.

<!--
INSTRUCTOR NOTE:

**Background:** This slide establishes that stakeholder awareness isn't optional — it's a core professional skill. The table shows concrete outcomes: the difference between surprise and anticipation, between ignored and acted-upon analysis.

**Key point:** Organizational dynamics aren't an obstacle to analysis. They're the context in which analysis creates value.

**Say something like:**
"Look at this table. The column on the left is what happens when you ignore stakeholders. You get surprised by resistance — someone shoots down your recommendation, and you didn't see it coming. Your analysis gets ignored — it was technically correct, but nobody acted on it. You ask 'why didn't anyone tell me?' — because you didn't ask.

The column on the right is what happens when you're aware. You anticipate resistance and address it before the meeting. Your analysis gets acted upon because you involved the right people. You see problems coming.

Here's the uncomfortable truth: every analysis exists in a political context. There are winners and losers from your findings. There are people whose budgets, headcounts, and reputations are affected. Ignoring that context is a choice — and it's usually a bad one.

I'm not asking you to become political operators. I'm asking you to be aware of the organizational context you're operating in."

**Transition:** "Let me give you a framework for mapping stakeholders..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_05_power_interest_grid.png)

---

## The Power-Interest Grid

Map every stakeholder to a quadrant. This determines your engagement strategy.

<!--
INSTRUCTOR NOTE:

**Background:** The Power-Interest Grid (also called the Mendelow Matrix) is a classic stakeholder analysis tool. Power = ability to affect outcomes. Interest = degree of engagement with this specific project. The key insight is that different quadrants require different engagement strategies.

**Key point:** Not all stakeholders are equal. Different quadrants require different approaches.

**Say something like:**
"This is the Power-Interest Grid. It's simple but powerful.

Power is on the vertical axis — can this person affect whether your project succeeds or fails? Interest is on the horizontal — do they care about this specific project?

The combination determines your strategy. High power, high interest — these are your key stakeholders. They can affect outcomes and they care. Manage them closely.

High power, low interest — they can affect outcomes but don't care yet. Keep them satisfied. Don't waste their time, but don't let them be surprised.

Low power, high interest — they care deeply but can't make decisions. Keep them informed. They're often great sources of information and can become champions.

Low power, low interest — monitor but don't over-engage. You have limited time."

**Transition:** "Let me define each quadrant more precisely..."
-->

---

## Power-Interest: Definitions

**High Power, High Interest** — Decision makers, sponsors → Manage closely

**High Power, Low Interest** — Execs with veto power → Keep satisfied

**Low Power, High Interest** — SMEs, ICs → Keep informed

**Low Power, Low Interest** — Tangential teams → Monitor

**Mistake:** Treating everyone the same.

<!--
INSTRUCTOR NOTE:

**Background:** Each quadrant has a specific engagement strategy. The most common mistake is treating all stakeholders equally — either over-engaging low-power people or under-engaging high-power people.

**Key point:** "Manage closely" ≠ "bother constantly." It means proactive, substantive engagement.

**Say something like:**
"Let me make each quadrant concrete.

High Power, High Interest: these are your sponsors and decision makers. Manage closely. That means regular updates, no surprises, genuine involvement in key decisions. If the VP of Product is your sponsor, they should never be surprised by what you present.

High Power, Low Interest: executives who could veto your project but probably won't pay attention unless something goes wrong. Keep satisfied. Don't waste their time with details, but make sure they're not blindsided. A 30-second update in a meeting is often enough.

Low Power, High Interest: subject matter experts, individual contributors who care deeply. Keep informed. They're often your best sources of context and can become powerful champions even without formal authority.

Low Power, Low Interest: tangential teams. Monitor. Check in occasionally, but don't over-invest. Your time is limited.

The mistake is treating everyone the same. Sending the same update to everyone. Scheduling the same meetings with everyone. That wastes time on low-priority stakeholders and under-serves high-priority ones."

**Transition:** "Beyond the grid, we need to identify two special categories..."
-->

---

## Champions & Blockers

Beyond the grid, identify:

**Champions:** Who actively wants this to succeed?
- They'll advocate in meetings you're not in
- They'll provide air cover when things get political

**Blockers:** Who might resist?
- **Why** do they resist? (Budget? Ego? Workload? Past failures?)
- Understanding motivation enables mitigation

<!--
INSTRUCTOR NOTE:

**Background:** Champions and blockers are special categories that cross-cut the power-interest grid. A champion might be low-power but incredibly valuable because they advocate for you in rooms you're not in. A blocker might be low-power but can still derail progress through passive resistance.

**Key point:** Champions advocate for you in rooms you're not in. Blockers can kill projects you've worked on for months.

**Say something like:**
"Beyond the grid, you need to identify two special categories: champions and blockers.

Champions actively want you to succeed. They might be in any quadrant. What makes them champions is that they'll advocate for you in meetings you're not invited to. They'll provide air cover when things get political. They'll say 'I've seen their analysis, it's solid' when someone questions you.

Champions are gold. Find them. Arm them with information. Make them look good.

Blockers might resist your project. The crucial question is: WHY do they resist? Budget threat? Ego protection? Additional workload? Past bad experiences with similar projects?

Understanding motivation is everything. A blocker who's worried about their budget needs a different conversation than one who's protecting their ego. We'll talk about mitigation strategies next."

**Transition:** "Let's look at common blocker motivations and how to address them..."
-->

---

## Common Blocker Motivations

**Threatens budget** — Frame as reallocation, not cut

**Threatens credibility** — Private preview, collaborative framing

**Creates work** — Show ROI, offer phased approach

**Past failures** — Involve in methodology, conservative estimates

**Ego/ownership** — Solicit input, share credit

<!--
INSTRUCTOR NOTE:

**Background:** This slide gives a quick reference for common blocker motivations and mitigation strategies. Each motivation requires a different approach — there's no one-size-fits-all.

**Key point:** Mitigation starts with understanding motivation. Wrong diagnosis = wrong treatment.

**Say something like:**
"Let me walk through these quickly.

Threatens budget: If your analysis recommends cutting their budget, frame it as reallocation. 'We're shifting resources to higher-ROI channels' sounds different from 'we're cutting your budget.'

Threatens credibility: If your findings imply their past work failed, give them a private preview. Let them process it without an audience. Frame collaboratively: 'What can we learn from this?' not 'you were wrong.'

Creates work: If acting on your analysis means more work for them, show the ROI. Offer a phased approach. 'We can start small and scale if results justify' is less threatening than 'change everything now.'

Past failures: If they've been burned by similar projects before, involve them in your methodology. Be conservative in your estimates. Acknowledge the history: 'I know this hasn't worked before. Here's what's different.'

Ego/ownership: If they feel territorial, solicit their input genuinely. Share credit for the success. Make them part of the solution, not just a victim of the recommendation."

**If asked:** "What if I can't figure out their motivation?"
A: Ask them. "I want to understand your concerns" often works. Or ask someone who knows them well.

**Transition:** "Let's practice mapping stakeholders..."
-->

---

## Exercise: Map Your Stakeholders

> **Think (2 min):**
>
> For one of yesterday's example analyses (Funnel, Attribution, Retention, etc.), who would be in each quadrant?

<!--
INSTRUCTOR NOTE:

**Background:** This brief exercise connects stakeholder mapping to the analyses students learned yesterday. It makes the abstract concept concrete.

**Key point:** Every analysis has stakeholders. Mapping them should become automatic.

**Facilitation:**
Give 2 min to think silently, then cold-call 2-3 students. Push them to be specific about names/roles, not just "product team."

**Example for Quickcart Funnel Analysis:**
- High Power, High Interest: VP Product (owns conversion), CFO (cares about revenue)
- High Power, Low Interest: CEO (trusts VP to handle, but could override)
- Low Power, High Interest: Checkout PM (owns the feature), Mobile team lead (technical implementation)
- Low Power, Low Interest: Warehouse ops (not affected), Customer Support (tangentially aware)

**Say something like:**
"Take 2 minutes. Pick one of the analyses from yesterday — Funnel, Attribution, Retention, any of them. Map the stakeholders to quadrants. Be specific: names or roles, not 'the team.'

[After 2 min]

Let me hear from a few of you. You — which analysis and who's in High Power, High Interest?"

**Transition:** "Let me give you the key takeaways from stakeholder management..."
-->

---

## Stakeholder Management: Key Takeaways

1. **Map stakeholders to Power-Interest grid** — different strategies per quadrant
2. **Identify champions and blockers** — understand *why* blockers resist
3. **Pre-brief uncomfortable findings** — never ambush in meetings
4. **Tailor communication by quadrant** — executives ≠ ICs
5. **Politics is part of the job** — technical correctness isn't enough

<!--
INSTRUCTOR NOTE:

**Background:** This slide summarizes the stakeholder management section. These five points are the minimum viable stakeholder awareness for any analyst.

**Key point:** These five practices should become automatic for every project.

**Say something like:**
"Let me summarize stakeholder management in five points.

One: Map stakeholders to the Power-Interest grid. Different quadrants, different strategies.

Two: Identify champions and blockers. Champions help you in rooms you're not in. For blockers, understand WHY they resist — that's the key to mitigation.

Three: Pre-brief uncomfortable findings. Never surprise anyone in a meeting. If your analysis makes someone look bad, they should hear about it privately first.

Four: Tailor communication by quadrant. Executives don't want the same level of detail as subject matter experts. Adjust.

Five: Politics is part of the job. I know some of you resist that idea. But ignoring organizational dynamics is a choice — and it usually leads to your work being ignored."

**Transition:** "Now let's talk about how you communicate — starting with processing fluency..."
-->

---

<!-- _class: lead -->

# Part 2: Processing Fluency
### *(8 minutes)*

---

## The Core Principle

> **"The more work your listener must do, the less they will trust it."**

This is **processing fluency** — the ease with which information is understood.

High fluency → Feels true, trustworthy
Low fluency → Feels suspicious, questionable

**Your job:** Make it easy for people to understand and believe your findings.

<!--
INSTRUCTOR NOTE:

**Background:** Processing fluency is a psychological phenomenon: information that's easy to process feels more credible, regardless of its actual truth value. This has been studied extensively — even simple things like using a legible font or presenting in simple language increase perceived credibility. This is counterintuitive for technical people who associate complexity with rigor.

**Key point:** Complexity doesn't signal rigor. It signals "this is hard to evaluate." Simplicity creates trust.

**Say something like:**
"This is one of the most counterintuitive findings from psychology research: the more work your listener has to do to understand something, the less they trust it.

This is called processing fluency. Information that's easy to process feels true. Information that's hard to process feels suspicious.

Now, why is this counterintuitive? Because many of us were trained to think that complex equals rigorous. If the analysis looks complicated, it must be thorough. If the explanation has caveats, it must be nuanced.

But that's not how audiences perceive it. When an executive sees a slide with 15 columns of numbers and three paragraphs of methodology caveats, they don't think 'wow, this is rigorous.' They think 'I don't understand this, so I can't trust it.'

Your job is to do the hard work of simplification. The complexity lives in your methodology. The audience sees the clear conclusions."

**If asked:** "Won't executives think simple analysis is shallow?"
A: Only if it's actually shallow. You can be rigorous AND simple. The methodology is complex; the communication is clear. Have the details ready if asked, but lead with clarity.

**Transition:** "Let me show you what low vs. high fluency looks like..."
-->

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_05_fluency_comparison.png)

---

## Why Simple Beats Complex

**Research shows:**
- Simple explanations are rated as more credible
- Jargon reduces persuasion (even with expert audiences)
- Visual clarity increases agreement

Complex ≠ Rigorous. Complex = Hard to trust.

<!--
INSTRUCTOR NOTE:

**Background:** These findings come from cognitive psychology research on fluency. The counterintuitive result is that even expert audiences are more persuaded by simpler explanations. Jargon signals in-group membership but reduces actual persuasion.

**Key point:** Complexity signals "I can't evaluate this" not "this must be rigorous."

**Say something like:**
"These are research findings, not my opinions.

Simple explanations are rated as more credible — even by experts. Why? Because fluency creates a feeling of truth. If I can understand it easily, my brain says 'this makes sense.'

Jargon reduces persuasion — even with expert audiences. Jargon signals 'I'm part of the in-group' but it doesn't actually convince people. In fact, excessive jargon makes people suspicious that you're hiding behind words.

Visual clarity increases agreement. A clean chart with one clear message is more persuasive than a complex chart with many messages.

The formula to remember: Complex ≠ Rigorous. Complex = Hard to trust. Do the hard work of simplification."

**Transition:** "Let me show you what this looks like in practice..."
-->

---

## Fluency in Practice

| Low Fluency | High Fluency |
|-------------|--------------|
| "The coefficient on the interaction term between channel and cohort was significant at p<0.05 controlling for..." | "Paid social users from Q3 retained 20% worse than Q2." |
| Dense tables with 15 columns | Highlighted key numbers with context |
| 40-slide appendix | 10 slides + "details available" |

**Rule:** If an executive can't understand it in 30 seconds, simplify.

<!--
INSTRUCTOR NOTE:

**Background:** This table provides concrete before/after examples. The left column is how many analysts actually communicate. The right column is what works.

**Key point:** The 30-second rule is real. If an executive can't understand it quickly, they'll delegate to someone who will simplify it anyway — and that person may misunderstand.

**Say something like:**
"Let me make this concrete.

Low fluency: 'The coefficient on the interaction term between channel and cohort was significant at p<0.05 controlling for...' Who is this sentence for? Other statisticians. Not decision makers.

High fluency: 'Paid social users from Q3 retained 20% worse than Q2.' Same finding. One sentence. Actionable.

Low fluency: Dense tables with 15 columns. Everything you computed.

High fluency: Highlighted key numbers with context. The one or two numbers that matter, with enough context to understand them.

Low fluency: 40-slide appendix proving how thorough you were.

High fluency: 10 slides with the story, and 'details available' for those who want to dig deeper.

Here's the rule: if an executive can't understand it in 30 seconds, simplify. If they have to work hard to understand you, they'll either stop listening or delegate to someone who will simplify it — and that person might misunderstand."

**Transition:** "Here's a test you can apply to any presentation..."
-->

---

## The Fluency Test

Before presenting, ask:

1. **Can I explain this in one sentence?**
2. **Would my non-technical friend understand?**
3. **What's the ONE number that matters?**
4. **Is everything else supporting detail?**

If you can't pass this test, you're not ready to present.

<!--
INSTRUCTOR NOTE:

**Background:** The Fluency Test is a self-check before any presentation. Each question forces simplification. If you can't pass this test, you're not ready — and presenting anyway will be less effective.

**Key point:** If you can't explain it simply, you either don't understand it or haven't done the work of simplifying.

**Say something like:**
"Before any presentation, run this test on yourself.

One: Can I explain this in one sentence? If you need three paragraphs to explain what you found, you haven't distilled it enough.

Two: Would my non-technical friend understand? Not 'would they understand the methodology' — would they understand the point? 'We should shift money from one channel to another because the second one is more profitable.' That's friend-explainable.

Three: What's the ONE number that matters? Not the five numbers you computed. The one that makes the decision. Everything else is supporting detail.

Four: Is everything else supporting detail? If you have information that isn't supporting the main point, why is it in your presentation?

If you can't pass this test, you're not ready to present. Go back and simplify."

**Transition:** "Let me give you a framework for structuring any presentation..."
-->

---

## Message Theory Cheat-Sheet

**Before any communication, complete this sentence:**

> "I'm presenting to **[specific person]** about **[topic in 10 words]** and my recommendation is **[specific action]**."

**Who?** A specific person, not "the team" → *"Sarah, the CFO"*

**What?** Topic in 10 words → *"Where should we spend next quarter?"*

**So what?** A specific action → *"Shift $200K from paid social to referral"*

**If you can't fill in this sentence, you're not ready to present.**

<!--
INSTRUCTOR NOTE:

**Background:** This is the Message Theory framework — a forcing function for clarity. Most presentations fail because the presenter hasn't answered these three questions clearly. The sentence structure forces specificity.

**Key point:** "The team" is not an audience. "We should consider options" is not a recommendation. Be specific.

**Say something like:**
"This is my favorite pre-presentation framework. Before any communication, fill in this sentence:

'I'm presenting to [specific person] about [topic in 10 words] and my recommendation is [specific action].'

Let me break that down.

Who? A specific person. Not 'the leadership team.' Not 'stakeholders.' Sarah, the CFO. Because Sarah has specific concerns, priorities, and decision-making styles. 'The team' doesn't.

What? Topic in 10 words or less. If you need more than 10 words to describe your topic, you haven't focused enough. 'Where should we spend next quarter?' That's clear.

So what? A specific action. Not 'we should consider our options.' Not 'here are some findings.' A specific recommendation: 'Shift $200K from paid social to referral.'

If you can't fill in this sentence, you're not ready to present. Go back and clarify until you can."

**If asked:** "What if I genuinely don't have a recommendation?"
A: Then your recommendation is 'I need [specific thing] to make a recommendation.' That's still specific. 'I need 2 more weeks of data to be confident' is a recommendation.

**Transition:** "Now let's talk about how to influence different stakeholders..."
-->

---

<!-- _class: lead -->

# Part 4: Four Influence Strategies
### *(30 minutes)*

---

<!-- _header: '' -->
<!-- _footer: '' -->

![bg contain](../figures/images/block_05_influence_compass.png)

---

## The Influence Compass

Four strategies, four directions. Each works differently.

Your stakeholder map determines which strategy to use with whom.

<!--
INSTRUCTOR NOTE:

**Background:** The Influence Compass organizes four distinct persuasion strategies. They're not mutually exclusive — most successful presentations combine 2-3. But each works differently and appeals to different stakeholder types.

**Key point:** Different stakeholders respond to different strategies. One size does not fit all.

**Say something like:**
"This is the Influence Compass. Four strategies, four directions.

Authority — North. Leveraging organizational hierarchy.
Credibility — South. Leveraging expertise and peer validation.
Social Proof — West. Leveraging data about what others do.
Consistency — East. Leveraging alignment with stated priorities.

Each strategy works differently. Each appeals to different stakeholder types. The key insight is: you don't use the same strategy with everyone. Your stakeholder map tells you WHO you're influencing. The compass tells you HOW.

Most successful presentations use 2-3 strategies combined. Let me walk you through each one."

**Transition:** "Let's start with Authority..."
-->

---

## Strategy 1: Authority (North)

**What it is:** Leveraging support from people with organizational power.

**How it sounds:**
> "The VP of Product has reviewed this approach and supports moving forward."
> "Leadership asked us to prioritize this."

**When to use:**
- Stakeholder respects hierarchy
- You have genuine top-down support
- Decision needs organizational weight

<!--
INSTRUCTOR NOTE:

**Background:** Authority is the most straightforward influence strategy — "someone powerful backs this." It works when stakeholders respect hierarchy and when you genuinely have top-down support. The danger is faking it or overusing it.

**Key point:** Authority requires genuine backing. Faking it destroys credibility permanently.

**Say something like:**
"Authority is the simplest strategy. Someone powerful supports your recommendation. You invoke that support.

'The VP of Product has reviewed this and supports moving forward.' That sentence does a lot of work. It says: I'm not a lone analyst with an idea. Someone with organizational power has validated this.

When to use it: when your stakeholder respects hierarchy, when you genuinely have top-down support, when the decision needs organizational weight to move forward.

The danger: don't fake it. If you say 'the VP supports this' and the VP hasn't actually reviewed it, you'll be caught. And that destroys your credibility permanently. Authority only works when it's genuine."

**Transition:** "But you probably don't have authority just because you're an analyst. Let me show you how to build it..."
-->

---

## Authority: How to Build It

You probably don't have inherent authority. So:

1. **Get a sponsor** — Find a leader who supports your work
2. **Secure explicit endorsement** — "Can I say you've reviewed this?"
3. **Cite the ask** — "This was requested by [leader]"

**Warning:** Don't fake authority. Being caught undermines everything.

<!--
INSTRUCTOR NOTE:

**Background:** Most analysts don't have inherent authority — they're not senior executives. But they can borrow authority through sponsorship and endorsement. The key is making it explicit and genuine.

**Key point:** "Can I say you've reviewed this?" is a magic question. It gets explicit permission to invoke authority.

**Say something like:**
"You probably don't have inherent authority. You're an analyst, not a VP. So how do you use this strategy?

Get a sponsor. Find a leader who supports your work. Build that relationship over time.

Secure explicit endorsement. This is the key move. When your sponsor reviews your work, ask: 'Can I say you've reviewed and support this approach?' That gives you explicit permission to invoke their authority. Without that permission, you're name-dropping without consent.

Cite the ask. If a leader asked for this analysis, say so: 'This was requested by [name].' That's authority by origin, not endorsement.

The warning is important: don't fake it. Don't say 'the CEO supports this' if you've never talked to the CEO. Getting caught faking authority is career-limiting."

**Transition:** "The opposite of Authority is Credibility — let's look at that..."
-->

---

## Strategy 2: Credibility (South)

**What it is:** Leveraging validation from respected experts or peers.

**How it sounds:**
> "The senior data scientist reviewed the methodology and confirmed it's sound."
> "Engineering validated that this is technically feasible."

**When to use:**
- Stakeholder is technical or detail-oriented
- Your personal credibility isn't established yet
- The methodology is complex or novel

<!--
INSTRUCTOR NOTE:

**Background:** Credibility is expert validation — "smart people have checked this." It works especially well with technical or skeptical stakeholders who won't just trust authority. It's the natural strategy for junior analysts who don't yet have personal credibility.

**Key point:** Credibility says "experts have validated this" — it's bottom-up influence vs. Authority's top-down.

**Say something like:**
"Credibility is the opposite direction from Authority. Instead of 'powerful people support this,' it's 'smart people have validated this.'

'The senior data scientist reviewed the methodology.' 'Engineering confirmed feasibility.' These sentences say: I'm not asking you to trust me. I'm asking you to trust the experts who've reviewed my work.

When to use it: when your stakeholder is technical or detail-oriented, when your personal credibility isn't established yet, when the methodology is complex or novel and needs validation.

This is the natural strategy for junior analysts. You might not have authority or reputation, but you can get your work reviewed by people who do."

**Transition:** "Let me show you how to build credibility..."
-->

---

## Credibility: How to Build It

1. **Get peer review** — Have respected ICs review your work
2. **Cite precedent** — "This is the same approach Airbnb used for..."
3. **Show your work** — Make methodology transparent and available
4. **Acknowledge limitations** — Credible people admit uncertainty

**Warning:** Over-claiming expertise you don't have destroys credibility permanently.

<!--
INSTRUCTOR NOTE:

**Background:** Credibility is built through peer validation, precedent, transparency, and intellectual honesty. The counterintuitive element is that acknowledging limitations INCREASES credibility rather than decreasing it.

**Key point:** Admitting uncertainty makes you more credible, not less. People trust those who know what they don't know.

**Say something like:**
"How do you build credibility?

Peer review. Have respected people review your work. 'The senior data scientist reviewed this' is powerful because it transfers their credibility to you.

Cite precedent. 'This is the same approach Airbnb used for their pricing optimization.' Precedent says: I'm not inventing something new. Smart companies have done this.

Show your work. Make methodology transparent. Credible people invite scrutiny. If you hide your methodology, people wonder what you're hiding.

Acknowledge limitations. This is counterintuitive. You might think admitting uncertainty makes you look weak. Actually, it makes you more credible. People trust those who know what they don't know. 'This analysis has a limitation in that...' signals intellectual honesty.

The warning: don't over-claim expertise. If you claim to be an expert in something you're not, and you get caught, your credibility is destroyed permanently."

**Transition:** "Third strategy: Social Proof..."
-->

---

## Strategy 3: Social Proof (West)

**What it is:** Leveraging data about what others do or believe.

**How it sounds:**
> "73% of users said they'd upgrade if we added this feature."
> "Industry benchmarks show 3:1 LTV:CAC is healthy; we're at 1.5:1."
> "Three other companies in our space have already made this change."

**When to use:**
- Stakeholder is risk-averse
- Decision feels uncertain
- You have relevant data or benchmarks

<!--
INSTRUCTOR NOTE:

**Background:** Social Proof says "others do this" or "data supports this." It works especially well with risk-averse stakeholders who don't want to be first. Benchmarks, survey data, and competitive intelligence all provide social proof.

**Key point:** Social proof reduces perceived risk. "Others do this" = "it's not crazy."

**Say something like:**
"Social Proof says: others do this. Or: data supports this.

'73% of users said they'd upgrade.' That's user data as social proof. 'Industry benchmarks show 3:1 is healthy.' That's benchmark data. 'Three other companies already made this change.' That's competitive intelligence.

When to use it: when your stakeholder is risk-averse. Risk-averse people don't want to be first. They want to know others have done this successfully. Social proof reduces perceived risk.

Also useful when the decision feels uncertain. 'I don't know if this will work' becomes 'others have done this and it worked for them.'

And obviously useful when you have the data. Survey results, benchmarks, competitor analysis — all provide social proof."

**Transition:** "How do you gather social proof?..."
-->

---

## Social Proof: How to Build It

1. **Survey data** — What do users/customers actually say?
2. **Industry benchmarks** — What do peers do?
3. **Internal precedent** — "We did something similar for X product"
4. **Competitive intelligence** — What are competitors doing?

**Warning:** Cherry-picked social proof backfires. Be honest about what the data shows.

<!--
INSTRUCTOR NOTE:

**Background:** This slide gives practical guidance on where to find social proof. Students often don't know where to look for external validation.

**Key point:** Social proof comes from four sources — survey data, benchmarks, internal precedent, and competitive intelligence. Use them honestly.

**Say something like:**
"So where do you actually find social proof? Four sources:

Survey data. What do your users or customers actually say? NPS data, customer interviews, support tickets. 'Customers have been asking for this' is powerful if it's true.

Industry benchmarks. What do your peers do? This is where Gartner, Forrester, and industry surveys are useful. '85% of SaaS companies have implemented this' gives cover to the decision-maker.

Internal precedent. 'We did something similar for X product, and here's what happened.' This is powerful because it's your own data. They can't dismiss it as 'but our situation is different.'

Competitive intelligence. What are your competitors doing? 'Spotify launched this feature 6 months ago' can motivate action. But be careful — 'because competitors are doing it' isn't always a good reason.

Now, the warning on this slide is critical: Cherry-picked social proof backfires. If you selectively quote the one survey that supports your point while ignoring three that don't, you'll lose credibility when someone checks. Be honest about what the data shows. If the evidence is mixed, say so. Your credibility in future recommendations depends on being trustworthy now."

**If asked:** "What if I can't find good social proof?"
A: Then don't force it. Use a different strategy. Weak social proof is worse than none — it makes you look like you're reaching.

**Transition:** "The fourth and final strategy is Consistency..."
-->

---

## Strategy 4: Consistency (East)

**What it is:** Connecting your recommendation to stated priorities.

**How it sounds:**
> "This aligns with our Q2 priority of improving retention."
> "The CEO said at all-hands that profitability is the focus this year."
> "This supports the roadmap item we already committed to."

**When to use:**
- Stakeholder has stated priorities or values
- Organization has clear strategy
- You can draw genuine connection

<!--
INSTRUCTOR NOTE:

**Background:** Consistency leverages the psychological principle that people want to be consistent with what they've already said. If the CEO said profitability matters, recommending something that improves profitability is aligned with what they've committed to.

**Key point:** Consistency says "you already said this matters." It's hard to argue against your own stated priorities.

**Say something like:**
"Consistency is powerful because it leverages something already said.

'This aligns with our Q2 priority of improving retention.' If the organization has committed to retention, you're not asking for something new. You're asking them to follow through on what they already said.

'The CEO said at all-hands that profitability is the focus.' If the CEO said that, recommending something that improves profitability is hard to argue against. They'd be contradicting themselves.

When to use it: when stakeholders have stated priorities, when the organization has clear strategy, when you can draw a genuine connection.

The key word is genuine. If you force a connection that isn't there, it feels manipulative. The alignment has to be real."

**Transition:** "Let me show you how to build consistency..."
-->

---

## Consistency: How to Build It

1. **Know the roadmap** — What has leadership committed to?
2. **Quote back priorities** — "You mentioned [X] was important..."
3. **Show alignment** — Make the connection explicit
4. **Avoid contradictions** — Don't recommend things that conflict with stated goals

**Warning:** Forced connections feel manipulative. The alignment must be genuine.

---

## Choosing Your Strategy

**Authority (N)** — For hierarchy-respecting stakeholders. Requires sponsor support.

**Credibility (S)** — For technical/skeptical stakeholders. Requires peer validation.

**Social Proof (W)** — For risk-averse stakeholders. Requires data, benchmarks.

**Consistency (E)** — For strategy-focused stakeholders. Requires knowledge of priorities.

**Most presentations use 2-3 strategies combined.**

<!--
INSTRUCTOR NOTE:

**Background:** This is the decision framework slide. Students need to understand that strategy selection depends on stakeholder characteristics, not personal preference.

**Key point:** Match the strategy to the stakeholder type. Wrong strategy = worse than no strategy.

**Say something like:**
"Let me give you the cheat sheet.

Authority works for hierarchy-respecting stakeholders. When someone cares about who said something, you lead with your senior sponsor. But it requires you to actually have that sponsor support.

Credibility works for technical or skeptical stakeholders. Engineers, data scientists, CFOs who want to see the math. It requires peer validation — they need to believe the methodology is sound.

Social Proof works for risk-averse stakeholders. 'What are other companies doing?' They don't want to be first; they want to be safe. It requires external data and benchmarks.

Consistency works for strategy-focused stakeholders. 'This aligns with what you said matters.' It requires knowledge of their stated priorities.

Here's the key insight: Most presentations use 2-3 strategies combined. You don't pick just one. For a CFO, you might lead with Social Proof (industry benchmarks) and anchor to Consistency (aligns with profitability goals). For a technical lead, you might combine Credibility (finance validated) with Authority (leadership asked us to look at this)."

**If asked:** "What if I don't know which type of stakeholder they are?"
A: Ask someone who's worked with them. Or observe in meetings: Do they ask "who said this?" (authority), "show me the math" (credibility), "what do others do?" (social proof), or "how does this fit our strategy?" (consistency)?

**Transition:** "Let me show you an example that combines all four..."
-->

---

## Example: MindfulApp Recommendation

Recommendation: "Shift $200K from paid social to referral program"

| Strategy | Application |
|----------|-------------|
| **Authority** | "The CEO asked us to find a path to profitability" |
| **Credibility** | "Finance validated our CAC calculations" |
| **Social Proof** | "Industry benchmark is 3:1 LTV:CAC; we're at 1.2x on paid social" |
| **Consistency** | "This aligns with our Series B milestone of positive unit economics" |

<!--
INSTRUCTOR NOTE:

**Background:** This is a worked example showing all four strategies applied to one recommendation. It demonstrates that real presentations combine multiple strategies.

**Key point:** Effective influence uses 2-3 strategies together, not just one. This example shows all four for completeness.

**Say something like:**
"Let me walk through a concrete example. MindfulApp wants to shift $200K from paid social to a referral program. How do we make this case?

Authority: 'The CEO asked us to find a path to profitability.' This establishes that leadership is behind this direction. It's not just the analytics team's idea.

Credibility: 'Finance validated our CAC calculations.' This shows we did the work. Finance — the skeptics — signed off on the math. This builds trust in the numbers.

Social Proof: 'Industry benchmark is 3:1 LTV:CAC; we're at 1.2x on paid social.' External validation. We're not just saying paid social is inefficient — the industry standard says so too. We're underperforming.

Consistency: 'This aligns with our Series B milestone of positive unit economics.' This connects to stated priorities. The board said unit economics matter for Series B. This recommendation gets us there.

Notice what's happening: We're not picking just one strategy. We're layering them. Authority gets attention. Credibility builds trust in the analysis. Social Proof provides external validation. Consistency anchors to priorities.

In your own presentations, you'll typically lead with 2-3 of these. Pick the ones that match your stakeholder."

**If asked:** "Do I need all four strategies?"
A: No. Most presentations use 2-3. Pick the ones that match your stakeholder. Authority + Consistency for executives. Credibility + Social Proof for technical leads. Don't force strategies that don't fit.

**Transition:** "Let's practice this. Quick exercise..."
-->

---

## Exercise: Strategy Selection

> **Think (2 min):**
>
> You need to convince a skeptical CFO to approve a $500K investment in a referral program.
>
> Which 2 strategies would you lead with? Why?

<!--
INSTRUCTOR NOTE:
Cold call 2-3 students.
Strong answer: Social Proof (ROI benchmarks, other companies' results) + Consistency (aligns with profitability goals)
CFOs often respond to data and financial alignment more than authority.
-->

---

## The Wrong Strategy Backfires

- **Technical expert** + Authority → *"Show me the math"*
- **Senior executive** + Excessive detail → *"I don't have time"*
- **Risk-averse PM** + Novelty framing → *"Too risky"*
- **Data-driven leader** + Anecdotes only → *"Where's the evidence?"*

**Know your audience.** The wrong strategy is worse than no strategy.

---

<!-- _class: lead -->

# Part 5: Stakeholder-Strategy Integration
### *(12 minutes)*

---

## Stakeholder Map → Influence Strategy

Your Power-Interest Grid tells you **what to communicate**.

Your influence strategy tells you **how to communicate it**.

| Quadrant | Likely Effective Strategies |
|----------|----------------------------|
| High Power, High Interest | Authority + Consistency |
| High Power, Low Interest | Authority + Social Proof (efficiency) |
| Low Power, High Interest | Credibility + Social Proof |
| Low Power, Low Interest | Minimal engagement needed |

<!--
INSTRUCTOR NOTE:

**Background:** This is the critical integration slide. It connects Block 4's stakeholder mapping (Power-Interest Grid) with Block 5's influence strategies. Students should see how the two frameworks work together.

**Key point:** The grid tells you WHO to focus on; the strategy tells you HOW to persuade them. They're complements, not substitutes.

**Say something like:**
"This is where the two halves of Block 5 come together.

Your Power-Interest Grid tells you WHAT to communicate. High power, high interest? They need the full picture — detailed engagement. High power, low interest? Keep it brief — just tell them what they need to know.

Your influence strategy tells you HOW to communicate. Are they hierarchy-respecting? Use authority. Are they data-driven? Use credibility and social proof.

Let me walk through each quadrant:

High Power, High Interest: These are your 'Manage Closely' stakeholders. They have the power to approve or kill your project, and they care about the details. Lead with Authority — 'the CEO asked us to look at this' — and anchor with Consistency — 'this aligns with our Q2 priorities.' They need to see strategic alignment.

High Power, Low Interest: These are 'Keep Satisfied' stakeholders. They can veto, but they don't want details. Lead with Authority to get their attention, and use Social Proof to show efficiency — 'other teams have done this successfully; it won't require your time.' Make it easy to say yes.

Low Power, High Interest: These are 'Keep Informed' stakeholders. They care a lot but can't approve. Lead with Credibility — show them the rigor — and Social Proof — 'this is industry best practice.' They often become your champions if you earn their trust.

Low Power, Low Interest: Minimal engagement. A brief update is fine."

**If asked:** "What if someone is both hierarchy-respecting AND data-driven?"
A: Use both strategies. Authority to frame, Credibility to support. Most real stakeholders respond to multiple strategies — that's why we combine 2-3.

**Transition:** "Once you've mapped your stakeholders, you need to arm your champions and neutralize your blockers. Let's start with champions..."
-->

---

## Champions: How to Arm Them

Champions advocate for you in rooms you're not in.

**Give them:**
1. **The one-sentence summary** — What they'll say when asked
2. **The killer stat** — The number that makes the case
3. **Anticipated objections + responses** — So they can defend
4. **Your recommendation clearly** — So they don't misrepresent

---

## Blockers: How to Neutralize Them

Blockers resist. Understand why:

| Motivation | Strategy |
|------------|----------|
| **Threatens their budget** | Show mutual benefit, or acknowledge tradeoff |
| **Threatens their credibility** | Private conversation, collaborative framing |
| **Creates work for them** | Offer to help, phase the approach |
| **Past bad experience** | Acknowledge history, show what's different |

**Pre-brief blockers privately.** Never surprise them in a meeting.

---

## The Pre-Brief Framework

Before any major presentation:

1. **Identify who might be uncomfortable**
2. **Schedule 15-min 1:1** — "I want to get your input before the meeting"
3. **Share key findings** — No surprises
4. **Solicit feedback** — "What am I missing?"
5. **Incorporate reasonable feedback** — Shows you listened
6. **In the meeting** — They're prepared, not ambushed

This transforms blockers into (at worst) neutrals.

<!--
INSTRUCTOR NOTE:

**Background:** The pre-brief is the single most practical tactical skill in this block. Most analytical disasters happen because someone was surprised in a meeting. Pre-briefing uncomfortable findings transforms potential blockers into at-worst neutrals. The framing "I want to get your input" is crucial — it positions the meeting as collaborative, not combative.

**Key point:** Never surprise stakeholders with uncomfortable findings. The pre-brief is the most underused tactical skill in analytics.

**Say something like:**
"This is the single most actionable thing I'll teach you today. The pre-brief.

Before any major presentation where someone might be uncomfortable with your findings, do this:

First, identify who might be uncomfortable. Whose budget are you cutting? Whose project are you critiquing? Whose judgment are you questioning?

Second, schedule a 15-minute 1:1. Frame it as: 'I want to get your input before the meeting.' Not 'I need to warn you about something.' Input. Collaborative.

Third, share your key findings. No surprises. Let them react privately, not in front of their colleagues.

Fourth, solicit feedback genuinely. 'What am I missing?' They might actually have valid points you didn't consider. And even if they don't, you've given them a chance to be heard.

Fifth, incorporate reasonable feedback. If they had a good point, acknowledge it. This shows you listened.

In the meeting, they're prepared. They might still disagree — that's fine — but they won't be blindsided. The worst reaction is 'why am I hearing this for the first time in this meeting?'

This transforms blockers into, at worst, neutrals. Sometimes even into supporters."

**If asked:** "What if they're hostile in the pre-brief?"
A: Better to know now than in the meeting. If they're hostile privately, you have time to adjust your approach, involve their concerns in your narrative, or escalate to your sponsor if needed.

**Transition:** "Let me show you what this looks like in practice..."
-->

---

## Example: DataDash Attribution

**Scenario:** You're recommending $600K shift from Paid Search to LinkedIn.

**Blocker:** Paid Search manager (budget cut = career threat)

**Pre-brief approach:**
- Meet privately before presentation
- Frame: "I want to understand your perspective"
- Share findings early
- Ask: "What am I missing about how Search contributes?"
- Incorporate valid points
- In meeting: "As [name] and I discussed, there are tradeoffs here..."

---

<!-- _class: lead -->

# Part 6: Influence Planning Exercise
### *(15 minutes)*

---

## The Exercise

**Scenario:** You've completed a retention analysis for SnapGram showing that D7 retention dropped because the new onboarding flow is too aggressive.

**Your recommendation:** Simplify onboarding (remove mandatory friend-adding step).

**The problem:** The Growth PM who designed the new onboarding flow will be in the presentation. Their promotion case cited this launch.

<!--
INSTRUCTOR NOTE:

**Background:** This exercise integrates everything from Block 5: stakeholder awareness (the blocker), influence strategies, and message clarity. The scenario is deliberately uncomfortable — recommending something that makes a colleague look bad.

**Key point:** This is realistic. Many analytics findings imply someone's past work was wrong. How you handle it matters.

**Say something like:**
"Here's your scenario. You've done a retention analysis. You found that D7 retention dropped because the new onboarding flow is too aggressive — the mandatory friend-adding step is causing drop-off.

Your recommendation: simplify onboarding. Remove that mandatory step.

The problem: the Growth PM who designed that onboarding flow is in the room. And their recent promotion case cited that launch as a success. Your finding implies their promoted work... failed.

This is realistic. Analytics findings often imply someone was wrong. How you handle that determines whether your work gets acted on — or whether it dies politically."

**Transition:** "Take 3 minutes to think through your approach..."
-->

---

## Think (3 min)

> 1. What's your topic in 10 words?
> 2. What's your specific recommendation?
> 3. What influence strategies will you use?
> 4. How will you handle the Growth PM (blocker)?

Write down your answers.

---

## Pair (5 min)

> Share your approach with a partner.
>
> Challenge each other:
> - Is the recommendation specific enough?
> - Will the influence strategy work for this audience?
> - Is the blocker mitigation realistic?

---

## Share (10 min)

> **Groups share approaches:**
>
> Let's hear 3-4 different approaches to this scenario.

<!--
INSTRUCTOR NOTE:
Looking for:
- Topic: "Why retention dropped and how to fix it"
- Recommendation: "Remove mandatory friend-adding, A/B test simplified flow"
- Strategies: Credibility (data), Social Proof (correlation with retention drop), Consistency (retention is company priority)
- Blocker: Pre-brief, frame as "learning" not "failure", acknowledge their other contributions

Push back on weak approaches. Ask "What if the Growth PM pushes back with...?"
-->

---

## Debrief: What Makes Influence Work

1. **Know your audience** — One person, not "the team"
2. **Have a clear recommendation** — Specific action
3. **Choose strategies based on stakeholder** — Not one-size-fits-all
4. **Pre-brief blockers** — Never surprise
5. **Make it easy to understand** — Processing fluency

Influence isn't manipulation. It's clear communication + stakeholder awareness.

<!--
INSTRUCTOR NOTE:

**Background:** This is the synthesis slide after the influence exercise. The five principles distill everything from Block 5 into actionable guidance. This is what students should remember when they walk out.

**Key point:** These five principles are the "cheat sheet" for professional influence. If they remember nothing else, remember these.

**Say something like:**
"Let me pull together what we learned from that exercise and the block overall.

Five things that make influence work:

First, know your audience. One person, not 'the team.' Sarah the CFO, not 'leadership.' You can't influence 'the team' — you influence individuals with individual concerns.

Second, have a clear recommendation. A specific action, not 'we should think about this more.' Tell them exactly what you want: 'Shift $200K from paid social to referral program.' If you don't know what you want, how can they give it to you?

Third, choose strategies based on the stakeholder. Different people respond to different things. The technical lead wants credibility. The executive wants efficiency. The risk-averse PM wants social proof. Match the strategy to the person.

Fourth, pre-brief blockers. Never surprise anyone with uncomfortable findings in a meeting. That's when they get defensive and dig in. Private conversation first. Give them time to process. Incorporate their feedback. Then the public meeting is a formality.

Fifth, make it easy to understand. Processing fluency. Simple beats complex. If your recommendation is hard to understand, it's hard to trust. Do the work of simplification so they don't have to.

Here's the key reframe: Influence isn't manipulation. Manipulation involves deception. Influence is just clear communication plus stakeholder awareness. It's a professional skill, not a dark art."

**If asked:** "Which principle is most important?"
A: Pre-briefing blockers. It's the one that saves the most heartache. Everything else can be fixed in the moment. A blindsided blocker who digs in publicly? That's much harder to recover from.

**Transition:** "Let me summarize Block 5 overall..."
-->

---

## Block 5 Summary

| Concept | Key Takeaway |
|---------|--------------|
| **Processing Fluency** | Simple beats complex; make it easy to trust |
| **Message Theory** | Audience + Topic + Recommendation (all specific) |
| **Four Strategies** | Authority, Credibility, Social Proof, Consistency |
| **Stakeholder Connection** | Grid tells you what; strategy tells you how |
| **Blockers** | Pre-brief privately; never surprise |

<!--
INSTRUCTOR NOTE:

**Background:** This summary captures the five core concepts from Block 5. Students should leave with these five things in mind.

**Key point:** These five concepts work together — stakeholder map informs strategy choice, which is communicated with fluency and message clarity.

**Say something like:**
"Let me summarize what we covered.

Processing Fluency: Simple beats complex. Do the hard work of simplification. If they can't understand it quickly, they won't trust it.

Message Theory: Audience + Topic + Recommendation. All specific. Sarah the CFO, not 'leadership.' 10 words on the topic. A specific action.

Four Strategies: Authority, Credibility, Social Proof, Consistency. Different strategies for different stakeholders. Most presentations use 2-3.

Stakeholder Connection: The Power-Interest Grid tells you WHO to focus on. The influence strategies tell you HOW to persuade them. They work together.

Blockers: Pre-brief privately. Never surprise anyone with uncomfortable findings. This single practice will save you more grief than anything else we discussed."

**Transition:** "Questions before we break?"
-->

---

## Questions?

<!--
INSTRUCTOR NOTE:

**Background:** Final Q&A before the break. Keep it brief — afternoon energy depends on protecting the break.

**Key point:** End on time. The break matters.

**Facilitation:**
Take 2-3 questions maximum. Common questions:

"What if I don't have authority or credibility?"
A: Build it through the other strategies. Social proof and consistency don't require seniority. You can have strong influence without personal authority.

"Isn't this manipulative?"
A: Only if you're dishonest. Clear communication + stakeholder awareness is professional skill, not manipulation. Manipulation involves deception; influence involves clarity.

"How do I know which strategy to use?"
A: Start with your stakeholder map. Technical people respond to credibility. Risk-averse people respond to social proof. Hierarchy-respecting people respond to authority. Strategy-focused people respond to consistency.

**Say something like:**
"Quick questions before we break? [Take 2-3] Great — see you at 15:40 for Block 6. We'll talk about your capstone and close out the course."

**Transition:** Move to break slide.
-->

---

<!-- _class: lead -->
<!-- _paginate: false -->

# Break Time!

**Block 6 starts at 15:40**

Capstone Preparation & Closing

<!--
INSTRUCTOR NOTE:

**Background:** This is the final break before Block 6. Energy management is critical — afternoon blocks can drag if students are tired.

**Key point:** Protect the break. 30 minutes matters.

**Say something like:**
"Take a break. Coffee, snack, stretch, whatever you need. Block 6 starts at 15:40 — that's the capstone preparation and course closing. See you then."

**Logistics:**
- Break is ~30 minutes
- Block 6 is the final block of the course
- This is a good time to check in with students who seemed confused earlier
-->

