# 🛡️ SafeMove — Women's Safety & Urban Mobility Analytics

> **An interactive Power BI dashboard analyzing incident patterns, geographic hotspots, transport-related risk factors, and emergency response efficiency across Indian cities.**



![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)




![DAX](https://img.shields.io/badge/DAX-Measures-512BD4?style=for-the-badge)




![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Cleaning-5B2D90?style=for-the-badge)




![Data Analytics](https://img.shields.io/badge/Data%20Analytics-Project-0EA5E9?style=for-the-badge)



---

## 🖼️ Dashboard Preview

### Overview


![Overview](assets/overview.png)



### Hotspots


![Hotspots](assets/hotspots.png)



### Transport, Environment & Severity


![Transport](assets/transport.png)



### Emergency Response & Outcomes


![Response](assets/response.png)



---

## 📌 Project Overview

**SafeMove** is an end-to-end Power BI analytics project built to transform a women's safety and urban mobility dataset into an interactive business intelligence dashboard.

The dashboard is designed from the perspective of a city safety planning team that wants to understand:
- How many incidents are occurring, and how many go reported
- Which areas and time windows carry the highest risk
- How transport mode relates to incident type and severity
- Whether environmental factors (lighting, crowd density, visibility) correlate with safety
- How fast emergency services respond, and where cases stand on resolution

The final dashboard contains **4 analytical pages**, connected through interactive navigation.

---

## 🎯 Project Objectives

1. Monitor overall incident volume and safety index across cities.
2. Identify geographic and time-based incident hotspots.
3. Analyze the relationship between transport mode and incident type/severity.
4. Measure how lighting, crowd density, and visibility correlate with safety.
5. Evaluate emergency response time and case resolution outcomes.
6. Present findings through a clean, professional, branded Power BI interface.

---

## 🧰 Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| **Microsoft Power BI** | Dashboard development and interactive reporting |
| **Power Query** | Data cleaning and transformation |
| **DAX** | Measures, KPIs and analytical calculations |
| **CSV Dataset** | Input data source (100,000 incident records) |
| **Power BI Visuals** | Charts, cards, tables, slicers, gauges and navigation |
| **GitHub** | Project documentation and version control |

---

## 🖥️ Dashboard Structure

### 1. 📊 Overview
A high-level summary of total incidents, safety index, risk distribution, and monthly trends — the entry point into the dashboard.

### 2. 🗺️ Hotspots
Focuses on geographic and time-based incident patterns — highest-risk areas, hour-by-day heatmap, and weekday vs weekend comparison.

### 3. 🚌 Transport, Environment & Severity
Compares incident type by transport mode, tests the lighting-vs-safety relationship, and tracks environmental scores (crowd density, visibility, transport availability).

### 4. 🚑 Emergency Response & Outcomes
Analyzes response time by city, the distance-to-response relationship, case resolution status, and an area-level safety scorecard.

---

## 📊 1. Overview

### KPI Cards
| Total Incidents | Total Reported Incidents | Overall Safety Index | High & Critical Risk % | Avg Emergency Response Time |
|---|---|---|---|---|
| 100K | 91K | 62.81 | 33.00% | 19.54 min |

### Visuals
- **Monthly Incidents vs Safety Index** — combo chart tracking incident volume against safety trend over the year
- **Total Incidents by Risk Level** — donut chart breaking incidents into Critical/High/Moderate/Low
- **Incidents by City** — bubble map showing geographic distribution
- **Total Incidents by Month** — line chart of incident trend

### Business Questions Answered
- How many incidents were recorded, and how many were reported?
- What is the overall safety index across all areas?
- What share of incidents fall into high/critical risk?
- How does incident volume trend month to month?

---

## 🗺️ 2. Hotspots

### KPI Cards
| High & Critical Risk % | Night-Time Incident % | Overall Safety Index |
|---|---|---|
| 33.00% | 39.42% | 62.81 |

### Visuals
- **Total Incidents by Area** — bar chart, Top 10 highest-incident areas
- **10 Lowest Safety Areas** — funnel chart ranking areas by safety index
- **Incidents by Hours & Day** — matrix heatmap (Hour × Weekday)
- **Incidents: Weekday vs Weekend** — clustered column comparison
- **Slicers**: City, Area, Risk_Level, Weekend_Flag

### Business Questions Answered
- Which areas carry the highest incident volume?
- Which areas have the lowest safety index?
- What hours and days see the sharpest spikes in incidents?
- How does incident volume differ between weekdays and weekends?

---

## 🚌 3. Transport, Environment & Severity

### KPI Cards
| Public Transport Incident % | Crowd Density Score | Visibility Score | Transport Availability Score |
|---|---|---|---|
| 44.85% | 56.95 | 65.94 | 69.84 |

### Visuals
- **Incidents by Transport Mode & Type** — clustered bar chart
- **Lighting Score vs Safety Index by Area** — scatter chart, colored by Risk_Level
- **Severity Mix by Transport Mode** — 100% stacked bar chart
- **Environmental score gauges** — crowd density, visibility, transport availability

### Business Questions Answered
- Which transport modes see the highest incident volume, and of what type?
- Does poor lighting correlate with lower safety scores?
- How does incident severity distribution vary by transport mode?
- How do crowd density, visibility, and transport availability compare across the dataset?

---

## 🚑 4. Emergency Response & Outcomes

### KPI Cards
| Average Emergency Response Time |
|---|
| 19.54 min |

### Visuals
- **Average Response Time by City** — bar chart
- **Police Distance vs Response Time** — scatter chart by city
- **Case Resolution Status** — donut chart
- **Area Safety Scorecard** — table with red-to-green conditional formatting on Safety Index

### Business Questions Answered
- Does response time vary meaningfully by city, or stay consistent nationwide?
- Does proximity to a police station predict faster response?
- What share of cases are resolved vs. still under investigation?
- Which specific areas need the most safety attention?

---

## 🧹 Data Preparation

- Reviewed the source schema (27 columns, 100,000 records)
- Fixed data types (Date, Decimal scores, Whole number Hour)
- Replaced blank `Emergency_Service` values with "None"
- Removed duplicate records on `Incident_ID`
- Built a dedicated `DateTable` using `CALENDAR()` and marked it as the official date table
- Related `DateTable[Date]` to the fact table on a one-to-many relationship

---

## 🧮 DAX & Analytical Calculations

The dashboard uses DAX measures for reusable calculations, including:

- Total Incidents
- Total Reported Incidents
- Overall Safety Index
- Average Emergency Response Time
- High and Critical Risk %
- Night-Time Incident %
- Public Transport Incident %

### Example: Reported Incidents
```dax
Total Reported Incidents =
COUNTROWS(
    FILTER(
        db,
        db[Reported] = "Yes"
    )
)
