Introduction to Map in Java (Made Simple)

A Map in Java is a collection that stores key-value pairs. Unlike List or Set, which store individual elements, a Map lets you look up a value using a unique key.

Think of it as a dictionary:

The word (key) helps you find the meaning (value).

Each word is unique, but meanings can be the same.

Instead of searching through a list, you can instantly get a meaning by looking up the word.



---

Easy Analogy: Map as a Contact List (Phone Book)

Imagine your phone contacts:

Each name (key) is mapped to a phone number (value).

Names must be unique, but phone numbers can be the same.

Instead of checking each contact manually, you can directly find the number by searching the name.

Now, let's see this in Java:

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Creating a phone book (Map)
        Map<String, String> phoneBook = new HashMap<>();

        // Adding contacts
        phoneBook.put("Alice", "123-456-7890");
        phoneBook.put("Bob", "987-654-3210");
        phoneBook.put("Charlie", "555-666-7777");

        // Retrieving a phone number
        System.out.println("Bob's number: " + phoneBook.get("Bob"));

        // Checking if a contact exists
        if (phoneBook.containsKey("Alice")) {
            System.out.println("Alice is in the phone book.");
        }

        // Removing a contact
        phoneBook.remove("Charlie");

        // Printing all contacts
        System.out.println("Phone Book: " + phoneBook);
    }
}
```

---

Key Concepts in Map and Different Types of Maps 
![add image](https://github.com/Hrithik-Mahato/MyJava/blob/main/IMG_20250307_181733.jpg)


Summary

A Map is like a phone book: you use a unique key (name) to get a value (number).

HashMap is the most common implementation (fast but unordered).

You can add, update, remove, and retrieve key-value pairs efficiently.


Would you like an example of iterating through a Map to print all keys and values?

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
