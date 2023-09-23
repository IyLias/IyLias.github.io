---
layout: post
comments: true
use_math: true
title:  "Graph Basics: walk, trail, path, circuit and cycle"
date:   2023-09-15 
categories: [math]
---

Let's start at some vertex $u$ of a graph $G$.

## Walk

If we proceed from $u$ to a neighbor of $u$ and then to a neighbor of that vertex and so on, until we finally come to a stop at a vertex $v$, then we have just described a walk from $u$ to $v$ in $G$. 

$u$-$v$ walk $W$ in $G$ is a sequence of vertices in $G$, beginning with $u$ and ending at $v$ such that consecutive vertices in the sequence are adjacent. 

$W$ = (u=$v_0$, $v_1$, ..., $v_k$=v)


* If $u$-$v$, then the walk $W$ is <U>closed</U>, while if $u \ne v$, then W is <U>open</U>.

* The number of edges encountered in a walk(including multiple occurrences of an edge) is called the <U>length of the walk</U>.


<br>

## Trail

$u$-$v$ $trail$ in graph $G$ to be a $u$-$v$ $walk$ in which no edge is traversed more than once.


<br>

## Path

$u$-$v$ $walk$ in a graph in which no vertices are repeated is a $u$-$v$ $path$.

<B> Every Path is a Trail </B>


<br><br>



## Distance

The distance between $u$ and $v$ is the smallest length of any $u-v$ path in $G$ and is denoted by $d_G(u,v)$.

Hence if $d(u,v) = k$, then there exists a $u-v$ path 
$P = (u=v_0,v_1,...,v_k=v)$



<br>

## Diameter 

The greatest distance between any two vertices of a connected graph G is called the 
<U>diameter of G</U> and is denoted by $diam(G)$. 






<br>

## Circuit 

A $circuit$ in a graph $G$ is a closed trail of length 3 or more.
Hence a circuit begins and ends at the same vertex but repeats no edges.


<br>


## Cycle

A $circuit$ that repeats no vertex, except for the first and last, is a $cycle$.

A k-cycle is a cycle of length k.








