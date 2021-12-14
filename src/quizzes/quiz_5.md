# Quiz 5: Inheritance 1

### 1. Which is relevant to the concept of inheritance in object-oriented programming?

  * Dynamic Binding
  * Method Overriding
  * Polymorphism
  * All of them

> **Correct answer**: All of them
>
> ---
> 
> **Explanation:**
> 
> - Polymorphism: a child class can "stand in" for its parent class.
> - Method Overriding: child class overrides a method inherited from a parent class
> - Dynamic Binding: more complicated - see the information under the dynamic binding definition in [section 5.3](../5/5.3.md)
> 
> More information can be found in [Section 5.3.](../5/5.3.md)

### 2. In the `Square` vs. `Rectangle` example discussed in class, which statement is correct?

  - `Rectangle` should be a subclass of `Square`
  - There should be no inheritance relationship between `Rectangle` and `Square`
  - `Square` should be a subclass of `Rectangle`
  - Either `Rectangle` or `Square` should be a subclass of the other

  > **Correct answer**: There should be no inheritance relationship between `Rectangle` and `Square`
  >
  > ---
  > 
  > **Explanation:**
  > 
  > In a mathematical sense, every square is a rectangle.
  > 
  > However, if a `Square` were to inherit from a `Rectangle`, it would inherit methods such as `setWidth()` and `setHeight()`. The `Square` could override these functions to provide correct functionality, but publicly exposing such an API defies the fundamental property of a square: a rectangle with equal height and width.
  > 
  > This is fundamentally the same issue as the `Stack<E> extends Vector<E>` problem.
  > 
  > [Further reading (consider the subtype definition)](../5/5.3.md#example-square-vs-rectangle-p-123-125)

### 3. Which of the following views about inheritance is based on the "is-a" relation?

   - Neither type view nor module view
   - Type view
   - Module view
   - Both type and module views

  > **Correct answer**: Type View
  >
  > ---
  > 
  > **Explanation:**
  > 
  > Recall the definition for subtype:
  >
  > > Data type \\(t_2\\) is a subtype of data type \\(t_1\\) if every value of \\(t_2\\) can be assigned to a variable of \\(t_1\\).

### 4. In Java, `Stack` is a subclass of `Vector`. Which of the following statements is *incorrect*?

  - The LIFO property of `Stack` can be violated when the methods inherited from `Vector` are called.
  - `Stack` reflects the module view of inheritance for code reuse.
  - `Stack` reflects the type view of inheritance.
  - `Stack` inherits all the methods of `Vector`.

  > **Correct answer**: `Stack` reflects the type view of inheritance.
  >
  > ---
  > 
  > **Explanation:**
  > 
  > The statement is incorrect because a `Stack` is *not* a `Vector`. The essential quality of a `Stack` is its LIFO property, which is violated by several methods inherited from `Vector`.