# Checking for null

If you are unsure whether something is null, you can
check by using `==`.

```java
void sayHello(String firstName, String lastName) {
    if (lastName == null) {
        IO.println("Hello " + firstName);
    }
    else {
        IO.println("Hello " + firstName + " " + lastName);
    }
}

void main() {
    sayHello("Sonny", "Bono");
    sayHello("Cher", null);
}
```