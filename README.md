# Probabilistic Binary Response Modeling

## Overview

This repository explores the modeling of the probability mass function for a binary response variable (y ∈ {0, 1}) in the presence of a set of observations $x = (x1 , ..., xp )^T ∈ ℝ^p)$ Traditional regression frameworks face challenges in this scenario, including issues like predicted probabilities outside [0,1], potential violations of constant variance, and non-normality of residuals.


To tackle these challenges, the project adopts the perspective of treating the binary response y as a Bernoulli variable. The probability parameter (p) is modeled as a linear combination of predictors using a probit or logit mapping. The problem is then reformulated as modeling the binary response through the equation:

$ Pr(y = 1 | x, \beta) = Φ(x^T \beta) $
![Probability Equation](https://latex.codecogs.com/svg.latex?Pr(y%20=%201%20|%20x,%20\beta)%20=%20\Phi(x^T%20\beta))


The primary goal is to infer the parameter vector \( \beta = (\beta_1, \ldots, \beta_p)^T ∈ ℝ^p \) from the available data.

## Methods

### 1. Frequentist Approach

This method utilizes Fisher Scoring for parameter estimation. Fisher Scoring is an iterative optimization algorithm that maximizes the likelihood function. The code for this approach is structured to provide efficient and accurate estimates of the parameter vector β.

### 2. Bayesian Approach

The second method employs Bayesian Statistics, leveraging data augmentation to obtain conjugate posteriors. This approach allows for the modeling of uncertainty in parameter estimates and facilitates a more comprehensive understanding of the parameter space. Sampling techniques like Gibbs Sampler are used to explore the posterior distribution of the parameters.

## Requirements

Make sure you have the following dependencies installed:

- Python 3.x
- [NumPy](https://numpy.org/)
- [SciPy](https://www.scipy.org/)

Feel free to reach out if you have any questions or suggestions!
