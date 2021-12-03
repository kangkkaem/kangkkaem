---
layout: single
title:  "Java - 조건제어문 switch문"
categories: java
tag: [java]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

## swich문 (조건 제어문)


```java
import java.util.Scanner;

public class Sample {

	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		System.out.print("시간.>");
		int time =scanner.nextInt();
		
		//switch case
		switch(time) {
		case 8:
			System.out.print("출근을 합니다.");
			break;
		case 9:
			System.out.print("회의를 합니다.");
			break;
		case 10:
			System.out.print("업무를 봅니다.");
			break;
		default:
			System.out.print("외근을 나갑니다.");
			break;
			
		}		  
	}
}
```

- if문 처럼 조건식이 true 일 경우에 블록 내부의 실행문을 실행하는 것이 아니라, 변수가 어떤 값을 갖느냐에 따라 실행문이 선택된다.
- 변수 값에 따라서 실행문이 결정되기 때문에 코드가 간결하다.



![시간 9](/assets/images/시간 9.JPG)

![외근](/assets/images/외근.JPG)

9를 찍으면 "회의를 합니다" 실행문이 선택되어서 swich문을 빠져나오게되서 출력됨.

11은 default 이므로 외근이 출력됨. default는 생략 가능하다.



- 영어 대소문자에 관계없이 똑같은 알파벳이라면 동일하게 처리되도록 만든 switch문

```java
import java.util.Scanner;

public class Sample1 {

	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		System.out.print("등급을 입력하세요 : ");
		String grade =scanner.next();
		
		switch(grade) {
			case "A":
			case "a":
				System.out.println("우수 회원입니다.");
				break;
			case "B":
			case "b":
				System.out.println("일반 회원입니다.");
				break;
			default:
				System.out.println("손님 입니다.");
		}

	}

}
```

![일반회원](/assets/images/일반회원.JPG)
