---
title: Nomadcoder node.js zoom 클론 강의
excerpt: Chapter00. Server, Frontend Setup

categories:
  - node.js
tags: Blog, node.js, nomadcoder, clone, zoom, error

date: 2022-08-22
last_modified_at: 2022-08-22
---

### Nomadcoder node.js zoom 클론 강의 Setup 에러


##### **1. 사용하고 있는 포트 에러**
![EADDRINUSE](https://user-images.githubusercontent.com/49359846/185800490-ebc38565-bffe-4bcd-add9-bb95a34fc598.PNG)
###### **Error 코드: EADDRINUSE**
###### 해결 방법 1) 포트 넘버를 3000에서 3001로 수정해준다.
######           2) 포트를 강제로 죽여준다.
![image](https://user-images.githubusercontent.com/49359846/185805567-595c0aaf-69c9-45cb-bab5-85d769e0382a.png)
###### **netstat -ano \ findstr 포트 넘버**
###### **taskkill /f /pid 해당 pid**

###### -> 참조 https://seomile.tistory.com/91 


##### **2. 모듈 설치 안됨**
![image](https://user-images.githubusercontent.com/49359846/185805691-ae89aed3-02f4-4a4f-a23c-f449b2701869.png)
###### **Error 코드: MODULE_NOT_FOUND**
###### 해결 방법: 에러 코드 중에 해당 모듈을 확인하고 설치해준다.
![image](https://user-images.githubusercontent.com/49359846/185805863-eea041f7-a74e-4c19-aa3c-6f4aa92a8bfb.png)
![image](https://user-images.githubusercontent.com/49359846/185805875-dbc3d5d1-6077-4149-ae0a-da7d19f5e528.png)
###### -> 노마드코더 node.js(zoom클론) 강의를 보면서 따라하다가 package.json 파일을 잘못 손댔을때 그때 지워졌던 거 같다..


### Nomadcoder node.js zoom 클론 강의 Setup Recap(요약)

##### 1. nodemon.js
###### nodemon
###### - 우리의 프로젝트를 살펴보고 변경 사항이 있을 시 서버를 재시작해주는 프로그램
###### - 서버를 재시작하는 대신에 babel-node 실행(Babel: 우리가 작성한 코드를 일반 NodeJS 코드로 컴파일 -> src/server.js 파일에 작업해주는 역할)


##### 2. server.js
###### - express를 import
###### - express 어플리케이션을 구성
###### - view engine을 pug로 설정
###### - views 디렉토리 설정
###### - public 파일들에 대해서도 똑같은 작업
###### - **public 파일들은 FrontEnd에서 구동되는 중요한 코드**