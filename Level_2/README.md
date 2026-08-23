# Level 2: Intermediate Analytics & Predictive Modeling

This level focuses on supervised regression modeling and unsupervised customer segmentation on the Telecom Customer Churn dataset.

---

## Task 1: Linear Regression (Usage vs. Charges)
- *Objective:* Train a simple linear regression model using scikit-learn to predict Total day charge based on Total day minutes.
- *Split:* 80% Training ($N = 533$), 20% Testing ($N = 134$).
- *Model Equation:* $\text{Total Day Charge} = (0.1700 \times \text{Total Day Minutes}) + 0.0003$
- *Performance:*
  - $R^2 = 1.0000$ (Near-deterministic linear relationship)
  - $\text{RMSE} \approx 0.0028$
  - $\text{MAE} \approx 0.0023$
- *Conclusion:* Proves a fixed billing rate of \$0.17 per day minute with zero base fee.

---

## Task 3: K-Means Clustering (Customer Segmentation)
- *Objective:* Segment customers by usage patterns (Total day minutes, Total eve minutes, Total night minutes, and Customer service calls).
- *Data Preprocessing:* Standardized using StandardScaler ($\mu=0, \sigma=1$).
- *Elbow Method:* Evaluated WCSS for $k=1$ to $10$; determined optimal cluster count at $k=3$.
- *Personas Identified:*
  1. *Standard/Balanced Users:* Moderate day/evening usage with low customer support reliance.
  2. *High-Usage Subscribers:* Heavy day and evening consumption; higher revenue potential.
  3. *High-Support / At-Risk Users:* Frequent customer service calls exhibiting elevated churn probability.
