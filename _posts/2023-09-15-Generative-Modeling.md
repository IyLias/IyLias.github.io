---
layout: post
comments: true
use_math: true
title:  "Generative Modeling"
date:   2023-09-15 
categories: [gan]
---


## Generative Modeling Framework

1.  We have sample dataset X

2. Suppose sample is generated from unknown distribution, $p_{data}$

3. Generative Model $p_{model}$ tries to mimic $p_{data}$. If done, you can generate a sample that appears to have been drawn from the $p_{data}$.


    <U>Which means $p_{model}$ is approximating real distribution $p_{data}$. </U>


    The true probability density function $p_{data}$, assuming it generated the observed dataset, is only one, but there are infinitely many probability density functions $p_{model}$ that can be used to estimate $p_{data}$.



<br>

## Parametric Model


We use parametric model $p_\theta(x)$ to find proper $p_{model}(X)$.





<br>

## Likelihood

The likelihood L($\theta$|$x$) estimates proper $\theta$ value when given sample point x.

So we define 

L($\theta$|$x$) = $p_\theta(x)$


When given whole dataset $X$ with independent samples, 

L($\theta$|$x$) = $\prod_{x \in X} p_\theta(x)$

we usually use log-likelihood instead..

L($\theta$|$x$) = $\sum_{x \in X} log p_\theta(x)$


<br>

## Maximum Likelihood Estimation


It is a method to find the estimate $\hat\theta$ that best describes the observed data $X$ from the parameter set theta of the probability density function $p_\theta(x)$.


$\hat\theta$ = $argmax_\theta$  L($\theta$ | $X$)




<br>

## Naive Bayes Model

It is based on applying strong independence assumptions between features.
Thus it assumes that each feature $x_j$ is independent from any other feature $x_k$.

$p(x_j|x_k)$ = $p(x_j)$


So for K features, we can reduce to 

$p(x)$ = $\prod_{i=1}^K p(x_k)$


Therefore, the Naive Bayes Model learns a structure from data and can use it to generate new samples that were not in the original dataset.


But when dealing with pixel features like in computer vision, it's not proper to use. 



<br><br>

## Representation Learning

Representation learning is a process in machine learning where algorithms extract meaningful patterns from raw data to create representations that are easier to understand and process.

