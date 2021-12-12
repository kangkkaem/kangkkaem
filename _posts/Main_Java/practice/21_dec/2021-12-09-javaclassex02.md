---
layout: single
title:  "Java -클래스 연습문제-3"
categories: 연습문제
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

예제)계산기 프로그램
```java
public class Area {
	
	//필드
	int type ; // 1. 정사각형, 2. 직사각형 3. 삼각형 4. 원
	
	//생성자
	
	//메서드
	
	public int area1 (int x) {
		return x*x;
	}
	
	public int area2 (int x, int y) {
		return x*y;
	}
	
	public double area3(int x, int y) {
		return (x* y)/2.;
	}
	
	public double area4(int x) {
		return x*x*3.14;
	}
}
```
```java
import java.util.Scanner;

public class Main2 {

	private static int tp;

	public static void main(String[] args) {
		Scanner s= new Scanner(System.in);
		Area area= new Area();
		boolean run = true;
		while(run) {
		System.out.println("------------------------------------------");
		System.out.println("1.정사각형    2.직사각형    3.삼각형    4.원    5.종료");
		System.out.println("--------------------------------------------");
		System.out.print("선택>");
		int menu = s.nextInt();
		
		
		switch(menu) {
			case 1: 
				System.out.print("한변의 길이 >");
				int x = s. nextInt();
				int area1 = area.area1(x);
				System.out.printf("한변의 길이가 %d 인 정사각형의 넓이는 %d\n",x,area1);
				System.out.println("");
				
				break;
			case 2:
				System.out.print("가로 길이 >");
				x = s. nextInt();
				System.out.print("세로 높이 >");
				int y= s. nextInt();
				int area2 = area.area2(x,y);
				System.out.printf("가로 길이가 %d , 세로 높이 %d 직사각형의 넓이는 %d\n",x,y,area2);
				System.out.println("");
				break;
			case 3:
				System.out.print("밑변 >");
				x = s. nextInt();
				System.out.print("높이 >");
				y = s. nextInt();
				double area3 = area.area3(x,y);
				System.out.printf("밑변의 길이가 %d, 높이가 %d 인 삼각형의 넓이는 %.2f\n",x,y,area3);
				System.out.println("");
				break;
			case 4:
				System.out.print("반지름 >");
				x = s. nextInt();
				double area4 = area.area4(x);
				System.out.printf("반지름 %d 인 원의 넓이는 %.1f\n",x,area4);
				System.out.println("");
				break;
			case 5:
				 run= false;
				 System.out.println("프로그램 종료!");
				break;
			default:
				System.out.println("1~4번을 선택하세요!");
		}
    }
}
```
![직사각형](/assets/images/직사각형.JPG)