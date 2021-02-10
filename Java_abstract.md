**abstract와 interface 같이 보기**

추상클래스를 이용하여 미리 설계해놓은 play, pause, stop을 반드시 구현해야만 하는 요소라고 알려줌

```java
abstract class Animal{
    abstract void crying();

}
```
```java
public class Dog extends Animal{
    void crying() { 
        System.out.println("월! 월!");

    }
}
```
```java
public class Cat extends Animal{
    void crying{
        system.out.println("야옹~");
    }
}
```
```java
public class Main{
    public static void main(Sturing[] args){
        Dog dog = new Dog();
        Cat cat = new Cat();
        dog.crying();
        cat.crying();

    }
}
```