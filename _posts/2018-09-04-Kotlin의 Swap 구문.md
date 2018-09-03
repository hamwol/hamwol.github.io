---
title: Kotlin의 Swap 구문
date: 2018-09-04 02:25:00
categories:
- Programming
tags:
- Kotlin
- Ruby
- Python
- Javascript
---

알고리즘 같은걸 배우다보면 두 변수의 값을 바꾸는 Swap은 참 자주도 나왔습니다.
C나 Java에서 보통은 이렇게 만들었죠.
```java
int a = 10;
int b = 20;
int tmp = 0;

tmp = a;
a = b;
b = tmp;
```
좀 더 머리를 쓰자면 이걸 함수로 만들어서 구현했고요.
근데 이거 살짝 헷갈립니다. 직관적이지도 않고, 쓸데없는 임시 변수가 하나 추가되는 것도 마음에 들지는 않습니다.

그래서인지 이후의 많은 언어들이 이 교환을 직관적으로 바꾸었습니다.

Python이나 Ruby는 물론.
```python
a = 10
b = 20
a, b = b, a
```

Javascript도 가능하지요.

```javascript
let a = 10
let b = 20
[a, b] = [b, a]
```

그렇다면 최근 제가 관심을 가지게 된 Kotlin은 어떨까요.
실망스럽게도 이런 직관적인 방법은 제공하지 않는 듯 싶습니다.

다만 聖 스택오버플로에 따르면 이런 [방법](https://stackoverflow.com/questions/45377802/swap-function-in-kotlin)은 있는 모양입니다.

```
var a = 10
var b = 20
a = b.also { b = a }
```

간단... 한가?