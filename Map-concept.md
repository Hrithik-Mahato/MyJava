## this code show how map word 
```java
import java.util.*; // `import` and `java.util` are predefined

public class Main { // `public`, `class` are predefined
    public static void main(String[] args) { // `public`, `static`, `void` are predefined
        // Creating a phone book (Map)
        Map<String, String> phoneBook = new HashMap<>(); // `Map`, `HashMap`, `String` are predefined

        // Adding contacts
        phoneBook.put("Alice", "123-456-7890"); // `put` is a method of `Map`
        phoneBook.put("Bob", "987-654-3210");
        phoneBook.put("Charlie", "555-666-7777");

        // Retrieving a phone number
        System.out.println("Bob's number: " + phoneBook.get("Bob")); // `get` is a method of `Map`

        // Checking if a contact exists
        if (phoneBook.containsKey("Alice")) { // `if` is predefined, `containsKey` is a method of `Map`
            System.out.println("Alice is in the phone book.");
        }

        // Removing a contact
        phoneBook.remove("Charlie"); // `remove` is a method of `Map`

        // Printing all contacts
        System.out.println("Phone Book: " + phoneBook); // `System.out.println` is predefined
    }
}
```
