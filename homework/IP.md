- **사설과 공용 IP**
    
    ## 사설IP
    
    집이나 사무실 내부의 로컬 네트워크에서 사용,인터넷에 직접연결되지 않는다
    
    로컬 네트워크 내에서만 유효,라우터를 통해 공인 IP로 변환되어야 다른 장치들과 통신가능
    
    범위 IP(10.0.0.0~10.255.255.255,172.16.0.0 ~ 172.31.255.255,192.168.0.0 ~ 192.168.255.255)
    
    ---
    
    ## 공용 IP
    
    인터넷 서비스 제공자에 의해 할당되며 전역 인터넷에서 사용
    
    인터넷을 통해 전세계적으로 공개되며 고유한 식별자 역할
    
    다른 장치나 인터넷 접근 가능
    
    ---
    
    ## 클래스
    
    **네트워크 영역과 호스트영역**을 나누는 방법
    
    IP주소를 3개의 클래스로 나누는 이유는 **네트워크 크기에 따른 구분**
    
    ### A Class
    
     **IP주소를 32자리 2진수로 표현했을때, 맨 앞자리 수가 항상 0 인 경우**
    
     **0xxx xxxx**. **xxxx xxxx. xxxx xxxx. xxxx xxxx**
    
    2진수:0000 0000. 0000 0000. 0000 0000. 0000 0000 ~ 0111 1111. 1111 1111. 1111 1111. 1111 1111
    
    10진수:0.0.0.0 ~ 127.255.255.255
    
    ### B Class
    
    **IP주소를 32자리 2진수로 표현했을때, 맨 앞자리 수가 항상 10인 경우**
    
     1**0xx xxxx**. **xxxx xxxx. xxxx xxxx. xxxx xxxx**
    
    2진수:1000 0000. 0000 0000. 0000 0000. 0000 0000~1011 1111. 1111 1111. 1111 1111. 1111 1111
    
    10진수:128.0.0.0 ~ 191.255.255.255
    
    ### C Class
    
    **IP주소를 32자리 2진수로 표현했을때, 맨 앞자리 수가 항상 110인 경우**
    
     11**0x xxxx**. **xxxx xxxx. xxxx xxxx. xxxx xxxx**
    
    10진수:192.0.0.0 ~ 223.255.255.255
    
    ---
    
    ## 결론
    
    우리가 대부분 사용하고 있는 것은 사설IP지만 간혹가다 공용을 사용하는 경우도 있다
    
    우리는 사설의 사설IP를 사용하고 있는 걸 수도