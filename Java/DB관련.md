# 프로시져

## 프로시져란?

- 저장 프로시저 또는 스토어드 프로시저(stored procedure)는 일련의 쿼리를 마치 하나의 함수처럼 실행하기 위한 쿼리의 집합이다.
- Dao 하나로 처리 가능
- 캐시 히트 재활용성 높다
- 쿼리 수정 업데이트가 DB 상에서 가능 하다.
- 소스 관리가 어렵다.
- 로직이 DB 이 집중된다. (DB 는 비싼자원, 유지보수가 어려울수 있다.)

# 트랜잭션

## 트랜 잭션이란 ?

- 한번의 커넥션에서 수행하는 작업의 단위

## 트랜 잭션 특징

### 트랜잭션의 특징은 크게 4 가지로 구분된다.

- 원자성 (Atomicity)
- 일관성 (Consistency)
- 독립성 (Isolation)
- 지속성 (Durability)

#### 원자성 (Atomicity)

- 트랜잭션이 데이터베이스에 모두 반영되던가, 아니면 전혀 반영되지 않아야 한다는 것

#### 일관성 (Consistency)

- 트랜잭션의 작업 처리 결과가 항상 일관성이 있어야 한다는 것
  (데이터베이스의 변경여부에 영향을 받지 않아야 한다.)

#### 독립성 (Isolation)

- 어느 하나의 트랜잭션이라도 다른 트랜잭션의 연산을 끼어들 수 없다.

#### 지속성 (Durability)

- 트랜잭션이 성공적으로 완료됬을 경우, 결과는 영구적으로 반영되어야 한다는 점

트랜잭션에서 ROLLBACK 이 가능한 경우는 DML 쿼리에 의한 조작일 경우
DDL 에 의한 조작의 경우 back up & restore 가 필요함

bulk insert 대용량 데이터 질의

no log option 데이터베이스 조작식 로그를 남기지 않는다
(bulk insert 등의 대용량 데이터베이스 조작시 log 를 최소화하여 성능을 개선하기 위해 사용한다.)

# DDL , DML , DCL 이란?

## DDL

#### 데이터 정의 언어 - ( DDL : Data Definition Language )

└ 테이블이나 관계의 구조를 생성하는데 사용하며 CREATE, ALTER, DROP,TRUNCATE 문 등이 있다.

- CREATE - 새로운 데이터베이스 관계 (테이블) View, 인덱스 , 저장 프로시저 만들기.

- DROP - 이미 존재하는 데이터베이스 관계 ( 테이블 ) , 뷰 , 인덱스 , 저장 프로시저를 삭제한다.

- ALTER - 이미 존재하는 데이터베이스 개체에 대한 변경 , RENAME 의 역할을 한다.

- TRUNCATE - 관계 ( 테이블 )에서 데이터를 제거한다. ( 한번 삭제시 돌이킬 수 없음.)

## DML

#### 데이터 조작 언어 - ( DML : Data Manipulation Language )

└ 테이블에 데이터 검색, 삽입, 수정, 삭제하는 데 사용하며 SELECT, UPDATE, DELETE, INSERT 문 등이 있다.

- SELECT - 검색(질의)

- INSERT - 삽입(등록)

- UPDATE - 업데이트(수정)

- DELETE - 삭제

## DCL

#### 데이터 제어 언어 - ( DCL : Data Control Language)

└ 데이터의 사용 권한을 관리하는 데 사용하며 GRANT, REVOKE 문 등이 있다.

- GRANT - 특정 데이터베이스 사용자에게 특정 작업에 대한 수행 권한을 부여한다.

- REVOKE - 특정 데이터베이스 사용자에게 특정 작업에 대한 수행 권한을 박탈 or 회수 한다.

- COMMIT : 트랜잭션의 작업 결과를 반영

- ROLLBACK : 트랜잭션의 작업을 취소 및 원래대로 복구
