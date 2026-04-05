# Problem Statement
You are a junior data analyst at a retail company. Your manager hands you a dataset of past customer orders and asks you to build a model that predicts whether a customer will make a repeat purchase within 30 days.

The dataset contains the following columns:

| Column | Description |
|--------|-------------|
| customer_id | Unique customer identifier |
| order_count_last_90d | Number of orders placed in the last 90 days |
| avg_order_value | Average order value in INR |
| days_since_last_order | Days elapsed since the customer's most recent order |
| repeat_purchase_flag | 1 if the customer made a repeat purchase within 30 days, 0 otherwise |
| discount_used_on_repeat_order | Discount applied on the repeat purchase order |

## Task 1
**Label Identification**: The label is `repeat_purchase_flag` because it directly indicates the target variable we aim to predict (repeat purchase within 30 days).

**Data Leakage Risk**: Including `discount_used_on_repeat_order` as a feature would introduce data leakage. This is because the discount information is only known after the repeat purchase occurs, making it unavailable during prediction and thus invalid for training.

## Task 2
Two critical steps skipped before training the gradient boosting model are:
1. **Data Preprocessing**: Handling missing values, outliers, and scaling features ensures the model learns from clean, standardized data, preventing biased or unstable predictions.
2. **Feature Engineering**: Creating meaningful derived features (e.g., recency, frequency) or encoding categorical variables improves model interpretability and performance by capturing patterns not evident in raw data.