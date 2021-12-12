---
layout: single
title:  "Java - next와 nextLine 차이"
categories: 기타지식
tag: [기타지식]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

next() 는 공백을 기분으로 한 단어 또는 한 문자씩 입력받는다.
nextLine() 은 한줄 단위로 데이터를 가져온다. 개행문자 전 모든 내용을 입력 받는다.


next()로 출력되는 예제다.
```java
import java.util.Scanner;

public class Sam {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		
		System.out.print("입력값:");
		String a = s.next();
		System.out.print("출력:");
		System.out.println(a);
	}
}
```
![next출력](/assets/images/next출력.JPG)

hello world 를 쳣을때 앞에 hello 만 출력된다.



nextline()로 출력되는 예제다.
```java
import java.util.Scanner;

public class Sam2 {

	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		
		System.out.print("입력값:");
		String a = s.nextLine();
		System.out.print("nextLine 출력  :");
		System.out.println(a);		
	}
}
```
![nextline](/assets/images/nextline.JPG)

hello world 다 출력된다.