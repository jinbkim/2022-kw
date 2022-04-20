### DDL
- ? : 생성
- ? : 변경
- ? : 삭제
- ? : 이름변경
- ? : 행 제거

### DML
- ? : 데이터 조회
- ? : 데이터 삽입
- ? : 데이터 수정
- ? : 데이터 삭제

### DCL
- ? : 권한 설정
- ? : 권환 회수

### Relation Schema and Instance
- ? : columns of table (A1, A2, ..., An)
- ? : rows of table
- ? : R = (A1, A2, ..., An)
- ? : real data of schema (rows of table)

### Key
- ? : 고유한 튜플을 식별하기에 충분한 attribute
- ? : 최소의 값만 가지는 super key
- ? : candidate key 중 하나 선택
- ? : 한 관계의 값이 다른 관계에 나타남

### Relational algebra
- 하나 또는 두개의 관계를 입력하여 새로운 결과를 얻어내는 작업으로 구성된 절차적 언어
- Select : ?
    * 주어진 조건을 만족하는 튜플들 선택
- Project : ?
    * 테이블의 특정한 attributes만 반환
    * 중복되는 행들은 결과에서 제거됨
- Cartesian-Product : ?
    * 두 테이블에서 가능한 각 튜플 쌍을 결합하여 반환
    * 같은 이름의 attribute를 가지면 attribute에 이름을 첨부하여 속성을 구분 
- Join : ?
    * 모든 튜플들을 연결하여 불필요한 정보가 많은 Cartesian-Product 연산의 단점을 보완
    * ? = ? : r과 s의 Cartesian-Product 연산결과에서 p 조건을 만족하는 결과

### Domain Types in SQL
- ? : 고정된 길이의 문자열
- ? : 가변길이의 문자열
- ? : 정수
- ? : 작은 크기의 정수
- ? : 정수 또는 소수 (p: precision, d: decimal point)
- ? : 실수
- ? : 부동소수점

### DDL grammer
- ? instructor(X)
    * X 형식을 가지는 새로운 테이블 instructor 생성
- ? instructor ?
    * instructor 테이블에 X 튜플을 삽입
- ? instructor
    * instructor 테이블의 모든 튜플 삭제
- ? instructor
    * instructor 테이블 삭제
- ? instructor ?
    * D(도메인)를 가지는 A(attribute)를 instructor 테이블에 삽입
- ? instructor ?
    * A(attribute)를 instructor 테이블에서 제거

### select
- ?
    * 중복을 제거한 뒤 데이터 조회
- ?
    * 중복을 포함한 데이터 조회
    * all은 생략이 가능 (SELECT all == SELECT)
- ?
    * attribute가 abc이고 value가 abc인 1행 1열의 데이터를 반환

### String Operation
- ? : 어떤 문자열과도 매치됨
- ? : 어떤 문자와도 매치됨 

### order by
- ? name : 오름차순으로 정렬
- ? name ? : 내림차순으로 정렬

### ?
- 그룹화 하여 데이터 조회
- 집계함수가 적용되지 않은 attribute들은 항상 ?에 포함이 되어야 함

### ?
- 출력하는 개수를 제한
- SELECT * FROM 테이블이름 ? 숫자;

### ?
- A, B, ... 중 하나에 포함되는지 확인
- SELECT * FROM 테이블이름 WHERE 칼럼이름 ? (A, B, ..);

### ?
- 문자열의 일부 글자를 검색
- SELECT * FROM 테이블이름 WHERE 칼럼 ? '__blabla%'

### ?
- 서브쿼리에 대한 결과가 존재하는지 확인
- SELECT * FROM 테이블이름 WHERE ? SELECT ~

### ?
- 집계 함수에 대해서 조건을 제시
- SELECT 집계함수 FROM 테이블이름 GROUP BY 칼럼이름 ? 집계함수_조건식;

### ?
- 서브쿼리에 대한 결과가 하나라도 일치하면 참
- SELECT age FROM 테이블이름 WHERE age > ? SELECT ~

### ?
- 서브쿼리에 대한 결과가 모두 일치하면 참
- SELECT age FROM 테이블이름 WHERE age > ? SELECT ~

### ?
- 데이터에는 없고, SQL만 저장되어있는 객체
- 보안과 함께 사용자의 편의성을 높이기 위해 사용

### ?
- 자동으로 실행되는 문장
- ?가 언제 어떻게 실행될지 명시해야함

### ?
- 다른 객체들과 중복되지 않는 고유한 값을 가진 Attribute
- ER 다이어그램에서 밑줄로 표현됨

### ?
- 여러 Attribute으로 나눌 수 없는 Attribute

### ?
- 여러 Attribute으로 나눌 수 있는 Attribute

### ?
- 하나의 값만 가질 수 있는 Attribute

### ?
- 여러 개의 값을 가질 수 있는 Attribute
- ER 다이어그램에서 두개의 원으로 표현됨

### ?
- 다른 Attribute가 갖고 있는 값으로부터 계산되어져 나온 Attribute
- ER 다이어그램에서 점선 원으로 표현됨

### ?
- 모든 객체가 관계집합에서 하나 이상의 관계가 존재해야 함

### ?
- 모든 객체가 관계집합에서 하나 이상의 관계가 존재하지 않아도 됨

### Choice of Primary key for Binary Relationship
- One To One : ?
- One To Many, Many To One : ?
- Many To Many :?