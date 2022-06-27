# Predicting-Customer-Defaults---Supervised-Learning
In this project, UCI Credit Default dataset is analyzed using statistical and visualization techniques to understand the relationship between variables and their relationship to the defualt outcome. The data is not balanced where only 22% of individuals defaulted. The variables analyzed consists of individuals balance amount in dollars, sex, education level, marriage status, age, and their payment status. Continuous variables are normalized and fed into the data.

After EDA, features are selected based on their correlation with the target variable and based on their relationship to the target variable analyzed during EDA.

Supervised learning algorithms, including logistic regression, random forest, and KNN algorithms are implemented to train the model to predict the defaul outcome of future customers. 

The data is scaled due to use of KNN (its senstiive to eucledian distance) and GridSearchCV is used to tune hyperparameters. Each model is trained using the best hyperparameters and compared using accuracy, precision, recall, and f1 score. 

Comparing the accuracy  and the data gathered from confusion matrix, Random Forest model is a little better to predict the outcome value. However, using Logistci Regression model will be much beneficial due to its processing time and performance, which is not that different than the performance of random forest.


Recommendations:

This model will correctly predict more than 80% of the population. Even though this is good, it does not predict 100% and banks will sometimes will loan an individual who will likely default. I believe including more features that would be more correlated with the target variable needs to be included in the data. Features can be credit score, individuals salary, and their total dept. 

Also, other models as Naive Bayes and Neural Networks could have been used and more effort to create better correlated features should've been given.  
