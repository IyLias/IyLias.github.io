---
layout: post
comments: true
title:  "Graph Basics: Connected Graph and Component"
date:   2023-09-16 
categories: [math]
---

In this post, let's check out connected and component.


## What is connected?

If $G$ contains a $u$-$v$ path, then $u$ and $v$ are said to be connected and $u$ is $connected$ to $v$.

Expand to all vertices, A graph $G$ is $connected$ if every two vertices of $G$ are connected, that is, if $G$ contains a $u$-$v$ path for every pair $u,v$ of vertices of $G$.


<br>

## Component

A connected subgraph of $G$ that is not a proper subgraph of any other connected subgraph of $G$ is a <B>component of $G$</B>.

Thus a graph $G$ is connected if and only if $k(G)=1$.



## Theorem: Equivalence Relation

Let $R$ be the relation defined on the vertex set of a graph G by $u \; R \; v$, where $u,v \in V(G)$, if $u$ is connected to $v$, that is, if $G$ contains a $u-v$ path. Then $R$ is an equivalence relation.


Proof)




