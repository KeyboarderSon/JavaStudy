input.txt를 읽어와서 file이라는 변수가 이를 처리하도록 한다.

콘솔창에서 사용자가 입력하는 것이 아닌 file 내용을 읽어오는 것이므로  ```new Scanner(file)```처럼 파라미터는 file이 되어야 할 것이다.

파일에 대한 예외처리를 해주는 것이 좋다.

```sc.hasNextInt()``` : 다음으로 읽어올 정수가 있는가

```sc.nextInt()``` : 다음 정수를 읽어옴

```java
import java.io.File;
import java.util.Scanner;
import java.io.FileNotFoundException;

public class Main{
    public static void main(String[] args){
        File file = new File("input.txt");
        
        try{
            Scanner sc = new Scanner(file);
            while(sc.hasNextInt()){
                System.out.println(sc.nextInt()*100);

            }
            sc.close();
        }
        catch(FileNotFoundException e){
            /* 오류 발생 시 취할 액션 */
        }
    }
}
```



