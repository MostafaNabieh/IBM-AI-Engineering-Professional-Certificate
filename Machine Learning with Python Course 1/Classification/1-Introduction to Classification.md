# Introduction to Classification

### What is classification ?
![2020-01-25_060203](https://user-images.githubusercontent.com/46414243/73116035-7876ee00-3f38-11ea-8208-586a8b8f403d.png)

In machine learning, **classification is a supervised learning approach** which can be thought of as a means of categorizing or classifying some unknown items into a discrete set of classes.

**Classification** attempts to learn the relationship between a set of feature variables and a target variable of interest. 

The target attribute in classification is a categorical variable with discrete values. 


### How does classification work?
![2020-01-25_060225](https://user-images.githubusercontent.com/46414243/73116034-7876ee00-3f38-11ea-8844-24245566b45f.png)

Given a set of training data points along with the target labels, classification determines the class label for an unlabeled test case. 
*Let's explain this with an example.A good sample of classification is the loan default prediction.* 




Suppose a bank is concerned about the potential for loans not to be repaid ? If previous loan default data can be used to predict which customers are likely to have problems repaying loans, these bad risk customers can either have their loan application declined or offered alternative products.

The goal of a loan default predictor is to use existing loan default data which has information about the customers such as age, income, education et cetera, to build a classifier, pass a new customer or potential future default to the model, and then label it, i.e the data points as defaulter or not defaulter. 

Or for example zero or one. This is how a classifier predicts an unlabeled test case. 
Please notice that this specific example was about a binary classifier with two values. **We can also build classifier models for both binary classification and multi-class classification.** 

### Example of multi-class classification
![2020-01-25_060432](https://user-images.githubusercontent.com/46414243/73116046-ad834080-3f38-11ea-87bf-097fb7df4de7.png)
for example, imagine that you've collected data about a set of patients, all of whom suffered from the same illness.During their course of treatment, each patient responded to one of three medications.You can use this labeled dataset with a classification algorithm to build a classification model.Then you can use it to find out which drug might be appropriate for a future patient with the same illness. 

### Classification use cases

![2020-01-25_060856](https://user-images.githubusercontent.com/46414243/73116082-369a7780-3f39-11ea-98b4-8b7e820cda86.png)
**Classification** has different business use cases as well. 
For example, to predict the category to which a customer belongs, for churn detection where we predict whether a customer switches to another provider or brand, or to predict whether or not a customer responds to a particular advertising campaign.

### Classification applications
![2020-01-25_060642](https://user-images.githubusercontent.com/46414243/73116068-0226bb80-3f39-11ea-9be6-42e2c2662ff3.png)

Data classification has several applications in a **wide variety of industries.**
Essentially, many problems can be expressed as associations between feature and target variables, especially when labelled data is available.This provides a broad range of applicability for classification. 

**For example, classification can be used for email filtering, speech recognition, handwriting recognition, biometric identification, document classification and much more.**

### Classification algorithms in machine learning

![2020-01-25_060753](https://user-images.githubusercontent.com/46414243/73116074-0fdc4100-3f39-11ea-8ec9-019b4f7952bc.png)

Here we have the types of classification algorithms and machine learning. They include decision trees, naive bayes, linear discriminant analysis, k-nearest neighbor, logistic regression, neural networks, and support vector machines. There are many types of classification algorithms. 
