---
layout: single
title:  "Java - 오버로딩"
categories: java
tag: [java]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

### 오버로딩 (overloading)

- 한 클래스 안에 같은 이름의 메서드 여러 개를 정의하는 것
- 매개 변수 갯수에 따라서 생성자는 여러개 생성할 수 있다.
- 대표적인 예는 println() 안에들어가는 매개변수는 다르다.

------



### 오버로딩이 성립하기 위한 조건

1. 메서드 이름이 같아야 한다.
2. 매개변수의 개수 또는 타입이 달라야 한다.
3. 반환 타입은 영향없다.

![예시](/assets/images/예시.JPG)
->오버로딩의 예시이다. 정사각형, 직사각형 타입은 같은데 변수 개수가 다르고
  삼각형넓이는 타입이 다르기 때문에 오버로딩이 성립한다.





참고 : 남궁성의 java의 정석 기초편