---
title: MariaDB 설정 파일 주요 속성 정리
author: hippo
date: 2024-02-20 18:30:00 +0900
categories: [IT, MariaDB]
tags: [IT, Database, MariaDB, Setting]
pin: true
---

## MariaDB 설정 파일 open
```bash
sudo vi /etc/my.cnf
```

## 'my.cnf' 파일 주요 속성 정리
```
[mysqld]

default_time_zone = '+9:00'

character-set-server = utf8mb4

collation-server = utf8mb4_unicode_ci

lower_case_table_names = 1

default_password_lifetime=0
```

- default_time_zone: DBMS Timezone 표준 시간대 설정
- character-set-server : 한글이 깨지거나 저장되지 않는 문제를 해결하기 위한 utf8mb4 설정
- collation-server : 한글이 깨지거나 저장되지 않는 문제를 해결하기 위한 utf8mb4_unicode_ci 설정
- lower_case_table_names: 이 값을 1로 설정하면 입력 값을 무조건 소문자로 인식되도록 설정한 것
- default_password_lifetime: 패스워드 만료 시간 설정 항목으로 0을 넣을 경우 만료 시간 없음으로 설정한 것

---
## reference
- [MariaDB/MySQL - Timezone 알아보기](https://server-talk.tistory.com/468?category=903840){:target="_blank"}
- [MariaDB Setting utf8mb4 Character Set](https://medium.com/oldbeedev/mysql-utf8mb4-character-set-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0-da7624958624){:target="_blank"}
- [MariaDB 캐릭터셋 UTF8 설정 방법](https://binwrite.com/mariadb-characterset-utf8/){:target="_blank"}
- [MariaDB DB 캐릭터 셋 utf-8으로 설정](https://gommin.tistory.com/17){:target="_blank"}
- [Docker MariaDB 설정 파일 수정하기 (테이블 검색 시 대소문자 구분 옵션 끄기)](https://velog.io/@ddmkim94/Docker-Docker-MariaDB-%EC%84%A4%EC%A0%95-%ED%8C%8C%EC%9D%BC-%EC%88%98%EC%A0%95%ED%95%98%EA%B8%B0){:target="_blank"}
- [MySQL 패스워드 정책 변경하기](https://blog.naver.com/mit5110/222150945309){:target="_blank"}
