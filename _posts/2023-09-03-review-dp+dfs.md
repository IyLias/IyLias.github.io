---
layout: post
comments: true
title:  "Combination of DP and DFS"
date:   2023-09-03 
categories: [algorithm]
---


Just got inspired using dp + dfs. <br><br>

I was always allocating "visited" array for DFS but this can be also solved with array value.


```c++

int mmap[MAXNUM][MAXNUM];
int M,N;

ll dp[MAXNUM][MAXNUM];

int dir[4][2] = { {0,-1},{-1,0},{0,1},{1,0} };

ll search(int r,int c) {

    if (r == M - 1 && c == N - 1) {
        return 1;
    }
    if (dp[r][c] != -1)
        return dp[r][c];

    // now visited [r,c]
    dp[r][c] = 0; 
    
    // 4 directions.. search downhill
    for (int i = 0; i < 4; i++)
    {
        int cr = r + dir[i][0], cc = c + dir[i][1];
        if (cr >= 0 && cr < M && cc >= 0 && cc < N)
            if (mmap[r][c] > mmap[cr][cc])
            {
                dp[r][c] += search(cr, cc);
            }

    }

    return dp[r][c];
}
```


In this code, I distinguished whether current spot (r,c) is visited by setting default value -1.

