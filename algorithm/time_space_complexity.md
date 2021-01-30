<h1>Time complexity and Space complexity</h1>

<h3>Complexity Notation</h3>
<ul>
	<ul>
		<li><b>Big-omega Notation(Best Case Complexity)</b></li>
		<li>점근적 하한선(Asymptotic lower bound)이므로 최소 이정도의 complexity를 가진다는 뜻이다.</li>
		<li>f(x) >= c * g(x)를 증명할 수 있는 c를 찾으면 참이다.</li>
	</ul>
	<ul>
		<li><b>Big-theta Notation(Average Case Complexity)</b></li>
		<li>점근적으로 근접한 한계값이다.(최대와 최소 사이라고 생각하면 된다.)</li>
		<li>Big-omega, Big-O 모두 참이면 참이다.</li>
	</ul>
	<ul>
		<li><b>Big-O Notation(Worst Case Complexity)</b></li>
		<li>점근적 상한선(Asymptotic upper bound)이므로 최대 이정도의 complexity를 가진다는 뜻이다.</li>
		<li>f(x) <= c * g(x)를 증명할 수 있는 c를 찾으면 참이다.</li>
	</ul>
</ul>

<h3>Time Complexity</h3>
<ul>
	<li>Python 기준 1초에 2000만 번의 연산을 수행한다고 가정하면 크게 무리가 없다.</li>
	<li>코딩테스트에서 python을 사용했을때 시간초과가 된다면 pypy3를 사용해보자.</li>
</ul>

<h3>Space Complexity</h3>
<ul>
	<li>Python 기준 list의 크기가 1000만 정도이면 40MB이다. 그러므로 list 하나의 크기가 1000만 이상인것이 존재한다면 다시 생각해보자.</li>
</ul>
