# broadcasting([UI 바로가기](http://jaebum7396.iptime.org:3000/broadcast/main))
    머신러닝과 소켓서버를 이용한 주가예측 시스템
    바이낸스 SDK를 통해 실시간 캔들데이타를 수신하고 해당 캔들 데이타를 학습(smile4j) 및 지표로 처리(ta4j)하여 레디스로 퍼블리싱합니다.  
    퍼블리싱된 지표와 매매 시그널은 STOMP로 구현된 소켓 서버를 통해 해당 토픽(/sub/channel/signalBroadCast)으로 발행됩니다.
    실시간 지표를 확인하시려면  
    [UI 바로가기](http://jaebum7396.iptime.org:3000/broadcast/main)

    가공된 캔들데이타를 누구나 쉽게 활용할 수 있도록 하기 위해 구현했습니다.  

### 구현방법
```
Java, Spring Boot, 스프링 클라우드, Jenkins, JPA, mysql, Gradle, Docker, redis, smile4j, ta4j 
```

### 구현예정기능
    - 심볼 선택시 대량의 캔들데이타를 csv형식으로 내려받도록 제공할 예정입니다.
    - 기타 심볼을 선택할 수 있도록하고 차트 인터벌을 구현할 예정입니다.
    
### 프로젝트 구성

