---
layout: single
title:  "Java - 배열 연습문제-4"
categories: 연습문제
tag: [연습문제]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---
## 배열 연습문제 -4

### 예제 )

```java

import java.util.Scanner;

public class Sample {

	public static void main(String[] args) {
		
			Scanner s = new Scanner(System.in);
			boolean run = true;
			String [] name =new String[100];
			int [] price =new int[100];
			int [] qua = new int[100];
			int [] sum = new int[100];
			int count = 0;
			while(run) {
			System.out.println("======================");
			System.out.println("1.상품등록");
			System.out.println("2.상품목록");
			System.out.println("3.상품검색");
			System.out.println("4.프로그램 종료!");
			System.out.println("======================");
			System.out.print("메뉴를 선택하세요 :");
			String smenu = s.nextLine();
			int menu = Integer.parseInt(smenu);
			
			switch(menu) {
			case 1:
				System.out.print("상품을 등록하세요 :");
				name[count]=s.nextLine();
				System.out.print("가격을 입력하세요 :");
				String price1 = s.nextLine();
				price[count]=Integer.parseInt(price1);
				System.out.print("수량을 입력하세요 :");
				String qua1= s.nextLine();
				qua[count] = Integer.parseInt(qua1);
				sum[count] = price[count] *qua[count];
				System.out.println("판매금액:" + sum[count]);
				System.out.println("상품등록완료!");
				count++;
				break;
			case 2:
				System.out.println("상품명"+"\t"+"가격"+"\t"+"수량"+"\t"+"총합");
				System.out.println("========================================");

				for(int i =0; i<count; i++) {
					System.out.println(name[i]+"\t"+price[i]+"\t"+qua[i]+"\t"+sum[i]);
				}
				break;
			case 3:
				System.out.print("상품이름 :");
				String sname = s.nextLine();
				boolean find = false;
				for(int i = 0; i<count; i++) {
					if(name[i].equals(sname)) {
						System.out.println("상품이름:"+name[i]);
						System.out.println("가격:"+price[i]);
						System.out.println("수량:"+qua[i]);
						System.out.println("총합:"+sum[i]);
						find = true;
					} 
				}
				if(find==false) System.out.println(" 등록된 상품이 없습니다.");
				break;
			case 4:
				run = false;
				System.out.println("프로그램 종료!");
				break;
			default:
				System.out.println("1~4번을 선택하세요!");
			}
		}
	}
}
```
![상품출력](/assets/images/상품출력.PNG)
3번 문제와 유사한 문제다.

------

추가된것은 case 3 : 에서 검색결과와 맞지않으면 불린을 써서 false로 출력이나오게된다.

1. 스캐너로 입력값을 입력받는다.
2. while 문을 true 로 해서 무한루프를 돌리기 위해 boolean 을 선언해준다.
3. 입력값이 계속 입력받을 수 있게 while문 안에서 menu를 입력받는다.
4. 여기서(while) 공백 값을 입력해도 에러가 나지 않게 nextline을 사용한다. 
5. menu값에 따라 case1 ~4 : 까지 출력된다.
6. 먼저, case 1: price 값은 int로 변수지정을 했는데 String 으로 변환하기위해서  Integer.parseInt를 사용.
7. qua 도 마찬가지이다.
8. case 2: 상품목록을 출력 for 문을 사용함
9. case 3: 검색결과가 틀릴경우를 생각해서 boolean타입을 사용했다. equals 메소드를 사용해서 검색값이 틀린지 아닌지 확인하고 맞다면 if 문에 해당하는 값을 출력한다.
10. case 4: while 문이 false 가 되어서 빠져나와서 종료
11. default : menu에 case에 해당하지않는 값을 입력할 경우 출력

------

나름대로 정리를 해봤다. 틀린부분이 있다면 다시와서 수정 추가할예정이다.
계속 반복해서 같은 유형의 문제를 푸니까 어느정도 이해는 가는것같다.