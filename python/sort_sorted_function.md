<h1>Python list.sort() and sorted() built-in function</h1>

<h3>list.sort(), sroted()</h3>

```
a = [9, 8, 7, 6, 5, 4, 3, 2, 1]
a.sort()
print(a) # a = [9, 8, 7, 6, 5, 4, 3, 2, 1]

a = [9, 8, 7, 6, 5, 4, 3, 2, 1]
li = sorted(a)
print(li) # [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

<p>리스트를 정렬하는 함수이다. reverse argument의 default value는 False로 오름차순이다. 이를 True로 하면 내림차순으로 정렬한다.<br>
merge sort와 insertion sort algorithm을 혼합한 하이브리드 방식의 sorting algorithm을 내부적으로 사용한다.<br>
내부적으로 C언어 기반으로 작성되어 있으며, 다양한 최적화 테크닉이 포함된 sorting algorithm으므로 더빠르게 동작한다.</p>
