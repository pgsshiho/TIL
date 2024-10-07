# Java
## 자료형
자료형은 2가지로 나뉘어진다 
1. 기본자료형
2. 참조자료형
### 기본자료형
기본 자료형은 
short,int,long,float,double,char,boolean,byte 등이있다
또한 아래의 코드로 최대,최소값을 알수있다
``` java
System.out.println(Short.MAX_VALUE);
System.out.println(Short.MIN_VALUE);
```  
### 참조자료형
참조자료형은 위 **기본 자료형을 제외한 모든 자료형**을 뜻한다
밑에는 참조 자료형의 예시 코드이다
```java
int arr[]; //배열선언
arr = new int[5] // 배열 생성
```  
---
## 조건문
if / else if / else / switch / 삼항 연산자 등이 있다 예시코드  
**if**
```java
if (i>10){
    System.out.println("10보다 큽니다");
}//만약에 이렇다면 이렇게 해라 라는식
```  
**else if**
```java
if (i%2==0){
    System.out.println("2의 배수");
}
else if (i%3==0){
    System.out.println("3의 배수");
}//2의 배수 3의 배수 구분
```  
**else** 
```java
if (i%2==0){
    System.out.println("짝수");
}
else {
    System.out.println("홀수");
}//짝수와 홀수 구분
```  
**switch**
```java
switch(day){
    case "주말":
        System.out.prinln("주말");
        break;//break가 없으면 조건에 충족하는 것이 하나있어도 밑에까지 충족이 되면 계속 나온다
    case "평일"
        System.out.println("평일");
        break;
    case "공휴일"
        System.out.println("공휴일");
        break;
}//else if 와 비슷하지만 많아질수록 switch 문이 편하다
```  
**삼항연산자**
```java
String a = (b<10) ? "10보다 작다" : "10보다 크다"
```  
---  
## 반복문
c언어 기반 언어라 그런지 비슷하다  
**for**
```java
for (int i = 0;i<5;i++){
    System.out.println(i)
}//0~4까지 출력이 되고 5까지가 아닌 5미만 이라는 뜻이기에 1~5 까지 할려면 i를 1로잡고 5가아닌 6이오면 된다 기본 of 기본
```  
**for each**
```java
ages = {15,20,43,72,11}
for (int age = ages){
    System.out.println(age);
}//파이썬에서 많이 사용됨
```  
**while**
```java
while(1){
    i += 1
    if(i > 100){
        break;
    }//선 조건 확인 후 실행 조건이 안맞으면 애초부터 실행 X
    System.out.printle(i)
}
```  
**do while**
```java
do{
    sum += (i+1)
    i ++;
}while (i<10>)
System.out.println(num);//선 실행 후 조건확인 즉 조건에 맞지 않아도 한번은 돤다
```  
---  
## 클래스,인스턴스,메소드
### 클래스
**공통 속성을 한 군데에 정의해 놓은 것**
예를 들자면 자동차라고 했을때 '자동차' 라는 것이 클래스
```java
class chicken{
    String name;
    int price;
}
public class Main{
    public static void main(String[] args){
        chicken.G = new chicken();//즉 이제부터 G는 chicken을 참조한다(그냥 알기쉽게 설명하면 chicken안에 있는것을 G.으로 사용 가능하다는 것)
        G.name = "허니콤보"
        G.price = 23000

        chicken.B = new chicken();//헷갈릴수 있는데 참조한것이지 G==chicken이 아니기에 다른걸로 참조하면 다른 값도 저장이 가능하다
        B.name = "자메이카"
        B.price = 21500
    }
}
```  
**메소드**
```java
int add(int x,int y){
    int result = x + y;
    return result
}//말이 메소드지 그냥 함수구나 하고 생각하면 편하다
```  
**생성자**
```java
class chicken{
    String name;
    int price;

    //생성자 우리가 자바를 쓸때 클래스를 만들고 한번더 탭누르면 나오는 그게 생성자이다
    chicken(String name,int price){
        this.name = name
        this.price = price//여기서 this는 자기 자신을 나타낼때 사용한다 앞쪽 name은 필드 뒷쪽 name 은 매개변수를 뜻함
    }

}
```  
---  
## 상속
1. 부모 클래스에서 정의된 필드,메소드를 물려받음
2. 새로운 필드,메소드 추가가능
3. 부모 클래스에서 받은 메소드 수정 가능  
``` java
class chicken{}
class BBQ extends chicken{}
class BHC extends chicken{}
```  
### super,super()메소드
부모 클래스로부터 상속받은 필드,메소드,생성자를 자식 클래스에서 참조하여 사용을 원할때 사용하는 키워드  
### this, this()메소드와의 차이
this()는 같은 클래스의 다른 생성자
super()부모클래스의 생성자
그래서 super()의 매개변수 자리에 부모 클래스 생성자의 매개 변수와 같게 들어가야한다
### 오버로딩과 오버라이딩
**오버로딩**
한 클래스 내에 동일한 이름의 메소드를 여러개 정의하는것
모두 같아야만 한다
```java
int add(int x, int y, int z) {
    int result = x + y + z;
    return result;
}
long add(int a, int b, long c) {
    long result = a + b + c;
    return result;
}
int add(int a, int b) {
    int result = a + b;
    return result;
}
```
**오버라이딩**
부모 클래스로부터 상속받은 메소드의 내용을 변경하는 것
단 메소드,이름.매개변수,반환타입이 모두 같아야한다
```java
class Animal {
    String name;
    String color;

    public void cry() {
        System.out.println(name + " is crying.");
    }
}

class Dog extends Animal {
    Dog(String name) {
        this.name = name;
    }
    @Override
    public void cry() {
        System.out.println(name + " is barking!");
    }
    public void swim() {
        System.out.println(name + " is swimming.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal dog = new Dog("코코");

        dog.cry();
    }
}
```  
---
## 접근 제어자
- private : 같은 클래스 내에서만 접근가능
- default(nothing) : 같은 패키지 내에서만 접근가능
- protected : 같은 패키지 내,다른 패키지의 자손클래스에서 접근 가능
- public : 접근 제한이 전혀 없음
  접근 제어자로 제어하는 것 == 캡슐화
---
## 추상클래스
- 추상메소드를 선언할 수 있는 클래스
- 상속받는 클래스 없이 그 자체로 인스턴스를 생성 불가능
- 설계만 되어있음
- 수행되는 코드에 대해서는 작성이 안된 메소드
- 
```java
// 추상 클래스 정의
abstract class Animal {
    // 추상 메서드 (구현이 없음)
    public abstract void sound();

    // 일반 메서드 (구현이 있음)
    public void sleep() {
        System.out.println("동물이 잠을 잡니다.");
    }
}

// 추상 클래스를 상속받은 자식 클래스
class Dog extends Animal {
    // 추상 메서드 구현
    public void sound() {
        System.out.println("멍멍");
    }
}

class Cat extends Animal {
    // 추상 메서드 구현
    public void sound() {
        System.out.println("야옹");
    }
}

public class Main {
    public static void main(String[] args) {
        // Animal 클래스는 추상 클래스이므로 직접 인스턴스화 할 수 없음
        // Animal animal = new Animal(); // 오류 발생!

        // 추상 클래스를 상속받은 자식 클래스를 인스턴스화
        Animal dog = new Dog();
        dog.sound();  // "멍멍" 출력
        dog.sleep();  // "동물이 잠을 잡니다." 출력

        Animal cat = new Cat();
        cat.sound();  // "야옹" 출력
        cat.sleep();  // "동물이 잠을 잡니다." 출력
    }
}
```
## 인터페이스
**단일 책임, 리스코프 치환, 의존성 역전 원칙을 따르도록 도와주는 중요한 개념**
```
정의가능
- 접근제어자
- 리턴타입
- 메소드 이름
```
함수내용 존재X  
형식  
```
interface 인터페이스명{ public abstract void 추상메서드명(); }
```
예시  
```java
interface Flyable{
    // 인터페이스는 멤버를 가지지 못하고, 동작(메서드)만 정의할 수 있다.
    // 또한 정의한 메서드는 내용을 가질 수 없다
    void fly(int x, int y, int z);
}
// 인터페이스는 다중 상속(implements)할 수 있다.
class Pigeon implements Flyable{
    private int x, y, z;
    @Override
    public void fly(int x, int y, int z) {
        printLocation();
        System.out.println("날아갑니다.");
        this.x = x;
        this.y = y;
        this.z = z;
        printLocation();
    }

    public void printLocation(){
        System.out.println("현재 위치 (" + x + ", " + y + ", " + z + ")");
    }
}
public class Main {
    public static void main(String[] args) {
        Flyable pigeon = new Pigeon();
        pigeon.fly(1,2,3);

    }
}
```
### 추상 클래스와 차이점
**인터페이스**
- 인터페이스는 모든 메소드가 추상메소드 이다
- 구현하려는 객체의 동작의 명세
- 다중 상속 가능
- implements를 이용하여 구현
- 메소드 시그니처(이름, 파라미터, 리턴 타입)에 대한 선언만 가능
- 같은 이름의 메서드가 클래스에 따라 다르게 동작하도록 구현되는 것을 말하는 다형성을 지님
**추상 클래스**
- 클래스를 상속받아 이용 및 확장을 위함
- 다중 상속 불가능, 단일 상속
- ectends를 이용하여 구현
- 추상메소드에 대한 구현 가능
- 추상 클래스의 기능을 재사용, 확장가능 측면에서 상속성을 지님
- 
