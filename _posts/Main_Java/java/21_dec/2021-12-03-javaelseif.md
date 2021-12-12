---
layout: single
title:  "Java - if-else문"
categories: java
tag: [java]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

조건문이 여러개인 if문도 있다. 

```java
import java.util.Scanner;

public class Sample {

	public static void main(String[] args) {
		Scanner scanner= new Scanner(System.in);
		System.out.print("상품명을 입력하세요.>");
		String name = scanner.next();
		System.out.print("단가를 입력하세요.>");
		int price = scanner.nextInt();
		System.out.print("수량을 입력하세요.>");
		int num = scanner.nextInt();
		int sum = price *num;
		System.out.print("금액: "+sum+"\n");
		
		String result = "";
		
		if(sum>=1000) {
			result = "최우수";
			
		} else if(sum>=500) {
			result = "우수";
		} else {
			result = "분발";
		}
		System.out.println("결과: "+result);
	}

}
```
상품명, 단가, 수량을 화면으로 입력받고 금액과 등급을 나눠서 출력해준다.

if문으로 최우수, 우수, 분발로 등급을 나눴다. 

조건식에 만족되는 등급을 출력하게 될것이다.

![상품명](/assets/images/상품명.JPG)