## (Inner) Join
- 공통된 부분만 결합
### select name, course_id from student natural join takes;
- select name, course_id from students, takes where student.ID = takes.ID;

#
## Outer Join
- 공통된 부분만 결합하는 Inner Join과 다르게 공통되지 않은 행도 유지
### Left Outer join
- 왼쪽 테이블의 행 유지
### Right Outer join
- 오른쪽 테이블의 행 유지
### Full Outer Join
- 양쪽 테이블의 행 유지

#
## Join Conditions
### natural
- 동일한 타입과 이름을 가진 칼럼을 조인 조건으로 이용
### on <predicate>
- 임의의 조인 조건을 지정
### using (A1, A2, ..., An)
- 선택한 칼럼들을 조인 조건으로 이용

#
## Views
- 데이터에는 없고, SQL만 저장되어있는 객체
- 보안과 함께 사용자의 편의성을 높이기 위해 사용
- Materialized Views : 자주사용되는 View의 결과를 실제 데이터로 저장하여 쿼리 속도를 향상

#
## View Updates in SQL
- 단순한 뷰에서만 업데이트가 허용됨
- FROM 절에서 데이터베이스 관계가 1개만 존재해야 함
- SELECT 절에서는 속성의 이름만 포함해야 함
- SELECT 절의 존재하지 않은 속성은 null로 설정해야 함
- 쿼리에 groupby 또는 having절은 없어야 함

#
## Transactions
- 트랜잭션은 Commit 또는 Rollback 으로 종료되어야 함
- Commit : 트랜잭션이 끝나고, DB에 성공적으로 반영됨
- Rollback : 트랜잭션에 의해 수행된 작업이 취소됨

#
## Integrity Constraints
- Integrity : 데이터의 정확성, 일관성을 나타냄
- Integrity Constraints : 데이터의 Integrity를 보장하기위한 조건

#
## Constraints on a Single Relation
- not null : null 이 아닌값이 들어와야 함
- unique : 해당 속성은 중복된 값을 저장할 수 없음
- check clause : 모든 튜플이 만족해야 하는 술어 지정

#
## Referential Integrity
- PK와 FK 간의 관계가 항상 유지됨을 보장
- FK가 존재하는한 참조되는 테이블의 행을 삭제 될수 없고, PK도 변경될 수 없음 
- Cascade : FK의 참조값을 NULL로 만들어 참조를 모두 끊은 후 필요한 작업을 해주는 옵션

#
## Assertions
- 데이터베이스가 항상 만족하기를 바라는 조건을 나타내는 술어

#
## Built-in Data Types in SQL
### date
- 날짜(년도, 월, 일)
- ex) '1995-8-7'
### time
- 하루 중 시간(시간, 분, 초)
- ex) '08:00:30'
### timestamp
- 날짜와 시간(data + time)
- ex) '1995-8-7 08:00:30'
### interval
- 기간
- date/time/timestamp 값을 다른 값에서 빼면 생기는 값
- date/time/timestamp에 interval 값을 더할 수 있음
### julianday
- 툭정한 날짜를 기준일로하여 기준일로부터 일차를 나타낸것 
- julianday 함수를 이용하면 쉽게 interval를 구할수 있음
- 단위 : 하루

#
## Large-Object Types
- 쿼리 문의 결과가 너무 크면, 객체 자체보다는 포인터를 반환함
### blob
- 해석되지 않은 바이너리 데이터의 대규모 집합
- 데이터의 해석은 데이터베이스 시스템 외부의 프로그램이 해야 함
### clob
- 문자 데이터의 큰 집합

#
## Index Creation
- 추가적인 저장 공간을 활용하여 데이터베이스 테이블의 검색 속도를 향상시키기 위한 자료구조

#
## Authorization
- 사용자에게 데이터베이스 일부에 대한 권한을 할당할 수 있음
- Read : 데이터 읽기 권한
- Insert : 데이터 삽입 권한
- Update : 데이터 수정 권한
- Delete : 데이터 삭제 권한
- Index : 인덱스를 생성하거나 삭제할수 있는 권한
- Resources : 새로운 관계 생성 권한
- Alteration : 관계에서 attribute를 추가하거나 삭제할 수 있는 권한
- Drop : 관계를 삭제 권한
- Roles : 사용자에게 효율적으로 권한을 부여하기 위해 여러 개의 권한을 묶어 권한을 행사