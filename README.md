Skip to content
Navigation Menu
brehima5
Mod5Project_by_thierno

Type / to search
Code
Pull requests
Actions
Projects
Wiki
Security
Insights
Settings
Mod5Project_by_thierno
/
README.md
in
main

Edit

Preview
Indent mode

Spaces
Indent size

2
Line wrap mode

Soft wrap
Editing README.md file contents
Selection deleted
119
120
121
122
123
124
125
126
127
128
129
130
131
132
133
134
135
136
137
138
139
140
141
142
143
144
145
146
147
148
149
150
151
152
153
154
155
156
157
158
159
160
161
162
163
164
165
166
167
168
169
170
171
172
173
174
175
176
177
178
179
180
181
182
183
184
185
186
187
188
189
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

 The analysis shows that most LinkNYC usage is driven by Engaged, High Value, and Quality sessions, with Convenient weeks accounting for only 13% of activity. Engaged users are the most recently active, while High Value and Quality sessions reflect consistent, high-bandwidth use. This pattern indicates that LinkNYC is primarily used as a reliable, habitual service, supporting its role as a functional public utility rather than a fleeting convenience.

<img width="490" height="133" alt="Screenshot 2025-10-15 at 5 45 15 PM" src="https://github.com/user-attachments/assets/77555405-50e1-47da-bb71-4fdc3c2fb6b3" />

---

## 4. Interpretation & Insights
### 4.1 Evidence of Utility Behavior

Strong and consistent engagement among Engaged, High Value, and Quality sessions.\
Low recency for Engaged weeks indicates ongoing, active usage.\
High frequency and substantial TB usage for High Value and Quality sessions show meaningful, habitual interaction.\
Seasonal patterns (Fall and Spring cohorts) demonstrate stable usage over time.

### 4.2 Evidence of Convenience Behavior
Convenient weeks account for only 13% of usage, highlighting limited opportunistic use.
Lower session frequency and smaller data consumption in Convenience weeks indicate occasional, non-essential usage.

Key Insight: Overall, the predominance of high-frequency, high-bandwidth segments confirms that LinkNYC functions more as a reliable public utility than a fleeting convenience.

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

Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
No file chosen
Attach files by dragging & dropping, selecting or pasting them.
Editing Mod5Project_by_thierno/README.md at main · brehima5/Mod5Project_by_thierno
