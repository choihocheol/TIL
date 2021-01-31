<h1>Python str.split(), str.join() built-in function</h1>

<h3>str.split()</h3>

<ul>
	<li>문자열을 delimiter(split() function의 첫번째 argument)을 기준으로 구분하여 리스트로 만들어주는 함수이다.</li>
	<li>만약 delimiter가 공백이라면 default로 공백을 delimiter로 리스트로 만든다.</li>
</ul>

```
a = '123 456 abc'
print(a.split()) # ['123', '456', 'abc']
```

<h3>str.join()</h3>

<ul>
	<li>리스트의 문자열 원소들을 문자열로 만들어주는 함수이다.</li>
	<li>리스트의 원소가 모두 문자열이어야 한다.</li>
</ul>

```
a = ["123", "456", "abc"]
print(''.join(a)) # 123456abc
```
