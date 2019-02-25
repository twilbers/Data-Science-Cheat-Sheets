# Cheat Sheet: Statistics

## Descriptive Statistic

### Population mean
$$
  \boxed{\mu = \frac{1}{n} \sum_{i=1}^{n}{x_i}}

$$
*Note*: the mean is not robust to outliers

### Variance

The average squared distance from the mean

$$
\sigma^2 = \frac{1}{n} \sum_{i=1}^{n}{x_i -\mu_x}^2
$$

#### Variance higher dimensions

For a data set D such that $D = \{x_{1}, \ldots, x_{n}\} x_{i} \in \!R^{D}$
$$\boxed{var[D] = \frac{1}{N}\sum_{i=1}^{N}(x_i-\mu)(x_i-\mu)^T}$$

#### Variance transformations
Variance to the linear transformation of a data set:

$var[A D+b] = A \cdot var[D] A^T$

### Covariance

$$\operatorname{cov}(x, y) =E[(x- \mu_x) (y-\mu_y)]$$

$$\operatorname{cov} (X,Y)=\frac{1}{n}\sum_{i=1}^n (x_i-E(X))(y_i-E(Y))
$$
#### Covariance matrix

$\Sigma =
\left[\begin{array}{cc}
    Var(x) & Cov(x,y)\\
    Cov(y,x) & Var(y)
\end{array}\right]$

$n$-dimensional case:

$$\Sigma
= \begin{bmatrix}
 \operatorname{E}[(X_1 - \mu_1)(X_1 - \mu_1)] & \operatorname{E}[(X_1 - \mu_1)(X_2 - \mu_2)] & \cdots & \operatorname{E}[(X_1 - \mu_1)(X_n - \mu_n)] \\ \\
 \operatorname{E}[(X_2 - \mu_2)(X_1 - \mu_1)] & \operatorname{E}[(X_2 - \mu_2)(X_2 - \mu_2)] & \cdots & \operatorname{E}[(X_2 - \mu_2)(X_n - \mu_n)] \\ \\
 \vdots & \vdots & \ddots & \vdots \\ \\
 \operatorname{E}[(X_n - \mu_n)(X_1 - \mu_1)] & \operatorname{E}[(X_n - \mu_n)(X_2 - \mu_2)] & \cdots & \operatorname{E}[(X_n - \mu_n)(X_n - \mu_n)]
\end{bmatrix}$$

### Corolation

$$\rho = \frac{\sum_{i=1}^{n}{(x_i -\mu_x)}{(y_i-\mu_y)}}{n\sigma_x\sigma_y}$$


### Hypothesis Testing

#### T-Test
##### One sample

Objective: To examine	the	average	difference	between	a	sample	and	the	known	value	of	the	population	mean

Assumptions:
* The	population	from	which	the	sample	is	drawn	is	normally	distributed.
* Sample	observations	are	randomly	drawn	and	independent.

$$t* = \frac{(\bar{x} -\mu_0)}{s/\sqrt{n}} \sim t_n-1$$

Compare	the	test	statistic	value	with	a	standard	table	of	t-values	to
determine	whether	the	test	statistic	surpasses	the	threshold	of	statistical
significance	(yielding	a	significant	p-value).


* Two sample: To	examine	the	average	difference	between	two	samples	drawn	from two	different	populations.

$$t* = \frac{(\bar{x}_1 -\bar{x}_2)}{\sqrt{\frac{s^2_1}{n_1}+\frac{s^2_2}{n_2}}} \sim t_{n1+n_2}-2$$

#### F-Test

* To	assess	whether	the	variances	of	two	different	populations	are	equal.

$$F* = \frac{s^2_1}{s^2_2} \sim F_{n1-1,n_2-1}
$$

#### One-Way ANOVA

#### $\chi^{2}$ Test

**Objective**: To	test	whether	two	categorical	variables	are	independent.
