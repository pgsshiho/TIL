# 정의
- CORS(Cross-Origin Resource Sharing)
- 애플리케이션을 통합하기 위한 매커니즘
- 한 도메인에서 로드되어 다른 도메인 에 있는 리소스와 상호작용 하는 것 
# 작동방법
1. 브라우저가 현재 오리진의 프로토콜,호스트,포트등에 대한 정보가 들어있는 오리진 해더를 요청
2. 서버는 현재 오리진 해더를 확인후 요청한 데이터와 Acess-Control-Allow-Origin 헤더로 응답
3. 브라우저는 액세스 제어 요청 헤더를 확인 후 반환된 데이터를 클라이언트 애플리케이션과 공유