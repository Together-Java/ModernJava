# Type Variables

After the name of a class in the class definition you can put one or more "type variables."
These look like `<` followed by a comma separated list of "type names" and ended by a `>`.

```java,no_run
class Box<T> {

}
```

Inside a class definition you can use these type variables on fields, method arguments,
and method return types.

```java,no_run
class Box<T> {
    T data;

    void setData(T newData) {
        this.data = newData;
    }
}
```

This indicates that you would be okay with any type being used in place of the type variable (in the above code `T`).
