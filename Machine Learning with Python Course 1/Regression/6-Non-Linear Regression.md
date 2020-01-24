# Non-Linear Regression.

### Should we use linear regression ?
These data points correspond to China's gross domestic product or GDP from 1960-2014.
The first column is the years and the second is China's corresponding annual gross domestic income in US dollars for that year. 
![2020-01-24_230621](https://user-images.githubusercontent.com/46414243/73104052-2b762600-3efe-11ea-9ee1-e465ab5f4dad.png)
This is what the data points look like. Now, **we have a couple of interesting questions.** 
First, can GDP be predicted based on time?
Second, can we use a simple linear regression to model it? 

**Indeed. If the data shows a curvy trend, then *linear regression* would not produce very accurate results when compared to a *non-linear regression.*** 


Simply because, as the name implies, linear regression presumes that the data is linear. The scatter plot shows that there seems to be a strong relationship between GDP and time, but the relationship is not linear.

As you can see, the growth starts off slowly, then from 2005 onward, the growth is very significant. Finally, it decelerates slightly in the 2010s. It looks like either a logistical or exponential function. So, it requires a special estimation method of the non-linear regression procedure. 

**For example,** if we assume that the model for these data points are exponential functions, such as Y hat equals Theta zero plus Theta one Theta two transpose X or to the power of X, our job is to estimate the parameters of the model, i.e., Thetas, and use the fitted model to predict GDP for unknown or future cases.


### Different types of regression

![2020-01-24_230734](https://user-images.githubusercontent.com/46414243/73104161-6bd5a400-3efe-11ea-9e96-7b53f6f39e87.png)

In fact, many different regressions exists that can be used to fit whatever the dataset looks like. 
**You can see a quadratic and cubic regression lines here**, and it can go on and on to infinite degrees. In essence, we can call all of these polynomial regression, where the relationship between the independent variable X and the dependent variable Y is modeled as an Nth degree polynomial in X. With many types of regression to choose from, there's a good chance that one will fit your dataset well. Remember, it's important to pick a regression that fits the data the best. 

### What is polynomial regression?

![2020-01-24_230924](https://user-images.githubusercontent.com/46414243/73104211-97f12500-3efe-11ea-931e-90d0e59dc00a.png)
**So, what is polynomial regression? Polynomial regression fits a curve line to your data.**

A simple example of polynomial with degree three is shown as Y hat equals Theta zero plus Theta 1_X plus Theta 2_X squared plus Theta 3_X cubed or to the power of three, where Thetas are parameters to be estimated that makes the model fit perfectly to the underlying data.

Though the relationship between X and Y is non-linear here and polynomial regression can't fit them, **a polynomial regression model can still be expressed as linear regression.**


I know it's a bit confusing, but let's look at an example. Given the third degree polynomial equation, by defining X_1 equals X and X_2 equals X squared or X to the power of two and so on, the model is converted to a simple linear regression with new variables as Y hat equals Theta zero plus Theta one X_1 plus Theta two X_2 plus Theta three X_3. This model is linear in the parameters to be estimated, right? Therefore, this polynomial regression is considered to be a special case of traditional multiple linear regression. 

So, you can use the same mechanism as linear regression to solve such a problem. Therefore, polynomial regression models can fit using the model of least squares. Least squares is a method for estimating the unknown parameters in a linear regression model by minimizing the sum of the squares of the differences between the observed dependent variable in the given dataset and those predicted by the linear function.

### What is non-linear regression ?

![2020-01-24_231056](https://user-images.githubusercontent.com/46414243/73104313-cff86800-3efe-11ea-8a53-53034d7a54c3.png)

**what is non-linear regression exactly?** First, non-linear regression is a method to model a non-linear relationship between the dependent variable and a set of independent variables.

Second, for a model to be considered non-linear, Y hat must be a non-linear function of the parameters Theta, not necessarily the features X.

When it comes to non-linear equation, it can be the shape of exponential, logarithmic, and logistic, or many other types. As you can see in all of these equations, the change of Y hat depends on changes in the parameters Theta, not necessarily on X only. 

That is, in non-linear regression, a model is non-linear by parameters. In contrast to linear regression, **we cannot use the ordinary least squares method to fit the data in non-linear regression.** In general, estimation of the parameters is not easy.

### Linear vs non-linear regression

![2020-01-24_231221](https://user-images.githubusercontent.com/46414243/73104402-01713380-3eff-11ea-8cdb-6bd3f86fed35.png)

 Let me answer two important questions here. 

**First, how can I know if a problem is linear or non-linear in an easy way? 
To answer this question, we have to do two things. The first is to visually figure out if the relation is linear or non-linear.**

It's best to plot bivariate plots of output variables with each input variable.

