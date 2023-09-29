---
layout: post
comments: true
use_math: true
title:  "Degrees of vertex"
date:   2023-09-29
categories: [math]
---



## Degree of a vertex

The degree of a vertex $v$ in a graph $G$ is the number of edges incident with $v$ and is denoted 
by $deg_Gv$.

The set $N(v)$ of neighbors of a vertex $v$ is called the $neighborhood$ of $v$.
Thus $deg \; v$ = $|N(v)|$

A vertex of degree 0 is referred to as an $isolated \;vertex$ and a vertex of degree 1 is an $end-vertex$.

The $minimum \; degree$ of $G$ is the minimum degree among the vertices of $G$ and is denoted by $\delta(G)$. The $maximum \;degree$ of $G$ is denoted by $\Delta(G)$. So if G is a graph of order $n$ and $v$ is any vertex of $G$, then 

$0 \le \delta(G) \le deg \; v \le \Delta(G) \le n-1$


## The First Theorem of Graph Theory

$\sum_{v \in V(G)} deg \; v = 2m$

proof)

When summing the degrees of the vertices of $G$, each edge of $G$ is counted twice, once for each of its two incident vertices.



## Corollary 

<strong>Every graph has an even number of odd vertices.</strong>

proof) 

Let $G$ br a graph of size $m$. Divide $V(G)$ into two subsets $V_1$ and $V_2$, where $V_1$ consists of the odd vertices of $G$ and $V_2$ consists of the even vertices of $G$. 

By the First Theorem of Graph Theory, 

$\sum_{v \in V(G)} deg \; v = \sum_{v \in V_1} deg \; v + \sum_{v \in V_2} deg \; v = 2m$

The number $\sum_{v \in V_1} deg \; v is even since it is a sum of even integers. Thus 

$\sum_{v \in V_1} deg \; v = 2m - \sum_{v \in V_2} deg \; v$,

which implies that $\sum_{v \in V_1} deg \; v$ is even.





