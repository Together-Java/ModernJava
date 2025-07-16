# Declaration

To declare an annotation you use `@interface` followed by a type name.

```java,no_run
@interface NonNegative {
}
```

We call these "annotation interfaces."[^shared] 

[^shared]: They share some properties with regular interfaces but it's best to think of them as their own thing.