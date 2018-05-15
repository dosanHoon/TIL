# MongoDB 시작하기

## NoSQL

Not Only SQL

```
{
    "_id": ObjectId("5099803df3f4948bd2f98391"),
    "username": "velopert",
    "name": { first: "M.J.", last: "Kim" }
}
```

### Document?

### Collection?

### Database?

| RDBMS       | MongoDB              |
| ----------- | -------------------- |
| Database    | Database             |
| Table       | Collection           |
| Tuple / Row | Document             |
| Column      | Key /Field           |
| Table Join  | Embedded Documents   |
| Primary Key | Primary Key (\|\_id) |

| Database Server & Client |        |
| ------------------------ | ------ |
| mysqld                   | mongod |
| mysql                    | mongo  |
