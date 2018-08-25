---
layout: post
title: "Combinatorics 07-2(另一種解法)"
tags: [Combinatorics]
---
## Problem

Let $$n$$ and $$k$$ be integers such that $$n\geq 2$$ and $$1\leq k\leq n.$$ Define 

$$
d_k(n)=\bigg\lvert{n\choose k}-{n\choose k-1}\bigg\rvert
$$

and 

$$
d_{\min}(n)=\min\{d_k(n)\mid 1\leq k\leq n\}.
$$ 

Prove that for $$n$$ different from 4 and 6, $$d_k(n) = n-1$$ if and only if $$k=1$$ or $$k=n.$$

## Solution

Suppose there exist $$k$$ is neither 1 nor $$n$$ s.t. $$d_k(n)=n-1,$$ let $$2\leq k \leq \frac{n}{2}$$, then we can rewrite 

$$
d_k(n)=\frac{n!}{k!(n-k)!} - \frac{n!}{(k-1)!(n-k+1)!} = n-1
$$

as 

$$
\tag{⋆}(n-2k+1)\times n\times(n-2)! = (k!)\times(n-k+1)!
$$

## Case : k = 2

Then the equation $$(\star)$$ becomes $$(n-3)n(n-2)! = 2!(n-1)!$$, hence we have $$n^2 - 5n + 2 = 0$$. However the root $$n$$ is not an integer.(Contradiction!!)

## Case : k = 3

Then the equation $$(\star)$$ becomes $$(n-5)n(n-2)! = 3!(n-2)!$$, hence we have $$n=6$$ is the only one positive solution. However $$n\neq 6.$$(Contradiction!!)

## Case : k > 3 

Then the equation $$(\star)$$ becomes

$$
(n-2k+1)\times n\times\prod\limits_{i=0}^{k-4}(n-k+2+i) = 2k\times\prod\limits_{i=0}^{k-4}(3+i)
$$

Since $$n\geq 2k$$, then $$n-2k+1\geq1,\; n-k+2\geq k+2>3.$$ So we have contradiction:

$$
(n-2k+1)\times n\times \prod\limits_{i=0}^{k-4}(n-k+2+i) > 1\times 2k \times \prod\limits_{i=0}^{k-4}(3+i)
$$

---
By all case above and symmetry we know it's true for $$\frac{n}{2}+1 \leq k \leq n-1.$$

And last case is that $$k = \frac{n+1}{2}$$. Since $$k$$ is integer, it means $$n$$ is odd, and $$d_k(n) = 0$$ by (b).

Hence $$n$$ different from 4 and 6, $$d_k(n) = n-1$$ if and only if $$k =1$$ or $$k = n.$$