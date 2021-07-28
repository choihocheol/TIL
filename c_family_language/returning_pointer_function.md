<h1>포인터를 반환하는 함수에서 발생 가능한 문제점</h1>

<p>어제 <a href="https://github.com/choihocheol/TIL/blob/main/operating_system/memory_structure.md">memory structure</a>에 대해 정리를 하다가 아래와 같은 상황에서 main() 함수의 변수 \*p는 과연 a() 함수의 변수 a의 주소를 여전히 가질 것인가 라는 생각을 하게 되었다.</p>

```
int* allocAddr() {
    int num = 10;
    int *p = &num;
    printf("allocAddr() => %p\n", &num);

    return p;
}

int main() {
    int *p = allocAddr();
    printf("main() => %p\n", p);

    return 0;
}
```

<p>실행결과</p>
```
allocAddr() => 0x7ffee887485c
main() => 0x7ffee887485c
```

<p>함수 allocAddr() 호출시에 할당받은 stack memory가 반납되었음에도 불구하고, 정상적으로 해당 stack memory를 main() 함수의 \*p변수가 접근하고 있다.</p>
