# void

All methods have to declare some return type. `void` is what you write when a method won't return any value.

```java
// Returns a String
String title() {
    return "All Night";
}

// Returns an int
int views() {
    return 4071;
}

// Doesn't return any value.
void talkAboutVideo() {
    IO.println(title() + " only has " + views() + " views.");
}

// This is what the void in "void main()" means
void main() {
    talkAboutVideo();
}
```