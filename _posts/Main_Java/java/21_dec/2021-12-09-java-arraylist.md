---
layout: single
title:  "Java -ArrayList"
categories: java
tag: [java]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

## ArrayList

- Array로 객체를 생성할때 배열의 크기를 넣어주게 되있다.
- ArrayList클래스는 데이터를 추가하는대로 사이즈가 늘어난다. 
   -> 배열방이 다차면 두배로 늘려주는 작업을 함. 검색할때는 고정된곳에서 검색
- ArrayList는 기존의 vector 를 개선한것 
- 저장순서가 유지되고 중복을 허용한다.
- 데이터 저장공간으로 배열을 사용한다.



1. ArrayList 생성 

   ```java
    ArrayList<String> array = new ArrayList<>();
   ```

![3개출력](/assets/images/3개출력.JPG)


2. ArrayList 값 추가

   ```java
   public class Array
   {
       public static void main(String[] args)
       {
           ArrayList<String> array = new ArrayList<>();
           array.add("냉장고");
           array.add("세탁기");
           array.add("청소기");
           
           System.out.println(array);
       }
   }
   ```

![2개출력](/assets/images/2개출력.JPG)

3.ArrayList 값 삭제

```java
public class Array
{
    public static void main(String[] args)
    {
        ArrayList<String> array = new ArrayList<>();
        array.add("냉장고");
        array.add("세탁기");
        array.add("청소기");
        
        System.out.println(array);
        array.remove("냉장고");
        System.out.println(array);
        
    }
}
```

4. ArrayList 크기 구하기

```java
System.out.println(array.size());   // 값은 2
```

5. ArrayList 값 출력

```java
System.out.println(array.get(0));   // 세탁기
```

6. ArrayList 값 검색

```java
public class Array
{
    public static void main(String[] args)
    {
        ArrayList<String> array = new ArrayList<>();
        array.add("세탁기");
        array.add("청소기");
        
        System.out.println(array.contains("세탁기"));
        System.out.println(array.contains("냉장고"));
    }
}
```

![값검색](/assets/images/값검색.JPG)

오우 이렇게 편리한 메소드가 있었다니 ! 기억해둬야겠다.
