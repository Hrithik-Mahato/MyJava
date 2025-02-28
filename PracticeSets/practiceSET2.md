2. Car Details (Shallow Copy Issue)
Problem Statement:
Fill in the missing parts of the Car class.
Create a constructor that initializes model, year, and features (an array of car features).
Implement a copy constructor, but use a shallow copy (just assign the features array directly).
Implement display() to print car details.
The modify() method should update features[0] to "Modified Feature", affecting both objects due to shallow copying.

Expected Input:
Tesla Model X
2023

Expected Output (Shallow Copy Effect):
Model: Tesla Model X
Year: 2023
Features: Modified Feature, Feature2, Feature3,

```java 
import java.util.*;

class Car {
    String model;
    int year;
    String[] features;

    // Implement constructor and copy constructor here

    public void modify() {
        features[0] = "Modified Feature";
    }

    public void display() {
        System.out.println("Model: " + model);
        System.out.println("Year: " + year);
        System.out.print("Features: ");
        for (String f : features) {
            System.out.print(f + ", ");
        }
        System.out.println();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        String model = s.nextLine();  // Enter car model
        int year = s.nextInt();  // Enter car year
        s.nextLine();  // Consume newline
        String[] features = {"Feature1", "Feature2", "Feature3"};

        Car c1 = new Car(model, year, features);
        Car c2 = new Car(c1);  // Copy constructor should copy data
        
        c1.modify();  // This modifies the first feature
        c2.display(); 
    }
}
```
### solution:
```java
import java.util.*;

class Car {
    String model;
    int year;
    String[] features;

    // Implement constructor and copy constructor here
    public Car(String model, int year, String[] features)
    { this.model=model;
      this.year=year;
      this.features=features;
    }
    public Car(Car obj)
    {
      this.model=obj.model;
      this.year=obj.year;
      this.features=obj.features;
    }

    public void modify() {
        features[0] = "Modified Feature";
    }

    public void display() {
        System.out.println("Model: " + model);
        System.out.println("Year: " + year);
        System.out.print("Features: ");
        for (String f : features) {
            System.out.print(f + ", ");
        }
        System.out.println();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        String model = s.nextLine();  // Enter car model
        int year = s.nextInt();  // Enter car year
        //s.nextLine();  // Consume newline
        String[] features = {"Feature1", "Feature2", "Feature3"};

        Car c1 = new Car(model, year, features);
        Car c2 = new Car(c1);  // Copy constructor should copy data
        
        c1.modify();  // This modifies the first feature
        c2.display(); 
    }
}
```
