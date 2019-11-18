---
layout: post
title: Classification Project
---
Summary of Classification Project

For my latest project in the machine learning class, I selected a dataset from Kaggle, selected a predictor variable from the dataset, and used scikit-learn to analyze the data and create a regression function for the predictor variable. I decided to analyze a dataset on California home pricing because the dataset had a large amount of explanatory variables and almost all of these variable were quantitative. I determined that the best variable to predict was the median house value of all properties within one block of the house.

The data needed very little cleaning. All of the explanatory variables made sense to me as factors influencing the median house value so I did not drop any columns. And for the rows, there were very few missing items in the data entire set of data that the easiest thing to do without losing a lot of data was to drop all rows in which there was a missing item. Less than 3% of the original data was lot after dropping all rows with a missing item in at least one of the columns. In order to run a regression, the only other thing I had to do was change my categorical explanatory variable, proximity to the ocean. So, I decided to create a one hot matrix for this categorical variable where the five possible options for category (<1 hour ocean, near bay, near ocean, island, inland) were added as their own columns to the dataset. I am very happy that I decided to use the one hot matrix instead of dropping the column because after I determined each explanatory variable’s correlation with the predictor variable, I found that three of the top four highest correlations were categories from the one hot matrix (<1 hour ocean, near bay, and near ocean).

For analyzing the data, I first plotted a histogram of the predictor variable (median house value) to determine if a transformation was necessary. The histogram displayed a relatively normal distribution with only a slight skew to the right so the log transformation which we learned in class did not seem that applicable here.

My next step was using polynomial regression to determine which degree polynomial was the best for running a Ridge cross validation. The program fit polynomials of various degree to the data and found that the mean squared error of the regression was minimized when polynomial was of degree three. 

My finally applied standard scaler and polynomial regression for the third degree in a pipeline to all of the quantitative data before running Ridge CV. I used alphas of size 0.0001, 0.001, 0.01, 0.1, 1, 10 and found that the best alpha was 10 and it had a corresponding R-Squared value of 0.7388059351489531.

Even though it is only a cubic function, the model I created has several hundred coefficients. Even though there are only 13 explanatory variables (including the one hot matrix), there are so many coefficients because there is one for every single multiplication combination of the variables which results in a degree that is 3 or less. If there were just two explanatory variables, named A and B, there would still have to be a coefficient for A, A^2, A^3, B, B^2, B^3, A x B, A^2 x B, and A x B^2 (9 coefficients total). Thus, when there are 13 explanatory variables in a cubic polynomial, there will have to be many coefficients to cover all of these potential combinations which are of degree three or less.

You can find my code located in my repository [here](https://github.com/jonahsong/REGRESSION_PROJECT)