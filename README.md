# Ames Housing Data

## Using features of houses, I will develop a model to predict the prices of houses in Ames, Iowa.

Knowing whether a feature is added or excluded from the model can help homeowners decide 
whether or not the feature adds to their property value and whether or not they want to invest in it.

This model can also help potential home buyers estimate the price of a house with all the features that they want in it
so they can determine whether or not a home may be in their budget.

## Types of models:

I tested out three different models: Linear, Lasso, and Ridge Regression.
Success was evaluated based off of R^2 and root mean squared error (RMSE) scores. 
A dummy model was created to evaluate the baseline, and my models were compared against it.
I used cross validation to find the best alphas for the Lasso and Ridge models.

## Features:
When testing my models, I included all housing features. Then I kept only features that were strongly
correlated with sale price. This reduced the number of features from 397 to 81.

## Findings:
My dummy model had a baseline of a testing R^2 of -0.0007 and a RMSE of 40 cents.

I found that the Linear Regression model performed the worst, with a testing R^2 score in the negatives.
The RMSE indicated that my prices were off by $108096602256.

My Lasso and Ridge models performed similarly, with testing R^2 scores of 0.878 and 
0.890, respectively. Both models had RMSE of about 13 cents. They both performed much better 
than the dummy model.

Finally, I removed almost 80% of the features and fit it to the Lasso model. I found that with these 
81 features, my model still performed just as well as the models with all the features. 
This model with reduced features had a testing R^2 of 0.866 and an RMSE of 14.7 cents.
It even performed very slightly better on the Kaggle competition than the original Lasso model.

## Conclusions:
I was able to build a model to predict the housing prices of Ames, Iowa. 
If I were to recommend renovations to current home owners, I would suggest to just focus on the features
that were strongly correlated with housing price.
