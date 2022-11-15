up:: 
tags:: #compsci #compsci/machinelearning  

# Empirical distribution function

This is a common method for estimating the continuous distribution function (CDF) of a feature.

> [!info]+ Definition
> You have a sample $\zeta = [ x_1 ... x_n ]$ with sample size $n$ and observations $x_1$... Then the empirical function is as follows:
> $$
> F_n(x) = \frac{1}{n}\sum^n_{i=1}I(x_i \leq x)
> $$

It gives equal weight to each data point ($\frac{1}{n}$) for each of the data points, and $I(x_i \leq x)$ is an indicator function that is either 0 or 1 (if $x_i$ is less than $x$). The value of the function at a given point $x$ is the proportion of observations of the sample that are less than or equal to $x$.

---
#### Sources
[An Introduction to the Bootstrap Method | by Lorna Yen | Towards Data Science](https://towardsdatascience.com/an-introduction-to-the-bootstrap-method-58bcb51b4d60)
