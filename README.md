# Mod5Project

Excellent — you’ve got a strong analytical foundation here. Your question *“Is LinkNYC a functional utility or a fleeting convenience?”* is strategic and data-driven, so the **README** should read like a short analytical report aimed at stakeholders (e.g. city officials, program managers, urban planners).

Below is a proposed **professional README structure** that balances storytelling, methodology, and data justification — ideal for a stakeholder audience while remaining technically transparent.

---

# 📘 README: LinkNYC Usage Analysis

**Business Question:**
*Is LinkNYC a functional utility or a fleeting convenience?*

---

## 1. Executive Summary

* **Objective:** Assess whether LinkNYC serves as a long-term public utility (consistent, essential use) or a short-term convenience (occasional, opportunistic use).
* **Key Insight (teaser):** Summarize your main finding here — e.g. *“Patterns of sustained high-intensity use across quarters and strong retention in high-usage cohorts suggest LinkNYC functions increasingly as a utility rather than a fleeting convenience.”*
* **Methodology Overview:** Briefly list major analytical approaches (e.g. session analysis, cohort trends, RFM segmentation, quarterly evolution).

---

## 2. Data Overview

* **Source:** LinkNYC weekly usage dataset
* **Coverage Period:** 2020–2025
* **Granularity:** Weekly records of users, sessions, and TB downloaded
* **Key Metrics:**

  * Sessions per user
  * TB downloaded
  * Session length
  * Derived metrics: activation, conversion, retention

---

## 3. Analytical Framework

### 3.1 Activation, Conversion & Retention (A/C/R)

* **Activation metric:** A week is *activated* if TB_downloaded > median → measures engagement threshold.
* **Conversion metric:** A week is *converted* if TB_downloaded ≥ top 25% → identifies power users.
* **Retention:** Track sessions per client over seasons/quarters → assess persistence of usage.
* **Why:** These metrics collectively measure sustained vs transient interaction.

---

### 3.2 Quarterly Performance Analysis

* **Method:** Aggregate usage (sessions & TB downloaded) quarterly from 2020–2025.
* **Objective:** Identify growth trends and volatility over time (YoY comparisons).
* **Justification:** Utility-like behavior should show consistent or growing engagement; convenience behavior would show decline or irregularity.
* **Result Summary:**

  * Show table or highlight trends (e.g. “YoY changes fluctuate sharply after 2021, suggesting usage patterns stabilized but plateaued.”).

---

### 3.3 Cohort Analysis

* **Definition:** Users grouped by **seasonal cohorts** (Winter, Spring, Summer, Fall).
* **Goal:** Identify seasonal retention patterns — do certain cohorts maintain activity longer?
* **Key Finding Example:**

  * *“Fall and Spring cohorts exhibit higher sustained session averages, implying consistent commuter or student-based use.”*
* **Justification:** Season-based segmentation helps separate behavioral cycles from infrastructure effects.

---

### 3.4 Fine-Grained Cohort (Monthly–Weekly Evolution)

* **Approach:** Within each 3-month season, track weekly session evolution.
* **Purpose:** Reveal short-term engagement decay or persistence within a cohort.
* **Interpretation:** Gradual decline = convenience; steady use = utility.

---

### 3.5 RFM Segmentation (Recency–Frequency–Monetary)

* **Segmentation Logic:**

  | Segment            | Criteria                                | Interpretation     |
  | ------------------ | --------------------------------------- | ------------------ |
  | Utility Usage Week | High sessions, high data, long duration | Core utility users |
  | Active Week        | Moderate–high use                       | Regular users      |
  | Occasional Users   | Light, intermittent                     | Convenience users  |
  | Convenience Users  | Minimal use                             | Opportunistic      |
  | Dormant Weeks      | No usage                                | Inactive           |
* **Results Summary:**

  * Utility usage weeks: **208** (dominant group)
  * Active weeks: **61**
  * Occasional/convenience: **31 total**
  * → Suggests 70–80% of usage weeks align with *utility behavior*.
* **RFM Results Interpretation:**

  * Utility users have **Recency = 0 weeks** (currently active), **Frequency = 208**, **TB_used = 26.6K**, reinforcing essential usage patterns.

---

## 4. Interpretation & Insights

### 4.1 Evidence of Utility Behavior

* Sustained quarterly engagement after 2023 rebound.
* Dominance of “utility usage” segments in RFM analysis.
* Low recency (continued activity) among high-usage cohorts.
* Seasonal stability, particularly in Fall and Spring cohorts.

### 4.2 Evidence of Convenience Behavior

* Sharp declines in specific quarters (e.g. Q1 2021, Q3 2022).
* Seasonal variability may indicate opportunistic use (e.g., weather, tourism).
* Shorter session durations among low-tier segments.

### 4.3 Synthesis:

> *“While LinkNYC usage fluctuated early in the dataset, the predominance of persistent, high-volume users and recurring seasonal retention patterns suggest that LinkNYC functions more as a **public utility** than a fleeting convenience.”*

---

## 5. Assumptions & Limitations

* **Data completeness:** Assuming weekly data accurately reflects total usage (no missing nodes).
* **User identity:** Sessions per client treated as unique users (may overcount shared devices).
* **Temporal assumptions:** Cohorts defined by calendar seasons, not event-based factors.
* **Measurement bias:** Median-based activation assumes symmetric data distribution.

---

## 6. Future Work & Recommendations

* Expand segmentation using demographics or location granularity.
* Model predictive retention based on early usage patterns.
* Integrate weather and event data to separate environmental effects.
* Present visualization dashboards (e.g., quarterly trend maps for stakeholders).

---

## 7. Appendix

* **Formulas used** (Activation, Conversion, Retention, RFM)
* **Code snippets** (segmentation function, cohort logic)
* **Summary tables** of key metrics

---

Would you like me to draft this README in **Markdown format with embedded visuals placeholders** (e.g., “Figure 1: Quarterly Trends”) — suitable for GitHub or stakeholder documentation?
That would make it directly publishable and presentation-ready.
