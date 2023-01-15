# Customer Churn Prediction
- In this project, I've used [Telecom customer churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) to predict the probability with which each customer could churn. The final probability of churning is predicted after testing various ML models such as: Logistic Regression Model, Support Vector Machine, k_Nearest Neighbour Model, Decision Tree and Rnadom Forest models. Out of all the models, it is observed that Logistic Regression Model gave the highest accuracy. So, the porbability was predicted using the same.
- The EDA is carried out using pandas-profiling. This was used to get a fast solution in one line.
- Below are some examples to show what the profiling report consists of

- Converted churn to a binary numeric variables, and removed all null values (only 0.15% fo the total data)
- PLotted various predictors against churn, such as gender, tech support, internet services, and etc,.
- Used One Hot ENcoding on categorical variables, so that the information can be fed into ML algorithms. 
- In irder to get the right results, we are required to bring, 'tenure', 'Monthly Charges' and 'Total Charges' onto the same scale. I used StandardScaler from sklearn.preprocessing for this task.
- Create feature variable X and target variable y. Further split the data into training dataset(70%) and testing dataset(30%). The training dataset is used for training the model, where as the testing dataset is used to validate the model.
- I trained a logistic regression model. Firt the model into the training dataset using fit. The model will find correlation between X_train and y_train. By establishing these correlations, the model will be able to predict the churn probability. Then we predict the result for the test observations. Accuracy is calculated by passing y_test and the predicted values. 
- The following models: Support Vector Machine, K-Nearest Neighbour, Decision Tree and Random Forest models are also trained the same way.
- To find out the model that works the best for us, I calculated the accuracy score. From the data, its observed that Logistic Regression Model has the highest accuracy score.
- I further went onto creating a confusion matrix for the model evaluation by passing y_test and predicted values. We have (1395+317) 1712 coorect predictions and (233+165) 398 false predictions.

