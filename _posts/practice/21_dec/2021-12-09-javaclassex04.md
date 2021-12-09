---
layout: single
title:  "Java -ArrayList 연습문제-1"
categories: 연습문제
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

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
}
```

```java
import java.util.ArrayList;
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		ArrayList<Product> array = new ArrayList<>();      //바구니(바구니의 이름 ->array)를 만들었다 .
		// 바구니 안에는 product 가 들어갔다. (들어간상태는아님)  -> product를 만들어서 안에다 넣어줘야함.
		Product p1 = new Product();          //붕어빵틀을 이용해서 붕어빵을 만들었다. p1(붕어빵)에 넣어줌 상품 
		p1.name = "냉장고" ;
		p1.price=150;
		p1.quantity = 50;
		array.add(p1);                           //바구니 1 붕어빵을 넣어준다.
		                      
		p1 = new Product();
		p1.name = "세탁기" ;
		p1.price=120;
		p1.quantity = 10;
		array.add(p1); 							//바구니 2
		
		p1 = new Product();
		p1.name = "스타일러" ;
		p1.price=180;
		p1.quantity = 50;
		array.add(p1);  							//바구니 3
		
		for(Product p:array) {   //array에서 하나씩 꺼내와서 p(product)에 넣어서 반복해라
			System.out.println("상품명 :" + p.name);
			System.out.println("상품단가 :" + p.price);
			System.out.println("판매수량 :" + p.quantity);
			p.sum();
			System.out.println("판매금액 :" +p.sum + "\n");
		}		
	}
}
```

![스타일러](/assets/images/스타일러.JPG)

![array설명](/assets/images/array설명.png)


1. arry라는 바구니를 만들었다. ( new ArrayList<>() ) 
2. 붕어빵틀(product)을 이용해서 붕어빵(객체)을 만들었다 (new Product() ) -> p1(변수명)에 상품을 넣어준다.
3. array.add(p1) 바구니에 붕어빵을 넣어준다.
4. Product p:array -> array에서 하나씩 꺼내와서 p(product) 에 넣어서 반복해라는 뜻이다.