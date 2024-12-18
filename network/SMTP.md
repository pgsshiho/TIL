# SMTP(Simple Mail Transfer Protocol)
## 정의
인터넷을 통해 이메일 메시지를 보내고 받는 데 사용되는 통신 프로토콜
## SMTPS
SMTP를 보호하는 방법
기밀성 및 무결성 보장
SSL/TLS로 보호함
## SMTP 서버 
발신 이메일 메시지를 처리하는 컴퓨터 또는 소프트웨어
**SMTP 서버는 발신 이메일을 적절한 목적지로 보내고 릴레이하는 작업에만 관심**
## SMTP 서버 설정
컴퓨터, 서버 또는 클라우드에 SMTP 서버 소프트웨어 설치
일반적으로 서버 주소, 포트 번호, 보안 프로토콜 및 인증 옵션과 같은 서버 설정을 구성
## 이메일 보내는 과정
1. 발신자의 이메일 클라이언트 또는 서버가 수신자의 SMTP 서버와 연결을 설정
2. 수신자의 이메일 주소와 같은 필수 정보를 제공
3. SMTP 서버는 이 정보를 처리하고 수신자의 주소를 확인하여 이메일 수락 여부를 결정
4. 수신자 주소가 유효하면 이메일이 배달 대기열에 추가
5. 수신자의 서버가 수신자의 이메일 받은편지함이나 지정된 폴더로 이메일을 전송하려고 시도
## 단점
**SMTPS로 암호화를 하지않으면 암호화가 되어있지않음**
**대체 기술이 많음 ex), IMAP(Internet Message Access Protocol), POP3(Post Office Protocol)**
**스팸 및 피싱등의 보안문제를 해결하는 데 복잡함**