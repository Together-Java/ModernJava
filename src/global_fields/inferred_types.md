# Inferred Types

Just like other field declarations, `var` cannot be used 
for inferring the type of a global field. You need to explicitly write out the type.

```java,does_not_compile
var x = 5;

void main() {
    System.out.println(x);
}
```