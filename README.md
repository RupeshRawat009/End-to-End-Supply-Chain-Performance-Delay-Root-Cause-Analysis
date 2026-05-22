# 📦 End-to-End Supply Chain Performance & Delay Root Cause Analysis
### Data-Driven Logistics Diagnostics and Predictive Analytics to Recover Profitability

---
![Project Banner](https://img.shields.io/badge/Status-Completed-brightgreen)
![Python](https://img.shields.io/badge/Python-3.x-blue)
![SQL](https://img.shields.io/badge/SQL-Server-red)
![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)
![ML](https://img.shields.io/badge/ML-Random%20Forest-orange)

## 📌 Project Overview
Global e-commerce companies lose massive amounts of revenue and brand trust every year due to fulfillment failures. This end-to-end analytics project identifies why deliveries are late, where operational bottlenecks occur, and how to proactively predict risks — by combining Python-based data engineering, machine learning, and interactive Power BI dashboards. A **54.71% late delivery rate** was detected across **172,765 orders**, putting **$2.1M profit at risk** — this project uncovers the structural flaws behind those numbers and deploys a predictive solution.

---

## 🎯 Purpose
* **Identify Key Operational Drivers:** Conduct Root Cause Analysis (RCA) to pin down why delivery delays occur.
* **Quantify Financial Impact:** Measure the exact dollar value and "Profit at Risk" tied to logistics failures.
* **Predict Delivery Risks:** Build an ML model to forecast which new orders are likely to be delayed right at checkout.
* **Visualize Bottlenecks:** Construct an interactive Power BI dashboard to monitor regional fulfillment patterns.
* **Enable Proactive Strategy:** Empower supply chain management to take data-driven action before SLAs are breached.

---

## 🛠️ Tech Stack

| Tool | Purpose |
| :--- | :--- |
| **Python** | Primary programming language for data manipulation, analysis, and modeling |
| **Pandas & NumPy** | Data extraction, cleaning, feature engineering, and matrix operations |
| **Scikit-learn** | Random Forest Classifier, Train-Test Split, and Classification Evaluation Metrics |
| **Imblearn (SMOTE)** | Handling target variable class imbalance via synthetic oversampling |
| **Matplotlib & Seaborn** | Statistical plotting, delay distributions, and feature importance visualization |
| **Power BI & DAX** | Interactive executive dashboards, KPI calculation, and root cause visual monitoring |

---

## 🗄️ Data Source
* **Dataset:** DataCo Smart Supply Chain Dataset (via Kaggle)
* **Total Records:** 172,765 highly validated orders (filtered from 180,000+ raw records)
* **Columns:** 53 raw features streamlined to 20 core analytical variables
* **Key Engineered Columns:**
  * `Order Processing Time`
  * `Delay (Days)`
  * `Is_Delayed` / `Late_delivery_risk` (Binary target variable)
  * `Order Hour` & `Order Month`

---

## 🚀 Features & Highlights

### 🔷 1. End-to-End Python Data Pipeline
* Loaded raw dataset using strictly defined `latin-1` encoding to handle global geographical data.
* Executed rigorous dimensionality reduction and dropped canceled orders to establish a clean analytical baseline.
* Applied **Frequency Encoding** to high-cardinality categorical columns (like *Order Region* and *Department Name*) to optimize for machine learning models.
* Engineered critical chronological tracking features (`Order Processing Time`, `Delay Days`).

### 🔷 2. Diagnostic & Root Cause Analysis (RCA)
* **Global Delay Rate:** `54.71%` of total orders failed to meet promised delivery windows.
* **Profit at Risk:** `$2.1 Million` of generated profit exposed to customer churn.
* **Primary Logistical Failure:** *First Class Shipping* shows a catastrophic `100%` delay rate.
* **Top Administrative Hurdle:** Orders stuck in `PAYMENT_REVIEW` suffer an `80%` delay rate.
* **Regional Bottleneck:** *Central Africa* leads global delays at `58.7%`.
* **Temporal Vulnerabilities:** Peak delays occur seasonally in **Aug, Sep, Dec**, and hourly at **8:00 PM (Hour 20)**.

### 🔷 3. Machine Learning Model
* **Algorithm:** Random Forest Classifier (Ensemble Decision Trees)
* **Class Imbalance Handling:** SMOTE (Synthetic Minority Over-sampling Technique) applied *exclusively* to training data to equalize classes at 79,000 records each.
* **Train/Test Split:** 80% Train / 20% Test
* **Top Predictive Features:** `Shipping Mode`, `Order Hour`, and `Order Region`.

### 🔷 4. Power BI Dashboard
Executive dashboard built using Power BI and DAX measures featuring:
* **Top Tier:** KPI cards tracking *Total Orders*, *Late Deliveries*, *On-Time %*, *Total Profit*, and *Profit at Risk ($2.1M)*.
* **Middle Tier:** Profitability Split (Donut Chart) and Delay % by Shipping Mode (Bar Chart).
* **Bottom Tier:** Delay distribution insights, regional bottlenecks, and temporal capacity trends mapping out peak stress months.

## 📊 Dashboard & Prediction Insights

<table>
  <tr>
    <td><b>Supply Chain Dashboard</b></td>
    <td><b>Delay Root Cause Analysis</b></td>
  </tr>
  <tr>
    <td><img src="https://github.com/RupeshRawat009/End-to-End-Supply-Chain-Performance-Delay-Root-Cause-Analysis/raw/main/SupplyChainDashboard.png" width="100%" alt="Supply Chain Dashboard"></td>
    <td><img src="https://github.com/RupeshRawat009/End-to-End-Supply-Chain-Performance-Delay-Root-Cause-Analysis/raw/main/DelayRootAnalysis.png" width="100%" alt="Delay Root Cause Analysis"></td>
  </tr>
</table>
---
## 🔍 Deep-Dive Insights & Data Discoveries

Through intensive **Exploratory Data Analysis (EDA)**, **Augmented AI Analytics**, and **Machine Learning Feature Importance evaluations**, this framework isolated three critical systemic vulnerabilities within the DataCo supply chain operations.

---

### 1. 💵 The Financial Paradox: Volume-Driven vs. Margin-Driven Loss
A structural correlation analysis was conducted by mapping aggregate financial performance against sequential delivery delay buckets (ranging from -2 days early to 4+ days late).

* **📉 The Margin Stability Discovery:** Counter-intuitively, the per-order profitability remains structurally fixed at a mean of **~$22.00** across the entire delay spectrum. An order delayed by 4+ days preserves virtually the same net margin as an order delivered on time.
* **⚠️ The Volume Trap:** The financial crisis is entirely **volume-driven**. The process failure peaks at the **1-Day Delay Bucket**, which chokes the infrastructure by trapping **30.96% of all global transactions (53,503 orders)**. 
* **🎯 Strategic Takeaway:** Delays do not immediately erode individual product margins through immediate logistical overhead; instead, they lock up **$1.19 Million** in shifting "Profit at Risk" zones, threatening long-term revenue through diminished Customer Lifetime Value (CLV) and brand friction.

---

### 2. 🕒 Operational Bottleneck: The Afternoon Shift Changeover Lag
Analyzing delivery dynamics across a continuous 24-hour cycle exposed a distinct operational inflection point embedded within warehouse fulfillment hours.

* **⚡ The 12:00 PM Inflection:** Up until mid-day, processing pathways remain highly efficient, maintaining a baseline delay rate of **53.4%**. However, immediately following 12:00 PM, the system experiences a profound performance degradation.
* **📈 The Peak Friction Zone:** Delay rates surge sharply, peaking at **62.4%** and sustaining high latency through **10:00 PM (22:00)**. 
* **💡 Strategic Takeaway:** Because 75% of total aggregate orders are committed before 5:00 PM, this temporal pattern isolates a severe resource deficit or tracking mismatch during the afternoon shift changeover. The incoming surge of late-day orders chokes processing queues due to an inefficient operational handover protocol.

---

### 3. 🚨 Structural Flaw: Flawed "First Class" Service Level Agreements (SLAs)
By deploying Power BI’s AI-driven Key Influencers visual (leveraging automated logistic regression), the system isolated categorical variables that disproportionately increase processing latency.

* **🏷️ The Premium Failure:** The framework mathematically proved that choosing **First Class shipping increases the global probability of an order hitting a delay by 51%** compared to all other shipping tiers. 
* **⚙️ The Root Cause:** This uncovers a severe operational contradiction. Standard Class segments (4–6 day delivery window) have lower failure rates simply because their SLA deadlines are lenient. First Class orders are scheduled with an aggressive 1-day turnaround target, while the baseline physical processing capabilities of the fulfillment centers require a minimum of **2.0 days** to complete packaging.
* **🎯 Strategic Takeaway:** The catastrophic delay rate is not a consequence of poor regional tracking or local execution failures; it is a **systemic administrative flaw** where premium transit targets are structurally misaligned with real-world warehouse capabilities.

---

## 📊 Prescriptive Action Matrix

Based on the empirical insights discovered above, the framework proposes a three-tiered corporate optimization strategy:

| Target Area | 🔍 Core Analytical Discovery | 🛠️ Prescriptive Action | 🚀 Expected Business Impact |
| :--- | :--- | :--- | :--- |
| **SLA Alignment** | First Class shipping increases delay probability by **51%**. | Recalibrate First Class scheduling algorithms from a **1-day** target to an operationally viable **2-day** baseline. | Eliminates systemic administrative failures; radically drops fulfillment risk KPIs. |
| **Warehouse Operations** | Latency peaks sharply to **62.4%** between **12:00 PM and 10:00 PM**. | Implement a **1-hour overlapping shift transition** and automate cross-dock queue handovers at 12:00 PM. | Smooths out the afternoon ordering surge; flattens the hourly delay curve. |
| **Risk Management** | Machine Learning features prioritize Shipping Mode and Order Hour. | Deploy the optimized **Random Forest Classifier** at the checkout layer to flag high-risk transactions instantly. | Shifts operations from **Reactive to Proactive**, allowing managers to adjust carriers before packages leave the loading dock. |


## 📈 Results Summary

| Metric | Value |
| :--- | :--- |
| **Total Orders Analyzed** | 172,765 |
| **Late Delivery Rate** | 54.71% |
| **Profit at Risk** | $2.1 Million |
| **90th Percentile Delay** | 3 Days |
| **Model Overall Accuracy** | 74% |
| **Model Precision (Late Risk)** | 79% |
| **Model Recall (Late Risk)** | 75% |
| **Model F1-Score** | 0.77 (Late Risk class) |

---

## 🙋 Author

**Rupesh Singh Rawat**
* 📧 Email: [rupeshrawat133@gmail.com](mailto:rupeshrawat133@gmail.com)
* 🔗 LinkedIn: [LinkedIn Profile](https://linkedin.com) *(Update with your actual link!)*
* 📬 Connect with me on LinkedIn: Rupesh Singh Rawat

---

⭐ **If you found this project helpful, please give it a star!**

_Built with ❤️ using Python | Scikit-Learn | Power BI_
