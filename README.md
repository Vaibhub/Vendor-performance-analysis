
# 🧾 Vendor Performance Analysis – Retail Inventory & Sales

Analyzing vendor efficiency and profitability to support strategic purchasing and inventory decisions using **SQL, Python, and Power BI**.

---

## 📌 Table of Contents

```html
Overview
Business Problem
Dataset
Tools & Technologies
Project Structure
Data Cleaning & Preparation
Exploratory Data Analysis (EDA)
Research Questions & Key Findings
Dashboard
How to Run This Project
Final Recommendations
Author & Contact
```

---

<h2><a class="anchor" id="overview"></a>Overview</h2>

This project evaluates vendor performance and retail inventory dynamics to drive strategic insights for purchasing, pricing, and inventory optimization. A complete data pipeline was built using **SQL for ETL, Python for analysis and hypothesis testing, and Power BI for visualization.**

---

<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Effective inventory and sales management are critical in the retail sector. This project aims to:
- Identify underperforming brands needing pricing or promotional adjustments
- Determine vendor contributions to sales and profits
- Analyze the cost-benefit of bulk purchasing
- Investigate inventory turnover inefficiencies
- Statistically validate differences in vendor profitability

---

<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- Multiple CSV files located in the `/data/` folder *(sales, vendors, inventory)*
- Summary table created from ingested data and used for analysis

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- SQL *(Common Table Expressions, Joins, Filtering)*
- Python *(Pandas, Matplotlib, Seaborn, SciPy)*
- Power BI *(Interactive Visualizations)*
- GitHub

---

<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```text
vendor-performance-analysis/
│
├── README.md
├── .gitignore
├── requirements.txt
├── Vendor Performance Report.pdf
│
├── notebooks/                  # Jupyter notebooks
│   ├── exploratory_data_analysis.ipynb
│   ├── vendor_performance_analysis.ipynb
│
├── scripts/                    # Python scripts for ingestion and processing
│   ├── ingestion_db.py
│   └── get_vendor_summary.py
│
├── dashboard/                  # Power BI dashboard file
│   └── vendor_performance_dashboard.pbix
````

---

<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>

* Removed transactions with:

 Gross Profit ≤ 0
 Profit Margin ≤ 0
 Sales Quantity = 0

* Created summary tables with vendor-level metrics
* Converted data types, Handled outliers, Merged lookup tables

---

<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

### Negative or Zero Values Detected

* **Gross Profit:** Minimum = **-52,002.78** *(loss-making sales)*
* **Profit Margin:** Minimum = **-∞** *(sales at zero or below cost)*
* **Unsold Inventory:** Indicates slow-moving stock

### Outliers Identified

* High Freight Costs *(up to 257K)*
* Large Purchase Prices
* Large Actual Prices

### Correlation Analysis

* Weak correlation between **Purchase Price & Profit**
* Strong correlation between **Purchase Quantity & Sales Quantity (0.999)**
* Negative correlation between **Profit Margin & Sales Price (-0.179)**

---

<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>

* **    Brands for Promotions:** 198 brands with low sales but high profit margins.

* **Top Vendors:** Top 10 vendors account for **65.69%** of purchases, indicating a risk of over-reliance.

* **Bulk Purchasing Impact:** Large orders provide approximately **72% cost savings per unit.**

* **Inventory Turnover:** Approximately **$2.71M** worth of inventory remains unsold.

### Vendor Profitability

* High Vendors: Mean Margin = **31.17%**
* Low Vendors: Mean Margin = **41.55%**

### Hypothesis Testing

A statistically significant difference in vendor profit margins indicates distinct vendor pricing strategies.

---

<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>

* The Power BI Dashboard includes:

 Vendor-wise Sales and Margins
 Inventory Turnover
 Bulk Purchase Savings
 Performance Heatmaps

! [Vendor Performance Dashboard](images\dashboard.png)

---

<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

### Clone the repository

```bash
git clone https://github.com/yourusername/vendor-performance-analysis.git
```

### Load CSV files and ingest into database

```bash
python scripts/ingestion_db.py
```

### Create vendor summary table

```bash
python scripts/get_vendor_summary.py
```

### Open and run notebooks

```text
notebooks/exploratory_data_analysis.ipynb

notebooks/vendor_performance_analysis.ipynb
```

### Open Power BI Dashboard

```text
dashboard/vendor_performance_dashboard.pbix
```

---

<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>

* Diversify vendor base to reduce risk
* Optimize bulk order strategies
* Reprice slow-moving, high-margin brands
* Clear unsold inventory strategically
* Improve marketing for underperforming vendors

---

<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Vaibhav agarwal**\n
**Data Analyst**

📧 Email: [vaibhavagarwal582@gmail.com] \n
🔗 [LinkedIn](https://www.linkedin.com/in/vaibhavagarwal582/)


```
```
