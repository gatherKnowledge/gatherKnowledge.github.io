---
layout: post
title: 라즈베리 파이 개요
categories: [raspberry pi, 3rd]
tags: [Iot, raspberry]
fullview: true
comments: true
published: true
---
### 라즈베리파이-3세대 (Rasberry Pi 3 Model B )
#### Pic.
![](https://www.kiwi-electronics.nl/image/cache/data/products/raspberry-pi/boards/KW-1615-1-1000x667.jpg)

#### Spec.
Processor : Quad Core 1.2GHz Broadcom BCM2837 64bit CPU
RAM : 1GB
ROM : Micro SD port for loading your operating system and storing data
그 외 추가
* BCM43438 wireless LAN and Bluetooth Low Energy (BLE) on board
* 40-pin extended GPIO
* 4 USB 2 ports
* 4 Pole stereo output and composite video port
* CSI camera port for connecting a Raspberry Pi camera
* DSI display port for connecting a Raspberry Pi touchscreen display
* Upgraded switched Micro USB power source up to 2.5A

 기기 하드웨어 스펙은 이정도, OS의 경우에는 Raspbian(오타 주의)이나 Noobs를 공식홈페이지에서 무료로 제공받을 수 있다. 이 외에 Ubuntu도 사용되는 데, 우분투가 익숙한 사람들에게나 접근성이 용이하다 라는 이유로 설치하는 것이지 제대로 우분투 써보지도 않은 나같은 사람들에게는 기기 최적화가 더 잘 돼있는 라즈비안을 쓰는 것이 더 낫다. 그 외에도 Ms Iot용 Os등을 사용할 수 있다고 한다.

 용도는 무궁무진한데, 애초에 개발도상국의 아이들에게 개인용PC를 제공하기 위해서 만들어진 제품이기 때문이다. 그래서 초기에는 인당 하나의 제품밖에 살 수 없다고 한다.
현재는 교육목적으로 많이 사용되고 개인서버용으로 구매하는 사람들도 있다. 사실 CPU/RAM/ROM이 달린 소형 컴퓨터인데, 못 할 것이 뭐가 있을까 싶다. 2016년 2월에 3세대 라즈베리 파이가 나왔고, 현재는 성능<->가격 간의 문제 때문에 스펙 향상을 하지 못 하고 있다고 한다. 그리고 내가 라파 산 지 얼마 안 됐는데 바로 다음 버전 나오는거 아니야? 걱정할 필요가 없는 이유가 또, 최소 3년동안은 이 모델을 쓸 것이라는 이야기를 라파 창립자가 이야기 했다고 하네요. 이 정도 스펙이면 못 할 것도 딱히 없고.. 이 가격에 저전력 Pc 한 대 인데..

+추가) 라즈베리 파이 의미 : raspberry -> 산딸기, pi-> 파이?(x), `python interpreter`

#### 나머지는 관련된 링크

http://forums.rasplay.org/topic/55/%EC%A0%95%EB%B3%B4-%EB%9D%BC%EC%A6%88%EB%B2%A0%EB%A6%AC%ED%8C%8C%EC%9D%B4-3-%EB%AA%A8%EB%8D%B8-%EB%B0%9C%EC%97%B4-%EA%B3%A0%EC%98%A8%ED%98%84%EC%83%81-%EC%97%90-%EB%94%B0%EB%A5%B8-%EC%85%A7%EB%8B%A4%EC%9A%B4-%ED%98%84%EC%83%81
- 라즈베리 파이3가 고온현상으로 이슈가 됐었다고하네요. 하지만 CPU 풀로드하여 테스트 했던만큼 실사용에서 저 정도까지 온도가 올라 갈 수가 없다는 이야기

http://chaz.tistory.com/150
- 라파3를 이용한 NAS서버 구축

http://pi.plus
- 클리앙 유저분이 만드신 것 같은데, 라파 입문자용 간단한 정보들을 얻을 수 있습니다.

https://www.formulapi.com/
- 라즈베리 파이를 이용한 경주 대회

http://blog.naver.com/PostView.nhn?blogId=alkydes&logNo=220973665012&parentCategoryNo=&categoryNo=156&viewDate=&isShowPopularPosts=true&from=search
- 기술적 한계(단가 한계)에 다달은 라파
