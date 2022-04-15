## Design Phases
1. 고객의 데이터 요구 사항을 파악
2. 데이터 모형 선택
3. 추상 데이터 모델로 데이터베이스를 구현

#
## Design Alternatives
- 데이터는 중복과 불완전성을 가지면 안됨

#
## Entity Sets
- Entity : 다른 객체과 구별할 수 있는 객체
- Entity Set : 같은 특성들을 공유하는 엔티티 집합

#
## Relationship Sets
- Relationship : 몇몇 엔티티들 사이의 연관성
- Relationship Set
    * 엔티티 집합에서 구한 관계 집합
    * 속성을 가질 수 있음

#
## Role
- 관계를 가지는 엔티티 집합은 고유하지 않음
- 각 엔티티 집합들은 발생한 관계에서 역할을 가짐

#
## Degree of a Relationship Set
### Binary relationship Sets
- 두 개의 엔티티 집합이 관계를 가짐
- 대부분의 관계집합은 이진 관계집합
### Non-binary Relationship Sets
- 3개 이상의 엔티티 집합이 관계를 가짐
- 각 객체는 하나의 관계만 가질 수 있음

#
## Complex Attributes
- Simple Attribute : 속성을 여러 속성으로 나눌 수 없음
- Composite Attributes : 속성을 여러 속성으로 나눌 수 있음
- Single-valued Attributes : 하나의 값만 가질 수 있음
- Multivalued Attributes : 여러개의 값을 가질 수 있음
- Derived Attributes : 다른 속성으로 계산이 가능한 속성

#
## Mapping Cardinality Constraints
### One To One
- 객체가 서로 1대1로 매핑 되는것
### One To Many, Many To One
- 하나의 객체가 여러 객체에 매핑 되는것
### Many To Many
- 두 객체의 관계를 참조하는 또 하나의 테이블이 존재하는 것

#
## Total and Partial Participation
### Total Participation
- 모든 객체가 관계집합에서 하나 이상의 관계가 존재해야 함
### Partial Participation
- 모든 객체가 관계집합에서 하나 이상의 관계가 존재하지 않아도 됨

#
## Notation for Expressing More Complex Constraints

        l..h
- 선에 숫자를 표시 함으로써 관계를 나타낼수 있음
- l : 관계의 최소 개수
- h : 관게의 최대 개수

#
## Primary Key
### Primary key for Entity Sets
- 속성들로 이루어져 있으며, 고유하게 식별할 수 있는 값이어야 함
### Primary Key for Relationship Sets
- 관계가 있는 엔티티의 PK 집합으로 이루어짐
### Choice of Primary key for Binary Relationship
- One To One : 두 엔티티 중 아무거나 하나 엔티티의 PK 선택
- One To Many, Many To One : Many 쪽의 엔티티의 PK 선택
- Many To Many : 두 엔티티의 PK 선택