# LINEAR REGRESSION CURIOSITY

This toy jupyter notebook is meant to give a curiosity interpretation/result of the lienar regression given a particular dataframe full of 1 and zeros (with at most only one 1 per rows, otherwise zero). This could be used as questions during interview

## Problem setting
We have three columns named x1, x2, x3. These are binary columns. A row has at most one 1, all the other values are zero. The target column y is fill with random values taken from a guassian of mu  = 50000 and sigma = 10000.

We fit an OLS model with and without the constant value.

## Question
Let's suppose you have a dataset wich each row is a person that could come from the either the north, or the south, or the east, ot the west. Let's state the target column y as the annual income of that person. Let's suppose you have binary columns x1, x2, x3 which are 1 if the person comes from north, south, east respectively. Clearly, if a row is full of zeros, that means the person comes from the west.

1) Let's suppose you want to fit a OLS model WITHOUT the constant term. What do you expect the coefficients associated with the variables to be? 

2) Now, Let's add the constant term. What do you expect the coefficient associated with the constant term to be? What about the other variables?

## Result

1) For instance, the coefficient associated with **x1** should be the mean of the target column suppose x1 == 1. Essentially, **it is the mean of the annual income of all people coming from the north**. The same result hold for the other two variables.

2) The **constant** term is the **mean of the annual income of all the person coming from the west**. The other coefficients then are the differences between each mean calculated above in 1) and the constant term.