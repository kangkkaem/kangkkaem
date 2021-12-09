---
layout: single
title:  "Java -클래스 연습문제-4"
categories: 연습문제
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---



```java
//성적관리
public class Score {
	//필드
	String name ;
	int kor ;
	int eng;
	int mat;
	int tot;
	double avg;
	
	//기본생성자
	public Score() {
	}

	//생성자
	public Score(String name, int kor, int eng, int mat) {
		super();
		this.name = name;
		this.kor = kor;
		this.eng = eng;
		this.mat = mat;
	}
	
	//메서드
	public void total () {
		tot = kor+eng+mat;
	}
	
	public void average() {
		avg = tot/3.;
	}
	
	public void print() {
		System.out.printf("총점=%d\n평균=%.2f\n",tot,avg);
	}
}
```
```java
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Score s1 = new Score();
		
			while(true) {
			System.out.println("==================");
			System.out.print("이름 >");
			s1.name = s.next();
			System.out.print("국어 >");
			s1.kor = s.nextInt();
			System.out.print("수학 >");
			s1.eng = s.nextInt();
			System.out.print("영어 >");
			s1.mat = s.nextInt();
			s1.total();
			s1.average();
			s1.print();
			
			System.out.println("계속입력하실래요? (y/n)");
			String sel = s.next();
			if (sel.equals("n") || sel.equals("N") ) {
				break;
			}else if (sel.equals("y")||sel.equals("Y")) {
				continue;
			}else {
				System.out.println("잘못입력하셨습니다!");
				continue;
			}
		}
		System.out.println("프로그램종료!");
			
//			
//			if(sel =="y" ) {                                                    //내가 짜본 if문
//				System.out.println("==================");
//			} else {				
//				System.out.println("프로그램 종료");
//				break;			
//				}
	}
}
```

![이름출력](/assets/images/이름출력.JPG)