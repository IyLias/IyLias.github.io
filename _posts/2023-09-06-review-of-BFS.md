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

Extra memory, <U>usually a queue</U>, is needed to keep track of the child nodes that were encountered but not yet explored.



<br>

## Pseudocode of BFS

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


<br>


## My Imagination and Image of BFS


It starts from one point and spreads in all directions at the same distance. This process is repeated to check if it reaches the destination.

When we want to search the shortest distance, we can consider BFS.




<br>


## Expansion of BFS

Let's think about the problem 


> You have a map represented as an N×M matrix. In the map, 0 represents a passable path, and 1 represents an impassable wall. You want to move from the position (1, 1) to the position (N, M) while taking the shortest path. The shortest path is defined as the path that passes through the fewest number of cells in the map, including the starting and ending cells.

> <U>If breaking one wall during the journey leads to a shorter path, you are allowed to break up to K walls. </U>

> You can move from one cell to an adjacent cell in four directions: up, down, left, or right.

> Given the map, write a program to find the shortest path.



<br>

If just given the map and find the shortest path, then we just use BFS to solve. But in this problem, 

