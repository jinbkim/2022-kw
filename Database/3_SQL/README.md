## SQL Parts
### DML
- Data Manipulation Language
- 데이터 접근 및 업데이트 하기위한 언어
### DDL 
- Data Definition Language
- 데이터베이스 스키마를 정의하기 위한 표기법
### Transaction control
- 트랜잭션의 시작과 끝을 지정하기 위한 명령
### Embedded SQL And Dynamic SQL
- 다른 프로그래밍 언어내에 SQL문을 포함하는 방법을 정의
### Authorization
- 액세스 권한을 지정

#
## Domain Types in SQL
- char(n) : 고정된 길이의 문자열
- varchar(n) : 가변길이의 문자열
- int : 정수
- smallint : 작은 크기의 정수
- numeric(p,d) : 정수 또는 소수 (p: precision, d: decimal point)
- real, double precision : 실수
- float(n) : 부동소수점

#
## DDL grammer
### create table instructor(X)
- X 형식을 가지는 새로운 테이블 instructor 생성
### insert into instructor values(X)
- instructor 테이블에 X 튜플을 삽입
### delete from instructor
- instructor 테이블의 모든 튜플 삭제
### drop table instructor
- instructor 테이블 삭제
### alter table instructor add A D
- D(도메인)를 가지는 A(attribute)를 instructor 테이블에 삽입
### alter table instructor drop A
- A(attribute)를 instructor 테이블에서 제거
### select A1, A2, ..., An from r1, r2, ... rm where P
- A1, A2, ..., An : 얻으려는 attribute
- r1, r2, ... rm : 검색할 대상의 테이블
- P : 조건식

#
## select
### SELECT distinct
- 중복을 제거한 뒤 데이터 조회
### SELECT all
- 중복을 포함한 데이터 조회
- all은 생략이 가능 (SELECT all == SELECT)
### SELECT *
- 모든 attribute 조회
### SELECT 'abc'
- attribute가 abc이고 value가 abc인 1행 1열의 데이터를 반환
### SELECT 'abc' as ABC
- as : attribute의 별칭
- as는 생략이 가능
- attribute가 ABC 이고 value가 'abc'인 1행 1열의 데이터를 반환
### SELECT 'abc' FROM instructor
- attribute가 abc이고 value가 abc인 n행 1열의 데이터를 반환
- n : instructor 테이블의 행

#
## from
### FROM instructor, teaches
-  instructor, teaches : instructor X teaches

#
## where
### WHERE salary BETWEEN 100 and 200
- salary가 100 이상 200이하

#
## String Operation
### %
- 어떤 문자열과도 매치됨
- \% : %를 직접 사용
### _
- 어떤 문자와도 매치됨 

#
## order by
### ORDER BY name
- 오름차순으로 정렬
### ORDER BY name desc
- 내림차순으로 정렬
### ORDER BY name, age
- name, age 순으로 오름차순 정렬

#
## Set Operation
- union : 합집합
- intersect : 교집합
- except : 차집합
- 중복된 값 자동제거
- 뒤에 all을 붙이면 중복값 허용
    * ex) union all

#
## Null Values
- is null : 알수 없는 값
- is not null : 알수 없는 값이 아닌 값

#
## Aggregate Function
- avg: 평균값
- min: 최소값
- max: 최대값
- sum: 모든 값을 더한값
- count: 모든 값의 개수
### group by
- 그룹화 하여 데이터 조회
- 집계함수가 적용되지 않은 attribute들은 항상 group by에 포함이 되어야 함
### having
- group by 된 필드에 조건을 줌

#
## Subquery
- 하나의 SQL 문에 포함되어 또 다른 SQL 문
- 비교연산자의 오른쪽에 기술해야 하고 반드시 괄호 안에 넣어햐 함
- 메인 쿼리가 실행되기 이전에 한번만 실행됨
- 서브쿼리에서는 ORDER BY를 사용하지 못함
### 단일 행 서브쿼리
- 서브쿼리가 단일 행 비교 연산자(=, <, <=, >, >=, <>)와 함께 사용할 때는 서브쿼리의 결과 건수가 반드시 1건 이하여야 함
- 그룹 함수를 사용하는 경우 결과값이 1건이기 때문에 단일 행 서브쿼리가 사용 가능
### 다중 행 서브쿼리
- 서브의 결과가 2건 이상 반활될 수 있다면 반드시 다중 행 비교 연산자와 함께 사용해야 함
- IN A : A를 포함하면 참
- NOT IN A : A를 포함하지 않으면 참
- SOME A : A중 하나만 만족하면 참
- ALL A : A를 모두 만족해야 참
- EXISTS : 공집합이 아니면 참
- NOT EXISTS : 공집합이면 참
- UNIQUE : 중복되는 값이 없으면 참
### 연관 서브쿼리
- 서브쿼리 내에 메인쿼리 컬럼이 사용된 서브쿼리
### Subqueries in the SELECT Clause (Scalar Subqueries)
- 서브쿼리를 끝마친 값하나를 메인쿼리에서 SELECT하기 때문에, 서브쿼리의 결과는 반드시 단일 행이나, 집계 함수를 거친 단일 값으로 반환되어야 함
### Subqueries in the From Clause (Inline Views Subqueries)
- 서브쿼리를 끝마친 테이블 하나를 메인쿼리의 FROM에서 테이블로 잡기 때문에, 서브쿼리의 결과는 반드시 하나의 테이블로 반환되어야 함
### Subqueries in the Where Clause (Nested Subqueries)
- 서브쿼리를 끝마친 값들을 메인쿼리의 조건절을 통해 비교등을 하기 때문에, 단일행과 복수행 둘다 반환이 가능
### With Clause
- 이름을 가진 서브쿼리를 정의한 후 사용하는 구문