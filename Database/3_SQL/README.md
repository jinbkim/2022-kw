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

## DDL grammer
### create table instructor(X)
- X 형식을 가지는 새로운 테이블 instructor 생성
### insert to instructor values(X)
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