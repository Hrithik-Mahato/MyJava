1. Student Record (Basic Constructor & Copy Constructor)
Problem Statement:
Complete the Student class by implementing:
A parameterized constructor to initialize rollNo, name, and marks.
A copy constructor to create a copy of another Student object.
A display() method to print student details.
### Expected Input:
101
Alice
95

### Expected Output:
Roll No: 101
Name: Alice
Marks: 95
```java 
import java.util.*;

class Student {
    int rollNo;
    String name;
    int marks;

    // Implement constructor and copy constructor here

    public void display() {
        System.out.println("Roll No: " + rollNo);
        System.out.println("Name: " + name);
        System.out.println("Marks: " + marks);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        
        int roll = s.nextInt();  // Enter roll number
        s.nextLine();  // Consume newline
        String name = s.nextLine();  // Enter student name
        int marks = s.nextInt();  // Enter marks
        
        Student s1 = new Student(roll, name, marks);
        Student s2 = new Student(s1);  // Copy constructor should copy s1 data
        
        s2.display(); 
    }
}
```
### solutin:
```java
import java.util.*;

class Student {
    int rollNo;
    String name;
    int marks;

    // Implement constructor and copy constructor here
    public Student(int rollNo, String name, int marks)
    {
      this.rollNo=rollNo;
      this.name=name;
      this.marks=marks;
    }
    public Student(Student obj)
    {
      this.rollNo=obj.rollNo;
      this.name=obj.name;
      this.marks=obj.marks;
    }

    public void display() {
        System.out.println("Roll No: " + rollNo);
        System.out.println("Name: " + name);
        System.out.println("Marks: " + marks);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        
        int roll = s.nextInt();  // Enter roll number
        s.nextLine();  // Consume newline
        String name = s.nextLine();  // Enter student name
        int marks = s.nextInt();  // Enter marks
        
        Student s1 = new Student(roll, name, marks);
        Student s2 = new Student(s1);  // Copy constructor should copy s1 data
        
        s2.display(); 
    }
}
```
