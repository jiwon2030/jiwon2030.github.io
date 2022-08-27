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
![image](https://user-images.githubusercontent.com/49359846/186481614-146350a6-7b18-47de-a6e3-e63026a74825.png)
###### [출처] 강의 Comments 중 ayyan님 댓글

#### 3. Room

###### room: user가 웹사이트로 가면 방을 만들거나, 방에 참가할 수 있는 form을 보게 될 것이다.
###### - 어떤 이름이든 상관없이 특정한 event를 emit해줄 수 있음.
###### - object를 전송할 수 있음.

##### Websocket에서 SocketIO로 바꾸고 난 후 발전된 점
###### 1) 모든 것이 message일 필요가 없다.
######   : 만약 여러 type의 메시지가 생기면 메시지 function이 엄청 커지기 때문에 힘들어짐.
###### 2) 대신, clinet로 원하는 어떤 event든 모두 emit해줄 수 있다.
######   -> **socket.emit과 socket.on에는 같은 이름을 사용해야 한다.**
###### 3) 전송할 때 원하는 아무거나 전송할 수 있다.(Websocket에서는 text만 전송 가능) & 한 가지만 보내야 한다는 제약이 없다.
######   -> font-end에서 **원하는 만큼** 숫자 또는 object를 전송할 수 있다. : SocketIO는 object를 string으로 바꿔주고 다시 알아서 Javascript object로 만들어줌.
###### +) back-end에서 front-end로 메시지를 보낸 후 응답으로 socket에서 메시지를 받고 싶다면, socket.emit에서 **마지막 argument**에 넣어줘야 한다.

#### 4. Adapter

###### Adapter: 기본적으로 다른 서버들 사이에 실시간 어플리케이션을 동기화하는 일을 한다.
###### - 지금 우리는 서버의 메모리에서 Adapter를 사용하고 있다. 데이터베이스에는 아무것도 저장하고 있지 않는다. 우리가 서버를 종료하고 다시 시작할 대 모든 room과 message와 socket은 없어진다. 우리가 재시작할 때는 모든 것들이 처음부터 시작된다.
###### - Adapter는 Mongo DB(데이터베이스의 예)를 사용해서 서버 간의 통신을 도와줌. 규모가 큰 어플리케이션은 많은 서버를 가지기 때문. 모든 클라이언트가 동일한 서버에 연결되는 것은 아님.
###### - 즉, Apdater는 어플리케이션으로 통하는 창문 역할을 함. 누가 연결되었는지, 현재 어플리케이션에 room이 얼마나 있는지 알려줌.