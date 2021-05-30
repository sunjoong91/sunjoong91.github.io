---
layout: post
title:  "데이터 타입"
date:   2021-05-31T01:27:52-05:00
author: sunjoong kim
categories: deep-dive-javascript
---

# 06. 데이터 타입
<br>
<br>

## 데이터타입
- 데이터타입(data type)은 값의 종료를 말한다. 자바스크립트의 모든 값은 데이터 타입을 갖는다
<br>
<br>

### 원시타입
- 숫자타입        : 숫자, 정수와 실수 구분없이 하나의 숫자 타입만 존재
- 문자열타입      : 문자열
- 불리언타입      : 논리적 참(true)과 거짓(false)
- undefined 타입  : var 키워드로 선언된 변수에 암묵적으로 할당되는 값
- null 타입       : 값이 없단느 것을 의도적으로 명시할 때 사용하는 값
- 심벌 타입        : ES6에서 추가된 7번째 타입
<br>
### 객체타입
- 객체, 함수, 배열 등
<br>

### 숫자타입
~~~js
var binary = 0b010101;//2진수
var octal  = 0o101;   //8진수
var hex    = 0x41;    //16진수 
~~~
<br>

### 문자타입
~~~js
var test;
test = '테스트'; //작은따옴표
test = "테스트"; //큰따옴표
test = `테스트`; //백틱(ES6)
~~~
<br>

### 템플릿 리터럴
- ES6부터 템플릿 리터럴 이라고 하는 새로운 문자열 표기법이 도입
- 백틱(``)을 사용해 표현
- 멀티라인 문자열 같은경우는 줄바꿈(개행)이 허용되지 않지만 백틱은 허용
<br>

### 표현식 삽입
- 템플릿 리터럴이 아닌 일반 문자열에서 표현식 삽입은 문자열로 취급
~~~js
var firstNm = 'sunjoong';
var lastNm = 'Kim';
console.log(`My name is ${firstNm} ${lastNm}.`);//''으로 사용불가
~~~
<br>

### 심벌(symbol) 타입
- 심벌(symbol)은 ES6에서 추가된 7번째 타입으로, 변경 불가능한 원시타입의 값
~~~js
var symbolTest = Symbol('key');
console.log(typeof symbolTest); //symbol
~~~