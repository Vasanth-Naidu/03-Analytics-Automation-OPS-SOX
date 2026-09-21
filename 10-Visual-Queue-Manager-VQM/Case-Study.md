# 📊 Project 10: Visual Queue Manager (VQM) — Near Real-Time Floor Telemetry & Capacity Orchestration Engine

## Executive Overview:

* **Enterprise Context:** Dell Technologies (Global Customer Care & Operations)
* **Role:** Operations Manager & End-to-End Systems Architect, Developer, Deployment & Maintenance Lead
* **Core Value Delivered:** Concepted, engineered, deployed, and maintained **Visual Queue Manager (VQM)**, a desktop-based floor telemetry and capacity orchestration platform built in MS Access and T-SQL. Operating as both the functional Operations Manager and sole system developer/maintenance lead, designed VQM to unify live telephony streams, case dispatch queues, and agent state metrics into a colour-coded visual command center, giving floor leads real-time control over intra-day operations.
* **Impact & Key Deliverables:**
  * **Intra-Day Latency Elimination:** Replaced static 2-hour delayed interval reports with a live, 30-second refreshing visual telemetry feed of queue backlogs and agent activity.
  * **Proactive SLA Protection:** Prevented queue spikes and SLA breaches by visually highlighting bottlenecked queues before holding thresholds were exceeded.
  * **Intelligent Capacity Dispatch:** Enabled team leads to re-route volume and dynamically reassign agent skills with one click during unexpected volume spikes.
* **Core Stack:** MS Access (Custom GUI Engine, Event Handlers & Local Data Cache), T-SQL (Automated Staging Views), Avaya Call Management System (CMS) Live Data Stream, Custom VBA Dispatch Algorithms.

---

## 1. Operational Challenge & Floor Visibility Blindspots:

### Baseline Operational Friction:
Managing multi-queue call centres across shifts suffered from severe operational lag and fragmented floor control:

* **Delayed Operational Telemetry:** Floor managers relied on 2-hour delayed static interval reports to track incoming volume, average speed of answer (ASA), and abandon rates.
* **Blindspot Capacity Allocation:** Team leads could not see which agents were stuck in extended wrap-up, idle, or handling complex cases without physically walking the floor.
* **Reactive SLA Triage:** By the time a volume spike appeared on interval reports, SLA thresholds were already breached and abandon rates had spiked.
* **Siloed Operational Data:** Telephony queue states, CRM case backlogs, and agent attendance rosters operated in silos, forcing leads to manually combine data during live shifts.

---

## 2. Solution Architecture & Dual-Hat Execution:

As both the Operations Manager facing floor friction and the hands-on system developer, designed and built a direct telemetry pipeline from core telephony and case management databases into an interactive MS Access visual engine:

```text
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                               LIVE OPERATIONAL DATA STREAMS                            │
│  ┌─────────────────────────┐   ┌───────────────────────────┐   ┌────────────────────┐  │
│  │ 1. Avaya CMS Telemetry  │   │ 2. Live CRM Case Queue    │   │ 3. Shift Roster &  │  │
│  │ (Live Calls & States)   │   │ (Backlog & Priority)      │   │ Agent Auxiliary    │  │
│  └────────────┬────────────┘   └─────────────┬─────────────┘   └─────────┬──────────┘  │
└───────────────┼──────────────────────────────┼───────────────────────────┼─────────────┘
                │                              │                           │
                └──────────────────────────┬───┴───────────────────────────┘
                                           ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                  VQM TELEMETRY ENGINE & DISPATCH ENGINE (MS ACCESS / T-SQL)            │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  • Automated 30-Second Micro-Batch Refresh & Local Data Caching                        │
│  • Dynamic Threshold Evaluator & Colour-coded Heatmap Renderer                         │
│  • Rule-Based Skill Re-Allocation & Capacity Dispatch Controller                       │
└───────────────────────────────────────────┬────────────────────────────────────────────┘
                                            ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                           VQM VISUAL FLOOR COMMAND CENTER UI                           │
├────────────────────────────────────────────────────────────────────────────────────────┤
│  • Live Queue Heatmap Grid  • Real-Time Agent State Matrix   • 1-Click Skill Dispatch  │
└───────────────────────────────────────────┴────────────────────────────────────────────┘

```

### Technical & Maintenance Component Breakdown:

1. **Automated Telemetry Ingestion Layer:** Engineered 30-second delta updates from Avaya CMS and CRM databases into indexed T-SQL staging tables, isolating heavy queries from production systems.
2. **Visual Heatmap & Threshold Engine:** Coded local evaluation routines for live metrics against predefined operational tolerances (Green = Normal, Amber = Warning, Red = SLA Breach Risk), instantly updating UI element colours.
3. **One-Click Capacity Orchestration:** Developed custom VBA action handlers enabling supervisors to initiate rapid skill updates and reassign agents across queues directly from the dashboard view.
4. **End-to-End Maintenance & Evolution:** Maintained database indexing, optimised query routines, and adapted business logic based on evolving shift structures and seasonal volume surges.

---

## 3. The 3 Core Visual Modules of VQM:

### Module 1: Live Queue Telemetry Heatmap
* **Features:** Colour-coded grid showing real-time call volume, longest wait time, current ASA, and abandon percentages across all active lines.
* **Impact:** Immediate visual signal when any individual queue crosses normal operating thresholds.

### Module 2: Agent State & Auxiliary Time Matrix
* **Features:** Real-time view of individual agent status (In-Call, Wrap-Up, Idle, Aux/Break) with automated timer alerts for excessive wrap-up or hold durations.
* **Impact:** Eliminates hidden floor leakage and provides instant visibility into available capacity.

### Module 3: Capacity Dispatch & Skill Re-Balancing Hub
* **Features:** Interactive panel providing recommendations for cross-queue agent re-allocation based on live inflow velocities.
* **Impact:** Reduces reaction time during unexpected volume surges from hours to minutes.

---

## 4. Measurable Business Results & Operational Impact:

| Performance Metric | 🛑 Baseline State (Pre-VQM) | 🎯 Post-Deployment State (VQM Engine) | 💡 Strategic Value |
| --- | --- | --- | --- |
| **Operational Data Recency** | 2-Hour Static Interval Reports | **30-Second Live Refresh** | Transformed floor control from reactive to real-time |
| **SLA Breach Prevention** | Post-incident triage | **Proactive Threshold Alerts (Amber/Red)** | Drastic reduction in queue abandon rates |
| **Intra-Day Re-Allocation Latency** | 45–60 minutes manual analysis | **<2 Minutes 1-Click Dispatch** | Rapid capacity response during sudden volume spikes |
| **Floor Shrinkage & Leakage** | Untracked Aux/wrap-up delays | **Live Timer Highlights & Alerts** | Maximised available FTE production hours |

---

## 5. Key Competencies Demonstrated:

* **Dual-Hat Leadership:** Combining direct operational ownership with full-stack desktop software development, deployment, and lifecycle maintenance.
* **Floor Telemetry & Operational Design:** Translating high-velocity call centre metrics into actionable, intuitive visual interfaces.
* **Rapid Application Architecture:** Developing scalable event-driven GUIs, data caches, and automation routines in MS Access, VBA, and T-SQL.

---
