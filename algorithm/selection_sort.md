<h1>Selection Sort</h1>

```
def selectionSort(arr):
    n = len(arr)
    for i in range(n):
        min_idx = i
        for j in range(i+1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]

arr = [64, 34, 25, 12, 22, 11, 90]
selectionSort(arr)
print(arr)
```

<ul>
	<li>Unstable Sort</li>
	<li>Time Complexity</li>
	<ul>
		<li>O(n<sup>2</sup>)</li>
	</ul>
</ul>
