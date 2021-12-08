---
layout: single
title:  "Java -클래스 연습문제-1"
categories: 연습문제
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

### 예제)

```java
public class Area {
	// 필드 
	// 생성자
	
	//메서드 (정사각형 넓이)
	public int area(int a) {        
		return a*a ;						
	}
	//메서드 (직사각형의 넓이 )
	public int area(int a, int b) {
		return a*b;
	}
	//메서드 (삼각형의 넓이)
	public double area(int a, double b) {       
		return (a*b)/2;
	}
}
```

```java

import java.util.Scanner;

public class Sample {

	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Area a = new Area();
		boolean run = true;
			while(run) {
			System.out.println("--------------------------------------------");
			System.out.println("1. 정사각형    2. 직사각형    3. 삼각형    4. 종료");
			System.out.println("-------------------------------------------");
			System.out.print("선택>");;
			int menu = s.nextInt();
		
			
			switch(menu) {
			case 1:
				System.out.print("한변의 길이 >");
				int length= s.nextInt();
				System.out.printf("정사각형넓이=%d\n",a.area(length));
				break;
			case 2:
				System.out.print("밑변 >");
				int a1= s.nextInt();
				System.out.print("높이 >");
				int a2= s.nextInt();
				System.out.printf("정사각형넓이=%d\n", a.area(a1, a2));
				break;
			case 3:
				System.out.print("밑변 >");
				int b1= s.nextInt();
				System.out.print("높이 >");
				double b2= s.nextDouble();
				System.out.printf("삼각형넓이=%.2f\n",a.area(b1, b2));
				break;
			case 4:
				run = false;
				System.out.println("프로그램종료");
				break;
			default:
				System.out.println("1~3번을 선택해주세요!");
			}
		}
	}
}
```
![정사각형](/assets/images/정사각형.JPG)