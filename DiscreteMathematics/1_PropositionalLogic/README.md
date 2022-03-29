## Operators/Connectives
### unary operator
- operand를 하나만 가지는 연산자
### Binary operator
- operand를 두개 가지는 연산자
### Boolean operators
- ￢ : Negation (NOT)
- ∧ : Conjunction (AND)
- ∨ : Disjunction (OR)
- ⊕ : Exclusive-OR (XOR)
- -> : Implication (IMPLIES)
- <-> : Biconditional (IFF)

## Tautologies and Contradictions
- Tautologies : 항상 참인 명제
- Contradictions : 항상 거짓인 명제

#
## Defining Operators via Equivalences
- Exclusive-OR : p⊕q : (p∨q)∧￢(p∧q), (p∧￢q)∨(q∧￢p)
- Implication : p->q : ￢p∨q
- Biconditional : p<->q : (p->q)∧(q->p), ￢(p⊕q)

#
## Equivalence via Symbolic Derivation
- ex) (p∧￢q)->(p⊕r) <-> ￢p∨q∨￢r

#
## Predicate Logic
- ex) “The dog is sleeping"
    * x : "the dog" : object/entity
    * P : "is sleeping" : predicate
    * P(x) = "x is sleeping"

#
## Quantifier Expressions
### universal quantifier ∀
- for all
- ∀xP(x) : 모든 x에 대해 P(x)는 참
### Existential quantifier ∃
- there exist
- ∃xP(x) : P(x)를 만족하는 x가 1개이상 존재

#
## Binding Variables
- Binding Variables : free variable을 바인딩 한 변수
- proposion : 표현식에 free variable이 없는 식
- predicate : 표현식에 free variable이 하나 이상 있는 식

#
## Negations of Quantifier Expressions
- ￢∀xP(x) = ∃x¬P(x)
- ￢∃xP(x) = ∀x¬P(x)

#
## Nested Quantifiers
- R(x,y)=“x relies upon y” (x, y : people)
- ∃yR(x,y) : x는 누군가 한명이상 의존
- ∀x(∃yR(x,y)) : 모든 사람들은 누군가 한명이상 의존
- ∀xR(x,y) : 모든 사람들은 y를 의존
- ∃y(∀xR(x,y)) : 모든 사람들이 의존하는 사람이 누군가 한명이상 존재
- ∀yR(x,y) : x는 모든사람들을 의존
- ∃x(∀yR(x,y)) : 모든사람을 의존하는 사람이 누군가 한명이상 존재
- ∃xR(x,y) : 누군가 한명이상 y를 의존
- ∀y(∃xR(x,y)) : 모든사람들은 자신에게 의존하는 누군가 한명이상 존재
- ∀x(∀yR(x,y)) : 모든 사람들은 자신을 포함한 모든사람들을 의존

#
## Quantifier Equivalence Laws
- ∀xP(x) <-> ￢∃x￢P(x)
- ∃xP(x) <-> ￢∀x￢P(x)
- ∀x∀yP(x,y) <-> ∀y∀xP(x,y)
-  x∃yP(x,y) <-> ∃y∃xP(x,y)
- ∀x(P(x) ∧ Q(x)) <-> (∀xP(x)) ∧ (∀xQ(x))
- ∃x(P(x) ∨ Q(x)) <-> (∃xP(x)) ∨ (∃xQ(x))

#
## Defining New Quantifiers
### ∃!xP(x)
- P(x)를 만족하는 x는 딱 한개만 존재
- ∃!xP(x) <-> ∃x(P(x) ∧ ￢∃y(P(y) ∧ y!=x)) 
- ∃!xP(x) <-> ∃x(P(x) ∧ ∀y(￢P(y) ∨ y==x))

#
## Examples in Number Theory
### E(x) : "A number x is even"
- E(x) <-> ∃y(x=2y)
### P(x) : "A number x is prime"
- P(x) <-> (x>1 ∧ ￢∃yz(x=yz) ∧ y!=1 ∧ z!=1)

#
## Proof Methods for Implications
- Direct Proof : 명제의 참을 보임으로 증명하는 방법
- Indirect Proof : 대우 명제의 참을 보임으로써 증명하는 방법
- Vacuous Proof : 가정이 항상 거짓을 보임으로써 증명하는 방법
- Trivial proof: 결론이 항상 참을 보임으로써 증명하는 방법

#
## Proof by Contradiction
- 명제의 결론을 부정하여 모순이 생김을 보임으로써 명제가 참임을 보이는 증명 방법

#
## Proving Existential : ∃xP(x)를 증명
- Constructive proof : P(a)가 참인 a를 직접 찾는 방법
- Non-constructive proof : ￢∃xP(x)의 모순을 찾아 명제의 참을 얻어내는 방법

#
## The Halting Problem
- 최초로 풀지 못하는 문제로 증명된 첫번째 문제