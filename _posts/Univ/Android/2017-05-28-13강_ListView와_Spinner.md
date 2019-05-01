---
layout: post
title: 13강.ListView와 Spinner
categories: [Android]
tags: [ListView, AdapterView, Spinner]
fullview: true
comments: true
published: false
---

##### ListView와 Spinner의 상속관계
```
View - ViewGroup - AdapterView - AbsListView - ListView
                               |- AbsSpinner |- Spinner
```
[안드로이드 Object 상속도 이미지 ](http://mblogthumb4.phinf.naver.net/20150924_295/highkrs_1443021756961fGR6v_PNG/%B1%D7%B8%B22.png?type=w2)
#### ListView
* 사용자가 정의한 데이터목록을 아이템 궝하ㅕㅇ 화면에 출려하는 viewgroup의 한종류
* LinearLayout과 RelativeLayout과 같이 배치만 담당하는 레이아웃과는 다르게 사용자와 상호작용도 처리 할 수 있으며 항목의 선택이 가능함
* 표시할 항목을 Adapter객체로부터 전달받아 화면에 출력함
* AdapterView는 해당하는 여러개의 차이들 View를 통하여 화면에 표시 할 수 있음.
* Adapter로 부터 받은 항목들을 수직으로 펼쳐서 보여줌

#### Adapter와 AdapterView의 관계
 - Adapter -> 데이터 / AdapterView -> 화면
 - ListView 레이아웃의 정의
 - Adapter에 View의 속성을 정해주는 인자가 있는데 `simnple_list_item_1, simple_list_item_, simple_list_item_checked, simple_list_item_single_choice, simple_list_item_multiple_choice`가 있다.

//MK 각 항목에 대한 설명 추가

정적인 단어들 이라면 이를 따로 관리하는 것이 유지보수 관리 측면에서 대부분 더 좋다(왜냐하면 소스 레벨로 내려가서 해당 항목을 찾는 것보다는 간단히 xml항목에서 해당 이름의 Adapter를 찾아 수정하는 것이 훨씬 심플하고 게다가 해당 목록을 여러군데에서 사용하고 있다면 일일이 찾을 수고도 덜어준다)

`choiceMode 속성`
항목선택에 대한 속성, 기본은 항목의 클릭은 가능할 뿐 **선택할 수 없지만**, choiceMode속성을 지정하면 하나 이상의 항목과 상호작용을 할 수 있다.

`divider 속성`
항목사이의 구분모양을 지정

` entires 속성` imageView의 속성이나 표시할 배열을 지정함

##### Spinner
ListView를 Spinner와 함께 사용하면 다채롭게 사용가능한데 Spinner의 경우에는 클릭 할 때만 팝업으로 펼쳐게 되며 목록을 보려면 팝업을 열어야 하고 최소 두 번 클릭 해야 하고 Spinner역시 Adapter로부터 데이터를 공급 받는다.

 prompt메시지 팝업 상단에 표시할 수있다는 점 역시 ListView와는 차이를 보인다. Spinner의 메소드는 두가지가 있는데 onItemSelected 항목이 선택될 때 발생하는 이벤트와 onNothingSelected 기존 선택 된 항목이 해제 될 때에 대한 이벤트 두 가지가 존재한다.
