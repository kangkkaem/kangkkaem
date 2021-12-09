---
layout: single
title:  "Java -ArrayList 연습문제-2"
categories: 연습문제
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

예제)
```java
public class Product {
	//필드
	String name;
	int price;
	int quantity;
	int sum ;
	
	// 생성자
	
	//메서드 (합계구하기)
	public void sum() {
		sum = price *quantity;
	}
	
	public void print() {
		sum();
		System.out.printf("%-5s\t%d\t%d\t%d\n",name,price,quantity,sum);
	}
}
```

```java

import java.util.ArrayList;
import java.util.Scanner;

public class Product2 {

	public static void main(String[] args) {
		ArrayList<Product> array = new ArrayList<>();   
		Scanner s = new Scanner(System.in);
		boolean run =true;
		while(run) {
			System.out.println("--------------------------");
			System.out.println("1. 상품등록");
			System.out.println("2. 상품목록 ");
			System.out.println("3. 상품검색");
			System.out.println("4. 상품삭제");
			System.out.println("5. 상품수정");
			System.out.println("6. 프로그램종료");
			System.out.println("--------------------------");
			System.out.print("선택>");
			int menu= s.nextInt(); s.nextLine();
			
			switch(menu) {
			case 1:
				Product p = new Product();
				System.out.print("상품명>");
				p.name=s.next();
				System.out.print("단가>");
				p.price = s.nextInt();
				System.out.print("수량>");
				p.quantity = s.nextInt();
				array.add(p);
				break;
			case 2:
					System.out.printf("%-5s\t%s\t\t%s\t%s\n","상품명","단가","수량","합계");
					for(Product p1:array) {
						p1.print();
					}
				break;
			case 3:  //상품검색
				System.out.print("상품명>");
				String sname =s.nextLine();
				System.out.printf("%-5s\t%s\t\t%s\t%s\n","상품명","단가","수량","합계");
				boolean find =false;
				for(Product p1:array) {
					if(sname.equals(p1.name)) {
						p1.print();
						find =true;
					}
				}
				if(find == false) System.out.println("등록된 상품이 없습니다.");
				break;
			case 4:
				System.out.print("상품명>");
				sname=s.next();
				find =false;
				for(Product p1:array) {
					if(sname.equals(p1.name)) {
						array.remove(p1);
						find =true;
						break;
					}
				}
				if(!find) {
					System.out.println("삭제할 상품이 없습니다.");
				} else {
					System.out.println("삭제되었습니다.");
				}
				break;
			case 5:
				System.out.println("");
				System.out.print("수정할 상품을 입력하세요>");
				sname =s.nextLine();
				find= false;
				for(Product p1:array) {
					if (sname.equals(p1.name)) {   //수정할 상품이 있으면
						System.out.print("단가 :" + p1.price+">");
						String price = s.nextLine();
						if(!price.equals("")) 
							p1.price = Integer.parseInt(price);
						System.out.print("수량:" + p1.quantity +">");
						String quantity = s.nextLine();
						if(!quantity.equals(""))
							p1.quantity=Integer.parseInt(quantity);
						find = true;
					}
				}
				if(!find) {
					System.out.println("수정할 상품이 없습니다!");
				}else {
					System.out.println("수정이 완료되었습니다.");
				}
			
				break;
			case 6:
				run = false;
				System.out.println("프로그램종료!");
				break;
			default:
				System.out.println("1~5번을 선택하세요!");
			}
		}
	}
}
```


![수정프로그램](/assets/images/수정프로그램.JPG)

+이해될때까지 반복해서 볼것.