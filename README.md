# Analysing_Time_Spent_on_Social_Platform
In this project, we aim to analyze the average time spent by users on social media platforms. By studying this metric, we can gain a deeper understanding of user behavior and preferences, which can help social media companies enhance their user experience and tailor their content to better meet user needs. 

Through this analysis, we seek to answer questions such as:

What is the average time spent by users on social media platforms?
How does the average time spent vary across different demographics (age, gender, location)?

Social media platforms have become an integral part of our daily lives, offering a wide range of services from connecting with friends and family to consuming news and entertainment. One key metric that social media companies often track is the average time spent by users on their platforms. Understanding this metric can provide valuable insights into user engagement and platform usage patterns.

# Input Features:
 #   Column        Non-Null Count  Dtype 
---  ------        --------------  ----- 
 0   age           1000 non-null   int64 
 1   gender        1000 non-null   object
 2   time_spent    1000 non-null   int64 
 3   platform      1000 non-null   object
 4   interests     1000 non-null   object
 5   location      1000 non-null   object
 6   demographics  1000 non-null   object
 7   profession    1000 non-null   object
 8   income        1000 non-null   int64 
 9   indebt        1000 non-null   bool  
 10  isHomeOwner   1000 non-null   bool  
 11  Owns_Car      1000 non-null   bool  
 
 # Target Feature
    time_spent
    
## Analysis Note:
### Overview
- In this analysis, I have evaluated three machine learning models<br/>
    —Random Forest, Logistic Regression, and Support Vector Machine (SVM)—for a classification task. 
- Correlation between input features is very low
- Employed GridSearchCV to find the best Hyper Parameters
### Feature Engineering
- Target feature is binned into 3 bins, to increase prediction accuracy
       7 to 9 hours time spender as 3 
       4 to 6 hours time spender as 2
       1 to 3 hours time spender as 1
  - Similarly age feature also categories into 6 bins
      bins = [0,20,30,40,50,60,70]
      labels = [1,2,3,4,5,6]
### Results
Random Forest: Achieved an accuracy of 42.5%<br/>
Logistic Regression: Achieved an accuracy of 40.5%<br/>
Support Vector Machine (SVM): Achieved an accuracy of 35%<br/>
### Interpretation
- The Random Forest model outperformed both Logistic Regression and SVM in terms of accuracy.
- While Random Forest achieved the highest accuracy, it is important to note that the overall accuracy of all models is relatively low, indicating that the models may not be capturing the underlying patterns in the data effectively.
- Further analysis is required to understand why the models are not performing well and to explore additional feature engineering, model tuning, or alternative algorithms to improve performance.
