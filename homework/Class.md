- **클래스와 객체 그리고 인스턴스**
    
    # 클래스
    
    프로그램에 사용될 객체의 틀,객체 생성을 위한 설계도 역할
    
    여러가지 멤버 변수와 메서드를 포함
    
    비슷한 것들끼리 모아놓은 것
    
    - 코드
        
        class 클래스 명()
        
    - 규칙
        
        하나 이상의 문자로 이루어져야 한다
        
        첫 번째 글자는 숫자가 올 수 없다
        
        $,_ 외에는 특수 문자 사용 불가능
        
        자바 키워드는 사용불가능 ex)class,system,for,while
        
    
    | 멤버 변수 | 클래스 내에서 사용되는 변수. 클래스의 속성을 나타냄. 인스턴스 변수(instance variable)라고 함. |
    | --- | --- |
    | 메서드 | 클래스 내에서 사용되는 함수. 클래스의 동작을 나타냄. 인스턴스 메서드(instance method)라고 함 |
    | 생성자 | 클래스로부터 객체를 생성할 때 호출되는 특별한 메서드. 객체의 초기화를 수행 |
    | 필드(Field) | 객체의 데이터가 저장되는 곳 |
    
    ---
    
    # 객체(object)
    
    정의:**클래스의 인스턴스나 배열**
    
    ## 생성방법
    
    클래스 선언→new 연산자 사용 ex)new 클래스()
    
    객체란 눈에 보이지는 않지만 실제로 존재하는것 이것은 실체화 한것을 인스턴스
    
    ---
    
    ## 인스턴스(instance**)**
    
    객체를 실체화 하기 위해 만들것을 인스턴스화