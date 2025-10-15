# LinkNYC Usage Analysis

*Academic project analyzing a LinkNYC data using Python and Tableau. Applies Business analytics including Funnel, cohort, RFM segmentation to explore real-world business scenarios, uncover patterns, and generate actionable insights to support decisions for stakeholders*



---

## **Business Question:**
LinkNYC was created to offer free public Wi-Fi and digital access across New York City, aiming to reduce the digital divide. After several years of operation, the key question is:

Is LinkNYC a functional utility—part of the city’s essential digital infrastructure—or a fleeting convenience used only occasionally?

This distinction matters for future funding and policy decisions. To explore it, we analyzed weekly usage data (2020–2025) using activation, conversion, retention, cohort, and segmentation analyses to determine whether LinkNYC is used as a daily necessity or an occasional convenience.

---

## 1. Executive Summary

* **Objective:** Assess whether LinkNYC serves as a long-term public utility (consistent, essential use) or a short-term convenience (occasional, opportunistic use).
* **Key Insight (teaser):** Our funnel analysis shows that 23.5% of total sessions reach the “High Value” stage, highlighting meaningful long-term engagement. Segmentation results reinforce this, with Engaged (64) and High Value (75) weeks representing the most consistent, high-impact usage, compared to Quality Sessions (122) and Convenient (39) weeks. Overall, these patterns suggest that LinkNYC functions more as a reliable public utility than a fleeting convenience.
* **Methodology Overview**To evaluate whether LinkNYC functions as a utility or a convenience, we applied several complementary analytical approaches:

1. **Session Analysis**: Measured sessions per user and total activity to gauge overall engagement intensity.
2. **Activation & Conversion Metrics**: Defined activation as weeks above the median data usage, and conversion as weeks in the top 25% of usage, to track progression through the user engagement funnel.
3. Funnel Analysis: Built a behavioral funnel with four stages—**Total Sessions** → **Quality Sessions** → **Engaged Sessions** → **High Value Sessions**—to measure progression toward high-value, consistent use.
4. **Retention Tracking**: Analyzed user sessions across seasons and quarters to assess persistence and habitual use.
5. **Quarterly Performance Analysis**: Compared year-over-year trends (2020–2025) to measure growth, stability, and shifts in usage patterns.
6. **Cohort Analysis**: Grouped users by seasonal cohorts to identify behavioral differences and long-term retention trends.
7. **RFM Segmentation**: Classified usage weeks by Recency, Frequency, and Total Bandwidth (TB) to distinguish between convenience users and utility-level users.
Together, these methods provide a multi-dimensional view of user behavior—linking engagement intensity, temporal consistency, and value generation to assess LinkNYC’s role in the city’s digital ecosystem.

---

## 2. Data Overview

* **Source:** LinkNYC weekly usage dataset
* **Coverage Period:** 2020–2025
* **Granularity:** Weekly records of users, sessions, and TB downloaded
* **Key Metrics:**

  * Sessions per client
  * Number of sessions
  * TB downloaded
  * Session length
  * Data usage per client
  * Derived metrics: activation, conversion, retention,

---

## 3. Analytical Framework

### 3.1 Activation, Conversion & Retention (A/C/R)

* **Activation metric:** A week is *activated* if TB_downloaded > median → measures engagement threshold.
* **Conversion metric:** A week is *converted* if TB_downloaded ≥ top 25% → identifies power users.
* **Retention:** Track sessions per client, Number of Sessions over seasons/quarters → assess persistence of usage.
* **Why:** These metrics collectively measure sustained vs transient interaction.

---

### 3.2 Quarterly Performance Analysis

* **Method:** Aggregate usage(Number of sessions and sessions per client) quarterly from 2020–2025.
* **Objective:** Identify growth trends and volatility over time (YoY comparisons).
* **Justification:** Utility-like behavior should show consistent or growing engagement; convenience behavior would show decline or irregularity.
* **Result Summary:**
* 
<img width="1209" height="170" alt="Screenshot 2025-10-15 at 4 30 11 PM" src="https://github.com/user-attachments/assets/9f400d79-0de2-4d10-9731-937318de4d5a" />


---

### 3.3 Cohort Analysis

* **Definition:** Weekly usage grouped by **seasonal cohorts** (Winter, Spring, Summer, Fall).
* **Goal:** Identify seasonal retention patterns — do certain cohorts maintain activity longer?
* **Key Finding Example:**

<img width="768" height="171" alt="Screenshot 2025-10-15 at 4 34 40 PM" src="https://github.com/user-attachments/assets/6444bb4b-9bcf-4bc3-9723-f431d9364922" />

 * *“Summer and Fall cohorts exhibit a more sustained session averages while we have high fluctuations accross years for Spring and Winter Cohorts*
 * 
* **Justification:** Season-based segmentation helps separate behavioral cycles from infrastructure effects.

---

### 3.4 Fine-Grained Cohort (Monthly–Weekly Evolution)

* **Approach:** Within each 3-month season, track weekly session evolution.
* **Purpose:** Reveal short-term engagement decay or persistence within a cohort.
* **Interpretation:** Gradual decline = convenience; steady use = utility.
  
<img width="458" height="160" alt="Screenshot 2025-10-15 at 4 42 25 PM" src="https://github.com/user-attachments/assets/8683606c-29bd-47d6-9ede-0d3cbf301b6d" />

*Number of Sessions for each monthly cohort from week 1 to week 4*

---
### 3.4 Funnel Analysis: Understanting User Progression and value Creation
To assess how users interact with LinkNYC over time, we developed a four-stage engagement funnel reflecting the journey from casual to high-value usage. The stages were defined as:
****Step 1**: Total Sessions** – all recorded user sessions, representing initial access to the network.
****Step 2:** Session Quality**
First, we defined quality sessions as those with an average session length of more than 5 minutes. We chose this threshold to filter out users who may have interacted with the kiosk out of curiosity rather than for meaningful use.
**Step 3: Engagement**
Next, we considered a session engaged if the user downloaded more than the median amount of terabytes (TB). This helped us identify users who were more actively using the kiosk’s capabilities.
**Step 4: High-Value Users**
Finally, we defined high-value users as those who met the engagement criteria and were in the top 25% (i.e., above the 75th percentile) of our data in terms of usage.

After completing the funnel analysis, we found that 23.5% of all sessions qualified as high-value. This indicates that LinkNYC kiosks serve more than just a momentary need, they provide real utility to a significant portion of users.

*Conversion table*
<img width="1174" height="270" alt="Screenshot 2025-10-15 at 4 54 30 PM" src="https://github.com/user-attachments/assets/c58b8d9f-b1cf-4b53-a5af-3cbec9625531" />


*Overall Conversion Funnel*
<img width="650" height="500" alt="newplot" src="https://github.com/user-attachments/assets/0be4d42d-07d6-40ac-aaf8-3b51c8641721" />

### 3.5 RFM Segmentation (Recency–Frequency–Monetary)
**Criteria:**
- **Usage** = TB Downloaded(TB)
- **duration** = Average session lenght (minutes)
* **Segmentation Logic:**
  | Segment            | Criteria                                | Interpretation     |
  | ------------------ | --------------------------------------- | ------------------ |
  | High Value Week    |  Top 25 data usage, Usage > 25%         | Core utility users |
  | Engaged Week       | Moderate–high use,up median data usage  | Regular users      |
  | Quality sessions   | Light, intermittent, Duration > 5       | Convenience users  |
  | Convenient weeks   | Minimal use, all remaing weeks          | Opportunistic      |
  
* **Results Summary:**

  * Quality sessions: **122** (dominant group)
  * High Value: **75** ( 2nd dominant group, proving usage)
  * Engaged: **64**
  * Convenients weeks: **39**
  * → Suggests **only** 13% of usage weeks align with *convenient behaviour*.
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
