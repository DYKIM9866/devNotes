# Dependency Injection(의존성 주입)
## 의존관계
"A클래스는 B클래스에 의존한다" 라는 말은 B클래스가 변하면 A클래스에 영향을 미친다는 뜻이다.

## 의존성 주입
보통 A클래스에 명시적으로 B클래스에 의존하는 부분이 있다 
```java
class car{
    private Sonata sonata;
    public car(){
        sonata = new Sonata;
    }
}
```
인터페이스를 추상화 하게 되어도
```java
class car{
    private Hyundai hyundai;
    public car(){
        hyundai = new Sonata;
        //hyundai = new Santafe;
        //hyundai = avante;
    }
}
```
다양한 차량을 의존 받을 수 있다.<br>
이것을 외부에서 정해주면 어떻게 될까? 지금까지 내가 차를 골라서 탔다면 이제는 와이프가 정해주는 것이다. (사람 입장에서야 내 선택권이 없어지는 것이 안좋아 지는 것이지만...) 이제는 내가 번거롭게 차를 고를필요가 없다 왜냐하면 외부(와이프)가 정해주니까!

이처럼 외부에서 의존관계를 외부에서 결정하고 주입하는 것이 DI이다.<br>
스프링의 바이블 토비의 스프링에서는 다음과 같이 정의하고 있다.
* 클래스모델이나 코드에는 런타임 시점의 의존관계가 드러나지 않는다. 그러기 위해서는 인터페이스만 의존하고 있어야 한다.
* 런타임 시점의 의존관계는 컨테이너나 팩토리 같은 제 3의 존재가 결정한다.
* 의존관계는 사용할 오브젝트에 대한 레퍼런스를 외부에서 제공해줌으로서 만들어진다.

## DI 구현
* 생성자를 이용
```java
class Car{
    private Hyundai hyundai;
    public Car(Hyundai hyundai){
        this.hyundai = hyundai;
    }
}
```
* setter 메서드를 이용
```java
class Car{
    private Hyundai hyundai;
    public void setCar(Hyundai hyundai){
        this.hyundai = hyundai;
    }
}
```

## DI의 장점
DI로 구현하면 어떤점이 좋을까?
1. 의존성이 줄어든다.
2. 재사용성이 높은 코드가 된다.
3. 테스트하기 좋은 코드가 된다.
4. 가독성이 좋아진다.

## 정리
DI는 객체가 의존하는 또 다른 객체를 외부에서 선언하고 이를 주입받아 사용하는 것이다.