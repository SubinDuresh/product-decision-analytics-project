# Customer Funnel & Churn Risk Analysis (E-commerce)

## Project Overview

This project analyses customer behaviour within an e-commerce product to identify where users drop off in the conversion funnel and to segment active customers by churn risk. The objective is to support retention prioritisation and inform product and customer strategy using behavioural and transactional data.

The analysis focuses on decision-ready insights rather than predictive modelling, reflecting real-world data constraints often encountered in product analytics contexts.

**Full Analysis:**
[View the full analysis notebook](Notebooks/01_data_cleaning_and_features.ipynb)

## Business Problem

Despite strong top-of-funnel engagement, e-commerce products frequently experience revenue leakage due to post-purchase disengagement and customer attrition.

This project addresses two core questions:  

Where and why are customers dropping off in the conversion funnel?  

Which active customers are at highest risk of churn, and why?

## Data Quality and Constraints
- Customer-level behavioural and transactional dataset (aggregated)
- No event-level interaction logs or time-series purchase history
- Churn observed as a binary outcome without timestamps

Given these constraints, the analysis prioritises transparent assumptions, rule-based logic, and internal validation over black-box modelling.

## Analytical Approach

The analysis followed four structured steps:

### 1. Data Quality Assessment & Cleaning
Handling missing behavioural metrics, unrealistic values, and distributional skew.

### 2. Feature Engineering
Construction of:

- Engagement score (multi-metric composite)
- Recency buckets
- Value proxies (lifetime value)
- Friction indicators (cart abandonment, returns behaviour)

### 3. Proxy Funnel Construction
A proxy funnel was built to reflect engagement, active conversion, and retention under data aggregation constraints.

### 4. Rule-Based Churn Risk Segmentation
Active customers were segmented into low, medium, and high churn risk groups using a hierarchical framework centred on recency, engagement, value, and friction.

## Funnel Analysis
The final funnel revealed that while a high proportion of engaged users convert to active purchasers, a significant drop-off occurs at the retention stage. This indicates that post-purchase retention, rather than acquisition or initial conversion, represents the primary source of revenue leakage.

## Churn Risk Segmentation

Churn risk was assessed only for active, non-churned customers to avoid outcome leakage.
A rule-based segmentation approach was used to ensure interpretability and alignment with business decision-making.

Internal validation confirmed clear behavioural separation between risk groups across:

- Purchase recency
- Engagement levels
- Lifetime value
- Friction incidence

## Key Insights

- Retention represents the largest opportunity for revenue impact, exceeding acquisition or conversion improvements.
- Purchase recency is the strongest early indicator of churn risk.
- High-risk customers are not inherently low-value; many exhibit substantial historical lifetime value.
- Friction behaviours strongly differentiate churn risk tiers.
- Medium-risk customers offer the highest return on targeted retention interventions.

## Business Recommendations & Next Steps

- Prioritise retention initiatives for medium-risk customers to maximise ROI.
- Implement recency-based triggers for proactive re-engagement campaigns.
- Address friction drivers (e.g., checkout or returns experience) for high-risk users.
- With access to event-level data, future work could extend this framework into predictive churn modelling and controlled retention experiments.

### Repository Contents
- `Data/README.md` — Data source documentation
- `Notebooks/01_data_cleaning_and_features.ipynb` — Full end-to-end analysis
- `README.md` — Project overview and insights
