---
layout: single
title:  "Java - SimpleDateFormat "
categories: 기타지식
tag: [기타지식]
toc: false
author_profile: true
search: true
sidebar:
  nav: "docs"
---

SimpleDateFormat 는 날짜를 형식화하고 구문 분석하기위한 구체적인 클래스이다.

|   y   |          년           |   Year    |     1996; 96     |
| :---: | :-------------------: | :-------: | :--------------: |
| **M** |        **월**         | **Month** | **Jul; jul; 07** |
| **d** |        **일**         | **숫자**  |      **10**      |
| **H** | **시간(하루 24시간)** | **숫자**  |      **0**       |
| **h** |    **시간(AM/PM)**    | **숫자**  |      **12**      |
| **m** |        **분**         | **숫자**  |      **30**      |
| **s** |        **초**         | **숫자**  |      **55**      |



**예시)**

```java

import java.text.SimpleDateFormat;
import java.util.Date;

public class Test {

	public static void main(String[] args) {
		SimpleDateFormat sdf = new SimpleDateFormat ("yyyy.MM.dd HH:mm:ss");
		
		Date date = new Date();
		
		System.out.println(sdf.format(date));
	}

}
```

![오늘](/assets/images/오늘.JPG)

