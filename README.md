# **Data Analysis for Marketing Campaign**
---

## **Introduction**
### **Project Background**
In today's competitive market, customer loyalty is a key element in the success of businesses. To encourage their clients to stick around, more and more businesses are making efforts to implement loyalty programs, which may support them in making informed decisions. It is of paramount importance to identify the customer segments most responsive to marketing campaigns and adopt effective strategies for attracting more subscriptions to term deposits. This study develops statistical learning models, including both parametric and non-parametric to predict the success of a marketing campaign for a telecommunication company, as well as assist the company in making decisions.

For the company, there are several reasons why understanding which customer segments are most responsive to the marketing campaign is essential in optimizing the success of the campaign. First, these customer segments would spend more money on re-subscribe to a new term deposit, and less likely to switch to competitors. Therefore, the company may have a steadily income flow and less likely to be negatively influenced by economic downturns. Second, focusing on important customer segments may help the company attract new customers because loyal customers tend to recommend it to their relatives, friends, and colleagues. Finally, focusing on responsive segments will help minimize marketing cost, as well as maximize the return on investment. By building machine learning models, we can gain insights which can help guide the development of effective business strategies, contribute to allocate resources more efficiently and make data-informed decisions.


### **Project Objectives**
The main aims of this research are to predict customers’ likelihood of responding to marketing campaigns, and recommend some strategies for the telecommunication company to maximize campaign success as well as minimize costs.

Research questions: 
  1.	Which customer segments are most responsive to the company’s marketing campaign?
  2.	Can statistical learning models accurately predict the success of a marketing campaign?
  3.	How can the telecommunication company implement effective business strategies based on findings to maximize the marketing campaign success and overall business growth?

Main obejectives:
  1.	Pre-process the given dataset
  2.	Develop and evaluate parametric and non-parametric machine learning models
  3.	Extract insights to assist the company in making decisions


### **Dataset***
The [telemarketing campaign dataset](telecom_data.csv) contains a total of 22 variables. However, this project will take only 9 attributes into consideration.
- `age` is divided into 4 age groups, including Teen, Early Adulthood, Early Middle Age, and Late Middle Age.
- `duration` is divided into 4 groups: under 200s, 200-500s, 500-1000, and over 1000s.
The table below shows the attributes used for this project:


| Attributes  | Types        | Description                                 | Categories                                         |
|-------------|--------------|---------------------------------------------|--------------------------------------------------|
| Age group   | Categorical  | Age group of clients                       | Teen: 17 – 21, Early Adulthood: 22-34, Early Middle Age: 35-44, Late Middle Age: 45-69 |
| Marital     | Categorical  | Marital status                             | Married/Single/Divorced                          |
| Default     | Categorical  | Has credit in default?                     | Yes/No                                           |
| Housing     | Categorical  | Has a housing loan?                        | Yes/No                                           |
| Loan        | Categorical  | Has a personal loan?                       | Yes/No                                           |
| Contact     | Categorical  | Contact communication type                 | Cellular/Telephone                               |
| Duration    | Categorical  | Last contact duration                      | Under 200s, 200-500s, 500-1000s, Over 1000s     |
| Previous    | Numeric      | Number of contacts performed before this campaign | 0-7 contacts                               |
| Poutcome    | Categorical  | Outcome of the previous marketing campaign | Yes/No                                           |
| y           | Categorical  | Has the client subscribed a term deposit?  | Yes/No                                           |

### **Usage**

### **Models used**
- Logistic Regression
- Naïve Bayes
- KNN
- Support Vector Machince

### **Features**
- Conduct hyperparameter optimization by employing GridSearchCV to optimize the performance of Logistics Regression.
- Apply Cross Validation to help reduce overfitting and maximize data utilization.
- Confusion Matrix


### **Results**
1. Which customer segments are most responsive to the company’s marketing campaign?
Customers with **successful previous campaign outcome** and customers with **500-1000s last contact duration** are two customer segments which are more likely to respond positively to the telecommunication campaign. Customers in the 45-69 age group are also highly responsive. 

3. Can statistical learning models accurately predict the success of a marketing campaign?

| Models                        | Accuracy Score | Average Accuracy (Cross-Validation) |
|-------------------------------|----------------|--------------------------------------|
| Logistic Regression           | 0.90508        |  0.90621                              |
| Naïve Bayes                   | 0.85464        | -                                   |
| K-Nearest Neighbors (KNN)     | 0.90188        | -                                   |
| Support Vector Machine (SVC)  | 0.91           | -                            |



### Model Prediction Results

|                                 | **Meaning**                                                                 | **Logistic Regression** | **SVC** |
|-------------------------------------------|-------------------------------------------------------------------------------|--------------------------|---------|
| **True Positives**                         | Customers correctly predicted as potential customers and subscribed to the term deposit. | 10144                    | 10157   |
| **True Negatives**                         | Customers correctly predicted as NOT potential customers and did not subscribe to the term deposit. | 322                      | 270     |
| **False Positives**                        | Customers incorrectly predicted as potential subscribers, but they did not subscribe. | 163                      | 150     |
| **False Negatives**                        | Customers incorrectly predicted as NOT potential customers, but they did subscribe. | 867                      | 919     |
| **Total Correct Predictions**             |                                                                               | **10466**               | **10427** |
| **Total Incorrect Predictions**           |                                                                               | **1030**                | **1069**  |


5. How can the telecommunication company implement effective business strategies based on findings to maximize the marketing campaign success and overall business growth?












