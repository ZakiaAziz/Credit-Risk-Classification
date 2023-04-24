                                    # Module 12 Report 

                                ## Overview of the Analysis




The challenge provides us a lending dataset where there are approximately 80,000 data for loan accounts. The dataset is consists of the following information: loan size, interest rate, income of the borrowers, debt to income ratio, total number of accounts per borrower, degratory marks, total debt and loan status. Based on the data provided, a lending company asked to create a model which will evaluate the creditworthiness of borrowers.

The main parts of the challenge are:
 1. Splitting the Data into Training and Test sets
 2. Creating a logistic Regression Model with the original Data
 3. Predicting a Logistic Regression Model with Resmapled Training Data
 

 
 ## Preparing The Data
 
Firstly, the CSV file was read into a DataFrame. The "loan_status" column is labelled as y and rest of the DataFrame was labelled as X. Value Count method was used to check the balance of the target values where 0 represents healthy loan and 1 represents high risk loan. The total number of borrowers are 77536 and among them 75036 have healthy loan status which means the borrowers are expected tp pay loan amount on time, 2500 borrowers fall on high risk of defaulting.
 Finally, train_test_split was used from sklearn to divide the dataset into train set and testing set.
 
## Results

Logistic Regression Model is used in two different sets of Data. The first Model uses the original Dataset and in the second model Dataset is fitted to the RandomOverSampler to create equal number of datapoints. 

Logistic Regression is used to predict binary outcomes from data. In case of predicting the loan is healthy or risky logistic Regression is used. In Model 1, the original dataset predicted the loan status and the process consists of accuracy score, confusion matrix and classification report.

Only accuracy rate is not sufficient to decide if a model is viable or not. Therefore, confusion matrix provide us the information about false positive, false negatives that we need to consider in a prediction. Finally, a classification report is used to measure precision and recall which can be used to eliminate false positives and false negatives. 

In a binary decision problem two possible correct answers are True Positive and True Negative. Accuracy is how often the model is correct-the ratio of correctly predicted observations to the total number of observations. In case of loan risks, accuracy rate may get impacted by the high amount of good loans. Therefore, a metric is needed that can help to evaluate each class prediction. Precision helps to identify the ration of correctly predicted positive observations to the total predicted positive observations. Recall is calculated to identify the ration of correctly predicted positive observations to all predicted observations for that class.  


* Machine Learning Model 1:
  * For Model 1, original data has been used for training and testing. Here, the accuracy is high which is 0.9924. However, precision and recall is calculated to verify the result. Precision is 1 for healthy loan which confirms low false rate. The recall is also 1 which implies comprehensive output and a low false negative rate. 
  
  As a result, the prediction seems almost accurate. 
  



* Machine Learning Model 2:

The second model uses random oversampling approach. Imbalanced Learn Library was imported to apply RandomOversampler to fit_resample the training datset. Here, the accuracy is high which is 0.9952. However, precision and recall is calculated to verify the result. Precision is 1 for healthy loan which confirms low false rate. The recall is also 1 which implies comprehensive output and a low false negative rate. 
  
  The accuracy rate is slightly higher and precision and recall are same. Hence, The prediction of loan/ creditworthyness seems accurate.

## Summary

As a result, I suggest the model works fine to evaluate creditworthyness of borrowers. Both models performing well. In this case, identyfing the risky loan is important because the high accuracy rate can be impacted by too many healthy loans. However, the precision and recall confirms the accuracy rate is right. 



