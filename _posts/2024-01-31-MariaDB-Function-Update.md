---
title: MariaDB CLI 환경에서 Function(함수) 수정하는 법
author: hippo
date: 2024-01-31 18:30:00 +0900
categories: [IT, MariaDB]
tags: [IT, Database, MariaDB, CLI, DB 함수, Function]
pin: true
---

## 함수 전체 확인

```sql
SHOW FUNCTION 데이터베이스이름;
```

## 함수 정의 확인

```sql
SHOW CREATE FUNCTION 데이터베이스이름.함수이름;
```

## CLI 환경에서 함수 만들기

- MariaDB에서는 함수 정의를 위해 `DELIMITER` 문을 사용하는 것이 일반적입니다. 이는 기본 SQL 명령 구분자(`;`)와 함수 본문 내의 세미콜론(`;`)과 구분하기 위함입니다.

```sql
DELIMITER //  
CREATE FUNCTION 데이터베이스이름.함수이름 (매개변수1 데이터_유형, 매개변수2 데이터_유형, ...) 
RETURNS 반환_데이터_유형
BEGIN
    -- 함수 내용
    -- ...
END// 

DELIMITER ;
```

- 예시 : 두 개의 파라미터를 받아서 더하는 함수

```sql
DELIMITER //

CREATE FUNCTION testDB.SUM(a INT, b INT)
RETURNS INT
BEGIN
    DECLARE result INT;
    SET result = a + b;
    RETURN result;
END//

DELIMITER ;
```

## 함수 수정하기
- OR REPLACE : 해당 함수 수정

```sql
DELIMITER //  
CREATE OR REPLACE FUNCTION 데이터베이스이름.함수이름 (매개변수1 데이터_유형, 매개변수2 데이터_유형, ...) 
RETURNS 반환_데이터_유형
BEGIN
    -- 함수 내용
    -- ...
END// 

DELIMITER ;
```


## 함수 삭제

```sql
DROP FUNCTION IF EXISTS 데이터베이스이름.함수이름;
```


