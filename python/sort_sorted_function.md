<h1>Python list.sort() and sorted() built-in function</h1>

<h3>list.sort(), sorted()</h3>

```
a = [9, 8, 7, 6, 5, 4, 3, 2, 1]
a.sort()
print(a) # a = [9, 8, 7, 6, 5, 4, 3, 2, 1]

a = [9, 8, 7, 6, 5, 4, 3, 2, 1]
li = sorted(a)
print(li) # [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

<ul>
	<li>Key argument를 통해 정렬 기준을 설정할 수 있다.</li>
	<li>Reverse argument의 default value는 False이다. 이를 True로 바꿔주면 내림차순으로 정렬한다.</li>
	<li>내부적으로 merge sort와 insertion sort algorithm을 혼합한 하이브리드 방식의 sorting algorithm을 사용한다.</li>
</ul>
