---
layout: single
title:  "Java - 사과를 담는데 필요한 바구니"
categories: java
tag: [java]
toc: false
author_profile: true
search: true
---

```java
public class apple {

	public static void main(String[] args) {
		int numOfApples = 123;
		int sizeOfBucket = 10;
		int numOfBucket = numOfApples/sizeOfBucket + (numOfApples%sizeOfBucket>0 ? 1:0);
		
		System.out.println("필요한 바구니의 수 : " +numOfBucket);

	}

}
```

10개의 사과를 담을 수있다면 바구니가 총 13개가 필요 할 것이다.

 numOfApples/sizeOfBucket 를 하면 반올림을 하지 않기 때문에 12가 된다.

따라서 나머지 연산자(%)를 사용해 나머지가 발생하는지 확인해서 발생하게된다면 1을 더해줘야한다.

필요한 바구니의 수는 13개
