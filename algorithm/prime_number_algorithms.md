<h1>Prime Number Algorithm</h1>

<h3>소수 확인 알고리즘</h3>

```c++
#include <bits/stdc++.h>
using namespace std;

bool isPrime(int n) {
    // 합성수 n이 존재하고, n=ab 라고 할때
    // a, b 둘 다 n의 제곱근보다 크다면 ab>n이 되어 n = ab는 모순이된다.
    // 따라서 a, b 중 적어도 하나는 n의 제곱근보다 작거나 같아야한다.
    // 위 증명 때문에 1 ~ n 까지의 수를 모두 나누지않고,
    // 1 ~ √n 까지의 숫자만으로도 소인수분해가 가능한 것을 알 수 있다.
    // 따라서 1 ~ √n 까지의 수만 가지고도 소수를 판별 가능하다.
    for(int i=2; i*i<=n; i++)
        if(n % i == 0)
            return false;
    return true;
}

int main() {
    int n = 7;
    bool result = isPrime(n);
    if(result)
        cout << "소수 입니다." << endl;
    else
        cout << "소수가 아닙니다." << endl;

    return 0;
}
```

<ul>
    <li>수 하나에 대하여 소수인지 아닌지 판별하기 위한 알고리즘</li>
    <li>Time Complexity: O(√N)</li>
</ul>


<h3>에라토스테네스의 체</h3>

```c++
#include <bits/stdc++.h>
using namespace std;

void sieveOfEratosthenes(int n) {
    bool prime_nums[n+1];
    // 먼저 n까지의 모든 수가 소수라고 가정
    memset(prime_nums, true, sizeof(prime_nums));

    for(int p=2; p*p<=n; p++) {
        if(prime_nums[p])
            // 이미 p^2보다 작은 수들은 이전에 처리됨
            for(int i=p*p; i<=n; i+=p)
                prime_nums[p] = false;
    }

    for(int p=2; p<=n; p++)
        if(prime_nums[p])
            cout << p << " ";
    cout << endl;
}

int main() {
    int n = 30;
    sieveOfEratosthenes(n);

    return 0;
}
```

<ul>
    <li>특정 범위 내에 소수를 찾기위해 사용되는 알고리즘</li>
    <li>Time Complexity: O(n*log(log(n)))</li>
</ul>
