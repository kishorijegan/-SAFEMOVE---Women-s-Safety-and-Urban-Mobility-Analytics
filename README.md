# SafeMove — Women's Safety & Urban Mobility Analytics

**A Power BI analytics dashboard analyzing women's safety incidents across urban transport and public spaces — built to surface risk hotspots, transport-safety links, and emergency-response performance for data-driven policy and planning decisions.**



![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)




![DAX](https://img.shields.io/badge/DAX-5B3E96?style=for-the-badge)




![Power Query](https://img.shields.io/badge/Power%20Query-D6336C?style=for-the-badge)



---

## 📌 Overview

SafeMove turns raw incident-report data into a 4-page interactive Power BI dashboard that helps city planners, safety analysts, and policymakers understand **where**, **when**, and **how** women's safety incidents occur in urban mobility contexts — and how effectively emergency services respond.

| Metric | Value |
|---|---|
| Total Incidents Logged | **100K** |
| Total Formally Reported | **91K (91%)** |
| Overall Safety Index | **62.81** |
| High & Critical Risk Share | **33%** |
| Incidents Involving Public Transport | **44.85%** |
| Avg. Emergency Response Time (nationwide) | **19.54 minutes** |

---

## 🗂️ Dashboard Pages

### 1. Overview
High-level KPIs and trend summary — total incidents, reporting rate, overall safety index, and risk distribution at a glance.

### 2. Hotspots
Geographic and category-level breakdown of where incidents concentrate — city/zone hotspot mapping and risk-density analysis.

### 3. Transport, Environment & Severity
Analysis of how incidents relate to transport mode (public vs. private), environmental conditions (lighting, location type), and severity classification.

### 4. Emergency Response & Outcomes
Response-time analysis, outcome tracking, and service-performance metrics for emergency/help-line interventions.

---

## 🛠️ Tools & Skills Used

- **Microsoft Power BI** — dashboard build, report design, cross-page navigation
- **Power Query** — data cleaning, transformation, shaping
- **DAX** — KPI measures, calculated columns, dynamic metrics
- **Data Modeling** — relationships, star-schema structuring
- **Data Visualization & Dashboard UI/UX** — layout, color system, interactivity

---

## 📊 Methodology

1. **Source Review** — understood the raw incident dataset structure and fields
2. **Data Cleaning** — handled blanks/nulls without deleting records (preserved data integrity), standardized categories
3. **Date Modeling** — built a proper date table and relationships for time-intelligence
4. **DAX Modeling** — authored measures for KPIs, risk scoring, and response-time analytics
5. **Validation** — cross-checked totals, tested slicers/filters, and verified visuals against source data

---

## 🎨 Design System

| Color | Hex | Use |
|---|---|---|
| Deep Navy-Plum | `#241B3A` | Primary dark background |
| Pale Lavender-Pink | `#F6EEF7` | Light background |
| Pink | `#D6336C` | Accent / alerts |
| Deep Purple | `#5B3E96` | Accent / categories |
| Blue | `#3B82F6` | Accent / transport |
| Cyan | `#22B8CF` | Accent / response |
| Amber | `#F59E0B` | Accent / warnings |

**Fonts:** Cambria (headings) · Calibri (body)

---

## 📁 Repository Structure

```
SafeMove/
├── README.md
├── SafeMove_Dashboard.pbix
├── SafeMove_Professional_Presentation.pptx
└── screenshots/
    ├── 01_overview.jpg
    ├── 02_hotspots.jpg
    ├── 03_transport_environment_severity.jpg
    └── 04_emergency_response.jpg
```

---

## 🚀 Key Insights

- **Scale:** 100K incidents logged, with a strong 91% formal reporting rate — indicating reasonably high trust in reporting channels.
- **Risk mix:** A third (33%) of all incidents fall into the High & Critical risk band, warranting targeted intervention.
- **Transport link:** Nearly 45% of incidents involve public transport, pointing to transit corridors as priority zones.
- **Response performance:** Average emergency response time sits at ~19.5 minutes nationwide — a useful benchmark for service-level targets.

> *These observations describe the current dashboard snapshot. They are not forecasts or causal conclusions.*

---

## 👩‍💻 Author

**Kishori J**
CS Engineering Graduate · Tirupattur, Tamil Nadu
Built as a Power BI analytics portfolio project.

---

## 📄 License

This project is shared for portfolio and educational purposes.
