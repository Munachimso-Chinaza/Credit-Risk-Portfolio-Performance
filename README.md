![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

# Credit Risk & Portfolio Performance Analytics

---

## 📌 Overview

This project presents a comprehensive evaluation of retail loan default risk, borrower credit profiles, and portfolio performance metrics based on an analysis of **32,581 loan records**[cite: 5]. The primary objective of this project is to identify primary risk drivers, evaluate current underwriting and risk-based pricing efficiency, and outline strategic recommendations to mitigate default exposure while optimizing loan portfolio yield.

---

## 🛠️ Technology Used

* **Programming Language:** Python[cite: 1]
* **Data Manipulation & Analysis:** Pandas, NumPy[cite: 5]
* **Data Visualization:** Matplotlib, Seaborn[cite: 2, 3]
* **Database / Querying:** SQL (PostgreSQL / SQLite syntax)
* **Interactive Dashboard:** Tableau[cite: 12]

---

## 🔄 Project Workflows

1. **Data Collection & Ingestion:** Loaded the raw credit risk dataset into Pandas and performed initial structural inspections (`credit.columns`, `head()`)[cite: 1, 5, 6].
2. **Data Cleaning & Handling:** Inspected missing values, standardized column names, and prepared data types for downstream manipulation.
3. **Feature Engineering:** 
   * Created custom age group brackets (**Teenager**, **Young Adult**, **Middle-Aged**, **Senior**).
   * Binned loan amounts relative to income into distinct tiers (`< 10%`, `10% - 20%`, `20% - 30%`, `> 30%`)[cite: 9].
4. **Exploratory Data Analysis (EDA):** Aggregated metrics using SQL and Pandas to evaluate default probabilities across loan purposes, risk grades, income burdens, and homeownership statuses[cite: 7, 8, 9, 10, 11].
5. **Dashboard Development:** Designed a multi-quadrant executive dashboard in Tableau incorporating interactive filters for age groups, loan grades, and default status labels[cite: 12].

---

## 📊 Key Insights

* **Prior Bureau Defaults:** Borrowers with a prior default on record default at **37.81%**, compared to **18.39%** for clean credit files[cite: 7].
* **Critical Debt Burden Tipping Point:** When loan amounts exceed **30% of annual income**, the default rate spikes dramatically to **70.32%**[cite: 9].
* **Loan Purpose Risk Ranking:** **Debt Consolidation** and **Medical** loans pose the highest portfolio risk with default rates of **28.59%** and **26.70%** respectively[cite: 8].
* **Credit Rating Calibration:** Risk grades show severe deterioration in higher tiers, culminating in a **98.44% default rate** for Grade G loans—where interest pricing fails to cover expected losses[cite: 10].
* **Homeownership Impact:** **Renters** present a **31.57% default rate**, whereas outright homeowners exhibit superior repayment discipline with a **7.47% default rate**[cite: 11].

---

## 💡 Recommendations

1. **Enforce Hard Debt Caps:** Implement a strict underwriting cap at **25%–30% loan-to-income** to eliminate the segment responsible for a 70.32% default rate[cite: 9].
2. **Restructure High-Risk Grades:** Discontinue automated approvals for **Grades E, F, and G** due to catastrophic default exposure (up to 98.44%)[cite: 10].
3. **Refine Pricing for Defaulters:** Introduce stricter debt-to-income criteria and mandatory co-signers for applicants with prior bureau default history[cite: 7].
4. **Targeted Policy by Purpose:** Require direct creditor disbursement for **Debt Consolidation** loans to prevent stacked debt accumulation[cite: 8].
5. **Incorporate Housing Status in Models:** Enhance liquidity verification requirements for **Renters** due to their elevated default frequency[cite: 11].
