# Problem Statement
The objective in this project is to build machine learning models to classify or identify fraudulent card transactions from a given card transactions data.
# Abstract
Credit Card Fraud is one of the biggest issues faced by the government and the amount of money involved in this is generally enormous. There are various challenges faced by service providers some of them are listed below.<br>
How can a credit card Fraud happen?<br>
Some of the most common ways it may happen are:<br>
•	Firstly and most ostensibly when your card details are overseen by some other person.<br>
•	When your card is lost or stolen and the person possessing it knows how to get things done.<br>
•	Fake phone call convincing you to share the details.<br>
•	And lastly and most improbably, a high-level hacking of the bank account details.<br>
Main challenges involved in credit card fraud detection are:<br>
•	Enormous Data is processed every day and the model build must be fast enough to respond to the scam in time.<br>
•	Imbalanced Data i.e most of the transactions(99.8%) are not fraudulent which makes it really hard for detecting the fraudulent ones<br>
•	Data availability as the data is mostly private.<br>
•	Misclassified Data can be another major issue, as not every fraudulent transaction is caught and reported.<br>
•	And last but not the least, Adaptive techniques used against the model by the scammers.<br>
How to tackle these challenges?<br>
•	The model used must be simple and fast enough to detect the anomaly and classify it as a fraudulent transaction as quickly as possible.<br>
•	Imbalance can be dealt with by properly using some methods which we will talk about in the next paragraph<br>
•	For protecting the privacy of the user the dimensionality of the data can be reduced.<br>
•	A more trustworthy source must be taken which double-check the data, at least for training the model.<br>
•	We can make the model simple and interpretable so that when the scammer adapts to it with just some tweaks we can have a new model up and running to deploy.<br>
# Data Description
Data Source: https://www.kaggle.com/mlg-ulb/creditcardfraud/data#<br>
The datasets contains transactions made by credit cards in September 2013 by european cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.<br>
It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, ... V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.<br>
We will see in the later parts of the article that the data we received is highly imbalanced i.e only 0.17% of the total Credit Card transaction is fraudulent. Well, a class imbalance is a very common problem in real life and needs to be handled before applying any algorithm to it.<br>

Dealing with Imbalance: So to compensate for the unbalancedness, we will use ADASYN oversampling method as implemented in imbalanced-learn package to resample the dataset. ADASYN (ADAptive SYNthetic) is an oversampling technique that adaptively generates minority data samples according to their distributions using K nearest neighbor.<br>

*This project checks the performance of Naïve Bayes, k-Nearest Neighbor and Random Forest Classifier on highly imbalanced credit card fraud dataset. The dataset is sourced from kaggle. The three methods are applied on the raw and preprocessed data. The work is implemented in Python. The dataset is spliited into train data and test data in the ratio 80:20 i.e. 80% train data and 20% test data. <br>
# Conclusion
The performance of the models are evaluated. Confusion matrix is shown and test data accuracy is calculated. The results shows of optimal accuracy for naïve bayes, k-nearest neighbor and random forest classifier are 94.96%, 99.7% and 99.9% respectively. The comparative results show that Random Forest Classifier performs better than naïve bayes and logistic regression techniques.
