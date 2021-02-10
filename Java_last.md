```java
/* Hero class */
public class Hero {
    String name;

    public Hero(String name){
        this.name = name;
    }

    public void attack(){
        System.out.println("주먹 지르기!");
    }   
}
```


if (heros[i] intanceof Warrior)
: 현재 접근하고 있는 캐릭터가 Warrior의 instance라면
```java
/* Warrior class */
public class Warrior extends Hero{
    public Warrior(String name){
        /* 부모클래스의 생성자 */
        super(name);
    }

    public void groundCutting(){
        System.out.println("대지 가르기!");
    }
}
```
```java
/* Archer class */
public class Archer extends Hero{
    public Archer(String name){
        super(name);
    }
    public void fireArrow(){
        System.out.println("불화살!");
    }
}
```

```java
/* Wizard class */
public class Wizard extends Hero{
    public Wizard(String name){
        super(name);
    }

    public void freezing(){
        System.out.println("얼리기!");
    }
}
```

```java
/* Main class */
public class Main{
    public static void main(String[] args){
        Hero[] heros = new Hero[3];
        heros[0] = new Warrior("전사");
        heros[1] = new Archer("궁수");
        heros[2] = new Wizard("마법사");

        for(int i = 0; i< heros.length; i++){
            heros[i].attack();

            if(heros[i] intanceof Warrior){
                Warrior temp = (Warrior) heros[i];
                temp.groundCutting();
            }
            else if(heros[i] instanceof Archer){
                Archer temp = (Archer)heros[i];
                temp.fireArrow();
            }
            else if(heros[i] instanceof Wizard){
                Wizard temp = (Wizard) heros[i];
                temp.freezing();
            }
        }
    }
}
```

#### output
주먹 지르기!
대지 가르기!
주먹 지르기!
불화살!
주먹 지르기!
얼리기!
