# Designing Analytics Projects

**A practical framework for analytics projects that deliver business value.**

Course materials for ECBS5228A at Central European University's MS in Business Analytics program.

---

## What's This Course About?

Most analytics courses teach you *how* to analyze data. This course teaches you *how to design analytics projects that matter* — the work that happens before you write any code.

You'll learn to ask:
- What decision will this analysis inform?
- What metric are we optimizing, and what breaks if we succeed?
- Who needs to buy in, and who might block us?

The course is built around a single artifact: the **Analytics Project Brief**. This one-page framework forces clarity on problem definition, metrics, stakeholders, methodology, and success criteria before any analysis begins.

---

## What's Included

```
├── slides/                    # 6 teaching blocks (100 min each)
│   ├── block_01_*            # The Analytics Project Brief framework
│   ├── block_02_*            # Acquisition Analyses
│   ├── block_03_*            # Retention & Growth Analyses
│   ├── block_04_*            # Application & Practice
│   ├── block_05_*            # Stakeholders & Influence
│   └── block_06_*            # Capstone Preparation
│
├── templates/                 # The Brief framework
│   ├── analytics_project_brief.md    # Blank template
│   └── examples/              # 9 worked examples
│
├── scenarios/                 # 12 company case studies for practice
├── figures/                   # Slide images and visuals
├── weekly_writeups/           # Student assignment prompts
├── syllabus.md               # Full course syllabus
└── scripts/                   # Utilities (slide overflow checker)
```

---

## The Analytics Project Brief

The centerpiece of this course is a 10-section framework:

| Section | Key Question |
|---------|--------------|
| 1. Problem & Decision | What decision will this analysis inform? |
| 2. Metrics | What's the primary metric? What are the counter-metrics? |
| 3. Stakeholders | Who has power/interest? Who might block? |
| 4. Methodology | What analyses will we run? |
| 5. Scope & Deliverables | What's in and out of scope? |
| 6. Success Criteria | What does success look like? |
| 7. Timeline | What are the key milestones? |
| 8. Risks & Assumptions | What could go wrong? |
| 9. Ethics & Privacy | Any PII or bias concerns? |
| 10. Pre-Mortem | It's 3 months from now and this failed. What happened? |

---

## The 9 Foundational Analyses

The course covers analyses across the customer journey:

**Acquisition**
- Funnel Analysis
- Channel Attribution
- Campaign Effectiveness
- CAC/LTV Analysis

**Retention**
- Retention Analysis
- Power User Analysis
- Failure Analysis

**Growth**
- Expansion & Monetization
- Ecosystem Analysis

Each analysis has a worked Brief example in `templates/examples/`.

---

## Using These Materials

### For Instructors

The slides are built with [Marp](https://marp.app/) (Markdown Presentation Ecosystem).

**To view with presenter notes:**
1. Open any `.html` file in a browser
2. Press `p` to enter presenter mode
3. Comprehensive instructor notes appear below each slide

**To modify and rebuild slides:**
```bash
# Install Marp CLI
npm install -g @marp-team/marp-cli

# Rebuild a single deck
marp slides/block_01_analytics_project_brief.md --html -o slides/block_01_analytics_project_brief.html

# Check for content overflow
pip install -r requirements.txt
python scripts/check_overflow.py
```

**Course structure:**
- 2 days × 3 blocks × 100 minutes = 600 minutes total
- Day 1: The Framework & Analyses (Blocks 1-3)
- Day 2: Application & Influence (Blocks 4-6)

### For Self-Study

1. **Start with the syllabus** (`syllabus.md`) to understand the course structure
2. **Read the Brief template** (`templates/analytics_project_brief.md`)
3. **Work through the examples** in `templates/examples/` — one for each analysis type
4. **Practice with scenarios** in `scenarios/` — complete Briefs for these cases
5. **Review the slides** for deeper explanation of each concept

**Key concepts to master:**
- Counter-metrics and the "What Breaks" framework
- Stakeholder mapping (Power-Interest Grid)
- Pre-mortem thinking
- The difference between correlation and causation in analytics recommendations

---

## Suggested Reading

| Reading | Time | Purpose |
|---------|------|---------|
| [Designing Experimentation Guardrails](https://medium.com/airbnb-engineering/designing-experimentation-guardrails-ed6a976ec669) — Airbnb Engineering | ~15 min | Counter-metrics framework |
| [Data Analyst Guide to Stakeholder Management](https://towardsdatascience.com/the-data-analysts-guide-to-stakeholder-management-6d71f6ae5a92) — Towards Data Science | ~12 min | Stakeholder mapping |

---

## License

This work is licensed under [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) (Creative Commons Attribution 4.0 International).

You are free to:
- **Share** — copy and redistribute the material
- **Adapt** — remix, transform, and build upon the material for any purpose

Under the following terms:
- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made.

---

## Author

**Eduardo Arino de la Rubia** (rubiae@ceu.edu)

Data science leader based in southern Spain. Former Senior Director of Data Science at Meta, Chief Data Scientist at Domino Data Lab (pre-seed through Series B), and Principal Data Scientist at Ingram.

---

## Contributing

Found an error? Have a suggestion? Issues and pull requests are welcome.

For questions about using these materials in your own teaching, feel free to reach out.
