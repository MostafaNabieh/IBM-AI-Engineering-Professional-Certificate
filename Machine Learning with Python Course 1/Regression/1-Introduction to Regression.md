# Introduction to Regression

### What is regression ?
Let's assume we have some historical data from different cars,and assume that a car such as,in row nine has not been manufactured yet,but we're interested in estimating its approximate CO_2 emission, after production.Is it possible?

![2020-01-23_152152](https://user-images.githubusercontent.com/46414243/72987991-2036d380-3df4-11ea-9851-7cb69e82b321.png)

We can use regression methods to predict a continuous value such as CO_2 emission,using some other variables.Indeed, regression is the process of predicting a continuous value.In regression, there are two types of variables,a **dependent variable**, and one or more **independent variables**.

The **dependent variable**, can be seen as the **state,target, or final goal** we study,and try to predict,and the **independent variables**,also known as **explanatory variables,can be seen as the causes of those states.**


The **independent variables** are shown conventionally by **X**,and the **dependent variable** is notated by **Y**.
Our regression model relates Y,or the dependent variable,to a function of X .
The **independent variables**.The **key point in the regression**,is that our **dependent value should be continuous and cannot be a discrete value.**
However, the **independent variable or variables,can be measured on either a categorical,or continuous measurement scale.**

### What is a regression model ?
So, what we want to do here is to use the historical data of some cars,using one or more of their features and from that data, make a model.We use regression to build such a regression estimation model,then the model is used to predict the expected CO_2 emission for a new, or unknown car.
![2020-01-23_152310](https://user-images.githubusercontent.com/46414243/72988084-4a889100-3df4-11ea-91b8-e60dfc98fdb6.png)

### Types of regression models
Basically, there are **two types of regression models.Simple regression, and multiple regression.**

**Simple regression is when one independent variable is used to estimate a dependent variable.** It can be either linear, or non-linear.
For example, predicting CO_2 emission using the variable of engine size.
Linearity of regression, is based on the nature of relationship between independent and dependent variables.

**When more than one independent variable is present, the processes is called multiple linear regression.** For example, predicting CO_2 emission using engine size,and the number of cylinders in any given car. Again, depending on the relation between dependent and independent variables,it can be either linear or nonlinear regression.
![2020-01-23_152504](https://user-images.githubusercontent.com/46414243/72988238-8e7b9600-3df4-11ea-8cce-e6efedd78eb9.png)


### Applications of regression
Essentially, we use regression when we want to estimate a continuous value. 
For instance, one of the applications of regression analysis could be in the area of sales forecasting. You can try to predict a salesperson's total yearly sales from independent variables, such as age, education, and years of experience. It can also be used in the field of psychology for example, to determine individual satisfaction based on demographic and psychological factors. 

![2020-01-23_152857](https://user-images.githubusercontent.com/46414243/72988583-2e392400-3df5-11ea-961e-9dec221688b5.png)

We can use regression analysis to predict the price of a house in an area, based on its size, number of bedrooms, and so on.

We can even use it to predict employment income, for independent variables such as hours of work, education, occupation, sex age, years of experience, and so on. 

Indeed you can find many examples of the usefulness of regression analysis in these and many other fields, or domains such as finance, healthcare, retail, and more.

### Regression algorithms
We have many regression algorithms. 
Each of them has its own importance, and a specific condition to which their application is best suited.

![2020-01-23_153006](https://user-images.githubusercontent.com/46414243/72988658-59bc0e80-3df5-11ea-81ba-868ee344e5b7.png)




