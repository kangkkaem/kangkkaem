---
layout: single
title:  "Java -클래스 연습문제-2"
categories: 연습문제
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---


```java
import java.text.DecimalFormat;

public class Bank {
	    //필드
		int balance; // 잔액
		
		//생성자
		
		//메서드 (입금)
		public int input(int money) {
			return balance=balance +money;
		}

		//메서드 (출금)
		public boolean output(int money) {
			if(balance>=money) {
				balance=balance-money;
				return true;
		} else {
			return false;
		}		
	}	
}
```
```java
import java.text.DecimalFormat;
import java.util.Scanner;

import ex13.Bank;

public class Main {

	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		DecimalFormat df = new DecimalFormat("#,###원");
		Bank b = new Bank();
		boolean run = true;
		int money = 0;
		
		while(run) {
		System.out.println("-------------------");
		System.out.println("1. 예금액 ");
		System.out.println("2. 출금 ");
		System.out.println("3. 잔액 ");
		System.out.println("4. 종료 ");
		System.out.println("-------------------");
		System.out.print("선택>");
		int menu = s.nextInt();
		
		switch(menu) {
		case 1:
			System.out.print("입금액>");
			money= s.nextInt();
			b.input(money);
			System.out.println("입금성공!");
			System.out.println("입금:" + df.format(b.balance));
			break;
		case 2:
			
			System.out.print("출금액>");
			money = s.nextInt();
			boolean success = b.output(money);
			if(success==false) {
				System.out.println("잔액부족\n잔고:" + df.format(b.balance));
			} else {
				System.out.println("잔액 :" + df.format(b.balance));
				
			}
			break;
		case 3:
			System.out.println("잔액:" + df.format(b.balance));
			break;
		case 4:
			run=false;
			System.out.println("프로그램 종료!");
			break;
		default:
			System.out.println("1~4번을 선택하세요!");
			}
		}
	}
}
```
![은행잔고](/assets/images/은행잔고.JPG)

------

혼자서 짜보던거다. 분명히 했던건데 class 를 사용해서 그런지 너무 헷갈렸다 ㅠㅠ
아직 완벽한 개념 이해는 안됐지만 , 이것또한 여러번 하다보면 손에 익겠지 ! 
그리고 넘 생각을 안하고 프로그램을 짜려고 해서 더오래걸린것도있다.
구조를 생각하면서 짜봐야할것같다.

