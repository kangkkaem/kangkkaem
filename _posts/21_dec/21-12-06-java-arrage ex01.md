---
layout: single
title:  "Java - 배열 연습문제"
categories: java
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---



```java
public class Sample {

	public static void main(String[] args) {
		//세사람 성적구하는 프로그램
		String[] name= {"홍길동" , "이순신" , "강감찬" };
		int[] kor = {90, 80, 95};
		int[] eng = {70, 80, 96};
		int[] mat = {88, 70, 50};
		
		for(int i =0; i<name.length; i++) {
			int tot = kor[i]+eng[i]+mat[i];
			double avg = tot/3.;
			System.out.println(name[i]+ "\t" + tot+ "\t" + avg);
		}
		System.out.println("=================================");
		String[] pname = {"세탁기" , "냉장고", "TV" };
		int[] price = {150, 300, 200};
		for(int i=0; i<pname.length; i++) {
			System.out.println(pname[i]+ "\t" +price[i]);
		}
	}
}
```