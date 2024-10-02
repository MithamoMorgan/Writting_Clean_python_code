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
  
  
