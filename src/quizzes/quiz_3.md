# Quiz 3: Pre/Postcondition Change

### 1. Which condition is weaker than \\(x > 0\\)?

  * \\(2x > 0\\)
  * \\(x \cdot x > 0\\)
  * \\(x + y > 0\\) 
  * \\(x > 1\\) 

> **Correct answer**: \\(x \cdot x > 0\\)
>
> ---
> 
> **Explanation:**
> 
> Recall: \\(P_1 \iff P_2\\) means the conditions are *equivalent*.
> 
> - \\(x > 0 \iff 2x > 0\\), so the conditions are equivalent.
> - \\(x > 0 \implies x \cdot x > 0\\), so \\(x > 0\\) is stronger.
> - \\(x > 0\\) and \\(x + y > 0\\) aren't comparable because \\(y\\) isn't included in the implicant.
> - \\(x > 1 \implies x > 0\\), so \\(x > 1\\) is stronger.
    
### 2. Which statement is correct?

  * \\(\text{length} = \text{count}\\) is stronger than \\(\text{length} = (\text{count}-1)\\)
  * \\(\text{length} = \text{count}\\) is neither stronger nor weaker than \\(\text{length} = (\text{count}-1)\\)
  * \\(\text{length} = \text{count}\\) is weaker than \\(\text{length} = (\text{count}-1)\\)
  * \\(\text{length} = \text{count}\\) is equivalent to \\(\text{length} = (\text{count}-1)\\)

> **Correct answer**: \\(\text{length} = \text{count}\\) is neither stronger nor weaker than \\(\text{length} = (\text{count}-1)\\)
>
> ---
> 
> **Explanation:**
> 
> It doesn't make sense to consider the implication relationship \\[\text{length} = \text{count} \implies 
\text{length} = (\text{count}-1)\\] or vice-versa. Thus, there is no relationship between their contract strengths.


### 3. Which of the following is the most reasonable precondition of the method `deposit(double amount)` in the BankAccount class?

  * \\(\text{amount} \neq 0\\)
  * \\(\text{amount} \geq 0\\)
  * \\(\text{amount}\\) is any `double` value
  * \\(\text{amount} > 0\\)

> **Correct answer**: \\(\text{amount} > 0\\)
>
> ---
> 
> **Explanation:**
> 
> The action of "depositing" at a bank only makes sense when you're depositing a positive amount of money. This rules out all but \\(amount > 0\\).


### 4. In the following code, Module B results in a call of `sqrt(5)`. Which statement is correct?
```java
// Module A
// Precondition: x >= 0
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

   - There is no bug in either A or B
   - There is a bug in both A and B
   - There is a bug in A
   - There is a bug in B

> **Correct answer**: There is a bug in B
>
> ---
> 
> **Explanation:**
> 
> Recall the [Pre/Postcondition Violation Rules.](/4/4.3.md#prepostcondition-violation-rules)
>
> Client B violates Supplier A's precondition, so the client (B) is at fault.
