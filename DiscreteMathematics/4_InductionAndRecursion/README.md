## Mathematical Induction
- n=1 일때, 성립함을 보임
- n=k 일때, 성립한다고 가정하고, n=k+1도 성립함을 보임

#
## Recursion
- 어떤 문제를 해결하기 위해 알고리즘을 설계할 때 동일한 문제의 조금 더 작은 경우를 해결함으로써 그 문제를 해결하는 것

#
## Homework
### 5.1.6
    Prove that 1*1! + 2*2! + ... + n*n! = (n+1)! - 1 whenever n is a positive integer

    n=1 이면, 
    좌변은 1*1! = 1.
    우변은 (2)!-1 = 1.
    좌변=우변 이기 때문에 식이 성립.
    n=k 일때 식이 성립한다고 가정하면,
    1*1! + 2*2! + ... + k*k! = (k+1)! - 1.
    n=k+1 이면, 1*1! + 2*2! + ... + k*k! + (k+1)*(k+1)! = (k+1)! - 1 + (k+1)*(k+1)! = (k+1)!(1 + k+1) -1 = (k+2)! -1.
    증명 완료.
### 5.1.10.a
    Find a formula for
    1/(1*2) + 1/(2*3) + ... + 1/(n*(n+1)) by examining the values of this expression for small values of n.

    1/(1*2) + 1/(2*3) + ... + 1/(n*(n+1)) = 1 - 1/(n+1).
### 5.1.10.b
    Prove the formla you conjectured in part (a).

    1/(1*2) + 1/(2*3) + ... + 1/(n*(n+1)) = 1 - 1/(n+1)
    n=1 이면,
    좌변은 1/2.
    우변은 1 - 1/2 = 1/2.
    좌변=우변 이기 때문에 식이 성립.
    n=k 일때 식이 성립한다고 가정하면,
    1/(1*2) + 1/(2*3) + ... + 1/(k*(k+1)) = 1 - 1/(k+1).
    n=k+1 이면, 1/(1*2) + 1/(2*3) + ... + 1/(k*(k+1)) + 1/((k+1)*(k+2)) = 1 - 1/(k+1) + 1/((k+1)*(k+2) = 1 - 1(k+2).
    증명 완료.
### 5.3.16
    Show that f0 - f1 + f2 - ... - f(2n-1) + f(2n) = f(2n-1) - 1 when n is a positive integer

    n=1 이면,
    좌변은 f(2)-f(1)+f(0) = 2-1+1=0.
    우변은 f(1)-1 = 1-1=0.
    좌변=우변 이기 때문에 식이 성립.
    n=k 일때 식이 성립한다고 가정하면,
    f0 - f1 + f2 - ... - f(2k-1) + f(2k) = f(2k-1) - 1.
    n=k+1이면, f0 - f1 + f2 - ... - f(2k-1) + f(2k) - f(2k+1) + f(2k+2) = f(2k-1) - 1 + - f(2k+1) + f(2k+2) = f(2k+1) + f(2k) - f(2k+1) + f(2k-1) - 1 = f(2k) + f(2k-1) - 1 = f(2k+1) -1.
    증명완료.

### 5.3.20
    Give a recursive definition of the functions max and min so that max(a1, a2, ..., an) and min(a1, a2, ..., an) are the maximum and minimum of the n numbers a1, a2, ..., an respectively.
    
    n=1이면, 
    min(a1) = a1.
    max(a1) = a1.
    n=2이면,
    min(a1, a2) = a2(if a1>= a2), a2(otherwise)
    max(a1, a2) = a1(if a1>= a2), a2(otherwise)
    n>2이면,
    min(a1, a2, ..., an) = min(min(a1, a2, ..., an-1), an)
    max(a1, a2, ..., an) = max(max(a1, a2, ..., an-1), an)

### 5.4.32
    Devise a recursive algorithm to find the nth term of the sequence defined by a0=1, a1=2, a2=3, and an=a(n-1)+a(n-2)+a(n-3), for n = 3,4,5 ...

    int solution(int n) {
        if (n <= 2)
            return n+1;
        return (solution(n-1) + solution(n-2) + solution(n-3));
    }