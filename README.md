# Credit Card Customer Segmentation

[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-green.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📊 Overview

This project performs unsupervised customer segmentation on credit card users using K-Means clustering. By analyzing spending patterns, payment behaviors, and credit utilization, the model identifies distinct customer segments to enable data-driven business strategies.

## 🎯 Business Impact

The analysis segments customers into **5 distinct clusters** based on their financial behavior, enabling:
- 🎯 **Targeted marketing campaigns** for each customer segment
- 💰 **Risk assessment** for high cash-advance users
- 📈 **Customer retention** strategies for low-activity accounts
- 💳 **Product recommendations** based on spending habits

## 📁 Dataset

**Source:** Credit Card Customer Data  
**Records:** 8,950 customers  
**Features:** 18 behavioral and financial metrics

### Key Features:
| Feature | Description |
|---------|-------------|
| `BALANCE` | Monthly average balance |
| `PURCHASES` | Total purchase amount |
| `CASH_ADVANCE` | Cash advance withdrawals |
| `CREDIT_LIMIT` | Customer's credit limit |
| `PAYMENTS` | Total payments made |
| `PURCHASES_FREQUENCY` | How often customer makes purchases |
| `TENURE` | Customer relationship duration (months) |

## 🛠️ Technical Approach

### Methodology
1. **Data Preprocessing**
   - Removed customer ID column
   - Handled missing values with median imputation
   - Standardized features using StandardScaler

2. **Optimal K Selection**
   - Elbow Method (Inertia/WSS analysis)
   - Silhouette Score evaluation
   - **Optimal clusters: K=5**

3. **Clustering Algorithm**
   - K-Means clustering with n_init=10 for stability
   - PCA for 2D visualization

4. **Analysis & Interpretation**
   - Cluster profiling across all features
   - Business labeling based on behavioral patterns
   - Risk assessment for each segment

### Libraries Used
pandas # Data manipulation
numpy # Numerical operations
scikit-learn # StandardScaler, KMeans, PCA, metrics
matplotlib # Visualizations
seaborn # Enhanced plotting


## 📈 Results

### Customer Segments Identified

| Cluster | Size | Primary Label | Key Characteristics |
|---------|------|---------------|---------------------|
| 0 | 3,910 (43.7%) | Moderate Regular Users | Average balance $1,050, moderate usage |
| 1 | 1,385 (15.5%) | Moderate Regular Users | Higher spending, good payment behavior |
| 2 | 85 (0.9%) | Moderate Regular Users | Premium tier, high spenders |
| 3 | 2,415 (27.0%) | Moderate Regular Users | Low balance, conservative users |
| 4 | 1,155 (12.9%) | Cash Advance Dependent | High cash advance usage at 61% utilization |

### Key Insights

- **Risk Identification:** Clusters 0 and 4 show elevated cash advance usage requiring monitoring
- **Opportunity Segments:** Clusters 1 and 2 represent high-value customers for premium offerings
- **Retention Focus:** Dormant customers identified for re-engagement campaigns

## 📊 Visualizations

The analysis includes:
- Elbow plot for optimal K selection
- Silhouette score analysis
- PCA scatter plot of clusters (2D projection)
- Balance vs Purchases scatter plot
- Cluster comparison bar charts for key metrics

## 🚀 Getting Started
