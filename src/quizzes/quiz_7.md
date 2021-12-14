# Quiz 7: Design Heuristics/SOLID

### 1. Which of the following statements about information hiding is *incorrect*?

  - Information hiding suggests that instance variables should be made public
  - Information hiding suggests only revealing the information necessary for the use of the class
  - Information hiding suggests that a class should not expose implementation details in public
  - Information hiding suggests minimizing the visibility of class members

> **Correct answer**: Information hiding suggests that instance variables should be made public.
>
> ---
>
> **Explanation:**
>
> The statement is incorrect because information hiding suggests that instance variables should be made *private*.

### 2. Which statement about the Command (mutator)-Query(accessor) Separation principle is correct?

  - No method in a class should change object states
  - Only mutators are expected to change object states
  - Both accessors and mutators may change object states
  - Only accessors are expected to change object states

> **Correct answer**: Only mutators are expected to change object states.
>
> ---
>
> **Explanation:**
>
> If this isn't self-explanatory, review [section 5.4.](../5/5.4.md#accessors-and-mutators)

### 3. Which of the following statements about the Single Responsibility Principle is correct?

  - A class should have only one reason to change
  - Single responsibility is the same as high cohesion
  - A class should do one thing
  - A class should have only one public method

> **Correct answer**:  A class should have only one reason to change.
>
> ---
>
> **Explanation:**
>
> This is the definition of the [Single Responsibility Principle](/5/5.5.md#single-responsibility-principle)