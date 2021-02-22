#### 부모 클래스

```java
/* Person class */
public class Person{
    private String name;
    private int age;
    private int height;
    private int weight;

    public void setName(String name){
        this.name = name;
    }

    public String getName(){
        return name;
    }
    public void setAge(int age){
        this.age = age;
    }
    public int getAge(){
        return age;
    }
    
    public void setHeigth(int height){
        this.height = height;
    }
    public int getHeight(){
        return height;
    }

    public void setWeight(int Weight){
        this.weight = weight;
    }

    public int getWeight(){
        return weight;
    }
    
    public Person(String name, int age, int height, int weight){
        super();
        this.name = name;
        this.age = age;
        this.height = height;
        this.weight = weight;
    }

}
```
<BR>

#### 상속받은 자식 클래스
```java
/* Student class */
public class Student extends Person{
    private String studentID;
    private int grade;
    private double GPA;

    public void setStudentID(String studentID){
        this.studentID = studentID;
    }

    public String getStudentID(){
        return studentID;
    }

    public void setGrade(int grade){
        this.grade = grade;
    }

    public String getGrade(){
        return grade;
    }

    public void setGPA(double GPA){
        this.GPA = GPA;
    }

    public double getGPA(){
        return GPA;
    }

    /* 상속받은 부모 클래스의 변수도 다같이 초기화 */
    public Student(String name, int age, int height, int weight, String studentID, int grade, double GPA){

        /* 부모가 가지던 생성자 실행 */
        super(name, age, height, weight);
        this.studentID = studentID;
        this.grade = grade;
        this.GPA = GPA;
    }

    public void show(){
        System.out.println("학생 이름 : " + getName());
        System.out.println("학생 나이 : " + getAge());
        System.out.println("학생 키 : " + getHeight());
        System.out.println("학생 몸무게 : " + getWeight());
        System.out.println("학번 : " + getStudentID());
        System.out.println("학년 : " + getGrade());
        System.out.println("학점 : " + getGPA());


    }

}

```

<br>
####Main
```java
/* Main class */
public class Main{
    public static void main(String[] args){
        Scaner scan = new Scanner(System.in);
        System.out.print("총 학생 수 : ");
        int number = scan.nextInt();

        Student[] students = new Student[number];

        for(int i = 0; i < number; i++){
            String name, studentID;
            int age, height, weight, grade;
            double GPA;

            System.out.print("학생 이름 : ");
            name = scan.next();
            System.out.print("학생 나이 : ");
            age = scan.nextInt();
            System.out.print("학생 키 : ");
            height = scan.nextInt();
            System.out.print("학생 몸무게 : ");
            weight = scan.nextInt();
            System.out.print("학생 학번 : ");
            studentID = scan.next();
            System.out.print("학생 학년 : ");
            grade = scan.nextInt();
            System.out.print("학생 학점 : ");
            GPA = scan.nextDouble();
            

            Student[i] = new Student(name, age, height, weight, studentID, grade, GPA);
             
        }

}
```