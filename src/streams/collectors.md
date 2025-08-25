# Collectors

The most common kind of terminal operation you will perform on a stream
is "collecting" elements into a new collection.

For this you use the `.collect` method along with an implemention of the
`Collector` interface.

```java
~void main() {
List<String> roles = List.of("seer", "clown", "nightmare");

Function<String, Integer> countVowels = s -> {
    int vowels = 0;
    for (int i = 0; i < s.length(); i++) {
        char c = s.charAt(i);
        if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') {
            vowels++;
        }
    }
    return vowels;
};

List<Integer> vowelCounts = roles.stream()
    .map(countVowels)
    .collect(Collectors.toList());

IO.println(vowelCounts);
~}
```

There are implementations available as static methods on the `Collectors` class for
collecting into `List`s, `Set`s, and even `Map`s.

Because collecting into specifically a `List` is so common, there is
also a `.toList()` method directly on `Stream` that serves as a shortcut
for `.collect(Collectors.toUnmodifiableList())`.

```java
~void main() {
List<String> roles = List.of("seer", "clown", "nightmare");

Function<String, Integer> countVowels = s -> {
    int vowels = 0;
    for (int i = 0; i < s.length(); i++) {
        char c = s.charAt(i);
        if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') {
            vowels++;
        }
    }
    return vowels;
};

// There is also Collectors.toUnmodifiableList
List<Integer> vowelCountsList = roles.stream()
    .map(countVowels)
    .collect(Collectors.toList());
    
IO.println(vowelCountsList);

vowelCountsList = roles.stream()
    .map(countVowels)
    .toList();
IO.println(vowelCountsList);

// ...and Collectors.toUnmodifiableSet()
Set<Integer> vowelCountsSet = roles.stream()
    .map(countVowels)
    .collect(Collectors.toSet());
IO.println(vowelCountsSet);

// ...and Collectors.toUnmodifiableMap
Map<String, Integer> vowelCountsMap = roles.stream()
    .collect(Collectors.toMap(
        s -> s,
        s -> countVowels.apply(s)
    ));
IO.println(vowelCountsMap);
~}
```