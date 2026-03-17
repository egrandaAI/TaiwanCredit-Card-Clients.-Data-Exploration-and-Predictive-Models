# Credit Risk Prediction & Customer Segmentation using Machine Learning

## 🌐 Live Report
Explore the full consulting-style report here:  
👉 [View Interactive Report](https://egrandaAI.github.io/Credit-Risk-ML-Analysis/)

## Overview

This project analyzes credit card client behavior using the **Default of Credit Card Clients dataset (UCI Repository)** to uncover key drivers of default risk and improve predictive modeling through machine learning.

The study combines **exploratory data analysis, supervised learning, and unsupervised clustering** to generate actionable insights for financial institutions aiming to enhance risk management and customer strategy.

---

## Business Problem

Credit default represents a major financial risk for banks and lending institutions. Traditional risk assessment models often struggle to capture the **complex, nonlinear relationships** between customer behavior, credit usage, and repayment patterns.

This project addresses three key challenges:

* Identifying the **main behavioral drivers of credit default**
* Improving prediction accuracy using **advanced machine learning models**
* Enabling **customer segmentation** for targeted financial strategies

---

## Dataset

* **Source:** UCI Machine Learning Repository
* **Size:** 30,000 credit card clients (Taiwan)
* **Timeframe:** April–September (historical data), predicting October default

### Key Features

* **Demographics:** Age, gender, education, marital status
* **Financial Capacity:** Credit limit (LIMIT_BAL)
* **Behavioral Data:**

  * Payment history (PAY_0 to PAY_6)
  * Billing amounts (BILL_AMT1 to BILL_AMT6)
  * Payment amounts (PAY_AMT1 to PAY_AMT6)
* **Target Variable:** Default payment (binary classification)

---

## Methodology

The project follows a three-layer analytical approach:

### 1. Exploratory Data Analysis (EDA)

* Feature engineering to improve interpretability:

  * `BILL_MEAN` (average bill)
  * `PAY_AMT_MEAN` (average payment)
  * `PAY_POWER` (payment-to-bill ratio)
  * `UTILIZATION` (credit usage ratio)
* Identification of nonlinear patterns and behavioral trends

### 2. Supervised Learning

* **Regression:** Predict credit limits
* **Classification:** Predict default risk
* Models evaluated using PyCaret and Scikit-learn

### 3. Unsupervised Learning

* **K-Means clustering** for behavioral segmentation
* **DBSCAN** for density-based validation

---

## Key Insights

### Behavioral Drivers of Default

* **Payment history is the strongest predictor of default risk**

  * Even small delays significantly increase future default probability
* **Credit utilization reflects financial stress**

  * High utilization correlates with higher risk
* **Spending alone is not predictive**

  * Must be combined with repayment behavior

### Data Characteristics

* Relationships are **nonlinear and noisy**
* Defaulting customers are **not linearly separable**
* Behavioral patterns evolve consistently over time

---

## Modeling Results

### Regression (Credit Limit Prediction)

* Linear Regression:

  * R² ≈ 0.59–0.61 → moderate performance
  * Limited by nonlinear relationships

* Tree-Based Models (Extra Trees Regressor):

  * R² ≈ 0.96 → strong predictive performance
  * Captures complex feature interactions

---

### Classification (Default Prediction)

* Best Model: **Gradient Boosting Classifier**

| Metric    | Value |
| --------- | ----- |
| AUC       | ~0.81 |
| Accuracy  | ~0.72 |
| Precision | ~0.79 |
| Recall    | ~0.61 |

#### Interpretation

* Strong ability to distinguish defaulters vs non-defaulters
* Low false positives → avoids unnecessary interventions
* Moderate recall → some defaulters remain undetected (key business risk)

---

## Customer Segmentation

### K-Means Clustering (k = 3)

Identified three behavioral segments:

* **Cluster 0 (Low Risk):**

  * Low utilization
  * Stable repayment behavior

* **Cluster 1 (Moderate Risk):**

  * Moderate utilization
  * Mixed repayment patterns

* **Cluster 2 (High Risk):**

  * High utilization
  * High payment stress and volatility

### Business Interpretation

* Enables **risk-based segmentation**
* Supports **personalized credit strategies**
* Identifies customers requiring **early intervention**

---

### DBSCAN Insights

* Revealed **continuous behavioral distribution** rather than distinct clusters
* Identified:

  * ~85% of customers in broad behavioral groups
  * ~17% noise → irregular or atypical profiles

Conclusion:
K-Means is more suitable for segmentation in this dataset

---

## Business Impact

This project demonstrates how machine learning can enhance financial decision-making through:

### Risk Management

* Early detection of high-risk customers
* Improved credit scoring systems

### Operational Strategy

* Dynamic credit limit adjustments
* Reduced financial losses from default

### Customer Experience

* Personalized financial products
* Targeted interventions for at-risk clients

---

## Limitations

* Missing key variables such as:

  * Income
  * Employment status
  * External credit scores
* Behavioral data alone limits full predictive accuracy

---

## Future Improvements

* Integrate **external financial data sources**
* Apply **advanced ensemble or deep learning models**
* Optimize classification thresholds based on business risk tolerance
* Deploy models into **real-time decision systems**

---

## Project Structure

```
credit-risk-analysis/
│
├── notebook.ipynb        # Full analysis and modeling
├── report.html           # Final report (visual version)
├── data/                 # Dataset
└── README.md             # Project overview (this file)
```

---

## License

This project is licensed under the **MIT License**.

You are free to use, modify, and distribute this project, provided that proper credit is given.

**Dataset:**
Default of Credit Card Clients Dataset — UCI Machine Learning Repository

---

## About Me

MSc in AI Management @ ESSCA (Paris)
Background in **Design, Data Analytics, and AI-driven Strategy**

I focus on bridging **data, business, and user experience** to build solutions that are both technically robust and strategically impactful.

---

## Key Takeaway

> Credit risk is not driven by isolated variables, but by **behavioral patterns over time**.
> Machine learning models that capture these dynamics can significantly improve financial decision-making and customer strategy.

---
