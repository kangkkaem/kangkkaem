---
layout: single
title:  "Java - == 과 equals"
categories: 연습문제
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

== 은 같다는 연산자이다. 
근데 프로그램을 돌리다가 분명 같은 값인데 false 라고 찍힌적이있다.



예제
```java
public class sam {

	public static void main(String[] args) {
				String a = "HI";
		        String b = "HI";
		        String c = new String("HI");
		        String d = new String("HI");
		        
		        System.out.println( a == b );         
		        System.out.println( b == c );    
		        System.out.println( c == d );  
		        System.out.println( a.equals(b) );     
		        System.out.println( b.equals(c) );    
		        System.out.println( c.equals(d) );
	}
}
```

문자열에 값을 할당하는 방법이 2개이다. 위 예제를통해서 출력값을 살펴보자.
![문자열](/assets/images/문자열.JPG)

== 비교연산자로 같다는 의미를 가진다. 
하지만 두번째, 세번째 출력값을 보면 false 가 나온다.



**왜그럴까 ?**

자바는 메모리를 자동으로 관리해주는데 메모리 할당 부분에서 틀려서 그렇다. 
== 으로 비교를 할때
a라는 값을 메모리에 집어넣고 주소값을 사용하여 비교를 하게된다. 
equals로 비교를 할때는 데이터 값 비교를 하기 때문이다.
