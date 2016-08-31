---
layout: post
title:  "Terminal Prompt 꾸미기"
date:   2015-07-02 20:00:23
---


Terminal 이용시 예픈 프롬프트 만들기...

`vi ~/.bash_profile`

그리고 나서 아래 한줄을 입력해 주고

`export PS1="\u@\[$(tput bold)\]\h\[$(tput sgr0)\] \w \\$\[$(tput sgr0)\]"`

적용해주기

`source ~/.bash_profile`
