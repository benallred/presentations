# Transformation Priority Premise

## Reading

- https://blog.cleancoder.com/uncle-bob/2013/05/27/TheTransformationPriorityPremise.html
- https://blog.cleancoder.com/uncle-bob/2013/05/27/FibTPP.html

## Summary

Supports the mantra

> As the tests get more specific, the code gets more generic.

Transform behavior from something specific to something generic in the smallest possible way.

### Proposed Transformations

from highest to lowest priority

- `({} → nil)` no code at all → code that employs nil
- `(nil → constant)`
- `(constant → constant+)` a simple constant to a more complex constant
- `(constant → scalar)` replacing a constant with a variable or an argument
- `(statement → statements)` adding more unconditional statements
- `(unconditional → if)` splitting the execution path
- `(scalar → array)`
- `(array → container)`
- `(statement → tail-recursion)`
- `(if → while)`
- `(statement → non-tail-recursion)`
- `(expression → function)` replacing an expression with a function or algorithm
- `(variable → assignment)` replacing the value of a variable
- `(case)` adding a case (or else) to an existing switch or if

There may be more transformations.

The proposed ordering could be refined.

## Practice

### Kata Suggestions

- [Numbers in words](http://codingdojo.org/kata/NumbersInWords/)
- [Prime factors](https://github.com/ardalis/kata-catalog/blob/main/katas/Prime%20Factors.md)
- [Fibonacci](https://www.codewars.com/kata/53d40c1e2f13e331fc000c26)
- [Roman numerals](https://github.com/UtahSC/roman-numeral-kata)

When passing a test, prefer higher priority transformations.

When posing a test, choose one that can be passed with higher priority transformations.

When an implementation seems to require a low priority transformation, backtrack to see if there is a simpler test to pass.

Suggestion: During practice, keep a running list of the transformations that you apply. Can you name the transformation you are applying? Is it the simplest thing you can do?

## Things to Think About

- Were you able to name the transformation you applied?
- Do any of these transformations need refining?
- Do they need to be reordered?
- Are there additional transformations you found?
- Did you ever feel like you had to jump too far down the list or had trouble seeing a simpler/higher priority transformation?
- Does this feel limiting when writing code to pass a test?
- Does keeping these transformations in mind help you find simpler solutions?
- Can the transformations apply to the tests, as well as the implementation?
