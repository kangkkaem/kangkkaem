---
layout: single
title:  "Java - 배열 연습문제-3"
categories: java
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---
배열 연습문제 -3
```java
import java.util.Scanner;

public class Sample {

	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		String[] name =new String[100];
		String[] tel= new String[100];
		String[] address= new String[100];
		int count =0; // 전체학생수 
		boolean run =true;
	
		while(run) { 
			System.out.println("");
			System.out.println("=====================================");
			System.out.println("1.주소를 등록하세요");
			System.out.println("2.주소 출력 ");
			System.out.println("3.주소 검색 ");
			System.out.println("4.프로그램 종료!");
			System.out.println("=====================================");
			System.out.print("메뉴를 선택하세요 :");
			int menu = s.nextInt();
			
			switch(menu) {
			case 1:
				System.out.print("학생명을 입력하세요 :");
				name[count]=s.next();
				System.out.print("전화번호를 입력하세요 :");
				tel[count]=s.next();
				System.out.print("주소를 입력하세요 :");
				address[count]=s.next();
				count++;
				break;
			case 2:
				for(int i = 0; i<count; i++) {
					System.out.println("이름 :" + name[i]);
					System.out.println("전화 :" + tel[i]);
					System.out.println("주소 :" + address[i]);
					System.out.println("");
				}
				break;
			case 3:
				System.out.print("검색이름 :");
				String sname=s.next();
				for(int i =0; i<count; i++) {
					if(sname.equals(name[i])) {
						System.out.println("이름 :" + name[i]);
						System.out.println("전화 :" + tel[i]);
						System.out.println("주소 :" + address[i]);
						System.out.println("");
					}
				}
				break;
			case 4:
				run =false;
				System.out.println("**프로그램 종료**");
				break;
			default:
				System.out.println("1~4번을 선택하세요!");
			}
		}
	}
}
```

![주소출력](/assets/images/주소출력.JPG)
배열 연습문제 2 번에서 살짝 다른문제이다. 구조는 똑같다.
