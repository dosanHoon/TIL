# 프로시져

#DDL , DML , DCL 이란?

## DDL

#### 데이터 정의 언어 - ( DDL : Data Definition Language )

3
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
