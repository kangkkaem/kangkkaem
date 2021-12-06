---
layout: single
title:  "Java - do while문"
categories: java
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

## do while 문

- 조건식에 의해 반복 실행한다는 점에서 while 문과 동일하다.
- 최소한 한번은 수행될 것을 보장한다.

do {

​		// 조건식의 연산결과가 참일 때 수행될 문장들을 적는다. ( 처음한번은 무조건 실행)

​		} while (조건식);

#### 예제)


```java
import java.util.Scanner;

public class Sample {

	public static void main(String[] args) {
		System.out.println("메세지를 입력하세요 :");
		System.out.println("프로그램을 종료하려면 q를 입력하세요.");
		
		Scanner scanner = new Scanner(System.in);
		String inputString;
		
		do {
			System.out.print(">");
			inputString = scanner.nextLine();
			System.out.println(inputString);
		} while( !inputString.equals("q"));
		
		System.out.println();
		System.out.println("프로그램 종료!");	
	}
}
```

![q입력](/assets/images/q입력.JPG)
