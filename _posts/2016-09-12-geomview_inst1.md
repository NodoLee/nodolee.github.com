---
layout: post
title:  Geomview 1.9.5 설치1
date:   2016-09-12 23:57:23
---


**전체 설치 순서**





> The most difficult part was that the latest Geomview release (1.9.5) no longer generates liboogl.a. Assuming that it's functionality was subsumed into libgeomview.a, I changed the makefile to look for libgeomeview.a rather than liboogl.a, Measure compiled without error.
> 
> - Christopher J. O'Brien     ([Link][1])

`liboogl.a` 라이브러리는 geomview (1.9.5) 에서는 더 이상 지원하지 않는다.
`/usr/local/lib` 경로에 가보면 `libgeomview.a`가 있는 것을 볼 수 있다.
이 라이브러리면 에러 없이 컴파일이 가능하다.

\</br\>\</br\>

**Makefile of Wulffman 1.2.5p1**

```	
`INCLDIR = -I. -I/usr/include/qhull -I/usr/include
GVINCLDIR = -I/root/geomview-1.9.5/include
LIBDIR = -L/usr/lib
VERSION = 1.2.5
MEASURE_VERSION = 1.1
TAR_DIR = /users/ryan/geomview/dist_src
DIST_DIR = wulffman_$(VERSION)
MEASURE_DIST_DIR = measure_$(MEASURE_VERSION)
```
`
`make wulffman`

`make measure`


.geomview에 Extra Module 경로 설정

`(emodule-define "wulffman" "/applic/wulffman_1.2.5p1/wulffman")`
`(emodule-define "measure" "/applic/wulffman_1.2.5p1/measure”)`


**Error 해결**

> In file included from mgopengl.c:34:0:
> mgopenglP.h:32:21: fatal error: GL/glu.h: No such file or directory
> compilation terminated.
> make[5](): *** [mgopengl.lo]() Error 1
> make[5](): Leaving directory `/home/nodolee/geomview-1.9.4/src/lib/mg/opengl'
> `
mesa 라이브러리 설치 (libglu1-mesa-dev) 하면 해결된다.

`sudo apt-get install libglu1-mesa-dev`

[1]:	https://sourceforge.net/p/geomview/mailman/message/29503281/
