# [프록시 서버](https://roadmap.sh/guides/proxy-servers)

### 프록시 서버란?
클라이언트와 인터넷 사이에 위치하여 클라이언트의 요청을 대신 처리해주는 서버  
-       [클라이언트] <---> [프록시 서버] <---> [인터넷]
웹 요청 IP주소를 프록시 서버의 IP 주소로 변경한 다음 이를 웹 서버로 전달한다.  
웹 서버는 클라이언트를 인식하지 못하고 프록시 서버만 볼 수 있다. 
이러한 방식은 메인 서버 부하를 줄여 회사 입장에서 수천 달러를 절약할 수 있다.

### 프록시 서버의 종류
#### 1. 정방향 프록시 (Forward Proxy) : 클라이언트 측에 위치하며 요청을 웹 서버로 전달
- 클라이언크 소스 앞에 위치한다
- 회사에서 직원들의 인터넷 사용을 관리하고 제한하기 위해 사용된다.
- 기업의 네트워크를 보호하기 위해 방화벽으로 사용하여 위협이 될 수 있는 요청을 막는다.
- 사용자가 국가에서 차단된 서비스를 사용하려고할 때 이를 우회해서 사용하기도 한다.  
이는 프록시 서버가 사용자의 정보를 웹사이트 서버로 숨겨주기 때문에 사용자가 익명으로 브라우징을 할 수 있다.

#### 2. 역방향 프록시 (Reverse Proxy) : 서버 측에 위치하여 들어오는 요청을 여러 웹 서버로 전달
- 서버 앞에 위치하여 클라이언트의 요청을 받아 내부 서버로 전달한다.
- 백엔드 웹 서버의 익명성을 제공하며, 클라이언트의 익명성은 제공하지 않는다.
- 인증, 콘텐츠 캐싱, 암호화/복호화를 처리한다.  

-> 이러한 작업은 웹 메인 서버에서 작업하기에는 CPU 자원을 많이 소모하게 되어 웹 속도가 저하될 수 있다.
역방향 프록시가 이를 대신 수행함으로써 웹 서버의 성능을 유지하며 최적화한다.
- 로드 밸런싱을 하여 들어오는 트래픽을 여러 웹 서버에 고르게 분산시켜 서버 부하를 줄여준다. 이는 주요 기능이 아니긴하다.

--- 
즉 프록시 서버는 클라이언크-서버 사이의 게이트웨이 역할을 한다.  
네트워크에서 프록시 서버의 튀치에 따라 정방향 프록시인지 역방향 프록시인지 결정된다