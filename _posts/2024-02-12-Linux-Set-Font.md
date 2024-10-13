---
title: Linux(리눅스) Console(콘솔) 화면 키우기, 글자 키우기
author: hippo
date: 2024-02-12 18:00:00 +0900
categories: [IT, Linux]
tags: [IT, Linux, 리눅스, Console, 콘솔, CLI, setfont]
pin: true
---

## 일시적 방법

1. 기본
```shell
setfont latarcyrheb-sun16
```


2. 2배 크게
```shell
setfont latarcyrheb-sun32
```



## 영구적 방법

1. vi 명령어로 grub 파일을 엽니다.
   * grub은 GRand Unified Bootloader의 약자로, 리눅스 부트로더의 한 종류 입니다. 
   * vi 명령어는 Unix 및 Unix 계열 운영 체제(Linux 등)에서 사용되는 텍스트 편집기입니다.
```shell
vi /etc/default/grub
```

2. grub 파일에 'GRUB_CMDLINE_LINUX'에 'vconsole.font=latarcyrheb-sun32 vga=795' 설정을 추가합니다.
   * vi로 연 텍스트 편집기 안에서 'i'를 누르면 편집 모드로 바뀌어, 파일을 수정할 수 있습니다. 
   * 파일 수정을 완료 할때는 'Esc' 키를 누르고, ':wq'를 입력한 후 'Enter' 로 마무리 하면 저장할 수 있습니다.
   * 파일 수정을 원치 않을 때는, 'Esc' 키를 누르고, ':q!'를 입력한 후 'Enter' 로 마무리 하면 편집 중인 파일을 저장하지 않고 강제 종료 할 수 있습니다.
   * vga 값은 해상도를 의미 합니다. [VGA 참고 자료 바로가기](#vga-resolution-and-color-depth-reference-chart)
```
GRUB_CMDLINE_LINUX="vconsole.font=latarcyrheb-sun32 vga=795"
```

3. grub 파일을 저장한 뒤 아래 명령어를 입력하면, 다음 재부팅 때부터 적용됩니다.
```shell
sudo update-grub
```



## VGA resolution and color depth reference Chart

| Depth  | 800×600  | 1024×768 | 1152×864 | 1280×1024 | 1600×1200 |
|--------|----------|----------|----------|-----------|-----------|
| 8 bit  | vga=771  | vga=773  | vga=353  | vga=775   | vga=796   |
| 16 bit | vga=788  | vga=791  | vga=355  | vga=794   | vga=798   |
| 24 bit | vga=789  | vga=792  |          | vga=795   | vga=799   |


---
## reference
- [CentOS 7 Console에서 글자 크기 변경하기](https://hec-ker.tistory.com/332){:target="_blank"}
- [Grub(리눅스 부트로더)의 기본 부팅 목록과 부팅 대기 시간을 바꿔보자](https://itmir.tistory.com/60){:target="_blank"}

