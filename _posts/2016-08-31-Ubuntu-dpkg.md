---
layout: post
title:  "Ubuntu apt-get dpkg 오류 해결방법"
date:   2016-08-31 00:57:23
---

Ubuntu에서 apt-get 이용할 때 아래와 같은 오류가 발생할 때가 있다.

E: Could not get lock /var/lib/dpkg/lock - open (11 Resource temporarily unavailable)
<br>
E: Unable to lock the administration directory (/var/lib/dpkg/) is another process using it?

    
해결방법은 아래와 같다. 해당파일들을 삭제해 주면 된다.

    sudo rm /var/lib/apt/lists/lock

    sudo rm /var/cache/apt/archives/lock


<br><br>


**참고**

[Ask Ubuntu Forum](http://askubuntu.com/questions/15433/unable-to-lock-the-administration-directory-var-lib-dpkg-is-another-process)