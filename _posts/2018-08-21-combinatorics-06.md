---
layout: post
title: "Combinatorics 06"
tags: [Combinatorics]
---

## Problem

Let $$1\leq k\leq n$$ and consider all $$k$$-subsets of $$\{1,2,\ldots,n\}$$. Each of these subsets has a smallest member. Let $$\mathcal{F}(n,k)$$ denote the arithmetic mean of these smallst numbers. Prove that $$\mathcal{F}(n,k) = \frac{n+1}{k+1}.$$

## Solution

Given an integer $$i$$, the number of $$k$$-subsets having the smallest number $$i$$ is $${n-i \choose k-1}$$. Then 

$$
\begin{aligned}
\mathcal{F}(n,k) &= \frac{1}{ {n \choose k} }\sum\limits_{i=1}^{n-k+1}i{n-i \choose k-1}\\
&=\frac{1}{ {n\choose k} }\sum\limits_{j=0}^{n-k}{n-j\choose k}\\
&={n+1\choose k+1}\bigg/{n\choose k}=\frac{n+1}{k+1}
\end{aligned}
$$