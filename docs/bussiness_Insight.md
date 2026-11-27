# Business Insights — Customer Churn Analysis

## 1. Business Objective

The objective of this project is to analyze customer churn in a telecommunications company, identify patterns associated with customer cancellations, and translate data into actionable business recommendations.

The analysis focuses on customer behavior, contract characteristics, subscribed services, payment methods, and potential financial impact.

## 2. Business Questions

The analysis is guided by the following questions:

- What is the overall customer churn rate?
- Which customer segments present different churn rates?
- Is contract type associated with customer cancellations?
- Are additional services associated with customer retention?
- Does customer tenure relate to churn behavior?
- Is there a relationship between payment methods and customer cancellations?
- What is the estimated monthly revenue associated with churned customers?

These questions guide the investigation and do not represent confirmed findings.

## 3. Methodology

### 3.1 Data Preparation

Before performing the analysis, the dataset was inspected and prepared.

The preparation process included:

- Checking dataset dimensions and data types.
- Identifying missing values and duplicated records.
- Validating categorical variables.
- Converting numerical columns to appropriate data types.
- Investigating inconsistencies in `TotalCharges`.
- Creating derived variables when necessary.

### 3.2 Exploratory Data Analysis

Exploratory Data Analysis (EDA) was conducted to understand customer characteristics and identify patterns associated with churn.

The analysis used:

- Descriptive statistics.
- Frequency distributions.
- Grouped comparisons.
- Churn rate calculations.
- Histograms and bar charts.
- Cross-segment comparisons.

### 3.3 Segment Comparison

Customer segments were compared using churn rates rather than absolute cancellation counts.

This approach helps account for differences in segment sizes.

For each categorical variable, the analysis considers:

- Total customers.
- Churned customers.
- Churn rate.
- Segment size.

### 3.4 Numerical Variable Analysis

Numerical variables such as `tenure`, `MonthlyCharges`, and `TotalCharges` were investigated using descriptive statistics, distributions, and grouped comparisons.

Where appropriate, numerical variables were divided into ranges to facilitate interpretation.

### 3.5 Financial Analysis

The financial analysis considers the monthly charges associated with customers who canceled their subscriptions.

**Revenue at Risk** is calculated as the sum of `MonthlyCharges` for churned customers.

This is an estimate of the monthly charges associated with canceled customers, not a confirmed measure of financial loss.

## 4. Key Performance Indicators (KPIs)

| KPI | Definition |
|---|---|
| Total Customers | Total number of unique customers. |
| Churned Customers | Number of customers who canceled. |
| Churn Rate | Percentage of customers who canceled. |
| Retention Rate | Percentage of customers who remained. |
| Average Tenure | Average customer relationship duration. |
| Monthly Revenue | Sum of monthly charges in the analyzed dataset. |
| Revenue at Risk | Sum of monthly charges associated with churned customers. |

## 5. Business Findings

This section will document the findings supported by the analysis.

#### 5.1 Customer Overview

**Business Question:**
- What is the overall customer churn situation, and how significant is customer loss for the company?

**Evidence:**
- The dataset contains 7,043 customer records.
- 1,869 customers have churned, while 5,174 remain with the company.
- Approximately one in every four customers has discontinued the service.
**Metrics analyzed:**
- Total customers: 7,043
- Churned customers: 1,869
- Retained customers: 5,174
- Churn rate: 26.54%
- Retention rate: 73.46%
**Finding:**
- The overall churn rate is 26.54%, meaning that more than a quarter of the customers in the dataset have left the company.
**Business interpretation:**
- Customer churn represents a significant retention challenge. Although most customers remain with the company, the proportion of customers who leave indicates that retention strategies deserve attention.
- This overview establishes a baseline for identifying which customer segments are more likely to churn in the following analyses.
**Business impact:**
- A churn rate of 26.54% highlights the importance of understanding customer behavior and identifying factors associated with cancellations.
- Reducing churn could help the company preserve its customer base and maintain recurring revenue. Further analysis is necessary to identify the segments and factors that should be prioritized.

### 5.2 Contract Analysis

**Business Question:** Is contract type associated with customer churn?

- **Evidence:** The analysis identified a churn rate of 42.71% among Month-to-month customers, compared to 11.27% for One-year contracts and 2.83% for Two-year contracts. Month-to-month customers accounted for 88.55% of all churned customers.
- **Additional Analysis:** Within the Month-to-month segment, customers with 0–10 months of tenure presented a churn rate of 52.57%.
- **Metrics Analyzed:** Total Customers, Churned Customers, Churn Rate, Share of Total Churn, Contract Type, and Tenure Groups.
- **Finding:** Customer churn rates differ substantially across contract types. The Month-to-month segment also presents elevated churn among customers with shorter tenure.
- **Business Interpretation:** Contract type and customer relationship duration are important dimensions to investigate when evaluating customer retention. However, the analysis does not establish that contract flexibility itself causes cancellations.
- **Business Impact:** The company could prioritize retention monitoring for Month-to-month customers, particularly during the initial months of their relationship.
- **Recommendation:** Investigate onboarding, customer experience, pricing perception, and contract renewal incentives for this segment. Test retention initiatives and monitor their results.

### 5.3 Customer Profile Analysis

**Business Question:** Do customer characteristics differ across churn segments?

- **Evidence:** Churn rates were compared across gender, senior citizen status, partner status, and dependent status. Gender presented similar rates, while the other profile dimensions showed larger differences.
- **Metrics Analyzed:** Total Customers, Churned Customers, Churn Rate, Gender, SeniorCitizen, Partner, and Dependents.
- **Finding:** Customer profile segments present different churn rates, although the magnitude of the differences varies by characteristic.
- **Business Interpretation:** Customer profile information may help identify segments that deserve further investigation. These characteristics should not be interpreted as direct causes of cancellation.
- **Business Impact:** Segment-level analysis may support more targeted customer retention strategies.
- **Recommendation:** Investigate whether the observed differences remain when controlling for contract type, tenure, and subscribed services.

### 5.4 Services Analysis

**Business Question:** Are subscribed services associated with different churn rates?

- **Evidence:** Within the Month-to-month segment, Fiber optic customers presented a churn rate of 54.61%, compared to 32.22% for DSL and 18.89% for customers without internet service.
- **Additional Evidence:** Customers subscribed to OnlineSecurity and TechSupport presented different churn rates compared to customers without these services. Similar comparisons were conducted for OnlineBackup, DeviceProtection, StreamingTV, and StreamingMovies.
- **Metrics Analyzed:** Total Customers, Churned Customers, Churn Rate, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, and StreamingMovies.
- **Finding:** Churn rates vary across internet service types and additional service subscriptions within the Month-to-month segment.
- **Business Interpretation:** The differences suggest that service subscription patterns are relevant dimensions for further investigation. The available data does not establish whether service adoption itself influences retention or whether other customer characteristics explain the differences.
- **Business Impact:** Understanding these patterns may help the company identify customer segments that require additional support or a different service strategy.
- **Recommendation:** Investigate service quality, customer support interactions, and subscription adoption. Evaluate whether targeted onboarding or support initiatives improve retention.

### 5.5 Payment Method Analysis

**Business Question:** Is payment method associated with customer cancellations?

- **Evidence:** Electronic check customers presented a churn rate of 45.29%, compared to 16.71% for automatic bank transfers, 15.24% for automatic credit card payments, and 19.11% for mailed checks.
- **Additional Evidence:** Within the Month-to-month segment, Electronic check customers presented a churn rate of 53.73%, while the other payment methods presented lower rates.
- **Metrics Analyzed:** Total Customers, Churned Customers, Churn Rate, Share of Total Churn, PaymentMethod, and Contract.
- **Finding:** Electronic check is associated with substantially higher churn rates in the overall customer base and within the Month-to-month segment.
- **Business Interpretation:** Payment method may be a useful dimension for identifying customer segments with higher cancellation rates. The analysis does not establish that the payment method causes churn.
- **Business Impact:** The company may be able to identify higher-risk customer groups and investigate potential friction in the payment experience.
- **Recommendation:** Investigate payment failures, billing complaints, and customer preferences. Test whether offering alternative payment methods improves retention.

### 5.6 Customer Tenure Analysis

**Business Question:** How does customer relationship duration relate to churn?

- **Evidence:** Customers with 0–10 months of tenure presented a churn rate of 49.14%. The rate progressively differed across the analyzed tenure groups, reaching 2.26% among customers with 71 or more months of tenure.
- **Metrics Analyzed:** Tenure, Tenure Groups, Total Customers, Churned Customers, and Churn Rate.
- **Finding:** Customer churn rates differ considerably across tenure groups, with higher rates observed among customers with shorter recorded relationship durations.
- **Business Interpretation:** The initial customer relationship period deserves attention when evaluating retention. However, the snapshot dataset does not provide a complete longitudinal history of each customer's behavior.
- **Business Impact:** Identifying customers at risk during the early relationship period may help the company prioritize retention initiatives.
- **Recommendation:** Investigate the onboarding experience and evaluate retention interventions during the first months of the customer relationship.

### 5.7 Financial Impact Analysis

**Business Question:** What is the estimated monthly revenue associated with churned customers?

- **Evidence:** The sum of MonthlyCharges associated with churned customers was $139,130.85. The total monthly charges across the analyzed customer base were $456,116.60.
- **Additional Evidence:** Month-to-month customers accounted for $120,847.10 of the monthly charges associated with churned customers.
- **Metrics Analyzed:** MonthlyCharges, Total Monthly Charges, Average Monthly Charges, Contract, and Churn.
- **Finding:** A substantial amount of monthly charges is associated with customers who canceled their subscriptions, with the largest portion coming from the Month-to-month segment.
- **Business Interpretation:** Customer cancellations have a relevant revenue dimension. The calculated amount represents monthly charges associated with churned customers, not confirmed future revenue losses.
- **Business Impact:** Improving customer retention may help preserve recurring revenue, although the financial benefit of any intervention must be measured separately.
- **Recommendation:** Prioritize the investigation of high-churn customer segments and evaluate retention initiatives using customer retention and recurring revenue indicators.

## 6. Business Recommendations

Recommendations will be developed based on validated findings.

For each recommendation, the following information must be documented:

1. Identified business problem.
2. Supporting evidence.
3. Proposed action.
4. Expected business benefit.
5. Suggested performance indicator.
6. How the company could evaluate the action.

Recommendations should be treated as proposals to test, not guaranteed outcomes.

## 7. Limitations

The analysis has some limitations:

- The dataset represents a specific customer snapshot.
- The available data does not establish a complete historical sequence of customer behavior.
- Statistical associations do not prove causation.
- The dataset may not represent the entire telecommunications market.
- Revenue at Risk is an estimate based on monthly charges, not confirmed future revenue loss.
- Segment comparisons should consider differences in sample sizes.

## 8. Conclusion

The final conclusion will summarize the most relevant findings, their potential business implications, and the recommendations supported by the analysis.

All conclusions will be based on calculated metrics and documented evidence.