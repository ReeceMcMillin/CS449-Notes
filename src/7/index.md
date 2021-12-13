# Chapter 7 - Refactoring for Design Improvement

> **Refactoring**
>
> ---
>
> *(noun)* A change made to the internal structure of software to make it easier to understand and cheaper to modify without changing its observable behavior.
> 
> *(verb)* To restructure software by applying a series of refactorings without changing its observable behavior.

Observable behavior has different definitions in different contexts. In the context of refactoring, it depends on who is *doing* the observing, which is usually related to code ownership.

It's generally safe to refactor if the refactoring only introduces a *new* public interface. *Changing* a public interface can be done safely if the programmer doing the refactoring also controls all calling code. If the interface has been published for external use, the old interface may need to be deprecated if the refactoring is highly desirable.

An alteration to a public interface without retaining the old one is considered a **revision** as opposed to a refactoring.

Refactoring is not:
  - adding or modifying functionality
  - fixing bugs
  - tuning performance

Automated tests help make refactoring safe and efficient.

## Why Refactor?

- Improve the design of software
  - Design decays by default, you have to work against it.[^entropy]
- Make software easier to understand
  - When you're just trying to get the program to *work*, you're probably not thinking about the future developer (you) who will have to maintain it.
- Help find bugs
  - Part of refactoring is building a deep understanding of the relevant code. Building this understanding can help make intended behavior more clear.
- Help program faster
  - Poor design causes bottlenecks, refactoring helps clear out bad design.


## Footnotes
[^entropy]: [Software Entropy - Wikipedia](https://en.wikipedia.org/wiki/Software_entropy)