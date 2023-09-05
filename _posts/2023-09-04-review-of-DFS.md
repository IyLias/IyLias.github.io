---
layout: post
comments: true
title:  "DFS from my view"
date:   2023-09-05 
categories: [algorithm]
---

First, let's consider what DFS is. 

## DFS

Depth First Search, or DFS, is a method of exploration that, as the name suggests, digs deep like digging a well. It keeps digging until it reaches the end or confirms that it can't go any further, then it returns to the starting point and begins exploring in another direction.


What data is needed to implement DFS?

* First and foremost, map data is necessary.

* Exploration should occur in all directions, and when a new location is explored, the next exploration point should not be the place where you started. Therefore, a variable is needed to distinguish whether this area has been visited or not.
What is needed for a more efficient implementation?


Here's sample code for searching area using DFS. <br>

Exploration is carried out in all 9 directions from each point, continuing the search until the end of the area is reached.



```c++
int myMap[MAXNUM+1][MAXNUM+1];
bool visited[MAXNUM+1][MAXNUM+1];
int dir[8][2] = {{-1,-1},{-1,0},{-1,1},{0,1},{1,1},{1,0},{1,-1},{0,-1}};
int island=0;

void search(int r,int c,int w,int h){

    visited[r][c] = true;

    for(int i=0;i<9;i++){
        int newR = r+dir[i][0],newC = c+dir[i][1];
        if(newR>=1 && newR<=h && newC>=1 && newC<=w)
            if(myMap[newR][newC]==1 && visited[newR][newC]==false)
                search(newR,newC,w,h);
    }
}

```

<br>

## Improvement of DFS


Let's assume a situation. We know that even if we continue to explore in this direction, we won't get the desired destination or result. However, the basic form of DFS requires us to reach the end to find this out, which is very inefficient in terms of speed.

Therefore, we insert condition code inside the DFS exploration that can cut off the exploration tree. This is called "pruning."

