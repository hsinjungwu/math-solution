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

Let 

$$
\text{RHS}=\lceil{\frac{n}{m}}\rceil+\lceil{\frac{n-1}{m}}\rceil+\ldots+\lceil{\frac{n-m+1}{m}}\rceil=\sum\limits_{i=0}^{m-1}\lceil{\frac{n-i}{m}}\rceil
$$

### Case 1

If $$0 \leq n \leq m$$, then for integer $$i$$

$$
\lceil\frac{n-i}{m}\rceil = 
\begin{cases}
1, &\text{where } 0\leq i\leq n-1\\
0, &\text{where } n\leq i\leq m-1
\end{cases}
$$

, so $$\text{RHS}=\sum\limits_{i=0}^{n-1}\lceil{\frac{n-i}{m}}\rceil+\sum\limits_{i=n}^{m-1}\lceil{\frac{n-i}{m}}\rceil = \overbrace{1+\ldots+1}^{n}+\overbrace{0+\ldots+0}^{m-n}=n$$.

### Case 2

If $$n > m$$, let $$n = km+r$$, where $$0\leq r < m$$. 

By case above, we have $$r=\sum\limits_{i=0}^{m-1}\lceil\frac{r-i}{m}\rceil$$, hence

$$
\text{RHS}
=\sum\limits_{i=0}^{m-1}\lceil\frac{km+r-i}{m}\rceil
=\sum\limits_{i=0}^{m-1}\big(k+\lceil\frac{r-i}{m}\rceil\big)
=km+\sum\limits_{i=0}^{m-1}\lceil\frac{r-i}{m}\rceil=km+r=n
$$