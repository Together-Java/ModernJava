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
        System.out.println("You must stop");
    }
    else {
        System.out.println("Full speed ahead!");
    }
}
```