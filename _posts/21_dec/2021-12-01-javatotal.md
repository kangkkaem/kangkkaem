---
layout: single
title:  "Java - 2또는 3의 배수가 아닌 수의 총합"
categories: java
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

```java
public class sum {

	public static void main(String[] args) {
		int sum = 0;
		
		for( int i =1; i<=50; i++) {
			if(i%2!=0 && i%3!=0)
				sum +=i;
		}
		
		System.out.println("sum="+sum);
	}
}
```

1~ 50의 정수중에서 2또는 3의 배수가 ***아닌***  수의 총합을 구하는 문제이다.

for문으로 1부터 50까지 1씩증가하고, if 문으로 2또는 3의 배수가 아닐때 sum에 i를 더한다.

결과는 433이 나온다.

