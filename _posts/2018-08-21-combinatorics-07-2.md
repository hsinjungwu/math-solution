---
layout: post
title: "Combinatorics 07-2"
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

Only do `=>` part, the other is easy.

### Claim <1>

> If $$n$$ is even, say $$n=2k$$, and $$n>6$$, then $$d_{k}(n)>1$$.

**Proof:**

If not, then there exist some $$k$$ such that 

$$
\begin{aligned}
&\quad &\frac{(2k)!}{k!k!} - \frac{(2k)!}{(k+1)!(k-1)!} &= 1\\
&\Rightarrow &\frac{(2k)!}{k!(k-1)!} &= k(k+1)\\
&\Rightarrow &(2k)! &= k!(k+1)!\\
&\Rightarrow &\prod\limits_{i=1}^{k}(k+i) &= \prod\limits_{i=1}^{k}(1+i)
\end{aligned}
$$
        
, but $$k > 1 \Rightarrow\!\Leftarrow.$$

----

### Claim <2>

> For $$n>6$$, $$d_k(n) > n-1$$ where $$1 < k \leq \lfloor\frac{n-1}{2}\rfloor$$

**Proof:**

Use induction on $$n$$

1. $$n=7$$, easy
2. Suppose $$n$$ holds, then

$$
\begin{aligned}
d_k(n+1) &= {n+1 \choose k} - {n+1 \choose k-1}\\ 
&= \bigg( {n\choose k} + {n\choose k-1} \bigg) - \bigg( {n\choose k-1} + {n\choose k-2} \bigg)\\
&= \bigg( {n\choose k} - {n\choose k-1} \bigg) + \bigg( {n\choose k-1} - {n\choose k-2} \bigg)\\
&= d_{k}(n) + d_{k-1}(n) 
\end{aligned}
$$

If $$1 < k \leq \lfloor\frac{n-1}{2}\rfloor$$, by induction we have

$$
d_{k}(n+1) = d_{k}(n) + d_{k-1}(n) \geq 2(n-1) = n+(n-2) > n
$$

, the equality part is for $$k=2$$.

Otherwise, $$\lfloor\frac{n-1}{2}\rfloor < k \leq\lfloor\frac{n}{2}\rfloor$$, that means $$n=2k$$. Hence by induction and *claim <1>*, we have

$$
d_{k}(n+1) = d_{k}(n) + d_{k-1}(n) > 1 + n-1 = n.
$$

----

### Claim <3>

> If $$n$$ is even, say $$n=2k$$, and $$n>6$$, then $$d_{k}(n)\neq n-1$$.

**Proof:**

If not, then there exist some $$k>3$$ such that $$d_{k}(n)=n-1$$. Then

$$
\begin{aligned}
&\quad&\frac{(2k)!}{k!k!} - \frac{(2k)!}{(k+1)!(k-1)!} &= 2k-1\\
&\Rightarrow &\frac{(2k)!}{k!(k-1)!} &= (2k-1)k(k+1)\\
&\Rightarrow &2(2k-2)! &= (k+1)!(k-1)!\\
&\Rightarrow &\prod\limits_{i=0}^{k-2}(k+i) &= \prod\limits_{i=0}^{k-2}(3+i)
\end{aligned}
$$

, but $$k > 3 \Rightarrow\!\Leftarrow.$$

----

### Finally

By *claim <2>*, it's clearly that $$d_{k}(n) > n-1$$, whenever $$n > 6$$, for $$\lceil\frac{n+1}{2}\rceil\leq k < n.$$

Hence by *claim <2>* and *claim <3>* we have $$d_{k}(n) \neq n-1$$, whenever $$n > 6$$, and when n = 2,3,5, it's easy to check that $$d_k(n) = n-1$$ only if $$k=1$$ or $$k=n$$.