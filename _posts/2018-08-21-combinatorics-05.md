---
layout: post
title: "Combinatorics 05"
tags: [Combinatorics]
---

## Problem

Prove that $$n$$ divides $$2n-2 \choose n-1$$ where $$n\geq1$$ is an integer.

## Solution

1. $$n=1$$ is trivial.
2. Since $${2n-2 \choose n-1} = \frac{n}{n-1}\times{2n-2 \choose n-2}$$ is an integer, where $$n>1$$. We know that $$n-1$$ and $$n$$ are relatively prime, so $$(n-1)\,\bigg\vert {2n-2 \choose n-2}$$, that means

$$
\frac{ {2n-2\choose n-1} }{n} = \frac{ {2n-2 \choose n-2} }{n-1} \in \mathbb{Z}
$$

,hence $$n\,\bigg\vert {2n-2 \choose n-1}$$.
