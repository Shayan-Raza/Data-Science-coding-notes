# Supervised Learning
**Training and Testing**
![[Pasted image 20220531163535.png]]

**Prediction** 
![[Pasted image 20220531164111.png]]

---
## Supervised learning Algorithms 
- *[[Supervised learning#Linear Regression Introduction to machine learning Regression Algorithm Regression |Linear Regression]]*: Estimate real values
- *[[Supervised learning#Logistic Regression |Logistic Regression]]*:  Estimate [[Statistics and Probability#Quantitative Data |Discrete]] values
- *[[Supervised learning#Decision Tree|Decision Tree]]*:  [[Introduction to machine learning#Classification Algorithm |Classification Algorithm |Classification Algorithm]]
- *[[Supervised learning#Random Forest |Random forest]]*:  Better than Decision Trees 
- *[[Supervised learning#Naive Bayes |Naive Bayes]]*: Based on [[Statistics and Probability#Bayes Theorem |Bayes Theorem]] 

### Linear Regression![[Introduction to machine learning#Regression Algorithm | Regression]] 
#### What is Regression?
Regression analysis is a form of predictive modelling techniques which investigates the relationship between a dependent and independent variable. 

#### Understanding Linear Regression 
![[Pasted image 20220606012715.png]]

![[Pasted image 20220606013144.png]]


**Calculating R^2**
![[Pasted image 20220606020615.png]]


**Using Scikit learn for calculation R^2 Score**
```Python 
from sklearn.linear_model import LinearRegression 
from sklearn.metrics import mean_squared_error

X = x.reshape(m,1)

reg = LinearRegression()

reg = reg.fit(x,y)

Y_pred = reg.predict(X)

r2 = reg.score(X, Y)
```
---
### Logistic Regression 
Logistic Regression produces results in a binary format which is used to predict the outcome of a categorical dependent variable. So the outcome should be discrete. 
![[Pasted image 20220606022721.png]]

**Use cases**
- Weather 
- Determine illness

**Implementing Logistic Regression**
- Collecting Data
- Analyzing Data
- Data Wrangling
- Train and test Data
- Accuracy check

**Confusion Matrix**
![[Pasted image 20220606162302.png]]

---
### Decision Tree 
- Graphical Representation of all the possible solutions 
- Decisions are based on some conditions 
- Decisions can be easily explained 
![[Pasted image 20220609170330.png]]


**Decision tree terminologies**
*Root node*: It represents the entire population and gets further divided
*Leaf node*: Node cannot be segregated into further nodes 
*Splitting*: Splitting is dividing a node based on some conditions
*Branch*: Formed by splitting the node 
*Pruning*: Removing unwanted branches from the tree 
*Parent/Child node*: Root node is the parent node and all other nodes are child nodes

---

### Random Forest
- Builds multiple decision trees and merges them together 
- More accurate and stable prediction 
- Do not overfit
- Trained with the bagging method

**Uses of random forest**
- Credit card detection 
- Medicine 
- Recommender system 
- Stocks
---

### KNN
- Stores all the available cases and classifies new cases based on a similarity measure 
- The K is the nearest neighbors we take vote from. K = 1 = only 1 neighbor 

**Uses of KNN**
- Recommender system
- Concept search

---
### Naive Bayes
- Classification based on  [[Statistics and Probability#Bayes Theorem |Bayes Theorem]]
- Assumes that the presence of a particular feature in a class is unrelated to the presence of any other feature
![[Pasted image 20220609203527.png]]

**Uses of naive bayes**
- News categorization 
- SPAM filtering 
- Medical Diagnosis
- Weather prediction

**Types of naive bayes**
- *Gaussian*: It is used in classification and it assumes that features follow a normal distribution.
- *Multinomial*: It is used for discrete counts. For example, let’s say,  we have a text classification problem. Here we can consider Bernoulli trials which is one step further and instead of “word occurring in the document”, we have “count how often word occurs in the document”, you can think of it as “number of times outcome number x_i is observed over the n trials”.
- *Bernoulli*: The binomial model is useful if your feature vectors are binary (i.e. zeros and ones). One application would be text classification with ‘bag of words’ model where the 1s & 0s are “word occurs in the document” and “word does not occur in the document” respectively.

---
### SVM(Support Vector Machines)
Support Vector Machines is a supervised classification method that separates data using hyperplanes. 

**Uses of SVM**
- Speech recognition

**What is a Hyperplane and how is it made**
A hyperplane is a decision boundary. An optimum hyperplane will have the maximum distance from a support vector (Data point). The hyperplane is made randomly until the result is achieved.