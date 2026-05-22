# 📦 End-to-End Supply Chain Performance & Delay Root Cause Analysis
### Data-Driven Logistics Diagnostics and Predictive Analytics to Recover Profitability

---

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

---

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
