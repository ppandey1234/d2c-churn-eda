# D2C Customer Churn Analysis & EDA

## Project Overview

This project performs a comprehensive **Data Quality Audit**, **Exploratory Data Analysis (EDA)**, and **Churn Risk Investigation** for a Direct-to-Consumer (D2C) business.

The objective is to identify customer behavior patterns, operational issues, and business drivers that contribute to customer churn.

---

## Business Problem

Customer churn directly impacts revenue, customer lifetime value, and acquisition costs.

This analysis aims to:

- Understand characteristics of churned customers
- Identify behavioral signals leading to churn
- Evaluate operational metrics impacting retention
- Generate actionable insights for churn reduction strategies

---

## Dataset Description

The project uses the following datasets:

| Dataset | Description |
|----------|-------------|
| customers.csv | Customer demographic and profile information |
| orders.csv | Customer order history |
| support_tickets.csv | Customer support interactions |
| web_events_snapshot.csv | Website/App engagement data |
| intervention_history.csv | Retention campaign history |
| churn_labels.csv | Target churn labels |

---

## Project Workflow

### 1. Data Quality Audit

Performed checks for:

- Missing values
- Duplicate records
- Invalid data types
- Referential integrity
- Outlier detection
- Data consistency

### 2. Exploratory Data Analysis

Analyzed:

#### Customer Behavior
- Order Frequency
- Average Order Value
- Recency
- Refund Rate

#### Operational Metrics
- Delivery Delay
- Support Ticket Volume
- Ticket Resolution Performance

#### Engagement Metrics
- Website Activity
- App Usage
- Campaign Responses

#### Churn Analysis
- Churn Distribution
- Feature-wise Churn Comparison
- Customer Segmentation

---

## Key Findings

### Low Order Frequency Increases Churn Risk

Customers with:

```text
Orders ≤ 3
```

show significantly higher churn rates.

---

### High Refund Rates Correlate with Churn

Customers with frequent refunds demonstrate elevated churn risk, indicating dissatisfaction with products or services.

---

### Delivery Delays Impact Retention

Long delivery delays are associated with increased customer churn.

---

### Support Issues are Strong Churn Indicators

Customers generating multiple support tickets tend to churn more frequently.

---

### Campaign Engagement Reduces Churn

Customers responding positively to retention campaigns exhibit lower churn rates.

---

## Visualizations Included

- Churn Distribution
- Order Frequency vs Churn
- Refund Rate vs Churn
- Delivery Delay vs Churn
- Support Ticket Analysis
- Campaign Response Analysis
- Customer Segmentation Charts

---

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Repository Structure

```text
├── customers.csv
├── orders.csv
├── support_tickets.csv
├── web_events_snapshot.csv
├── intervention_history.csv
├── churn_labels.csv
├── eda_audit.ipynb
├── README.md
```

---

## How to Run

### Clone Repository

```bash
git clone https://github.com/ppandey1234/d2c-churn-eda.git
cd d2c-churn-eda
```

### Create Virtual Environment

```bash
python -m venv .venv
```

### Activate Environment

Windows:

```bash
.venv\Scripts\activate
```

Linux/Mac:

```bash
source .venv/bin/activate
```

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Run Notebook

```bash
jupyter notebook eda_audit.ipynb
```

---

## Future Enhancements

- Churn Prediction Model
- Customer Segmentation using Clustering
- Retention Strategy Recommendation Engine
- Automated EDA Dashboard
- Real-Time Churn Monitoring

---

## Author

**Piyush Pandey**

Data Science | Machine Learning | Generative AI

GitHub: https://github.com/ppandey1234