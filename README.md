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
