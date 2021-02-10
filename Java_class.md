this.x
: 자신이 갖는 고유한 x
set 함수에서는 매개변수명과 private의 변수명이 겹쳐서 this를 사용해 구분한다.

```java
/* node class */

public class Node{
    private int x;
    private int y;


    public int getX(){
        return x;
    }
    public void setX(int x){
        this.x = x;
    }
    public int getY(){
        return y;
    }
    public void setY(int y){
        this.y = y;
    }

    /* 생성자 */
    public Node(int x, int y){
        this.x = x;
        this.y = y;
    }

    /* 정중앙을 갖는 node 반환 */
    public Node getCenter(Node other) {
        return new Node(this.x + other.getX()) / 2, (this.y + other.getY()) / 2);
    }

}
```

```java
/* Main class */

public class Main{
    public static void main(String[] args){
        Node one = new Node(10, 20);
        Node two = new Node(30, 40);
        
        /* one과 two의 정중앙 */
        Node result = one.getCenter(two);

        System.out.println(result.getX() + ", " + result.getY());
    }
}