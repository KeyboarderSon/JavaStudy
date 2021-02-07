배열
```int[] arr = new int[100];```


아래와 같이도 가능하다.

    int num = 5;
    int[] arr = new int[num];




<br>Math.random() : 0보다 크거나 같고 1보다 작은 수 생성
아래 코드는 0이상 100 미만의 랜덤한 수가 요소가 됨

 ```java
int num = 100;
int[] arr = new int[num];
for(int i = 0; i < num; i++){
    arr[i]=(int)(Math.random() * 100);
}
```

