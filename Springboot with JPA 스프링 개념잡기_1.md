## Springboot with JPA 스프링 개념잡기 



1. ##### 스프링이란?

   * 스프링은 프레임워크이다.

     	-  틀안에서 동작하다. 
     	-  틀 안에서 벗어나지 말라는 것 
     	-  틀에 맞춰서 개발을 해라 

     

   * 스프링은 오픈소스이다 

     	-  오픈소스라는 의미는 내부를 뜯어 고칠 수 있다는 말

     

   * 스프링은 IOC 컨테이너를 가진다

      - IOC(Inversion of Controll : 제어의 역전) 

      - class - 설계도 , object - 실체화가 가능한 것

      - class, abstract class  -  차이점은 실체화가 되야한다는 것 

      - Instance - 실체화가 된것을 의미한다.  

      - 오브젝트 - new를 해서 - heap 이라는 메모리 공간에 올린다.

      - EX) chair ch = new chair(); 

      - chair 는 heap 메모리에 new 하는 순간 올라가고 주소가 'ch' 라는 것이다.

        ```java
        // 해당 'ch'는 같은 Chair를 가리키는 것인가요 ?
        public void maker(){
            Chair ch = new Chair();
         }
        public void user(){
            Chair ch = new Chair();
        }
        ```

     - 정답은 '아니다' 이다.  참조 주소 (레퍼런스 주소 ) ch는 각각의 메서드가 관리한다. 

     - 따라서 새로운 Chair를 하나 더 만든 것이 되어 두 의자는 다른 의자이다.

     - maker 메서드에서 가리키는 Chair를 user에서도 사용하고 싶은데 그것이 안되는거다.

       

   * 스프링은 DI를 지원한다

     - DI(Dependency Injection : 의존성 주입) :  필요한 곳에 가져다가 쓰는 것 

     - 내가 만든 Object들을 스프링이 스캔을 한다 

     - 그럼 내가 관리하는 Object가 아닌 스프링이 관리하는 Object들이 된다. 

     - 특정 메소드에서 사용되는 Object를 공유할 수 있게 된다 

     - 이것을 싱글톤 패턴이라고 한다. 

     - 프로그램을 짜는데 편하게 만들어 주기 위함이라는 것 

       

   * 스프링은 엄청나게 많은 필터를 가지고 있다.

     - 필터란 문지기 같은 개념 
     - 톰캣이 가지는 필터는 filter라 불리며 관리하는 파일은 web.xml
     - 스프링 컨테이너가 가지는 필터는 intersepter라 불림 
     - 권한을 체크

     

   * 스프링은 엄청나게 많은 어노테이션을 가지고 있다.

     - 어노테이션 은 주석
     - 주석은 컴파일러가 무시하는게 무시하는 것이 주석
     - 그러나 어노테이션은 컴파일러가 체크할 수 있게 힌트를 주는 주석 
     - 컴파일러가 무시하지 않는다. 
     - 자식 클래스에 해당 override 어노테이션이 있으면  부모 클래스에서 확인한다 
     - 어노테이션은 객체를 생성하기 때문에 해당 어노테이션의 사용법을 약속한다 
     - 어노테이션은 주석 + 힌트이다 
- 리플렉션(분석하는 기법 - > 런타임 때 분석한다.)
     

   

   

   * 스프링은 MessageConverter를 가지고 있다. 기본값은 JSON 이다.

      -  중간데이터 :  JSON 
   
      -  파이썬이든 자바든 모든 랭귀지가 이해할 수 있는  JSON 데이터 
   
      - MessageConverter : 자바 오브젝트를  JSON데이터로 컨버팅 해주는 것
   
      -  상대방한테 응답받을 때도 메세지 컨버터가 JSON 데이터를 자바 오브젝트로 컨버팅 해줌 
   
        
   
   * 스프링은 BufferReader와 BufferedWriter를 쉽게 사용할 수 있다. 
   
      - 가변 길이의 문자를 받을 수 있다. 
      - 요청 시에 데이터를 담아서 요청할 수 가 있다 .
      - request .getReader 를 사용한다.
      - PrintWriter = BufferdWriter  => Println();
      - 
   
   * 스프링은 계속 발전중이다. 
   
   