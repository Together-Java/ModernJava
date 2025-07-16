# Switch

```java
enum StopLight {
    RED,
    YELLOW,
    GREEN
}

void main() {
    StopLight light = StopLight.RED;
    
    if (light == StopLight.RED) {
        IO.println("You must stop");
    }
    else {
        IO.println("Full speed ahead!");
    }
}
```