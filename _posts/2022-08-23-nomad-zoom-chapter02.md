---
title: Nomadcoder node.js zoom 클론 강의
excerpt: Chapter02. SOCKETIO

categories:
  - node.js
tags: Blog, node.js, nomadcoder, clone, zoom

date: 2022-08-23
last_modified_at: 2022-08-25
---

### Nomadcoder node.js zoom 클론 강의 Chapter02. SocketIO


#### 1. SocketIO vs WebSockets

#### Socket IO
##### SocketIO란?
###### - 프론트와 백엔드 간 실시간 통신을 가능하게 해주는 framework 또는 라이브러리
###### - 실시간, 양방향, event 기반의 통신을 가능하게 함.
###### - websocket 연결을 할 수 없는 경우 HTTP long polling 사용
###### - 신뢰성과 빠른 속도 제공

###### Websocket: Socket IO가 실시간, 양방향, event 기반 통신을 제공하는 방법 중 하나


#### SocketIO vs WebSockets
##### websocket와 공통점 
##### - 실시간으로 작동, 양방향으로 통신, 브라우저와 back-end의 양방향을 의미. 
##### - event 기반의 통신
##### Socket IO의 차이점 
###### - websocket을 실행하지 않음. 
###### - framework인데 실시간, 양방향, event 기반 통신 제공
###### - websocket보다 탄력성이 뛰어남

#### 2. 강의 내용(Installing SocketIO) 중 버전 차이로 인한 오류
![image](https://user-images.githubusercontent.com/49359846/186481288-55c94901-71d5-470a-a299-6aac86175620.png)
###### SocketIO의 버전 차이로 인한 오류가 났다면 다음과 같이 수정해주면 된다.
<<<<<<< HEAD
![image](https://user-images.githubusercontent.com/49359846/186481614-146350a6-7b18-47de-a6e3-e63026a74825.png)
###### [출처] 강의 Comments 중 ayyan님 댓글
=======
