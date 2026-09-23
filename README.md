# 📊 Customer Service Analytics — Excel Data Analysis Project

## 📌 Project Overview

This project is a **Customer Service Analytics** solution built in Excel to evaluate operational performance across cases, agents, customer satisfaction, handling time, consult outcomes, languages, resolution status, and agent tenure.

The project combines **data cleaning, Power Query preparation, Data Modeling, DAX measures, PivotTables, interactive filtering, KPI reporting, and business insights** to turn raw customer-service data into an analytical report.

---

## 🧹 Data Cleaning & Preparation

A major part of the project was preparing the data before analysis and ensuring that the model works with reliable and consistent data.

The cleaning process focused on the main data-quality checks:

- **Missing Values** — identifying and handling missing data.
- **Errors** — detecting and resolving data errors.
- **Duplicates** — checking for duplicate records.
- **Validate** — validating values and ensuring they follow the required rules.
- **Detected Type** — checking and correcting detected data types.
- **Outliers** — identifying unusual values using the **IQR (Interquartile Range) method**.

The prepared data was then structured for analysis and loaded into the workbook's analytical model.

---

## 🧩 Data Model

The project uses an Excel **Data Model** to connect the analytical tables and allow measures to work consistently across different dimensions.

### Main Model Tables

- **AHT Data**
- **Survey Data**
- **Hire Dates**
- **Date**
- **Dim_Tenure**
- **Dim_Consult_Outcome**
- **MeasuresTable**

### 🔗 Relationships

The model connects the main fact data with dimension tables through fields such as:

- `Date`
- `Agent`
- `Tenure Range`
- `Consult Outcome`

A dedicated **Date table** is used for time-based analysis, while separate dimension tables are used for **Tenure** and **Consult Outcome**.

This structure makes it possible to analyze the same KPIs from multiple perspectives without duplicating calculations.

---

## 🧮 DAX & Measures

The project uses **DAX measures** to create dynamic KPIs and analytical calculations instead of relying only on static Excel calculations.

Key analytical measures include:

- **# Cases**
- **# Agents**
- **# Active Agents**
- **CSAT**
- **CSAT Target**
- **AHT Avg**
- **AHT Target**
- **Average Wrap Time**
- **Helped Resolve Rate**
- Resolution-related KPIs

The measures are designed to respond dynamically to filters such as:

- Agent
- Consult Outcome
- Tenure Range
- Month
- Year

A dedicated **MeasuresTable** is also included to organize the model's measures.

---

## 📊 Report & Dashboard

The report presents customer-service performance through KPI cards, PivotTables, and analytical views.

### Main KPI Overview

The overall report shows:

| KPI | Actual | Target |
|---|---:|---:|
| Cases | 12,954 | — |
| Agents | 65 | — |
| Active Agents | 46 | — |
| CSAT | 3.82 | 4.20 |
| AHT Avg | 38.74 min | 28 min |

The dashboard/report can be analyzed interactively using slicers for **Agent, Consult Outcome, Tenure Range, Month, and Year**.

---

## 📈 Key Insights

### 1. Overall Performance Gap

Overall performance is below target:

- **CSAT = 3.82 vs 4.20 target**
- **AHT = 38.74 min vs 28 min target**

This indicates that the main challenge is not only customer satisfaction but also efficiency.

### 2. Consult Outcomes Are Major Performance Drivers

The analysis shows that specific **Consult Outcomes** have a much stronger relationship with performance than tenure alone.

#### 🔴 Issue Code 2
- **1,587 cases**
- **CSAT: 2.70**
- **AHT: 23.78 min**

CSAT is significantly below target even though AHT is below the target. This suggests that speed is not the main issue; resolution quality or customer expectations may require further investigation.

#### 🔴 Issue Code 4
- **892 cases**
- **CSAT: 2.95**
- **AHT: 40.95 min**

This outcome negatively affects both CSAT and AHT and should be a priority for root-cause investigation.

#### 🔴 Issue Code 6
- **1,211 cases**
- **CSAT: 3.60**
- **AHT: 41.15 min**

Its relatively high volume combined with below-target CSAT and above-target AHT makes it an important performance gap.

#### 🟠 Issue Code 1
- **5,507 cases**
- **CSAT: 4.26**
- **AHT: 42.17 min**

CSAT is slightly above target, but the very high case volume and high AHT make this the largest contributor to efficiency pressure.

#### 🟠 Issue Code 7
- **1,866 cases**
- **CSAT: 4.43**
- **AHT: 49.57 min**

Customer satisfaction is strong, but AHT is significantly above target. This represents an opportunity to improve efficiency without sacrificing customer satisfaction.

---

## 📅 Time-Based Insights

December is a major area for investigation:

- **CSAT: 1.67**
- **AHT: 60.57 min**

December combines the **lowest CSAT** with the **highest AHT** in the available monthly analysis, making it a clear operational warning period.

---

## 👥 Agent & Tenure Analysis

The analysis compares agent performance across different tenure ranges.

The results show that the performance gap is relatively consistent across tenure groups. This suggests that **agent tenure alone is not the primary explanation for the overall performance gap**.

Therefore, investigating specific **Consult Outcomes and operational processes** is likely to provide more actionable results than focusing only on tenure.

---

## 🌍 Language Performance

The report also compares AHT across languages:

- English
- French
- German
- Italian
- Spanish

This allows the team to identify languages with relatively higher handling times and investigate whether additional operational or process factors may be contributing.

---

## ✅ Resolution Analysis

The project analyzes resolution status and its relationship with customer satisfaction.

The overall resolution rate is approximately **73.27%**, while resolved cases have substantially higher CSAT than unresolved cases:

- **Resolved CSAT: 4.48**
- **Not Resolved CSAT: 2.02**

This is one of the strongest findings in the analysis and highlights the importance of effective case resolution for customer satisfaction.

---

## 🎯 Business Recommendations

Based on the analysis:

1. **Prioritize Issue Codes 4 and 6** because they create both CSAT and AHT pressure.
2. **Investigate Issue Code 2** to understand why CSAT is low despite relatively low AHT.
3. **Review Issue Code 1 and Issue Code 7** for efficiency improvements because of their high AHT and significant case volumes.
4. **Investigate December operations** because of the extreme CSAT and AHT gap.
5. Focus on improving **case resolution quality**, since resolved cases show much higher CSAT.
6. Use the interactive model to drill down from overall KPIs to **agent, tenure, language, month, and consult outcome**.

---

## 🛠️ Tools & Techniques

- Microsoft Excel
- Power Query
- Data Cleaning
- Missing Values Handling
- Error Handling
- Duplicate Detection
- Data Validation
- Data Type Detection
- Outlier Detection using IQR
- Data Modeling
- Relationships
- DAX
- Measures
- PivotTables
- Slicers
- KPI Analysis
- Customer Service Analytics
- Business Insights

---

## 📁 Workbook Structure

The project contains:

- `AHT Data`
- `Survey Data`
- `Hire Dates`
- `Date`
- `Dim_Tenure`
- `Dim_Consult_Outcome`
- `Measures`
- `Report`
- `Dashboard`
- `insights`

---

## 👨‍💻 Author

**Hamada Ahmed**

Customer Service Data Analysis Project
