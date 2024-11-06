# Linux
## 정의
무료 오픈 소스 운영 체제(시스템 그룹)  
### Linux의 구성요소
```
- 부트로더(Bootloader):컴퓨터의 부팅 프로세서를 처리하는 소프트웨어
- 커널(kernel):시스템과 컴퓨터의 모든 부분을 관리하는 시스템의 핵심 부분
- 데몬(Daemon):사운드와 같은백그라운드 서비스
- Init 시스템:사용자 계정괴 데몬을 처리하는 시스템
- 그래픽 서버:모니터의 그래픽 디스플레이를 관리하는 하위 시스템
- 데스크톱 환경: 사용자 인터페이스(UI)
- 애플리케이션: 워드 프로세서,인터넷 브라우저등 사용자가 다양한 기능을 위해 사용하는 소프트웨어
```
## 특징
다른 운영체제와 다르게 UX에 중점을 둔 다른 운영체제와 달리 **미니멀한 UI**를 가짐  
매우 기능적으로 설계되어 사용자가 **시스템과 하드웨어를 광범위하게 제어**가능  
자유로운 커스터마이징과 **제어가 가능한 오픈 소스 코딩 그리고 운영 체제를 유지하는 대규모 커뮤니티**  
여러 배포판 존재(Ubuntu,Suse,Redhat,Cent OS등)  
**리눅스 OS**
```
서버 OS:모든 유형의 대용량 서버 애플리케이션의 적합
데스크톱 OS:기존 데스크톱 환경을 선호하는 일반 컴퓨터 사용자에게 적합
헤드리스 서버 OS:그래픽 UI가 필요하지 않는 원격 네트워크 서버에 적합
임베디드 디바이스 OS:가전제품과 같은 간단한 컴퓨팅 기능용
네트워크 OS:네트워킹이 필요한 경우
소프트웨어 개발 OS:엔터프라이즈 소프트웨어 개발의 적합
클라우드 OS:주요 클라우드 컴퓨팅용
```
Windows 및 MacOS보다 더 복잡한 운영 체제이며 훨씬 더 많은 커스터마이징 옵션을 제공하기 때문에 기술 경험이 풍부한사람들이 널리 사용  
## 차이점
대부분의 운영 체제는 독립 아키텍처에서 실행,Linux는 오픈 소스 소프트웨어→누구나 코드와 시스템을 보고 편집가능  
다양한 배포판과 소프트웨어 옵션이 있어 커스터마이징이 가능  
## 보안
안전성 보장에 도움이 되는 다양한 기능을 갖추고 있음에도 불구하고 완벽하게 안전한 운영 체제는 존재X
Linux를 더 안전한 운영 체제로 만드는 몇 가지 기능이 있음
### 사용자 권한
모든 사용자는 개별 ID와 비밀번호가 필요
접근 권한이 여러 수준으로 구분
### 오픈 소스 코드
소스 코드는 신중하게 검토되고 유지되는 여러 하위 시스템으로 나뉘어져 있어 모든 변경 사항을 신중하게 검사 가능  
오픈 소스 코드이므로 더 많은 사람이 코드를 보고 취약점을 테스트 가능  
취약점이 발견되면 Linux의 안전성 유지에 도움이 되는 보안 패치를 삽입하는 향상된 코드를 배포 가능  
### 시스템 이벤트 로그
모든 파일 및 시스템 액세스를 추적하는 로그 파일을 유지: 실패한 로그인 시도, 변경 사항, 보안 문제 로그 파일 등이 있음
### SELinux
Linux Kernel에 유연한 강제적 접근통제 시스템을 기본적으로 제공하여 관리자가 파일 접근 권한을제어할 수 있도록 해줌  
관리자는 SELinux를 통해 모든 애플리케이션과 프로세스, 파일에 대한 접근 권한을 정의하여 보안을 관리 가능
### Linux가 Windows나 다른 운영 체제보다 안전한가
더 안전함 ㅇㅇ 
```
사용자 권한(User permissions)
소프트웨어 설치
코드
업데이트
사용자층
다양성
```의 이유로