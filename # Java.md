# Java
## 자료형
자료형은 2가지로 나뉘어진다 
1. 기본자료형
2. 참조자료형
### 기본자료형
기본 자료형은 
short,int,long,float,double,char,boolean,byte 등이있다
또한 아래의 코드로 최대,최소값을 알수있다
``` System.out.println(Short.MAX_VALUE);
System.out.println(Short.MIN_VALUE);
```
### 참조자료형
참조자료형은 위 **기본 자료형을 제외한 모든 자료형**을 뜻한다
밑에는 참조 자료형의 예시 코드이다
```
int arr[]; //배열선언
arr = new int[5] // 배열 생성
```
## 조건문
if / else if / else / switch / 삼항 연산자 등이 있다 예시코드
if
```
if (i>10){
    System.out.println("10보다 큽니다");
}//만약에 이렇다면 이렇게 해라 라는식
```
else if
```
if (i%2==0){
    System.out.println("2의 배수");
}
else if (i%3==0){
    System.out.println("3의 배수");
}//2의 배수 3의 배수 구분
```
else 
```
if (i%2==0){
    System.out.println("짝수");
}
else {
    System.out.println("홀수");
}//짝수와 홀수 구분
```
switch
```
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
삼항연산자
```
String a = (b<10) ? "10보다 작다" : "10보다 크다"
```
## 반복문
c언어 기반 언어라 그런지 비슷하다
```
for (int i = 0;i<5;i++){
    System.out.println(i)
}//0~4까지 출력이 되고 5까지가 아닌 5미만 이라는 뜻이기에 1~5 까지 할려면 i를 1로잡고 5가아닌 6이오면 된다
```

