---
title: [C/C++] Pointer VS Reference return types
date: 2021-10-11 19:00:57
categories: C/C++
tags:
  - 모각코
sitemap: true
---

# 1. NULL 허용 여부

포인터는 Null을 허용, 레퍼런스는 Null이 허용되지 않는다.

# 2. 참조 대상 할당 및 접근

포인터는 참조대상의 주소값을 할당, 레퍼런스는 참조 대상을 그대로 할당한다.

```
int tmp = 10;
int *ptr = &tmp;
int &ref = tmp;
```
