# DB 설계 고려

### join 속도

* inner join 이 제일 빠르고
* outer join 느림

필드 조건 검사 쿼리 복잡해지고 연산 느려짐데이터가 많지 않을시 그냥 outer join
