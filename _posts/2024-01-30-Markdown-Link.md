---
title: Markdown 마크다운 링크 새창에서 열리도록 작성하는 법
author: hippo
date: 2024-01-30 19:45:00 +0900
categories: [IT, Markdown]
tags: [IT, Markdown, 마크다운, 마크다운 문법, 새창으로 열기]
pin: true
---

> 결론부터 말하자면 `target="_blank"`을 넣어주면 됩니다.

## 기본
```md
[baby-hippo 블로그](https://baby-hippo.github.io/)
```
결과 : [baby-hippo 블로그](https://baby-hippo.github.io/posts/Markdown-Link/)

## 새창에서 열리도록 작성
```md
<a href="https://baby-hippo.github.io/" target="_blank"> baby-hippo 블로그 </a>
```
결과 : <a href="https://baby-hippo.github.io/" target="_blank"> baby-hippo 블로그 </a>


## 번외 - Jekyll Chirpy 테마에서 적용
```md
[baby-hippo 블로그](https://baby-hippo.github.io/){:target="_blank"}
```
결과 : [baby-hippo 블로그](https://baby-hippo.github.io/){:target="_blank"}


<br>
<br>
<br>

---
## reference
- [URL-링크가-새창에서-열리도록-VELOG-작성하기](https://velog.io/@countifs/URL-%EB%A7%81%ED%81%AC%EA%B0%80-%EC%83%88%EC%B0%BD%EC%97%90%EC%84%9C-%EC%97%B4%EB%A6%AC%EB%8F%84%EB%A1%9D-VELOG-%EC%9E%91%EC%84%B1%ED%95%98%EA%B8%B0){:target="_blank"}


