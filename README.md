![](https://miro.medium.com/v2/format:webp/1*hicFMnjJf8GyP0sleHrTbA.png)

## Introduction

I have observed that significant portion of my working time is spent waiting for my code to finish running. Additionally, I've noticed that many works are challenging to understand due to lack of explanation. I believe that writing efficient python code can help reduce runtime and save computational resources, ultimately freeing more meaningful tasks as a Data Scientist.

One of Guido's key insights is that code is read much more often than it is written. The guidlines provided here are intended to improve the readability of code. A style guide is about consistency. Consistency with this style guide is important. Consistency within a project is more important. Consistency within one module or function is the most important.

However, know when to be consistent, sometimes a style guide recommendations just aren't applicable. When in doubt, use your best judgement. Look at other examples and decide what looks best.

## General Tips for Clean code:

### 1. Follow PEP 8:

  Adhere to pythons style guide, PEP 8 (Python Enhancement Proposal). It covers conventions for naming, identation, and other aspects of writting clean and readable code. Check out the official website [pep 8 - style Guide for python code](https://peps.python.org/pep-0008/). You can also check out the [PEP-8: Python Naming Conventions & Standards](https://www.datacamp.com/tutorial/pep8-tutorial-python-code) by datacamp.

### 2. Use Meaningful Names:

  Choose descriptive and meaningful names for variables, functions, and classes. Names should convey the purpose and content of the entity.

### 3. Keep Functions Short and Focused:

  Functions should ideally perform one task and do it well. if a function is becoming too long, consider breaking it into smaller, more focused functions.

### 4. Comments and Documentation:

  Add comments when necessary (sparingly), but strive to write self-explanatory code. Document your code, especially for complex functions or projects, using [docstrings](https://www.geeksforgeeks.org/python-docstrings/)

### 5. Whitespace and Formatting:

  Use consistent identation (usually 4 spaces) and spacing. Don't overuse blank lines, but use them to separate logical sections of code.

## Tips for Writing Efficient Codee:

### 1. Use List Comprehension:

List comprehensions are concise and often more readable than traditional loops for creating lists.

### 2. Choose the Right Data Structures:

  Select the appropriate data structures for your needs. For example, use sets for membership testing, dictionaries for key-value pairs, etc.

### 3. Generator Expressions:

  Use [generator expressions](https://www.geeksforgeeks.org/generator-expressions/) when you don't need to store the entire result in memory.

### 4. Avoid Unnecessary Variables:

  Minimize the use of unnecessary variables. Sometimes, operations can be performed without storing intermediate results.

### 5. Use Efficient Libraries:

  Leverage efficient libraries and functions from the python standard Library or third party libraries when applicable. avoid reinventing the wheel.

### 6. Profile and Optimize:

  Use profilling tools to identify bottlenecks in your code. Optimize critical sections if needed, but focus on readability unless performance is a critical concern

### 7. Error Handling:

  Implement proper error handling to make your code robust. Use try-except blocks to catch and handle exceptions gracefully.

### 8. Version Control:

  Use version control systems like Git to track changes and collaborate with others.

### 9. Testing:

  Write unit test for your code. Automated tests help catch errors early and provide a safety net for [refactoring](https://www.freecodecamp.org/news/best-practices-for-refactoring-code/).

### 10. Readability Matters:

  Prioritize code readability over cleverness. Write code so that others (or future you can understand it easily).

### 11. Continuous Learning:

  Stay updated with best practises, new language features, and community guidelines. Continuous learning helps improve your coding skills.

## PEP 8 Summary:

### Indentation

* The recommendation is to use 4 spaces for indentation

* When you write a big expression, it is best to keep the expression vertically aligned. When you do this you will create a "hanging indent"
  ```python
  list_of_people = [
      "Rama"
      "John"
      "shiva"
  ]
  ```
  ```python
  def square_of_number(
      num1, num2,
      num3, num4):
  ```
  * Generally, spaces are the preferred indentation means
 
  ### Maximum Line Length

  * Generally, it's good to aim for a line of 79 characters in your python code. By doing this it is possible to open files side by side to compare. You can also view the whole expression without scrolling horizontally, which adds to better readability and understanding the code.
 
### Blank Lines

* In python scripts, top-level functions and classes are separated by two lines. Method definitions inside classes should be separated by one blank line.
* Blank lines may be omitted between a bunch of related one-liners.
* Use blank lines in functions, sparingly to indicate logical sections.

```python
import unittest

class SwapTestSuite(unittest.TestCase):
    """
        Swap Operation Test Case
    """
    def setUp(self):
        self.a = 1
        self.b = 2

    def test_swap_operations(self):
        instance = Swap(self.a,self.b)
        value1, value2 =instance.get_swap_values()
        self.assertEqual(self.a, value2)
        self.assertEqual(self.b, value1)


class OddOrEvenTestSuite(unittest.TestCase):
    """
        This is the Odd or Even Test case Suite
    """
    def setUp(self):
        self.value1 = 1
        self.value2 = 2

    def test_odd_even_operations(self):
        instance1 = OddOrEven(self.value1)
        instance2 = OddOrEven(self.value2)
        message1 = instance1.get_odd_or_even()
        message2 = instance2.get_odd_or_even()
        self.assertEqual(message1, 'Odd')
        self.assertEqual(message2, 'Even')
```

### Should a Line Break Before or After a Binary Operator?

* In python code, it is permissible to break before or after a binary operator, as long as the convention is consistent locally. However, following the tradition from mathematics, breaking before a binary operation provides a more readable code.

```python
# easy to match operators with operands
income = (gross_wages
          + taxable_interest
          + (dividends - qualified_dividends)
          - ira_deduction
          - student_loan_interest)
```

### Imports
* Imports should usually be on separate lines:

```python
# Correct:
import os
import sys
```
* It's okay to say this though:
  
```python
# Correct:
from subprocess import Popen, PIPE
```
* Imports are always put at the top of the file, just after any module comments and docstring, and before module globals and constants.
  
* Imports should be grouped in the following order:
    1. Standard library imports
    2. Related third party imports
    3. Local application imports

* You should put a line between each group of imports.

### Whitespace in Expressions and Statements

Avoid extraneous whitespace in the following situations:

* Immediately inside paretheses, brackets or braces:
```python
# Correct:
spam(ham[1], {eggs: 2})
```

* Between a trailing comma and a following close parenthesis:
```python
# Correct:
foo = (0,) # Tuple with a single element
```

* Immediately before a comma, semicolon, or colon:
```python
# Correct:
if x == 4: print(x, y); x, y = y, x
```
However, in a slice the colon acts like a binary operator and should have equal amounts on either side. In an extended slice, both colons must have the same amount of spaces applied. Exception: When a slice parameter is omitted, the space should be omitted:
```python
# Correct:
ham[1:9], ham[1:9:3], ham[:9:3], ham[1::3], ham[1:9:]
ham[lower:upper], ham[lower:upper:], ham[lower::step]
ham[lower+offset : upper+offset]
ham[: upper_fn(x) : step_fn(x)], ham[:: step_fn(x)]
ham[lower + offset : upper + offset]
```
* More than one space around an assignment (or other) operator:
```python
# Correct:
x = 1
y = 2
long_variable = 3
```
* Always surround these binary operators with a single space on either side: assignment (`=`), augmented assignment (`+=`, `-=` etc.), comparisons (`==`, `<`, `>`, `!=`, `<>`, `<=`, `>=`, `in`, `not in`, `is`, `is not`), Booleans (`and`, `or`, `not`).

* If operators with different priorities are used, consider adding whitespace around the operators with the lowest priority(ies). Use your own judgment; however, never use more than one space, and always have the same amount of whitespace on both sides of a binary operator:
```python
# Correct:
i = i + 1
submitted += 1
x = x*2 - 1
hypot2 = x*x + y*y
c = (a+b) * (a-b)
```

* Function annotations should use the normak rules for colons and always have spaces around the `->` arrow if present.
```python
# Correct:
def munge(input: AnyStr): ...
def munge() -> PosInt: ...
```

### Comments
