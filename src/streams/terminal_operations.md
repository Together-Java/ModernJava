# Terminal Operations

We call `.map`, `.filter`, and methods like them "intermediate operations."
This is because they run "in the middle" of the entire process.

For consuming a stream you use "terminal operations." Terminal operations
"consume" the stream and produce some result.

The simplest terminal operation is `.forEach`. It consumes the entire stream and does
something for each element in the flow.

```java
~void main() {
List<String> cities = List.of(
    "St. Louis", "Dallas", "London", "Tokyo"
);

cities.stream()
    .filter(city -> !city.startsWith("S"))
    .forEach(IO::println); // Dallas, London, Tokyo
~}
```

Once a terminal operation has been performed the stream is no longer
usable.

```java,panics
~void main() {
List<String> cities = List.of(
    "St. Louis", "Dallas", "London", "Tokyo"
);

Stream<String> citiesStream = cities.stream()
    .filter(city -> !city.startsWith("S"));

// Dallas, London, Tokyo
citiesStream.forEach(IO::println);

// java.lang.IllegalStateException: stream has already been operated upon or closed
citiesStream.forEach(IO::println);
~}
```