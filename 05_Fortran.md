---
layout: page
title: Fortran
permalink: /fortran/
order: 2
---

HelloWorld.f90

```fortran
PROGRAM HELLOWORLD
IMPLICIT NONE
REAL::TX, TY, TZ
INTEGER, PARAMETER::N=100, M=1000
REAL::A=2.61828
REAL(KIND=8)::B=3.141592.                 ! KIND
CHARACTER(LEN=8)::CH                      ! LEN
INTEGER,DIMENSION(-3:5,7)::IAA            ! ARRAY

TX = 1.0;  TY = 2.0;   TZ = TX \* TY

PRINT\*, &
  TX, TY, TZ
PRINT\*, 'N =',N, 'M =', M
PRINT\*, 'A =',A, 'B =', B
PRINT\*, 'HELLO WORLD'

END PROGRAM HELLOWORLD
```
