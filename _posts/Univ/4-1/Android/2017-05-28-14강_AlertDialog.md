---
layout: post
title: 14강.AlertDialog
categories: [Android]
tags: [activity, intent]
fullview: true
comments: true
published: false
---
#### AlertDialog
AlertDialog는 사용자에게 전달 사항을 알리고 질문을 통해 사용자의 선택을 받아 들이는 기본적인 통신 수단으로 액티비티 위에 나타나는 작은 윈도우이며, 다이얼로그 아래에 놓인 액티비티는 포커스를 잃고 다이얼로그가 사용자와의 상호작용을 처리하게 된다 _물론 버전마다 차이가 있어 특정 버전에서는 아래 놓인 액티비티가 클릭 되는 경우도 있다_ 다이얼로그의 종류에는  AlertDialog, ProgressDialog, DatePickerDialog, TimepickerDialog등이 있다.

<!-- <img src="{{site.BASE_PATH}}/images/post/DialogImages.png"> -->

 * 제목은 하나, 최대 세개의 버튼을 추가 할 수 있고, 선택 가능한 품목을 표시할 수 있는 대화상자이다.
 * Toast도 사용자에게 알리는 방법이지만 사용자와의 상호작용을 할 수 없기 때문에 Dialog보다는 사용성이 떨어지게 된다._Toast보다 좀 더 복잡한 내용을 전달 할 때 사용된다._
 * AlertDialog는 생성자가 protected로 숨겨져 있으므로 직접적으로 생서할 수 없어 내부 클래스인 Builder를 통해 생성해야 한다.
 * Toast와는 달리(Long, short의 인자를 준다) AlertDialog는 사용자가닫을 때까지는 사라지지지 않으므로 장시간동안 메시지를 표시 할 수 있음

#### AlertDialog의 버튼
Alert이 열리면 닫힐 때까지 뒤쪽의 액티비티는 실행 금지상태가 된다. 긍정, 부정, 중립으로 각각 명명돼 있고 다음 메서드들로 붙혀줄 수 있다.

> setPositiveButton()<br>setNeutralButton()<br>setNegativeButton()

~~클릭  리스너 onClick메소드에 아무코드가 없으면 핸들러가 비어있는 버튼을 이요하여 다이얼로그가 닫히는 동작만 함
!! 다이얼로그쪽은 Builder가 구현을 해 줘야 한다~~

클릭 리스너가 null인 경우, 해당 다이얼로그를 닫기 버튼을 만든 것과 같은 기능을 수행시키게 할 수 있습니다. 속성 중에 setCancelable(false)이 있는데 이를 false로 설정할 경우 의 경우 스마트폰의 Back버튼에 대한 동작이 불가능하게 된다(사용자의 response에 대한 답을 꼭 얻어야 하는 경우 이용할 수 있겠습니다.)

---
~~** 라마인드 !!
1.activity.xml/R.ajva/Strings.xml 등등 기초적인 파일들의 구성
 - view, viewgroup, widget, textView, ImageView
 - Layout - linearLayout, relativeLayout, FrameLayout
2.CustomView를 통해서 Canvas, Paint
 - Toast, 소리 출력
3.EventHandling
 - callback,listener ..
 - 리스너의 경우에는 인터페이스 !!
 - 재활용, 실행순서
4.액티비티
 - 인텐트
5.Adapter
6.AlertDialog~~
