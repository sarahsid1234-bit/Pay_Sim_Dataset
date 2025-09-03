# Pay_Sim_Dataset
## 📌 Project Overview
This project uses the **PaySim synthetic dataset**, which simulates mobile money transactions, to analyze fraud patterns and evaluate fraud detection gaps.  

The analysis was conducted in **SQL (DuckDB)** within Jupyter Notebooks, with additional visualization planned in **Power BI**.  
The project focuses on **business insights** rather than only technical metrics — highlighting risk areas, financial exposure, and system vulnerabilities.  

---

## 🛠️ Tools & Skills Used
- **SQL (DuckDB)** – Data querying, aggregation, and risk segmentation  
- **Python (Jupyter Notebook)** – Environment for SQL execution and analysis  
- **Power BI** – Dashboard creation and visualization (planned)  
- **Data Analytics & BI Skills** – KPI design, fraud pattern analysis, risk segmentation  
- **Business Context** – Fraud risk management, financial transaction analysis  

---

## 🔹 Analysis & Insights

### 1. Transaction Overview
- Fraud accounts for **<1% of transactions**, but with **high monetary impact**.
- Even rare fraud events can cause **major financial losses**.

### 2. Fraud by Transaction Type
- Fraud occurs only in **TRANSFER** and **CASH_OUT** transactions.
- Fraudulent transactions are significantly **higher in average value** compared to legitimate ones.
- Focus areas for fraud detection: **TRANSFER → CASH_OUT pipeline**.

### 3. User-Level Behavior
- Fraudulent accounts are mostly **receivers (`nameDest`)**, not senders.
- Patterns of repeated fraud:
  - **High Burst** – multiple frauds within 24 hours  
  - **Short Term** – repeated frauds within 7 days  
  - **Long Term** – spread over weeks  
- Indicates **money mule accounts** being reused.

### 4. Transaction Size Patterns
- Fraud likelihood increases sharply with **transaction amount**.  
- Fraudsters avoid low-value detection and focus on **large-value transfers**.

### 5. Temporal Trends
- Fraud events cluster around specific **time windows (`step`)**.  
- Suggests fraudsters exploit **system gaps (e.g., off-hours, batch cycles)**.

### 6. Counterparty Relationships
- Repeated fraud is concentrated in a **small group of receiver accounts**.  
- Sender accounts are usually **one-time fraud sources**.  
- Implies **fraud networks using repeated receivers**.

### 7. Financial Impact
- Fraud transactions sum up to **billions in value**.  
- A few **very large frauds dominate total losses**.  
- Blocking high-value frauds could drastically reduce financial risk.

### 8. Detection Gaps
- Only **0.2% of frauds were flagged** by the system (`isFlaggedFraud`).  
- **99.8% of fraud went undetected**, exposing serious monitoring gaps.  
- Stronger rules for **large transactions** and **repeat receivers** are needed.

---

## Key Takeaways
- Fraud is **low frequency, high severity**.  
- Targeted monitoring can drastically reduce risk:  
  - Focus on **TRANSFER + CASH_OUT** flows  
  - Flag **large-value transactions**  
  - Monitor **repeat receiver accounts**  
- Analytical methods like these can inform **fraud prevention systems** in financial institutions.
