# 📊 Project 13: Multi-Factor Stack Ranking Framework (MSRF) — Homogenised, Rationalised & Commensurated Team Performance Ranking

## Executive Overview:
* **Enterprise Context:** Dell Technologies (Global Customer Operations & Support)
* **Role:** Senior Automation & Data Analytics Lead (Enterprise Analytics & Process Intelligence)
* **The Strategic Objective:** Build a **Homogenised, Rationalised, and Commensurated** performance stack ranking framework across diverse support teams. The system needed to be analytically sound and mathematically bulletproof, yet simple enough to explain to frontline agents who had zero background in statistics.
* **Bottom-Up Grassroots Adoption Strategy:** Rather than imposing a top-down mandate, we conducted multiple interactive warmup and education sessions directly with floor reps. We demonstrated how the math protected them from unfair evaluations and queue biases, securing grassroots trust and buy-in *before* looping in and briefing executive leadership.
* **The Big Problem:** Legacy ranking relied on raw percentage averages. Reps handling easy, high-volume requests artificially looked like "top performers," while reps tackling complex technical issues appeared as "low performers"—even with flawless quality and CSAT scores.
* **The Solution:** Engineered the **Multi-Factor Stack Ranking Framework (MSRF)**—an automated engine that "grades on a curve" across heterogeneous metrics (CSAT, Speed, Volume, Quality). It neutralises queue disparities, stops system gaming, and provides an apples-to-apples performance comparison across the enterprise.


* **Core Value Delivered:**
* **Homogenised & Commensurated Metrics:** Standardised disparate metrics (seconds, percentages, survey scores) onto a single, fair comparative scale.
* **Grassroots Buy-In & Cultural Shift:** Achieved 100% floor acceptance by demystifying the math for agents prior to executive rollout.
* **Automated Leadership Roll-Ups:** Generated automated scorecards streaming performance transparently from Reps to Team Leads, Managers, and Directors.
* **Tools & Stack:** Applied Statistics ($Z$-Score Normalisation, Standard Deviation Capping), MS Excel Analytics Architecture, VBA Automation, SQL Data Staging, Executive PowerPoint Integration.

---

## 1. Why the Old Way Was Broken:

To explain the flaw to frontline agents during floor enablement sessions, we used a simple academic analogy:
* **Student A** takes 10 elementary quizzes and scores 90%.
* **Student B** takes 3 advanced physics exams and scores 85%.

Under the **legacy ranking system**, Student A was ranked higher simply because raw volume numbers were larger. This created severe friction on the operational floor:
1. **Apples-to-Oranges Evaluation:** High-volume queues naturally experienced wide swings, while CSAT and Quality scores moved in tight percentage increments. High-volume swings completely drowned out quality.
2. **Penalising Complex Work:** Reps taking tough, multi-layered customer issues looked "slow," even though they were handling the most difficult cases.
3. **Gaming the System:** Reps realised they could ignore customer service quality entirely—if they processed enough fast tickets, raw average formulas still placed them in the top quartile.

---

## 2. The Solution Architecture: Homogenised, Rationalised & Commensurated

MSRF acts as an **intelligent, fair leveller** across four automated stages:

```text
┌──────────────────────────────────┐     ┌──────────────────────────────────┐     ┌──────────────────────────────────┐
│    1. Homogenise Metric Data     │     │     2. Rationalise Performance   │     │    3. Commensurate & Apply Caps  │
│  Convert speed, quality, & CSAT  │ ──> │   "Grade on a curve" against     │ ──> │ Bounded statistical capping     │
│   onto one unified scale.        │     │    actual peer cohort averages.  │     │  blocks single-metric gaming.    │
└──────────────────────────────────┘     └──────────────────────────────────┘     └──────────────────────────────────┘
                                                                                                   │
                                                                                                   ▼
                                                                                      ┌──────────────────────────────────┐
                                                                                      │  4. Grassroots & Exec Dashboard  │
                                                                                      │ Transparent roll-up from Reps to │
                                                                                      │  Team Leads & Operations Directors│
                                                                                      └──────────────────────────────────┘

```

### The 3 Core Rules Built Into the Engine:

1. **Directional Logic:** Flipped orientation automatically—recognising that for **CSAT/Quality**, *higher is better*, whereas for **Handle Time**, *lower is better*.
2. **Peer-Group Normalisation ($Z$-Score):** Rather than evaluating raw scores, it measured standard deviation distances above or below the cohort mean for agents performing identical work types.
3. **Outlier Safety Capping:** Bounded extreme values (between $-3.0\sigma$ and $+3.0\sigma$), ensuring overachievement on a single metric could not mask failure in customer satisfaction.

---

## 3. Change Management & Grassroots Floor Enablement

A core driver of MSRF's success was how the analytics team approached change management:

```text
┌─────────────────────────────────────────┐
│ PHASE 1: Analytics & Model Validation   │  --> Built & back-tested MSRF on historical data.
└────────────────────┬────────────────────┘
                     ▼
┌─────────────────────────────────────────┐
│ PHASE 2: Floor Warmup & Agent Workshops │  --> Conducted interactive sessions explaining 
└────────────────────┬────────────────────┘      "grading on a curve" & fairness mechanics.
                     ▼
┌─────────────────────────────────────────┐
│ PHASE 3: Rep Buy-In & Trust Sign-Off   │  --> Secured floor confidence that hard work & 
└────────────────────┬────────────────────┘      complex cases were protected.
                     ▼
┌─────────────────────────────────────────┐
│ PHASE 4: Executive Briefing & Rollout   │  --> Briefed leadership & deployed automated 
└─────────────────────────────────────────┘      site-wide reporting dashboards.

```

* **Translating Math into Everyday Logic:** Conducted interactive enablement sessions breaking down statistical curves into plain language ("grading on a curve" and "levelling the playing field").
* **Demonstrating Protection:** Proved to agents on complex queues that the new math actively protected their rankings from being swamped by high-volume transactional teams.
* **Grassroots Approval Before Executive Briefings:** By securing 100% rep endorsement first, leadership was presented with a framework that was both statistically robust and culturally embraced by the floor.

---

## 4. Operational Modules & System Architecture
* **Module 1: Data Ingestion & Schema Alignment Engine** — Automatically pulled weekly performance and QA audit feeds into a unified processing pipeline.
* **Module 2: MSRF Calculation Engine** — Applied directional target indexing, standard deviation transformations, and weighted composite scoring.
* **Module 3: Multi-Level Executive Scorecard Suite** — Streamed transparent, decision-ready reports from individual rep scorecards up to site-level executive dashboards.

---

## 5. Measurable Business Results & Operational Impact

| Performance Metric | 🛑 Legacy Model (Raw Averages) | 🎯 MSRF Engine (Commensurated Scale) | 💡 Operational Impact |
| --- | --- | --- | --- |
| **Evaluation Fairness**<br> | Volume swings swamped quality & CSAT scores | **100% Homogenised Scale ($\sigma = 1$) across all metrics**<br> | Quality, CSAT, and Speed carry balanced, rationalised weight. |
| **System Gaming**<br> | Easy to rank top by ignoring quality | **Statistical Outlier Caps block single-metric gaming**<br> | Reps must deliver balanced excellence to reach top quartiles. |
| **Complex Queue Bias**<br> | Reps on hard technical cases were penalised | **Normalised against actual peer cohort baselines**<br> | Fairly rewards reps handling complex, high-effort cases. |
| **Floor Adoption & Culture**<br> | Distrust in management stack rankings | **100% Rep Acceptance via Bottom-Up Enablement**<br> | Grassroots trust established prior to executive sign-off. |

---

## 6. Key Competencies Demonstrated:

* **Advanced Data Analytics & Applied Statistics:** Translating $Z$-scores, population variance, and outlier capping into practical enterprise solutions.
* **Homogenised Performance System Architecture:** Designing rationalised, commensurated scoring frameworks across multi-faceted operational metrics.
* **Strategic Change Management & Leadership:** Driving bottom-up floor adoption, demystifying complex statistics for non-technical teams, and securing executive endorsement.


* **Automation & Enterprise Reporting:** Building automated analytics pipelines in Excel, VBA, and SQL to support multi-level leadership roll-ups.
