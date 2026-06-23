#  FedEx Logistics Performance Analysis

## Project Overview

This project performs an in-depth Exploratory Data Analysis (EDA) on the FedEx Logistics Performance dataset to uncover patterns in pharmaceutical supply chain operations. The analysis focuses on shipment performance, freight costs, delivery delays, transportation modes, product distribution, and global shipment trends.

The goal is to transform raw logistics data into actionable business insights that can help optimize transportation costs, improve delivery efficiency, and strengthen supply chain decision-making.

---

# Executive Summary / Key Insights

### Key Findings

* **Freight costs increase with shipment weight**, indicating a positive relationship between transportation expenses and shipment size.
* **Line Item Value and Insurance Cost show a very strong positive correlation (0.958)**, suggesting that higher-value shipments require significantly higher insurance coverage.
* **Delivery performance varies across shipment modes**, with certain transportation methods experiencing higher delays and greater variability.
* **A small number of countries contribute a significant share of total shipment value**, highlighting key markets within the pharmaceutical supply chain.
* **Shipment quantity strongly influences shipment value**, making volume planning a critical factor in logistics cost management.

---

# Dataset Information

### Dataset

**FedEx Logistics Performance Analysis Dataset (SCMS Delivery History Dataset)**

### Source

The dataset contains historical pharmaceutical shipment records including:

* Shipment details
* Vendor information
* Product groups
* Delivery dates
* Shipment modes
* Freight costs
* Insurance costs
* Product quantities
* Country information
* Delivery performance metrics

### Dataset Size

* **Rows:** 10,324
* **Columns:** 36

### Business Objective

Analyze logistics operations to identify opportunities for:

* Freight cost optimization
* Delivery performance improvement
* Supply chain efficiency enhancement
* Better shipment planning
* Risk reduction in global pharmaceutical distribution

---

# Repository Structure

```text
FedEx-Logistics-Performance-Analysis
│
├── notebooks/
│   └── FedEx_Logistics_Analysis.ipynb
│
├── images/
│   ├── correlation_heatmap.png
│   ├── shipment_mode_vs_delay.png
│   ├── global_shipment_map.png
│
├── README.md
│
└── requirements.txt
```

---

# Key Visualizations & Insights

## 1. Correlation Heatmap

![Correlation Heatmap](images/correlation_heatmap.png)

### Key Insight

The strongest positive relationship exists between:

* Line Item Value
* Line Item Insurance (USD)

This indicates that shipment insurance costs rise proportionally with shipment value. Shipment quantity also strongly influences overall shipment value.

---

## 2. Shipment Mode vs Delivery Delay

![Shipment Delay](images/shipment_mode_vs_delay.png)

### Key Insight

Different shipment modes exhibit varying levels of delivery delay and consistency.

This analysis helps identify transportation methods that offer more reliable delivery performance and lower operational risk.

---

## 3. Global Shipment Value Distribution

![Global Shipment Map](images/global_shipment_map.png)

### Key Insight

Shipment value is concentrated in a limited number of countries, indicating the presence of key markets that drive a significant portion of logistics activity.

These regions should be prioritized for inventory planning and operational improvements.

---

# Data Cleaning & Feature Engineering

The following preprocessing steps were performed to prepare the dataset for analysis:

### Missing Value Treatment

* Replaced invalid values in Weight (Kilograms) with null values.
* Replaced invalid values in Freight Cost (USD) with null values.
* Filled missing Weight values using median imputation.
* Filled missing Freight Cost values using median imputation.
* Filled missing Shipment Mode values using mode imputation.
* Filled missing Dosage values using mode imputation.
* Filled missing Insurance values with zero where appropriate.

### Date Processing

Converted the following columns into datetime format:

* Delivered to Client Date
* Delivery Recorded Date
* PO Sent to Vendor Date
* Scheduled Delivery Date
* PQ First Sent to Client Date

### Feature Engineering

Created the following new features:

* **Delay** = Delivered Date − Scheduled Delivery Date
* **Delivery Status** = On Time / Late
* **Month** = Extracted from Delivered to Client Date

---

# Exploratory Data Analysis

The project includes 20+ visualizations covering:

### Univariate Analysis

* Shipment Mode Distribution
* Fulfill Via Distribution
* Insurance Cost Distribution
* Weight Distribution

### Bivariate Analysis

* Country vs Shipment Count
* Weight vs Freight Cost
* Unit Price vs Pack Price
* Product Group vs Shipment Mode
* Shipment Mode vs Freight Cost
* Shipment Mode vs Delivery Delay

### Multivariate Analysis

* Bubble Chart Analysis
* Correlation Heatmap
* Pairplot
* Country vs Delivery Status
* Country vs Shipment Mode Heatmap
* Global Shipment Value Distribution

---

# Business Recommendations

Based on the analysis, the following recommendations are suggested:

1. Optimize freight costs through route planning and shipment consolidation.
2. Prioritize shipment modes with lower delays and more consistent performance.
3. Strengthen logistics operations in high-value countries.
4. Monitor high-value shipments to reduce insurance and transportation risks.
5. Diversify logistics strategies to improve supply chain resilience.
6. Implement real-time dashboards for continuous logistics monitoring.

---

# How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/fedex-logistics-performance-analysis.git

cd fedex-logistics-performance-analysis
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
FedEx_Logistics_Analysis.ipynb
```

and run all cells sequentially.

---

# Conclusion

This project demonstrates how exploratory data analysis can be used to uncover meaningful insights from logistics and supply chain data. Through data cleaning, feature engineering, statistical analysis, and visualization, the study identified key factors affecting freight costs, shipment value, insurance expenses, and delivery performance.

The insights generated from this analysis can help organizations improve operational efficiency, reduce transportation costs, strengthen delivery reliability, and support data-driven decision-making across the pharmaceutical supply chain.

---

## Author

**Jayati Nilekar**

B.Tech (Electronics & Communication Engineering)

Aspiring Data Analyst

### Skills

Python • SQL • Excel • Power BI • Tableau • Pandas • NumPy • Data Visualization • Exploratory Data Analysis
