---
layout: post
title: "Combinatorics 02"
tags: [Combinatorics]
---

## Problem

Prove for positive integers $$m$$ and $$n$$ that

$$
n =\lceil{\frac{n}{m}}\rceil+\lceil{\frac{n-1}{m}}\rceil+\ldots+\lceil{\frac{n-m+1}{m}}\rceil
$$

## Solution

Let $$n = km+r$$, where $$k$$ is a nonegative integer and $$0\leq r < m$$. 

Since $$0 \leq r < m$$, we have

$$
\lceil\frac{r-i}{m}\rceil = 
\begin{cases}
1, &\text{where } 0\leq i\leq r-1\\
0, &\text{where } r\leq i\leq m-1
\end{cases}
$$

for nonegative integer $$i$$.

Then we have 

$$
\begin{aligned}
\sum\limits_{i=0}^{m-1}\lceil\frac{n}{m}\rceil&=\sum\limits_{i=0}^{m-1}\lceil\frac{km+r-i}{m}\rceil\\
&=\sum\limits_{i=0}^{m-1}\big(k+\lceil\frac{r-i}{m}\rceil\big)\\
&=km+\sum\limits_{i=0}^{m-1}\lceil\frac{r-i}{m}\rceil\\
&=km+\sum\limits_{i=0}^{r-1}\lceil{\frac{r-i}{m}}\rceil+\sum\limits_{i=r}^{m-1}\lceil{\frac{r-i}{m}}\rceil\\
&=km+\overbrace{1+\ldots+1}^{r}+\overbrace{0+\ldots+0}^{m-r}\\
&=km+r=n
\end{aligned}
$$