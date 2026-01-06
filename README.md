# Instacart Customer Behavior & Product Popularity Analysis

## Overview
This project analyzes the Instacart Online Grocery Shopping Dataset (2017) to understand customer purchasing behavior and predict product popularity. Using large scale transactional data, we combine exploratory analysis, customer segmentation, and machine learning to derive actionable business insights.

## Dataset
- **Source:** Instacart Market Basket Analysis (Kaggle)
- **Scale:** 3M+ orders, 200K+ users, 49K+ products
- **Data Files Used:** orders, products, aisles, departments, order_products_prior, order_products_train

## Project Objectives
- Segment customers using behavioral RFM (Recency, Frequency, Monetary) features
- Identify distinct customer purchasing patterns using K-Means clustering
- Predict product popularity using supervised machine learning models
- Analyze reorder behavior, category influence, and temporal shopping patterns

## Methodology

### Data Integration & Processing
- Merged six relational tables using `order_id`, `user_id`, and `product_id`
- Optimized memory usage for large-scale data using efficient Pandas operations
- Validated merged data through missing value checks, duplicates, and consistency checks

### Exploratory Data Analysis (EDA)
- Department and aisle-level demand analysis
- Reorder ratio distribution analysis
- Weekly and hourly shopping behavior trends
- Identification of high-loyalty and low-loyalty products

### Feature Engineering
- Computed **RFM metrics** for each customer:
  - Recency: Days since last purchase
  - Frequency: Total number of orders
  - Monetary: Average basket size
- Engineered product level features such as reorder ratio and total orders
- Encoded categorical variables (aisle, department)

## Customer Segmentation (Unsupervised Learning)
- Applied **K-Means clustering (k = 4)** on standardized RFM features
- Identified distinct customer segments including high-frequency loyal users and low-engagement users
- Interpreted clusters using scatter plots and box plots

## Product Popularity Prediction (Supervised Learning)
- Defined popularity as **top 25% of products by total historical orders**
- Trained and evaluated:
  - Logistic Regression
  - Decision Tree
  - Random Forest
- Used stratified train–test split for balanced evaluation

## Model Evaluation
Models were evaluated using:
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

**Random Forest** achieved the best overall performance, effectively capturing nonlinear relationships and feature interactions.

## Key Insights
- Reorder ratio is the strongest predictor of product popularity
- Produce and Dairy & Eggs are dominant, high-loyalty departments
- Peak ordering occurs between 10 AM – 4 PM, with Sundays and Mondays showing highest demand
- High-frequency customers represent the most valuable segment for retention strategies

## Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

## Project Status
- Code: Complete
- Report & Presentation: Complete

## Future Work
- Incorporate pricing, discounts, and review sentiment
- Apply time-series forecasting for demand prediction
- Explore deep learning and sequence-based recommendation models
