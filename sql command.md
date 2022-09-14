# 자주 사용하는 명령어 / 단축키

## 📍database 리스트 확인하기
```
\l
```

## 📍database 생성, 삭제
```java
// 데이터베이스 생성
CREATE DATABASE "데이터베이스";

// 데이터베이스 삭제
DROP DATABASE "데이터베이스";
```

## 📍 사용자 생성, 삭제
```java
// 사용자 만들기
CREATE USER 사용자;

// 사용자 삭제하기
DROP USER 사용자;
``` 
## 📍 사용자 리스트 확인하기
```
/dg, /du
``` 
## 📍 사용자 권한 database 생성하기
```
CREATE DATABASE 데이터베이스 OWNER 사용자;
``` 
## 📍 사용자 권한 database 접속하기
```
\c 데이터베이스 사용자
``` 
## 📍 table 생성하기
```java
CREATE TABLE 테이블이름 (
  필드이름1 필드타입,
  필드이름2 필드타입,
  ...
);
``` 
## 📍 table 리스트 확인하기
```
\d
``` 
## 📍 table 내용 확인하기
```
\d "테이블"
``` 
## 📍 PostgreSQL 터미널 나가기
```
\q
``` 

## 📍 PostgreSQL 터미널 청소( clear / clean )
```
// 명령어
\!clear


// 단축키
control + L

command(⌘) + L
```
