# K-Nearest Neighbours

### Intro to KNN
![2020-01-25_063429](https://user-images.githubusercontent.com/46414243/73116310-ddccde00-3f3c-11ea-9f3b-6ef7ef49ac54.png)
Imagine that a telecommunications provider has segmented his customer base by service usage patterns, categorizing the customers into four groups. 


If demographic data can be used to predict group membership the, company can customize offers for individual perspective customers.This is a classification problem. That is; given the dataset with predefined labels, we need to build a model to be used to predict the class of a new or unknown case. The example focuses on using demographic data, such as; region, age, and marital status to predict usage patterns.The target field called custcat has four possible values that correspond to the four customer groups as follows; Basic Service, E Service, Plus Service, and Total Service. 

**Our objective is to build a classifier.**
*For example, using the row zero to seven to predict the class of row eight, we will use a specific type of classification called K-Nearest Neighbor.* 

### Determining the class using 1(st) KNN

![2020-01-25_063649](https://user-images.githubusercontent.com/46414243/73116332-356b4980-3f3d-11ea-827f-ff74a26124aa.png)

Now, let's say that we have a new customer.For example, record number eight, with a known age and income. 
How can we find the class of this customer? Can we find one of the closest cases and assign the same class label to our new customer? Can we also say that the class of our new customer is most probably group four i.e Total Service, **because it's nearest neighbor is also of class four? Yes, we can.**

In fact, it is the first nearest neighbor. 

**Now, the question is,** to what extent can we trust our judgment which is based on the first nearest neighbor? It might be a poor judgment especially, if the first nearest neighbor is a very specific case or an outlier, correct? Now, let's look at our scatter plot again. 

Rather than choose the first nearest neighbor, what if we chose the five nearest neighbors and did a majority vote among them to define the class of our new customer? In this case, we'd see that three out of five nearest neighbors tell us to go for class three, which is Plus Service.

Doesn't this make more sense? Yes. In fact, it does. In this case, the value of K in the K-Nearest Neighbors algorithm is five. 
This example highlights the intuition behind the K-Nearest Neighbors algorithm. Now, let's define the **K Nearest Neighbors.**

### What is k nearest neighbor (or KNN) ?

![2020-01-25_063840](https://user-images.githubusercontent.com/46414243/73116344-6481bb00-3f3d-11ea-8a5f-dc7f936ce034.png)

The **K-Nearest Neighbors algorithm** is a classification algorithm that takes a bunch of labeled points and uses them to learn how to label other points. This algorithm classifies cases based on their similarity to other cases.



In K-Nearest Neighbors, data points that are near each other are said to be neighbors.**K-Nearest Neighbors** is based on this paradigm. Similar cases with the same class labels are near each other. 

Thus, the distance between two cases is a measure of their **dissimilarity.**

There are different ways to calculate the similarity or conversely, the distance or dissimilarity of two data points. 
For example, this can be done using *Euclidean distance.*


### The K-Nearest Neighbors algorithm
![2020-01-25_064038](https://user-images.githubusercontent.com/46414243/73116367-cd693300-3f3d-11ea-8ec8-b93eaa75380a.png)

In a classification problem, the K-Nearest Neighbors algorithm works as follows.

One, pick a value for K. 

Two, calculate the distance from the new case hold out from each of the cases in the dataset. 

Three, search for the K-observations in the training data that are nearest to the measurements of the unknown data point. 

And four, predict the response of the unknown data point using the most popular response value from the K-Nearest Neighbors. 

There are two parts in this algorithm that might be a bit confusing.
**First,** how to select the correct K and second, how to compute the similarity between cases, for example, among customers. 

Let's first start with the second concern. That is; how can we calculate the similarity between two data points? 

### Calculation the similarity/distance in 1-dimensional space
![2020-01-25_064234](https://user-images.githubusercontent.com/46414243/73116384-02758580-3f3e-11ea-925c-fdbcefbae4d2.png)

Assume that we have two customers, customer one and customer two, and for a moment, assume that these two customers have only one feature, H. 
We can easily use a specific type of Minkowski distance to calculate the distance of these two customers, it is indeed the Euclidean distance. 
Distance of X_1 from X_2 is root of 54 minus 50 to power of two, which is four. What about if we have more than one feature?

### Calculation the similarity/distance in 2-dimensional space

![2020-01-25_064245](https://user-images.githubusercontent.com/46414243/73116385-0e614780-3f3e-11ea-9d86-92c41728b50e.png)

For example, age and income. If we have income and age for each customer, we can still use the same formula but this time, we're using it in a two dimensional space. 



### Calculation the similarity/distance in multi-dimensional space
![2020-01-25_064432](https://user-images.githubusercontent.com/46414243/73116404-541e1000-3f3e-11ea-8e0d-21e947400fed.png)

We can also use the same distance matrix for multidimensional vectors. Of course, we have to normalize our feature set to get the accurate dissimilarity measure. There are other dissimilarity measures as well that can be used for this purpose but as mentioned, it is highly dependent on datatype and also the domain that classification is done for it. 

### What is best value of K for KNN

![2020-01-25_064703](https://user-images.githubusercontent.com/46414243/73116425-c2fb6900-3f3e-11ea-8f51-891571e72556.png)

As mentioned, K and K-Nearest Neighbors is the number of nearest neighbors to examine.It is supposed to be specified by the user.
So, how do we choose the right K? Assume that we want to find the class of the customer noted as question mark on the chart.What happens if we choose a very low value of K? Let's say, K equals one. The first nearest point would be blue, which is class one. 

This would be a **bad prediction,** since more of the points around it are magenta or class four.In fact, since its nearest neighbor is blue we can say that we capture the noise in the data or we chose one of the points that was an anomaly in the data. 

A low value of K causes a highly complex model as well, which might result in overfitting of the model. It means the prediction process is not generalized enough to be used for out-of-sample cases. Out-of-sample data is data that is outside of the data set used to train the model. In other words, it cannot be trusted to be used for prediction of unknown samples.

**It's important to remember** that overfitting is bad, as we want a general model that works for any data, not just the data used for training. 

Now, on the opposite side of the spectrum, if we choose a very high value of K such as K equals 20, then the model becomes overly generalized. 

So, how can we find the best value for K? **The general solution is to reserve a part of your data for testing the accuracy of the model.**

*Once you've done so, choose K equals one and then use the training part for modeling and **calculate the accuracy** of prediction using all samples in your test set.Repeat this process increasing the K and see which K is best for your model.
For example, in our case, K equals four will give us the best accuracy.*

### Computing continuous target using KNN

![2020-01-25_064910](https://user-images.githubusercontent.com/46414243/73116433-d60e3900-3f3e-11ea-8c37-34e312670be5.png)

Nearest neighbors analysis can also be used to compute values for a continuous target.In this situation, the average or median target value of the nearest neighbors is used to obtain the predicted value for the new case. For example, assume that you are predicting the price of a home based on its feature set, such as number of rooms, square footage, the year it was built, and so on. You can easily find the three nearest neighbor houses of course not only based on distance but also based on all the attributes and then predict the price of the house as the medium of neighbors. 

