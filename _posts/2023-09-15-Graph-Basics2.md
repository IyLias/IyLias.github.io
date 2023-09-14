---
layout: post
comments: true
title:  "Graph Basics: walk, trail, path, circuit and cycle"
date:   2023-09-15 
categories: [math]
---

Let's start at some vertex u of a graph G.

## Walk

If we proceed from u to a neighbor of u and then to a neighbor of that vertex and so on, until we finally come to a stop at a vertex v, then we have just described a walk from u to v in G. 

u-v walk W in G is a sequence of vertices in G, beginning with u and ending at v such that consecutive vertices in the sequence are adjacent. 

W = (u=$v_0$, $v_1$, ..., $v_k$=v)


* If u-v, then the walk W is <U>closed</U>, while if $u \ne v$, then W is <U>open</U>.

* The number of edges encountered in a walk(including multiple occurrences of an edge) is called the <U>length of the walk</U>.





