
# Machine Learning

# Table of Contents
* [Overview](#overview)
* [Regression](#regression)
* [Classification](#classification)
	* [Classification Algorithms](#classification-Algorithms)

# Overview

## What is Machine Learning?


## Types of Machine Learning**
|  Types         |  Description      |
|----------------|------------------|
|Supervised      |-labed data      |
|Unsupervised    | -unlabed data   |
|Semi-Supervised |                 |
  
## Regression versus Classification


# Regression

## Algorithms

### Decision Trees
* For numerical data, each leaf node is a predicted value (basically choose average of last leaf node)

# Classification

## Classification Algorithms

| **Algorithm** 				|**Description** |
|-------------------------------|----------------|
| **Logistic Regression**       |                |
|**Naive Bayes** 			    |                |
|**Linear Support Classifiers** |				 |
|**K-Nearest Neighbors**        |				 |
|**Decision Trees**             |				 |
|**Random Forests**             |				 |
|**Support Vector Machine**     |				 |



### Decision Trees
(Also called Classification & Regression Trees (CART); Use If-Then-Else logic to classify)

<details><summary>More</summary>
<p>
#### How to Optimize <br>
<li>Look at every feature and decide which to split up
<li>Build split by split to determine best splits (find feature that gives the best separation)
<li>Uses greedy algorithm - always choose feature that optimizes on one of the following metrics:

#### Metrics for Fitting
1. Max Entropy Rule (for categorical)
	a. [Information Entropy Graph](https://upload.wikimedia.org/wikipedia/commons/2/22/Binary_entropy_plot.svg)
2. Gini Coefficient (for continuous feature)
3. Misclassification Error - how many things you get wrong as a percentage (goal minimize)

Pruning - take off nodes to generalize/prevent overfitting and improve performance

#### Variations/Methods
Ensemble (of Decision Trees) - using multiple trees
1. Bagging (Bootstrap Aggregating) - take randomly sampled subsets of training set (with replacement); Find different splits for each tree; predicts class that was choosen the most
2. Random Forests - using bagging but choose sqrt(n_features); then finds best split amoung those features; predicts class with majority vote (but can use weighted vote)


#### Additional
1. Pruning - take off nodes to generalize/prevent overfitting and improve performance
2. Boosting - improve model based on previously constructed classifiers

</p>
</details>

## Class Imbalances
(When one class that you are trying to classify is greater than the other - e.g. an unfair coin)

If we build a model on an imbalanced dataset, the model may predict the majority call all the time (which could lead to high acuracy - misleading). 

### Method 1: Oversampling 
<details><summary>Approaches</summary>
<p>
1. **Random** - Repeat data for minority class until it is balaned with the majority class. 
	
2. **Synthetic Minority Oversampling Technique (SMOTE)** - Similar to KNN, Create a new point in minority class that is between two nearest neighbors
	
3. **ADAptive SYNthetic oversampling (ADASYN)** - generates point where the class imbalance is the greatest; 

Note: Each approach comes at a cost (e.g. classifying more of minority class could cause more misclassification of majority class). The best solution depends on your problem and dataset.

</p>
</details>

### Method 2: Undersampling 

<details><summary>Approaches</summary>
<p>
1. **Random** - Randomly select observations in majority class so that the size of each class is equal. 
2. **Near Miss** - only sample points from the majority class necessary to distinguish between the classes
3. **NearMiss-1** select samples from the majority class for which the average distance of the N _closest_ samples of a minority class is smallest.

</p>
</details>

Note: If these methods don't work, see Anomaly Detection Algorithm. 


# Ensemble Methods

## Bagging

**Bootstrap aggregating**, or  **bagging**, is a type of machine learning algorithm that is designed to improve the accuracy and stability of the model.

1. Bootstrapping - sampling technique; Out of the 𝑛n samples in our dataset, 𝑘k samples are chosen **with replacement**.
2. Aggregating - 
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzU5Nzk0OTk1LDQyMTQwNTk0OCwtMzUyNz
g0Mjg5LDEyOTgxNTQxMzMsNzQ4NTY5NDU3LDEyMzQzMzE2MTUs
MTEwMjQzMzIxMSwtMTEwMTI5NTg0NiwtMTg4MTczMDI4OSw4Mj
MyNzk0OTcsLTE5OTE3NDk2NDksMjAxMDc5MDA2Myw0MDQzODU4
ODIsMTcyODU1MzMzNCwtMTUzOTEzOTkxMCwyNzg4MjMyODMsMT
kzODk2ODkwNSw2Mjk3MjU5NjksLTEzNTk3OTI3ODQsLTIwNjU2
MjYzNTNdfQ==
-->