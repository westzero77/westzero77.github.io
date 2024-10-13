---
title: Windows 명령어로 사용자 ID/PW 확인 및 변경
author: hippo
date: 2024-02-14 18:00:00 +0900
categories: [IT, Windows]
tags: [IT, Windows, 윈도우, cmd, 명령 프롬프트, 윈도우 명령어]
pin: true
---

## 사전 준비

1. 윈도우 검색창에 'cmd' 또는 '명령 프롬프트'를 입력하세요.
2. 명령 프롬프트를 **관리자 모드로 실행** 하세요. 
3. 관리자 모드로 실행된 명령 프롬프트 창에서 아래 명령어를 입력하세요.


## 계정 확인
```
net user
```
- USERNAME : 사용자 명
- USERDOMAIN : 컴퓨터 이름

## 계정 추가
```
net user 사용자이름 사용자패스워드 /add

net user admin admin1234 /add
```

## 계정 상세 확인
```
net user 사용자이름

net user admin
```

## 계정 비밀번호 수정
```
net user 사용자이름 수정할패스워드

net user admin admin0987
```

## 계정 삭제
```
net user 사용자이름 /del

net user admin /del
```

<br>

---
## reference
- [net user를 이용한 사용자 확인/추가/암호변경](https://m.blog.naver.com/newyks/150183566080){:target="_blank"}

