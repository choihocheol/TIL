<h1>Floyd Warshall Algorithm</h1>

```python
INF = int(1e9)

nv, ne = 4, 7

# Graph represented by adjacency matrix
graph = [[INF for _ in range(nv+1)] for _ in range(nv+1)]
for x in range(nv+1):
    for y in range(nv+1):
        if x == y:
            graph[x][y] = 0
graph[1][2] = 4
graph[1][4] = 6
graph[2][1] = 3
graph[2][3] = 7
graph[3][1] = 5
graph[3][4] = 4
graph[4][3] = 2

for k in range(nv+1):
    for x in range(nv+1):
        for y in range(nv+1):
            graph[x][y] = min(graph[x][y], graph[x][k]+graph[k][y])

for x in range(1, nv+1):
    for y in range(1, nv+1):
        if graph[x][y] == INF:
            print("INF", end=' ')
        else:
            print(graph[x][y], end=' ')
    print()
```

<ul>
	<li>All Paires Shortest Path Algorithm</li>
	<li>Non-negative cycle</li>
	<li>Time complexity: O(V^3)</li>
</ul>
