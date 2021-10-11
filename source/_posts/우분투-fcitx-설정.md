---
title: Ubuntu 20.04 fcitx 한글 입력 설정
date: 2021-07-29 16:14:36
categories: Ubuntu
tags:
  - ubuntu
  - 우분투 한글 설정
  - ubuntu fcitx
---

## 1. fcitx 설치

terminal을 실행 후, 아래의 명령어를 순차적으로 입력해줍니다.

```shell
$ sudo apt-get update
$ sudo apt-get install fcitx-hangul
$ sudo reboot
```

<br/>

## 2. Language Support 실행

하단 Keyboard input method system -> fcitx 변경합니다.

```shell
$ sudo reboot
```

<br/>

## 3. fcitx 설정

- 상단에 생긴 키보드 버튼을 클릭 -> configure
- 좌측 하단의 +버튼을 클릭
- Only show Current Language 체크 해제 후, hangul 선택 후 OK
- 한/영 키 변경
  - 상단의 global config 탭 클릭 -> Trigger Input method -> shif+space버튼 누르기
  - 개인 취향에 맞춰 설정하시면 됩니다.
