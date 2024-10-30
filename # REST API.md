# REST API
## REST정의
Representational State Trsnfer  
자원의 이름으로 구분하여 해당 자원의 상태를 교환하는 것을 의미  
REST는서버와 클라이언트의 통신 방식 중 하나임  
HTTP URI(Uniform Resource Identifier)를 통해 자원을 명시하고 HTTP Method룰 통해 자원을 교환하는것
```
HTTP Method
Creat  
Read  
Upadate  
Delete  
```
### URI란?
인터넷에 있는 자원을 나타내는 **유일한 주소**
인터넷에 존재하는 **각종 정보들의 유일한 이름이나 위치를 표시하는 식별자** 
## REST특징
### Server -client 구조
자원이 있는 쪽이 Server, 요청하는 쪽이 Client
클라이언트와 서버가 **독립적으로 분리**되어 있어야 함
### Stateless
요청 간의 클라이언트 정보가 **서버에 저장되지 않음**  
서버는 각각의 요청을 **완전히 별개의 것으로 인식**하고 처리
### Cacheable
HTTP 프로토콜을 그대로 사용하기 때문에 **HTTP의 특징인 캐싱 기능을 적용**  
대량의 적용을 효율적으로 처리하기 위해 캐시를 사용  
## REST장점
HTTP 표준 프로토콜을 사용하는 **모든 플랫폼에서 호환 가능 ** 
서버와 클라이언트의 역할을 **명확하게 분리**  
여러 서비스 설계에서 생길수 있는 문제를 최소화   
## REST API의 정의
REST 아키택처의 조건을 준수하는 어플리케이션 프로그래밍 인터페이스를 뜻함  
최근 많은 API가 REST API로 제공중  
일반적으로 REST 아키택처를 구현하는 웹 서비스를 RESTful이라고 표현  
## REST API의 특징
REST 기반으로 시스템을 분산하여 **확장성과 재사용성을 높임**
HTTP 표준을 따르고 있어 **여러 프로그래밍 언어로 구현가능**
## REST API의 설계규칙
1. 웹 기반의 REST API를 설계할 경우 URI를 통해** 자원을 표현**해야함
   ```
   https://thinkground.studio/member/589  
   Resource : member  
   Resource id:589  
   ```
2. 자원의 대한 조작은 **HTTP Method(CRUD)를 통해 표현**해야 함
   ```
   URI에 행위가 들어가면 안됨  
   HEADER를 통해 CRUD를 표현하여 동작을 요청해야 함  
3. 메세지를 통한 리소스 제작  
   ```
   HEADER를 통해 content-type을 지정하여 데이터를 전달  
   대표적 형식으로는 HTML,XML,JSON,TEXT가 있음  
   ```

