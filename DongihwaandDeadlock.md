# 동기화
## 정의
한 번에 하나의 프로세스만 접근할 수 있도록 제한을 두는 것
## 사용이유
공유된 자원에 여러 프로세스/스레드가 동시에 접근하면 Critical section 문제가 발생하기 떄문
```critical section이란 각 프로세스에서 공유 자원에 접근하는 프로그램 코드 영역```
## 동기화 기법
1. wait
2. signal
2개의 atomic operations을 사용
```atomic operations 원자와 같이 기능적으로 분할할 수 없거나 분할되지 않도록 보증된 조작```
- wait 임계 구역에 들어가도 되는지 확인하고, 안되면 계속해서 기다린다.
- Signal 임계 구역에서 작업을 마치고 Wait중인 프로세스/스레드를 깨워줘서 들어갈 수 있게 한다.
### Mutex
![Mutex](C:\Users\user\Desktop\image.png)