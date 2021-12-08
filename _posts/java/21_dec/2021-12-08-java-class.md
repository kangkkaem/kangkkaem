---
layout: single
title:  "Java - Class와 객체"
categories: java
tag: [java]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

클래스는 붕어빵틀 ! 객체는 붕어빵이다.
1. 객체 : 실제로 존재하는 것. 사물 또는 개념. 
-> 객체가 가지고 있는 기능과 속성에 따라 다름
2. 클래스 : 객체를 정의 해놓은 것
-> 객체를 생성하는데 사용한다.

## 클래스
구성멤버에는 필드(객체를생성하기위한), 생성자, 메서드가 있다.

##### 예시) 클래스

```java
import java.text.DecimalFormat;

public class Product {
	//필드
	String name;
	int price;
	int quantity;
	int sum;

	//기본생성자 (자동으로들어간다. source -> generate constructor using Fields)
	public Product() {
	}

	//메소드 -> 중복해서 처리해야될경우에 사용한다.
	public void print() {
		DecimalFormat df = new DecimalFormat("#,###원");
		DecimalFormat df1 = new DecimalFormat("#,###개");
		System.out.println("");
		System.out.println("상품명 : "+ name);
		System.out.println("가격 : "+ df.format(price) );
		System.out.println("수량 : "+ df1.format(quantity));
		sum = price *quantity;
		System.out.println("금액 : "+ df.format(sum));
	}
	public Product(String name, int price, int quantity) {
		super();
		this.name = name;
		this.price = price;
		this.quantity = quantity;
	}
	public Product(String name) {
		super();
		this.name = name;
	}
}
```
##### 메인메서드

```java
import java.util.Scanner;

public class Sample {

	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		
		
		System.out.print("상품명>");
		String name=s.nextLine();
		System.out.print("상품가격>");
		int price=Integer.parseInt(s.nextLine());
		System.out.print("상품수량> ");
		int quantity =Integer.parseInt(s.nextLine());
		
		Product p1 = new Product (name, price, quantity);
		p1.print();
        }
}
```
![냉장고](/assets/images/냉장고.JPG)


 클래스를 사용해서 객체를 쉽게 사용할 수 있다.