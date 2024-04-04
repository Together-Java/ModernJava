## Modifiers
### Intro: 

| Modifier | Description |
| --- | --- |
| public | Accessible from any other class |
| private | Accessible only within the class they are declared |
| protected | Accessible within the package and outside the package but through inheritance only |
| static | Belongs to the class rather than the object |
| final | Value can't be changed |
| abstract | Can't be instantiated |
| synchronized | Threads handle the method or block of the method sequentially |
| volatile | Value can be modified by different threads |
| default | No modifier specified, accessible within the same package |

### Explanation

`public`: You can access a variable/function from any package/class doesnt need to extend/impl

`protected`: It extends visibility to subclasses regardless of their package however it should extend/impl the class or it wont work

`default`: Its limited to the same package (you cant access it from sub-packages)

`private` : You can only access it from the same class

`static`: This means when you have an object (an instance of a class) the function/data is for the class not the object meaning if you run it 1000 times it wont change based on what the object gives. Its completely static to the class

`final`: Given to a variable given `API_KEY` wont change thus we will associate it with `final`

`abstract`:  Acts like a blueprint. Its good for making sure subclasses are pretty synchronized in the methods they have. Also you can share functions between subclasses instead of repeating them. `interface` **Acts the same** but it also assumes everything within it is also abstract. 

### Differences between `abstract`  and `interface`

- You can have multiple interfaces but only one abstract method
- Fields inside interfaces are both `static` and `final` So the same values apply to each object
