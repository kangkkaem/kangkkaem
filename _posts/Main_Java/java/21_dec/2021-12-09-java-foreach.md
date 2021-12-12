---
layout: single
title:  "Java -for each 문"
categories: java
tag: [java]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

for each 문


for문을 더 간단하게 쓰기위한 방법이다.

예시)
```java

public class Foreach {

	public static void main(String[] args) {
		int [] num = {1, 2,3,4,5,6};
		for( int n :num) {
			System.out.println(n + "입니다.");
		}
	}
}

```
![foreach](/assets/images/foreach.JPG)

- :(콜론) 뒤에 오는 num의 값들을 반복문이 동작할때마다 n변수에 담아준다.
  반복문안에서는 n을 사용해서 num에해당하는값을 하나씩 꺼낸다.

훨신 단순하고 깔끔하다!  -> 반복문과 배열은 함께 많이 쓰인다.