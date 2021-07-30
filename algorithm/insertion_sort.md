<h1>Insertion Sort</h1>

```python
def insertionSort(arr):
    n = len(arr)
    for i in range(1, n):
        key = arr[i]
        j = i-1
        while j >= 0 and key < arr[j]:
            arr[j+1] = arr[j]
            j -= 1
        arr[j+1] = key

arr = [64, 34, 25, 12, 22, 11, 90]
insertionSort(arr)
print(arr)
```

<ul>
	<li>Stable Sort</li>
	<li>Time Complexity</li>
	<ul>
		<li>O(n<sup>2</sup>)</li>
		<li>O(n) => 이미 list가 정렬된 상태 일때</li>
	</ul>
</ul>
