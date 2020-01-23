# Supervised vs Unsupervised
### What is supervised learning ?
An easy way to begin grasping the concept of supervised learning is by looking directly at the words that make it up.Supervise, means to observe,and direct the execution of a task, project, or activity.
So, **how do we supervise a machine learning model?** We do this by teaching the model, that is we load the model with knowledge so that we can have it predict future instances.

But this leads to the next question which is, **how exactly do we teach a model?** 

![2020-01-23_044349](https://user-images.githubusercontent.com/46414243/72952576-fdc49c00-3d9a-11ea-9a3d-3b7fba9a303a.png)



### Teaching the model with labeled data
We teach the model by training it with some data from a labeled dataset. It's important to note that the data is labeled,and **what does a labeled dataset look like?**
![2020-01-23_044638](https://user-images.githubusercontent.com/46414243/72952759-85aaa600-3d9b-11ea-8b68-47e66fdc783d.png)

Well, it could look something like this.This example is taken from the cancer dataset. As you can see, we have some historical data for patients,and we already know the class of each row. and we already know the class of each row.Let's start by introducing some components of this table.The names up here which are called clump thickness,uniformity of cell size,uniformity of cell shape,marginal adhesion and so on are called attributes.The columns are called **features** which include the data.If you plot this data,and look at a single data point on a plot,it'll have all of these attributes that would make a row on this chart also referred to as an observation.

Looking directly at the value of the data, you can have **two kinds**.**The first is numerical**.When dealing with machine learning,the most commonly used data is numeric.

**The second is categorical**,that is its non-numeric because it contains characters rather than numbers.In this case, it's categorical because this dataset is made for **classification**.


### Types of supervised learning
There are **two types** of supervised learning techniques.
They are **classification**, and **regression**.
![2020-01-23_044959](https://user-images.githubusercontent.com/46414243/72952856-d7ebc700-3d9b-11ea-842b-d51ac635694f.png)

### What is Classification ?
**Classification** is the process of predicting a discrete class label, or category.
![2020-01-23_045138](https://user-images.githubusercontent.com/46414243/72952929-108ba080-3d9c-11ea-8b1e-6305bae3cf43.png)

### What is Regression ?
**Regression** is the process of predicting a continuous value as opposed to predicting a categorical value in classification. 
![2020-01-23_045313](https://user-images.githubusercontent.com/46414243/72952991-4c266a80-3d9c-11ea-9eef-4c49f4707537.png)

Look at this dataset.It is related to CO2 emissions of different cars.It includes; engine size, cylinders,fuel consumption, and CO2 emission of various models of automobiles.Given this dataset, you can use regression to predict the CO2 emission of a new car by using other fields such as engine size,or number of cylinders.

### What is unsupervised learning ?
Since we know the meaning of supervised learning,**what do you think unsupervised learning means?**

Yes, **unsupervised learning** is exactly as it sounds.We do not supervise the model, but we let the model work on its own to discover information that may not be visible to the human eye.It means, the unsupervised algorithm trains on the dataset,and draws conclusions on unlabeled data.

![2020-01-23_045545](https://user-images.githubusercontent.com/46414243/72953082-a3c4d600-3d9c-11ea-8e02-470645ea6149.png)

Generally speaking, unsupervised learning has more difficult algorithms than supervised learning since we know little to no information about the data,or the outcomes that are to be expected.

**Dimension reduction, density estimation, market basket analysis, and clustering** are the most widely used unsupervised machine learning techniques.

**Dimensionality reduction, and/or feature selection**, play a large role in this by reducing redundant features to make the classification easier. 

**Density estimation** is a very simple concept that is mostly used to explore the data to find some structure within it.

**Market basket analysis** is a modeling technique based upon the theory that if you buy a certain group of items, you're more likely to buy another group of items.

And finally, **clustering**

### What is Clustering ?
**Clustering** is considered to be one of the most popular unsupervised machine learning techniques used for grouping data points,or objects that are somehow similar.

![2020-01-23_045800](https://user-images.githubusercontent.com/46414243/72953192-f56d6080-3d9c-11ea-8f36-59944834157a.png)

Cluster analysis has many applications in different domains,whether it be a bank's desire to segment his customers based on certain characteristics, or helping an individual to organize in-group his, or her favorite types of music.

Generally speaking though, **clustering** is used mostly for discovering structure,summarization, and anomaly detection.

### Supervised vs unsupervised learning
So, to recap, the biggest difference between **supervised and unsupervised learning** is that **supervised learning** deals with **labeled data** while **unsupervised learning** deals with **unlabeled data.**

In **supervised learning**, we have machine learning algorithms for **classification and regression.**

In **unsupervised learning**, we have methods such as **clustering**.

In comparison to supervised learning, **unsupervised learning** has fewer models and fewer evaluation methods that can be used to ensure that the outcome of the model is accurate.

As such, **unsupervised learning** creates a less controllable environment as the machine is creating outcomes for us. 

![2020-01-23_045953](https://user-images.githubusercontent.com/46414243/72953275-38c7cf00-3d9d-11ea-91f4-a63147a5c1f3.png)

