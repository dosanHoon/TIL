# MongoDB 시작하기

## NoSQL

Not Only SQL

* 동적인 스키마로 구성된다.

### Document?

### Collection?

### Database?

### Document ?

```javascript
{
    "_id": ObjectId("5099803df3f4948bd2f98391"),
    "username": "velopert",
    "name": { first: "M.J.", last: "Kim" }
}
```

* RDMS 의 record 와 대칭 되는 개념

### Collection ?

* Document 의 그룹

### Database?

* Database 는 Collection 들의 물리적인 컨테이너입니다. 각 Database 는 파일시스템에 여러파일들로 저장됩니다.

### RDMS 와 비교

| RDMS                     | MongoDB              |
| ------------------------ | -------------------- |
| Database                 | Database             |
| Table                    | Collection           |
| Tuple / Row              | Document             |
| Column                   | Key /Field           |
| Table Join               | Embedded Documents   |
| Primary Key              | Primary Key (\|\_id) |
| Database Server & Client |                      |
| ------------------------ | ------               |
| mysqld                   | mongod               |
| mysql                    | mongo                |
