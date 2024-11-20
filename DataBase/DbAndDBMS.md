# DB and DBMS
## 정의
여러 사람이 공유하여 사용할 목적으로 체계화해 통합, 관리하는 데이터의 집합
## 종류
**Key=value Database**(키와 수를 나누는 DB 서브용으로 쓰임)
**redis**(Key=value Database와 비슷하지만 하드디스크가 아닌 램에 1차적으로 저장 / 메인DB에서 받은걸로 유저에게 전해주는 식으로 서브용으로 사용)
일반적인 용도로 사용
### Relational Database (정확도가 중요한 서비스에 사용)
- 오라클,MySQL등등(대량의 데이터를 저장하고 싶을 때 사용)
- ACID Transaction 기능 탑제
- 데이터를 큐형태로 저장하고 싶을 때 사용
- DB사용률이 가장 높다
- 보통 데이터를 정규화해 저장(중복X)
### Document Database(입출력이 잦으면사용)
- MongoDB,CouchDB등이있음
- 일반적인 DB
- 폴더을 만들고 그안에 document파일을 만듦 그안에 데이터를 JSON으로 저장
- 수정이 편함
- 데이터의 중복 제거안함(정규화X)
- 분산처리가 좋음
### Graph Database(관계를 주로 저장)
- neo4j,OrientDB등이 있음
- 노드를 만들고 노드에 저장가능
- 노드끼리 어떤관계인지도 작성가능
- 비행기 노선,SNS 친구관계등에 사용
### Column-family Database
- cassadra,apacheHBASE등이있음
- 테이블을 만든후→로우를 만들어 데이터기입
- 표를 만들때 좋음
- 얘네들 언어사용해야함
- 정규화X
- 복제,분산잘함(일관성부족)
- 시간기록 잘됨
### Search engine
- 일반적인 DB로 사용가능 하지만 Index보관의 특화
- (Index:빠른 검색 도와주는 것,기존DB에서 받음)
- 실시간 검색,추천,오타 교정등이 쉬움
##  DBMS(Database Management System)
### 정의
DB를 사용하기 위한 도구
### 특징
c언어로 예를 들면 DBMS=vs DB=c언어(예시일뿐 전혀 다르다)
데이터베이스를 운영하고 관리하는 소프트웨어.
계층형, 망형, 관계형 DBMS 중 대부분의 DBMS가 테이블로 구성된 관계형 DBMS(RDMBS)형태로 사용됨.
여러 접근을 가능하게 만드는 것을 가능하게 만듦
### 종류
MySQL, 오라클(Oracle), SQL 서버, MariaDB등
### 계층형 DBMS
각각 층을 가지 DBSM 현재는 사용하지 않음
### 망형 DBMS
망처럼 이어진 DBMS 현재는 잘 사용하지않음
### 관계형 DBMS
대부분의 DBMS가사용
## 장점
1. **자료의 통합성**증진
2. **데이터의 접근성**이 용이
3. 애플리케이션 프로그램들을 **쉽게 개발하고 관리**가능
4. **보안 강화**
## SQL(Structured Query Language)
구조화된 질의 언어
DB에서 사용되는 언어
Relational Database에서 사용되는 언어, 표준 SQL을 배우면 대부분의 DBMS를 사용가능.
