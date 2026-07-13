# Customer_Churn_Analysis

### Overview
![image](https://github.com/beatrice-kirui/Phase-3-Project/assets/124546863/23cb49da-c595-4124-b08f-e9b5c2efe70e)
 
 This repository contains code for a machine learning project that analyzes a dataset of SyriaTel Customer Churn. The goal of this project is to analyze the dataset and develop a predictive model to identify factors that contribute to customer churn.By understanding these factors, the company can take proactive measures to reduce churn and improve customer retention. .

 ### Business Understanding:
 
 Customer churn refers to the phenomenon of customers leaving or discontinuing their services with the company.
 
 SyriaTel is a telecommunications company in Syria. They have realised that some of their customers have started to churn, discontinue their service.

This analysis will determine what features will indicate if a customer will ("soon") discontinue their service.By gaining insights into the factors contributing to churn, the company can take proactive measures to retain customers and improve customer loyalty.

### Data Understanding:

We used a dataset that contains relevant information about customers and their interactions with the company. The dataset includes features such as:-

1.CustomerID: Unique identifier for each customer.

2.AccountLength: The length of time the customer has been with SyriaTel.

3.InternationalPlan: Whether the customer has an international calling plan or not.

4.VoiceMailPlan: Whether the customer has a voicemail plan or not.

5.NumberVmailMessages: The number of voicemail messages received by the customer.

6.TotalDayMinutes: Total number of minutes the customer used during the day.

7.TotalEveMinutes: Total number of minutes the customer used during the evening.

8.TotalNightMinutes: Total number of minutes the customer used during the night.

9.TotalIntlMinutes: Total number of international minutes used by the customer.

10.TotalDayCalls: Total number of calls made by the customer during the day.

11.TotalEveCalls: Total number of calls made by the customer during the evening.

12.TotalNightCalls: Total number of calls made by the customer during the night.

13.TotalIntlCalls: Total number of international calls made by the customer.

14.CustomerServiceCalls: Number of customer service calls made by the customer.

15.Churn: Binary indicator of whether the customer churned or not.Additionally, it provides a binary target variable indicating whether a customer has churned or not. The dataset consists of structured data, including numerical, categorical, and ordinal variables.
        Explain your stakeholder audience and dataset choice here
### Modeling
![image](https://github.com/beatrice-kirui/Phase-3-Project/assets/124546863/49c3448f-4519-4268-a106-6d5cf83a0b5e)

* Out of 3,333 customers in the dataset ,483 have churned whereas 2850 have not churned.
* The distribution shows class imbalance which we will address before modelling. 

![image](https://github.com/beatrice-kirui/Phase-3-Project/assets/124546863/ef59381e-b53a-4e55-8b17-a78dd4587785)

* All of the plots displayed above except 'customer service calls' plot show a normal distibution.

* Total international calls is skewed to the right but still is normally distributed.

![image](https://github.com/beatrice-kirui/Phase-3-Project/assets/124546863/65193bee-06cd-4181-9923-0f0ca495d059)

Based on the AUC scores above,the models can be ranked in terms of perfomance:

    Random Forest: AUC = 0.93
    Logistic Regression: AUC = 0.83
    SVM: AUC = 0.72
    K Nearest Neighbors (KNN): AUC = 0.67

Based on the AUC scores, the Random Forest model appears to be the best-performing model among the four, followed by Logistic Regression, SVM, and KNN.

### Evaluation of the Final Model.

  After refining and evaluating several models, the Random Forest classifier was selected as the final model for this problem.

  The model underwent feature engineering, hyperparameter tuning, and cross-validation to optimize its performance.

  The final model, a Random Forest classifier, achieved an impressive overall performance with an accuracy of 96.64%. This indicates that the model correctly classified the majority of instances in the test set. Additionally, the model exhibited perfect precision with a score of 1.0, meaning that all instances predicted as positive were indeed true positives. However, there is room for improvement in terms of recall, as the model captured only 74.77% of the actual positive instances.

  The F1-score, which combines precision and recall into a single metric, was found to be 0.8556701030927836. This suggests a balanced performance between the two, although recall appears to be the weaker aspect of the model's performance. Nonetheless, the weighted average F1-score of 0.96 demonstrates a high level of overall model performance.

  
 In conclusion, the Random Forest model exhibited strong accuracy and precision, making it a reliable classifier. However, the model's lower recall indicates that it may not identify all positive instances accurately. It is crucial to consider the specific requirements and priorities of the problem at hand when interpreting these evaluation metrics and deciding on the final model. Further refinements could focus on improving the model's recall without sacrificing its high accuracy and precision.


### Conclusion

In conclusion after analysis the dataset provided valuable insights and recommendations to improve customer retention strategies. Through the modeling and evaluation process, a predictive model was developed to identify customers who are likely to churn. The analysis revealed that several factors contribute to customer churn in the telecom industry. By analyzing the dataset and building the predictive model, it was found that features such as call duration, customer complaints, billing issues, and contract type play a significant role in predicting churn. The model showed promising performance in accurately identifying potential churners.
