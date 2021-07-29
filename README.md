# AI_Case_Studies

<h1>Santander Customer Satisfaction - Kaggle Competition</h1>
<h2> Problem Overview </h2>
From frontline support teams to C-suites, customer satisfaction is a key measure of success. Unhappy customers don't stick around. What's more, unhappy customers rarely voice their dissatisfaction before leaving.

Santander Bank is asking Kagglers to help them identify dissatisfied customers early in their relationship. Doing so would allow Santander to take proactive steps to improve a customer's happiness before it's too late.

In this problem, the task is to work with hundreds of anonymized features provided in the dataser to predict if a customer is satisfied or dissatisfied with their banking experience.

<h2> Avaibale Data </h2>
Anonymized dataset containing a large number of numeric variables. The "TARGET" column is the variable to predict. It equals 1 for unsatisfied customers and 0 for satisfied customers.

<h2> Task </h2>
The competition task is to predict the probability that each customer in the test set is an unsatisfied customer.

<h2> Implementation Approach </h2>
1. I had started the code by importing the required libraries of Python3 to implement their functions.
<br>
2. Then reading the given datasets of the provided problem.
<br>
3. While reading the dataset, I took the 'ID' column as an index column so that the operations don't reflect on that and I can directly use it in the submission time.
<br>
4. Now preprocessing and data visualization methods are used to deal with the data.
<br>
5. After visualization, I founded many imbalanced data. To remove Imbalancing, I tried SMOTE with logistic Regression but founds it worthless as compared to simple Logistic      Regression algorithm. So, I continued without balancing the data.
<br>
6. Then after splitting and Normalization, I applied Model Building.
<br>
7. In Model Building, I tried many algorithms but here I put only two best approaches which I got,
<br>
   a. Logistic Regression: To train the model I have used a logistic regression algorithm with SMOTE as well as without SMOTE.
<br>
   b. XGBoost: In XGBoost I tried balancing the data as well as without balancing the data and the best one from both put here.
<br>
8. For each ID in the test set, The predicted probability for the TARGET variable gives the score of 0.79560 for Logistic Regression and 0.67370 for Gaussian Naive Bayes with    PCA which are comparatively better than all others.

<h1> Result with different Models </h1>
Here I am putting all the Model scores which I tried according to my observations:
<br>
1. Logistic Regression : 0.79560
<br>
2. Logistic Regression with PCA : 0.79255
<br>
3. Logistic Regression with SMOTE : 0.72225
<br>
4. Gaussian Naive Bayes with PCA : 0.67370
<br>
5. XGBoost with SMOTE : 0.66979
<br>
6. Gaussian Naive Bayes : 0.52078
<br>
7. Random Forest Classifier : 0.51457
<br>
8. Decision Tree Classifier : 0.50306
