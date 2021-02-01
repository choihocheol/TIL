<h1>Dijkstra Algorithm(Using min heap)</h1>

```
import heapq
INF = int(1e9)

nv, ne = 6, 11
source = 1
distance = [INF] * (nv+1)
graph = [
    [],
    [(2, 2), (3, 5), (4, 1)],
    [(3, 3), (4, 2)],
    [(2, 3), (6, 5)],
    [(3, 3), (5, 1)],
    [(3, 1), (6, 2)],
    []
]

def dijkstra(source):
    q = []
    distance[source] = 0
    heapq.heappush(q, (0, source))
    while q:
        dist, v = heapq.heappop(q)
        # 현재 노드가 이미 처리된 적이 있는 노드라면 무시
        # 한번 더 거치면 어차피 cost가 더 들기때문에 한번 거쳐간 vertex에 대해서는 고려하지않는다.
		if dist > distance[v]:
			continue
        for d, c in graph[v]:
            cost = dist + c
            if cost < distance[d]:
                distance[d] = cost
                heapq.heappush(q, (cost, d))

dijkstra(source)

for i in range(1, nv+1):
    if distance[i] == INF:
        print("INF")
    else:
        print(distance[i])
```

<ul>
	<li>Single Source Shortest Path Algorithm</li>
	<li>Only Non-negative edge weights graph</li>
	<li>Time Complexity: O(ElogV) => Graph의 모든 edges를 min heap에 넣었다가 빼는 연산과 매우 유사하다고 볼 수 있다.</li>
</ul>
