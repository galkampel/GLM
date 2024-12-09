# GLM
* In this repository I am usnig the GLM framework for regression and classification modeling and making them Bayesian via PyMC and Bambi packages.

## Classification Tasks
* GLM enables modeling binary classification and multiclass classificaiton
  * Binary classification- Logistic Regression, Bernoulli/Binomial Regression
  * Multiclass classificaiton- Categorical/Multinomial Regression

## Count Regression Tasks
* Motivation- there are cases where we care about predicting discrete values (e.g., demand, count number of events...)
* Count Regression- Poisson Regression 

### Zero Inflated Distribtution
* Motivaiton- in cases where we have many zero values, we can treat the distribution as a multimodal distribution, which can be represented by two consecutive processes:
  * Bernoulli process which helps us to choose the "right" distribution (out of two)
  * "Standard" distribtution w.p. $p$ (e.g., Poisson process) and "zero" distribution (i.e., a distribution that gets only zeros) w.p. $1-p$
* ZIP- zero inflated Poisson
* ZINB- zero inflated Negative Binomial

## Overdispersion
* Motivation- there are cases where the variability of the data cannot be captured by the model due to the inherint limitation of the likelihood distribution.
  In order to overcome this problem, we can add variability using __compound distribtutions__- treat the distribution's parameter as a random variable.
* Gamma-Poisson- for Count Regression
* Beta-Binomial- for Binary Classificaion

## Hierarchical Models
* Hierarchical models can help remove random effects (e.g., heteroskedasticity)
* Use partial pooling, where the global paramerers are constraining the local parameters
* There are two main representations of Hierarchical Models:
  * Centered parameterization
  * Non-Centered parameterization
