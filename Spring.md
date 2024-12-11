# Spring
## 정의
Java의 오픈소스 애플리케이션 프레임워크
## 특징
### 경량 컨테이너
IoC(제어의 역전)를 통해 객체를 관리, 애플리케이션의 의존성 설정 및 조립
XML, 자바 Config, 어노테이션 기반 설정을 지원
### IoC,DI
IoC: 객체 생성 및 생명주기 관리의 책임을 스프링 컨테이너가 맞음
DI:객체 간의 의존성을 코드가 아닌 설정으로 주입
```Java
@Autowired
private UserService userService;
```
### AOP
관점 지향 프로그래밍을 지원하여 로깅, 트랜지션 관리 등 공통 기능을 쉽게 모듈화 가능
```Java
@Aspect
public class LoggingAspect {
    @Before("execution(* com.example.service.*.*(..))")
    public void logBefore(JoinPoint joinPoint) {
        System.out.println("Method: " + joinPoint.getSignature().getName());
    }
}
```
### 트랜지션(SQL언어로 DB에 접근하는 것) 관리
데이터베이스 트랜잭션 처리를 손쉽게 처리할 수 있도록 지원
```Java
@Transactional()
public void processOrder() {
    // 트랜잭션 안에서 수행될 작업
}
```
### POJO기반 개발
스프링은 특별한 API 없이 일반 자바 객체(POJO)를 활용해 개발을 지원
### 모듈화된 구조
필요한 기능만 선택적으로 사용 가능,특정 기능의 의존성을 최소화
## spring boot
스프링 기반으로 하여 애플리케이션을 쉽게 생성하고 배포하기 위한 모듈
의존성 관리와 라이브러리의 설정을 해줌,배포가 편해짐
### 내장 서버
톰캣이라고 하는 내장 서버가 있어서 별도의 서버를 설치할 필요가 없음
### 자동 라이브러리 관리
수많은 라이브러리를 베스트 프랙티스 기반으로 자동으로 성택하고 관리함으로써 프로젝트를 빨리 시작할 수 있음
### 자동 구성
복잡한 스프링 설정을 자동화함으로써 개발자가 쉽고 빠르게 애플리케이션을 개발 가능
### 외부 설정
애플리케이션을 개발 환경  ↔  운영 환경처럼 서로 다른 환경에서 사용할 때 필요한 외부 설정값을 편리하게 조회가능
### 모니터링 & 관리 기능
애플리케이션의 수많은 지표를 자동으로 수집/모니터링/관리 기능 제공