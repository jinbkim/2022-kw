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