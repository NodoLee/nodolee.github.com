---
layout: post
title:  Shell> Case문 활용한 명령어 실행기
date:   2016-10-08
Tags:   Shell, Case

---

Case문을 활용한 명령어 실행기

\2. sh

```sh
#!/bin/bash

clear
echo -e "\033[0;34m
# ---------------------------------------
# File Transfer Script
# ---------------------------------------
"
echo -e "\033[0;32m 1. \033[0m Torrent   -->  Tanji2"
echo -e "\033[0;32m 2. \033[0m smi       -->  Tnaji2"
echo ""


echo -e "\033[0;34m
# ---------------------------------------
# github push
# ---------------------------------------
"
echo -e "\033[0;32m 3. \033[0m Github Push"


echo ""
echo -en "\033[0;33mChoose the option. > "
echo -en "\033[0;39m"
read num


```