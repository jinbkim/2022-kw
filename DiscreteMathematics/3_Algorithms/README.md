#
## Growth Of Functions
### Big O
- n1<=n, f(n) <= Cg(n)을 성립하는 C, n1이 존재하면 f(n)=O(g(n))
### Small O
- n1<=n, f(n) < Cg(n)을 성립하는 C, n1이 존재하면 f(n)=o(g(n))
### Big Theta
- n1<=n, C1g(n) <= f(n) <= C2g(n)을 성립하는 C1, C2, n1이 존재하면 f(n)=θ(g(n))
### Big Omega
- n1<=n, Cg(n) <= f(n)을 성립하는 C, n1이 존재하면 f(n)=Ω(g(n))
### Small Omega
- n1<=n, Cg(n) < f(n)을 성립하는 C, n1이 존재하면 f(n)=w(g(n))

#
## Strict Ordering of Functions (항상 시험에 나옴)
- lim(x->∞) f(x)/g(x)=0 <=> f < g
- if k>1, 1 < log(logn) < log(n),logk(n) < (log(n))^k < n^(1/k) < n < nlog(n) < n^k < k^n < n! < n^n

#
## Terminology for Complexity
- O(1) : Constant
- O(logc n) : Logarithmic ("c)
- O((logn)^c) : Polylogarithmic
- O(n) : Linear
- O(n^c) : Polynomial
- O(c^n): Exponential
- O(n!) : Factorial

#
## P, NP
### P
- Tractable(Feasible) Problems
- 결정론적 튜링 기계 : 어떤 상태에서 다음 행동이 1개로 정해진 기계
- 결정론적 튜링 기계를 사용해 다항사긴 내에 답을 구할 수 있는 문제의 집합
### NP
- Non deterministic Polynomial Bounded
- 비결정론적 튜링 기계 : 어떤 상태에서 다음 행동이 1개 이상인 기계
- 비결정론적 튜링 기계를 이용해 다항시간 내에 답을 구할 수 있는 문제의 집합
- P ⊆ NP



#
## Homework
### 3.1.4
    Describe an algorithm that takes as input a list of n integers and produces as output the largest difference obtained by substracting an integer in the list from the one following it.

    n개의 정수 중에서 한 정수와 그 다음 정수의 차이 들 중에서 가장 큰 차이를 출력하는 알고리즘을 설명하시오.
- 첫번째와 두번째, 두번째와 세번째, ... n-1번째와 n번째 차이의 절대값을 구하기
- 반복문을 돌며 차이의 절대값들 중 최대값 구하기
### 3.1.12
    Describe an algorithm that uses only assignment statements that replaces the triple(x, y, z) with (y, z, x).

    what is the minimum number of assignment statements needed?
    (x, y, z)를 (y, z, x)를 대체하는데 알고리즘을 설명하시오. 
    필요한 변수의 개수의 최소값은 무엇인가요?
- 필요한 변수는 한개입니다. 
- 변수 이름을 temp 라고 하면, temp에 x값을 저장하고, x에 y값을 저장하고, y에 z값을 저정하고, z에 temp값을 저장하면 (x, y, z)를 (y, z, x)로 대체할수 있습니다.
### 3.2.4
    Use the definition of "f(x) is O(g(x))" to show that 2^x + 17 is O(3^x)

    lim(x->∞) f(x)/g(x) = 0 이므로, n1<=n, f(n) <= Cg(n)을 성립하는 C, n1이 존재
### 3.3.8
    Given a real number x and positive integer k, determine the number of multiplications used to find x^2^k starting with x and successively squaring (to find x^2, x^4, and so on.) Is this a more efficient way to find x^2^k than by multiplying x by itself the appropriate number of times?

    x^2^k 를 x를 2^k번 곱하는것보다

    1. x * x = x^2
    2. x^2 * x^2 = x^4
    3. x^4 * x^4 = x^8
    ...
    k-1. x^2^(k-1) * x^2^(k-1) = x^2^(k)
    
    x^2^k 를 x를 2^k번 곱하는것보다, 위에처럼 k-1번의 곱셈을 하여 답을 구할수 있습니다.