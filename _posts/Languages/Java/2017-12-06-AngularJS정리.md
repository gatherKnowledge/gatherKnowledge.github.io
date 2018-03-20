---
layout: post
title: 당장 보고 쓸 수 있는 AngularJS
categories: [angularJS]
tags: [angularJS]
fullview: true
comments: true
published: true
---

다음은 ng-* 선언을 추가한 HTML이다:
```
<div ng-app="myApp">
    <div ng-controller="MainCtrl">
        <!-- controller logic -->
    </div>
</div>
```
그리고 Angular 모듈과 컨트롤러다:

```
var myApp = angular.module('myApp', []);

myApp.controller('MainCtrl', ['$scope', function ($scope) {
  // Controller magic
}]);
```
더 진행하기 전에 모든 로직을 담을 Angular 모듈 을 하나 만들어보자. 모듈을 정의하는 방법은 다양하며 그 중 하나가 다음과 같이 로직을 묶는 방법이다(필자는 이런 방식을 별로 안좋아한다):
```
angular.module('myApp', [])
.controller('MainCtrl', ['$scope', function ($scope) {...}])
.controller('NavCtrl', ['$scope', function ($scope) {...}])
.controller('UserCtrl', ['$scope', function ($scope) {...}]);
```
위 비효율적인 코드 => 중간에 오류가 생기면 나머지도 같이 오류가 생길 수 있다.
```
var myApp = angular.module('myApp', []);
myApp.controller('MainCtrl', ['$scope', function ($scope) {...}]);
myApp.controller('NavCtrl', ['$scope', function ($scope) {...}]);
myAp
p.controller('UserCtrl', ['$scope', function ($scope) {...}]);
```
View 외부 모듈 작성 부분
----
Controller
```
<div ng-app="myApp">
    <div ng-controller="MainCtrl">
         {{ text }}
    </div>
</div>
```
```
var myApp = angular.module('myApp', []);

myApp.controller('MainCtrl', ['$scope', function ($scope) {

    $scope.text = 'Hello, Angular fanatic.';

}]);
```
여기서 가장 중요한 개념은 특정 컨트롤러안에 모든 기능을 담는 $scope 라는 개념이다. $scope 는 DOM의 현재 요소/영역을 참조하며(this 와는 다르다), 요소안의 데이터와 로직을 주시하는 아주 멋진 관찰 기능을 가지고 있다. 이 기능으로 DOM에 자바스크립트 public/private 스코프를 멋지게 만들 수 있다.

$scope 개념이 처음에는 조금 이상해 보일지 몰라도 서버로부터 DOM을 만드는 아주 좋은 방법이다(정적 데이터인 경우도 역시)! 예제를 보면 DOM으로 데이터를 어떻게 주입하는지에 대한 기본 개념을 익힐 수 있을 것이다.

```
var myApp = angular.module('myApp', []);

myApp.controller('UserCtrl', ['$scope', function ($scope) {

    // user details라는 네임스페이스를 사용하자. DOM에서 알아보기도 좋을 것이다.
    $scope.user = {};
    $scope.user.details = {
      "username": "Todd Motto",
      "id": "89101112"
    };

}]);
```
```
<div ng-app="myApp">
    <div ng-controller="UserCtrl">
        <p class="username">Welcome, {{ user.details.username }}</p>
        <p class="id">User ID: {{ user.details.id }}</p>
    </div>
</div>
```
컨트롤러는 JSON 데이터로 서버와 통신하는 함수(이벤트 함수도!)와 데이터 만을 다룬다는 걸 기억하는 게 중요하다. DOM 조작을 컨트롤러에서 해선 안되며 jQuery도 일단은 생각하지 말자. DOM 조작은 디렉티브로 하면 되니까 조금 있다 다시 살펴보자.

출처 : 하루만에 끝내는 AngularJS

http://soomong.net/blog/2014/01/20/translation-ultimate-guide-to-learning-angularjs-in-one-day/
