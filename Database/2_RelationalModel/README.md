## Relation Schema and Instance
- attributes : columns of table (A1, A2, ..., An)
- tuple : rows of table
- schema : R = (A1, A2, ..., An)
- instance : r(R)

#
## Attributes
- domain : 각 attribute가 허용되는 값의 집합
- atomic 해야 함 (값을 한개만 가져야 함)
- null : 알수 없음을 의미

#
## Schema
- 데이터베이스의 논리적 구조
- instacne : 데이터베이스 데이터의 스냅샷

#
## Key
- 스키마 R의 부분집합
- super key : 고유한 튜플을 식별하기에 충분한 attribute
- candidate key : 최소의 값만 가지는 super key
- primary key : candidate key 중 하나 선택
- foreign key 제약조건 : 한 관계의 값이 다른 관계에 나타남

#
## Relational algebra
- 하나 또는 두개의 관계를 입력하여 새로운 결과를 얻어내는 작업으로 구성된 절차적 언어

#
## Select : σp(r)
- 주어진 조건을 만족하는 튜플들 선택
### p : 선택 조건문
- ex) name = "jinbkim"
- =, ≠, <, ≤, >, ≥ 기호들 사용 가능
- 조건문들을 ∧, ∨, ¬ 기호들로 결합 가능
- 두 attribute 간의 비교도 가능
### r : instructor (table name)

#
## Project : π(A1, A2, ..., An)(r)
- 테이블의 특정한 attributes만 반환
- 중복되는 행들은 결과에서 제거됨
### r : instructor (table name)

#
## Cartesian-Product : r X s
- 두 테이블에서 가능한 각 튜플 쌍을 결합하여 반환
- 같은 이름의 attribute를 가지면 attribute에 이름을 첨부하여 속성을 구분 
- ex) r.id, s.id

#
## Join : r▷◁s
- 모든 튜플들을 연결하여 불필요한 정보가 많은 Cartesian-Product 연산의 단점을 보완
- r▷◁s = σp(rXs) : r과 s의 Cartesian-Product 연산결과에서 p 조건을 만족하는 결과

#
## Union : r ∪ s
- 합집합 연산

#
## Set-Intersection : r ∩ s
- 교집합 연산

#
## Set-Difference : r - s
- 차집합 연산

#
## Union, Set-Intersection, Set-Difference의 r과 s의 관계
- r과 s는 attribute 수가 같아야함
- r과 s의 도메인 값이 같아야 함

#
## Assignment : r → s
- 할당 연산

#
## Rename : ρx(A1, A2, ..., An)(E)
- 이름을 부여하거나 변경하는 연산
- E의 이름을 x로 변경
- attribute 이름을 각각 A1, A2, ..., An으로 변경

#
## Equivalent Queries
- 쿼리가 동일하지는 않지만 데이터베이스에 동일한 결과를 제공하는 쿼리
