# MySQL 

## 명령어 정리
```bash
> mysql -u [username] -p;
> 예) mysql -u root -p; -> 비밀번호 입력하라고 나옴
```

### DB CRUD
1. DB 생성
```sql
mysql> CREATE DATABASE <데이터베이스 이름>;
```



### Table CRUD

### Index
1. 인덱스 생성

(1) 테이블 만들 때 인덱스 생성하기
```sql
mysql> CREATE TABLE player (
id INT PRIMARY KEY,
name VARCHAR(20) NOT NULL,
team_id INT,
backnumber INT,
INDEX player_name_idx(name),
UNIQUE INDEX team_id_backnumber_idx (team_id, backnumber)
);
```
(2) 테이블은 이미 만들어졌고, 나중에 인덱스 생성하기
```sql
mysql> CREATE INDEX player_name_idx ON player (name),
mysql> CREATE UNIQUE INDEX team_id_backnumber_idx ON player(team_id, backnumber);
```
2. 인덱스 조회
```sql
mysql> SHOW INDEX FROM player;
```


### Tuple CRUD


