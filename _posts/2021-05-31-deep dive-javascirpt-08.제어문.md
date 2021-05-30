---
layout: post
title:  "제어문"
date:   2021-05-31T01:27:52-05:00
author: sunjoong kim
categories: deep-dive-javascript
---

# 08. 제어문
- 제어문은 조건에 따라 코드 블록을 실행(조건문)하거나 반복 실행(반복분)할 때 사용한다.
<br>
<br>

## 블록문
- 블록문은 0개 이상의 문을 중괄호({})로 묶은 것으로, 코드 블록 또는 블록이라고 부르기도 한다.
- 블록문은 언제나 문의 종료를 의미하므로 블록문 끝에는 세미콜론을 붙히지 않는다.
<br>
<br>

## 조건문
- 조건문은 주어진 조건식의 평가 결과에 따라 코드 블록(블록문)의 실행을 결정한다.
### if-else문
- if-else문은 주어진 조건식의 평가 결과, 즉 논리적 참 또는 거짓에 따라 실행할 코드 블록을 결정
### switch문
- switch 문은 주어진 표현식을 평가하여 그 값과 일치하는 표현식을 갖는 case 문으로 실행 흐름을 옮김
~~~js
switch(표현식){
    case 표현식1 :
        //switch 문의 표현식과 표현식1이 일치하면 실행될 문;
        break;
    case 표현식2 :
        //switch 문의 표현식과 표현식2이 일치하면 실행될 문;
        break;
    default:
        //switch 문의 표현식과 일치하는 case문이 없을때 실핼될 문
}
~~~

## 반복문
- 반복문은 조건식의 평가 결과가 참인 경우 코드블록을 실행
### for문
- for문은 조건식이 거짓으로 평가될때까지 코드 블록을 반복 실행
### while문
- while문은 주어진 조건식의 평가과 참이면 코드 블록을 계속해서 반복 실행
### do-while문
- do-while문은 코드블록을 먼저 실행하고 조건식을 평가한다.
<br>
<br>

## break문
- switch문과 while문에서 코드 블록을 탈출

## continue문
- continue문은 반복문의 코드 블록 실행을 현 지점에서 중단하고 반복문의 증감식으로 실행 흐름을 이동시킴
~~~js
var t = "Hello world";
var returnArr = [];
for(var i = 0 ; i< t.length; i++) {
    if(i == 0 ) {
    continue;
    }
    returnArr.push(i);
}
console.log(returnArr)//;0은 찍히지 않는다.
~~~
