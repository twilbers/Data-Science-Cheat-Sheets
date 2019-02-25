## Naive Bayes

### Bayes Theorem

 $$P(Y|X) = \frac{P(X|Y)P(Y)}{P(X)}$$


Deduce Bayes Theorem from joint probabilities
\[
  P(Y, X) = P(Y|X) P(X)\\
  P(Y, X) = P(X|Y) P(Y)\\
  =\\
  \frac{P(Y|X)\sout{P(X)}}{\sout{P(X)}} = \frac{P(X|Y) P(Y)}{P(X)}
\]
</details>

$$P(Y = k|X = x) = \frac{P(X = x|Y = k)P(Y) = k}{\sum_{l}{P(X|Y = l)}P(Y = l)}$$

Prior: $P(Y = k) \approx \frac{n_k}{n}$

Bayes error rate:

### LDA

**Assumptions:**
* The observations within each class $k$ come from a normal distribution with a class-specific mean vector and a common variance $\sigma^2$, and plugging estimates for these parameters into the Bayes classifier.


### QDA
LDA the decision boundry is linear
$\frac{\hat{\mu}_k + \hat{\mu}_2}{2}$
QDA the decision boudry is quadratic
Decision boundry: $P(Y=0|X) = P(Y=1|X)$
