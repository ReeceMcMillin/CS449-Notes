# Quiz Questions

# Quiz 3
1. Which condition is weaker than \\(x > 0\\)?
    * \\(x \cdot x > 0\\)
    * Because \\(x > 0 \implies x \cdot x > 0\\)
2. Which statement is correct?
    * \\(length = count\\) is neither stronger nor weaker than \\(length = (count-1)\\)
3. Which of the following is the most reasonable precondition of the method `deposit (double amount)` in the BankAccount class?
    * \\(\text{amount} > 0\\)
4. In the following code, Module B results in a call of `sqrt(5)`. Which statement is correct?
```java
// Module A
// Precondition: $x >= 0$
// Postcondition: return x's square root

double sqrt(double x) {
    ...
}
```

```java
// Module B

double x = -5;
double y = sqrt(x);

assert abs(y * y-x) < eps
```
- There is a bug in Module B

# Quiz 4

# Quiz 5
1. Which is relevant to the concept of inheritance in object-oriented programming?
    * Dynamic binding, method overriding, polymorphism