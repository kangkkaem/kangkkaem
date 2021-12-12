---
layout: single
title:  "Java - 총점과 평균 출력 프로그램"
categories: 연습문제
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

## 문제

과목 점수를 입력받아서 총점과 평균을 출력해주는 프로그램

```java
import java.util.Scanner;

public class Sample {

	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		boolean run = true;
		while(run) {  //true인 동안에 실행
			System.out.println("");
			System.out.println("---------------------------");
			System.out.println("1.성적입력");
			System.out.println("2.프로그램종료!");
			System.out.println("---------------------------");
			System.out.printf("메뉴를 선택하세요:");
			int menu = scanner.nextInt();
			switch(menu) { //menu 값에따라서 실행.
			case 1:
				System.out.print("국어 :");
				int kor = scanner.nextInt();
				System.out.print("영어 :");
				int eng = scanner.nextInt();
			
				int tot = kor+eng;
				double avg = tot/2.;
				System.out.println("총점 :" +tot);
				System.out.println("평균 :" +avg);				
				break;
			case 2:
				run= false; //종료되게 하는것 while 문을 빠져나온다.
				System.out.println("프로그램종료!");
				break;
			default:
				System.out.println("1번 또는 2번을 선택하세요!");
			}
		}
	}
}

```

![성적프로그램](/assets/images/성적프로그램.JPG)

1.  while 문 true 로 해서 무한루프로 돌려지면서 입력값을 받는다.
2.  switch 으로 menu 값에 따라서 실행값을 출력하는데 
3. case 1: 성적입력값으로 국어 , 영어 성적을 입력받는다. +총점, 평균도계산
4. case 2: run = false 되어서 무한루프가 종료되고  while 문 밖으로 빠져나온다.
5. 1번 2번이아닌 값 default 가 입력되면 다시 처음으로 돌아가서 입력값을 받는다.

