# Week 1

In this week, you will learn about applications of Machine Learning in different fields such as health care, banking, telecommunication, and so on. You’ll get a general overview of Machine Learning topics such as supervised vs unsupervised learning, and the usage of each algorithm. Also, you understand the advantage of using Python libraries for implementing Machine Learning models.


## Introduction to Machine Learning
### Is this a Benign or Malignant cell?
This is a human cell sample extracted from a patient, and this cell has characteristics. For example, its clump thickness is 6, its uniformity of cell size is 1, its marginal adhesion is 1, and so on.

![2020-01-22_200443](https://user-images.githubusercontent.com/46414243/72920751-9d117100-3d52-11ea-8ac3-96ed08e72bc7.png)
One of the interesting questions we can ask, at this point is: **Is this a benign or malignant cell ?**

In contrast with a benign tumor, a malignant tumor is a tumor that may invade its surrounding tissue or spread around the body, and diagnosing it early might be the key to a patient’s survival.
One could easily presume that only a doctor with years of experience could diagnose that tumor and say if the patient is developing cancer or not. Right?
### Machine Learning helps with predictions
Well, imagine that you've obtained a dataset containing characteristics of thousands of human cell samples extracted from patients who were believed to be at risk of developing cancer. 
Analysis of the original data showed that many of the characteristics differed significantly between benign and malignant samples.
You can use the values of these cell characteristics in samples from other patients to give an early indication of whether a new sample might be benign or malignant.
You should clean your data, select a proper algorithm for building a prediction model, and train your model to understand patterns of benign or malignant cells within the data.
Once the model has been trained by going through data iteratively, it can be used to predict your new or unknown cell with a rather high accuracy.
**This is machine learning!** It is the way that a machine learning model can do a doctor’s task or at least help  that doctor make the process faster.

![1](https://user-images.githubusercontent.com/46414243/72922953-b0264000-3d56-11ea-8646-fc333e4e3ca0.png)


### What is Machine Learning ? 
Machine learning is the subfield of computer science that gives "computers the ability to learn without being explicitly programmed.” 
![2020-01-22_210314](https://user-images.githubusercontent.com/46414243/72925069-bcac9780-3d5a-11ea-815f-0ba39ef2cd87.png)

**Let me explain what I mean when I say “without being explicitly programmed.”**

### How machine learning works ?
Assume that you have a dataset of images of animals such as cats and dogs, and you want to have software or an application that can recognize and differentiate them.
![2020-01-22_210926](https://user-images.githubusercontent.com/46414243/72925826-021d9480-3d5c-11ea-9c30-189b852e328b.png)
**The first thing** that you have to do here is interpret the images as a set of feature sets.For example, does the image show the animal’s eyes? If so, what is their size? Does it have ears? What about a tail? How many legs? Does it have wings? Prior to machine learning, each image would be transformed to a vector of features.

**Then,** traditionally, we had to write down some rules or methods in order to get computers to be intelligent and detect the animals.
**But, it was a failure.**

**Why?** *Well, as you can guess, it needed a lot of rules, highly dependent on the current dataset, and not generalized enough to detect out-of-sample cases.*

Using machine learning, allows us to build a model that looks at all the feature sets, and their corresponding type of animals, and it learns the pattern of each animal.
It is a model built by machine learning algorithms. It detects without explicitly being programmed to do so.
In essence, machine learning follows the same process that a **4-year-old child uses to learn**, understand, and differentiate animals.
**So, machine learning algorithms, inspired by the human learning process, iteratively learn from data, and allow computers to find hidden insights.** 
**These models help us in a variety of tasks, such as**
* Object recognition,
* Summarization,
* Recommendation,and so on.

