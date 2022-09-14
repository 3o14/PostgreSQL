# 데이터베이스 연동하기

## 🖥 PostgreSQL 사용하기 위해 초기 설정하기
```java
// postgres 명령창(shell) 접속
sudo -u postgres psql


// 사용자 계정 만들기 ( 옵션을 추가할 수 있음 )
CREATE USER <이름> PASSWORD '<비밀번호>' SUPERUSER;

// PASSWORD : 비밀번호 설정
// SUPERUSER : 관리자 권한 부여


// 전체 사용자 조회하기
SELECT * FROM PG_SHADOW;
\dg, \du


// 사용자 전용 DB 만들기
CREATE DATABASE <이름> OWNER <사용자>;


// DB 확인하기
\l


// postgres 명령창 나가기
\q


// 사용자 전용 DB에 접속하기
psql -h localhost -p 5432 -U <사용자> -d <DB>;

// -h : 호스팅 주소 설정
// -p : 호스팅 포트 설정
// -U : 사용할 사용자 설정
// -d : 사용할 DB 설정
```

<br/><br/><br/>
***
## 참고
* [[PostgreSQL] PostgreSQL, pgAdmin4 이란? / 명령어](https://defineall.tistory.com/852)
