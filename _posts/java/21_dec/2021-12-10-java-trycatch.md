---
layout: single
title:  "Java- 예외처리 try catch "
categories: java
tag: [java]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---



자바에서는 에러 이외에 예외라고 부르는 오류가 있다. 예외란 사용자의 잘못된 조작 또는 개발자의 코딩으로 인해 발생하는 오류인데 예외는 예외처리를 통해 프로그램을 종료하지 않고 정상 실행 상태를 유지되도록 할 수있다.

- try/catch/finally 문을 사용할수있다.


### 문법

try {

    예외를 처리하길 원하는 실행 코드;

} catch (e1) {
    e1 예외가 발생할 경우에 실행될 코드;
} catch (e2) {
    e2 예외가 발생할 경우에 실행될 코드;

}
...
finally {

    예외 발생 여부와 상관없이 무조건 실행될 코드;

}