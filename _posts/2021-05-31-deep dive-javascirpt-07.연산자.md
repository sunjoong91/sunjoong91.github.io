---
layout: post
title:  "연산자"
date:   2021-05-31T01:27:52-05:00
author: sunjoong kim
categories: deep-dive-javascript
---

# 07. 연산자

## 산술 연산자
- 산술연산자는 피연산자를 대상으로 수학적 계산을 수행해 새로운 값을 만든다.
- 산술연산이 불가능한 경우 NaN을 반환한다.

### 이항 산술 연산자
- +,-,*,/,%

### 단항 산술 연산자
- 증가/감소(++/--) 연산자는 피연산자의 값을 변경하는 부수효과가 있음
~~~js
var x = '1';
console.log(+x); //1
console.log(x); //'1'

var x = true;
console.log(+x); //1
console.log(x); //true

var x = false;
console.log(+x); //0
console.log(x); //false

var x = 'Hello';
console.log(+x); //NaN
console.log(x); //'Hello'
~~~

### 문자열 연결 연산자
- +연산자는 피연사 중 하나 이상이 문자열인 경우 문자열 연결 연산자로 동작한다
~~~js
//문자열 연결연산자
'1' + 2; //'12'
1 + '2'; //'12'

//산술연산자
1 + 2 ; //3

//true는 1로 타입 변환
1 + true;//2

//true는 1로 타입 변환
1 + false;//1

//true는 1로 타입 변환
1 + null;//1

//undefined는 숫자로 타입 변환되지 않음
+undefined; //NaN
1 + undefined; //NaN
~~~
<br>

## 할당 연산자
- 할당연산자는 우항에 있는 피연산자의 평가 결과를 좌항에 있는 변수에 할당
- =,+=,-=,*=,/=,%=
~~~js
//연쇄할당
var a,b,c;
//오른쪽에서 왼쪽으로 진행
a = b = c = 0;

console.log(a,b,c); //0 0 0
~~~
<br>

## 비교 연산자
- 비교 연산자는 좌항과 우항의 피연산자를 비교한다음 그 결과를 불리언 값으로 반환
### 동등/일치 비교 연산자
- == 동등비교      ex)x == y //x와 y의 값이 같음
- === 일치비교     ex)x === y //x와 y의 값과 타입이 같음
- != 부동등 비교   ex)x != y // x와 y의 값이 다름
- !== 불일치 비교  ex)x !== y //x와 y의 값과 타입이 다름

- 동등 비교(==) 연산자는 좌항과 우항의 피연산자를 비교할때 암묵적 타입변환을 통해 탕비을 일치 시킨 후 같은 값인지 비교.
- 일치 비교(===) 연산자는 좌항과 우항의 피연산자가 타입도같고 값도 같은 경우에 한하여 true를 반환
~~~js
NaN === NaN; //false
~~~
NaN은 자신과 일치하지 않는 값이므로 isNaN을 사용한다.

### 대소 관계 비교연산자
- <,>, <=, >=
<br>
<br>

## 삼항 조건 연산자
- 조건식? 조건식이 true일때 반환할값 : 조건식이 false일때 반환할 값

## 논리연산자
- ||(or), &&(and), !(not)

## typeof 연산자
- string, number, boolean, undefined, symbol, object, function

## 지수 연산자
- 2**2 == Math.pow(2,2);
- 2**0 == Math.pow(2,0);

## 연산자의 부수효과
- 할당연산자(=), 증가/감소연산자(++/--), delete연산자
~~~js
var test = {a:1};
delete test.a;
console.log(test); //{}
~~~