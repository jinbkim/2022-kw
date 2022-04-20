### DDL
- Data Definition Language
- 각 관계를 정의하기 위해 사용하는 언어
- CREATE : 생성
- ALTER : 변경
- DROP : 삭제
- RENAME : 이름변경
- TRUNCATE : 행 제거

### DML
- Data Manipulation Language
- 데이터를 추가/수정/삭제를 위한 언어
- SELECT : 데이터 조회
- INSERT : 데이터 삽입
- UPDATE : 데이터 수정
- DELETE : 데이터 삭제

### DCL
- Data Control Language
- 데이터에 대한 권한을 다루기 위한 언어
- GRANT : 권한 설정
- REVOKE : 권환 회수

### Relation Schema and Instance
- attributes : columns of table (A1, A2, ..., An)
- tuple : rows of table
- schema : R = (A1, A2, ..., An)
- instance : real data of schema (rows of table)

### Key
- 스키마 R의 부분집합
- super key : 고유한 튜플을 식별하기에 충분한 attribute
- candidate key : 최소의 값만 가지는 super key
- primary key : candidate key 중 하나 선택
- foreign key 제약조건 : 한 관계의 값이 다른 관계에 나타남

### Relational algebra
- 하나 또는 두개의 관계를 입력하여 새로운 결과를 얻어내는 작업으로 구성된 절차적 언어
- Select : σp(r)
    * 주어진 조건을 만족하는 튜플들 선택
- Project : π(A1, A2, ..., An)(r)
    * 테이블의 특정한 attributes만 반환
    * 중복되는 행들은 결과에서 제거됨
- Cartesian-Product : r X s
    * 두 테이블에서 가능한 각 튜플 쌍을 결합하여 반환
    * 같은 이름의 attribute를 가지면 attribute에 이름을 첨부하여 속성을 구분 
- Join : r▷◁s
    * 모든 튜플들을 연결하여 불필요한 정보가 많은 Cartesian-Product 연산의 단점을 보완
    * r▷◁s = σp(rXs) : r과 s의 Cartesian-Product 연산결과에서 p 조건을 만족하는 결과

### Domain Types in SQL
- char(n) : 고정된 길이의 문자열
- varchar(n) : 가변길이의 문자열
- int : 정수
- smallint : 작은 크기의 정수
- numeric(p,d) : 정수 또는 소수 (p: precision, d: decimal point)
- real, double precision : 실수
- float(n) : 부동소수점

### DDL grammer
- create table instructor(X)
    * X 형식을 가지는 새로운 테이블 instructor 생성
- insert into instructor values(X)
    * instructor 테이블에 X 튜플을 삽입
- delete from instructor
    * instructor 테이블의 모든 튜플 삭제
- drop table instructor
    * instructor 테이블 삭제
- alter table instructor add A D
    * D(도메인)를 가지는 A(attribute)를 instructor 테이블에 삽입
- alter table instructor drop A
    * A(attribute)를 instructor 테이블에서 제거

### select
- SELECT distinct
    * 중복을 제거한 뒤 데이터 조회
- SELECT all
    * 중복을 포함한 데이터 조회
    * all은 생략이 가능 (SELECT all == SELECT)
- SELECT 'abc'
    * attribute가 abc이고 value가 abc인 1행 1열의 데이터를 반환

### String Operation
- % : 어떤 문자열과도 매치됨
- _ : 어떤 문자와도 매치됨 

### order by
- ORDER BY name : 오름차순으로 정렬
- ORDER BY name desc : 내림차순으로 정렬

### group by
- 그룹화 하여 데이터 조회
- 집계함수가 적용되지 않은 attribute들은 항상 group by에 포함이 되어야 함

### LIMIT
- 출력하는 개수를 제한
- SELECT * FROM 테이블이름 LIMIT 숫자;

### IN(A, B, ...)
- A, B, ... 중 하나에 포함되는지 확인
- SELECT * FROM 테이블이름 WHERE 칼럼이름 IN (A, B, ..);

### LIKE
- 문자열의 일부 글자를 검색
- SELECT * FROM 테이블이름 WHERE 칼럼 LIKE '__blabla%'

### EXISTS
- 서브쿼리에 대한 결과가 존재하는지 확인
- SELECT * FROM 테이블이름 WHERE EXISTS SELECT ~

### HAVING
- 집계 함수에 대해서 조건을 제시
- SELECT 집계함수 FROM 테이블이름 GROUP BY 칼럼이름 having 집계함수_조건식;

### SOME, ANY
- 서브쿼리에 대한 결과가 하나라도 일치하면 참
- SELECT age FROM 테이블이름 WHERE age > SOME SELECT ~

### ALL
- 서브쿼리에 대한 결과가 모두 일치하면 참
- SELECT age FROM 테이블이름 WHERE age > ALL SELECT ~

### View
- 데이터에는 없고, SQL만 저장되어있는 객체
- 보안과 함께 사용자의 편의성을 높이기 위해 사용

### Triggers
- 자동으로 실행되는 문장
- 트리거가 언제 어떻게 실행될지 명시해야함

### Key Attribute
- 다른 객체들과 중복되지 않는 고유한 값을 가진 Attribute
- ER 다이어그램에서 밑줄로 표현됨

### Simple Attribute
- 여러 Attribute으로 나눌 수 없는 Attribute

### Composite Attribute
- 여러 Attribute으로 나눌 수 있는 Attribute

### Single Valued Attritue
- 하나의 값만 가질 수 있는 Attribute

### Multi Valued Attribute
- 여러 개의 값을 가질 수 있는 Attribute
- ER 다이어그램에서 두개의 원으로 표현됨

### Derived Attribute
- 다른 Attribute가 갖고 있는 값으로부터 계산되어져 나온 Attribute
- ER 다이어그램에서 점선 원으로 표현됨

### Total Participation
- 모든 객체가 관계집합에서 하나 이상의 관계가 존재해야 함
### Partial Participation
- 모든 객체가 관계집합에서 하나 이상의 관계가 존재하지 않아도 됨

### Choice of Primary key for Binary Relationship
- One To One : 두 엔티티 중 아무거나 하나 엔티티의 PK 선택
- One To Many, Many To One : Many 쪽의 엔티티의 PK 선택
- Many To Many : 두 엔티티의 PK 선택