---
layout: single
title:  "Java- 접근 제한자 "
categories: java
tag: [java]
toc: true
author_profile: true
search: true
sidebar:
  nav: "docs"
---

## 접근 제한자 

: 라이브러리 클래스를 설계할 때에는 외부 클래스에서 접근 할 수 있는 멤버로 구분해서 필드, 생성자, 메서드를 설계하는 것이 좋다.

- public : 외부 클래스가 자유롭게 사용할 수 있는 공개 멤버를 만든다

- protected : 같은 패키지 또는 자식 클래스에서 사용할 수 있는 멤버를 만든다.
- private : 단어의 뜻 그대로 개인적인 것이라 외부에 노출되지 않는 멤버를 만든다.
- default : 같은 패키지에 소속된 클래스에서만 사용할 수 있는 멤버를 만든다.

private > default > protected > public   
<---------------------------------------**접근제한이강화**







### 클래스의 접근제한

```
//default 접근 제한
class 클래스 { ... }

//public 접근 제한
public class 클래스 { ... }
```

: 고려사항은 같은 패키지 내에서만 사용할것인지, 다른 패키지에서도 사용할 수 있도록 할 것인지 결정해야한다. default와 public 두가지를 적용할수있다.







### 생성자의 접근 제한

```
public class ClassName {
	//public 접근 제한
	public ClassName(...) {...}
	
	//protected 접근 제한
	protected ClassName(...){...}
	
	//default 접근 제한
	ClassName(...){...}
	
	//private 접근 제한
	private ClassName(...){...}
}
```

: 객체를 생성하기 위해서는 new 연산자로 생성자를 호출해야한다. 하지만 생성자가 어디에서나 호출할 수 있는 것은 아니다. 생성자가 어떤 접근 제한을 갖느냐에 따라 호출 가능 여부가 결정된다.







### 필드와 메소드의 접근 제한

```
//필드 선언
[public : protected : private][static] 타입 필드;

//메소드 선언
[public : protected : private][static] 리턴 타입 메소드(...) {...}
```

: 고려사항은 클래스 내부에서만 사용할 것인지, 패키지 내에서만 사용할 것인지, 아니면 다른 패키지에서도 사용할 수 있도록 할것인지 결정해야한다.
