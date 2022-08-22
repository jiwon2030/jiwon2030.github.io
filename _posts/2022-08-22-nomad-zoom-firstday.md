---
title: Nomadcoder node.js zoom 클론 강의
excerpt: Frontend Setup 에러

categories:
  - node.js
tags: Blog, node.js, nomadcoder, clone, zoom, error

date: 2022-08-22
last_modified_at: 2022-08-22
---

### Nomadcoder node.js zoom 클론 강의 Frontend Setup 에러

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