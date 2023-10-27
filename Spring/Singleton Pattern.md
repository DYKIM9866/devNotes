# Singleton Pattern(싱글턴 패턴)
객체의 인스턴스가 단 하나만 생성되는 것을 의미한다.

## 싱글턴패턴 사용하는 이유
객체를 생성할 때 메모리가 할당된다 같은 용도의 사용을 위해 계속해서 새로운 객체를 생성하게 되면 메모리 낭비가 발생하게 된는데 이를 방지하기 위해 사용한다.<br>
예로는 데이터베이스에서 커넥션 풀,캐시,로그 등이 있다.

## 싱글턴패턴 문제점
* 상속이 불가능하다, 자신만이 객체를 생성할 수 있도록 생성자가 private으로 제한되기 때문 
* 테스트가 어렵다,
* 멀티스레드 환경에서 싱글톤이라고 해서 인스턴스가 한개만 생성된다는 보장이 없다.
* 전역으로 자원을 공유하기 때문에 바람직하지 못하다.

## 자바 싱클톤과 스프링 싱글톤의 차이
```java
public class Car{
    private static Car instance;
    
    private Car(){
         throw new IllegalStateException("Private Constructor");
    }

    public static Car getInstance(){
        if(instance == null){
            instance = new Car();
        }
        return instance;
    }
}
```
```java
public class Car{

}
```
위의 두 코드는 차례로 자바와 스프링으로 각각 싱글턴 클래스를 작성한 것이다.<br>
자바같은 경우 직접 instance를 static으로 생성해주고 생성자 또한 private으로 작성한다.<br>
스프링은 생성되는 빈을 직접 싱글톤으로 관리할 수 있고 위의 자바와는 다르게 불필요한 코드들은 모두 삭제 되었다. 이로인해 스프링은 자바에서 가지고 있던 문제점들을 보다 좋게 바꾸어준다. 
* 상속이 가능하다.
* 테스트가 편해졌다
* 한개의 인스턴스를 보장받는다.
* 객체지향적으로 개발 가능하다.
스프링은 직접 싱글톤 형태의 오브젝트를 만들고 관리하는 기능을 제공하는데, 싱글톤 레지스트리이다. 이를 통해 static메서드나 private 생성자등을 사용하지 않게 해준다.