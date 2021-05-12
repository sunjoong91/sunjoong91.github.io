---
layout: post
title:  "다양한 소프트웨어 버전 명명 (Software versioning)"
date:   2021-05-13T01:12:50-00:00
author: sunjoong kim
categories: ETC
---

## 다양한 소프트웨어 버전 명명 (Software versioning)


# Semantic Versioning
- Major, Minor 그리고 Patch의 의미를 담고 있는 버전 명명법입니다.  
  {major}.{minor}.{patch}   
  Major: 이전 버전과 호환이 안 되는 변경이 있다면 숫자를 올립니다  
  Minor: 이전 버전과 호환되는 기능 추가가 있다면 숫자를 올립니다.  
  Patch: 이전 버전의 버그를 수정했다면 숫자를 올립니다.  
  그리고 시험판(알파 베타 등) 및 추가 메타데이터들은 patch 뒤에 확장으로 제공됩니다.  
  공개된 라이브러리나 오픈소스라면 필수적인 Versioning 방법입니다.  
  
# CalVer (날짜 기반 Versioning)
- Ubuntu Linux를 보면 다음과 같은 버전을 가지고 있습니다.
  Ubuntu 4.10 (Warty Warthog)  
  ...  
  Ubuntu 19.04 (Disco Dingo)  
  Ubuntu 19.10 (Eoan Ermine)  
  Ubuntu 20.04 LTS (Focal Fossa)  
  우분투는 버전 명명을 연도 및 월로 사용하고 있습니다.  
  <br>  
  처음 우분투가 릴리즈 된 게 2004년도 10월이란 걸 버전명만 보고 알 수 있습니다.  
  이런 버저닝을 통해서 우리는 SemVer와는 다른 이점을 가질 수 있습니다.  
  예를 들어 우분투는 짝수년 2/4 분기에 발생하는 모든 4번째 릴리즈를 LTS 릴리즈로 지정합니다.  
  그리고 이런 LTS 버전의 경우 5년 정도의 지원을 해주게 됩니다.  
  이 말인즉 만약 제가 16.04 LTS 버전을 쓰고 있었다면, 이 버전의 지원 기간이 2021년도 4월까지인걸 패치 명만 보고도 짐작할 수 있기 때문에 이에 따른 액션을 할 수 있습니다.  
  날짜 번호는 마케팅으로도 사용될 수 있습니다.  
  Microsoft Office, Windows를 보면 쉽게 알 수 있습니다.  
  Microsoft Windows 95 -> MS-DOS 7.00 or Windows 4.00  
  Microsoft Windows 2000 Server - Windows NT 5.0  
  마케팅을 위해 사용자가 인식하기 쉬운 타이틀을 사용하지만, 실제로 각각의 버전은 전혀 다른 실제 버전을 따로 가지고 있습니다.  
  
# NumVersion (숫자 기반 버저닝)
- Apple은 NumVersion을 기반으로 한 공식 버전 번호 구조로 되어 있습니다.  
  한자리 혹은 두 자리의 메이저 버전, 한자리의 마이너 버전, 한자리의 버그 버전이 있고 스테이지 단계에서 추가 suffix를 사용하고 릴리즈 할 때 추가 suffix를 제거합니다.  
  1.0 버전에다 다음 버전을 개발한다면, 1.1.0a0 이런 식으로 suffix를 가지고 있습니다. 그 후 1.1.0f0와 같이 개발 버전이 올라가고, 릴리즈 시에는 스테이지 단계의 suffix를 제거하여 1.1이 됩니다.  
  이는 최종단계에서 깔끔한 버전을 사용하게 되는 장점이 있습니다.  
  소프트웨어 개발 시 패치 별로 제공하려는 기능에 대한 집중이 가능하기도 합니다.  
  
# TeX  
- 스탠퍼드대학교의 도널드 커누스(Donald Knuth) 교수가 만든 조판 언어, 시스템입니다.  
  markdown에서 수식 입력으로 사용하는 LaTeX가 TeX를 기반으로 만들어졌습니다.  
  The Art of Computer Programming 책을 집필하는데 그 당시 제공되던 출판 프로그램의 수식 표시가 마음에 들지 않아 만들었다고 합니다.  
  
# Java 
- Java는 복잡한 버전 명명법을 가지고 있습니다.  
  우선 마케팅 버전과 실제 버전, 즉 두 가지의 버전이 있습니다.  
  마케팅 버전은 또다시 아래와 같이 나뉩니다.  
  <br/>  
  Standard Edition (SE)  
  Micro Edition (ME)  
  Enterprise Edition (EE)  
  Java의 Android 또한 Java SE와 크게 다릅니다.  
  실제 버전은 아래와 같이 표현됩니다.  
  1.8.0_101-b13  
  이것은 JDK 1.8.0, Update 101, Build # 13을 말합니다. Oracle은 릴리스 노트에서 다음과 같이 언급합니다.  
  Java™ SE Development Kit 8, Update 101 (JDK 8u101)  
  
  
  
# 출처
- https://blog.sonim1.com/243 [Kendrick's Blog]