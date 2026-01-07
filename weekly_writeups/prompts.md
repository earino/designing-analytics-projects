# Weekly Write-Up Prompts

## Overview

These 6 weekly prompts span February 10 through March 17. They prepare you for your capstone project through practice exercises and concept application.

**Structure:**
- **Weeks 1-6 (Feb 10 – Mar 17):** Concept practice, capstone search journey, skill building
- **Your actual capstone Brief** is built through the PID process (due Mar 30), not these write-ups

**Grading:** Pass/Fail
**Length:** ~1 page per write-up
**Submission:** Via LMS by Monday 23:59 CET each week

| Week | Due Date | Topic |
|------|----------|-------|
| 1 | Feb 10 | Capstone Search Kickoff |
| 2 | Feb 17 | Counter-Metrics in the Wild |
| 3 | Feb 24 | Analysis Methodology Selection |
| 4 | Mar 3 | Evaluating Project Opportunities |
| 5 | Mar 10 | Pre-Mortem on a Hypothetical |
| 6 | Mar 17 | Capstone Readiness Check |

---

## Week 1: Capstone Search Kickoff (Due: Feb 10)

### Prompt

Document the start of your capstone search journey.

**Your submission should address:**

1. **Where Are You Looking?**
   - What sources are you exploring? (employer, personal network, CEU database, cold outreach, nonprofits)
   - Which source feels most promising right now? Why?

2. **What Makes a Good Capstone Project?**
   - Revisit the criteria from class: real business question, data access, engaged sponsor, feasible scope, demonstrable impact
   - Which of these criteria concerns you most for finding a project?

3. **Conversations So Far**
   - Who have you talked to?
   - What responses have you received?
   - If you haven't started conversations yet, who will you reach out to this week?

4. **Your Biggest Challenge**
   - What's the hardest part of the capstone search for you?
   - What would help you overcome it?

5. **Messy Situation Practice**
   > A potential sponsor says: "We have tons of data. Just explore it and find interesting things. I'm sure there's value in there somewhere."

   Write a 2-3 sentence email response that pushes back professionally to get a real business question. What would you say?

**Reflection:** What did you learn about yourself in this first week of searching?

---

*Before submitting: What decision would your capstone drive? What could break if it succeeds?*

---

## Week 2: Counter-Metrics in the Wild (Due: Feb 17)

### Prompt

Find and analyze a real-world example of metric optimization gone wrong.

**Your submission should include:**

1. **The Article/Case**
   - Find a news article, blog post, or case study about a company optimizing a metric with unintended consequences
   - Provide the link or source
   - Summarize what happened in 2-3 sentences

2. **Apply the "What Breaks" Framework**
   - What was the primary metric they were optimizing?
   - What directly worsened as a result?
   - What quality degraded?
   - Which user segments were harmed?
   - What long-term metrics suffered?

3. **What Counter-Metrics Should They Have Tracked?**
   - Identify 2-3 counter-metrics that could have caught the problem
   - Label each as Guardrail or Tradeoff
   - What threshold should have triggered concern?

4. **Personal Connection**
   - Have you seen something similar at work or in your experience?
   - How does this change how you'll think about metrics in your capstone?

**Note:** Can't find an article? Use one of the examples from class (Wells Fargo accounts, YouTube watch time, etc.) and go deeper.

---

*Before submitting: What decision would your capstone drive? What could break if it succeeds?*

---

## Week 3: Analysis Methodology Selection (Due: Feb 24)

### Prompt

Practice selecting and justifying foundational analyses for a real business problem.

**The Mini-Case: FreshMart Grocery Delivery**

> FreshMart is an online grocery delivery service operating in 8 cities. Last quarter, they noticed that first-order customers who receive their delivery within the 1-hour "Express" window have a 45% higher 30-day reorder rate than those who receive standard 3-hour delivery.
>
> The VP of Operations wants to invest $2M in expanding Express capacity.
>
> The CFO is skeptical: "Maybe Express customers are just wealthy professionals who would order anyway — they self-select into Express because they value their time, not because Express delivery makes them loyal."

**Available Data:**
- `orders`: order_id, customer_id, order_date, delivery_window_selected, actual_delivery_time, order_value
- `customers`: customer_id, signup_date, zip_code, first_order_date
- `census_data`: zip_code, median_income, population_density

**Your submission should include:**

1. **Analysis Selection (Choose 2-3)**
   - Which foundational analyses from class would help answer this question?
   - For each, explain:
     - What specific question does this analysis answer?
     - What would you learn from it?
     - What would it NOT tell you?

   *Reminder — The 9 Foundational Analyses:*
   - Acquisition: Funnel, Channel Attribution, Campaign Effectiveness, CAC/LTV
   - Retention: Retention Analysis, Power User Analysis, Failure Analysis
   - Growth: Expansion & Monetization, Ecosystem Analysis

2. **Data Validity Checks (Stop/Go Gates)**
   - What must be true about the data before you can draw conclusions?
   - For each check:
     - What are you validating?
     - How would you validate it?
     - What would make you stop the analysis?

3. **Causation vs. Correlation Challenge**
   - The CFO's concern is about selection bias. How would you address it?
   - What additional data or analysis design would help establish causation?
   - What would you tell stakeholders if you CAN'T establish causation?

4. **Counter-Metric**
   - If the VP is right and you recommend Express expansion, what could break?
   - Identify 1 counter-metric and explain why it matters

**Reflection:** What did this exercise reveal about the difficulty of analysis selection in ambiguous situations?

---

*Before submitting: What decision would this analysis drive? What could break if it succeeds?*

---

## Week 4: Evaluating Project Opportunities (Due: Mar 3)

### Prompt

Update on your capstone search and evaluate potential projects.

**Your submission should include:**

1. **Search Update**
   - What's happened since Week 1?
   - Any new leads? Closed doors?
   - What's your current status?

2. **Project Evaluation (1-2 potential projects)**
   - For each project you're considering, evaluate against the "red flags" checklist:

     | Red Flag | Status |
     |----------|--------|
     | Can they articulate the business question? | |
     | Is data available? When? | |
     | Is there a named sponsor? | |
     | What decisions will this inform? | |
     | Is the sponsor engaged or "too busy"? | |

   - Based on this evaluation, how promising is each project?

3. **Scope Negotiations**
   - Have you had any conversations about scope?
   - What did the sponsor initially want vs. what's feasible?
   - How did you (or will you) negotiate?

4. **Plan B**
   - If your current leads fall through, what's your backup?
   - When is your personal deadline to have a project locked in?

5. **Messy Situation Practice**
   > One of your potential sponsors says: "The data is definitely available, we just need to work out access with IT. Should be ready in a few weeks, maybe a month. Let's not let that slow us down."

   Is this a red flag? What questions would you ask? What would make you walk away?

**Reflection:** What's the most important lesson you've learned about finding a good capstone project?

---

*Before submitting: What decision would your capstone drive? What could break if it succeeds?*

---

## Week 5: Pre-Mortem on a Hypothetical (Due: Mar 10)

### Prompt

Practice the pre-mortem exercise on a project you're NOT doing.

**Your task:**

Choose one of the following:
- One of the scenarios from the class assignment
- A potential capstone project you decided NOT to pursue
- A hypothetical project based on your work experience

**Your submission should include:**

1. **Project Summary**
   - 2-3 sentences describing the project, sponsor, and goal

2. **The Pre-Mortem Narrative**
   - Imagine it's 6 months from now. The project failed.
   - Write 2-3 paragraphs telling the story of what went wrong
   - Be specific: What happened? What was the root cause?
   - Include at least one of:
     - Correlation/causation confusion
     - Stakeholder dynamics gone wrong
     - Scope creep
     - Data quality issues
     - Metric gaming
     - **The data turned out to be garbage** (missing, inconsistent, or unusable)
     - **The sponsor went dark** (stopped responding, left company, lost interest)

3. **What Should Have Been Done Differently?**
   - Looking back at your failure story, what interventions could have prevented it?
   - Be specific

4. **How This Informs Your Capstone**
   - What will you do differently in your actual capstone because of this exercise?
   - What risks will you watch for?

**Reflection:** What did the pre-mortem reveal that you hadn't considered before writing it?

---

*Before submitting: What decision would your capstone drive? What could break if it succeeds?*

---

## Week 6: Capstone Readiness Check (Due: Mar 17)

### Prompt

Projects are assigned on March 16. This is your final write-up before you begin building your actual capstone Brief through the PID process (due Mar 30).

**Your submission should include:**

1. **Search Journey Summary**
   - How did your capstone search go?
   - What worked? What didn't?
   - What would you do differently if you had to start over?

2. **Key Lessons from Write-ups**
   - What's the most important thing you learned from each exercise?
     - Week 1 (Search Kickoff): _____
     - Week 2 (Counter-Metrics): _____
     - Week 3 (Methodology Selection): _____
     - Week 4 (Project Evaluation): _____
     - Week 5 (Pre-Mortem): _____

3. **Your Capstone Brief Checklist**
   - Based on what you've practiced, what will you prioritize when building your Brief?
   - What's your plan for:
     - Defining a precise primary metric?
     - Identifying counter-metrics?
     - Mapping stakeholders (especially blockers)?
     - Writing your pre-mortem?

4. **Questions for Your Sponsor**
   - List 3-5 questions you'll ask your sponsor in your first meeting
   - These should help you fill out your Brief

5. **Confidence Check**
   - On a scale of 1-5, how confident are you in:
     - Understanding what makes a good capstone project? ___
     - Defining metrics with precision? ___
     - Identifying what could break? ___
     - Navigating stakeholder dynamics? ___
   - For any score below 4: What will you do to improve?

**Reflection:** What are you most excited about? What are you most nervous about?

---

*Final check: Are you ready to build a Brief that drives a decision?*

---

# Grading Criteria

Each write-up is graded **Pass/Fail**.

## Pass
- Genuine engagement with the prompt
- Applies course concepts correctly
- Shows evidence of thought and reflection
- Approximately 1 page in length
- Submitted on time (or within grace period)

## Fail
- Superficial or copy-paste responses
- Ignores course concepts
- No evidence of genuine reflection
- Significantly too short (<half page)
- Submitted late without extension

---

# Late Policy

- **Due:** Monday 23:59 CET each week
- **Grace period:** 24 hours with no penalty
- **After grace period:** Must request extension via email before deadline
- **Missing more than 2 write-ups:** Course grade penalty

---

# Why This Structure?

These 6 write-ups prepare you for capstone success:

**Weeks 1-6 (Feb 10 – Mar 17):** You're searching for and evaluating projects. These prompts help you:
- Document your search journey (useful for reflection and troubleshooting)
- Apply course concepts to real-world examples
- Practice skills you'll need when you have a project
- Build confidence before your Brief is "for real"

**After Mar 17:** Your actual capstone Brief is built through the PID process (due Mar 30). The PID template includes all Brief sections. These write-ups have prepared you to fill it out effectively.
