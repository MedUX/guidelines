# Coding Design Guidelines

## Fundamentals
* **Clarity at the point of use** is your most important goal. Entities such as methods and properties are declared only once but used repeatedly. Design APIs to make those uses clear and concise. When evaluating a design, reading a declaration is seldom sufficient; always examine a use case to make sure it looks clear in context.
* **Clarity is more important than brevity**. Although code can be compact, it is a non-goal to enable the smallest possible code with the fewest characters.
* **Write a documentation comment** for every declaration. Insights gained by writing documentation can have a profound impact on your design, so don’t put it off.

## Naming

### Promote Clear Usage
* **Include all the words needed to avoid ambiguity** for a person reading code where the name is used.
* **Omit needless words**. Every word in a name should convey salient information at the use site.
* **Name variables, parameters, and associated types according to their roles**, rather than their type constraints.
* **Compensate for weak type information** to clarify a parameter’s role.

### Strive for Fluent Usage
* **Prefer method and function names that make use sites form grammatical English phrases**.
* **Name functions and methods according to their side-effects**:
  * Those without side-effects should read as noun phrases, e.g. `x.distanceTo(y)`, `i.successor()`.
  * Those with side-effects should read as imperative verb phrases, e.g., `print(x)`, `x.sort()`, `x.append(y)`
* **Uses of Boolean methods and properties should read as assertions about the receiver** when the use is nonmutating, e.g. `x.isEmpty`, `line1.intersects(line2)`
* **Interfaces that describe what something is should read as nouns** (e.g. `Collection`).
* The names of other **types, properties, variables, and constants should read as nouns.**

### Use Terminology Well
* **Avoid obscure terms** if a more common word conveys meaning just as well. Don’t say “epidermis” if “skin” will serve your purpose. Terms of art are an essential communication tool, but should only be used to capture crucial meaning that would otherwise be lost.
* **Stick to the established meaning** if you do use a term of art (“a word or phrase that has a precise, specialized meaning within a particular field or profession”). The only reason to use a technical term rather than a more common word is that it _precisely_ expresses something that would otherwise be ambiguous or unclear. Therefore, an API should use the term strictly in accordance with its accepted meaning.
  * **Don’t surprise an expert**: anyone already familiar with the term will be surprised and probably angered if we appear to have invented a new meaning for it.
  * **Don’t confuse a beginner**: anyone trying to learn the term is likely to do a web search and find its traditional meaning.
* **Avoid abbreviations**. Abbreviations, especially non-standard ones, are effectively terms-of-art, because understanding depends on correctly translating them into their non-abbreviated forms.
* **Embrace precedent**. Don’t optimize terms for the total beginner at the expense of conformance to existing culture.
  > It is better to name a contiguous data structure `Array` than to use a simplified term such as `List`, even though a beginner might grasp of the meaning of `List` more easily. Arrays are fundamental in modern computing, so every programmer knows—or will soon learn—what an array is. Use a term that most programmers are familiar with, and their web searches and questions will be rewarded.

## Conventions

Our coding conventions are strongly based on [Hapijs' Coding Conventions](https://github.com/hapijs/contrib/blob/master/Style.md). This helps understanding very quickly the code of others and facilitate working together. Embrace this conventions and propose changes that are helpful for the community.
