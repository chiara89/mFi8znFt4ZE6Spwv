# Happy customers predictor
## Background:
We are one of the fastest growing startups in the logistics and delivery domain. We work with several partners and make on-demand delivery to our customers. During the COVID-19 pandemic, we are facing several different challenges and everyday we are trying to address these challenges.

We thrive on making our customers happy. As a growing startup, with a global expansion strategy we know that we need to make our customers happy and the only way to do that is to measure how happy each customer is. If we can predict what makes our customers happy or unhappy, we can then take necessary actions.

Getting feedback from customers is not easy either, but we do our best to get constant feedback from our customers. This is a crucial function to improve our operations across all levels.

We recently did a survey to a select customer cohort. You are presented with a subset of this data. We will be using the remaining data as a private test set.

## Data Description:
Y = target attribute (Y) with values indicating 0 (unhappy) and 1 (happy) customers
X1 = my order was delivered on time
X2 = contents of my order was as I expected
X3 = I ordered everything I wanted to order
X4 = I paid a good price for my order
X5 = I am satisfied with my courier
X6 = the app makes ordering easy for me

Attributes X1 to X6 indicate the responses for each question and have values from 1 to 5 where the smaller number indicates less and the higher number indicates more towards the answer.

## Goal:
Predict if a customer is happy or not based on the answers they give to questions asked.

## Methodology:
Exploratory Data Analysis and feature engineering were adopted to select the most informative features. Five different model were trained and evaluated:Logistic Regression, Support Virtual Machine (SVM), Decision Tree, Random Forest and XGBoost. The XGBoost outpermed the other models reaching 73% accuracy. Also the values of the precision, recall and F1_score on the two class predicted are accetable considering the limited amount of data. 

## Conclusions:
According to the analysis X1 corresponding to score of the delivery on time seems to be a key feature for predicting customer happiness. Two other important features are X5 (courier satisfaction) and X6 (app satisfaction). However surprisingly adding X5 in a previous attempt did not improve the classifier accuracy and for this reason the classifier were trained and tested using only X1 and X6. This finding could be explained by the small dataset containing only 126 samples. The size is certaintly not enough to train and test a classifier with acceptable accuracy and generalisation ability. The model with best accuracy was the XGBoost with 73% of accuracy on a test dataset of 26 samples. The main recomendation is to collect more data in order to improve accuracy. Question X2 (relation content as expected), X3(order everything wanted) and X4 (good price) seem to be not important so could be avoided and substituted with other questions related to the delivery. However given the limited amount of data it is better to collect more data and see if this conclusion is still valid before to eliminate potentially useful information.
