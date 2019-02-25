# Regression: Cheat Sheet

**Assumptions**:
* Linearity
  * The underlying function connecting the independent variable to the dependent variable is indeed linear.
  * **Check**: scatter plot of dependent vs. independent variable

* Constant Variance (Homoscedasticity)
  * implies that the error terms have the same variance no matter where they appear along the regression line.
  * **Check**: A scatter plot of the standardized predicted values vs the standardized residuals

  ![homoscedasticity](https://i.stack.imgur.com/Cc2x4.png)

* Normality
  * the error terms are drawn from an identical Gaussian distribution at each value of the explanatory variable. In other words, we assume a normal distribution of the dependent variable for each value of the independent variable.
  * **Check**: Normal Probability Plot.

* Independent Errors
  * the residual value for an arbitrary observation is not predictable from knowledge of another observation’s residual value; they are uncorrelated.
  *  **Check**: If all the errors obey the same distribution, we should obtain the same (or very similar) PDF (probability density function) plot when we randomly choose a (large enough) subset from the
observations.

### Simple linear regression

$$Y \approx \beta_0 + \beta1 X + \epsilon$$

In order to regress Y onto X, we need to estimate two coefficients/parameters:
* $\beta_0$: The intercept of the line; the expected value of Y when X is 0.
* $\beta_1$: The slope of the line; the expected change in Y when X shifts by one unit.
* $\epsilon$: is called the error term. This represents the deviation of the value
from the linearity.

#### Resitual

The difference vecor in a space of samples is the resitual:
$$e = Y - (\hat{\beta}_0 + \hat{\beta}_1 X)$$

We call the difference between the ith observed response (the actual value) and the ith response prediction (the estimated value) the ith residual

$$e_i = y_i - \hat{y_i}$$

We would like the residual to be as small as possible for all observations in our dataset. This is essentially an optimization problem where we would like to minimize error as much as possible

$$RSS = \sum_{i=1}^{n}{e^2_i}$$
$$=$$
$$RSS = \sum_{i=1}^{n}{(y_i - \hat{y_i})^2}$$
$$=$$
$$RSS = \sum_{i=1}^{n}{(y_i - \hat{\beta_0} - \hat{\beta_1} x_i})^2$$

#### Estimating the coefficients
Our goal now becomes to find the minimum point of $RSS(\beta)$

The model is denoted as

$$\hat{Y} = \hat{\beta}_1 + \hat{\beta}_0 X$$

The coefficients are called the ordinary least square estimator (OLS).

$$\hat{\beta}_1 = \frac{\sum_{i=1}^{n}{(x_i - \bar{x})(y_i - \bar{y})}}{\sum_{i=1}^{n}{(x_i - \bar{x})^2}}
$$

Conceptually this is the same as the following:

$$\beta_1 = \frac{cov(x,y)}{var(x)}$$

$$\hat{\beta}_0 = \bar{y} - \hat{\beta}_1\bar{x} $$

Given our data, these are the best estimates for $\beta_0$ and $\beta_1$ as they ensure the sum of the squared vertical distances from the observations to the regression line (i.e., the RSS) is at a minimum.

#### Standard error of coefficients

$$\boxed{{SE}(\hat{\beta}_0)^2 =
\sigma^2
\left[
  \frac{1}{n} + \frac{\bar{x}^2}{\sum_{i=1}^n(x_i-\bar{x})^2}
\right]\text{}}$$

$$
\boxed{
  {SE}(\hat{\beta}_1)^2 =
  \frac{\sigma^2}{\sum_{i=1}^n(x_i-\bar{x})^2}\\[15pt]

\text{where $\sigma^2 = Var(\epsilon)$}
}
$$

**Estimating the standard error ($RSE^2$)**

Residual Standard Error estimates the standard deviation of

$$\hat{o} = RSE = \sqrt{\frac{RSS}{n-p-1}}
$$

$$\hat{SE}  = \frac{RSS}{n - p - 1}$$


#### Deriving Formulas from Calculus
 > $RSS = ...$
 >

##### Interpretation

A $\hat{\beta}_1$ is the estimated rate of change of the conditional mean of Y with respect to x. On average how much you can expect Y to increase upon a change in X.

#### Accuracy of Coefficients

##### Standard Error

SE yield an approximation of how much our estimates vary from the true parameter values:

##### Residual Standard Error

### Transformations

#### The Box-Cox Transformation


#### Assessing the Goodness of Fit

* **Smaller** RSS & RSE values indicate a **better** fit.
* **Larger** RSS & RSE values indicate a **worse** fit

#### TSS

The total sum of squares measures the amount of variability inherent in our dependent variable:

$$TSS = \sum_{i=1}^{n}{(y_i - \bar{y})^2}$$

This is a measure of the total squared deviation of our response
variable from its mean value

#### $R^2$ (The Coefficient of Determination)

A better measure of model fit is to assess the coefficient of determination R2. This value is defined as the proportion of total sample variability in the dependent variable that is explained by the regression model:

$$R^2 = \frac{TSS - RSS}{TSS} = 1- \frac{RSS}{TSS}
$$

$R^2$ will always be bound between 0 and 1, regardless of the units of measurement used for our response variable. And it measures the amount of variance in Y that is predictable from the regression model.

A **higher** $R^2$ value indicates a **better** model fit (i.e., a greater percentage of the variability in the response variable has been explained by the explanatory variable).

#### Adjusted $R^2$

$$\bar{R}^2 = 1 - (1 - R^2)\frac{n-1}{n-p-1}$$
where $p$ is the total number of explanatory variables in the model and n is the sample size
$$\bar{R}^2 = 1 - \frac{RSS/df_e}{TSS/df_t}$$
