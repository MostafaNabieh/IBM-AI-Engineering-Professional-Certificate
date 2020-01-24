# Multiple Linear Regression

### Types of regression models

![2020-01-24_113654](https://user-images.githubusercontent.com/46414243/73059239-f803af00-3e9d-11ea-81bb-71d793f85a75.png)

As you know, there are two types of linear regression models, simple regression and multiple regression. 
**Simple linear** regression is when one independent variable is used to estimate a dependent variable.
For example, predicting CO_2 emission using the variable of engine size. 

In reality, there are multiple variables that predict the CO_2 emission. 
When **multiple independent** variables are present, the process is called multiple linear regression. 
For example, predicting CO_2 emission using engine size and the number of cylinders in the car's engine. 

### Examples of multiple linear regression

![2020-01-24_113910](https://user-images.githubusercontent.com/46414243/73059331-2ed9c500-3e9e-11ea-8fcf-fbe170d43fe1.png)

Before we dive into a sample dataset and see how multiple linear regression works, I want to tell you what kind of problems it can solve, when we should use it, and specifically,what kind of questions we can answer using it.

Basically, there are two applications for multiple linear regression. 

**First,** it can be used when we would like to identify the strength of the effect that the independent variables have on the dependent variable.
EX :
lecture attendance and gender have any effect on exam performance of students? 

**Second,** it can be used to predict the impact of changes, that is, to understand how the dependent variable changes when we change the independent variables.
For example, if we were reviewing a person's health data, a multiple linear regression can tell you how much that person's blood pressure goes up or down for every unit increase or decrease in a patient's body mass index holding other factors constant.

### Predicting continuous variable with multiple linear regression

![2020-01-24_114106](https://user-images.githubusercontent.com/46414243/73059449-706a7000-3e9e-11ea-88fa-e20ad8458084.png)

It uses **multiple variables** called independent variables or predictors that best predict the value of the target variable which is also called the dependent variable. In multiple linear regression, the target value Y, is a linear combination of independent variables X.For example, you can predict how much CO_2 a car might admit due to independent variables such as the car's engine size, number of cylinders, and fuel consumption.

Multiple linear regression is very useful because you can examine which variables are significant predictors of the outcome variable. 
Also, you can find out how each feature impacts the outcome variable. Generally, the model is of the form y hat equals theta zero, plus theta one x_1, plus theta two x_2 and so on, up to theta n x_n. Mathematically, we can show it as a vector form as well. This means it can be shown as a dot product of two vectors; the parameters vector and the feature set vector. 

Generally, we can show the equation for a multidimensional space as **theta transpose** x, where theta is an n by one vector of unknown parameters in a multi-dimensional space, and x is the vector of the featured sets,as theta is a vector of coefficients and is supposed to be multiplied by x. onventionally, it is shown as transpose theta. **Theta is also called the parameters or weight vector of the regression equation.Both these terms can be used interchangeably, and x is the feature set which represents a car.**

For example, x_1 for engine size or x_2 for cylinders, and so on. The first element of the feature set would be set to one, because it turns that theta zero into the intercept or biased parameter when the vector is multiplied by the parameter vector.
**Please notice** *that theta transpose x in a one-dimensional space is the equation of a line, it is what we use in simple linear regression.*

In **higher dimensions** when we have more than one input or x the line is called **a plane or a hyperplane,** and this is what we use for multiple linear regression. 

So, the whole idea is to find the best fit hyperplane for our data. To this end and as is the case in linear regression, we should estimate the values for theta vector that best predict the value of the target field in each row. To achieve this goal, we have to minimize the error of the prediction. 

**Now, the question is, how do we find the optimized parameters?**

### Using MSE to expose the errors in the model 

![2020-01-24_114239](https://user-images.githubusercontent.com/46414243/73059599-baebec80-3e9e-11ea-98ea-75d8800a3f36.png)

To find the optimized parameters for our model, **we should first understand what the optimized parameters are, then we will find a way to optimize the parameters.**

**In short, optimized parameters are the ones which lead to a model with the fewest errors.**

Let's assume for a moment that we have already found the parameter vector of our model, it means we already know the values of theta vector.

Now we can use the model and the feature set of the first row of our dataset to predict the CO_2 emission for the first car, correct? 
If we plug the feature set values into the model equation, we find y hat. 

Let's say for example, it returns 140 as the predicted value for this specific row, what is the actual value? 
Y equals 196.

How different is the predicted value from the actual value of 196? Well, we can calculate it quite simply as 196 subtract 140,which of course equals 56. This is the error of our model only for one row or one car in our case. 

As is the case in linear regression, we can say the error here is the distance from the data point to the fitted regression model. 
The mean of all residual errors shows how bad the model is representing the data set, it is called the mean squared error, or MSE. 
Mathematically, **MSE** can be shown by an equation. While this is not the only way to expose the error of a multiple linear regression model,**it is one of the most popular ways to do so.** 
The best model for our data set is the one with minimum error for all prediction values. 
So, the objective of multiple linear regression is to minimize the MSE equation. 

**To minimize it, we should find the best parameters theta, but how?**

### Estimation multiple linear regression parameters

![2020-01-24_114406](https://user-images.githubusercontent.com/46414243/73059716-f981a700-3e9e-11ea-85f7-2341d399a4b5.png)

Okay, how do we find the parameter or coefficients for multiple linear regression? There are many ways to estimate the value of these coefficients. However, **the most common methods are the ordinary least squares and optimization approach.**

**Ordinary least squares** tries to estimate the values of the coefficients by minimizing the mean square error. **This approach uses the data as a matrix and uses linear algebra operations to estimate the optimal values for the theta.**

**The problem with this technique** is the time complexity of calculating matrix operations as it can take a very long time to finish.
When the number of rows in your data set is less than 10,000, you can think of this technique as an option. However, for greater values, you should try other faster approaches.

**The second option** is to use an optimization algorithm to find the best parameters. 
That is, you can use a process of optimizing the values of the coefficients by iteratively minimizing the error of the model on your training data. For example, you can use gradient descent which starts optimization with random values for each coefficient,then calculates the errors and tries to minimize it through y's changing of the coefficients in multiple iterations. 

**Gradient descent is a proper approach if you have a large data set.**

**After you find the best parameters for your model, you can go to the prediction phase.** After we found the parameters of the linear equation, making predictions is as simple as solving the equation for a specific set of inputs.

### Making predictions with multiple linear regression

![2020-01-24_114537](https://user-images.githubusercontent.com/46414243/73059831-351c7100-3e9f-11ea-9f56-4a77c2081108.png)

Imagine we are predicting CO_2 emission or Y from other variables for the automobile in record number nine. Our linear regression model representation for this problem would be y hat equals theta transpose x.Once we find the parameters, we can plug them into the equation of the linear model. For example, let's use theta zero equals 125, theta one equals 6.2, theta two equals 14, and so on. 

If we map it to our data set, we can rewrite the linear model as CO_2 emissions equals 125 plus 6.2 multiplied by engine size, plus 14 multiplied by cylinder, and so on.As you can see, multiple linear regression estimates the relative importance of predictors. For example, it shows cylinder has higher impact on CO_2 emission amounts in comparison with engine size. Now, let's plug in the ninth row of our data set and calculate the CO_2 emission for a car with the engine size of 2.4. So, CO_2 emission equals 125 plus 6.2 times 2.4, plus 14 times four, and so on. 

### Q&A - on multiplue linear regression

Now, let me address some concerns that you might already be having regarding multiple linear regression. 

As you saw, you can use multiple independent variables to predict a target value in multiple linear regression. It sometimes results in a better model compared to using a simple linear regression which uses only one independent variable to predict the dependent variable. 

**Now the question is how, many independent variable should we use for the prediction? Should we use all the fields in our data set? Does adding independent variables to a multiple linear regression model always increase the accuracy of the model?** 

Basically, **adding too many independent variables without any theoretical justification may result in an overfit model.** An **overfit model** is a real problem because it is too complicated for your data set and not general enough to be used for prediction. So, it is recommended to avoid using many variables for prediction. There are different ways to avoid overfitting a model in regression.

**The next question is, should independent variables be continuous?** 

**Basically, categorical independent variables can be incorporated into a regression model by converting them into numerical variables.**

For example, given a binary variables such as car type, the code dummy zero for manual and one for automatic cars. 

**As a last point, remember that multiple linear regression is a specific type of linear regression.So, there needs to be a linear relationship between the dependent variable and each of your independent variables. There are a number of ways to check for linear relationship. For example, you can use scatter plots and then visually checked for linearity.** 

If the relationship displayed in your scatter plot is not linear, then you need to use **non-linear regression.**
