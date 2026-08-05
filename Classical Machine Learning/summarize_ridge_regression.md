#What result did the Author try to reach?
This paper resolved a problem that we now call overfitting or it is also called as regularization technique. To be specific, when we train a machine learning model, for the shake of simplicity, I assume a linear regression model. As you may know, we use OLS method to estimate the coefficient (beta), but one of the prerequisite of this method is the features (X) must be independent with each other (in linear algebra, for matrix X, we define it as matrix X must be linear independent). If the model violate it, the model is multicolinearity. It makes the coefficients (the beta) become really sensitive to the fluctuate of the features. This is the major reason of overfitting problem. So the target of the Author is that desensitizing the model in case of multicolinearity (In real datasets, it's very normal)    

#What were the key elements of the approach?
The Author proposed a biased estimator that subtitute for OLS method. It's called Ridge regression
##Loss function of OLS
$$\min_{\beta_0, \beta_1, \dots, \beta_p} \sum_{i=1}^{n} \left( y_i - \left( \beta_0 + \sum_{j=1}^{p} \beta_j x_{ij} \right) \right)^2$$

##Loss function of Ridge regression
$$\min_{\beta_1^*, \dots, \beta_p^*} \sum_{i=1}^{n} \left( y_i - \sum_{j=1}^{p} \beta_j^* x_{ij} \right)^2 + k \sum_{j=1}^{p} (\beta_j^*)^2$$

The target is minimizing the loss function. So the difference of the two formulas show different actions. Briefly, the OLS estimator is unbiased but Ridge regression deliberately add some biased through "k" parameter in formular but this make vector of beta become shorter (or simply be smaller), then the sum of square of (beta_hat - beta) is smaller and variance of it also be smaller. This make the model become more stable and more accurate.

#What can you use yourself?
This paper is the basis of regularization technique using for solving overfitting when training machine learning models

#What other references do you want to follow?
K-Nearest Neighbor is my subsequent paper
