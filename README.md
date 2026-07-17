# Customer Churn Analysis

## Project Summary

Customer churn is one of the most significant challenges faced by subscription-based businesses. Acquiring a new customer is often more expensive than retaining an existing one, making early identification of customers at risk of leaving a valuable business capability.

This project analyzes customer data from SyriaTel to identify the factors associated with customer churn and develops machine learning models capable of predicting customers who are likely to discontinue their services. The project follows a complete data science workflow, including exploratory data analysis, feature engineering, data preprocessing, model development, evaluation, and business recommendations.

Among the models evaluated, the Random Forest classifier achieved the best performance with an **AUC score of 0.93**, demonstrating a strong ability to distinguish between customers who churn and those who remain.

---

# Business Problem

SyriaTel has experienced customer attrition, leading to revenue loss and increased customer acquisition costs. The company requires a predictive solution that can identify customers at high risk of churning before they leave.

By understanding the drivers of customer churn and building predictive machine learning models, the business can implement proactive retention strategies, improve customer satisfaction, and reduce revenue loss.

---

# Project Objectives

The objectives of this project were to:

- Explore customer behavior using exploratory data analysis (EDA).
- Identify factors associated with customer churn.
- Prepare and preprocess data for machine learning.
- Compare multiple classification algorithms.
- Evaluate model performance using appropriate classification metrics.
- Recommend business strategies to reduce customer churn.

---

# Dataset

The dataset contains information for **3,333 SyriaTel customers** and includes customer demographics, account information, service plans, call usage, and customer service interactions.

### Target Variable

- **Churn**
    - 0 = Customer retained
    - 1 = Customer churned

### Initial Class Distribution

|Class|Customers|
|------|---------:|
|Retained|2,850|
|Churned|483|

The dataset exhibited class imbalance, making it necessary to apply techniques that improve the model's ability to identify minority-class observations.

---

# Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- imbalanced-learn (SMOTE)
- Jupyter Notebook

---

# Data Preprocessing

Several preprocessing steps were performed before model development.

### Feature Engineering

Categorical variables were transformed into numerical features using **One-Hot Encoding**.

The following variables were encoded:

- State
- Area Code
- International Plan
- Voice Mail Plan

### Feature Scaling

Numerical variables were scaled to improve model performance.

The project utilized:

- StandardScaler
- MinMaxScaler

depending on the requirements of the machine learning algorithm.

### Handling Class Imbalance

The target variable was highly imbalanced:

|Before SMOTE|Customers|
|-------------|---------:|
|Retained|2,850|
|Churned|483|

To prevent the models from becoming biased toward the majority class, the **Synthetic Minority Oversampling Technique (SMOTE)** was applied.

After applying SMOTE:

|After SMOTE|Customers|
|-------------|---------:|
|Retained|2,850|
|Churned|2,850|

This balanced dataset enabled the models to better learn patterns associated with customer churn.

### Train-Test Split

The dataset was divided into:

- **75% Training**
- **25% Testing**

using:

- `random_state = 123`

---

# Exploratory Data Analysis

Exploratory Data Analysis was conducted to understand customer behavior, identify patterns, detect class imbalance, and explore relationships between variables.

Key observations included:

- The dataset was highly imbalanced.
- Most numerical variables followed approximately normal distributions.
- Customers with international plans and frequent customer service calls showed stronger associations with churn.
- Call usage and customer interaction variables provided valuable predictive information.

---

# Model Development

Four supervised machine learning models were developed and evaluated.

- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

### Hyperparameter Tuning

Logistic Regression was optimized using **GridSearchCV** with **5-fold cross-validation**.

The following parameters were tuned:

- Regularization strength (C)
- Solver

This helped identify the optimal model configuration before evaluation.

---

# Model Performance

|Model|AUC Score|
|------|---------:|
|Random Forest|**0.93**|
|Logistic Regression|0.83|
|Support Vector Machine|0.72|
|K-Nearest Neighbors|0.67|

The Random Forest classifier produced the strongest predictive performance and was selected as the final model.

---

# Final Model Evaluation

The Random Forest model achieved:

- Accuracy: **96.64%**
- Precision: **1.00**
- Recall: **74.77%**
- F1 Score: **0.86**

The model demonstrated excellent overall performance while maintaining high precision. Although recall indicates that some churning customers were still missed, the model provides a reliable foundation for customer retention initiatives.

---

# Business Recommendations

Based on the analysis, SyriaTel could reduce customer churn by:

- Monitoring customers who make frequent customer service calls.
- Identifying high-risk customers using the predictive model.
- Developing targeted customer retention campaigns.
- Reviewing service plans associated with higher churn.
- Implementing proactive customer engagement before customers decide to leave.

---

# Repository Structure

```

customer-churn-analysis/
│
├── customer_churn_analysis.ipynb
├── syria_churn.csv
├── README.md
├── documentation.pdf
├── Notebook.pdf
├── Presentation.pdf

```

---

# How to Run the Project

Clone the repository:

```bash
git clone https://github.com/beatrice-kirui/customer-churn-analysis.git
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook and open:

```
customer_churn_analysis.ipynb
```

---

# Future Improvements

Potential enhancements include:

- Experimenting with XGBoost and LightGBM.
- Optimizing recall for better identification of churning customers.
- Deploying the model as a web application.
- Building an interactive Power BI or Tableau dashboard.

---

# Author

**Beatrice Kirui**

Data Analyst | Python | SQL | Machine Learning | Data Visualization

GitHub: https://github.com/beatrice-kirui
LinkedIn: https://www.linkedin.com/in/beatrice-kirui-2a38a9205/
