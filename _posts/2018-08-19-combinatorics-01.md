---
layout: post
title: "Combinatorics 01"
tags: [Combinatorics]
---

## Problem

Prove that $$\lfloor\sqrt{\lfloor{x}\rfloor}\rfloor = \lfloor\sqrt{x}\rfloor$$ for any real number $$x$$.

## Solution

It's clearly that there exist a positive integer n, s.t.

$$
\begin{aligned}
& n^2\leq\lfloor{x}\rfloor\leq x < {(n+1)}^2\\
\Rightarrow & n\leq \sqrt{\lfloor{x}\rfloor} \leq \sqrt{x} < n+1\\
\Rightarrow & n\leq \lfloor\sqrt{\lfloor{x}\rfloor}\rfloor \leq \lfloor\sqrt{x}\rfloor < n+1
\end{aligned}
$$

Hence $$n = \lfloor\sqrt{\lfloor{x}\rfloor}\rfloor = \lfloor\sqrt{x}\rfloor$$