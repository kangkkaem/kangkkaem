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

### 예제)

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

계속 비슷한 문제로 반복학습을 하고있는데 완벽하게 이해한후 보지않고 내머리로 작성할 수 있는 정도가 되야할것같다.
ArrayList 에 대한 개념이 어느정도는 이해가 된것같다! 근데 뭔가 부족한 느낌이라
책을 보면서 한번더 학습할것이다. 

------

아 그리고 특히 !! 나혼자 짜볼때 계속 실수하는 부분이 있는데 	array.add(); 이부분을 계속 까먹어서 안적는다. (바구니에 담아야 출력이될것아니니,, 꼭 적어 ..)

switch 문에 break; 계속 까먹는거랑 비슷한 실수같다 ㅎㅎ.. 
한참 고민끝에 해결하긴 하지만 속도가 빨리질수록 좋을테니 꼭 유념해서 코딩하쟈