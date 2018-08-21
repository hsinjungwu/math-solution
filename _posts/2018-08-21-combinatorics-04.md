---
layout: post
title: "Combinatorics 04"
tags: [Combinatorics]
---

## Problem

Prove that the string "1101" does not occur consecutively in any row of a modulo 2 Pascal's triangle.

## Solution

If there exist the 4 numbers. let they be $${n\choose{k-1}}$$, $${n\choose{k}}$$, $${n\choose{k+1}}$$, $${n\choose{k+2}}$$.

Since $${n\choose{k+1}}$$ is even, we can rewrite 

$$
{n\choose{k+1}} = 2^pm\text{ where } p > 0\text{ and } m \text{ is odd.}
$$

then we have

$$
\begin{aligned}
{n\choose{k+2}} &= 
\frac{2^p(n-k-1)m}{k+2} &\equiv 1 \pmod{2}\\
{n\choose{k}} &= \frac{2^p(k+1)m}{n-k} &\equiv 1 \pmod{2}
\end{aligned}
$$

thus $$k+2=2^pr_1$$ and $$n-k=2^pr_2$$, where $$r_1, r_2$$ are both odd.

If not, suppose $$r_1$$ is even then $$n-k-1$$ is even, so $$n-k$$ is odd. (contradiction!!)

Similarly when $$r_2$$ is even, we still have the contradition.

So by discuss above, 

$$
\begin{aligned}
1\equiv {n\choose{k-1}} &= \frac{2^p(k+1)km}{(n-k)(n-k+1)}\\
&= \frac{(2^pr_1-1)(2^pr_1-2)m}{r_2(2^pr_2+1)}\\
&= 2\times\frac{(2^pr_1-1)(2^{p-1}r_1-1)m}{r_2(2^pr_2+1)} \equiv 0 \pmod{2}
\end{aligned}
$$

,we have contradition.