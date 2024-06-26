# 인터넷은 어떻게 동작할까?

### 네트워크 용어 정리

- **패킷(Packet)**: 인터넷을 통해 전송되는 작은 데이터 단위입니다.
- **라우터**: 서로 다른 네트워크 간에 데이터 패킷을 전달하는 장치입니다.
- **IP 주소**: 네트워크의 각 장치에 할당된 고유 식별자로, 데이터를 올바른 대상으로 라우팅하는 데 사용됩니다.
- **TCP** : 패킷이 올바른 순서로 안정적으로 전송되도록 보장.
- **도메인 이름**: 예를 들어 `google.com`과 같이 웹사이트를 식별하는 데 사용되는 사람이 읽을 수 있는 이름입니다.
- **DNS (도메인 이름 시스템)**: 도메인 이름을 IP 주소로 변환하는 역할을 담당합니다.
- **HTTP (하이퍼텍스트 전송 프로토콜)**: 클라이언트(예: 웹 브라우저)와 서버(예: 웹 사이트) 간에 데이터를 전송하는 데 사용됩니다.
- **HTTPS**: HTTP의 보안 버전으로, 클라이언트와 서버 간의 보안 통신을 제공합니다.
- **SSL/TLS (Secure Sockets Layer / Transport Layer Security)**: 인터넷을 통한 보안 통신을 제공하는 프로토콜입니다.

1. 인터넷을 통해 데이터를 패킷 단위로 라우터로 전송
2. 패킷은 받은 라우터는 목적지까지 도달하기 위한 다음 라우터로 전송
3. 목적지까지 옳바른 전송을 위해 IP,TCP등 다양한 프로토콜 사용

### 도메인으로 웹사이트 실행
1. 도메인 입력
2.  해당 브라우저가 IP주소를 받기위해 DNS 서버로 요청을 보냄
3. IP주소를 받으면 브라우저는 서버로 접속 요청을 보냄
3. 페킷 형태로 데이터를 받아서 사람들이 볼 수 있게 인코딩함  (UTF-8) - `bytes`
4. 엔진이 받은 문서(html)을 하나하나 토큰화함, 하나하나 읽는다. - `Character` `Tokens`
5. 토큰 -> 객체로 다시 재해석한다. - `Nodes`
6. 문서의 관계를 설정함(head---body...) - `DOM`
7. 만약 style.css의 경우 다시 한번 더 요청을 받아 파일을 가져온다.
8. 서버가 요청을 받으면 광섬유로 데이터를 이동시킴
9. 사용자의 IP주소로 도착하면 라우터가 광섬유의 빛 신호를 전기신호로 변환함
![img.png](../../images/img.png)

### TCP와 IP
- 포트 : 장치에서 실행중인 애플리케이션이나 서비스를 식별하는데 사용. 각각 고유한 포트 번호가 있음
- 소켓 : = IP주소 + 포트 번호. 데이터를 주고받는 연결 지점.  
- 연결 : 소켓 사엥 연결이 설점. 
- 데이터 전송 : 연결이 되면 데이터 전송이 가능해진다. 일반적으로 세그먼트로 전송된다. 