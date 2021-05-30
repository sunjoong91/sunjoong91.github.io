---
layout: post
title:  "타입 변환과 단축평가"
date:   2021-05-31T01:27:52-05:00
author: sunjoong kim
categories: deep-dive-javascript
---

# 09. 타입 변환과 단축평가

### 암묵적 타입변환(타입 강제 변환)
~~~js
var x = 10;
var str = x + '';
~~~
### 문자열 타입으로 변환
- 1 + '2' // "12"
### 숫자 타입으로 변환
- 1 - '1' // 0
- 1 * '10' // 10
### 불리언 타입으로 변환
- 자바스크립트 엔진은 불리언 타입이 아닌 값을 Truthy 값(참으로 평가되는 값)또는 Falsy 값(거짓으로 평가되는 값)으로 구분
~~~js
if('')      console.log('false')
if(true)    console.log('true')
if(0)       console.log('false')
if('str')   console.log('true')
if(null)    console.log('false')
~~~

## 명시적 타입변환(타입 캐스팅)
- 개발자가 의도적으로 값의 타입을 변환하는것
~~~js
var x = 10;
var str = x.toString(); //의도적으로 String형태로 평환
var str2 = String(x); //의도적으로 String형태로 평환
~~~
### 문자열 타입으로 변환
- String(1), 1.toString()
### 숫자 타입으로 변환
- Number('1'), parseInt('1'), parseFloat('1.123123')
### 불리언 타입으로 변환
- Boolean('x'), Boolean(NaN), Boolean({})//true, Boolean([])//true, !!'x'//true

## 단축평가
### 논리연산자를 사용한 단축평가
- 논리곱(&&) 연산자는 두 개의 피연산자가 모두 true로 평가될때 true를 반환 한다. 논리곱 연산자는 좌항에서 우항으로 평가가 진행 되므로, 논리연산의 결과를 결정해 두번째 피연산자, Animal를 그대로 반환
~~~js
'Human' && 'Animal' //->Animal
~~~

- 논리합(||) 연산자는 두 개의  피연산자 중 하나만 true로 평가 되어도 true를 반환 한다. 논리 연산의 결과를 결정한 첫 번째 피연산자, Human을 그대로 반환
~~~js
'Human' || 'Animal' //->Human
~~~
- true || anything - > true
- false || anything -> anything
- true && anything  -> anything
- false && anything  -> false






