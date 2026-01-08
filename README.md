
# **Analyzing Fatal Injury Patterns in Construction Incidents**

*An Explanatory Data Science Approach*

[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/) [![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)](https://powerbi.microsoft.com/) [![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## **🧭 Overview**

This project investigates workplace injuries in the **construction industry**, focusing on **factors associated with fatal outcomes**. Unlike predictive modeling, the goal here is to **analyze patterns, explore relationships, and explain which injury types or conditions are most likely to result in death**.

Key objectives:

* Identify high-risk injury types and body parts
* Understand environmental, human, and task-related factors influencing fatalities
* Use statistical and explanatory modeling to quantify risk
* Create interactive visualizations for actionable insights

---

## **📊 Dataset**

**Source:** OSHA Accident Reports
**Size:** ~4,800 incidents
**Columns:** 25+ fields including injury type, body part affected, human/environmental factors, date, task assignment, etc.

**Target Variable:** `Degree of Injury`

* 1 = Fatal
* 0 = Non-Fatal

**Key Features Used:**

* Nature of Injury
* Part of Body
* Event Type
* Human Factor
* Environmental Factor
* Task Assigned
* Is_Holiday
* Season

---

## **🔍 Exploratory Analysis Highlights**

* **61%** of incidents resulted in fatalities
* **High fatality risk**: Head, internal, and whole-body injuries
* **Low fatality risk**: Fingers, hands, limbs
* Slightly higher odds of fatal injuries during holidays, but **not statistically significant**
* Seasonal and task-based patterns observed

---

## **🧪 Statistical Testing**

**Test:** Fisher’s Exact Test for holidays vs. non-holidays

**Result:**

* Odds Ratio: 1.35
* P-value: 0.18

**Interpretation:** No statistically significant evidence that fatal injuries are more likely on holidays

---

## **🤖 Explanatory Modeling: Logistic Regression**

A logistic regression model was used to **quantify the impact of features on fatality risk**.

**Model Performance:**

* ROC AUC = 0.96 → Excellent ability to distinguish fatal vs. non-fatal injuries

**Top Features Associated with Fatalities:**

| Feature                                  | Coefficient | Odds Ratio |
| ---------------------------------------- | ----------- | ---------- |
| Nature of Injury: Asphyxiation, Drowning | +2.46       | ~11.7x     |
| Part of Body: Head                       | +2.14       | ~8.5x      |
| Part of Body: Whole Body                 | +2.02       | ~7.5x      |
| Part of Body: Internal Injuries          | +1.92       | ~6.8x      |
| Part of Body: Neck                       | +1.74       | ~5.7x      |

---

## **📊 Data Visualization**

A **Power BI dashboard** complements the analysis and allows **interactive exploration**:

* Total, fatal, and non-fatal incidents
* Most common injury types and affected body parts
* Environmental and human factors contributing to injuries
* Trends over time with filterable slicers

![Dashboard Preview](https://github.com/user-attachments/assets/5de8c746-0f12-42cc-bcfa-bf651c532ca9)

---

## **💡 Key Takeaways**

* Certain injury types and affected body parts carry **significantly higher fatality risk**
* Logistic regression is effective for **explanatory analysis**
* No significant difference in fatalities was observed on holidays
* Explanatory data science provides **valuable insights for high-risk industries** like construction

---

## **🛠 Tools Used**

* Python: `pandas`, `scikit-learn`, `matplotlib`, `seaborn`, `statsmodels`
* Jupyter Notebook
* Power BI for interactive dashboard visualizations
* Git & GitHub for version control


