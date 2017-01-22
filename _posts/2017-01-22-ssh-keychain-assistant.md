---
layout: post
title:  macOS Sierra - ssh-keychain 문제해결
date:   2017-01-22
Tags:   Linux, Mac, crontab 
---

macOS Sierra로 업그레이드를 한 이후부터 ssh-keychain을 사용하는데 문제가 생겼다. 컴퓨터를 켜고 ssh key를 한번만 입력해주면 터미널을 사용하는 동안 암호 입력이 필요 없는 것이 정상적인 동작이지만, Sierra로 업그레이드 한 이후부터는 ssh, scp, rsync를 사용할 때마다 key를 입력해주어야 하는 문제가 발생함. Google을 해보니 opens 7.3p1로 업데이트 되면서 정책이 바뀐 것 때문이라고 함.

해결방법은 여러가지가 있지만, 가장 편리한 방법을 이용하기로 함.

`~/.ssh/config` 파일을 만들어 주고 파일 안에는 아래와 같이 입력해 준다.

```
Host * (asterisk for all hosts or add specific host)
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_rsa
```

**더보기**

- [리눅스 반복 예약작업 cron, crond, crontab][1]

[1]:	http://zetawiki.com/wiki/%EB%A6%AC%EB%88%85%EC%8A%A4_%EB%B0%98%EB%B3%B5_%EC%98%88%EC%95%BD%EC%9E%91%EC%97%85_cron,_crond,_crontab