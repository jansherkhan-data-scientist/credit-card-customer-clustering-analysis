# Credit Card Customer Clustering Analysis

[![Python 3.13+](https://img.shields.io/badge/Python-3.13+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

## 📊 Overview

This Jupyter Notebook performs **unsupervised customer segmentation** using K-Means clustering to identify distinct behavioral groups among credit card customers. The analysis helps financial institutions understand customer behavior, identify risk segments, and develop targeted business strategies.

## 🎯 What It Does

- Segments **8,950 customers** into **5 distinct behavioral clusters**
- Identifies **high-risk customers** (excessive cash advance usage)
- Discovers **high-value premium customers** for targeted retention
- Provides **actionable business recommendations** per segment

## 🔑 Key Insights

| Finding | Value |
|---------|-------|
| High-risk segment (cash advance dependency) | **43.7%** of customers |
| High-value premium customers | **0.9%** of customers |
| Optimal number of clusters | **K = 5** |
| Total customers analyzed | **8,950** |
| Features used for clustering | **17** |

## 📈 Output & Results

### Cluster Distribution
Cluster 0: 3,910 customers (43.7%) - High cash advance users
Cluster 1: 1,385 customers (15.5%) - Frequent purchasers
Cluster 2: 85 customers ( 0.9%) - Premium high-spenders
Cluster 3: 2,415 customers (27.0%) - Moderate regular users
Cluster 4: 1,155 customers (12.9%) - Extreme cash advance users


### Cluster Profiles (Averages)

| Cluster | Balance | Purchases | Cash Advance | Credit Limit | Payments | Purchase Freq | Risk |
|---------|---------|-----------|--------------|--------------|----------|---------------|------|
| **0** | $1,050 | $279 | $618 | $3,343 | $1,006 | 16.3% | ⚠️ HIGH |
| **1** | $1,905 | $2,925 | $361 | $6,987 | $2,789 | 92.4% | ✅ LOW |
| **2** | $4,516 | $15,897 | $1,040 | $12,452 | $15,564 | 92.7% | ✅ LOW |
| **3** | $644 | $797 | $178 | $3,198 | $935 | 85.6% | ✅ LOW |
| **4** | $4,604 | $485 | $4,611 | $7,529 | $3,578 | 27.9% | ⚠️ HIGH |

### Visualizations Generated

The notebook produces the following visualizations:
- **Elbow Method plot** for determining optimal K
- **Silhouette Score plot** for clustering quality validation
- **PCA scatter plot** showing cluster separation in 2D space
- **Balance vs Purchases scatter plot** for behavioral comparison
- **Bar charts** comparing cluster averages across key metrics

### PCA Explained Variance

- PC1 captures: **27.30%** of the variance
- PC2 captures: **20.31%** of the variance
- Total variance preserved: **47.61%**

## 💡 Business Recommendations

### Cluster 0 & 4 - High Risk (Cash Advance Dependent)
**56.6% of total customers (Clusters 0 & 4 combined)**

| Priority | Action | Expected Impact |
|----------|--------|-----------------|
| 🔴 IMMEDIATE | Implement automated alerts for excessive cash advance usage | Reduce risk exposure by 30-40% |
| 🔴 IMMEDIATE | Offer lower cash advance rates as retention incentive | Decrease default rates by 15-20% |
| 🟡 SHORT-TERM | Provide financial education and budgeting tools | Improve payment behavior within 3-6 months |
| 🟡 SHORT-TERM | Offer balance transfer options to reduce debt | Lower credit utilization by 20-25% |
| 🟢 LONG-TERM | Review and adjust credit limits based on risk assessment | Prevent future high-risk behavior |

**Risk Mitigation Metrics to Track:**
- Cash advance to purchase ratio (target: < 0.5)
- Credit utilization percentage (target: < 50%)
- Payment to balance ratio (target: > 1.0)

### Cluster 2 - Premium High-Value Customers (0.9%)

| Priority | Action | Expected Impact |
|----------|--------|-----------------|
| 🔴 IMMEDIATE | Assign dedicated relationship managers | Increase retention by 25-30% |
| 🟡 SHORT-TERM | Offer exclusive VIP benefits and luxury perks | Boost spend by 15-20% |
| 🟡 SHORT-TERM | Introduce premium travel and lifestyle rewards | Strengthen loyalty and advocacy |
| 🟢 LONG-TERM | Consider credit limit increases based on usage | Capture more high-value transactions |
| 🟢 LONG-TERM | Create referral programs with premium incentives | Acquire similar high-value customers |

### Cluster 1 & 3 - Regular Healthy Users (42.5%)

| Priority | Action | Expected Impact |
|----------|--------|-----------------|
| 🟡 SHORT-TERM | Launch personalized cashback programs | Increase transaction frequency by 10-15% |
| 🟡 SHORT-TERM | Offer tiered rewards based on spending tiers | Upgrade 5-10% to premium segment |
| 🟢 LONG-TERM | Cross-sell additional banking products | Increase share of wallet by 15-20% |
| 🟢 LONG-TERM | Build loyalty through engagement campaigns | Reduce churn by 10-15% |
| 🟢 LONG-TERM | Send targeted offers based on spending patterns | Boost average transaction value by 8-12% |


## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| **Language** | Python 3.13+ |
| **Data Processing** | Pandas, NumPy |
| **Machine Learning** | Scikit-learn (K-Means, PCA, StandardScaler) |
| **Visualization** | Matplotlib, Seaborn |

## 📈 Methodology

1. **Data Preprocessing** - Handle missing values, feature scaling
2. **Optimal K Selection** - Elbow method + Silhouette Score (K=5 selected)
3. **Clustering** - K-Means algorithm with 10 initializations
4. **Visualization** - PCA for 2D cluster visualization
5. **Interpretation** - Business insights & recommendations

## 📁 Dataset

The analysis uses **Credit Card Customer Data** with 8,950 records and 18 features including:
- Balance & credit limits
- Purchase behavior (frequency, amount, type)
- Cash advance patterns
- Payment history
- Customer tenure
