# MSCS 634 – Lab 4: Regression Analysis with Regularization Techniques

## Overview

This lab is dedicated to studying and applying various regression algorithms through Python programming language and the Scikit-learn library. The main goal is to study how the predictions of regression models are made depending on their type and the way of data representation. The lab is also focused on learning about the role of regularization in controlling the complexity of a model and avoiding overfitting.

A total of five regression models were considered: Simple Linear Regression, Multiple Linear Regression, Polynomial Regression, Ridge Regression, and Lasso Regression. All these models were built and evaluated using the Diabetes dataset. The comparison of their results was done using traditional metrics for assessing the quality of regression algorithms such as MAE, MSE, RMSE, and R².

With the help of this experiment, the relationship between input variables, complexity of the model, and its predictive ability was studied. Visualization of results was also provided.
## Techniques Used

### 1. Simple Linear Regression

Simple Linear Regression was used with BMI as the independent variable and the progression of the diabetes disease as the dependent variable. This technique involves finding the relationship between one input variable and the output.

The simple linear regression model was trained using the training data and tested using the test data. The relationship between BMI and disease progression was visualized by plotting the regression line.

### 2. Multiple Linear Regression

Multiple Linear Regression was used taking into account all ten independent variables from the Diabetes dataset. This method differs from the Simple Linear Regression in the sense that multiple independent variables are considered while predicting the target variable.

This method was used to see whether having additional health parameters in consideration increases the prediction accuracy.
### 3. Polynomial Regression

In this case, the Polynomial Regression algorithm was employed to determine whether there were nonlinear relationships between BMI and diseases. Polynomial models of the second, third, and fourth degrees were created and compared.

This experiment showed how model complexity is affected by increasing the polynomial degree. More complex relationships could be modeled using higher-degree models. However, it is also possible to overfit due to learning patterns in the data that cannot generalize.

### 4. Ridge Regression

The purpose of implementing Ridge Regression was to evaluate the impact of L2 regularization on model performance. It adds a penalty for having large regression coefficients and thus helps manage the complexity of models.

Several different alpha values were used to see how the regularization intensity impacts model predictions. Greater alpha values result in greater coefficient shrinkage; however, too strong regularization causes underfitting.

### 5. Lasso Regression

Lasso Regression was applied with the use of L1 regularization. Compared to Ridge Regression, it shrinks some feature coefficients to zero, which allows performing feature selection.

Several different alpha values were considered to see how the regularization intensity affects model predictions.


## Dataset

The Diabetes dataset was sourced from the Scikit-learn package using `load_diabetes()`.

It has 442 instances and 10 base attributes, namely age, sex, body mass index, blood pressure, and six blood serum test results. The target attribute is the quantitative assessment of diabetes disease progression after a year from the time of the base assessment.

Exploratory analysis of the data was conducted using Pandas.

The data was split into training and test sets with the proportion of 80% to 20%. The same split was used for all the regression models.

## Evaluation Metrics

Four evaluation measures were employed in order to evaluate the model performance:

- **Mean Absolute Error (MAE):** Indicates the average absolute differences between the actual value and the predicted value. The lower the MAE, the better the prediction.
- **Mean Squared Error (MSE):** Indicates the average squared error in prediction. This measure puts higher weight on larger errors of predictions.
- **Root Mean Squared Error (RMSE):** Is the square root of MSE. It shows the prediction error in the same scale as the target variable.
- **R-Squared (R²):** Shows the proportion of the variance in the target variable that can be accounted for by the regression model. The higher the R², the better the prediction.

These measures were utilized to choose the best method among the evaluated ones.

## Key Insights

One useful takeaway point from this lab is that the choice of input variables plays an important role in regression. Simple Linear Regression allows for analyzing the connection between BMI and development of diabetes. Multiple Linear Regression adds several health-related variables to the model, which increases its capacity to learn.

It is also essential to note the connection between the complexity of the model and its generalization ability. Polynomial Regression shows how increasing the degree of a polynomial increases the flexibility of the model. At the same time, higher complexity does not necessarily mean better results; it is necessary to compare the results on training and testing data to see if complexity leads to better predictions or to overfitting.

The regularization tests allowed gaining additional insights related to the control of complexity of models. With Ridge Regression, the coefficients' magnitude was decreased, whereas Lasso Regression was able to delete some features, reducing their coefficient to zero. Different values of alpha were tested for the purpose.

In conclusion, it is necessary to mention the importance of experimenting with different regression techniques and not to assume that a more complex model always gives better results.
## Challenges and Decisions

The first step in the lab was choosing an appropriate independent variable for Simple Linear Regression. BMI was used as the variable since it is a meaningful variable which can be explored in context with diabetes disease progression. In case of Multiple Linear Regression, all ten existing features were used to determine whether additional information will be beneficial.

Another question was to choose the appropriate polynomial degrees. The degrees 2, 3 and 4 were used in order to understand how increased flexibility of the model influences the connection between input variables and output values. It was needed to compare different models while taking into account their training and test performance to identify overfitting.

Choosing the regularization parameters was a part of the lab in case of Ridge and Lasso Regression as well. Several alpha values were tested since it can affect the value of coefficients in a large way. Feature scaling was performed before applying regularized regression.

Interpreting the multiple evaluation measures was also challenging. Even though a model has relatively high R² value, it does not mean that prediction errors are meaningless. That is why all MAE, MSE, RMSE, and R² were considered together.

## Tools and Libraries

The following software tools and libraries have been used:

- **Python:** The programming language that was used to build regression models.
- **Google Colab:** Cloud-based Jupyter notebook where Python programs run.
- **NumPy:** Library for mathematical operations.
- **Pandas:** Library for data analysis, preprocessing, and visualizing the performance of models.
- **Matplotlib:** Library for building graphs.
- **Scikit-learn:** Library for loading data, splitting the data into train-test sets, building regression algorithms, regularization, and evaluating model performance.

## Conclusion

Through this lab, we got the practical opportunity to implement and compare various regression approaches on the basis of the Diabetes dataset. Thus, the Simple Linear Regression showed how to apply a basic method for disease prediction based on the BMI, whereas Multiple Linear Regression allowed us to understand how it is possible to use more input parameters in the prediction algorithm. As for the Polynomial Regression, it helped us understand the connection between the level of model flexibility and the possibility of overfitting. Comparing models with different polynomial degrees, we understood that increasing complexity must be confirmed by better results in testing. Finally, Ridge and Lasso Regression taught us about the regularizations and how different coefficients can affect the results. The experiments with various alpha values highlighted the necessity of choosing the appropriate regularization strength. Also, the evaluation process emphasized the importance of using several performance measures. In particular, MAE, MSE, RMSE, and R² allowed us to make a more objective comparison of the prediction algorithms. In general, this lab helped me understand the basics of regression analysis, the model evaluation, the feature selection, and regularizations. All these techniques are very useful in real life as part of data
