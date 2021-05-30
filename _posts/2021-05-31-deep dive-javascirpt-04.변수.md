---
layout: post
title:  "변수"
date:   2021-05-31T01:27:52-05:00
author: sunjoong kim
categories: deep-dive-javascript
---


# 04. 변수

## 변수
- 하나의 값을 저장하기 위해 확보한 메모리 공간 자체 또는 그 메모리 공간을 식별하기 위해 붙힌 이름을 말한다.

### 변수에 여러개의 값을 저장하는 방법(배열이나 객체 이용)
~~~js
var studentId = '1';
var studentNm = '강감찬';

//여러 개의 값을 하나로 그룹화해서 하나의 값으로 사용
var students = {id : '1', name : '강감찬'
              , id : '2', name : '홍길동'}

~~~

## 식별자
- 변수의 이름, 어떤 값을 구별해서 식별할 수 있는 고유의 이름을 말한다.

## 변수 선언
- var, let, const
- var : 선언단계와 초기화 단계과 동시에 진행, 재할당 가능
- const : 재할당 불가능, 상수

### 변수 호이스팅
- 변수 선언이 소스코드가 한 줄씩 순차되는 시점, 런타임이 아니라 그 이전단계에서 실행 되어, 동작하는 자바스크립트 고유의 특징  
but, 값의 할당은 소스코드가 순차적으로 실행되는 시점인 런타임에 실행

~~~js
console.log(score);
var score = 100;
//undefined 출력
~~~

~~~js
var score = 100;
console.log(score);
//100 출력
~~~

### 네이밍 컨벤션
~~~js
var myName; //카멜 케이스(camelCase)
var my_name; // 스네이크 케이스(snake_case)
var MyName; //파스칼 케이스(PascalCase)

//헝가리언 케이스(typeHungarinCase)
var strMyName; //type + identifier
var $elem = document.getElementById('myName'); //DOM 노드
~~~