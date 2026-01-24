# Customer Drop-off, Conversion & Attrition Risk Analysis for an E-commerce Product

### Objective:
#### Analyse customer engagement, identify conversion drop-off points, and segment customers by attrition risk to support product and retention decisions.

---
## Data Quality and Assumption
Behavioural engagement metrics with missing values were imputed using the median. This decision reflects the skewed nature of engagement data and ensures robust segmentation without overstating or understating user activity. Missing values are treated as unknown rather than zero activity.

---
## Funnel Construction

### Engagement Score
A composite engagement score was constructed using normalised login frequency, average session duration, and pages per session. A simple average was chosen to maintain interpretability and avoid arbitrary weighting. Users above the median engagement score were classified as “engaged” for funnel analysis.

### Conversion and Value Features
Conversion was defined as at least one completed purchase. Revenue per customer was derived to support value-based segmentation. Cart abandonment was treated as a relative friction score and high-abandonment users were identified using percentile-based thresholds to avoid unit ambiguity.

### Recency and Frequency Segmentation
Customers were segmented into recency and purchase-frequency buckets to support churn risk assessment. Thresholds were chosen to reflect common retention intervention windows rather than optimise predictive accuracy.

### Exploratory Proxy Funnel Construction
Due to the absence of event-level data, a customer-level proxy funnel was constructed using behavioural engagement, friction indicators, and purchase outcomes. This approach allows identification of meaningful drop-off points while remaining robust to data granularity constraints.

Note: This funnel was constructed as an initial proxy but exhibited near-total conversion between intent and purchase, indicating structural bias in the dataset.

### Revised Funnel: Engagement -> Conversion -> Retention
Initial conversion logic based on lifetime purchase resulted in near-total conversion among engaged users, reflecting dataset bias toward historical purchasers. Conversion was therefore refined to represent active purchasing behaviour by incorporating recency criteria, aligning the funnel with decision-making and retention use cases.

---
