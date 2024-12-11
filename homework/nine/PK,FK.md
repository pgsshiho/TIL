# PK,FK
## 기본 키(PK)
### 정의
테이블 내에서 유일하게 존재하는 값의 조합을 설정해서,**중복된 데이터가 테이블에 삽입되는것을 방지**
- 중복된 값X
- 데이터를 매우 빠르게 찾을 수 있음O
### 특징
- 해당 필드가 NOT NULL 과 UNIQUE 제약 조건의 특징을 모두 가지게 됨
- 반드시 존재하므로, NOT NULL
- 유일한 값이므로, UNIQUE
## 외래 키(FK)
### 정의
- 다른 기본 키를 참조하는 속성 or 속성들의 집합
### 특징
- 참조 관계의 기본 키와 같은 속성을 가짐
- 데이터가 새롭게 추가될 때, 외래 키에 해당하는 값이 외래 키가 참조하는 테이블에 존재하는지를 확인
### 하나의 테이블을 다른 테이블에 의존하게 만듦 (두 테이블을 연결하는 다리 역할)
- 외래 키가 포함된 테이블 = 자식 테이블
- 외래 키 값을 제공하는 테이블 = 부모 테이블
### 데이터의 무결성 보장
- 하나의 테이블에서 중복된 데이터가 삽입되는 것을 방지
- 외래 키를 가지는 테이블이 참조하는 기준 테이블의 열은 반드시 PK, UNIQUE 제약조건이 설정되어 있어야 한다.
### DB 는 무조건 다(N)쪽이 외래 키를 갖는다
- 연관관계의 주인 O : 두 객체 사이에서 '조회, 저장, 수정, 삭제' 가능
- 연관관계의 주인 X : '조회'만 가능
## Spring 에서 기본 키 적용
### JPAd에서 기본 키 설정
- @id 어노테이션: 엔티티 클래스에서 기본 키를 설정할 때 사용
- @GeneratedValue: 기본 키 값이 자동 생성되도록 설정. 이 때 전략을 지정 가능
```java
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY) // AUTO_INCREMENT
    private Long id;

    private String name;
}
```
### 기본 키 생성 전략
- GenerationType.AUTO: 데이터베이스의 기본 설정을 따름
- GenerationType.IDENTITY: 데이터베이스의 AUTO_INCREMENT 기능 사용
- GenerationType.SEQUENCE: 데이터베이스 시퀀스를 사용
- GenerationType.TABLE: 별도의 키 생성 테이블을 사용
### 복합 키 설정
- @IdClass: 기본 키가 복합적인 경우 별도의 클래스에 복합 키 정의
- @EmbeddedId: 내장 객체를 사용하여 복합 키를 정의
## Spring에서 외래 키 적용
### JPA에서 외래 키 설정
- @ManyToOne: 다대일 관계에서 외래 키를 설정
- @OneToMany: 일대다 관계를 설정 (실제로 FK는 Many 측에 위치)
- @JoinColumn: 외래 키 열의 이름을 명시적으로 설정
```java
@Entity
public class Order {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @ManyToOne
    @JoinColumn(name = "user_id") // FK가 매핑될 열
    private User user;
}
```
### 관계 설정의 방향
- 양방향 관계: @OneToMany와 @ManyToOne을 모두 설정
- 단방향 관계: 한쪽에서만 외래 키를 참조
### Cascade 옵션
- CascadeType.ALL: 엔티티 상태 변화(삽입, 수정, 삭제)가 관계된 엔티티에도 전파.
- CascadeType.PERSIST: 저장만 전파.
- CascadeType.REMOVE: 삭제만 전파.
```java
@OneToMany(mappedBy = "user", cascade = CascadeType.ALL)
private List<Order> orders;
```
### 연관 관계의 주인 설정
- mappedBy를 사용하여 주인을 명시.
- 연관 관계의 주인만 데이터베이스 변경을 처리.
## Spring Boot 데이터베이스 무결성 및 검증
