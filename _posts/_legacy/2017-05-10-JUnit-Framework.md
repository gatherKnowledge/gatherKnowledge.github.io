---
layout: post
title: JUnit과 TDD
categories: [JUnit]
tags: [TestFramework]
fullview: true
comments: true
published: true
---

##### 단위 테스트를 해야 하는 이유
> 웹 테스트에 대한 생산성, **퇴근 길에 이것 때문에 기존 기능 안되는것 아냐??** 하는 상황 미연에 방지, 결과를 사람의 눈으로 직접하는데에 대한 신뢰성, 결과 값 예측과 결과를 쌍으로 제공 받는다(이 말은 다른데서 긁어 온 말인데 이해 안됨)

##### JUnit 명명 규칙
> 메소드 명 앞에 `test`접두어
  - add() --> testAdd()

##### 사용되는 메서드
> Assert를 접두어로 하는 JUnit 패키지의 메서드
```
assertArrayEquals(a,b) : 배열 a와b가 일치함을 확인
assertEquals(a,b) : 객체 a와b의 값이 같은지 확인
assertSame(a,b) : 객체 a와b가 같은 객체임을 확인
assertTrue(a) : a가 참인지 확인
assertNotNull(a) : a객체가 null이 아님을 확인
이외에도 다양한 단정문이 존재합니다. 자세한 내용은 아래 링크를 가시면 확인하실 수 있습니다. http://junit.sourceforge.net/javadoc/org/junit/Assert.html
```

##### 느낀점
당연히 메서드나 명명 규칙에 대해 아는 것도 중요하긴 하겠지만 `어떤 방식으로 테스트를 해야겠다` 웹개발 같은 경우에는 특정한 상황을 맞춰주는 것이 상당히 신경 쓰이는데 혹은 아예 불가능할 수도 있고, 예를 들면 `HttpServletRequest의 getParameterMap()`의 key값이 id인 String[]을 얻는다고 가정했을 때, 다음과 같은 값을 테스트 코드로 테스트 할 수 있을까 
