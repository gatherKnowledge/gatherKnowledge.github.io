---
layout: post
title: 8강.Toast와 Canvas
categories: [Android]
tags: [Canvas, Toast]
fullview: true
comments: true
published: false
---
#### Paint 속성
그리기에 대한 속성정보를 가지는 개체이며 모든 그리기 메서드에게 인수로 전달된다

1. setAntiAlias(Boolean) : 원을 그릴 때 혹은 휘어진 부분을 그릴 때 픽셀로 구현돼 있기 때문에 태생적으로 휘어진 것을 표현 할 때 역시 직각을 이용해서 그리게 되는데 이를 보정해주는 기능
2. setColor
3. setStyle : 사각형이나 원처럼 내부가 채워진 도형을 그릴 때 외곽선의 모양을 결정하는 속성
4. setStrokeCap : 선의 끝 모양을 지정(뭉뚝하게, 조금 벗어나게, 각지게)
5. setStrokeJoin : 선들이 만나는 곳의 모양
```
 --     --\     --
  |       |       |
miter, BEVEL, ROUND,
= MITER : 모서리를 90도 각진 형태 (Default)
= BEVEL : 모서리가 깍인 형태
= ROUND : 둥근 형태
```

---
onDraw 메서드
Paint 객체를 생성해서 도형이나 점, 선, 면을 그리고 canvas객체에 좌표 값과 paint객체를 집어넣으면 해당 Cavnvas에 그릴 수 있게 된다
```
Paint pnt = new Patint () ;
canvas.drawRact(120,  100, 320, 500, pnt) ;
```
---
#### Toast
작은 팝업 상자. 사용자에게 임시적인 알림사항을 전달 때, 디버깅용으로도 사용할 때 유용하다. 플로팅 형태로 화면 하단에 잠시 나타나며 일정시간이 지나면 사라짐_Length.Long, short에 의해 결정_, Focus를 받지않습니다.

---
#### 소리 출력
static MediaPlayer create(Context context, int resid)를 호출하고 소리파일이 `raw폴더`에 저장되므로 ID는 R.raw.id의 형식으로 저장되고, R.java파일에 자동으로 등록된다.

SoundPool 객체는 효과음이나 음악을 메모리에 적재하고 실행하는 방식이다. 여러 개의 효과음을 적재해놓고 실행 할 수 있다. load : 메모리에 음악을 올린다. play : 실행

AudioManager 안드로이드 시스템(안드로이드 프레임워크)에서 기본적으로 제공되는 객체로 출력장비와 오디오를 관리하고, 별도의 파일(음악)을 준비하지도 않고 시스템 제공 오디오 파일을 사용 할 수있다. `playSoundEffect()` 효과음 종류를 설정해주면 소리가 출력된다.
