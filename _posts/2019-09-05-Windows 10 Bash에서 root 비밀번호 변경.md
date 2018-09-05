---
title: Windows 10 Bash에서 root 비밀번호 변경
date: 2018-09-05 20:49:00
categories:
- OS
tags:
- Windows
- Bash
---

심심해서 bash를 깔았는데 su 명령을 쓰려니 루트 비밀번호를 알 수 없었습니다.  

설치할 때 비밀번호는 묻지도 않던데...  

아무튼 [변경 방법](https://askubuntu.com/questions/772050/reset-the-password-in-linux-bash-in-windows)을 찾았습니다. 

1. 우선 커맨드에서 기본 사용자를 root로 변경합니다.

```
>ubuntu config --default-user root
```

1. 이제 bash를 치면 root로 들어가 있습니다. 거기서 root 비밀번호를 변경합니다.

```
#passwd root
```

1. bash를 빠져나와서 기본 사용자를 되돌려 놓습니다.

```
>ubuntu config --default-user [내 계정]
```

이제는 변경된 루트 비밀번호를 쓸 수 있습니다.