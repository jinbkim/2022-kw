## Set
- 순서가 정렬되지 않은 객체들의 모음
### Basic Notations for Sets
- Tabular Form : {a, b, c}
- Set-builder Form : S={x|P(x)}
### Basic Properties of Sets
- 순서가 존재하지 않음
- 중복이 문제가 되지 않음
### Subsets and Supersets
- Subsets : S⊆T <-> ∀x (x∈S -> x∈T)
- Supersets : 자기 자신을 제외한 Subsets
### Power Sets
- P(S) = {x | x⊆S}
- 모든 Subsets 집합
### Ordered n-tuples
- 순서가 존재
- 중복이 문제가 됨
### Cartesian Products of Sets
- AXB = {(a, b) | a∈A ∧ b∈B }
- |AXB|=|A||B|
- AXB != BXA

#
## Set Operations
### Disjointedness
-  A∩B = ∅
### Principles of Inclusion-Exclusion
- |A∪B| = |A| + |B| - |A∩B|

#
## Functions
### Terminologies
- domain : 정의역
- codomain : 공역
- image : 상
- pre-image : 전상
- range : 치역
### Operators over Functions
- f,g:A->B , (f●g)(a) = f(a)●g(a)
### Operator for Composite Functions
- f:B->C, g:A->B, (f●g)(a) = f(g(a))
### One-to-One Functions, f:A->B
- f is injective
- ￢∃x,y : x!=y ∧ f(x)=f(y)
### Sufficient Conditions for Injection
- Strictly increasing : x>y -> f(x)>f(y)
- Strictly decreasing : x>y -> f(x)<f(y)
- if Strictly increasing/decreasing, f is one-to-one
### Onto Functions, f:A->B
- f is surjective
- ∀b∈B, ∃a∈A : f(a)=b
### One-to-One Correspondence Functions
- f is bijection or reversible or invertible
- f is one-to-one + onto
- f^-1(f(x)) = x
### Identity Function, I:A->A
- ∀a∈A : I(a)=a
### Some Important functions
- ⌈x⌉ : ceiling function
- ⌊x⌋ : floor function

#
## Sequences And Summations
### Sequences
- f(n) = {a1, a2, ..., an}
- f : generating function
- a1, a2, ..., an : n-th term
- n : index
### Euler’s Trick
- Σ(i: 1~n) i = n*(n+1)/2
### Geometric Series
- Σ(i: 0~n) ar^i = a*(r^(n+1)-1)/(r-1)
    * if r=1, Σ(i: 0~k) ar^i = a(n+1)