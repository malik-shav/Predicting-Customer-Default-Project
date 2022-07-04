### Objective
The objective of this task is to analyze the "UCI Credit Card" dataset to predict if the consumer will default on their next month payment.

Why predicting consumer defaults important?

-Total credit card debt in the US is more than 900 billion dollars where 1.57% are in delinquencies, meaning that 14 billion dollars are not paid on time.
    
-Predicting will lead banks to choose appropriate individuals to receive the loan and save money by reducing the number of loans given to individuals that are likely to default. 


### Data Description
Data consists of 30,000 samples and 23 variables, containing information on default payments, demographic factors, credit data, history of payment, and bill statements of credit card clients in Taiwan from April 2005 to September 2005.

UCI Credit Card dataset can be accessed from https://www.kaggle.com/uciml/default-of-credit-card-clients-dataset


### Methods Used 
The data is not balanced where default customers only account for ~22%. I will oversampling and undersampling techniques to balance the data during modeling phase. Data was checked for missing values but none were found, and outliers in continuous variables using boxplot. Using winsorization, outliers were modified.

Primarily, graphs were used to conduct univariate and bivariate analysis of the variables. Education, sex, marriage, age, pay variables correlate with defualt outcome. Furthermore, there is a correlation between amount billed to and payed by two classes, but not much correlation between classes for average amount billed.

Features were identified based on their correlation with the default variable and based on the analysis during EDA. However, primarily PCA was used to select best features that maintained 95% variance, where number of features is 15. PCA data is used for modeling after scaling using StandardScaler and splitting into X_train and X_test, labeled as original data. This data was oversampled and undersampled using SMOTE and RandomUnderSampling to balance the data. The balanced datas were also used in training the models to compare their performance to models trained using original data.


### Summary of the Models Used and Best Model
This is a classification task. Models trained include Logistic Regression, Random Forest Classifier, and KNN. GridSearchCV is used to find best parameters to utalize. Each model was trained using original, SMOTE and undersampled data, and compared using accuracy, recall, precision, AUC, and f1 scores.

KNN and Random Forest performed better than Logistic Regression and either can be used as the best models. However, if companies don't want computationally intensive model, Logistic Regression is better.


### Best Insight
The best predictor of an individual who would default is their history of monthly payments, as described with PAY_0 to PAY_6 variables. There are differences in classes within variables as education, sex, marriage, and age in terms of defaults. For example, university degree holders default more than high school diploma holders.


### Recommendation:
Other features like credit score, individuals salary, and their total dept can have high correlation with the default outcome. If these features can be collected, next steps would analyze and integrate them into our model. 
