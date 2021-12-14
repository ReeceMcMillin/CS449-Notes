# Quiz 6: Inheritance 2

### 1. It is usually considered a bad design to make `KansasCity` a subclass of `City` because:

   - It violates the rule of polymorphism
   - The classification for use of inheritance is premature as `KansasCity` is an *instance* of `City`
   - It violates the Law of Demeter
   - It violates the rule of change

> **Correct answer**: The classification for use of inheritance is premature as `KansasCity` is an *instance* of `City`
>
> ---
>
> **Explanation:**
>
> Inheritance shouldn't be used when a simple instance would suffice.

### 2. Defining `CarOwner` as a subclass of `Car` violates the:

  - change rule of inheritance
  - rule of reuse
  - polymorphism rule of inheritance
  - rule of modularity

> **Correct answer**: polymorphism rule of inheritance
>
> ---
>
> **Explanation:**
>
> A car owner is not themselves a car.

### 3. Given the following code in Java, which statement about methods `getAnimalForAdoption` and `putAnimal` in class `CatShelter` is correct?

```java
//Cat extends Animal

class AnimalShelter {
    Animal getAnimalForAdoption() {}
    void putAnimal(Animal animal) {}
}

class CatShelter extends AnimalShelter {
    Cat getAnimalForAdoption() {}
    void putAnimal(Object animal) {}
}
```

  - Neither of them is an overriding method
  - Both are overriding methods
  - Neither of them is an overloading method
  - `getAnimalForAdoption()` is an overriding method while `putAnimal()` is an overloading method

> **Correct answer**: `getAnimalForAdoption()` is an overriding method while `putAnimal()` is an overloading method
>
> ---
>
> **Explanation:**
>
> With `getAnimalForAdoption()`, `CatShelter` promises to return a more *specific* type of `Animal`. This follows a *covariance* relationship.
> 
> With `putAnimal()`, `CatShelter` agrees to allow a more *general* argument that may or may not be an `Animal`. This follows a *contravariance* relationship.
> 
> Note: some languages (including Java/C++) do not allow or put heavy restrictions on use of contravariance.[^dzone]

### 4. Subcontracting refers to:

  - inheritance with overriding and dynamic binding, where the overriding rule is followed
  - instance variables of a class are the subcontractors of the class
  - the module view of inheritance
  - a class delegates its task to its clients

> **Correct answer**: inheritance with overriding and dynamic binding, where the overriding rule is followed.
>
> ---
>
> **Explanation:**
>
> Subcontracting is a form of design by contract that makes certain guarantees about the pre/postcondition behavior of class descendants.
> 
> Recall the Subcontracting Rule of Inheritance listed in [section 5.3.](../5/5.3.md#prepostcondition-of-method-overriding)

## Footnotes

[^dzone]: [Covariance and Contravariance In Java | Edwin Dalorzo](https://dzone.com/articles/covariance-and-contravariance)