---
layout: single
title:  "Java - 배열"
categories: java
tag: [연습문제]
toc: true
author_profile: true
search: true
sidebar:
  nav: "docs"
---


```java
public class Sample {

	public static void main(String[] args) {
		//배열 
		int[] a = {30,47,504,204,402};
		a[0] = 300;
		
		int sum =0;
		for(int i= 0; i<a.length; i++) {
			System.out.println(a[i]);
			sum=sum+a[i];
		}
		System.out.println("합계: " + sum);
		
		double avg = sum/(double)a.length;
		System.out.println("평균: " + avg);
		
		String[] name = {"홍길동","이순신","강감찬", "성춘향","이몽룡"};
		for(int i = 0; i<name.length; i++) {
			System.out.println(name[i]);
		}
		
		
		//정수타입
		int[] b =new int[5]; //어떤값이들어갈지모를때 방만만들어줌
		b[0] = 2;
		b[4] =3;
		for(int i =0; i<b.length; i++) {
			System.out.println(b[i]);
		}
		//실수타입
		double[] c = new double[3];
		c[0] =1.123;
		c[2] = 2.145;
		for(int i= 0; i<c.length; i++) {
			System.out.println(c[i]);
			
		//문자열타입
		String[] d = new String[3];
		d[0] ="홍길동";
		d[2] ="심청이";
		for(int i=0; i<d.length; i++) {
	         System.out.println(d[i]);

		}
		}
	} 	
}
```