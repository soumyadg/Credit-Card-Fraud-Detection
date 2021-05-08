# Credit-Card-Fraud-Detection

# Machine Learning project to detect credit card fraud.

CONTEXT: Credit Card Fraud is one of the biggest problems plaguing payment technology. When this type of fraud is discussed in mainstream media, customers and vendors, and their loss of money is usually discussed, however an important player is often ignored, the financial institution. In 2018, 10% of the total data-breaches all over the world involved financial companies including banks and credit unions. It is estimated that the cost of fraud adds up to billions of dollars per annum. With the increased dependency on the internet and e-commerce transactions, the number of fraud cases have increased significantly is expected to rise exponentially every year. Analysts predict that online credit card fraud is expected to increase to $32 billion in 2021. The pressing problem with credit card fraud is that financial institutions need to identify fraudulent transactions, and at the same time allow legitimate transactions to be processed correctly. 
Due to the sheer volume of transactions that take place daily, it is impossible to detect such activities only through human intervention and therefore AI and Machine Learning techniques is being used by banks to categorize such transactions based on multiple factors (features). While it’s impossible to identify all of such cases, machine learning is helping the financial institutions to identify out such transactions to a certain level of reliability. Modern fraud analysts use historical payment data, customer profiles and payment information for predicting such frauds. These methodologies have had quite a lot of success in differentiating fraudulent transactions from legitimate ones. In machine learning, fraud detection can be framed as a classification problem. In a classification problem we predict a discrete class label output given a data observation. In the case of fraud detection observations are classified as “fraud” or “non-fraud” based on the features in those observations. A big issue with using a classifier to solve this problem is with class imbalance. For example, if you had a data set where you were trying to detect a disease, and there were 2 positive cases out of 1000, even if the algorithm were to always predict it to be positive, it would still be correct 99.8% of the time. According to a Nilson Report, 1.01 billion credit card transactions take place per day. Out of this only a small portion of the transactions would actually be fraudulent. The problem this causes is that metrics used to assess the ML algorithm such as accuracy breaks down.

DATASET: The Dataset is obtained from KAGGLE. The dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions. Most of the features of this dataset has been anonymized for the sake of privacy and they have been represented with strings V1-V28. It can be seen from the dataset that this is a classification problem, and we would like to detect the fraud and non-fraud transactions, while reducing the misclassifications to an extent that the model can be relied on.

METHODOLOGY: The methodology of the entire process has been mentioned below:

  1. Data Cleaning: The first step of any machine learning exercise is data processing. Data Cleaning is a process of preparing the data for analysis or manipulating the data that is incomplete, irrelevant or incorrectly formatted. Regardless of any type of visualizations, data cleaning is a very important step that gives a clear idea of the dataset. For this dataset, a new feature 'Size' was created to separate the class of Fraud and Not-Fraud transactions. Another important feature that was added was 'Hour'. 'Hour' feature lets us know the hour of the day when the transaction had taken place.

  2. EDA: Next step is EDA (Exploratory Data Analysis). EDA is a critical procedure of performing initial investigations on data to identify patterns, spot trends, to test hypothesis and to check assumptions using graphical representations and summary statistics. To gather as much of insights from the data first and to visualize it with the help of graphs and plots is always a good idea before delving further into machine learning.
EDA steps performed in the exercise are as follows: 
                                      1. Plotting fraud vs non-fraud transactions 
                                      2. Grouping and plotting the count of transactions based on hour
                                      3. Grouping the transactions by 'fraud' or 'not-fraud' category and plotting the counts of transactions based on the hour.
                                      4. Scatter plot all the transactions with more weight to the 'fraud' transactions for better perspective.
                                      5. Plotting the distribution of fraud and not-fraud transaction amount.

  3. Modeling: After the data cleaning and EDA, we are now ready for machine learning. Judging from the data, we can see that this is clearly a classification problem where we have to develop a model which would seamlessly categorize fraud and not-fraud transactions. We have used multiple models for building and for prediction purposes and we have used them to compare which model have suited this dataset best. Different models used are as follows:
                                      1. 2 feature logistic regression 
                                      2. All feature logistic regression
                                      3. Support Vector Classifier
                                      4. Decision Tree
                                      5. Random Forest
                                      6. Ada-Boost Classifier
                                      7. Neural Networks
                              
All the machine learning models that has been used have been followed by their individual evaluation metrics that lets us realize how well the model has performed.

  4. Evaluation : While accuracy is a measure for most of the machine learning models, accuracy will not be valid measure for this dataset as it’s an unbalanced dataset. Accuracy would always be high because it’s the ratio of the sum of True positives and true negatives over the sum of all data points. The most important metric that we have to focus on while working with unbalanced dataset is Precision and Recall. 
Precision basically tells us that out of the results classified as positive by our model, how many were actually positive.
Recall tells us how many true positives (points labelled as positive) were recalled or found by our model.
While we have two classes in the analysis, Fraud (0) and Non-Fraud (1) transactions, we have to check the precision and recall for both the classes. We would look into the confusion matrix as well, a confusion matrix is a 2x2 matrix that lets us determine the numbers of true positives, true negatives, false positives and false negatives. Finally, we would also check the AUC-ROC curve for each classifier model. AUC - ROC curve is a performance measurement for the classification problems at various threshold settings. ROC is a probability curve and AUC represent the degree or measure of separability. It tells how much the model is capable of distinguishing between classes. Higher the AUC, the better the model is at predicting 0s as 0s and 1s as 1s. By analogy, the Higher the AUC, the better the model is at distinguishing between transactions which are fraud, and which are not. For the tree-based models, the feature importance plot has also been elucidated as well. Tree based models come with a feature importance attribute that outputs an array containing a value for each feature representing how important each feature of the data has been in trying to predict the model.

![](/Images/feature.png)




CONCLUSION AND FUTURE WORK: From the analysis, it can be seen that several machine learning models have been attempted to categorize fraud and not-fraud transactions. Out of all the methods used, Random forest and Decision Trees performed the best with a AUC-ROC score of 0.89. Even with same score, I have decided to use Random Forest for the final model as Decision Trees have a tendency to overfit the data. While there are other modeling techniques which could have been used, they have been kept for future work. To address the issue of class imbalance, SMOTE (synthetic minority oversampling technique) could also be used which has also been left for future work. 

