# 📊 Project 13: Multi-Factor Stack Ranking Framework (MSRF) — Fair & Automated Team Performance Ranking

## Executive Overview:

* **Enterprise Context:** Dell Technologies (Global Customer Operations & Support)
* **Role:** Senior Automation & Data Analytics Lead (Enterprise Analytics & Process Intelligence)
* **The Big Problem:** Managers were ranking customer support reps using simple averages. This created unfair scores: reps handling easy, high-volume requests always looked like "top performers," while reps handling complex technical issues looked like "low performers"—even if their quality and customer satisfaction scores were spotless.
* **The Solution:** I led the creation of the **Multi-Factor Stack Ranking Framework (MSRF)**. It’s an automated system that "grades on a curve" across different metrics (CSAT, Speed, Volume, Quality). It neutralises unfair advantages, stops people from gaming the system, and gives leaders a true, apples-to-apples comparison of team performance.
* **Core Value Delivered:**
  * **Fair Rankings:** Replaced raw percentage averages with a balanced scoring model that treats quality and speed with equal importance.
  * **No More System Gaming:** Stopped reps from hiding poor customer service by simply answering a high volume of quick calls.
  * **Automated Leadership Dashboards:** Built automated scorecards rolling up individual performance to Team Leads, Managers, and Directors.
* **Tools & Stack:** Data Analytics & Statistics (Standard Deviation Normalisation), MS Excel Architecture, VBA Automation, SQL Data Staging, Executive PowerPoint Integration.

---

## 1. Why the Old Way Was Broken (The "Layman" Problem):

Imagine comparing two students:
* **Student A** takes 10 very easy quizzes and scores 90%.
* **Student B** takes 3 advanced physics tests and scores 85%.

Under the **old performance ranking system**, Student A was ranked higher simply because their raw numbers looked bigger. This created major issues on the operational floor:
1. **Comparing Apples to Oranges:** High-volume, simple queues naturally had massive swings in numbers, while Quality and CSAT scores moved in tiny increments. The high-volume numbers completely drowned out quality.
2. **Punishing Hard Work:** Reps taking complex, difficult customer cases looked "slow," even though they were doing the hardest work.
3. **Gaming the System:** Reps figured out they could ignore customer quality entirely—if they closed enough quick tickets, the old formula would still rank them as a "top performer."

---

## 2. How the MSRF Framework Fixes It (Simple Concept):
The MSRF system acts as an **intelligent leveller**. It processes performance through four simple steps:

```text
┌──────────────────────────┐     ┌──────────────────────────┐     ┌──────────────────────────┐
│   1. Standardise Data    │     │   2. "Grade on a Curve"  │     │   3. Apply Smart Caps    │
│  Convert speed, quality, │ ──> │ Compare each rep against │ ──> │ Prevent extreme outliers │
│   & CSAT to one scale.   │     │  their actual peer group.│     │   from skewing scores.   │
└──────────────────────────┘     └──────────────────────────┘     └──────────────────────────┘
                                                                               │
                                                                               ▼
                                                                  ┌──────────────────────────┐
                                                                  │  4. Fair Stack Ranking   │
                                                                  │ Roll up scores to Leads, │
                                                                  │  Managers, & Directors.  │
                                                                  └──────────────────────────┘

```

### The 3 Core Rules Built Into the Engine:

1. **Directional Logic:** The system knows that for **CSAT**, *higher is better* (100% is great), but for **Handle Time**, *lower is better* (faster is great). It flips the math automatically.
2. **Peer-Group Normalisation ($Z$-Score):** Instead of looking at raw numbers, it measures how far above or below average a rep is compared to peers doing the exact same type of work.
3. **Outlier Safety Caps:** If a rep goes crazy high on one single metric, the system caps its impact so it can't mask total failure in customer service.

---

## 3. What We Built (System Modules)

* **Module 1: Automated Data Ingestion** — Pulls weekly performance and quality audit data across different business groups into a single clean pipeline.
* **Module 2: The Fair Scoring Engine** — Converts raw metrics into balanced, standardised scores, applying weighting rules based on business priorities.
* **Module 3: Executive Scorecards & Dashboards** — Generates instant, clear performance reports for Team Leads to coach struggling agents and for Executives to see real team health.

---

## 4. Real Business Impact

| What We Measured | 🛑 Old Way (Raw Averages) | 🎯 MSRF Way (Smart Ranking) | 💡 Why It Matters |
| --- | --- | --- | --- |
| **Scoring Fairness** | High call volume crushed quality scores | **100% Equalised Scale across all metrics** | Speed and Quality now carry equal, fair weight. |
| **System Gaming** | Easy to trick the system by ignoring quality | **Outlier Caps block single-metric gaming** | Reps must deliver balanced, quality performance to rank top. |
| **Difficult Case Bias** | Reps on hard cases were punished | **Normalised against peer averages** | Fairly rewards reps handling complex work. |
| **Executive Visibility** | Messy, separate spreadsheets per team | **One automated roll-up deck for Directors** | Leadership sees true top talent and coaching needs instantly. |

---

## 5. Key Skills Displayed

* **Data Analytics & Applied Statistics:** Turning complex mathematical concepts (Standard Deviations, $Z$-Scores) into practical business tools.
* **Performance Framework Design:** Designing fair, unbiased scoring systems for large operational teams.
* **Automation & Process Improvement:** Building automated pipelines in Excel/ VBA/ SQL to replace manual spreadsheet work.
* **Executive Storytelling:** Translating complex data into clear, decision-ready leadership dashboards.

---
