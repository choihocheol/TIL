<h1>Python  "in" operator time complexity</h1>

<h3>list, tuple</h3>
<ul>
	<li>Average: O(n)</li>
	<li>모두 순회해야 하므로 크기만큼의 time complexity를 가지게 된다.</li>
</ul>

<h3>set, dictionary</h3>
<ul>
	<li>Average: o(1), Worst: O(N)</li>
	<li>Python에서 set과 dictionary는 내부적으로 hash data structure를 가지므로 time complexity가 O(1)로 상수시간이다.</li>
	<li>다만 hash table에서 collision이 많이 발생하였을땐 시간복잡도가 O(n)이 되고, 공간적인 측면에서는 hash table 때문에 더 cost가 있는 편이다.</li>
</ul>
