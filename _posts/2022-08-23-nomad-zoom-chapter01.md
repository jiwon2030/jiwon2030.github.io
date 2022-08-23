---
title: Nomadcoder node.js zoom 클론 강의
excerpt: Chapter01. CHAT WITH WEBSOCKETS

categories:
  - node.js
tags: Blog, node.js, nomadcoder, clone, zoom

date: 2022-08-23
last_modified_at: 2022-08-23
---

### Nomadcoder node.js zoom 클론 강의 Chapter01 Recap

##### 1. backend

###### - websocket server
###### - **connection이라는 이벤트를 listen** -> connection event 발생 -> 누가 socket에 연결했는지 알 수 있음
![image](https://user-images.githubusercontent.com/49359846/186090756-d34336a6-67a6-439a-9ce4-f40273080b45.png)
###### - Backend -> Frontend: socket.on("message")
![image](https://user-images.githubusercontent.com/49359846/186090889-5a87660c-d0a0-4818-b679-d34e92bceabd.png)
###### - 익명 함수(이름없는 function)


##### 2. frontend

###### - Frontend -> Backend: addEventListener("message")