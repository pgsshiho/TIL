# 정의
- 프로세스가 네트워크에 데이터를 보내거나 데이터를 받기위한 실직적인 창구역할
- IP,Protocall,Port 등이 전부 여기에 포함된다
# 소켓통신의 흐름
- 소켓의 흐름은 크게 서버와 클라이언트로 나뉜다
## 서버(Server)
1. socket()함수로 소켓을 생성
2. bind() 함수로 ip와 prot번호 설정
3. listen() 함수로 클라이언트의 접은 요청에 수신 대기열을 만들어 몇 개의 클라이언트를 대기 시킬지 결정
4. accept() 함수를 사용하여 클라이언트와 연결을 기다림
## 클라이언트
1. socket() 함수로 가장먼저 소켓을 염
2. connect() 함수를 이용하여 통신 할 서버의 설정된 ip와 port 번호의 통신을 시도
3. 통신을 시도 시, 서버가 accept()함수를 이용해 클라이언트의 socket descriptor를 반환
4. 이를 통해 클라이언트,서버는 서로 read(),write() 를 하며 통신(이 과정이 반복)
# 종류
- [스트림 (TCP)](https://github.com/pgsshiho/TIL/blob/main/network/TCP.md)
- [데이터그램 (UDP)](https://github.com/pgsshiho/TIL/blob/main/network/UDP.md)
# HTTP 통신과 SOCKET 통신의 비교
## [HTTP](https://github.com/pgsshiho/TIL/blob/main/network/HTTP.md) 통신
- 클라이언트의 요청이 있을때만 서버가 응답을 하여 해당 정보를 전송후 곧바로 연결을 종료함
## SOCKET
- Server와 Client가 특정 Port를 통해 실시간으로 양방향 통신을 하는 방식
### SOCKET 통신의 특징
- Server와 Client가 계속 연결을 유지하는 양방향 통신이다.
- Server와 Client가 실시간으로 데이터를 주고받는 상황이 필요한 경우에 사용된다.
- 실시간 동영상 Streaming이나 온라인 게임 등과 같은 경우에 자주 사용된다.
