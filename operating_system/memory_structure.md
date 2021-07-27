<h1>Memory Structure</h1>

<div align="center">
    <img src="https://media.geeksforgeeks.org/wp-content/uploads/memoryLayoutC.jpg"></img>
</div>

<h3>Code Segment</h3>
<ul>
    <li>Text Segment라고도 부른다.</li>
    <li>프로그램의 코드(기계어)가 저장되는 영역이다.</li>
    <li>CPU가 해당 영역에서 한줄(32bits or 64bits)씩 가져가서 처리한다.</li>
</ul>

<h3>Data Segment</h3>
<ul>
    <li>Global variable, static variable이 저장되는 영역이다.</li>
    <li>Initialized data segment, uninitialized data segment로 나뉜다.</li>
    <li><b>Initialized Data Segment</b></li>
    <ul>
        <li>주로 data segment라고 부른다.</li>
        <li>이름에서 알 수 있듯이 초기화된 variables(0으로 초기화된 variables 또한 해당 되지 않음)가 저장되는 영역이다.</li>
    </ul>
    <li><b>Uninitialized Data Segment</b></li>
    <ul>
        <li>BSS Segment(Block Started by Symbol Segment)라고도 부른다.</li>
        <li>이름에서 알 수 있듯이 초기화되지않은 variables 또는 0으로 초기화된 variables(NULL pointer로 초기화된 pointer variables도 이에 포함됨)가 저장되는 영역이다.</li>
    </ul>
</ul>

<h3>Heap Segment</h3>
<ul>
    <li>Software engineer가 직접 system call을 통해 동적으로 관리하는 영역이다.</li>
    <li>Heap segment에 저장된 variables는 전역에서 접근가능하다.</li>
    <li>메모리가 낮은주소에서 높은주소 방향으로 할당된다.</li>
    <li>Run time 시에 크기가 결정된다.</li>
    <li>주로 필요한 메모리의 크기를 예측하기 힘들때 사용한다.</li>
    <li>Stack 보다 느리다. 그 이유는 동적인 메모리를 할당으로 인한 memory fragmentation 관련 문제들이 발생하기 때문이다.</li>
</ul>

<h3>Stack Segment</h3>
<ul>
    <li>함수에서 local variables, parameters가 저장되는 영역이다.</li>
    <li>OS에 의해 자동으로 함수 호출시에 할당되고, 함수가 끝나면 반환된다.</li>
    <li>Stack segment에 저장된 variables는 local에서만 접근가능하다.</li>
    <li>메모리가 높은주소에서 낮은주소 방향으로 할당된다.</li>
    <li>Compile 시에 크기가 결정된다.</li>
    <li>Heap보다 빠르다. 그 이유는 stack frames가 연속적으로 메모리에 저장되어있고, 그 크기도 이미 다 알고있기때문에 CPU는 그저 주소값에서 더하기 혹은 빼기 연산만 하면되기 때문이다.</li>
</ul>

<h3>Overflow in Stack and Heap</h3>
<ul>
    <li>Stack segment에서 메모리가 높은주소에서 낮은주소 방향으로 할당되다가 heap segment를 침범할 수 있다. 이것을 <b>stack overflow</b>라고 한다.</li>
    <li>Heap segment에서 메모리가 낮은주소에서 높은주소 방향으로 할당되다가 stack segment를 침범할 수 있다. 이것을 <b>heap overflow</b>라고 한다.</li>
</ul>
