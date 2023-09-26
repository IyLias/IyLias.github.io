---
layout: post
comments: true
use_math: true
title:  "Complete Graph and Complement"
date:   2023-09-24
categories: [math]
---


## Complete Graph

A graph $G$ is complete if every two distinct vertices of G are adjacent.

A complete graph of order n is denoted by $K_n$

Therefore $K_n$ has the maximum possible size for a graph with n vertices. Since every 
two distinct vertices of $K_n$ are joined by an edge, the number of pairs of vertices in $K_n$ is $\binom{n}{2}$ = $\frac{n(n-1)}{2}$





<br><br>

## Complement

The complement $\bar G$ of a graph $G$ is that graph whose vertex set is $V(G)$ 
and such that for each pair $u,v$ of distinct vertices of $G$, $uv$ is an edge of $\bar G$ if and only if $uv$ is not an edge of $G$.

So if $G$ is a graph of order $n$ and size $m$, then $\bar G$ is a graph of order $n$ and 
size $\binom{n}{2} - m$