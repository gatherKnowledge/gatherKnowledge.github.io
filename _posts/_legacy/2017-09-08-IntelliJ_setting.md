---
layout: post
title: 이클립스 프로젝트 IntelliJ로 이동시키기
categories: [intelliJ]
tags: [intelliJ, eclipse, IDE]
fullview: true
comments: true
published: true
---
##### VCS에 의해서 관리되고 있는 프로젝트 일 경우(사실 별 차이는 없다.)
1. intelliJ 첫화면 - `check out frm version cotnrol`로 들어가 각자 사용하고 있는 툴을 이용해 소스를 내려받는다(svn의 경우, configure-svn설정에서 관련 설정을 해야한다.)

2. [ctrl + shift + alt + s]를 눌러 `project structure` 메뉴로 들어간다
3. project탭 - `project sdk`에 jdk 설정을 한다.
4. module탭 - 빨간색으로 표시 된 오류 사항들을 환경에 맞게 수정한다
5. mvn으로 모듈 관리를 하는 프로젝트의 경우 프로젝트에서 우클릭 - `Add frameworks support` - `Maven`을 클릭하고 `OK`버튼을 눌러준다.
6. 상단탭의 `run` - `edit configure` 클릭 - `+`버튼 - `tomcat server -local`을 추가한다
7. 띄워져 있는 창에 Server, Deployment... 탭이 있는데 `Deployment`탭에 들어가 +버튼을 눌러 현재 모듈에 대한 추가를 한다. `(exploded)`로 표시돼 있는 모듈쪽을 추가해야 한다.
    * 간혹 웹 관련 설정을 할 수 없는 경우가 있는데 프로젝트 속성에서 web관련된 속성이 빠져서 그런것이니 당황하지 않고 속성을 추가해준다.

---
 한 두번 해보면 쉽게 별 거 아니란 것을 알 수 있게되며 지겨운 이클립스 플러그인 지옥에서 빠져나올 수 있게되니 꼭 사용해보길 추천한다. 
