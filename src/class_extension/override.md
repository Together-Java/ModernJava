# Override

Just as you can provide an alternative implementation for a default method
in an interface, you can override a method inherited from a superclass.

```java
class BodyOfWater {
    long depth;

    BodyOfWater(long depth) {
        if (this.depth < 0) {
            throw new IllegalArgumentException();
        }
        this.depth = depth;
    }

    void swim() {
        if (depth > 50) {
            IO.println("You have drowned");
        }
        else {
            IO.println("You are fine");
        }
    }
}

class Ocean extends BodyOfWater {
    String name;

    Ocean(String name, long depth) {
        this.name = name;
        super(depth);
    }

    @Override
    void swim() {
        IO.println("You have been eaten by a shark");
    }
}

void main() {
    BodyOfWater pacific = new Ocean("Pacific", 36201L);
    pacific.swim();
}
```

This can be prevented by marking a method as `final`. This explicitly disallows
overriding it in a subclass.

```java,does_not_compile
class BodyOfWater {
    long depth;

    BodyOfWater(long depth) {
        if (this.depth < 0) {
            throw new IllegalArgumentException();
        }
        this.depth = depth;
    }

    // Cannot be overriden
    final void swim() {
        if (depth > 50) {
            IO.println("You have drowned");
        }
        else {
            IO.println("You are fine");
        }
    }
}

class Ocean extends BodyOfWater {
    String name;

    Ocean(String name, long depth) {
        this.name = name;
        super(depth);
    }

    @Override
    void swim() { // We cannot override a final method
        IO.println("You have been eaten by a shark");
    }
}

void main() {
    BodyOfWater pacific = new Ocean("Pacific", 36201L);
    pacific.swim();
}
```

Another way to prevent this is to make it so the method is not visible to the subclass.
This can be done either by marking the method `private` or by having it be package-private
and simply in a different package.

```java,does_not_compile
class BodyOfWater {
    long depth;

    BodyOfWater(long depth) {
        if (this.depth < 0) {
            throw new IllegalArgumentException();
        }
        this.depth = depth;
    }

    // Cannot be override what you cannot see
    private void swim() {
        if (depth > 50) {
            IO.println("You have drowned");
        }
        else {
            IO.println("You are fine");
        }
    }
}

class Ocean extends BodyOfWater {
    String name;

    Ocean(String name, long depth) {
        this.name = name;
        super(depth);
    }

    @Override
    void swim() { // Cannot be override what you cannot see
        IO.println("You have been eaten by a shark");
    }
}

void main() {
    BodyOfWater pacific = new Ocean("Pacific", 36201L);
    pacific.swim();
}
```

If you want to use the definition of the method you are overriding you can access it by writing `super.`
before the name of the method.

```java
class BodyOfWater {
    long depth;

    BodyOfWater(long depth) {
        if (this.depth < 0) {
            throw new IllegalArgumentException();
        }
        this.depth = depth;
    }

    void swim() {
        if (depth > 50) {
            IO.println("You have drowned");
        }
        else {
            IO.println("You are fine");
        }
    }
}

class Ocean extends BodyOfWater {
    String name;

    Ocean(String name, long depth) {
        this.name = name;
        super(depth);
    }

    @Override
    void swim() {
        if ("Pacific".equals(name)) {
            IO.println("You have been eaten by a shark");
        }
        else {
            // Calls the definition on BodyOfWater
            super.swim();
        }
    }
}

void main() {
    BodyOfWater pacific = new Ocean("Pacific", 36201L);
    pacific.swim();
    BodyOfWater atlantic = new Ocean("Atlantic", 28232L);
    atlantic.swim();
}
```