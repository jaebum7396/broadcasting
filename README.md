# broadcasting([UI 바로가기](http://jaebum7396.iptime.org:3000/broadcast/main))

## 머신러닝과 소켓서버를 활용한 가격 예측 및 지표 스트리밍
    바이낸스 SDK를 통해 실시간 캔들데이타를 수신하고  
    해당 캔들 데이타를 학습(smile4j) 및 지표로 처리(ta4j)하여 레디스로 퍼블리싱합니다.  
    퍼블리싱된 지표와 매매 시그널은 STOMP로 구현된 소켓 서버를 통해  
    해당 토픽(/sub/channel/signalBroadCast)으로 발행됩니다.
    UI 바로가기 버튼을 통해 시각화된 라이브 지표를 확인하실 수 있습니다.
    해당 토픽 구독 시에 가공된 양질의 지표를 쉽게 활용할 수 있도록 하기 위해 구현했습니다. 

### 라이브차트 및 지표구현 예시화면
![image](https://github.com/user-attachments/assets/4795bf8e-0c52-4b92-816d-ad8d646bc7ed)
![image](https://github.com/user-attachments/assets/0876e7d1-fffb-47f8-86c3-990405001d9c)
### 구현방법
```
Java, Spring Boot, 스프링 클라우드, JPA, mysql, Gradle, redis, smile4j, ta4j 
```

### 배포방법
```
Docker, jenkins
```

### 구현예정기능
    - 심볼 선택시 대량의 캔들데이타를 csv형식으로 내려받도록 제공할 예정입니다.
    - 기타 심볼을 선택할 수 있도록 하고 차트 인터벌을 제공할 예정입니다.

### 프로젝트구성
    
#### 환경
* [discovery](https://github.com/jaebum7396/discovery) : 로드밸런싱을 위한 디스커버리 netflix eureka
* [gateway](https://github.com/jaebum7396/gateway) : 각 서비스 라우팅을 위한 게이트웨이

#### fe
* [client](https://github.com/jaebum7396/client) : 프로젝트 ui

#### service
* [signal](https://github.com/jaebum7396/signal) : 지표 가공 및 신호전파 서비스
* [socket-streamer](https://github.com/jaebum7396/socket-streamer) : 웹 소켓 서비스
* [message](https://github.com/jaebum7396/message) : 레디스로 전파받은 채팅 메시지 저장 및 채팅 메시지 쿼리 서비스
* [random-nickname](https://github.com/jaebum7396/random-nickname) : 닉네임 랜덤 제공 서비스



  
##### 함께하시려면 to [jaebum7396@naver.com](jaebum7396@naver.com)



