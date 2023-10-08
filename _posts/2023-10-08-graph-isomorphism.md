---
layout: post
comments: true
use_math: true
title:  "Graph Isomorphism"
date:   2023-10-08
categories: [math]
---

We dealt with the isomorphism concept in Group Theory. Now we apply this in graph.


## Graph Isomorphism

Two(labeled) graph $G$ and $H$ are $isomorphic$(have the same structure) if there exists a one-to-one correspondence $\phi$ from $V(G)$ to $V(H)$ such that $uv \in E(G)$ if and only if $\phi(u)\phi(v) \in E(H)$.

In this case, $\phi$ is called an $isomorphism$ from $G$ to $H$.

Thus if $G$ and $H$ are isomorphic graphs, then we say that $G$ is $isomorphic$ to $H$ and we write 
$G \cong H$




<br>

### Properties

* If two graphs are isomorphic, there exists an one-to-one correspondence from $V(G_1)$ to $V(G_2)$ but also two vertices $u_1$ and $v_1$ of $G_1$ are adjacent in $G_1$ if and only if the corresponding vertices $\phi(u_1)$ and $\phi(u_2)$ are adjacent in $G_2$.

<br>

* If two graphs are isomorphic, then they must have the same order, tehir sizes are the same and the degrees of their vertices are the same.



