# MultiLabel-Classification

Data Source: https://github.com/zalandoresearch/fashion-mnist

# Introduction

The aim of the project was to predict the label of an image based on the observations of brightness factor of 49 pixels(7*7). The labels 
include Tshirts, Shirts, Pullovers, Trousers, Ankle Boots etc. The training set involves 60,000 observarions and the trained models 
were tested on 10,000 observations acting as the validation set. 

# Evaluation 
The main evaluation metric of the machine learning algorithms is based on the trade-off between accuracy, time taken to run the model and sample size taken from training dataset for training the model.

Scoring Criterion:

Points = 0.25 * A + 0.25 * B + 0.5 * C

where

A is the proportion of the training rows that is utilized in the model. For instance, if you use 30,000 of the 60,000 rows, then A = 30,000 / 60,000 = 0.5;

B = min(1,X60)
, where X is the running time of the selected algorithm in seconds. Algorithms that take at least 1 minute to run will have the value B = 1, which incurs the full run-time penalty.

C is the proportion of the predictions on the testing set that are incorrectly classified. For instance, if 1000 of the 10000 rows are incorrectly classified, then C = 1000 / 10000 = 0.1.

Hence, the focus was not only on accuracy but also on efficiency of coding as time is valuable and the trade off between accuracy and
computational speed matters. 

# Sample Sizes

To use different sample sizes, 3 iterations for 3 different sample sizes were taken for each model. Therefore, for each model 9 samples
were taken. So, in total 90 separate models.(9 * 10). 

# Machine Learning

The machine learning algorithms file shows each model and the iterations performed. The following modeling techniques were applied:

1) Support Vector Machine(SVM)
2) kNN
3) Ridge Regression
4) Random Forest
5) Multinomial Regression
6) Lasso Regrerssion
7) Ensemble Model of Random Forest, SVM and Multinomial regression.


Interpretation of Models

In this trade off between accuracy and computational efficiency, Random Forest came out as a clear winner with points recorded
as low as 0.11

Support vector machines did really good as well in terms of points scored (0.14), performing well in accuracy of predictions and also
not taking enough time but random forest was slighly better in both these areas. 

Ridge regression was as good as support vector machines when it comes to evaluating the points (0.15) but accuracy was lesser than 
that of svm and time taken to compute was lesser. So SVM was a better choice to give a good balance of both the parameters

k-nearest neighbour technique performed better with a low value of k but still was not good enough with its accuracy when compared to other
modeling techniques discussed earlier. (avg points observed: 0.20)

Multinomial regression did a good job on efficiency but lacked the accuracy parameter which did not make it a point friendly 
algorithm. The points revolved around 0.22

Lasso was the worst performing technique in terms of the points observed (0.35) as the time taken to run was too high. 

Finally, the ensembled model was evaluated which gave good predictions. However, random forest as a standalone model did much better than the combined model
consisting of average predictions taken from random forest, svm and multinomial. 


