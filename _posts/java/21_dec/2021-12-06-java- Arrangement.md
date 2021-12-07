---
layout: single
title:  "Java - 배열"
categories: java
tag: [java]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

## 배열

**예제)**

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
			
		}
	}
} 	
```
![배열출력](/assets/images/배열출력.JPG)



- **배열** : *같은 타입 *의 여러변수를 하나의 묶음으로 다루는것

------

int [] score = new int[5];             // 5개의 int 값을 저장할 수 있는 배열을 생성한다.

------

![score](/assets/images/score.PNG)

```
타입[] 변수이름;   //배열을 선언(배열을 다루기 위한 참조변수 선언)
변수이름 = new 타입[길이];     // 배열을 생성(실제 저장공간을 생성)
```



- 인덱스의 범위는 0부터 배열길이 -1까지 이다.


```java
public class Sample {

	public static void main(String[] args) {
				int []  a=new int [5];
				a[0] = 3;
				a[1] = 5;
				for(int i = 0; i <a.length; i++) {
					System.out.println(a[i]);
				}
				
				System.out.println("----------");
				int[] b = {3,5};
				for(int i = 0; i <b.length; i++) {
					System.out.println(b[i]);
				}
				
				int[] [] c = new int[2][3];   //2차원 배열 개념 넣기
				c[0][0]=1;
				c[0][1]=2;
				c[0][2]=3;
				c[1][0]=4;
				c[1][1]=5;
				c[1][2]=6;
				System.out.println("----------");
				
				for(int i=0; i<c.length ; i++) {
					for (int j =0; j<c[i].length; j++) {
						System.out.print(c[i][j]+ "\t");
					}
					System.out.println("");
				}
				
				System.out.println("----------");
				String[][] d = {
						{"A","B","C" },
						{"D", "E" },
						{"F", "G", "H","I"}
				};
				for(int i=0; i<d.length ; i++) {               //행
					for (int j =0; j<d[i].length; j++) {       //열
						System.out.print(d[i][j]+ "\t");
					}
					System.out.println("");
				}
		}
}
```
![이차원배열](/assets/images/이차원배열.JPG)

2차원 배열의 선언

------

타입 변수이름[][] [][];
ex ) int [][] score = new int[4][3]    // 4행 3열의 2차원 배열을 선언한다.

------

- 2차원 배열은 주로 테이블 형태의 데이터를 담는데 사용한다.
- 예시의 문장이 실행되면 , 밑에 표와 같은 4행 3열의 데이터를 저장할 수 있는 공간이 마련된다.

| score[0][0] | score[0][1] |score[0][2] |
| ----------- | ------- | ------- |
| **score[1][0]** | **score[1][1]** | **score[1][2]** |
| **score[2][0]** | **score[2][1]** | **score[2][2]** |
| **score[3][0]** | **score[3][1]** | **score[3][2]** |

