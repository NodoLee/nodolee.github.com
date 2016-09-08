---
layout: post
title:  Ubuntu predefs.h 파일 못찾을 때
date:   2016-09-07 23:57:23
---

ubuntu에 wulffman 설치시 아래와 같이 헤더 파일을 못찾는 경우가 있다. Ubuntu를 기본 서버 버전으로 설치하는 바람에 대부분의 패키지는 설치가 안된 것 같다.

> ‘make: \*\*\* No rule to make target '/usr/include/bits/predefs.h', needed by 'wulffman.o'.  Stop.

해결방법은 libc를 설치하는 것이다.

`sudo apt-get install libc*`

**참고**

- [Ubuntu Forums][1]

[1]:	https://ubuntuforums.org/showthread.php?t=1877944