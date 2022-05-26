## Pigeonhole Principle
- n +1개의 물건을 n개의 상자에 넣은 경우, 최소한 한 상자에는 그 물건이 반드시 두 개 이상 들어있다는 원리

## Permutation
- nPr = n! / (n-r)!

## Combinations
- nCr = n! / ((n-r)! * r!)

## Pascal's triangle
- 첫 번째 줄에는 1을 씀
- 그 다음 줄을 만들 때 바로 위의 왼쪽 숫자와 오른쪽 숫자를 더함
- C(n+1, k) = C(n, k-1) + C(n, k)

## Recurrence Relations
- 어떤 함수를 자신보다 더 작은 변수에 대한 함수와의 관계로 표현한 것

## Tower of Hanoi
- Hn = 2Hn−1 + 1 = 2^n - 1


## Exercise
### How many shortest paths from (0, 0) to (m, n)?
- C(m+n, n)

### 8.2.4) Solve these recurrence relations together with the initial conditions given
a) a(n) = a(n-1) + 6 * a(n-2) (n>=2, a0=3, a1=6)
    
        r^2 = r + 6
        (r+2)(r-3) = 0
        r = -2 or 3
        a(n) = A*(-2)^n + B*3^n
        a(0) = A+B = 3
        a(1) = -2A + 3B = 6
        A = 3/5, B = 12/5
        a(n) = (3/5)*(-2)^n - (12/5)*(3)^n 

b) a(n) = 7 * a(n-1) - 10 * a(n-2) (n>=2, a0=2, a1=1)

        r^2 = 7r - 10
        (r-2)(r-5) = 0
        r = 2 or 5
        a(n) = A*2^n + B*5^n
        a(0) = A + B = 2
        a(1) = 2A + 5B = 1
        A = 3, B = -1
        a(n) = 3*2^n - 5^n

### 8.2.24) Consider the nonhomogeneous linear recurrence relation an = 2 * an-1 + 2^n
a) Show that an = n*2^n is a solution of this recurrence relation

        2*(n-1)*2^(n-1) + 2^n = 2^(n-1)(2n-2 + 2) = n*2^n = an
b) Use Theorem 5 to find all solutions of this recurrence relation

        homogeneous equation is an = c*2^n
        c*2^n + n*2^n = (c+n)*2^n
c) Find the solution with a0 = 2

        2 = c
        an = (n+2)*2^n
