## Accessing SQL from a Programming Language
- 범용 프로그래밍 언어에서 SQL에 접근하는 방법은 두가지가 있음
### General Purpose Program
- 범용 프로그램은 함수를 사용하여 데이터베이스 서버에 접속하여 통신할 수 있음
### Embedded SQL
- 응용 프로그램에서 데이터베이스를 사용하기 위해 표현하는 SQL

#
## JDBC
- Java Database Connectivity
- 데이터베이스 시스템과 통신하기 위한 Java API
- JDBC는 동적이기 때문에 컴파일러에서 오류를 감지할 수 없음

#
## ODBC
- Open DataBase Connectivity

#
## Embedded SQL
- Host Language : SQL 쿼리가 내장된 언어
- 호스트 언어 변수를 SQL 변수와 구분하기 위해 콜론(:)이 앞에 붙음

#
## Function
### 함수 선언
    CREATE FUNCTION 함수이름 (매개변수이름 매개변수타입) 
        RETURNS 반환타입
    BEGIN
        ~
        RETURN 반환값;
    END

    함수이름(매개변수);  // 호출 방법
### 테이블을 반환하는 함수 선언
    CREATE FUNCTION 함수이름 (매개변수이름 매개변수타입) 
        RETURNS TABLE (
            ~
        )
    BEGIN
        ~
        RETURN TABLE (
            ~
        )
    END

    TABLE 함수이름(매개변수);  // 호출 방법

#
## Triggers
- 자동으로 실행되는 문장
- 트리거가 언제 어떻게 실행될지 명시해야함