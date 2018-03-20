---
layout: post
title: 라즈비안 에뮬레이터 세팅 with Qemu
categories: [raspberry pi, 3rd]
tags: [Iot, emul, emulator]
fullview: true
comments: true
published: true
---
#### Qemu세팅 시 주의 할 점
* 64비트 운영체제 사용할 시 64비트용으로 설치하지 말고 32비트 호환용으로 설치해줘야 한다. 그렇지 않으면 알수 없는 오류가 발생 할 수 있음
* Qemu를 설치했을 때 설치된 에뮬레이터 들은 target보드의 CPU를 확인하고 할 것.
    - 우리 같은 경우에는 라즈베리 파이3를 사용하기 때문에 당연히 ARM 에뮬레이터를 써주면 될 것(qemu-sysetm-arm.exe, 같은 이름의 armw파일도 있는데 이 파일과의 차이가 뭔지 모르겠다.)
- RSP iso파일이랑 커널 파일이 둘 다 있어야 한다(윈도우 설치할 때 생각해보면 그냥 `iso`파일 하나만 있으면 설치되지 않았던가.. 왜 커널이 필요하지?) - 확인이 필요 할 것 같다.
