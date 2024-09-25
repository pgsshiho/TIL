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

