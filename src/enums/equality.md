# Equality

You can check if two enums contain the same variant
using the `==` operator.

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