# Customer Churn Analysis

A data analysis project focused on identifying customer churn patterns, understanding the characteristics of customers who leave a telecommunications company, and generating actionable business insights.

## Project Overview

Customer churn is one of the main challenges for subscription-based businesses. Understanding why customers leave helps companies identify risk factors and develop customer retention strategies.

This project explores the **Telco Customer Churn** dataset to investigate customer behavior, contract characteristics, service usage, payment methods, and potential revenue impact.

## Objectives

- Measure the overall customer churn rate.
- Identify which contract types have the highest churn rates.
- Investigate the relationship between customer tenure and churn.
- Analyze how additional services relate to customer retention.
- Evaluate churn patterns across payment methods.
- Estimate the monthly charges associated with customers who churned.
- Translate analytical findings into business recommendations.

## Dataset

The project uses the Telco Customer Churn dataset, which contains information about telecommunications customers.

| Attribute | Description |
|---|---|
| Records | 7,043 customers |
| Features | 21 columns |
| Target variable | `Churn` |
| Data categories | Customer demographics, services, contracts, payments, and charges |

## Technologies Used

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

## Analysis Process

The project followed these analytical stages:

1. **Data Understanding:** Examining the dataset structure, variables, and data types.
2. **Data Cleaning:** Identifying inconsistent values and handling missing information.
3. **Exploratory Data Analysis (EDA):** Investigating distributions and relationships between variables.
4. **Customer Segmentation:** Comparing churn rates across contracts, tenure groups, services, and payment methods.
5. **Business Insights:** Interpreting the findings and identifying potential retention opportunities.


## Project Structure

```text
customer-churn-analysis/
│
├── dashboard/
│   └── Costumer Churn Analysis.pbix
│   └── screenshots/
│       └── page1.png
│       └── page2.png
│       └── page3.png
│       └── page4.png
│
├── data/
│   └── processed
│       └── customer_churn_clean.csv
│   └── raw 
│       └── WA_Fn-UseC_-Telco-Customer-Churn.csv
│
├── notebooks/
│   └── 01_data_cleaning.ipynb
│   └── 02_exploratory_analysis.ipynb
│
├── docs
│   └── bussiness_Insight.md
│
└── README.md
```
## Limitations

- The analysis identifies statistical associations, not causal relationships.
- The dataset does not provide enough information to establish the exact reasons behind every cancellation.
- The financial impact calculation represents the monthly charges associated with churned customers, not actual realized losses.
- Further analysis and validation would be necessary before implementing business strategies.

## Author

**Vinicius Santos Silva**

Data Science student interested in Data Analytics, Business Intelligence, and data-driven decision-making.
