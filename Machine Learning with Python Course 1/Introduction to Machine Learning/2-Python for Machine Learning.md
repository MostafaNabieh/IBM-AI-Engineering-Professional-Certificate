# Python for Machine Learning
### Python libraries for machine learning
**Python** is a popular and powerful general purpose programming language that recently emerged as the preferred language among data scientists.
there are a lot of modules and libraries already implemented in Python, that can make your life much easier.
![2020-01-23_034613](https://user-images.githubusercontent.com/46414243/72950109-0618d900-3d93-11ea-8cdf-f2e2cfe009b8.png)

the Python packages in **the first package is NumPy** which is a math library to work with N-dimensional arrays in Python. It enables you to do computation efficiently and effectively. It is better than regular Python because of its amazing capabilities.For example, for working with arrays, dictionaries,functions, datatypes and working with images you need to know NumPy.

**the second package is SciPy** is a collection of numerical algorithms and domain specific toolboxes, including signal processing, optimization,statistics and much more. SciPy is a good library for scientific and high performance computation.

**Third package is  Matplotlib** is a very popular plotting package that provides 2D plotting, as well as 3D plotting.
is a good asset for data scientists who want to work with real-world problems.

**Pandas library** is a very high-level Python library that provides high performance easy to use data structures.It has many functions for data importing, manipulation and analysis.In particular, it offers data structures and operations for manipulating numerical tables and timeseries.


### More about Scikit-learn( known as sklearn )
**SciKit Learn** is a free Machine Learning Library for the Python programming language.It has most of the classification, regression and clustering algorithms, and it's designed to work with a Python numerical and scientific libraries: NumPy and SciPy. Also, it includes very good documentation. On top of that, implementing machine learning models with SciKit Learn is really easy with a few lines of Python code.
![2020-01-23_040241](https://user-images.githubusercontent.com/46414243/72950953-7b85a900-3d95-11ea-9733-ca349499c56c.png)

Most of the tasks that need to be done in a machine learning pipeline are implemented already in **Scikit** Learn including :
1. pre-processing of data, feature selection,feature extraction,
2. train test splitting, 
3. defining the algorithms, 
4. fitting models, 
5. tuning parameters, 
6. prediction, 
7. evaluation, 
8. and exporting the model.
### Scikit-learn functions
![2020-01-23_041508](https://user-images.githubusercontent.com/46414243/72951447-0ca94f80-3d97-11ea-858f-b01ae514e93e.png)

Basically, machine-learning algorithms benefit from standardization of the dataset. If there are some outliers or different scales fields in your dataset,you have to fix them.The **pre-processing** package of SciKit Learn provides several common utility functions and transformer classes to change raw feature vectors into a suitable form of vector for modeling.

You have to **split your dataset into train and test sets to train your model and then test the model's** accuracy separately. 
SciKit Learn can split arrays or matrices into random train and test subsets for you in one line of code. 

Then you can **set up your algorithm**. For example, you can build a classifier using a support vector classification algorithm. We call our estimator instance CLF and initialize its parameters. 

Now you can train your model with the train set by passing our training **set to the fit method**, the CLF model learns to classify unknown cases.

Then we can use our test set to run **predictions**, and the result tells us what the class of each unknown value is.

Also, you can use the different metrics to **evaluate** your model accuracy. For example, using a confusion matrix to show the results.

And finally, **you save your model**. 


