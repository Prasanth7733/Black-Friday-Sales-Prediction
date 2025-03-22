# Black Friday Sales Prediction
![alt text](https://nypost.com/wp-content/uploads/sites/2/2024/10/black-friday-predictions.jpg?resize=1536,1024&quality=75&strip=all "Black Friday Sales Prediction")
## Table of Contents
- [Project Overview](#project-overview)
- [Dataset Description](#dataset-description)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Preprocessing](#data-preprocessing)
- [Modeling Phase](#modeling-phase)
- [Evaluation Metric](#evaluation-metric)
- [Conclusion](#conclusion)

## Project Overview
Black Friday marks one of the biggest shopping events in the United States, kicking off the holiday season with massive discounts. Retailers face the critical challenge of optimizing product prices to maximize profits. This project aims to predict purchase amounts using historical sales data, enabling businesses to make data-driven pricing decisions and improve revenue outcomes.

## Dataset Description
The dataset used in this project is sourced from an Analytics Vidhya hackathon and contains sales transaction records with the following features:
- **Demographics:** Age, Gender, Marital Status, City Category
- **Purchase Behavior:** Product Categories, Purchase Amount
- **City Dynamics:** Stay in Current City (Years)

### Dataset Statistics:
- **Records:** 537,577
- **Columns:** 12
- **Target Variable:** Purchase Amount

## Exploratory Data Analysis (EDA)
Through data visualization and analysis, we derived several key insights:
- **Gender-Based Spending:** Male consumers contribute approximately 75% of total purchases and tend to spend more on average than female consumers.
- **Marital Status:** Single men are the highest spenders, while spending decreases post-marriage, likely due to increased responsibilities.
- **Age Group Trends:** The 25-40 age group exhibits the highest spending behavior.
- **City Stay Duration:** Consumers new to a city (1-year residents) tend to spend the most, whereas long-term residents (4+ years) have reduced purchasing tendencies.
- **City-Wise Insights:** While City B generates the highest revenue overall, certain products sell more frequently in City C.

## Data Preprocessing
To prepare the data for modeling, we performed the following steps:
- **Encoding:** Used `LabelEncoder` for categorical features such as Age, Gender, and City Category.
- **One-Hot Encoding:** Applied `pd.get_dummies()` to transform `Stay_In_Current_City_Years` into indicator variables.
- **Missing Values:** Imputed missing values in `Product_Category_2` and `Product_Category_3`.

## Modeling Phase
We implemented multiple supervised machine learning models to predict purchase amounts:
1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**
4. **XGBoost Regressor**

### Train-Test Split:
- **Training Set:** 80%
- **Test Set:** 20%

## Evaluation Metric
The model performance was evaluated using **Root Mean Square Error (RMSE)**, which measures the difference between predicted and actual values. RMSE provides a reliable estimate of model accuracy.

## Conclusion
Among the tested models, **XGBoost Regressor** outperformed others with the best RMSE score of **2912**, making it the most effective model for predicting Black Friday purchase amounts. This project showcases the potential of machine learning in retail analytics, aiding businesses in strategic decision-making for optimal pricing strategies.

---
### 🔹 Author: Prasanth Babu  
### 🚀 Technologies Used: Python, Pandas, Scikit-Learn, XGBoost, Matplotlib, Seaborn

