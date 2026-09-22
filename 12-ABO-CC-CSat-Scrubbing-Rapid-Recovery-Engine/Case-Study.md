# Project 12: ABO CC CSat Scrubbing & Rapid Recovery Engine

## Executive Overview:

* **Enterprise Context:** Built for Dell's American Business Ops Customer Care (ABO CC) team to automate Customer Satisfaction (CSat) survey ingestion, enforce 100% root-cause scrubbing, and drive responsible service recovery across customer touchpoints.
* **Role:** Operations Manager & End-to-End Systems Architect, Developer, Deployment & Maintenance Lead
* **Core Value Delivered:** Replaced manual reporting with an automated MS Access ingestion tool that fetches daily CSat Excel feeds from central FTP repositories, cross-references employee databases to isolate ABO CC records, and feeds scrubbed error drivers directly into Process Trainers for targeted 1-on-1 coaching and floor refreshers.
* **Impact & Key Deliverables:**
  * Architecturalized an automated FTP ingestion pipeline that automatically parses raw daily CSat Excel files, validates record ownership against employee databases, and filters low-performing scores (ratings 01–06).
  * Designed a 24-hour manager scrubbing workflow that enforces issue resolution and root-cause logging for both Detractors (01–04) and Neutrals (05–06) to address customer pain points regardless of score outcome.
  * Embedded a closed-loop training feedback loop where Process Trainers extract scrubbed error call drivers to run targeted 1-on-1 coaching for repeat CSat error generators and lead floor-wide refresher sessions.
  * Dispatched real-time alerts across Email, Chat, and Voice Customer Care Managers to drive fast operational turnaround and feed executive Pareto analytics for continuous service line improvement.
* **Core Stack:** MS Access, VBA, DAO, SQL, MS Excel Integration, FTP Automation, Outlook/SMTP Notification Modules.

---

### 1. Baseline Operational Friction:

* **Manual FTP & Excel Processing:** Raw CSat survey data was deposited daily as MS Excel files into central FTP repositories, requiring manual downloading, filtering, and distribution across disparate care teams.
* **Data Attribution Overhead:** Care managers spent significant time manually checking survey records against internal employee rosters to isolate surveys belonging specifically to ABO CC representatives.
* **Unaddressed Customer Pain Points:** Unhappy (01–04) and neutral (05–06) customer responses went un-scrubbed due to delayed visibility, leaving underlying product, process, or agent issues unresolved.
* **Disconnected Training Feedback Loop:** Process Trainers lacked structured line-of-sight into actual customer-reported call drivers, preventing them from running targeted remediation’s for repeat CSat error generators or updating floor training modules.

---

### 2. Solution Architecture & Technical Workflow:

#### 2.1 Automated Ingestion, Validation & Recovery Architecture:
* **FTP Excel Ingestion:** The engine automatically picks up daily raw CSat survey MS Excel files from the central repository FTP folders.
* **Employee Roster Cross-Referencing:** The system bounces incoming records against the internal employee database using VBA/ DAO routines to isolate surveys belonging strictly to ABO CC representatives.
* **Score Threshold Isolation:**
* **Detractors (Ratings 1–4):** Immediately flagged for urgent root-cause scrubbing and operational recovery.
* **Neutrals (Ratings 5–6):** Flagged for process gap identification and neutral-to-positive conversion analysis.
* **Real-Time Alert Dispatch:** Triggers instant automated alert notifications to Email, Chat, and Voice Customer Care Managers based on operational routing rules.
* **Mandatory 24-Hour Scrubbing:** Managers log into the scrubbing module, engage the customer, fix the underlying issue to uphold service responsibility, and log standardised root-cause categories.
* **Process Trainer Feedback Loop:** Process Trainers review the scrubbed output to pull actual call drivers, triggering targeted 1-on-1 coaching for high CSat error generators and conducting floor-wide refresher training.

```text
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                   FTP DATA INGESTION & ROSTER VALIDATION PIPELINE                      │
│  ┌─────────────────────────┐   ┌───────────────────────────┐   ┌────────────────────┐  │
│  │ 1.Central FTP Repository│   │ 2. Daily CSat Excel Feed  │   │ 3.Internal Employee│  │
│  │    Folders              │   │    (Raw Survey Data)      │   │    Roster Database │  │
│  └────────────┬────────────┘   └─────────────┬─────────────┘   └─────────┬──────────┘  │
└───────────────┼──────────────────────────────┼───────────────────────────┼─────────────┘
                │                              │                           │
                └─────────────────────────────┬┴───────────────────────────┘
                                              ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                ABO CC CSAT INGESTION & FILTERING ENGINE (MS ACCESS/ DAO)               │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  • Bounces FTP Excel records against Employee Database to isolate ABO CC team data     │
│  • Evaluates score thresholds: Low Score Detector (< 7 on 1–10 scale)                  │
│  • Auto-routes Detractors (1–4) & Neutrals (5–6) to Care Manager Queues                │
└────────────────────────────────────────────┬───────────────────────────────────────────┘
                                             │ (Automated Alert Dispatch)
                                             ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│             24-HOUR SLA SCRUBBING & CLOSED-LOOP PROCESS TRAINER ENGINE                 │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  • Multi-Channel Alerts dispatched to Email, Chat, and Voice Care Managers             │
│  • Manager Scrubbing Form enforces 24-Hour SLA for Issue Rectification & Root Cause    │
│  • Trainers pull scrubbed error drivers for 1x1 coaching & floor-wide refresher topics │
│  • Executive Dashboards aggregate Root-Cause Pareto Analytics & Retraining Pipelines   │
└────────────────────────────────────────────────────────────────────────────────────────┘

```

#### 2.2 System Modules & Engine Functionality:

Engineered in MS Access using a modular VBA/DAO model designed for high-speed processing and operational ease:
* **FTP / Excel Ingestion Module:** Automated background parser that fetches daily Excel files from FTP paths and loads raw data into processing tables.
* **Validation & Roster Matching Engine:** Cross-references employee IDs against active team rosters to filter out non-ABO CC survey records.
* **Rules & Alert Dispatch Engine:** Generates real-time alerts across Email, Chat, and Voice queues based on manager mapping.
* **Manager Scrubbing Form:** Standardised interface enforcing 24-hour SLA tracking, customer contact logs, and root-cause drop-downs.
* **Trainer & Quality Coaching Module:** Dedicated view for Process Trainers to extract scrubbed error call drivers, assign 1-on-1 coaching sessions, and flag systemic floor refresher topics.
* **Pareto & Root-Cause Analytics Module:** Executive dashboard categorising negative/neutral drivers into policy, process, product, and agent coaching needs.

---

### 3. Key Metrics & Business Impact

| 📊 Metric / KPI | ⏳ Before | 🚀 After / Impact |
| --- | --- | --- |
| **Data Ingestion & Routing** | Manual Downloads / Daily Delays | **100% Automated FTP Excel Ingestion & Roster Match** |
| **Low Score Resolution SLA** | Ad-hoc / Days Delayed | **100% Enforced 24-Hour SLA** |
| **Root-Cause Visibility** | Unstructured / Unknown | **100% Standardised Categorisation (Detractors & Neutrals)** |
| **Training Feedback Loop** | Generic / Unlinked to CSat | **Closed-Loop 1x1 Coaching & Floor Refresher Deployment** |

---

### 4. Measurable Business Results & Operational Impact:

* **Automated Data Processing:** Eliminated manual file downloads and roster checks by automating the ingestion of FTP Excel feeds directly into MS Access.
* **Responsible Customer Recovery:** Enforced a culture of service accountability where managers proactively rectified customer issues within 24 hours, taking ownership of service failures regardless of initial score.
* **Targeted Quality Remediation:** Enabled Process Trainers to utilise scrubbed error drivers directly, shifting coaching from generic recaps to high-impact 1-on-1 interventions for repeat CSat error generators.
* **Pulse of the Customer Captured:** Unlocked actionable intelligence from neutral scores (05–06), enabling leadership and trainers to fix hidden friction points before they escalated into dissatisfaction.

---

### 5. Key Competencies Demonstrated:

* **Database & Data Pipeline Automation:** MS Access, VBA, DAO, SQL, Excel API integration, and automated FTP file parsing.
* **Customer Experience (CX) Governance:** Closed-loop recovery frameworks, 24-hour SLA enforcement, and root-cause categorisation.
* **Closed-Loop Quality & Training Architecture:** Error driver extraction, targeted 1x1 coaching integration, and floor refresher program design.
* **Process Optimisation & Analytics:** Employee roster cross-referencing, Pareto analysis, qualitative feedback structuring, and executive reporting.
