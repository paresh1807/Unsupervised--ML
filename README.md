# Unsupervised--ML
**Online Retail Customer Segmentation**

**Problem Statement:** In this project, our task is to identify major customer segments on a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

**Project Summary:** we have given a transactional dataset which contains all the transactions occurring between 01/12/2010 and 09/12/2011 having 541909 data records and 8 features.Our task is to identify major customer segments on the basis of this transaction dataset which will have a positive impact on business.

Key steps taken and approach towards our problem:

1.**Data Gathering and Cleaning:** We started by gathering the dataset, which contains 541909 records and 8 attributes. We performed data cleaning, handling null values, checking data distribution, and handling outliers to ensure data quality.

2.**Exploratory Data Analysis(EDA):** In this phase, we conducted an in-depth analysis of the dataset. We employed various visualization techniques, separating them into univariate, bivariate categories. Through EDA, we gained meaningful insights that guided our decision-making for the subsequent steps.

3.**Feature Engineering and Data Preprocessing:**  We performed feature engineering to extract new features like Recency, Frequency and Monetary from the given features.we have clubbed these new features with customerID to form a new dataframe so that it will reduce the data dimensionality and also got RFM score with the help of recency, frequency and monetary values by virtue of which we can segment the customers or we can do clustering on the basis of these features and scores.

4.**Data Transformation:** To achieve normally distributed data, we applied Logarithmic transformations. Additionally, we employed the StandardScaler from the sklearn library to scale the data.

5.**Clustering:**  As the data is normalised now, we have performed K-Means clustering and with the help of clustering analysis,silhouette score and elbow curve we have came up with the optimal number of cluster as 4. I have then clubbed the optimal cluster label to recency, frequency and monetary dataframe for cluster based modelling.

6.**Model Implementation:** We split the data into train and test sets, and evaluated several classification models, including Logistic Regression, Random Forest, XGBoost. Various metrics such as Precision, Recall, F1 Score, Accuracy, and AUC-ROC score were compared using classification reports and confusion matrices.After thorough experimentation, XGBoost(untuned) emerged as the optimal model, achieving the highest metrics overall.

**conclusion:**

**Clustering Based Modelling:**

1. I have clubbed the optimal cluster label to Recency, Frequency and Monetary dataframe for applying classification models.
2. I have implemented a total of three classification machine learning models in our analysis, which are Logistic Regression, Random Forest, XGBoost.
3. Accuracy and AUC_ROC Score has been chosen as the model evaluation metric according to our target problem.
4. According to our analysis, Monetary is the most contributing feature followed by frequency and recency,towards making predictions for our selected model.
5. After evaluating various metrics such as recall, precision, F1 score, accuracy, and AUC-ROC Score, XGBoost(untuned) has been considered as our final optimal model since it achieved the highest scores for all these metrics having accuracy of 97% and AUC_ROC Score of 99.99%.
6. During our analysis, no overfitting was observed in any of the models. This indicates that the models were able to generalize well to new, unseen data, and were not solely relying on the training data to make accurate predictions. This is an important aspect of model evaluation, as overfitting can lead to poor performance on new data and limit the model's ability to be useful in real-world scenarios.

