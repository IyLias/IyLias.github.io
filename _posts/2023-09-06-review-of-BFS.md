---
layout: post
comments: true
title:  "BFS from my view"
date:   2023-09-06 
categories: [algorithm]
---

First, let's consider what BFS is. 

## BFS

Breadth First Search, or BFS, is an algorithm for searching a tree data structure for a node that satisfies a given property. It starts at the tree root and explores all nodes at the present depth prior to moving on to the nodes at the next depth level.

Extra memory, <U>***usually a queue***</U>, is needed to keep track of the child nodes that were encountered but not yet explored.


Here's pseudocode from wiki.

```
 1   procedure BFS(G, root) is
 2      let Q be a queue
 3      label root as explored
 4      Q.enqueue(root)
 5      while Q is not empty do
 6          v := Q.dequeue()
 7          if v is the goal then
 8              return v
 9          for all edges from v to w in G.adjacentEdges(v) do 
10              if w is not labeled as explored then
11                  label w as explored
12                  w.parent := v
13                  Q.enqueue(w)
```



It starts from one point and spreads in all directions at the same distance. This process is repeated to check if it reaches the destination.

When we want to search the shortest distance, we can consider BFS.

