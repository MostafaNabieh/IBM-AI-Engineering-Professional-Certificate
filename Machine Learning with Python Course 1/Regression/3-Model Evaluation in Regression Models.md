# Model Evaluation in Regression Models

### Model evaluation approaches
The goal of regression is to build a model to accurately predict an unknown case. To this end, we have to perform regression evaluation after building the model. These approaches are train and test on the same dataset and train/test split.

![2020-01-24_090545](https://user-images.githubusercontent.com/46414243/73050521-d5b36680-3e88-11ea-8ec3-a29bffbc501b.png)

### Best approach for most accurate results ?
Let's look at the first approach. When considering evaluation models,  we clearly want to choose the one that will give us the most accurate results. 

**So, the question is,  how can we calculate the accuracy of our model?
In other words, how much can we trust this model for prediction of  an unknown sample using a given dataset and having built a model such as linear regression?**

![2020-01-24_090846](https://user-images.githubusercontent.com/46414243/73050631-2925b480-3e89-11ea-9374-6d02ed9d8f41.png)

**One of the solutions is to select a portion of our dataset for testing.** For instance, assume that we have 10 records in our dataset.  
We use the entire dataset for training, and we build a model using this training set.

Now, we select a small portion of the dataset, such as row number six to nine,  but without the labels.**This set is called a test set**, which has the labels, but the **labels are not used for prediction and is used only as ground truth.The labels are called actual values of the test set.**

Now we pass the feature set of the testing portion to our built model and predict the target values. Finally, **we compare the predicted values by our model with the actual values in the test set.** This indicates how accurate our model actually is. 

There are different metrics to report the accuracy of the model, **but most of them work generally based on the similarity of the predicted and actual values.**

### Calculation the accuracy of a model
Let's look at one of the simplest metrics to  calculate the accuracy of our regression model.As mentioned, we just compare the actual values y with the predicted values, which is noted as y hat for the testing set. The error of the model is calculated as the average difference between the predicted and actual values for all the rows.

![2020-01-24_090918](https://user-images.githubusercontent.com/46414243/73050700-5a9e8000-3e89-11ea-846c-b2edbb9b8287.png)

### Train and Test on the same dataset
So, the first evaluation approach we just talked about is the simplest one, train and test on the same dataset. Essentially, the name of this approach says it all. You train the model on the entire dataset, then you test it using a portion of the same dataset. In a general sense, when you test with a dataset in which you know the target value for each data point, you're able to obtain a percentage of accurate predictions for the model. This evaluation approach would most likely have a high training accuracy and the low out-of-sample accuracy since the model knows all of the testing data points from the training.

![2020-01-24_091102](https://user-images.githubusercontent.com/46414243/73050753-8ae61e80-3e89-11ea-9e24-c2f7c80c1406.png)

### What is training accuracy and out-of-sample accuracy?
We said that training and testing on the same dataset produces a high training accuracy,  but **what exactly is training accuracy? 
Training accuracy is the percentage of correct predictions that the model makes when using the test dataset.** 

**However, a high training accuracy isn't necessarily a good thing.For instance, having a high training accuracy may result in an over-fit the data.**

**This means that the model is overly trained to the dataset**, which may capture noise and produce a non-generalized model. 

**Out-of-sample accuracy is the percentage of correct predictions that the model makes on data that the model has not been trained on.** 

Doing a train and test on the same dataset will most likely have low out-of-sample accuracy due to the likelihood of being over-fit.
**It's important that our models have high out-of-sample accuracy because the purpose of our model is,** of course, to make correct predictions on unknown data. So, how can we improve out-of-sample accuracy?

![2020-01-24_091255](https://user-images.githubusercontent.com/46414243/73050820-bd901700-3e89-11ea-8735-1519801c495b.png)

### Train/Test split evaluation approach
**One way is to use another evaluation approach called train/test split.** 
In this approach, we select a portion of our dataset for training, for example, row zero to five, and the rest is used for testing, for example, row six to nine.The model is built on the training set. Then, the test feature set is passed to the model for prediction.
Finally, the predicted values for  the test set are compared with the actual values of the testing set. 

![2020-01-24_091730](https://user-images.githubusercontent.com/46414243/73051035-6474b300-3e8a-11ea-8acb-71929cd92114.png)
![2020-01-24_091355](https://user-images.githubusercontent.com/46414243/73051034-6474b300-3e8a-11ea-8b52-8d3b391aee78.png)

**The second evaluation approach is called train/test split.** **Train/test split** involves splitting the dataset into training and testing sets respectively, which are mutually exclusive. After which, you train with the training set and test with the testing set.

**This will provide a more accurate evaluation on out-of-sample accuracy because the testing dataset is not part of the dataset that has been used to train the data.**

Since this data has not been used to train the model,the model has no knowledge of the outcome of these data points. **So, in essence, it's truly out-of-sample testing.**

However, please ensure that you train your model with the testing set afterwards, as you don't want to lose potentially valuable data.
The issue with train/test split is that it's highly  dependent on the datasets on which the data was trained and tested. 
**The variation of this causes train/test split to have a better out-of-sample prediction than training and testing on the same dataset, 
but it still has some problems due to this dependency.**  

### How to use k-fold cross-validation ?
Another evaluation model, **called K-fold cross-validation**,  resolves most of these issues. How do you fix a high variation that results from a dependency? 
The entire dataset is represented by the points in the image at the top left. If we have K equals four folds, then we split up this dataset as shown here. 
**In the first fold for example, we use the first 25 percent of the dataset for testing and the rest for training.** 

The model is built using the training set and is evaluated using the test set. Then, in the **next round or in the second fold, the second 25 percent of the dataset is used for testing and the rest for training the model.** 
**Again, the accuracy of the model is calculated. We continue for all folds.**
**Finally, the result of all four evaluations are averaged.**
That is, the accuracy of each fold is then averaged, keeping in mind that each fold is distinct, where no training data in one fold is used in another. **K-fold cross-validation** in its simplest form performs multiple train/test splits, using the same dataset where each split is different.Then, the result is average to produce a more consistent out-of-sample accuracy.

![2020-01-24_091628](https://user-images.githubusercontent.com/46414243/73051054-6dfe1b00-3e8a-11ea-8e56-1758da940291.png)
