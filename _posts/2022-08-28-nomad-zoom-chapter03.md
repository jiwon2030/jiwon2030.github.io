---
title: Nomadcoder node.js zoom 클론 강의
excerpt: Chapter03. VIDEO CALL

categories:
  - node.js
tags: Blog, node.js, nomadcoder, clone, zoom

date: 2022-08-28
last_modified_at: 2022-08-29
---

### 1. 동기 vs 비동기
##### 1) 동기(synchronous : 동시에 일어나는)
###### - 말 그대로 동시에 일어난다는 뜻.
###### - 요청과 결과가 한 자리에서 동시에 일어남
###### - A노드와 B노드 사이의 작업 처리 단위(transaction)를 동시에 맞추겠다.
###### - 장점 : 설계가 매우 간단하고 직관적
###### - 단점 : 결과가 주어질 때까지 아무것도 못하고 대기해야 함

##### 2) 비동기(Asynchronous : 동시에 일어나지 않는)
###### - 동시에 일어나지 않는다를 의미
###### - 요청한 그 자리에서 결과가 주어지지 않음
###### - 노드 사이의 작업 처리 단위를 동시에 맞추지 않아도 된다.
###### - 장점 : 결과가 주어지는데 시간이 걸리더라도 그 시간 동안 다른 작업을 할 수 있으므로 자원을 효율적으로 사용
###### - 단점 : 동기보다 복잡
###### - [출처] https://private.tistory.com/24 [오토봇팩토리:티스토리]
###### - [출처] https://velog.io/@khy226/%EB%8F%99%EA%B8%B0-%EB%B9%84%EB%8F%99%EA%B8%B0%EB%9E%80-Promise-asyncawait-%EA%B0%9C%EB%85%90


### 2. webRTC(Web Real-Time Communication)
##### webRTC란? 
###### - 웹 애플리케이션과 사이트가 중간자 없이 브라우저 간에 오디오나 영상 미디어를 포착하고 마음대로 스트림할 뿐 아니라, 임의의 데이터도 교환할 수 있도록 하는 기술
###### - 즉, 실시간 커뮤니케이션을 가능하게 해주는 기술
###### - peer-to-peer 연결을 가능하게 해준다. -> 서버에 전달하지 않고 컴퓨터, 브라우저에 영상이나 오디오 등을 직접 전달하면 된다.

![image](https://user-images.githubusercontent.com/49359846/187207485-2bdf5859-747e-40c2-9550-6a47e942ff5f.png)

### 3. Sender
##### Sender이란?
###### - 우리의 peer로 보내진 media stream track을 컨트롤하게 해준다.

### 4. webRTC DataChannel
##### 