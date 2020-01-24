# Simple Linear Regression

### Using linear regression to predict continuous values
The question is, given this data set, can we predict the Co2 emission of a car using another field such as engine size? **Quite simply, yes.**

We can use linear regression to predict a continuous value such as Co2 emission by using other variables.

![2020-01-24_084930](https://user-images.githubusercontent.com/46414243/73049883-9e43ba80-3e86-11ea-9d28-c2c19431e2f4.png)
![2020-01-24_073505](https://user-images.githubusercontent.com/46414243/73046815-2c667380-3e7c-11ea-8453-70747f28d152.png)

**Linear regression** is the approximation of a linear model used to describe the relationship between two or more variables.
In simple linear regression, there are two variables, **a dependent variable and an independent variable.**

The key point in the linear regression is that **our dependent value should be continuous and cannot be a discrete value.**

However, **the independent variables can be measured on either a categorical or continuous measurement scale.**

### Linear regression typology

There are two types of linear regression models. **They are simple regression and multiple regression.**

**Simple linear regression is when one independent variable is used to estimate a dependent variable.**
For example, predicting Co2 emission using the engine size variable. 

**When more than one independent variable is present the process is called multiple linear regression**, for example, predicting Co2 emission using engine size and cylinders of cars.


![2020-01-24_073735](https://user-images.githubusercontent.com/46414243/73046901-6fc0e200-3e7c-11ea-9c7f-b5309a497287.png)


### How does linear regression work ?
To understand linear regression, we can plot our variables here. 
We show engine size as an independent variable and emission as the target value that we would like to predict.
A scatter plot clearly shows the relation between variables where changes in one variable explain or possibly cause changes in the other variable. Also, it indicates that these variables are linearly related.

With linear regression you can fit a line through the data.

![2020-01-24_073845](https://user-images.githubusercontent.com/46414243/73046953-a39c0780-3e7c-11ea-99e9-e212e84cb41e.png)

For instance, as the engine size increases, so do the emissions. With linear regression you can model the relationship of these variables. A good model can be used to predict what the approximate emission of each car is. How do we use this line for prediction now?
Let us assume for a moment that the line is a good fit of the data. We can use it to predict the emission of an unknown car.
For example, for a sample car with engine size 2.4, you can find the emission is 214.

### Linear regression model representation
We're going to predict the target value y. In our case using the independent variable engine size represented by x1.
The fit line is shown traditionally as a polynomial. In a simple regression problem, a single x,the form of the model would be theta 0 plus theta 1 x1.

![2020-01-24_084940](https://user-images.githubusercontent.com/46414243/73049932-c7644b00-3e86-11ea-96a2-614aa1dca85d.png)

![2020-01-24_074049](https://user-images.githubusercontent.com/46414243/73047007-e6f67600-3e7c-11ea-8c53-c9b434fc3d17.png)

In this equation, **y hat is the dependent variable** of the predicted value. And **x1 is the independent variable.**

**Theta 0 and theta 1 are the parameters of the line that we must adjust.Theta 1 is known as the slope or gradient of the fitting line and theta 0 is known as the intercept.Theta 0 and theta 1 are also called the coefficients of the linear equation.**

You can interpret this equation as y hat being a function of x1, or y hat being dependent of x1.

**How would you draw a line through the points? And how do you determine which line fits best?**

*Linear regression estimates the coefficients of the line. This means we must calculate theta 0 and theta 1 to find the best line to fit the data.*
### How to find the best fit ?
Now, let's go through all the points and check how well they align with this line. Best fit here means that if we have, for instance, a car with engine size x1 = 5.4 and actual Co2 = 250, its Co2 should be predicted very close to the actual value, which is y = 250 based on historical data.

But if we use the fit line, or better to say using our polynomial with known parameters to predict the Co2 emission, it will return y hat = 340. Now if you compare the actual value of the emission of the car with what we've predicted using our model, you will find out that we have a 90 unit error.

This means our prediction line is not accurate. This error is also called the **residual error.**

![2020-01-24_074233](https://user-images.githubusercontent.com/46414243/73047057-1c02c880-3e7d-11ea-8bdf-5067b87eff8c.png)

So we can say the error is the distance from the data point to the fitted regression line. The mean of all residual errors shows how poorly the line fits with the whole data set. 

**The objective of linear regression, is to minimize this MSE equation and to minimize it, we should find the best parameters theta 0 and theta 1.**

Now the question is how to find theta 0 and theta 1 in such a way that it minimizes this error? How can we find such a perfect line? Or said another way, how should we find the best parameters for our line?

**Should we move the line a lot randomly and calculate the MSE value every time and choose the minimum one? 
Not really.**

Actually, **we have two options here. Option one, we can use a mathematic approach, or option two, we can use an optimization approach.**

**Mathematically** it can be shown by the equation **Mean Squared Error, shown as MSE.**

### Estimating the parameters

**(MSE)**
Let's see how we could easily use a mathematic formula to find the theta 0 and  theta 1. As mentioned before, theta 0 and theta 1 in the simple linear regression are the coefficients of the fit line. We can use a simple equation to estimate these coefficients. That is, given that it's a simple linear regression with only two parameters, and knowing that theta 0 and theta 1 are the intercept and slope of the line, we can estimate them directly from our data.

**It requires that we calculate the mean of the independent and dependent or target columns from the data set.**

![2020-01-24_074357](https://user-images.githubusercontent.com/46414243/73047124-6126fa80-3e7d-11ea-8c58-d4c0a3655f73.png)

**We can start off by estimating the value for theta 1.**

This is how you can find the slope of a line based on the data. X bar is the average value for the engine size in our data set. 
Please consider that we have nine rows here, rows 0 to 8.

**First we calculate the average of x1 and of y,then we plug it into the slope equation to find theta 1.**

The xi and yi in the equation refer to the fact that we need to repeat these calculations across all values in our data set.
Applying all values, we find theta 1 equals 39.

**It is our second parameter.**

It is used to calculate the first parameter which is the intercept of the line. Now we can plug theta 1 into the line equation to find theta 0. 

It is easily calculated y hat theta 0 equals 125.74. So these are the two parameters for the line, where theta 0 is also called the **bias coefficient**, and  theta 1 is the **coefficient** for the Co2 emission column.

**As a side note,** you really don't need to remember the formula for calculating these parameters, as most of the libraries used for machine learning in Python, R and Scala can easily find these parameters for you. **But it's always good to understand how it works.**
Now, we can write down the polynomial of the line. So we know how to find the best fit for our data and its equation.

**Now the question is how can we use it to predict the emission of a new car  based on its engine size?**

### Predictions with linear regression

After we found the parameters of the linear equation,  making predictions is as simple as solving the equation for a specific set of inputs. Imagine we are predicting Co2 emission, or y, from engine size, or x for the automobile in record number 9. 

Our linear regression model representation for this problem would be **y hat= theta 0 + theta 1 x1.** Or if we map it to our data set, it would be **Co2Emission = theta 0 + theta 1 EngineSize.**

![2020-01-24_074658](https://user-images.githubusercontent.com/46414243/73047229-bbc05680-3e7d-11ea-9c87-49001d2b61ba.png)

As we saw, we can find theta 0, theta 1 using the equations that we just talked about. Once found, we can plug in the equation of the linear model. For example, let's use theta 0 = 125 and theta 1 = 39.

So we can rewrite the linear model as Co2Emission equals 125 plus 39 EngineSize.  Now let's plug in the 9th row of our data set and calculate the Co2 emission for a car with an engine size of 2.4. 

**So Co2Emission = 125 + 39 x 2.4. Therefore, we can predict that the Co2Emission for this specific car would be 218.6.**

### Pros of linear regression
Quite simply, it is the most basic regression to use and understand. 
In fact, **one reason why linear regression is so useful is that it's fast.**
It also doesn't require tuning of parameters. 
So something like tuning the K parameter and K nearest neighbors, or the learning rate in neural networks isn't something to worry about. **Linear regression is also easy to understand, and highly interpretable.**

![2020-01-24_074800](https://user-images.githubusercontent.com/46414243/73047284-e01c3300-3e7d-11ea-97f1-bbe281e99861.png)
