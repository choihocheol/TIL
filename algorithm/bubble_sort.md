<h1>Bubble Sort</h1>

```python
def bubbleSort(arr):
    n = len(arr)
    for i in range(n):
        swapped = False
        for j in range(n-i-1):
            print("Occured")
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        if swapped == False:
            break

arr = [64, 34, 25, 12, 22, 11, 90]
bubbleSort(arr)
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
