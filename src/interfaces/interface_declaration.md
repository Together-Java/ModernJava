# Interface Declaration

To declare an interface you write the word `interface` followed by the name of the interface
and `{}`.

```java
interface Dog {}
```

Inside of the `{}` you can write the signatures for methods followed by a `;`. That means 
no method body and no `public` or `private` modifiers.

```java,no_run
interface Dog {
    void bark();

    String fetch(String ball);
}
```
