# Transporting Data

If you ask someone multiple questions you likely will get multiple variables
worth of information.

```java,no_run
~import java.util.Scanner;
~
~Scanner scanner = new Scanner(System.in);
~
~String input(String message) {
~    System.out.print(message);
~    return scanner.nextLine();
~}
~
void main() {
    String firstName = input("What is your first name? ");
    String lastName = input("What is your last name? ");

    System.out.println("Hello " + firstName + " " + lastName + ".");
}
```

This is fine and dandy so long as you immediately use those variables. But once you add in
reprompting logic code can get pretty lengthy.

```java,no_run
~import java.util.Scanner;
~
~Scanner scanner = new Scanner(System.in);
~
~String input(String message) {
~    System.out.print(message);
~    return scanner.nextLine();
~}
~
void main() {
    String firstName;
    do {
        firstName = input("What is your first name? ");

        if (firstName.isBlank()) {
            System.out.println("First name cannot be blank.");
        }
        else {
            break;
        }
    } while (true);

    String lastName;
    do {
        lastName = input("What is your first name? ");

        if (lastName.isBlank()) {
            System.out.println("First name cannot be blank.");
        }
        else {
            break;
        }
    } while (true);

    System.out.println("Hello " + firstName + " " + lastName + ".");
}
```

And once code gets lengthy it is sometimes useful to separate it into smaller functions.

I mention all this as a reminder that when you want to return multiple values from a function
you can use a class.[^dto]

```java,no_run
~import java.util.Scanner;
~
~Scanner scanner = new Scanner(System.in);
~
~String input(String message) {
~    System.out.print(message);
~    return scanner.nextLine();
~}
~
class Person {
    String firstName;
    String lastName;

    Person(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }
}

Person askForName() {
    String firstName;
    do {
        firstName = input("What is your first name? ");
        
        if (firstName.isBlank()) {
            System.out.println("First name cannot be blank.");
        }
        else {
            break;
        }
    } while (true);

    String lastName;
    do {
        lastName = input("What is your first name? ");

        if (lastName.isBlank()) {
            System.out.println("First name cannot be blank.");
        }
        else {
            break;
        }
    } while (true);
    
    return new Person(firstName, lastName);
}

void main() {
    Person person = askForName();

    System.out.println("Hello " + person.firstName + " " + person.lastName + ".");
}
```



[^dto]: When you make a class just to make objects which transfer data between different parts of your program we
call those DTOs - data transfer objects. You will learn better ways to make DTOs in the future.