# PaySim Kaggle Dataset Fraud Analysis

## 📊 Project Overview
This project analyzes fraud patterns and risks using the [PaySim synthetic dataset](https://www.kaggle.com/datasets/ntnu-testimon/paysim1), which simulates mobile money transactions. The goal is to surface business insights, identify system vulnerabilities, and inform fraud prevention strategies in financial services.

---

## 🛠️ Tools & Environment
- **Python (Jupyter Notebook):** Data wrangling, EDA, and SQL execution
- **DuckDB (via Python):** Fast, in-memory SQL analytics
- **Pandas & Plotly:** Data manipulation and interactive visualizations
- **Power BI (optional):** Advanced dashboarding and reporting
- **Business Analytics:** KPI design, fraud segmentation, risk analysis

---

## 📂 Data Source

- Dataset: [PaySim Kaggle Dataset](https://www.kaggle.com/datasets/ntnu-testimon/paysim1)
- License: See Kaggle dataset page for licensing and usage restrictions.

---

## 🚀 Getting Started

1. **Clone repository and download dataset:**
    ```bash
    git clone https://github.com/sarahsid1234-bit/Pay_Sim_Dataset.git
    ```
    Download `PS_20174392719_1491204439457_log.csv` from [Kaggle](https://www.kaggle.com/datasets/ntnu-testimon/paysim1) and place it in the project directory.

2. **Install dependencies:**
    ```bash
    pip install duckdb pandas plotly jupyter
    ```

3. **Run analysis:**
    - Open and run the Jupyter Notebook:  
      ```bash
      jupyter notebook
      ```
    - Follow notebook instructions to execute SQL queries and generate insights.

4. **(Optional) Visualize in Power BI:**
    - Export processed data for dashboarding.

---

## 🔎 Analysis & Insights

### 1. Transaction Overview
- Fraud accounts for **<1% of transactions** but results in **high financial impact**.

### 2. Fraud by Transaction Type
- Fraud found only in **TRANSFER** and **CASH_OUT** types.
- Fraudulent transactions have **much higher average values**.

### 3. User-Level Patterns
- Fraudulent accounts are primarily **receivers (`nameDest`)**.
- Notable patterns: **high burst**, **short-term**, and **long-term** frauds—suggesting money mule reuse.

### 4. Transaction Size & Temporal Trends
- Larger transaction amounts = higher fraud likelihood.
- Fraud clusters in specific **time windows**, indicating exploitation of system gaps.

### 5. Counterparty Relationships
- Fraud networks use a **small group of repeated receivers**.
- Senders are mostly **one-time fraud sources**.

### 6. Financial Impact & Detection Gaps
- Fraud losses total **billions**, with a few large transactions dominating.
- Only **0.2% of fraud flagged** by system—**99.8% undetected**, showing major monitoring gaps.

---

## 💡 Key Takeaways

- **Low frequency, high severity:** Even rare fraud events can cause substantial losses.
- **Improve detection:** Focus on large-value transactions, repeat receivers, and the TRANSFER→CASH_OUT pipeline.
- **Business impact:** Targeted monitoring can drastically reduce risk for financial institutions.

---

## 📑 References

- [PaySim Dataset on Kaggle](https://www.kaggle.com/datasets/ntnu-testimon/paysim1)
- [PaySim: A financial mobile money simulator for fraud detection research](https://www.sciencedirect.com/science/article/pii/S2352340918301186)
