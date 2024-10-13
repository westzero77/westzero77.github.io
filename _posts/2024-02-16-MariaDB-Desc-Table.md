---
title: MariaDB 테이블 구조 확인 명령어
author: hippo
date: 2024-02-16 18:00:00 +0900
categories: [IT, MariaDB]
tags: [IT, Database, MariaDB, CLI, Table]
pin: true
---

## 기본 확인
```sql
desc 테이블명;

desc tb_user;
```

```sql
show columns from 테이블명;
     
show columns from tb_user;
```

## 상세 확인
```sql
show full columns from 테이블명;
          
show full columns from tb_user;
```

<br>

---
## reference
- [mysql, mariadb 테이블 구조(상세 정보) 확인 명령](https://erider.co.kr/131/){:target="_blank"}

