# Credit Risk Classification Analysis

## Purpose of analysis
What this analysis aims to do is to convey either the accuracy or inaccuracy of Logistic Regression models. Specifically the models accuracy when it comes to predicting whether a loan is healthy or high-risk.

## Information of the data
This data set contained around 78,000 rows of information and 8 columns. Our target for this data set was the loan_status column. This column tells us whether a loan is health or high risk. A 0 means a loan is health and a 1 means that the loan has a high risk of defaulting. of the 77,535 rows of data only around 2500 are labeled as high-risk, where as 75036 are considered to be healthy.
## Steps taken to train the model
There 3 stages to the machine learning process.

### Stage 1. Prep
The first thing we do after importing in our modules is read in the CSV file. After reading in the file we need to do is separate the labels and features. In this case we need to separate loan_status from the rest of the DataFrame. Since loan status is what we are trying to predict we are assigning that to the y variable, and the rest of the features to the X variable. 

    Next get the value counts for your y label. Though not necessary for the the machine learning code it is very helpful in understanding any over fitting that may happen.

The final part of the prep is the train_test_split. This will break your data up into 2 parts. part one will be used to train your model and a set to test your model on.

### Stage 2. Putting together the Model
In this instance we will be using the Logistic Regression Model. First thing we want to do is initiate the LogisticRegression and fir that to our training data.

After fitting the model we will then make a prediction using the test data.

### Stage 3. Evaluating the Models Performance
First we find the models balanced_accuracy_score which in the case the model was 97% accurate.

Next we generate a confusion matrix table to describe the performance of our classification model. 

Finally we generate a classification_report. This report will give us a comprehensive summary of how our classification model preformed. More specifically it will give us the: 

* precision: This is ratio of true positive prediction to the total number of positive prediction. Meaning how many of the positive prediction are actually positive.

* Recall: This is the ratio of true positive predictions to the total number of actual positive instances. Recall measures the models ability to capture all the positive instances.

* F1-Score: Grabs the harmonic mean of both precision and recall. It provides a balance between precision and recall.


            precision    recall  f1-score   support

        0       1.00      0.99      1.00     18765
        1       0.84      0.94      0.89       619

      accuracy                      0.99     19384
      macro avg  0.92     0.97      0.94     19384
      weighted avg 0.99   0.99      0.99     19384

    
