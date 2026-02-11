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

**Background:** This is Day 1, first substantive block. Students just sat through syllabus logistics. Energy may be low or nervous. Your job in the first 5 minutes is to establish psychological safety and signal that this class will be different from their technical courses.

**Key point:** Set the tone that this is interactive, practical, and safe to make mistakes.

**Say something like:**
"Before we get into content, let me check in. By show of hands — who's excited to be here? [Pause, hands up] Now who's terrified? [Pause, fewer hands] Here's the thing: both is the right answer. If you're only excited, you might not be taking it seriously enough. If you're only terrified, you'll be too tense to learn. The best place to be is a little of both.

This class is going to be different from your technical courses. I'm going to ask you questions. I'm going to cold-call people. Not to embarrass anyone — but because this material only makes sense when you engage with it. The Brief framework we're learning today isn't something you memorize. It's something you practice."

**If asked:** "Will you really cold-call us?"
A: Yes. But I'm not trying to catch you out. I'm trying to get you thinking. If you don't know, say 'I don't know' — that's a valid answer and we'll work through it together.

**Transition:** "Alright, let's start with a question that might surprise you..."
-->

---

## A Question to Start

> **Think for 30 seconds:**
>
> What percentage of data science projects actually deliver business value?

<!--
INSTRUCTOR NOTE:

**Background:** The "60-85% failure rate" comes from multiple industry studies (Gartner, VentureBeat, IDC, academic papers) over the past decade. Exact numbers vary — some say 60%, others 85% — but the pattern is consistent. Crucially, when researchers investigate WHY projects fail, it's almost never the model or the code. It's scoping, stakeholder misalignment, solving the wrong problem, or scope creep.

**Key point:** Technical skills are necessary but not sufficient. This course exists because the failure mode is upstream of the code.

**Say something like:**
"I want you to think about this for 30 seconds. Don't answer yet — just think. Of all the data science and analytics projects out there — in companies, in research, in startups — what percentage do you think actually deliver the business value they promised?"

[PAUSE — let silence sit for 30 seconds. Silence is uncomfortable but necessary.]

"Okay, let me hear some guesses. [Point to student] What's your guess?"

[Take 2-3 guesses. Usually students guess 40-60%.]

"Those are reasonable guesses. Here's what the research actually says: somewhere between 60 and 85 percent of data science projects FAIL to deliver their intended value. Let that sink in. That's not 'partial success' — that's failure. The project didn't do what it was supposed to do.

Now here's the part that matters for this course: when researchers dig into WHY these projects failed, it's almost never the model. The algorithm worked. The code ran. The pipeline deployed. But nobody used it. Or it solved the wrong problem. Or the stakeholder who was supposed to act on it had already moved on to something else.

That's what this course is about — the 80% of the iceberg that's underwater. The work that happens BEFORE you write code."

**If asked:** "Where does that statistic come from?"
A: Multiple sources — Gartner, VentureBeat surveys, academic studies by researchers like Bessen and Righi. Numbers vary by methodology, but the pattern is extremely consistent. I can share links after class if you want to dig deeper.

**If asked:** "What about successful projects — what do they do differently?"
A: Great question. That's exactly what we're going to learn today. Spoiler: they fill out something like the Brief before they start.

**Transition:** "So if it's not technical failure, what IS causing these projects to fail? Let me show you the four most common failure modes..."
-->

---

## Why Most Analytics Projects Fail

It's rarely the model. It's usually:

- **Wrong problem** — solved something nobody needed

- **Wrong metric** — optimized the wrong thing

- **Wrong stakeholders** — built it, nobody used it

- **Wrong scope** — took too long, world moved on

This course is about avoiding those failures.

<!--
INSTRUCTOR NOTE:

**Background:** These four failure modes come up again and again in post-mortems. Each one maps directly to a section of the Brief we'll teach today. This slide is the "hook" — it creates the problem that the Brief solves.

**Key point:** Failures happen upstream of technical work. None of these are model failures.

**Say something like:**
"Look at these four failure modes. Notice what's NOT on this list: 'The model was inaccurate.' 'The code had bugs.' 'The algorithm was wrong.' Those things happen, but they're rarely why projects fail to deliver value.

Wrong problem — you built something beautiful that answers a question nobody actually had. Wrong metric — you optimized the hell out of something, and in doing so, broke something else that mattered more. Wrong stakeholders — you delivered insights to someone who couldn't or wouldn't act on them. Wrong scope — you took so long that by the time you finished, the business had moved on to different priorities.

Every single one of these is preventable. That's what this course is about."

**If asked:** "What if the problem is actually technical?"
A: Then you fix the technical problem. But in my experience, by the time you've scoped correctly and aligned stakeholders, the technical problems are solvable. The unsolvable problems are usually the ones on this list.

**Transition:** "So what does this mean for what we're going to teach you? Let me be clear about what this course is — and isn't..."
-->

---

## What This Course Is NOT

❌ How to build models
❌ How to write Python/SQL
❌ Statistical methods
❌ Machine learning techniques

You have other courses for those.

<!--
INSTRUCTOR NOTE:

**Background:** Students in MSBA programs often expect every course to be technical. They may feel anxious that this course "doesn't count" or isn't teaching "real skills." This slide preempts that concern by explicitly validating their technical courses AND positioning this as complementary.

**Key point:** Technical skills are covered elsewhere. This course is about the skills you DON'T get in those courses.

**Say something like:**
"I want to be very clear about what this course is NOT. We're not going to teach you how to build models — you have other courses for that. We're not going to write Python or SQL together — same thing. Statistics, machine learning, all of that — covered elsewhere in your program.

If you came here hoping to learn gradient boosting, I apologize in advance. [Light laughter expected]

But here's the thing: those skills are necessary but not sufficient. You can be the best model builder in the world, and if you're solving the wrong problem or you can't get stakeholders to act on your insights, none of it matters."

**Transition:** "So what IS this course? Let me tell you..."
-->

---

## What This Course IS

✅ The work that happens **before** you write code
✅ How to scope projects that actually matter
✅ How to navigate organizational dynamics
✅ How to avoid the most common failure modes

**One framework. Applied repeatedly.**

<!--
INSTRUCTOR NOTE:

**Background:** Students often wonder why "soft skills" courses exist in technical programs. The answer is that the gap between technical capability and business impact is filled by the skills this course teaches. This slide is the positive framing after the negative framing of the previous slide.

**Key point:** One framework (the Brief), applied repeatedly across different contexts. Simplicity is the point.

**Say something like:**
"This is what we're actually going to teach you. The work that happens before you write code. How to figure out which projects actually matter — because not all data science projects are created equal. How to navigate the political realities of organizations — because your analysis lives or dies based on whether stakeholders act on it. And how to avoid the four failure modes we just talked about.

Here's the good news: it's one framework. The Analytics Project Brief. You're going to learn it once, and then you're going to apply it over and over in different contexts. By the end of this course, filling out a Brief will be second nature."

**If asked:** "Will we use this in our capstone?"
A: Absolutely. The capstone project explicitly requires a Brief. This course is designed to prepare you for that.

**Transition:** "And all of this serves a single throughline — the reason data science exists at all..."
-->

---

## The Throughline

Your job — as a data scientist, analyst, or anyone working with data — is simple:

# Drive better decisions with data.

That's it. Everything else is in service of this.

<!--
INSTRUCTOR NOTE:

**Background:** This is the philosophical anchor of the course. Students often define their value as "building models" or "writing code." This reframes their purpose at a higher level of abstraction. This framing also helps when they encounter career uncertainty — job titles change, but this core purpose remains.

**Key point:** Your value is in decisions improved, not models deployed.

**Say something like:**
"I want you to remember this statement. Write it down if you want. Your job — as a data scientist, analyst, ML engineer, whatever title you end up with — is to drive better decisions with data.

Not to build models. Not to write code. Not to create dashboards. Those are all tools. The purpose — the reason anyone pays you money — is that decisions in the organization get better because of your work.

When you frame your work this way, everything changes. A beautiful model that nobody uses? Failure. A simple spreadsheet analysis that changes a $10M decision? Success. The output format doesn't matter. The decision quality matters."

**If asked:** "What if my job is just to maintain data pipelines?"
A: Even then, you're enabling better decisions by ensuring data quality. The decision-support chain has many links. But always ask yourself: 'What decisions am I enabling?'

**Transition:** "And when we look at failures through this lens, we see what goes wrong..."
-->

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

<!--
INSTRUCTOR NOTE:

**Background:** This slide is the "aha moment" — students should see that the Brief isn't bureaucracy, it's prevention. Each row in this table maps directly to a Brief section they'll learn. This creates motivation for the framework before they see the details.

**Key point:** The Brief exists because each section prevents a specific failure mode.

**Say something like:**
"Look at this table carefully. Each row is a failure mode, and each one maps to a section of the Brief.

'Solved something nobody needed' — that's what happens when you skip the Problem & Decision section. No clear decision to drive means you're doing analysis for its own sake.

'Optimized the wrong thing' — that's the counter-metrics section. We'll spend a lot of time on this one because it's the most commonly skipped.

'Built it, nobody used it' — stakeholder mapping. You delivered great work to someone who couldn't or wouldn't act on it.

'Didn't see the disaster coming' — the pre-mortem. You didn't imagine failure, so you didn't prevent it.

The Brief isn't paperwork. It's a checklist of things that kill projects when you skip them."

**If asked:** "Can't we just keep these in our heads?"
A: You can try. But under pressure, you'll skip steps. The Brief forces you to slow down and check each box. It's like a pilot's pre-flight checklist — even experienced pilots use it every time.

**Transition:** "So let's look at this single artifact that prevents all four failures..."
-->

---

## The Single Artifact

Everything in this course revolves around one thing:

# The Analytics Project Brief

A structured framework that forces clarity **before** you start analyzing.

<!--
INSTRUCTOR NOTE:

**Background:** This slide anchors the entire course around one artifact. Students may expect a survey of many tools and techniques. Instead, they're getting depth on one framework. This intentional simplicity is a pedagogical choice — mastery comes from repeated application, not from knowing many things superficially.

**Key point:** One artifact, applied repeatedly. Depth over breadth.

**Say something like:**
"[Pause on the big heading]

This is it. The Analytics Project Brief. One artifact. You're going to learn it today, and you're going to use it for the rest of your career.

I know that might sound like an exaggeration. But here's the thing: every analytics project needs scoping. Every one. Whether you call it a 'Brief' or a 'project charter' or 'requirements doc' — the questions are the same. What decision are we driving? What metrics? Who are the stakeholders? What could go wrong?

By learning this framework deeply — applying it to nine different analyses over the next two days — you'll internalize the questions. Eventually, you won't need the template. The questions will be automatic."

**If asked:** "Is this a standard industry framework?"
A: The specific format is mine, but the questions are universal. Every good PM, every good data scientist, asks these questions — whether they write them down or not. The Brief just makes it explicit and systematic.

**Transition:** "Let me tell you what you'll be able to do by the end of this course..."
-->

---

## Learning Outcomes

By the end of this course, you will be able to:

1. **Use the Analytics Project Brief** to scope projects

2. **Identify counter-metrics** and stakeholder dynamics

3. **Recognize which analyses** apply to different problems

4. **Apply influence strategies** to gain buy-in

<!--
INSTRUCTOR NOTE:

**Background:** These four outcomes map to the course structure: Brief (Blocks 1-3), counter-metrics (Block 1), analyses (Blocks 2-3), and influence (Block 5). Each outcome is assessed — #1 and #2 in the Brief assignment and exam, #3 in the exam, #4 in week 5-6 write-ups.

**Key point:** Four outcomes. Each will be assessed. This is your accountability checklist.

**Say something like:**
"Four outcomes. By the end of these two days, you'll be able to do each of these.

[Point to each one]

Use the Brief to scope projects — that's the core skill. By tomorrow, filling out a Brief should feel natural.

Identify counter-metrics and stakeholder dynamics — you'll learn frameworks for both today. Counter-metrics in about an hour. Stakeholders tomorrow.

Recognize which analyses apply — we'll cover nine foundational analyses in Blocks 2 and 3. Given a business problem, you should know which analysis fits.

Apply influence strategies — that's Block 5 tomorrow. How to actually get stakeholders to act on your findings.

These aren't aspirational. They're what you'll be tested on. The exam, the assignment, the write-ups — they all map to these outcomes."

**Transition:** "Speaking of assessment, here's how you'll be graded..."
-->

---

## Assessment Overview

| Component | Weight | When |
|-----------|--------|------|
| Scenario → Brief | 30% | Jan 16 |
| Pen & Paper Exam | 30% | Jan 27 |
| Weekly Write-ups | 30% | Jan 23 – Feb 27 |
| Participation | 10% | During class |

Each of you gets a **unique scenario** for the Brief assignment.
No two students have the same one.

<!--
INSTRUCTOR NOTE:

**Background:** The unique scenarios prevent collaboration that crosses into copying. With 18 scenarios distributed randomly, students can discuss approaches but can't share answers. This also means grading will show variation — there's no single "right answer" to compare against, only quality of reasoning.

**Key point:** Unique scenarios mean you can discuss approaches with classmates, but you can't copy.

**Say something like:**
"Let me highlight something about the Brief assignment. Each of you gets a unique scenario. There are 18 different scenarios, assigned randomly. No two students have the same one.

Why does this matter? It means you can — and should — discuss the Brief framework with your classmates. Talk about how to structure counter-metrics. Debate stakeholder strategies. That's learning.

But you can't copy each other's work, because you're working on different problems. Your Quickcart funnel analysis is different from their MindfulApp retention problem.

This also means there's no single 'right answer.' I'm grading quality of reasoning, not matching against an answer key. A thoughtful, well-reasoned Brief for a difficult scenario beats a formulaic Brief for an easy one."

**Transition:** "Here's how today fits into the full two days..."
-->

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

<!--
INSTRUCTOR NOTE:

**Background:** This roadmap helps students orient themselves and manage energy across a long day. The "you are here" marker reduces anxiety. Mentioning breaks signals that you respect their attention spans.

**Key point:** Quick orientation. Don't linger — it's just a map.

**Say something like:**
"Here's today. [Point to table] You are here — Block 1, the Analytics Project Brief. This runs until 12:30.

After lunch, we cover acquisition analyses: funnel, attribution, campaign effectiveness, CAC/LTV. That's Block 2.

After a break, we finish with retention and growth analyses: retention curves, power users, failure analysis, expansion, ecosystems. Nine analyses total by end of day.

By 5:20 today, you'll know the Brief framework and have seen all nine foundational analyses in action. Tomorrow we practice, go deep on stakeholders and influence, and connect everything to your capstone."

**Transition:** "Any questions before we start the framework itself?"
-->

---

## Questions Before We Dive In?

<!--
INSTRUCTOR NOTE:

**Background:** This is a transition point before Part 2. Students may have questions about logistics, assessment, or high-level course structure. Keep this short — 2-3 questions max — to maintain momentum into the Brief framework.

**Key point:** Big picture questions only. Details come later.

**Say something like:**
"Before we dive into the Brief framework, any questions? Big picture questions only — the details will become clear as we go through each section.

[Take 2-3 questions, redirect detailed questions]

If someone asks about specific Brief sections: 'Good question — we'll cover that in detail in about 10 minutes. Hold that thought.'

If someone asks about the assignment: 'You'll get your scenario after class today. The Brief template is in the course repo. We'll work through examples so you know what 'good' looks like.'

If no questions: 'Great. Let's dive in.'"

**Transition:** "Alright, let's look at why we need a structured framework at all..."
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

<!--
INSTRUCTOR NOTE:

**Background:** This scenario happens constantly in industry. An eager analyst takes a vague request, interprets it their way, works for weeks, and delivers something the requester didn't want. The exec isn't wrong — they had something specific in mind but didn't articulate it. The analyst isn't wrong — they tried their best with limited information. The problem is the process.

**Key point:** Hard conversations now prevent wasted work later.

**Say something like:**
"Let me tell you about a pattern I've seen dozens of times. An executive walks up to a data scientist and says, 'Can you look into why revenue is down?' The data scientist says 'Sure!' — because they want to be helpful, they want to show they can deliver.

Three weeks later, the data scientist comes back with a beautiful analysis of customer churn patterns. The exec looks at it and says, 'This isn't what I wanted. I already know we have churn. I wanted to know if the new pricing is causing it.'

Who's at fault? [Pause] Neither of them. The exec had something specific in mind but didn't say it. The analyst made reasonable assumptions but didn't verify them. The failure is the PROCESS.

The Brief exists to force those hard conversations upfront. Instead of 'Sure!', you say, 'Let me write up a one-page Brief so we're aligned on scope.' Takes 30 minutes. Saves 3 weeks."

**If asked:** "What if the exec doesn't want to spend time on alignment?"
A: Then you have important information: this isn't a real priority. If someone won't spend 15 minutes aligning on scope, they probably won't spend the time to act on your findings either.

**Transition:** "So let's look at what this framework actually contains..."
-->

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

<!--
INSTRUCTOR NOTE:

**Background:** The Brief has 10 sections, but they're not all created equal. Sections 1-3 (Problem, Metrics, Stakeholders) are where most failures occur. Section 10 (Pre-Mortem) is the most under-utilized but high-value section. Students don't need to memorize the numbers — they need to internalize the questions.

**Key point:** The Brief is structured around questions, not answers.

**Say something like:**
"Ten sections might sound like a lot, but each one is just answering a question. And notice these are questions that any reasonable person would ask before starting a project.

What decision will this inform? — Because if there's no decision at stake, why are we doing this?
What are we optimizing? What breaks? — Because every optimization has tradeoffs.
Who has power? Who might block? — Because analysis is useless if the right people don't act on it.

We're going to go through each of these sections in detail. But I want you to notice: none of these are technical questions. They're strategic and political questions. That's deliberate."

**If asked:** "Do we have to fill out all 10 sections for every project?"
A: For the assignment, yes. In practice, some sections are lighter for smaller projects. But Problem, Metrics, and Stakeholders are always critical.

**Transition:** "Let me show you the second half of the framework..."
-->

---

## The Analytics Project Brief (cont.)

| # | Section | Key Question |
|---|---------|--------------|
| 6 | Success Criteria | How will we know this worked? |
| 7 | Timeline | Key milestones? |
| 8 | Risks & Assumptions | What could go wrong? |
| 9 | Ethics & Privacy | PII? Bias risks? |
| 10 | Pre-Mortem | It failed. What happened? |

<!--
INSTRUCTOR NOTE:

**Background:** Sections 6-10 are the "downstream" sections — they assume you've already defined the problem, metrics, and stakeholders. Section 10 (Pre-Mortem) is the most valuable but most skipped. Ethics & Privacy (Section 9) is increasingly important and often overlooked by students focused on technical execution.

**Key point:** The second half of the Brief is about planning for success and failure.

**Say something like:**
"Sections 6 through 10. These are the 'what happens after' sections.

Success Criteria — not just 'the analysis is done,' but 'how do we know it was good?' What makes this valuable?

Timeline — keep it simple. Key milestones. When do we check in?

Risks & Assumptions — what are you taking for granted? What could invalidate your analysis?

Ethics & Privacy — this one's important. Does your analysis require personal data? Could it harm certain groups? We'll touch on this briefly, but it's a career-long consideration.

Pre-Mortem — [pause] this is my favorite section. We'll spend time on this. 'It failed. What happened?' Imagining failure in advance is how you prevent it."

**Transition:** "Let me dive deep into Section 1 — Problem & Decision..."
-->

---

## Section 1: Problem & Decision

The most important section. Everything flows from here.

**Three questions to answer:**
1. What business question will this analysis inform?

2. Who is asking, and why now?

3. Who is the ultimate decision maker?

<!--
INSTRUCTOR NOTE:

**Background:** This section is where most project failures are seeded. Students (and professionals) often skip to methodology because it's comfortable. The hard work of aligning on the decision is uncomfortable. "Who is asking and why now?" uncovers urgency and political context. "Ultimate decision maker" prevents building for the wrong audience.

**Key point:** If you can't answer these three questions, STOP. You're not ready to start.

**Say something like:**
"This is the most important section of the Brief. Everything else flows from here. Get this wrong, and nothing else matters.

Three questions. Write them down.

First: What business question will this analysis inform? Notice I didn't say 'what question will this analysis answer.' You inform decisions. Rarely do you answer questions definitively. But there has to be a decision at stake.

Second: Who is asking, and why now? [Pause] Why is this question important? [Cold call a student]

[Expected answer: urgency, priorities, context]

Exactly. 'Why now?' tells you a lot. Is this urgent because of a quarterly review? Because a competitor launched something? Because someone's job is on the line? That context shapes everything — your timeline, your framing, your stakeholder strategy.

Third: Who is the ultimate decision maker? Not 'who is sponsoring' — who will actually decide. Sometimes the same person. Often not. You need to know who you're ultimately serving."

**If asked:** "What if I don't know who the decision maker is?"
A: Then your first task is to find out. Ask your sponsor: 'Once this analysis is done, who decides what we do with it?' If they can't answer, that's a red flag.

**Transition:** "You should also include a hypothesis..."
-->

---

## Section 1: The Hypothesis

Also include a hypothesis:

> *We believe [X] because [Y], and this analysis will confirm or refute that.*

**Why?** Forces you to be specific about what you expect to find.

If you don't have a hypothesis, that's okay — mark it as **exploratory**.

<!--
INSTRUCTOR NOTE:

**Background:** The hypothesis forces pre-commitment and prevents fishing for results. Without a hypothesis, it's easy to analyze data, find any pattern, and present it as if you'd expected it. The "because [Y]" part is crucial — it surfaces your reasoning and makes the hypothesis testable.

**Key point:** A hypothesis isn't a prediction to be right about — it's a commitment to intellectual honesty.

**Say something like:**
"A hypothesis forces you to put a stake in the ground. 'We believe X because Y, and this analysis will confirm or refute that.'

The 'because Y' part is critical. It's not enough to say 'We believe mobile users convert less.' You have to say 'We believe mobile users convert less BECAUSE the checkout flow has 3 more steps on mobile than desktop.' Now you have a testable claim.

And here's the key thing: you're not trying to be right. You're trying to be honest about what you expect. If you have no hypothesis — you're genuinely exploring — that's fine. Just say so explicitly. Write 'This is exploratory. We don't have a hypothesis; we're looking for patterns.'

What you can't do is pretend to be exploratory, fish around in the data until you find something, and then act like you knew it all along. That's how bad analytics gets published."

**If asked:** "What if our hypothesis is wrong?"
A: Great! That's a result. You learned something. A refuted hypothesis is still valuable. What you can't accept is a vague question that can't be refuted.

**Transition:** "Let me check that we're all following..."
-->

---

## Check for Understanding

> **Quick check:**
> Why is "Who is asking and why now?" important?

<!--
INSTRUCTOR NOTE:

**Background:** This is a formative assessment moment — checking that students understood the Problem & Decision section before moving on. Cold calling creates engagement and surfaces confusion early. Expected answers should connect "why now" to urgency, political context, or priority signals.

**Key point:** Cold call to check understanding. Validate good answers; correct misconceptions.

**Say something like:**
"Quick check. I want to make sure we're all following.

[Cold call a student by name]

'[Name], why is 'Who is asking and why now?' important?'

[Wait for answer]

**Good answers include:**
- Urgency: 'Why now' tells you the timeline and how much pressure there is
- Political context: Understanding who's asking helps you navigate stakeholders
- Priority signal: If someone can't explain 'why now,' it might not be a real priority
- Resource implications: 'Why now' often reveals what resources are available or constrained

**If the answer is weak:**
'Good start. Let me add to that. The 'why now' question often reveals political context. Is this urgent because of a board meeting? A competitor launch? Someone's job on the line? That context shapes everything about how you approach the project.'

**If the answer is strong:**
'Exactly. You've internalized the key insight. The 'why now' is never just about timing — it's about context, urgency, and politics.'"

**Transition:** "Now let's look at the second section — Metrics..."
-->

---

## Section 2: Metrics

Two parts:

### Primary Metric
What are you optimizing? **Be precise.**

❌ "Conversion rate"
✅ "Users who complete checkout / Users who reach cart page, excluding guest checkout, trailing 7 days"

<!--
INSTRUCTOR NOTE:

**Background:** Imprecise metric definitions are one of the top causes of analytics project failure. "Conversion rate" can mean a dozen different things — different numerators, different denominators, different time windows, different exclusions. The precision standard we're teaching here is "could you write the SQL from this definition?" If not, it's not precise enough.

**Key point:** If you can't write the SQL from the definition, it's not defined.

**Say something like:**
"Two parts to the metrics section. Let's start with the primary metric — what are you optimizing?

The most important thing I'll teach you about metrics is this: be precise. [Point to the ❌ example] 'Conversion rate' is NOT a metric definition. It's a category. Ten people in a room will interpret 'conversion rate' ten different ways.

What's the numerator? Users? Sessions? Orders? What's the denominator? All visitors? Cart viewers? Signed-in users? What time window? What exclusions?

[Point to the ✅ example] THIS is a metric definition. 'Users who complete checkout divided by users who reach cart page, excluding guest checkout, trailing 7 days.'

Someone could write SQL from this. That's the test. If an engineer can't write a query from your metric definition, you haven't defined it yet."

**If asked:** "Isn't this overkill for early-stage exploration?"
A: For exploratory work, you can be looser. But once you're making recommendations or measuring success, precision is non-negotiable. Get in the habit now.

**Transition:** "Let me show you what a complete metric definition looks like..."
-->

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

<!--
INSTRUCTOR NOTE:

**Background:** This table is a checklist for metric precision. Students should use this as a template when defining metrics in their Brief assignments. Missing any component leads to ambiguity. The "Event/table" component is often forgotten — it specifies WHERE the data comes from, which matters for data quality and availability.

**Key point:** Walk through each row. Every row matters.

**Say something like:**
"Let me walk through each component. [Point to each row]

Event/table: What data source are you using? 'checkout_completed' events from the events table? 'orders' from the orders table? This matters because different tables have different quality, different latency, different definitions.

Numerator: What's on top of the fraction? Users, sessions, transactions? Be specific.

Denominator: What's on the bottom? This is where people mess up most often. 'Conversion rate' with an undefined denominator is meaningless.

Filters: What are you excluding? Guest checkout, internal users, test accounts, international markets? Every filter needs to be explicit.

Time window: Trailing 7 days? Calendar month? Since product launch? Time windows change your numbers dramatically.

[Pause]

In your Brief assignment, I want to see this table filled out. Not 'conversion rate' — THIS."

**If asked:** "What if I don't know the exact table names?"
A: Use placeholders like '[user_events table]' — but be specific about what KIND of data you need. The specificity forces clarity even if you don't know the exact schema.

**Transition:** "Now, the other half of the metrics section — counter-metrics..."
-->

---

## Section 2: Counter-Metrics

We'll go deep on this in Part 3, but the key idea:

> **Counter-metrics** are what breaks if your primary metric succeeds.

You optimize checkout completion → Revenue per order drops (people buying cheaper stuff)

Always identify 2-3 counter-metrics.

<!--
INSTRUCTOR NOTE:

**Background:** This is a preview of Part 3 content. Don't go deep here — just plant the seed. The key idea is that success on one metric can cause failure on another. The checkout example is intuitive and will be expanded later.

**Key point:** Preview only. We'll go deep in Part 3.

**Say something like:**
"Counter-metrics. We'll spend 35 minutes on this in Part 3, so I'll just preview the concept now.

[Read the definition]

Counter-metrics are what breaks if your primary metric succeeds. Not fails — succeeds. If you WIN, something else loses.

Example: you optimize checkout completion. More people complete checkout — great! But they're buying cheaper stuff. Revenue per order drops. Your 'success' created a new problem.

For your Brief, you need 2-3 counter-metrics. Not zero — that means you haven't thought hard enough. Not ten — that means you're overthinking or haven't prioritized.

We'll learn how to systematically find them in Part 3."

**Transition:** "Now let me show you a discussion exercise on metric precision..."
-->

---

## Discussion: Metric Precision

> **Think-Pair-Share (2 min):**
>
> Someone says their metric is "user engagement."
> What questions would you ask to make this precise?

<!--
INSTRUCTOR NOTE:

**Background:** "User engagement" is the canonical vague metric. This exercise trains students to instinctively push for precision. The Think-Pair-Share format (think alone → discuss with neighbor → share with class) builds confidence before public speaking.

**Key point:** Practice the instinct to push for precision. "Engagement" is never specific enough.

**Say something like:**
"Think-Pair-Share. I'll give you a vague metric, and you'll figure out what questions to ask.

Someone says their metric is 'user engagement.'

[Set timer or watch]

30 seconds: think individually. What questions would you ask?
1 minute: turn to your neighbor and compare notes.
30 seconds: we'll share out.

[After ~2 minutes total]

'Okay, let's hear it. [Point to a pair] What questions did you come up with?'

**Expected questions:**
- What counts as engagement? Logins? Time spent? Actions taken? Messages sent?
- Engagement by whom? All users? Active users? New users?
- Over what time period? Daily? Weekly? Monthly?
- What's the denominator? Engaged users / all users? Engaged sessions / all sessions?
- What threshold? One action counts? Five actions?

[After 2-3 contributions]

'Great. Notice what just happened. You instinctively knew 'engagement' was too vague. You asked the right questions. That instinct is what I want you to carry into every project. When someone says 'engagement' or 'conversion' or 'retention' — your first response should be: 'Define it precisely.''"

**Transition:** "Now let's look at stakeholders..."
-->

---

## Section 3: Stakeholders

Use the **Power-Interest Grid**:

|   | High Interest | Low Interest |
|---|---------------|--------------|
| **High Power** | Manage Closely | Keep Satisfied |
| **Low Power** | Keep Informed | Monitor |

<!--
INSTRUCTOR NOTE:

**Background:** The Power-Interest Grid (also called the Mendelow Matrix) is a classic stakeholder management tool from the 1990s. It's simple but effective: plot stakeholders by their power (ability to affect the project) and interest (motivation to do so). Different quadrants need different engagement strategies.

**Key point:** Not all stakeholders are equal. Spend energy proportional to their power and interest.

**Say something like:**
"The Power-Interest Grid is a simple tool that works. Two axes: power and interest.

Power means: can this person kill the project, starve it of resources, or block implementation? Interest means: do they care enough to get involved?

High power, high interest — manage closely. These are your sponsors and key stakeholders. Update them frequently. Get their input. Don't surprise them.

High power, low interest — keep satisfied. They can kill your project but don't care about details. Don't bother them with updates, but make sure they're not unhappy.

Low power, high interest — keep informed. They care a lot but can't really affect the outcome. Helpful as advocates but don't let them consume your time.

Low power, low interest — monitor. Check in occasionally but don't invest energy here.

When you fill out this grid, you should end up with specific names in each quadrant — not just roles."

**If asked:** "How do I know someone's power level?"
A: Ask: Can this person approve or deny budget? Block implementation? Fire or promote you? Influence someone who can? If yes to any of these, they have power.

**Transition:** "Beyond the grid, you need to identify champions and blockers..."
-->

---

## Section 3: Champions & Blockers

Beyond the grid, identify:

**Champions** — Who actively wants this to succeed?
**Blockers** — Who might resist? *Why* do they resist?

The "why" matters. People block for reasons:
- Threatens their budget

- Makes their past work look bad

- Creates work for their team

<!--
INSTRUCTOR NOTE:

**Background:** Students often think politics is dirty or that good work speaks for itself. It doesn't. Every project has blockers, and understanding WHY they block is the key to neutralizing resistance. The three reasons listed (budget, reputation, workload) cover most blocking behavior.

**Key point:** Blockers aren't irrational. They're protecting something. Understand what.

**Say something like:**
"Beyond the grid, you need to identify two specific roles: champions and blockers.

Champions are people who actively want your project to succeed. They'll advocate for you in meetings you're not in. They'll defend your timeline when someone wants to cut it. Identify them explicitly — you'll need their help.

Blockers are people who will resist. And here's the thing: every project has blockers. If you write 'no blockers' in your Brief, you haven't thought hard enough.

But the key isn't just identifying blockers — it's understanding WHY they block. Nobody thinks of themselves as a blocker. They have reasons that are rational from their perspective.

[Point to bullets]

Threatens their budget: Your project requires engineering resources that would come from their team's allocation.

Makes their past work look bad: You're analyzing why their previous initiative didn't work. If you find problems, their judgment looks poor.

Creates work for their team: Even if your findings are great, implementing them falls on their team. More work, same headcount.

When you understand the motivation, you can address it. Private pre-briefs. Reframing. Including them in the solution. You can't neutralize a blocker you don't understand."

**If asked:** "What if the blocker is my manager?"
A: Then you have a serious problem that the Brief just surfaced. Better to know now than after you've invested months.

**Transition:** "Let's move on to methodology..."
-->

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

<!--
INSTRUCTOR NOTE:

**Background:** The Methodology section is where technical planning meets strategic clarity. Students often want to dive straight into methods, but this section forces them to think about data availability first. The fallback column is crucial — it acknowledges that data is rarely perfect and plans accordingly.

**Key point:** Plan for imperfect data. The fallback column is where realism lives.

**Say something like:**
"Section 4 is where you get tactical. Two parts.

First: which analyses? You'll learn nine foundational analyses in Blocks 2 and 3. Funnel analysis, attribution, retention curves, and so on. For your Brief, you'll select which ones apply to your problem. Usually 1-3 analyses per project.

Second: data availability. This table forces you to be realistic. [Point to table]

What data do you need? Is it available? If no — and it's often no — what's your fallback?

See that 'Partial' in the middle column? That's realistic. You wanted all purchase history; you only have 6 months. So your fallback is: use what you have, acknowledge the limitation.

The fallback column is where good analysts separate from naive ones. Naive analysts assume data will be perfect. Good analysts plan for imperfection."

**Transition:** "Related to data availability — you need to validate your data before analyzing..."
-->

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

**Background:** Data validity checks are the most commonly skipped part of the Brief. Students (and professionals) want to start analyzing immediately. But bad data in = bad conclusions out. The stop conditions are critical — they define what "broken" means and prevent subjective judgment after seeing results.

**Key point:** This is a grading criterion. Generic "check data quality" gets zero points.

**Say something like:**
"Data validity checks. This is the most commonly skipped part of the Brief, and I'm grading you on it.

[Point to the table]

See the structure? Each check has three parts: What you're checking. How you validate it. When you stop.

Not 'we'll check data quality.' That's meaningless. Instead: 'We'll verify iOS events fire correctly by comparing iOS vs Android event counts. If discrepancy exceeds 10%, we stop and investigate before drawing conclusions.'

[Pause for emphasis]

The stop condition is critical. Without it, you'll rationalize. 'Well, there's some data quality issues, but probably fine...' No. Define the stop condition in advance. 10% discrepancy? Stop. 1% duplicates? Stop. This protects you from your own optimism.

**Grading note:** Your Brief must include 2+ specific checks with validation method AND stop condition. Generic statements get zero points for this section."

**If asked:** "What if we hit a stop condition and the data is actually fine?"
A: Great — you investigated and confirmed. That's the process working. Better to stop and verify than to build an analysis on broken data.

**Transition:** "Okay, let's take a quick break to recharge..."
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

<!--
INSTRUCTOR NOTE:

**Background:** Scope creep is one of the top project killers. The "Out of Scope" section is more important than "In Scope" because it prevents assumptions about what you'll do. Every item in "Out of Scope" is something someone might assume you'd include. Being explicit prevents the "but I thought you were also doing X" conversation.

**Key point:** The "Out of Scope" section prevents scope creep. It's the most important part.

**Say something like:**
"Scope & Deliverables. This is your contract with stakeholders.

In Scope is straightforward — what ARE you doing? US market, 6 months of data, web platforms.

Out of Scope is more important. [Point to the list] These are things someone might ASSUME you're doing. Native app? 'Oh, I thought you were looking at the app too.' International? 'Wait, you're not including Europe?'

Every item in Out of Scope is a future argument you're preventing. If it's not explicitly out, someone will assume it's in.

Here's a technique: ask stakeholders, 'What else might you expect from this project that I should explicitly exclude?' Their answers go in Out of Scope. Now you have documented agreement."

**If asked:** "What if stakeholders want to add scope later?"
A: Point to the Brief. 'We agreed this was out of scope. We can add it, but let's revisit timeline and resources.' The Brief gives you leverage.

**Transition:** "Now, how will you know if the project succeeded..."
-->

---

## Section 6: Success & Decision Criteria

**Analytical success:** What makes the analysis itself good?
- Metric defined with <20% confidence interval

- 3+ statistically significant drivers identified

**Business success:** What makes it valuable?
- Product team changes roadmap based on findings

- Clear A/B test hypotheses generated

<!--
INSTRUCTOR NOTE:

**Background:** Separating analytical success from business success prevents two failure modes: (1) great analysis that nobody uses, (2) sloppy analysis that drives decisions by coincidence. Students often focus only on analytical quality and forget that the ultimate goal is business impact.

**Key point:** Two types of success. Both matter. Neither is sufficient alone.

**Say something like:**
"Two types of success, and you need both.

Analytical success — was the analysis good? Did you achieve statistical rigor? Are your confidence intervals tight enough? Did you find clear drivers, not just noise?

This is what most analysts focus on. And it matters — sloppy analysis is dangerous. But it's not enough.

Business success — did it matter? Did anyone change their behavior based on your findings? Did the product team actually change their roadmap? Did you generate testable hypotheses that someone ran?

Here's the uncomfortable truth: a mediocre analysis that changes a $10M decision is more valuable than a brilliant analysis that sits in a deck nobody reads. I'm not saying be sloppy — but don't confuse analytical elegance with business impact.

Your Brief should define both. What makes the analysis sound? What makes it valuable?"

**Transition:** "Let me show you how to pre-commit to decisions..."
-->

---

## Section 6: Decision Criteria Table

Pre-commit to decisions:

| If we find... | We will... |
|---------------|------------|
| Checkout friction is #1 driver | Prioritize UX redesign |
| Price sensitivity is #1 driver | Test promotional strategy |
| No clear driver found | Run qualitative user research |

**Including the null result.** What if you find nothing?

<!--
INSTRUCTOR NOTE:

**Background:** This table is one of the most under-utilized tools in analytics. By pre-committing to actions before seeing results, you prevent post-hoc rationalization and ensure the analysis drives decisions. The null result row is critical — most analysts don't plan for "we didn't find anything conclusive," which leads to scope creep or wasted work.

**Key point:** Pre-commit to actions. Especially for the null result.

**Say something like:**
"This table is powerful. You're pre-committing to what you'll do BEFORE you see the results.

Why does this matter? Because without pre-commitment, here's what happens: you run the analysis, you find something sort of interesting, and you tell a story about why it matters. That's not decision-making — that's rationalization.

Pre-commitment forces honesty. If checkout friction is the #1 driver, we do UX redesign. If it's price sensitivity, we test promotions. You decide the action thresholds before you're biased by the results.

[Point to last row]

And here's the row most people skip: the null result. What if you don't find anything clear? What if the data is inconclusive?

If you haven't planned for that, you'll thrash. You'll extend the analysis. You'll try new cuts of the data. That's scope creep disguised as thoroughness.

Instead, plan for it: 'If we find no clear driver, we run qualitative user research.' Now you know what to do if the data doesn't give you a clear answer."

**If asked:** "What if stakeholders want to change the criteria after seeing results?"
A: Push back. Politely. 'We agreed to these criteria upfront. If we change them now, we're just finding reasons to do what we already wanted to do.' Pre-commitment only works if you hold to it.

**Transition:** "Related to this — you need action thresholds..."
-->

---

## Section 6: Action Thresholds

Be specific about magnitude:

> "We will only recommend action if effect size ≥5 percentage points AND p<0.05"

> "We will not act if sample size <1000 users per variant"

This prevents "statistically significant but meaningless" results driving decisions.

<!--
INSTRUCTOR NOTE:

**Background:** Action thresholds prevent the "statistically significant but practically meaningless" trap. A 0.1% improvement with p<0.01 is real but worthless if the cost of acting exceeds the benefit. Students from statistics backgrounds may over-index on p-values; this section forces them to think about practical significance.

**Key point:** Statistical significance ≠ practical significance. Define both thresholds.

**Say something like:**
"Action thresholds. This is how you prevent the 'technically true but useless' trap.

[Read the first quote]

Two conditions: effect size AND statistical significance. You need both. Why?

You can have a tiny effect that's statistically significant with enough data. A 0.01% improvement in conversion might be 'real' — it shows up with p<0.05 in your A/B test — but is it worth changing the product for? Probably not.

[Read the second quote]

This is the opposite case. You found something interesting, but your sample size is tiny. Are you confident it's real? Not yet. Don't act.

The action threshold forces you to define what matters BEFORE you see results. What effect size is worth acting on? What sample size gives you confidence? Write it down. Pre-commit. Otherwise, you'll rationalize whatever you find."

**If asked:** "How do I know what effect size to set?"
A: Work backwards from cost/benefit. If the action costs $100K to implement, what's the minimum benefit that justifies that? That's your threshold.

**Transition:** "Sections 7-9 are lighter — let me cover them quickly..."
-->

---

## Sections 7-9: Quick Overview

**Timeline:** Key milestones and dates. Keep it simple.

**Risks & Assumptions:** What are you assuming is true? What could invalidate the analysis?

**Ethics & Privacy:** Does this require PII? Any bias risks? GDPR considerations?

<!--
INSTRUCTOR NOTE:

**Background:** Sections 7-9 get compressed treatment because they're more straightforward than 1-6 and 10. However, Ethics & Privacy (Section 9) is increasingly important and students should know it exists even if we don't deep-dive.

**Key point:** Quick coverage. Ethics & Privacy deserves a mention even in the compressed version.

**Say something like:**
"Sections 7, 8, and 9 are more straightforward, so let me cover them quickly.

Timeline — just key milestones. When do you check in? When do you deliver? Don't over-engineer this.

Risks & Assumptions — what are you taking for granted? If you assume the data is complete, say so. If the analysis is invalidated by a product change, note that risk.

Ethics & Privacy — [slow down slightly] this one matters more than students often realize. Does your analysis require personal data? Could your findings be used to harm certain user groups? Are there GDPR or privacy implications?

In your career, you'll face situations where technically you COULD do an analysis, but you shouldn't. Section 9 is where you surface those considerations before you start, not after someone raises concerns."

**Transition:** "Now, the most valuable section that people skip — the Pre-Mortem..."
-->

---

## Section 10: Pre-Mortem

The most valuable section.

> **Prompt:** It's 3 months from now. This project failed spectacularly. What happened?

Write it as a story. Be specific. Be pessimistic.

This surfaces risks you wouldn't otherwise consider.

<!--
INSTRUCTOR NOTE:

**Background:** The pre-mortem was popularized by psychologist Gary Klein. Research shows that "prospective hindsight" — imagining an event has already happened — increases ability to identify reasons for outcomes by 30%. It's psychologically easier to explain failure after imagining it happened than to abstractly list risks. The pre-mortem also creates psychological safety to name concerns.

**Key point:** A pre-mortem isn't pessimism — it's structured imagination that surfaces risks you'd otherwise miss.

**Say something like:**
"This might be the most valuable section of the Brief, and it's the one people skip most often. The pre-mortem.

Here's the prompt: It's three months from now. This project failed spectacularly. Write the story of what happened.

Not 'what might go wrong' — that's too abstract. What DID go wrong. Write it as if you're explaining to your manager why the project failed. Be specific. Be pessimistic. Be honest.

Why does this work? Psychology research shows that when you imagine something has already happened — psychologists call it 'prospective hindsight' — you're 30% better at identifying reasons than if you try to predict the future abstractly. It's easier to explain a failure than to predict one.

And there's a social benefit too. In a team setting, saying 'Here's what might go wrong' can feel like you're being negative. Saying 'Here's how this failed in my pre-mortem' is just... doing the exercise. It creates safety to name concerns."

**If asked:** "How long should a pre-mortem be?"
A: A paragraph to a page. Enough to tell a specific story with a causal chain. Not a bulleted list of risks — that's a different exercise.

**Transition:** "Let me show you what a good pre-mortem looks like..."
-->

---

## Example Pre-Mortem

> We found that mobile users converted 40% less than desktop. Product redesigned the mobile checkout flow.
>
> Three months later, mobile conversion was flat. Turns out mobile users were just *browsing* — they always completed purchases on desktop. We solved the wrong problem because we didn't segment by user journey, just by device.

<!--
INSTRUCTOR NOTE:

**Background:** This example illustrates a common failure mode: confusing correlation with causation and not understanding user behavior before optimizing. Mobile conversion rates are a classic analytics trap — the numbers look actionable but the causal story is often wrong.

**Key point:** A good pre-mortem has a causal chain: we did X → because of Y → which caused Z. The lesson is implicit in the story.

**Say something like:**
"Look at the structure of this pre-mortem. It's not just 'mobile conversion didn't improve.' It tells a causal story.

We found a data pattern: mobile users convert less. We acted on it: redesigned mobile checkout. We failed: conversion stayed flat. Here's why: mobile users weren't trying to convert — they were browsing. They always intended to buy on desktop.

The lesson is implicit: we should have segmented by user journey, not just by device. We would have seen that users who browse on mobile and buy on desktop are the same people.

This is what I want your pre-mortems to look like. A story with causation, not just a list of things that went wrong. When you write 'we didn't have good data' — that's not a pre-mortem. When you write 'we assumed the signup event fired on iOS the same way it did on Android, but iOS users appeared to have 40% lower signup rates because the event was misconfigured' — that's a pre-mortem."

**If asked:** "Is this example realistic?"
A: Very. Multi-device user journeys are one of the most common traps in analytics. People research on mobile, buy on desktop, or vice versa. If you don't track users across devices, you'll draw wrong conclusions.

**Transition:** "So let me summarize the key principle for using the Brief..."
-->

---

## The Brief in Practice

Key principle:

> **Fill out the Brief before you start analyzing.**

Not after. Not during. Before.

It will feel slow at first. It saves time overall.

<!--
INSTRUCTOR NOTE:

**Background:** This is the behavioral change the course requires. Students' instinct is to start analyzing immediately — it feels productive. The Brief feels like overhead. But analysis without scoping is how projects fail. The "slow at first, saves time overall" framing helps students accept the upfront cost.

**Key point:** Before. Not during. Not after. BEFORE.

**Say something like:**
"I want you to remember this principle. It's the single most important behavioral change this course asks of you.

Fill out the Brief BEFORE you start analyzing.

Not after — that's just documentation. Not during — that's retrofitting. BEFORE.

[Pause]

I know what you're thinking: 'But I need to explore the data to know what's possible.' Fair. You can do light exploration to understand what data exists. But the moment you start building a model, writing a dashboard, or running a regression — you should have a Brief.

It will feel slow at first. 30 minutes to scope before a 3-week project feels like overhead. But that 30 minutes prevents you from spending 3 weeks on the wrong question. It prevents the 'this isn't what I wanted' conversation.

The Brief is an investment. It pays for itself."

**If asked:** "What if requirements change mid-project?"
A: Update the Brief. It's a living document. But having the original Brief means you can point to what changed and why. 'We originally scoped X, but stakeholder feedback shifted us to Y.' That's accountability, not rigidity.

**Transition:** "Any questions on the framework before we move to Part 3?"
-->

---

## Questions on the Framework?

<!--
INSTRUCTOR NOTE:

**Background:** This is the transition between Part 2 (the Brief framework) and Part 3 (counter-metrics deep dive). Students may have questions about sections we covered quickly or want clarification before moving on. This is also a good moment to gauge energy and understanding.

**Key point:** Take 3-4 questions. Common questions have prepared answers.

**Say something like:**
"Questions on the framework before we move to Part 3?

[Take 3-4 questions]

**Common questions and answers:**

Q: 'How long does filling out a Brief take?'
A: 30-60 minutes once you're practiced. First few times, longer — maybe 2 hours. But that time investment pays off in weeks of saved rework.

Q: 'Do I need to fill out every section for every project?'
A: For the assignment, yes. In practice, some sections are lighter for smaller projects. But Problem, Metrics, and Stakeholders are always essential.

Q: 'What if my stakeholder won't spend time on alignment?'
A: That's valuable information — they may not care enough to act on your findings. Better to learn that now than after you've done the work.

Q: 'Can I iterate on the Brief?'
A: Absolutely. It's a living document. But start with your best guess before analyzing. Update as you learn.

[If time is running short]
'Let me hold remaining questions — we'll have another Q&A at the end of Part 3.'"

**Transition:** "Alright, Part 3: Counter-Metrics and Adversarial Thinking. This is where we go deep on Goodhart's Law..."
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

<!--
INSTRUCTOR NOTE:

**Background:** Goodhart's Law is foundational to understanding counter-metrics. Charles Goodhart was a British economist who observed this pattern in monetary policy. The law applies everywhere: education, healthcare, tech, government. The second quote ("tell me how you measure me") is often attributed to Eli Goldratt and is more visceral.

**Key point:** Metrics change behavior, and not always in the direction you want.

**Say something like:**
"This is one of the most important ideas in analytics. Charles Goodhart was a British economist who noticed something troubling: the moment you use a measure to control behavior, it stops measuring what you think it measures.

[Read the quote on screen]

Here's the more visceral version: 'Tell me how you measure me, and I'll tell you how I'll behave.'

Think about that. It's not cynical — it's human nature. If you tell me my bonus depends on X, I'm going to optimize for X. And if X is imperfectly correlated with what you actually care about, I'm going to find the gap and exploit it. Not maliciously — just rationally.

This is why counter-metrics exist. You can't just set a target and walk away. You have to ask: 'What happens when people start gaming this?'"

**If asked:** "Is this the same as Campbell's Law?"
A: Yes, very similar. Campbell focused on social programs, Goodhart on economics. Same insight: measurement changes behavior.

**Transition:** "Let me show you some examples of this in practice..."
-->

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

<!--
INSTRUCTOR NOTE:

**Background:** These three examples span public sector (healthcare, education) and private sector (tech) to show the universality of the pattern. Students in a business analytics program will relate most to the tech example, but the healthcare and education examples are less politically charged.

**Key point:** This pattern is universal. It's not about bad actors — it's about rational responses to incentive structures.

**Say something like:**
"Let me walk through three examples. Healthcare: hospitals get measured on length of stay because payers don't want to pay for unnecessarily long hospitalizations. What happened? Hospitals discharged patients earlier. Length of stay went down — metric improved! But readmissions spiked because people were sent home before they were ready. The metric looked great. The outcome was worse.

Education: No Child Left Behind measured schools on test scores. Teachers started teaching to the test — because their jobs depended on it. Test scores went up. But ask any educator what happened to critical thinking, creativity, deep understanding. The metric went up; the thing the metric was supposed to measure went down.

Tech: social media companies measured engagement. What gets engagement? Outrage. Conflict. Emotional provocation. The algorithm optimized for what kept people scrolling, and what keeps people scrolling isn't what's good for them. We're still dealing with the consequences.

In none of these cases were the people involved evil. They responded rationally to the incentives they were given. That's Goodhart's Law."

**If asked:** "How do you prevent this?"
A: Counter-metrics. In healthcare, you'd track readmission rates alongside length of stay. In education, you'd measure critical thinking alongside test scores. In tech — well, some companies are starting to track 'regretted sessions.'

**Transition:** "So what does this mean for you, specifically?"
-->

---

## The Problem for Data Scientists

You're often asked to optimize a metric.

If you succeed, **something else gets worse**.

Your job is to figure out what that is **before** you start.

<!--
INSTRUCTOR NOTE:

**Background:** This slide frames the problem that counter-metrics solve. Students may not have encountered the "everything has tradeoffs" mindset yet. In school, problems often have single right answers. In industry, every optimization creates losers. This is the setup for the counter-metrics framework.

**Key point:** Optimization always has tradeoffs. Your job is to anticipate them.

**Say something like:**
"Here's the reality of your job. Someone will come to you and say 'optimize this metric.' Increase signups. Reduce churn. Improve engagement.

And if you succeed — if you ACTUALLY make that metric go up — I can almost guarantee something else will get worse.

Increase signups? Maybe signup quality drops. Reduce churn? Maybe you're just annoying people into staying. Improve engagement? Maybe you're addicting people to junk.

This isn't pessimism — it's physics. Resources are finite. User attention is finite. Optimizing one thing takes resources from another. Every win has a cost.

Your job is to figure out what that cost is BEFORE you start. Not after you've shipped something that looked great on the target metric but broke something else."

**If asked:** "Are there ever pure wins with no tradeoffs?"
A: Rarely. Sometimes you find genuine inefficiencies — waste that can be eliminated. But even then, eliminating waste often means someone's job changes, someone's process gets disrupted. There's almost always a cost, even if it's worth paying.

**Transition:** "So let's define this more precisely — what is a counter-metric?"
-->

---

## Counter-Metrics Defined

> **Counter-metric:** A metric that could worsen if you optimize the primary metric.

Two types:

| Type | Definition | Example |
|------|------------|---------|
| **Guardrail** | Must not worsen | Data quality, fraud rate |
| **Tradeoff** | May worsen within bounds | Short-term revenue for LTV |

<!--
INSTRUCTOR NOTE:

**Background:** The guardrail vs. tradeoff distinction is crucial for operational clarity. Guardrails are hard stops — if they move in the wrong direction, you kill the project. Tradeoffs are acceptable costs — you expect them to worsen but within limits. Students often struggle with this distinction because it requires judgment about what's negotiable.

**Key point:** Guardrails are hard stops. Tradeoffs are acceptable costs. Know which is which.

**Say something like:**
"Let me define counter-metric precisely: it's a metric that could worsen if you optimize the primary metric. Not 'will worsen' — 'could worsen.' You're identifying risks.

Two types, and the distinction matters.

[Point to Guardrail row]

Guardrails are hard stops. If this metric worsens, you kill the project. Full stop. Examples: data quality drops below acceptable levels, fraud rate spikes, you break legal compliance. These aren't negotiable. If you hit a guardrail, you roll back.

[Point to Tradeoff row]

Tradeoffs are different. You expect them to worsen — that's the cost of your optimization. But you accept it within bounds. Example: you invest in long-term retention, and short-term revenue dips temporarily. That's okay — you planned for it. But if short-term revenue drops 50%, that's beyond acceptable bounds.

When you write counter-metrics in your Brief, label each one. Is it a guardrail or a tradeoff? What are the bounds for tradeoffs? This operational clarity prevents arguments later."

**If asked:** "Who decides what's a guardrail vs. tradeoff?"
A: Ideally, stakeholders decide with your input. You bring the options; they decide what's acceptable. But push them to be explicit — 'Is fraud rate a hard stop or just something to monitor?'

**Transition:** "Now, how do you find counter-metrics? Here's a systematic framework..."
-->

---

## The "What Breaks" Framework

Five questions to find counter-metrics:

1. **Direct negative:** What directly worsens when X improves?

2. **Quality degradation:** What quality suffers?

3. **User segments:** Which users are harmed?

4. **Temporal tradeoffs:** What long-term metrics suffer?

5. **Cross-functional:** Whose goals are threatened?

<!--
INSTRUCTOR NOTE:

**Background:** The "What Breaks" framework is a practical tool for finding counter-metrics. Each question targets a different failure mode. Students should use this systematically when identifying counter-metrics for their assignments.

**Key point:** These five questions are a checklist. Use all five for every project.

**Say something like:**
"Here's a practical framework for finding counter-metrics. Five questions. Write them down.

First: Direct negative. What directly gets worse when your metric improves? If you increase checkout completion, maybe revenue per order drops because people buy the minimum to finish quickly.

Second: Quality degradation. What quality suffers? If you increase content production, maybe content quality drops. If you speed up customer service, maybe resolution quality suffers.

Third: User segments. Which users are harmed? This is often the most overlooked. When you optimize for the average user, you often hurt edge cases. Power users. New users. Users with disabilities. International users. Someone usually gets worse treatment.

Fourth: Temporal tradeoffs. What long-term metrics suffer? Short-term revenue vs. LTV. Engagement today vs. retention next month. Shipping features fast vs. technical debt.

Fifth: Cross-functional. Whose goals are threatened? Your metric improves, but another team's metric gets worse. Sales vs. support. Growth vs. quality. These create organizational tension — often the source of blockers.

Use all five questions for every project. You won't always have answers for all five, but asking the questions is what matters."

**If asked:** "Do we need a counter-metric from each category?"
A: No. You need 2-3 total, from whichever categories are most relevant. But check all five categories.

**Transition:** "Let me show you what this looks like in practice..."
-->

---

## Example: Checkout Optimization

**Primary metric:** Checkout completion rate

**What breaks?**
1. Revenue per order (people buy cheaper stuff to "just finish")

2. Return rate (impulse purchases get returned)

3. Customer service load (confused customers)

4. Fraud rate (less friction = more fraud)

<!--
INSTRUCTOR NOTE:

**Background:** This is a concrete worked example. Students should see how the "What Breaks" framework generates specific counter-metrics. Each counter-metric has a clear causal story — if X improves, Y worsens because Z. Walk through each one to model the thinking process.

**Key point:** Each counter-metric has a causal story. Spell out the mechanism.

**Say something like:**
"Let me walk through a concrete example. Primary metric: checkout completion rate. We want more people to complete checkout.

[Point to each item]

Revenue per order — if we simplify checkout, if we remove upsells and cross-sells, people complete faster but they buy less. They 'just finish' without adding to cart. The metric improves; revenue suffers.

Return rate — if checkout is TOO easy, people impulse-buy. Fast checkout means less time to reconsider. Those impulse purchases get returned. Returns cost money and erode trust.

Customer service load — counterintuitive, right? If we simplify checkout, shouldn't that reduce support tickets? Not necessarily. If we change the flow, people get confused. 'Where did my cart go?' 'Why can't I find the promo code field?' Change creates support load, even good change.

Fraud rate — this is the big one. Friction in checkout isn't just annoying — it's also a fraud signal. Adding CVV, address verification, CAPTCHAs — these slow down checkout but they also slow down fraudsters. Remove friction, and fraud goes up.

Four counter-metrics, each with a causal story. That's the level of thinking I want in your Briefs."

**Transition:** "Let me show you another example with a different domain..."
-->

---

## Example: Notification Optimization

**Primary metric:** Click-through rate on notifications

**What breaks?**
1. Notification opt-out rate (annoy people → they disable)

2. App uninstalls (too many notifications → rage quit)

3. Session quality (clicked but didn't engage)

4. User trust (feels spammy → brand damage)

<!--
INSTRUCTOR NOTE:

**Background:** Notification optimization is a classic case of Goodhart's Law in tech. Easy to measure clicks, hard to measure annoyance. This example shows how short-term metric improvement can destroy long-term user relationships. It's also a good example of cross-functional tension — growth team wants clicks, brand team cares about trust.

**Key point:** Short-term metric success can destroy long-term value. Notifications are the canonical example.

**Say something like:**
"Different domain, same pattern. Primary metric: notification click-through rate. Every growth team optimizes this.

[Walk through each item]

Opt-out rate — the more notifications you send, the more clicks you get... until people opt out entirely. Once they opt out, you've lost that channel forever. Optimizing short-term CTR destroys long-term reach.

App uninstalls — even worse than opt-out. Some users don't bother finding the settings. They just delete the app. Your notification optimization just cost you a customer.

Session quality — this is subtle. Someone clicks a notification. Great! Metric goes up! But then they look around for 3 seconds, realize it's not what they wanted, and leave. You got a click but not engagement. If you only measure clicks, you'll never see this.

User trust — hardest to measure, most damaging to break. Users start associating your brand with spam. This affects everything — willingness to recommend, tolerance for errors, benefit of the doubt. Brand damage doesn't show up in your click metrics."

**If asked:** "How do you measure brand damage or user trust?"
A: NPS scores, survey data, qualitative research. Harder to measure, slower to move, but critical. Some companies track 'regretted sends' — users who opt out or uninstall within X days of a notification campaign.

**Transition:** "Now let's practice. I'll give you a primary metric, you find the counter-metrics..."
-->

---

## Discussion: Find the Counter-Metrics

> **Think-Pair-Share (3 min):**
>
> Primary metric: "Increase free-to-paid conversion rate"
>
> What could break if you succeed?

<!--
INSTRUCTOR NOTE:

**Background:** Free-to-paid conversion is a common freemium metric and illustrates multiple counter-metric categories. This exercise applies the "What Breaks" framework to a realistic scenario. Students should generate 3-4 counter-metrics using the framework they just learned.

**Key point:** Apply the "What Breaks" framework. Expect 3-4 distinct counter-metrics.

**Say something like:**
"Let's practice. Think-Pair-Share.

Primary metric: increase free-to-paid conversion rate. You want more free users to become paying customers.

If you succeed — if conversion rate goes UP — what could break?

1 minute: think individually. Use the 'What Breaks' framework.
2 minutes: discuss with your neighbor.
Then we'll share out.

[After ~3 minutes]

'Okay, let's hear it. [Point to a pair] What counter-metrics did you identify?'

**Expected answers:**
- **Paid user churn:** Pushed people to convert before they were ready → they churn faster
- **Free user satisfaction/NPS:** Made the free tier worse to push conversions → free users hate you
- **Brand perception:** Aggressive conversion tactics → seen as 'pushy' or 'sleazy'
- **Support load:** Confused upgrades → more support tickets
- **LTV of converted users:** Converted low-intent users → lower average LTV
- **Viral/referral rate:** Unhappy free users don't recommend you

[After 2-3 contributions]

'Great range of answers. Notice how each one tells a causal story: if we push conversions too hard, THEN this bad thing happens. That's the quality of thinking I want in your Briefs.'"

**Transition:** "Now, let me show you the right number of counter-metrics..."
-->

---

## How Many Counter-Metrics?

**2-3 is right.**

Too few: You're not thinking hard enough
Too many: Analysis paralysis, false positive problem

Every additional guardrail at p<0.05 adds ~5% false alarm rate.

<!--
INSTRUCTOR NOTE:

**Background:** The "2-3" guidance is practical wisdom from experimentation. Too few counter-metrics means you haven't done adversarial thinking. Too many creates the multiple comparisons problem — with 20 guardrails at p<0.05, you expect 1 false alarm by chance. The statistical point about false alarm rate is worth emphasizing for students with stats backgrounds.

**Key point:** 2-3 is the sweet spot. It's not arbitrary — it's practical wisdom.

**Say something like:**
"How many counter-metrics should you have? The answer is 2-3. Not zero. Not ten. 2-3.

Why not zero? If you can't think of a single thing that could go wrong when you optimize your metric, you haven't thought hard enough. Go back and use the 'What Breaks' framework.

Why not ten? Two reasons.

First, analysis paralysis. If you have 10 counter-metrics, you'll never act on anything. Something will always be moving in the wrong direction. You'll be stuck in endless monitoring.

Second, statistics. [Point to the false alarm rate line] If you test 20 guardrails at p<0.05, you expect one false alarm by chance — just random noise that looks like a problem. The more guardrails you add, the more false alarms you'll chase.

2-3 forces you to prioritize. Which counter-metrics are MOST important? Those make the list. The rest you can monitor informally."

**If asked:** "What if I genuinely have 5 critical counter-metrics?"
A: Challenge yourself: are they all equally critical? Usually, 2-3 are existential and the others are 'nice to track.' Promote the existential ones; demote the rest.

**Transition:** "Now, the distinction between guardrails and tradeoffs..."
-->

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

<!--
INSTRUCTOR NOTE:

**Background:** This reinforces the guardrail/tradeoff distinction with concrete examples. Students need to understand that guardrails are non-negotiable — they represent organizational values and risk tolerance. Tradeoffs require judgment and bounds. The act of labeling forces clarity about what's actually important.

**Key point:** Guardrails are organizational values. Tradeoffs are judgment calls. The labeling creates accountability.

**Say something like:**
"Let me make this concrete. Look at the guardrails list: fraud rate, data quality, legal compliance.

These aren't negotiable because they represent organizational values. If fraud rate spikes, it doesn't matter how good your checkout completion numbers look — you've created risk that could sink the company. If data quality drops, every downstream analysis is suspect. If you break legal compliance, you're exposing the company to lawsuits and fines.

Guardrails are the 'we will never accept this' list. If you hit one, you stop. You roll back. You don't negotiate.

[Point to tradeoffs]

Tradeoffs are different. Short-term revenue might drop if you invest in retention — that's expected. You're trading present value for future value. Acceptable, as long as the drop is within bounds. Complexity might increase if you add a valuable feature. Acceptable, as long as it doesn't become unmaintainable.

The key is: you have to label them. In your Brief, every counter-metric should say 'Guardrail' or 'Tradeoff.' If it's a tradeoff, what are the bounds? How much is acceptable? This prevents arguments later when someone says 'but revenue dropped' and you can say 'yes, we expected that — it's within the 10% bound we agreed to.'"

**If asked:** "What if stakeholders disagree on what's a guardrail?"
A: That's a conversation worth having BEFORE you start. Better to surface that disagreement during scoping than during review.

**Transition:** "Now let's put all of this into practice with an exercise..."
-->

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

**Background:** This is the first hands-on pre-mortem exercise. Students write individually to develop the skill before sharing. The "50% signup increase" goal is aggressive enough to trigger creative failure scenarios. The 5 minutes of writing time is important — resist the urge to cut it short.

**Key point:** Silent writing time is essential. Let them think. Silence is productive.

**Say something like:**
"Time to practice. Individual exercise — 5 minutes of writing.

[Read the scenario aloud]

You're tasked with increasing user signups by 50% in Q1. That's aggressive. It's the end of Q1. The project failed spectacularly.

Your job: write a 2-3 sentence pre-mortem. What happened? Be specific — not 'it didn't work,' but 'here's the causal chain of what went wrong.' Then identify: what counter-metric would have caught this early?

5 minutes. Write. I'll be quiet.

[Set timer. Walk around the room. Silence is okay — productive thinking looks like people staring at their notebooks.]

[At 4 minutes]
'One more minute.'

[At 5 minutes]
'Pens down. Let's hear some failure stories.'"

**If students struggle to start:**
"Think about HOW you might hit that 50% target. What shortcuts might you take? Now imagine those shortcuts backfiring."

**Transition:** "Now let's share — I want to hear your failure stories..."
-->

---

## Pre-Mortem Sharing

Let's hear some failure stories.

<!--
INSTRUCTOR NOTE:

**Background:** This is the debrief of the pre-mortem exercise. Cold calling ensures participation and creates learning from diverse failure scenarios. The follow-up question ("What counter-metric would have caught this?") connects pre-mortems back to the counter-metrics framework.

**Key point:** Cold call 3-4 students. Always follow up with "What counter-metric would have caught this?"

**Say something like:**
"Alright, let's hear some failure stories.

[Cold call by name]

'[Name], what happened in your pre-mortem? Read it to us.'

[After they share]

'Good. Now, what counter-metric would have caught this early?'

[Repeat for 3-4 students]

**Common pre-mortems and counter-metrics:**

1. **Signup quality dropped:**
   'We hit 50% more signups, but they were junk. Bots, fake emails, people who never returned. D7 retention showed the problem — new signups had 10% D7 retention vs. 40% for previous cohorts.'
   Counter-metric: D7 or D30 retention of new signups

2. **Fraud increased:**
   'We removed friction from signup to hit the target. Fraud rings noticed. Fake accounts spiked, and we spent Q2 cleaning up the mess.'
   Counter-metric: Fraud rate, fake account detection rate

3. **Support overwhelmed:**
   'We launched aggressive campaigns that brought in confused users. Support tickets per signup tripled. The team burned out.'
   Counter-metric: Support tickets per new signup

4. **Brand damaged:**
   'We used dark patterns — hiding the 'skip' button, pre-checking boxes. Signups went up. So did complaints on Twitter. Our NPS dropped 20 points.'
   Counter-metric: NPS, social sentiment, complaint rate

[After 3-4 shares]

'Notice the pattern. Every failure scenario has a counter-metric that would have caught it early. That's why we define counter-metrics in advance — so we see the problem before it becomes a disaster.'"

**Transition:** "Let me explain why pre-mortems work psychologically..."
-->

---

## Why Pre-Mortems Work

Psychology research shows:

- **Prospective hindsight** increases ability to identify reasons for outcomes by 30%

- Easier to generate specific failures than abstract risks

- Creates psychological safety to name concerns

It's not pessimism. It's **preparation**.

<!--
INSTRUCTOR NOTE:

**Background:** The psychology research on prospective hindsight comes from Deborah Mitchell, Gary Klein, and colleagues (1989). The 30% improvement in identifying reasons is from their experimental studies. The key insight is that the brain processes "what happened" differently from "what might happen" — the former engages causal reasoning more effectively.

**Key point:** Pre-mortems work because of how the brain processes causality. It's not just a technique — it's leveraging cognitive science.

**Say something like:**
"Why do pre-mortems work? It's not just a productivity trick — there's psychology behind it.

[Point to first bullet]

Prospective hindsight: when you imagine something has already happened, your brain processes it differently. You shift from 'what might happen' — which is vague and abstract — to 'what did happen' — which triggers causal reasoning. Research shows this improves your ability to identify reasons by about 30%.

[Point to second bullet]

It's easier to generate specific failures than abstract risks. If I ask 'what could go wrong?' you get vague answers. If I ask 'it failed — what happened?' you get specific stories.

[Point to third bullet]

Psychological safety. In a team setting, saying 'this might fail because...' can feel negative, like you're being a downer. But saying 'in my pre-mortem, the project failed because...' is just doing the exercise. Same content, different framing. People feel safer naming concerns.

This isn't pessimism. It's strategic imagination. You're not hoping for failure — you're preparing to prevent it."

**Transition:** "Now let's summarize the key takeaways from our counter-metrics discussion..."
-->

---

## Key Takeaways: Counter-Metrics

1. **Every metric optimization breaks something else**

2. **Use the "What Breaks" framework** to find counter-metrics

3. **Identify 2-3** — not zero, not twenty

4. **Label as Guardrail or Tradeoff**

5. **Pre-mortem** surfaces risks you'd otherwise miss

<!--
INSTRUCTOR NOTE:

**Background:** Takeaway slides reinforce key learnings. These five points are the minimum students should remember from Part 3. Consider having students repeat them back or write them down.

**Key point:** Five points. If they remember nothing else, remember these.

**Say something like:**
"Five takeaways from Part 3. Write these down.

[Point to each one, pause]

One: Every metric optimization breaks something else. That's the foundational insight. Internalize it.

Two: Use the 'What Breaks' framework. Five questions to systematically find counter-metrics.

Three: 2-3 counter-metrics. Not zero — that means you haven't thought. Not twenty — that means you haven't prioritized.

Four: Label each as Guardrail or Tradeoff. Guardrails are hard stops. Tradeoffs are acceptable costs.

Five: Pre-mortems surface risks you'd otherwise miss. Imagine failure to prevent it.

[Pause]

Can someone repeat these back to me? [Cold call]"

**Transition:** "Let me recap the entire block..."
-->

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

<!--
INSTRUCTOR NOTE:

**Background:** Recaps help with retention. The three key takeaways map to the three parts of Block 1. Students should be able to repeat these by the end of the day.

**Key point:** If students remember nothing else, remember these three things.

**Say something like:**
"Let me summarize what we've covered. Three key takeaways.

First: One framework, applied repeatedly. The Analytics Project Brief. You're going to use this for your assignment, for the exam, and for your capstone. The framework itself is simple — the skill is in applying it well.

Second: 10 sections — fill it out BEFORE you analyze. Not during. Not after. Before. The Brief exists to prevent wasted work, not to document work you've already done.

Third: What breaks if you succeed? This is the counter-metrics question. Goodhart's Law. Every optimization creates unintended consequences. Your job is to anticipate them.

If you remember nothing else from this block, remember these three things. [Pause] Can someone repeat them back to me? [Cold call]"

**If asked:** "Will this be on the exam?"
A: Yes. The exam will ask you to complete Brief sections for a new scenario. Everything we covered today is fair game.

**Transition:** "Before lunch, let me preview what's coming in Block 2..."
-->

---

## Before Next Block

We'll cover the **9 foundational analyses** in Blocks 2-3.

Each one will be introduced through a completed Brief example.

**After lunch:** Funnel, Channel Attribution, Campaign Effectiveness, CAC/LTV

<!--
INSTRUCTOR NOTE:

**Background:** This preview sets expectations for the afternoon and creates continuity across the lunch break. Students should know what's coming so they can mentally prepare. The Brief connection reinforces that the framework is applied throughout.

**Key point:** Preview what's coming. Maintain the Brief connection.

**Say something like:**
"Here's what's coming after lunch.

We'll cover the nine foundational analyses in Blocks 2 and 3. These are the analyses you'll use most often in your career: funnel analysis, attribution, campaign measurement, retention curves, and so on.

Each analysis will be introduced through a completed Brief example. You'll see how the framework applies to real problems. By the end of today, you'll have nine worked examples in the course repo — one for each analysis.

After lunch: Funnel, Channel Attribution, Campaign Effectiveness, CAC/LTV. Four acquisition analyses. These are about getting customers.

Enjoy lunch. We start at 1:30 sharp."

**Transition:** "Final questions before we break?"
-->

---

## Questions?

<!--
INSTRUCTOR NOTE:

**Background:** Final Q&A before lunch. Keep it brief — lunch time is sacred for energy management. If many hands go up, promise to address remaining questions after lunch or via email.

**Key point:** 2-3 questions max. End on time. Respect the break.

**Say something like:**
"Final questions before lunch?

[Take 2-3 questions]

[If many hands]
'I see lots of hands. Let me take 2 more, and I'll catch the rest after lunch or via email. I want to respect your break time.'

[Common end-of-block questions:]

Q: 'When do we get our scenarios?'
A: Today after class. Check your email tonight.

Q: 'How long should the Brief assignment be?'
A: Fill out the template completely. Quality matters more than length. A tight 3-page Brief beats a rambling 10-page one.

Q: 'Will you share these slides?'
A: They're in the course repo. You have access.

[Wrap up]
'Great block. You now have the framework. After lunch, we see it in action with real analyses. Enjoy your break — 1:30 sharp.'"
-->

---

<!-- _class: lead -->
<!-- _paginate: false -->

# See you after lunch!

**Block 2 starts at 13:30**

Acquisition Analyses: Funnel → Attribution → Campaign → CAC/LTV
