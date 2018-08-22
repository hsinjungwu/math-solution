---
layout: post
title: "Combinatorics 07-1"
tags: [Combinatorics]
---
## Problem

Let $$n$$ and $$k$$ be integers such that $$n\geq 2$$ and $$1\leq k\leq n$$. Define 

$$
d_k(n)=\bigg\lvert{n\choose k}-{n\choose k-1}\bigg\rvert
$$

and 

$$
d_{\min}(n)=\min\{d_k(n)\mid 1\leq k\leq n\}.
$$ 

Prove that

1. $$d_{\min}(n)=0$$ if and only if $$n$$ is odd.
2. For odd $$n$$, $$d_k(n)=0$$ if and only if $$k=(n+1)/2$$.

## Solution of 1

### =>

If $$d_{\min}(n) = 0$$ then $$d_k(n) = 0$$ for some $$k$$. Then

$$
\begin{aligned}
&\quad &{n\choose k} &= {n\choose k-1}\\
&\Rightarrow &(n-k)!k! &= (n-k+1)!(k-1)!\\
&\Rightarrow &k &= (n-k+1)\\
&\Rightarrow &n &= 2k-1
\end{aligned}
$$

, hence $$n$$ is odd.

### <=

If $$n$$ is odd, pick $$k = (n+1)/2$$, then 

$$ 
0 \leq d_{\min}(n) \leq d_k(n) = \bigg\lvert {n\choose k}-{n\choose k-1} \bigg\rvert = 0.
$$

----

## Solution of 2

Similarly as solution 1.