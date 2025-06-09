# PostgreSQL

## docker에서 PostgreSQL 접속하기
```bash
# postgreSQL 실행중인지 확인
$ docker ps   
CONTAINER ID   IMAGE                   COMMAND                  CREATED      STATUS        PORTS                           NAMES
4c5a234db3e8   dpage/pgadmin4:latest   "/entrypoint.sh"         5 days ago   Up 5 days     443/tcp, 0.0.0.0:8080->80/tcp   board_pgadmin
4c6b58332cf6   postgres:15-alpine      "docker-entrypoint.s…"   5 days ago   Up 19 hours   0.0.0.0:5432->5432/tcp          board_postgres

# 접속
$ docker exec -it 4c6b58332cf6 bash

/# psql -U postgres

# DB 선택
postgres=# \c board_db
You are now connected to database "board_db" as user "postgres".

# DB에 있는 테이블 조회
board_db=# \dt
               List of relations
 Schema |       Name        | Type  |  Owner   
--------+-------------------+-------+----------
 public | point_histories   | table | postgres
 public | posts             | table | postgres
 public | product_entity    | table | postgres
 public | review_point      | table | postgres
 public | reviews           | table | postgres
 public | user              | table | postgres
 public | user_review_point | table | postgres
```

## DB
```bash
# DB 생성

# DB 선택
postgres=# \c board_db

# DB 삭제

```


## Table
```bash
# Table 생성

# Table 선택
postgres=# \c board_db

# Table 삭제
```

## 데이터
```bash
# 데이터 생성
INSERT INTO employees (id, name, email) VALUES (1, '홍길동', 'hong@example.com');

```
