# 🏦 Mitron Bank Credit Card Analysis — Power BI

An interactive Power BI dashboard analyzing credit card usage patterns, spending behaviors, and customer segments to support a fictional bank's new credit card product launch strategy.

---

## 📌 Project Overview

Mitron Bank is planning to launch a new line of credit cards. This project analyzes transactional and demographic data of **4,000 customers** across **5 cities** to identify high-value customer segments, spending categories, and payment behaviors — enabling data-driven product design and marketing decisions.

> 🏆 This project is based on **Codebasics Resume Project Challenge #8**

---

## 📊 Key Results

| Metric | Finding |
|---|---|
| Customers Analyzed | **4,000 customers** |
| Cities Covered | **5 major cities** |
| Spending Categories | **6 categories tracked** |
| Customer Segments | **4 demographic segments** |
| Dashboard Pages | **4 interactive report pages** |

---

## 🗂️ Dataset

- **Source:** [Codebasics Resume Project Challenge #8](https://codebasics.io/challenge/codebasics-resume-project-challenge)
- **How to get it:**
  1. Go to 👉 https://codebasics.io/challenge/codebasics-resume-project-challenge
  2. Find **Challenge #8 — Provide Insights to the Product Strategy Team in the Banking Domain**
  3. Download the dataset zip file — it contains:

| File | Description |
|---|---|
| `dim_customers.csv` | 4,000 customers — age group, city, gender, occupation, income |
| `fact_spends.csv` | Transaction data — spend amount, category, payment type, month |

> 💡 **Note:** The data is also embedded inside the `.pbix` file — you can open it directly in Power BI Desktop without downloading the CSVs separately.

---

## 🛠️ Tech Stack

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures-orange?style=flat-square)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat-square&logo=microsoft-excel&logoColor=white)

---

## 🔍 Analysis Breakdown

### 👥 Customer Demographics
- Age group distribution and credit card usage patterns
- Income utilization % by segment
- Gender-wise spending comparison
- City-wise customer distribution

### 💳 Spending Analysis
- Top spending categories: Bills, Groceries, Electronics, Travel, Food, Entertainment
- Monthly spending trends across categories
- Average transaction value by customer segment

### 💰 Payment Behavior
- Credit card vs UPI vs net banking vs debit card usage
- Payment method preference by age group and city
- On-time payment rate analysis

### 🎯 Customer Segmentation
- High-value vs low-value customer identification
- Income utilization ratio to flag credit-worthy segments
- Salaried vs business owner vs freelancer spend patterns

---

## 💡 Key Business Insights

- 💼 **Salaried IT employees** had the highest income utilization (43%) — prime target segment
- 🛒 **Bills and groceries** account for 35%+ of total spend — cashback features recommended
- 🏙️ **Mumbai and Delhi** customers drive the highest transaction volumes
- 📅 **August–October** shows consistent spending spikes — seasonal campaign opportunity
- 💳 **Ages 25–34** are most likely to adopt new credit card products

---

## 📁 Project Structure

```
Mitron-Bank-Credit-Card-Analysis/
│
├── Bank Credit Card Analysis.pbix    # Full Power BI dashboard (data embedded)
├── datasets.zip                      # Dataset: dim_customers.csv + fact_spends.csv
└── README.md
```

---

## ▶️ How to Open

1. Download and install **Power BI Desktop** — free at [powerbi.microsoft.com](https://powerbi.microsoft.com)
2. Download `Bank Credit Card Analysis.pbix` from this repo
3. Open the file in Power BI Desktop
4. Use slicers (city, age group, gender, month) to explore the interactive dashboard

---

## 📐 DAX Measures Used

```dax
-- Income Utilization %
Income Utilization % =
DIVIDE(SUM('fact_spends'[spend_amount]), SUM('dim_customers'[monthly_income])) * 100

-- Average Transaction Value
Avg Transaction Value =
AVERAGEX('fact_spends', 'fact_spends'[spend_amount])

-- Credit Card Usage Rate
CC Usage Rate =
DIVIDE(
    CALCULATE(COUNT('fact_spends'[id]), 'fact_spends'[payment_type] = "Credit Card"),
    COUNT('fact_spends'[id])
) * 100
```

---

## 💡 Key Learnings

- Building multi-page interactive Power BI dashboards for business stakeholders
- Writing DAX measures for KPI calculations and ratio analysis
- Customer segmentation and behavioral analysis using visual analytics
- Translating raw transactional data into actionable product strategy recommendations

---

## 👩‍💻 Author

**Devika Lahari Bandi**
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/devika-lahari/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat-square&logo=github)](https://github.com/Devikalahari03)
