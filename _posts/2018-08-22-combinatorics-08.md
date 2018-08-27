---
layout: post
title: "Combinatorics 08"
tags: [Combinatorics]
---

## Problem

For every positive integer $$m$$, prove there exist at least one fibonacci $$F_n$$, $$n>0$$, divisible by $$m$$.

## Solution

Given $$m$$, suppose there is no $$F_n$$ s.t. divisible by $$m$$. Let $$P_n = (R_{n+1}, R_n)$$ for $$n\geq 0$$ , where $$R_i\equiv F_i \pmod{m}$$ and $$R_i\equiv 0 \pmod{m}$$ iff $$i = 0$$.

Then choose the sequence $$\mathcal{S} = \{P_1, P_2, \ldots, P_{ {(m-1)}^2+1 }\}$$, then we know there exist some $$P_i = P_j$$ for $$i < j, P_i, P_j\in \mathcal{S}$$ (By [Pigeonhole Principle](https://en.wikipedia.org/wiki/Pigeonhole_principle))

i.e. $$P_i = (R_{i+1}, R_i) = (R_{j+1}, R_j) = P_j$$, then 

$$
\begin{aligned}
P_{i-1} &= (R_i, R_{i-1})\\
&= (R_i, R_{i+1}-R_i)\\
&= (R_j, R_{j+1}-R_j)\\ 
&= (R_j, R_{j-1})\\
&= P_{j-1}
\end{aligned}
$$

Repeat the progress, we have $$P_0 = P_{j-i} = (1,0)$$. It means $$R_{j-i} = 0$$ but $$j-i > 0, \Rightarrow\!\Leftarrow.$$

Then there exist some $$F_n$$ s.t. divisible by $$m$$.