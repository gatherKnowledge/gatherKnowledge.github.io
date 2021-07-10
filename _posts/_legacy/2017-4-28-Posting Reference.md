---
layout: post
title: 이것 저것 적어보는 Jekyll 기반 블로그 포스팅 Tips
categories: [blog]
tags: [format, tips]
fullview: true
comments: true  
---
1. [Prose.io](prose.io )를 이용하면 git local파일을 만들지 않고 편하게 `github`계정을 이용해 바로 바로 문서 생성과 커밋이 가능하다.
  - 물론 알고있듯이 기본으로 git hub자체에서 어느정도까지 수준의 수정은 가능하다
2. `MARKDOWN language`에 익숙하지 않다면 Tool의 도움을 받는 것이 현명하다.
  * 필자 역시 이래저래 끙끙대며 테스트하다가 결국에는 `ATOM TEXTEDITOR`의 힘을 빌려 글을 작성하고 있다. 효과 들어가는 부분에 대해 컬러로 표시를 해주고 `markdown preview`라는 메뉴가 있어 간단하게 결과를 preview 할 수 있다.
  * `Atom`에는 github plus라는 추가 구성 패키지가 있기 때문에 전체 세팅이 변경되면 마우스만으로도 편하게 `commit, push`작업을 진행 할 수 있다.
  * _(며칠 타이핑해보니 알록달록한 글자들을 보니 예뻐보이기까지 한다)_
  * 깃허브를 사용하는데 GUI환경에서 편하게 사용하고 싶다면, Github Desktop을 이용하는 것을 추천한다.
3. Title rules
  1. **YYYY-MM-DD-[title명.md]** 현재 보고 있는 게시물의 타이틀도 나의 입장에서 보면 **2017-04-26-Blog posting Reference.md** 와 같은 룰을 따른다(YYYY-MM-DD-[title명.md])
  2. 포스팅 파일에 대한 제목과 별개로 user들에게 보여주는 title을 정해주고 싶다면 포스팅 최상단에
    <img src="{{site.BASE_PATH}}/images/post/201704/Title.PNG">
    이런 스타일로 명명해주면 파일에 대한 제목과 별개로 세팅 할 수 있다.
    `title:(space)name`의 한 칸 공백룰을 어기지 않도록 해야 한다
4. `Disqus`와 `google analytics`라는 서비스를 통해 단순한 게시글 나열이 아닌 양방향성을 지닌 블로그를 만들 수 있다.
  * 현재 Jekyll 기반 블로그를 며칠 써보고 느낀 것 **클라우드 서비스를 받는** 기분. 직접 세팅 할 수 있는 부분이 상상이상, 커스터마이징이 가능 한가? 라는 생각, 물론 그만큼 사람의 손이 많이 가야 한다는 것이기도 하지만 반대로 신경 안 쓰고 글만 쓸 것이라도 문제 없이 쓸 수 있다 _그렇다면 naver나 다른 기타 플랫폼의 블로그를 하는 것이 훨씬 편하겠지만_
  * _github의 compile오류를 받아 본 것도 상상이상으로 놀랐습니다. 당연하지만.._
  * `Disqus` : `Disqus`홈페이지에 들어가 계정을 만들고 세팅하게되면 _Disqus계정과 본인의 서버 모두 세팅 해줘야한다_ 본인이 원하는 서버에 댓글기능이 생성되게 한다. 서버에 iFrame으로 외부페이지 넣듯이 들어간 것 같은 느낌을 받을 수 있다.
  * `google analytics`
5. 전역변수, 지역변수 개념을 이용할 수 있다. `_config.yml`에 변수를 만들게 되면 전역변수로 이용 할 수 있고, 각 포스트의 상단에 세팅을 통해 지역변수를 이용 할 수 있도 있다.

```
---
title: 나의개발
name: ekul
---
```
