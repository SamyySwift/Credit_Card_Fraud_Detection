# Credit_Card_Fraud_Detection

![](/images/fraud_detection.png)

## **Project Overview**
In this project, I useed a credit card fraud detection dataset, and build a binary classification model that can identify transactions as either fraudulent or valid, based on provided, historical data.
The payment fraud data set (Dal Pozzolo et al. 2015) was downloaded from Kaggle. This has features and labels for thousands of credit card transactions, each of which is labeled as fraudulent or valid. In this notebook, we'd like to train a model based on the features of these transactions so that we can predict risky or fraudulent transactions in the future.

## **EDA**
* The dataset I used to train the model was downloaded using this [link](https://s3.amazonaws.com/video.udacity-data.com/topher/2019/January/5c534768_creditcardfraud/creditcardfraud.zip).
* I loaded and explored the dataset.
* Dataset was split into training and testing set.

## **Modelling**
* In this notebook, I defined and train the SageMaker, built-in algorithm, [LinearLearner](https://sagemaker.readthedocs.io/en/stable/linear_learner.html).
Since we are predicting a credit card transaction as either valid or frudulent, the problem requires a binary classification algorithm, in which a line is separating two classes of data and effectively outputs labels; either 1 for data that falls above the line or 0 for points that fall on or below the line.
                                        ![](/images/linear_seperator.png)
* I instantiated a LinearLearner Estimator passing it important arguments.
* Finally, I converted the data into Record_set format and fitted it to the estimator.
