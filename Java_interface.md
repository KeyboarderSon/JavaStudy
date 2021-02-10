인터페이스는 다중 상속을 구현하게 해주는 고급 기술이다. 

추상클래스는 추상 메소드 외에 멤버 변수나 일반 메소드를 가질 수 있지만
인터페이스에서는 반드시 사전에 정의된 추상 메소드와 상수만을 가질 수 있다  .

추상클래스에서 public으로 메소드가 정의되었다면 함수 구현을 해줘야 한다.

```java
/* Dog class */
public interface Dog{
    abstract crying();
    public void show();
    /*
    {
        Dog class가 abstract class로 선언되었다면 아래 메소드 내용을 적는 것이 가능하지만,
        interface에서는 절대 불가하다. 
    }
    */
    public void one();

}
```
```java
/* Cat class */
public interface Cat{
    abstract void crying();
    public void two();
}
```


```java
/* Main class */

/* 
abstract class 사용 시,
public class Main extends Dog{ ~ }
*/
public class Main implements Dog, Cat{
    public static void main(String[] args){
        Main main = new Main();
        main.crying();
        main.show();
        main.one();
        main.two();
    }

    @Override
    public void crying(){
        System.out.println("월월!");
    }

    @Override
    public void show(){
        System.out.println("hello");
    }

    @Override
    public void one(){
        System.out.println("one!");
    }

    @Override
    public void two(){
        System.out.println("two!");
    }
}
