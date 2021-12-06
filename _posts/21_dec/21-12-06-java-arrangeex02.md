---
layout: single
title:  "Java - 배열 연습문제-2"
categories: java
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---




```java
import java.util.Scanner;

public class Sample {

	public static void main(String[] args) {
		//성적입력받아서 출력
		Scanner s = new Scanner(System.in);
		boolean run = true;
		int count =0; // 전체학생수 (while 밖으로 빼줘야한다.)
		int index = 0; // 학생입력한수 1씩증가
		String[] name =new String[100];
		int[] kor= new int[100];
		int[] eng= new int[100];
		int[] tot=new int[100];
		double[] avg = new double[100];
		
		
		
		while(run) { 
			System.out.println("");
			System.out.println("================================");
			System.out.println("1.학생수를 입력하세요 :");
			System.out.println("2.신규학생을 등록하세요 :");
			System.out.println("3.학생 목록을 출력");
			System.out.println("4. 프로그램종료");
			System.out.println("================================");
			System.out.print("메뉴를 선택하세요 :");
			int menu = s.nextInt();
			
			switch(menu) {
			case 1:   //전체학생수 입력
				System.out.print("전체학생수 :");
				count=s.nextInt();
				
				break;
			case 2:  //신규학생등록
				System.out.print("학생명 :");
				name[index] = s.next();
				System.out.print("국어점수를 입력하세요:");
				kor[index] =s.nextInt();
				System.out.print("영어점수를 입력하세요:");
				eng[index] =s.nextInt();
				tot[index] =kor[index]+eng[index];
				avg[index] = tot[index]/2.;
				index++;
				break;
			case 3: //전체학생목록출력
				System.out.println("==전체학생목록==");
				for(int i=0; i<count; i++) {
					System.out.println(i+"\t"+name[i]+ "\t"+kor[i]+"\t"+eng[i]+"\t"+tot[i]);
				}
				
				break;
			case 4:
				run=false;
				System.out.println("프로그램종료!");
				break;
			default:
				System.out.println("1~4번을 선택하세요!");
			}
		}
	}
}
```








점점 코드 줄이 늘어나기 시작한다. ! 
뭔가 뿌듯하면서도 더 머리아파질거같아서 두렵다 ,,
