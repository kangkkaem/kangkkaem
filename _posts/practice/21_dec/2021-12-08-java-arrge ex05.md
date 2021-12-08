---
layout: single
title:  "Java - 배열 연습문제-5"
categories: 연습문제
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---
## 배열 연습문제 -5

### 예제 )
```java
import java.text.DecimalFormat;
import java.util.Scanner;

public class Sample {

	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		boolean run = true ;
		String [] name = new String[100];
		int [] kor = new int[100];
		int [] eng = new int[100];
		int [] mat = new int[100];
		int [] sum = new int[100];
		double [] avg = new double[100];
		int count =0;  //입력학생수
		DecimalFormat df = new DecimalFormat("###.00");    //소숫점 이하 로 출력하기위해서 하는것 
		
		
		while(run) {
		System.out.println("");
		System.out.println("-------------------");
		System.out.println("1.성적등록");
		System.out.println("2.성적목록");
		System.out.println("3.성적검색");
		System.out.println("4.프로그램종료");
		System.out.println("-------------------");
		System.out.print("선택하세요 >");
		int menu = Integer.parseInt(s.nextLine());
		
		switch(menu) {
		case 1:
			System.out.print("이름 >");
			name[count]=s.nextLine();
			System.out.print("국어 >");
			kor[count] = Integer.parseInt(s.nextLine());
			System.out.print("영어 >");
			eng[count] = Integer.parseInt(s.nextLine());
			System.out.print("수학 >");
			mat[count] = Integer.parseInt(s.nextLine());
			sum[count]= kor[count]+eng[count]+mat[count];
			avg[count] =sum[count] / 3.;
			String favg = df.format(avg[count]);
			System.out.println("총점 :" + sum[count]);
			
			System.out.println("합계 :" + favg);
			count ++;
			break;
		case 2:
			
			System.out.println("이름"+"\t"+"\t"+"국어"+"\t"+"영어"+"\t"+"수학"+"\t"+"총점"+"\t"+"합계");
			System.out.println("=================================");
			for (int i = 0; i<count ; i++) {
				favg = df.format(avg[i]);
				System.out.println(name[i]+"\t"+kor[i]+"\t"+eng[i]+"\t"+mat[i]+"\t"+sum[i]+"\t"+favg);
			}
			break;
		case 3:
			System.out.print("이름>");
			String sname =s.nextLine();
			boolean find = false;
			for( int i =0 ; i<count; i++) {
				if(sname.equals(name[i])) {
					favg = df.format(avg[i]);
					System.out.println("국어:"+kor[i]);
					System.out.println("영어:"+eng[i]);
					System.out.println("수학:"+mat[i]);
					System.out.println("총점:"+sum[i]);
					System.out.println("평균:"+favg);
					find =true;
				}
			}
			if(find==false) System.out.println(" 등록된 이름이 없습니다.");
			break;
		case 4:
			run = false;
			System.out.println("프로그램종료!");
			break;
		default:
			System.out.println("1~4를 선택하세요!");
		}
		}

	} //main
} //class
```

![성적국어](/assets/images/성적국어.JPG)

------

새롭게 알게된 개념 ! 

### DecimalFormat  

-> 10진수의 값을 원하는 포멧으로 변형해 주는 클래스

DecimalFormat df = new DecimalFormat("");

-> new 연산자를 사용한다. format 메소드를 사용해서 특정 패턴을 포맷가능하다.

| Format | 설명                                   |
| ------ | -------------------------------------- |
| 0      | 10진수, 값이 없는 자리는 0으로 채운다. |
| #      | 10진수, 값이 없는 자리는 나타나지 않음 |
| .      | 소수점 이하 나타냄                     |
| -      | 음수 부호                              |
| ,      | 단위 구분자                            |
| E      | 지수 기호                              |
| %      | 퍼센트                                 |
| '      | escape문자                             |

출처 : https://docs.oracle.com/en/java/javase/12/docs/api/java.base/java/text/DecimalFormat.html



## DecimalFormat 예시

```java
import java.text.DecimalFormat;

public class Test {

	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		DecimalFormat df = new DecimalFormat("###,###");
		
		int a= 123;
		int b= 1234;
		int c= 12345;
		int d= 123456;
		int f= 1000000000;
		
		System.out.println(df.format(a));
		System.out.println(df.format(b));
		System.out.println(df.format(c));
		System.out.println(df.format(d));
		System.out.println(df.format(f));
	}
}

```

![deci](/assets/images/deci.JPG)
