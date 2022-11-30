---
title: 코틀린을 활용한 안드로이드 프로그래밍
excerpt: Chapter04. 기본 위젯 익히기

categories:
  - android
tags: Blog, android, kotlin

date: 2022-11-22
last_modified_at: 2022-11-22
---

# Chapter04. 기본 위젯 익히기

## 직접 풀어보기 4-2. 다음과 같은 화면을 XML로 코딩하라. 버튼, 텍스트뷰, 에디트텍스트, 버튼을 차례로 지정하고 앞에서 배운 속성을 사용하라.
![image](https://user-images.githubusercontent.com/49359846/203237898-d7112a08-5127-492f-864d-4c27eb289fe6.png)
![image](https://user-images.githubusercontent.com/49359846/203237985-0920bcfd-3c6b-4f8f-bd43-8bb016005d37.png)


## 실습 4-1. 초간단 계산기 앱 만들기
– 가장 기본적인 위젯인 텍스트뷰, 에디트텍스트, 버튼을 이용한 앱 만들기
– 두 정수를 입력하고 버튼을 누르면 계산 결과가 나오는 계산기
• 안드로이드 프로젝트 생성
 (1) 새 프로젝트를 만들기
  – 프로젝트 이름: ‘Project4_1’
  – 패키지 이름: ‘com.cookandroid. project4_1’
  – 그 외 규칙은 [실습 2-4]의 (1)~(4)를 따름
• 화면 디자인 및 편집
 (2) Project Tree에서 [app]-[res]-[layout]-[activity_main.xml]을 열고, 아래쪽의 [Text] 탭을 클릭하여 화면 코딩
– 에디트텍스트 2개, 버튼 4개, 텍스트뷰 1개를 생성
– 각 위젯에 layout_margin을 적절히 지정(예: 10dp)
– 결과를 보여줄 TextView는 색상을 빨간색으로, 글자 크기를 30dp로 함
– 각 위젯의 id는 위에서부터 차례로 Edit1, Edit2, BtnAdd, BtnSub, BtnMul, BtnDiv, TextResult로 함
![image](https://user-images.githubusercontent.com/49359846/203238913-d14c3902-8f56-49a3-bebf-ff8812ec65e3.png)
