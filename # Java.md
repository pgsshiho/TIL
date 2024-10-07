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
- extends를 이용하여 구현
- 추상메소드에 대한 구현 가능
- 추상 클래스의 기능을 재사용, 확장가능 측면에서 상속성을 지님
## 예외 처리
**목적**
1. 예외의 발생으로 인한 실행 중인 프로그램의 비정상 종료를 막기 위해
2. 개발자에게 알려서 코드를 보완할 수 있도록 하기 위해
**Throwable 에는 크게 두 종류의 자식 클래스가 있다 (Error & Exception)**
```
예외처리를 할 수 있는 최상위 클래스
```
```
필요한 것으로 표현할 수 없거나 구체적인 목적을 가진 예외를 정의한다면
Throwable 또는 그 하위에 있는 예외 클래스를 상속받아서 자신만의 예외 클래스를 정의가능
```
![예외](https://media.vlpt.us/images/codepark_kr/post/a70025be-d97d-4ba4-81de-bf9b8fe48d2b/ExceptionClassHierarchy.png)  
**try-catch(-finally) 형식**
```java
public class Main {
    public static void main(String[] args) {
        int number = 10;
        int result;

        for(int i = 10; i >= 0; i--){
        	//예외가 발생할 가능성이 있는 코드
            try{
                result = number / i;
                System.out.println(result);
            //예외가 발생했을 시 실행되는 코드 (catch는 여러개 작성 가능)
            }catch (Exception e){
                System.out.println("Exception 발생: " + e.getMessage());
            //예외의 발생여부에 관계없이 항상 수행되어야하는 코드
            }finally {
                System.out.println("항상 실행되는 finally 구문");
            }
        }

    }
}
```
**try-with-resource 형식**
(입출력과 함께 자주 쓰이는 구문, try-catch-finally구문보다 편리,알아서 close()호출)
```java
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.nio.charset.StandardCharsets;

public class Main {
    public static void main(String[] args) {
        //try 소괄호 안에 Closable의 인스턴스만 선언할 수 있다.
        //만약 소괄호 안에 쓰지 않는다면 메서드에도 exception 시그니쳐를 써야하며 close()구문도 추가해야한다.
        try (FileOutputStream out = new FileOutputStream("test.txt")){
            out.write("Hello".getBytes());
            out.flush();
        }catch (IOException e){
            System.out.println("IO Exception발생: " + e.getMessage());
            e.printStackTrace();
        }
    }
}
```
## DataTime
java.time패키지
LocalDate와 LocalTime은 java.time 패키지의 가장 기본이 되는 클래스
```java
package Chap_01;

import java.time.*;
import java.time.format.DateTimeFormatter;
import java.time.format.FormatStyle;
import java.util.Date;

public class Main {
    public static void main(String[] args) {

        System.out.println("now usage");
        LocalDate date = LocalDate.now();
        LocalTime time = LocalTime.now();
        LocalDateTime dateTime = LocalDateTime.now();

        System.out.println(date);
        System.out.println(time);
        System.out.println(dateTime);

        System.out.println("of() usage");
        LocalDate dateOf = LocalDate.of(2021, 3, 30);
        LocalTime timeOf = LocalTime.of(22, 50, 30);

        System.out.println(dateOf);
        System.out.println(timeOf);

        //formatter를 먼저 설정한다 (FormatStyle.SHORT/MEDIUM/LONG/FULL)
        DateTimeFormatter formatter = DateTimeFormatter.ofLocalizedTime(FormatStyle.SHORT);
        //formatter.format에 시간을 넣으면 String 타입으로 리턴된다.
        String shortFormat = formatter.format(LocalTime.now());
        System.out.println(shortFormat);

        //내가 직접 지정한 형식의 날짜를 출력할 수도 있다.
        DateTimeFormatter myFormatter = DateTimeFormatter.ofPattern("yyyy년 MM월 dd일").withZone(ZoneId.systemDefault());
        String myDate = myFormatter.format(new Date().toInstant());
        System.out.println(myDate);

        // 기간은 Period 클래스의 내장 메서드인 between을 사용하면 쉽게 구할 수 있다.
        LocalDate today = LocalDate.now();
        LocalDate birthday = LocalDate.of(1995, 2, 20);
        Period period = Period.between(today, birthday);
        System.out.println(period.getYears());
        System.out.println(period.getMonths());
        System.out.println(period.getDays());

    }

}
```
## Collection 프레임워크
**정의**
-다수의 데이터를 다루기 위한 자료구조를 표현하고 사용하는 클래스의 집합을 의미  
-데이터를 다루는데 필요한 풍부하고 다양한 클래스와 기본함수를 제공하기 때문에 유용  
-컬렉션 프레임워크의 모든 클래스는 Collection interface를 구현(implement)하는 클래스 또는 인터페이스  
**프레임워크 자료구조**
-List : 순서가 있는 데이터의 집합이며 데이터의 중복 허용 → ArrayList, LinkedList, Stack 등  
-Set : 순서를 유지하지 않는 데이터의 집합이며 데이터의 중복 허용X → HashSet, TreeSet 등  
-Map : 키(key)와 값(value)의 쌍으로 이루어진 데이터의 집합 순서는 유지되지 않으며 키는 중복 허용X 값은 중복 허용→ HashMap, TreeMap 등  
-Stack :마지막에 넣은 데이터를 먼저 꺼내는 자료구조LIFO(Last In First Out) → Stack, ArrayDeque 등  
-Queue :먼저 넣은 데이터를 먼저 꺼내는 자료구조입니다. FIFO(First In First Out)→ Queue, ArrayDeque 등  
## 제네릭스
### 정의
다양한 타입의 객체들을 다루는 메소드나 컬렉션 클래스에 컴파일 시의 타입 체크를 해주는 기능을 의미
**사용이유**
객체의 타입을 컴파일 시에 체크하기 때문에 안정성이 높아짐
```java
public class 클래스명<T> {...}
public interface 인터페이스명<T> {...}

//자주 사용되는 타입인자 약어

<T> == Type
<E> == Element
<K> == Key
<V> == Value
<N> == Number
<R> == Result

import java.util.ArrayList;
import java.util.Collection;
import java.util.List;

public class Main {
    public static void main(String[] args) {

        //List와 ArrayList의 Docs에서 get()을 보면
        //List에는 함수의 body가 없으나 ArrayList에는 있음!
        List<String> list = new ArrayList();
        list.add("String");

        // Collection docs로 가면 <E>가 선언되어있다.
        // <E>는 어떤 타입이든 올 수 있고, 원소를 뜻한다.
        // 해당 <>가 아닌 경우에는 앞에 <다른타입>을 지정한 뒤 사용한다 (toArray 참고)
        // <?>는 클래스 선언부에 쓰인 타입이 아니어도 괜찮다는 뜻이다.
        Collection<String> collection = list;

        List<Exception> exceptionList = new ArrayList<>();
        Collection<Exception> exceptionCollection = exceptionList;

        List<IllegalArgumentException> exceptions = new ArrayList<>();
        // 아래 주석을 풀면 addAll(Collection<? extends E> c)의 기능이 나옴!
        //exceptionCollection.addAll(list) -> Exception을 exepect하나 String이 들어왔다고 오류남
        exceptionCollection.addAll(exceptions);

    }
}
```
## 람다
### 정의
식별자 없이 실행 가능한 함수
### 특징
-람다식이 코드를 보다 간결하게 만들어주는 역할
-람다를 사용하여서 만든 익명 함수는 재사용이 불가능
-람다만을 사용할 경우 비슷한 메소드를 중복되게 생성할 가능성이 있으므로 지저분해질 수 있음
```java
//[기존의 메소드 형식]
반환타입 메소드이름(매개변수 선언) {
    수행 코드 블록
}

//[람다식의 형식]
반환타입 메소드이름(매개변수 선언) -> {
    수행 코드 블록
}

import java.util.ArrayList;
import java.util.List;
import java.util.Locale;
import java.util.stream.Stream;

public class Main {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        list.add("Korea");
        list.add("Japan");
        list.add("France");
        Stream<String> stream = list.stream();
        // map() 은 앞의 값을 어떤 값으로 변경할 때 사용한다.
        // 아래에서 str은 람다식에서 쓰일 매개변수명이며 여기에선 stream을 받아온다.
        // 람다에서 중괄호를 사용하면 return이 필요하다.
        stream.map(str -> {
            System.out.println(str);
            return str.toUpperCase();
        // ::은 매개변수가 하나일 때 간결하게 표현해주는 방법이다.
        }).forEach(System.out::println);
    }
}

// :: 연산자
public class Main {
    public static void main(String[] args) {
        List<String> cities = Arrays.asList("서울", "부산", "속초", "수원", "대구");
        cities.forEach(System.out::println);
    }
}
//이중 콜론 연산자는 매개변수를 중복해서 사용하고 싶지 않을 때 사용하곤 합니다. 
//출력결과를 보시면 cities의 요소들이 하나씩 출력 될 것입니다. 
//즉, cities.forEach(x -> System.out.println(x)); 와 같은 의미
```
## 스트림
### 정의
**데이터의 흐름**
컬렉션의 저장 요소를 하나씩 참조해서 람다식으로 처리할 수 있도록 해주는 반복자
스트림을 활용해서 필터링,데이터 변경, 다른 타입이나 자료구조로 변환 등 가능
### 특징
데이터 소스를 변경X
작업을 내부적으로 반복 처리
컬렉션의 요소를 모두 읽고 나면 닫혀서 재사용이 불가 -> 필요할 경우 재생성
### 구조
1. 스트림생성`Stream<T> Collection.stream()`
2. 중간 연산(데이터의 형변환 혹은 필터링, 정렬 등 스트림에 대한 가공)(map,변환/sorted,정렬/skip,스트림 자르기/limit,스트림 자르기)
3. 최종 연산(요소를 소모해서 결과를 반환하는 단계)(collect()를 이용해서 다른 콜렉션으로 바꾸는 것, reduce를 이용해서 incremental calculation하는 것도 가장 많이 쓰이는 패턴)
```java
import java.util.ArrayList;
import java.util.List;
import java.util.stream.Stream;

public class Main {
    public static void main(String[] args) {
        // stream을 통해 흘러들어오는 데이터를 처리해줄 수 있다.
        // (Collection 등).stream()을 하면 stream을 생성할 수 있다.
        List<String> list = new ArrayList<>();
        list.add("korea");
        list.add("japan");
        list.add("france");
        Stream<String> stream = list.stream();
        // 생성된 후 부터는 해당 스트림의 요소 하나씩! iterator 처럼 돌며 연산을 해준다.
        //map()은 요소의 상태를 변경시킬 때 사용한다.
        stream.map(str -> {
            //따라서 하나의 요소마다 소문자, 대문자가 출력되는 것이다!
            System.out.println(str);
            return str.toUpperCase();
            // ::은 매개변수가 하나일 때 간결하게 표현해주는 방법이다.
        }).forEach(x -> System.out.println(x));

        // stream은 데이터 원본을 변경하지 않는다. 따라서 소문자 리스트가 출력된다.
        System.out.println(list);
    }
}
```