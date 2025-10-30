I understand. I'll rewrite the notes with all formulas using single dollar signs with no spaces (like $formula$) instead of double dollar signs.

# Covariance and Correlation

## Introduction

Covariance and correlation are key concepts in probability and statistics, especially when working with data, machine learning, and fitting models. Correlation appears in many contexts (e.g., principal component analysis, singular value decomposition), and is essentially a normalized version of covariance. Covariance quantifies the joint dependence between two variables $X$ and $Y$.

## Covariance Definition

The **covariance** of two random variables $X$ and $Y$ measures how much the variables change together. Formally:
- Covariance of $X$ and $Y$:
  $\mathrm{Cov}(X,Y)=\mathbb{E}[(X-\mu_X)(Y-\mu_Y)]$
  where $\mu_X$ is the expected value (mean) of $X$, and $\mu_Y$ is the expected value of $Y$.

- For $X$ with itself:
  $\mathrm{Cov}(X,X)=\mathrm{Var}(X)$

## Covariance Calculation Property

Expanding the definition gives a useful shortcut:
- $\mathrm{Cov}(X,Y)=\mathbb{E}[XY]-\mathbb{E}[X]\mathbb{E}[Y]$

If $X$ and $Y$ are independent, then $\mathbb{E}[XY]=\mathbb{E}[X]\mathbb{E}[Y]$, so:
- $\mathrm{Cov}(X,Y)=0$

(But the converse is not always true: zero covariance does not always imply independence.)

## Counterexample: Dependent but Uncorrelated

Let $X$ be uniform on $\{-1,0,1\}$ and $Y=X^2$. Then $X$ and $Y$ are dependent, but $\mathrm{Cov}(X,Y)=0$.

## Variance of a Sum

For $Z=X+Y$:
- $\mathrm{Var}(Z)=\mathrm{Var}(X)+\mathrm{Var}(Y)+2\,\mathrm{Cov}(X,Y)$

If $X$ and $Y$ are independent, $\mathrm{Cov}(X,Y)=0$, so:
- $\mathrm{Var}(Z)=\mathrm{Var}(X)+\mathrm{Var}(Y)$

## Interpreting Covariance

- Large positive covariance: when $X$ is above its mean, $Y$ tends to be above its mean.
- Large negative covariance: when $X$ is above its mean, $Y$ tends to be below its mean.
- Covariance near zero: no linear dependence between $X$ and $Y$.

## Correlation Definition

Correlation is a normalized covariance:
- $\mathrm{Corr}(X,Y)=\frac{\mathrm{Cov}(X,Y)}{\sigma_X\sigma_Y}$
  where $\sigma_X$ and $\sigma_Y$ are the standard deviations of $X$ and $Y$.

- Alternative notation: $\sigma_{XY}$ for covariance, so correlation is $\frac{\sigma_{XY}}{\sigma_X\sigma_Y}$.

## Linearity Property

If you linearly transform $X$ and $Y$ (e.g., $aX+b$ and $cY+d$), correlation remains unchanged:
- $\mathrm{Corr}(aX+b,cY+d)=\mathrm{Corr}(X,Y)$

However, covariance will change with scaling.

## Summary of Key Formulas

- Covariance:
  $\mathrm{Cov}(X,Y)=\mathbb{E}[(X-\mu_X)(Y-\mu_Y)]$
  $\mathrm{Cov}(X,Y)=\mathbb{E}[XY]-\mathbb{E}[X]\mathbb{E}[Y]$
  
- Variance as covariance:
  $\mathrm{Var}(X)=\mathrm{Cov}(X,X)$
  
- Variance of sum:
  $\mathrm{Var}(X+Y)=\mathrm{Var}(X)+\mathrm{Var}(Y)+2\mathrm{Cov}(X,Y)$
  
- Correlation:
  $\mathrm{Corr}(X,Y)=\frac{\mathrm{Cov}(X,Y)}{\sigma_X\sigma_Y}$
  
- Invariance under linear transformation:
  $\mathrm{Corr}(aX+b,cY+d)=\mathrm{Corr}(X,Y)$
