# Logistic_Regression_Wed_Wine
Logistic Regression to Predict Wine Quality
Logistic Regression is supervised machine learning method used to classify or predict class labels (category) based on a one or more attributes.  In this exercise, we set up a logistic regression model to observe how well eleven attributes of wine can predict whether the quality is above average or not (average or below).  The prediction in logistic regression is based likelihood of being one class label or another.  The prediction comes from training the model with part of the dataset, then testing the model on the test part of the dataset. 

In this Python exercise, we focus on the impact the C parameter has on the performance of the model.  The C parameter is a function used to protect against model overfitting.  If you have a high value of C, the model prioritizes classifying each individual in the training set but has a high chance of overfitting the data, thus resulting in lower accuracy on the test data.  If the value of C is low, the model creates a more restricted boundery, prioritizing the majority of data, thus decreasing the chance of overfitting the data. 

The file has 4,898 records and 12 columns.  The 11 predictor variables are fixed_acidity, citric_acid, residual_sugar, chlorides, free_sulfur_dioxide, total_sulfur_dioxide, density, ph, sulphates, and alchohol.  These are all continuous variables with no missing values.  The target variable is quality with values ranging from 3 to 9 (7 classes).  Logistic Regression can only be used to predict one of two classes.  The One vs All is an alternative method, however, in this exercise the 7 classes will be binarized to two classes: at or below 6 and above 6.  

Logistic Regression performs better when the attributes are of equal scale, therefore the predictor variable are standardized with each having a mean of zero, making all on equal scale.  

The first model has the C parameter high at 10.  The prediction accuracy on the test data = 26% (very low)
The second model has the C parameter lowered to 1.0.  The prediction accuracy on the test data increased to 40% (still not good)
The third model has the C parameter lowered to 0.01.  The prediction accuracy on the test data increased to 66% (much better but still not good, espectially with only two categories)
