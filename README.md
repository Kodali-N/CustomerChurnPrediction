# Customer Churn Prediction
- In this project, I've used [Telecom customer churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) to predict the probability with which each customer could churn. The final probability of churning is predicted after testing various ML models such as: Logistic Regression Model, Support Vector Machine, k_Nearest Neighbour Model, Decision Tree and Random Forest models. Out of all the models, it is observed that Logistic Regression Model gave the highest accuracy. So, the probability was predicted using the same.
- The EDA is carried out using pandas-profiling. This was used to get a fast solution in one line.
- Below are some examples to show what the profiling report consists of
<img src="https://user-images.githubusercontent.com/86663030/212525106-6a051d20-12f6-42ea-898d-71d5dbe2d35f.jpeg" width="500" height="350">
<img src="https://user-images.githubusercontent.com/86663030/212525014-19634d18-7853-4578-b360-309b20d2a63f.jpeg" width="450" height="250">
<img src="https://user-images.githubusercontent.com/86663030/212525016-98a5221e-28cb-49f7-b665-0082c0bee498.jpeg" width="450" height="250">

- Converted churn to a binary numeric variables, and removed all null values (only 0.15% of the total data)
- Plotted various predictors against churn, such as gender, tech support, internet services, and etc,.
<img src="https://user-images.githubusercontent.com/86663030/212525305-be7c6d9f-a3b0-4510-9aa9-e4fc29599d03.jpeg" width="450" height="300"> Percent of people who churned = 26.6%
- <img src="https://user-images.githubusercontent.com/86663030/212525316-516ff5d5-8ee2-49db-a7b2-83cc4ee4ea0a.jpeg" width="550" height="300"> Customers with no tech support are more likely to churn
- <img src="https://user-images.githubusercontent.com/86663030/212525323-dbb9b6dc-98c1-4684-8f5f-637ba0f69565.jpeg" width="550" height="300"> Customer on monthly contracts churn more
- <img src="https://user-images.githubusercontent.com/86663030/212525329-1697f42e-2396-4064-b461-cbbb81d009cd.jpeg" width="550" height="300"> As the customer's tenure increases, he/she is less likely to churn
- Used One Hot Encoding on categorical variables, so that the information can be fed into ML algorithms. 
- In order to get the right results, we are required to bring, 'tenure', 'Monthly Charges' and 'Total Charges' onto the same scale. I used StandardScaler from sklearn.preprocessing for this task.
<img src="https://user-images.githubusercontent.com/86663030/212525335-13758ff7-3fc5-46cd-aabf-69c49cdb7cbf.jpeg" width="550" height="300">
- Create feature variable X and target variable y. Further split the data into training dataset(70%) and testing dataset(30%). The training dataset is used for training the model, where as the testing dataset is used to validate the model.
- I trained a logistic regression model. Fit the model into the training dataset using fit. The model will find correlation between X_train and y_train. By establishing these correlations, the model will be able to predict the churn probability. Then we predict the result for the test observations. Accuracy is calculated by passing y_test and the predicted values. 
<img src="https://user-images.githubusercontent.com/86663030/212525340-25fa485b-e940-4cea-bce1-9602ddca36e3.jpeg" width="700" height="300">
- The following models: Support Vector Machine, K-Nearest Neighbour, Decision Tree and Random Forest models are also trained the same way.
- To find out the model that works the best for us, I calculated the accuracy score. From the data, its observed that Logistic Regression Model has the highest accuracy score.
<img src="https://user-images.githubusercontent.com/86663030/212526072-6344f913-d223-4da5-aff9-3fb255d4a097.jpeg" width="300" height="200">
- I further went onto creating a confusion matrix for the model evaluation by passing y_test and predicted values. We have (1395+317) 1712 correct predictions and (233+165) 398 false predictions.
<img src="https://user-images.githubusercontent.com/86663030/212525343-bfa1fe70-ff8b-4d44-bde9-f9a3d61a9ac0.jpeg" width="550" height="200">
- Result:
<img src="https://user-images.githubusercontent.com/86663030/212525344-5eb5f699-de55-45b7-8412-a845402ee79c.jpeg" width="300" height="200">

