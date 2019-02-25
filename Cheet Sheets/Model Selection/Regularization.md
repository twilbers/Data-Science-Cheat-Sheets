# Regularization and Dimension Reduction

Regularization introduces an alternative fitting procedure can be used to increase prediction accuracy and model interoperability.

**Accuracy**
* if there is a linear relationship between response and predictor, then least squares regression tends to have low bias.
* if n $>>$ p (number of observation much bigger than number of features), then least squares regression tend to have a low variance.
* if p > n, then there is no longer a unique least squares coefficient estimate: the variance is infinite so the method cannot be used at all.

By constraining the estimated coefficients, we can often substantially reduce the variance at the cost of a negligible increase in bias.

**Interoperability**

It is often the case that some or many of the variables used in a multiple regression model are in fact not associated with the response. Including such irrelevant variables leads to unnecessary complexity in the resulting model. By removing these variables—that is, by setting the corresponding coefficient estimates to zero—we can obtain a model that is more easily interpreted.

## Forward Stepwise


## Backward Stepwise

## Forward and Backward Stepwise

## Regularization

We cannot use $R^2$ aa metric because it increase monotonically as the number of features increase and the $R^2$ indicates a model that has low training error

## Mallows' $C_P$
For a fitted least squares model containing p predictors, the $C_p$ estimator a fitted least squares model containing p predictors, the $C_p$ estimate

$$C_p=\frac{1}{n} RSS + 2p\hat{\sigma}^2$$
Sometime defines as

$$C_p=\frac{RSS}{\hat{\sigma}^2} - n + 2p$$
