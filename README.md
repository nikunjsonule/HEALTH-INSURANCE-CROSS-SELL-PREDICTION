
# Project Title

Health-Insurance-Cross- Sell-Prediction

# Problem Description

An insurance policy is an arrangement by which a company 
undertakes to provide a guarantee of compensation for 
specified loss, damage, illness, or death in return for 
the payment of a specified premium. A premium is a sum of
 money that the customer needs to pay regularly to an 
 insurance company for this guarantee. We were provided with
 'Health Insurance Cross Sell Prediction’ dataset to 
 perform machine learning task, were to get insights from
  the independent and dependent variable of a dataset. 
  Having all record and data with different Age, Driving 
  License, Region Code, Previously Insured, Vehicle Age,
   Vehicle Damage, Annual Premium, Policy Sales Channel, 
   Vintage, Response (Target variable – 1 and 0). 
   Providing specific data analysis and prediction to 
   done with this data.

# Data Description

The dataset has shape (381109,12) which include - id, Gender,
Age, Driving License, Region Code, Previously_Insured, 
Vehicle Age, Vehicle_Damage, PolicySalesChannel, Vintage,
Response (i.e dependent variable) information.

# Attribute information



* id : Unique ID for the customer

* Gender : Gender of the customer

* Age : Age of the customer

* Driving_License 0 : Customer does not have DL, 1 : Customer already has DL

* Region_Code : Unique code for the region of the customer

* Previously_Insured : 1 : Customer already has Vehicle Insurance, 0 : Customer doesn't have Vehicle Insurance

* Vehicle_Age : Age of the Vehicle

* Vehicle_Damage :1 : Customer got his/her vehicle damaged in the past. 0 : Customer didn't get his/her vehicle damaged in the past.

* Annual_Premium : The amount customer needs to pay as premium in the year

* PolicySalesChannel : Anonymized Code for the channel of outreaching to the customer ie. Different Agents, Over Mail, Over Phone, In Person, etc.

* Vintage : Number of Days, Customer has been associated with the company

* Response : 1 : Customer is interested, 0 : Customer is not interested



# Summary of Project

An insurance policy is an arrangement by which a company 
undertakes to provide a guarantee of compensation for 
specified loss, damage, illness, or death in return for
 the payment of a specified premium. A premium is a sum
  of money that the customer needs to pay regularly to an
   insurance company for this guarantee. We were provided
 with ‘Health Insurance Cross Sell Prediction’ dataset to
  perform machine learning task, were to get insights from 
  the independent and dependent variable of a dataset.
   We’ve all record and data with different Age, Driving
License, Region Code, Previously Insured, Vehicle Age,
 Vehicle Damage, Annual Premium, Policy Sales Channel,
  Vintage, Response (Target variable – 1 and 0). Providing
   specific data analysis and prediction to done with this 
   data.

As the first step, I performed data preprocessing and 
EDA part. The Age, Region Code and Policy Sales Channel 
column was an important feature to gets smaller insights
 from its. Extracting YoungAge, MiddleAge and OldAge from
  Age to create a new feature in dataset. Similarly, 
  getting Region A, Region B and Region C from Region Code.
   For Policy Sales Channel I’ve got Channel A, Channel B, 
   Channel C and Channel D. The extraction has made very
easy to get useful insights.
In EDA plotting heatmap for correlation, univariate and 
bivariate analysis, graphs and other plots to get some 
insights from the data.

After data preprocessing, our data was ready to fit into 
the models. Different model used to get optimal roc_auc score,
 precision, recall, f1 score and test accuracy score, models
  are – Logistic Regression, XGBoost Classifier model.

The third step is to do some hyperparamter tuning. Doing
 GridSearchCV on Logistic Regression and XGBoost Classifier
  part to get best roc_auc score and to shrink the coefficient 
and get optimal model. As per roc_auc score we find Logistic 
Regression as optimal model.

As to get more about TPR and FPR point view, the threshold 
was main important to know. The ROC curve and Confusion 
matrix has helped a lot to understand how those curve differ.
 The Confusion matrix is better to know a score for precision, recall, test accuracy and f1 score. The desired score has satisfy the confusion matrix. TPR and TNR is higher which is a good thing in imbalance dataset.

The final section is to observe model evaluation metrics.
 Logistic regression shows roc_auc score with 98%, test 
 accuracy score with 93.71%, precision with 63%, recall 93%
  and f1 score with 75%. As for XGBoost Classifier we got 
  roc_auc score with 90.33%, test accuracy with 84.32%, 
  precision with 72%, recall and f1 score with 95% and 82%
   respectively.

So roc_auc score of the best model is 98% for this dataset.
 This performance could be due to various reasons: no proper
  pattern of data, it may be some negligible noise in the 
  data, different model give different accuracy score.

# Machine Learning (Classification) Data Pipeline

1.	Data Preprocessing

2.	Exploratory Data Analysis

•	Univariate Analysis on numeric and categorical features

•	Bivariate Analysis on numeric and categorical features

•	Analysis from categorical variables
                                
3. Fitting different models
                
•	Logistic Regression

•	XGBoost Classifier

4. Hyper parameter Tuning with GridSearchCV in Logistic Regression and XGBoost
   Model

5. Model Evaluation Metrics

•	Roc_auc score

•	Precision

•	recall

•	F1 score

•	Test accuracy

6.  Getting detail insights from ROC curve and Confusion Matrix


# Conclusion

* Male category is slightly greater than that of female and chances of getting the insurance is also little high for male.
* People aged between 28-65 are more likely to be interested but overall their are people were Age matters they deserve the insurance.
* Customers are having Driving License more those who are not interseted in insurance as compared to customers who are intrested in Insurance are less.
* Customer who are not previously insured are likely to be interested in Insurance.
* Customers with vechicle age 1-2 years are more likely to interested as compared to the others. Customers with Vehicle_Age >2 years have very less chance of getting insurance but Vehicle_Age < 1 year is also less likely to get insurance.
* Annual Premium very less people pay for 500k and above.
* Region_C in Region Code has the highest chances of not taking insurance but in Region_A most of them prefer as compared to other who wants Insurance.
* Channel_A Customers has the highest chances of not taking the insurance but Channel_C customers wants to claim Insurance as compared to others.
* We can say that the no. of male customers in our data set is higher than female customers. Most of the Male customers are likely to take Insurance.
* Customers with Vehicle Damage are likely to buy insurance.
* The variable such as Age, Previously_Insured,Annual_Premium are more affecting the 'Response' feature.
* Comparing ROC curve we can see that Logistic Regression model preforming better as compared to XGBoost Classifier . Because curves closer to the top-left corner, it indicate a better performance.


