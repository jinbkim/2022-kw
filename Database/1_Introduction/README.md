## Purpose of Database Systems
- Data redundancy and inconsistency : 데이터 중복 및 불일치
- Difficulty in accessing data : 데이터에 접근하기 어려움
- Data isolation : 데이터 격리
- Integrity problems : 데이터 무결성
- Atomicity of updates : 업데이트의 원자성
- Concurrent access by multiple users : 여러 사용자의 동시 접근
- Security problems : 보안 문제

#
## Relational Model
- 모든 데이터가 다양한 테이블에 저장됨

#
## Instances and Schemas
- Instance:변수, Schemas:타입
- Logical Schema : 데이터베이스의 논리적 구조 (DB table의 column)
- Physical schema : 데이터베이스의 물리적 구조
- Instance : 특정 시점의 데이터베이스의 실제 값

#
## Physical Data Independence 
- 논리적 스키마를 변경하지 않고 물리적 스키마를 수정할 수 있는 기능

#
## DDL 
- Data Definition Language
- 데이터베이스 스키마를 정의하기 위한 표기법
- Data dictionary는 메타데이터를 가짐
    * 데이터베이스 스키마
    * 무결성 제약 조건 (기본 키)
    * 인증

#
## DML
- Data Manipulation Language
- 데이터 접근 및 업데이트 하기위한 언어
- Procedural DML : 사용자가 필요한 데이터와 데이터를 가져오는 방법을 지정
- Declarative DML : 사용자가 데이터를 가져오는 방법은 지정하지 않고 필요한 데이터만 지정 

#
## SQL Query Language
- Declarative DML에 속함
- 항상 단일 테이블을 반환

#
## Database Design
- logical design : 데이터베이스 스키마를 결정
- physical design : 데이터베이스의 실제 레이아웃 결정

#
## Database Engine
- 데이터베이스 시스템은 역할에 따라 각 모듈로 분할됨
### Storage Manager
- 스토리지 관리자는 다음과 같은 요소들을 포함
    * 인증, 무결성 관리자
    * 트랜잭션 관리자
    * 파일 관리자
    * 버퍼 관리자
- 스토리지 관리자는 다음과 같은 여러 데이터 구조를 구현
    * 데이터 파일 : 데이터 베이스 자체를 저장
    * 데이터 사전 : 데이터베이스의 스키마에 대한 메타데이터를 저장
    * 색인 : 특정 값을 포함하는 데이터 항목에 대한 포인터를 제공하여 빠른 접근이 가능
### Query Processor
- 쿼리 프로세스는 다음과 같은 요소들을 포함
    * DDL interpreter : DDL 문을 해석하고 정의를 데이터 사전에 기록
    * DDL compiler : 질의 언어로 된 DML 문을 질의 평가 엔진이 이해하는 하위 수준의 지시어로 변환
### Transaction Management
- 트랜잭션 : 단일 논리 함수를 실행하는 연산 모음
- 시스템 장애 및 트랜잭션 장애에도 불구하고 데이터베이스를 일관된 상태로 유지해야 함
- Concurrency-control manager : 데이터베이스의 일관성을 보장하기 위해 동시 트랜잭션 간의 상호 작용을 제어함

#
## Database Architecture
- 중앙 집중식

#
## Database Applications
### Two-tier architectures
- 응용 프로그램은 클라이언트 시스템에 상주하며 서버 시스템에서 데이터베이스 시스템을 호출
### three-tier architectures
- 클라이언트 시스템은 프론트엔드 역할을 하며 직접적인 데이터베이스 호출을 하지 않음
- 클라이언트는 폼 인터페이스를 통해 애플리케이션 서버와 통신
- 애플리케이션 서버는 데이터베이스 시스템과 통신하여 데이터에 접근

#
## DBA
- Database Administrator
- DBA의 기능
    * 스토리지 구조 및 액세스 권한 정의
    * 자료접근 권한 부여
    * 주기적인 데이터베이스 백업
    * 충분한 디스크 공간 확보