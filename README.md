### Rock Density XRay Prediction with various models

![boring](https://user-images.githubusercontent.com/86251750/145718479-95dcdfad-e030-4515-a7ed-ae02f1b7b484.jpg)

## Table of CONTENTS 
---------------------
 * [Aim](#aim)
 * [Dataset used](#data)
 * [Exploring the Data](#viz)
   - [Matplotlib](#matplotlib)
   - [Seaborn](#seaborn)
 * [using various models](#using_various_model)
 * [Conclusion](#conclusion)

 

## AIM:<a name="aim"></a>

We just got hired by a tunnel boring company which uses X-rays in an attempt to know rock density, ideally this will allow them to switch out boring heads on their equipment before having to mine through the rock!

They have given us some lab test results of signal strength returned in nHz to their sensors for various rock density types tested. You will notice it has almost a sine wave like relationship, where signal strength oscillates based off the density.

## Dataset Used:<a name="data"></a>

Dataset can be found at my respository.

## Exploring the Data:<a name="viz"></a>

Here I have used matplotlib and seaborn visualization skills.

**Matplotlib:**<a name="matplotlib"></a>
--------
Matplotlib is a Python 2D plotting library which produces publication quality figures in a variety of hardcopy formats and interactive environments across platforms. Matplotlib can be used in Python scripts, the Python and IPython shells, the Jupyter notebook, web application servers, and four graphical user interface toolkits.You can draw up all sorts of charts(such as Bar Graph, Pie Chart, Box Plot, Histogram. Subplots ,Scatter Plot and many more) and visualization using matplotlib.

Environment Setup==
If you have Python and Anaconda installed on your computer, you can use any of the methods below to install matplotlib:

     pip: pip install matplotlib

     anaconda: conda install matplotlib
     
     import matplotlib.pyplot as plt

for more information you can refer to [matplotlib](https://matplotlib.org/) official site

**Seaborn:**<a name="seaborn"></a>
------
Seaborn is built on top of Python’s core visualization library Matplotlib. Seaborn comes with some very important features that make it easy to use. Some of these features are:

**Visualizing univariate and bivariate data.**

**Fitting and visualizing linear regression models.**

**Plotting statistical time series data.**

**Seaborn works well with NumPy and Pandas data structures**

**Built-in themes for styling Matplotlib graphics**

**The knowledge of Matplotlib is recommended to tweak Seaborn’s default plots.**

Environment Setup==
If you have Python and Anaconda installed on your computer, you can use any of the methods below to install seaborn:

    pip: "pip install seaborn"*

    anaconda: " conda install seaborn"*
    import seaborn as sns
    
for more information you can refer to [seaborn](https://seaborn.pydata.org/) official site.

## using various models:<a name="using_various_model"></a>

**Linear Regression**

![download](https://user-images.githubusercontent.com/86251750/145717203-79a61286-ba30-4052-bb70-a9d91268e3be.png)

we can see that the Linear Regression didn't fit our data well thus it can clearly be shown that the model is underfitting

**Polynomial Regression**

Polynomial regression is a form of Linear regression where only due to the Non-linear relationship between dependent and independent variables we add some polynomial terms to linear regression to convert it into Polynomial regression.

Suppose we have X as Independent data and Y as dependent data. Before feeding data to a mode in preprocessing stage we convert the input variables into polynomial terms using some degree.

Consider an example my input value is 35 and the degree of a polynomial is 2 so I will find 35 power 0, 35 power 1, and 35 power 2 And this helps to interpret the non-linear relationship in data.
The equation of polynomial becomes something like this.

                 y = a0 + a1x1 + a2x12 + … + anx1n

The degree of order which to use is a Hyperparameter, and we need to choose it wisely. But using a high degree of polynomial tries to overfit the data and for smaller values of degree, the model tries to underfit so we need to find the optimum value of a degree.

![download](https://user-images.githubusercontent.com/86251750/145717379-8a95d77a-9757-4132-b927-0ce13f7336bd.png)

    with polynomial_feature = 10. I was able to fit my data well and it gives me RMSE : 0.1405023263432936

**KNN Regression**

KNN regression is a non-parametric method that, in an intuitive manner, approximates the association between independent variables and the continuous outcome by averaging the observations in the same neighbourhood. The size of the neighbourhood needs to be set by the analyst or can be chosen using cross-validation to select the size that minimises the mean-squared error or RMSE.

![download](https://user-images.githubusercontent.com/86251750/145717551-ac5d3ee8-583d-48fa-9417-87f5966c244e.png)

    RMSE : 0.13277855732740926
    
** DecisionTree Regression**

![download](https://user-images.githubusercontent.com/86251750/145717588-f4d3362a-83d0-4a7d-a76d-d1d53e7a7372.png)

    From above plot we can clearly see that our model tries to capture data along with Noise thus creating a risk of Overfitting and gives RMSE : 0.152348
    
** Support Vector Regression**

Support Vector Machine can also be used as a regression method, maintaining all the main features that characterize the algorithm (maximal margin). The Support Vector Regression (SVR) uses the same principles as the SVM for classification, with only a few minor differences. First of all, because output is a real number it becomes very difficult to predict the information at hand, which has infinite possibilities. In the case of regression, a margin of tolerance (epsilon) is set in approximation to the SVM which would have already requested from the problem. But besides this fact, there is also a more complicated reason, the algorithm is more complicated therefore to be taken in consideration. However, the main idea is always the same: to minimize error, individualizing the hyperplane which maximizes the margin, keeping in mind that part of the error is tolerated. 

![SVR_2](https://user-images.githubusercontent.com/86251750/145717773-22988387-e08d-43df-9e9d-67f98de1afa9.png)

le's see the plot for SVM

![download](https://user-images.githubusercontent.com/86251750/145717850-72a52b8d-a944-4660-81df-5a4450226d96.png)

      It fits our data quite well and gives us RMSE : 0.12646999302046696

** RandomForest Regression**

![download](https://user-images.githubusercontent.com/86251750/145717913-04887741-ed79-4df6-9f01-cffe75e5f3af.png)

    Model is overfiiting, RMSE : 0.13406031602544485

** Gradient Boosting**

![download](https://user-images.githubusercontent.com/86251750/145717949-dc45fbce-1326-4260-90bd-17ab11b069cf.png)

     RMSE : 0.13294148649584667

** AdaBoost**

![download](https://user-images.githubusercontent.com/86251750/145717975-4b682909-52b8-4619-9ca3-3fa30972fe5e.png)

    RMSE : 0.13294148649584667
    
## CONCLUSION:<a name="conclusion"></a>

I have various Models in which some model shows underfitting and some model shows overfitting But Support Vector Regression provides me good RMSE score and also it didn't
overfit so I have used it as my final model.

***language used***
--------------------------
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

**Tools**
-----------------------
[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)    ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)   ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)  ![Made with matplotlib](https://user-images.githubusercontent.com/86251750/132984208-76ce70c7-816d-4f72-9c9f-90073a70310f.png)  ![seaborn](https://user-images.githubusercontent.com/86251750/132984253-32c04192-989f-4ebd-8c46-8ad1a194a492.png)

