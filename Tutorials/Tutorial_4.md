# An Introduction to Python: 4. Loops

Loops are fundamental in programming, allowing for repetitive execution of code blocks. Python provides two primary loop mechanisms: `while` and `for`. This tutorial introduces the basics of both.

## 1. `while` Loop

### Introduction

The `while` loop is a control flow statement that allows code to be executed repeatedly based on a given Boolean condition. The `while` loop can be thought of as a repeating `if` statement.

### General Structure

```python
[Initialization]
while [Condition]:
    [Loop Body]
    [Update Statement]
```

- **Initialization**: Before the loop starts, variables used in the condition or the loop body are usually initialized.
  
- **Condition**: This is a Boolean expression that determines whether the loop will continue. If it evaluates to `True`, the loop body executes. If `False`, the loop terminates.
  
- **Loop Body**: This is the main set of statements that need to be repeatedly executed.
  
- **Update Statement**: Within the loop body, certain variables (often those in the condition) are updated to ensure that the loop progresses and eventually terminates.

### Example

```python
x = 0  # Initialization
while x < 10:  # Condition
    print(x, x*x)  # Loop Body
    x = x + 1  # Update Statement
```

**Reflection**: Before running the code, consider: How many times will the loop execute?

### Key Insights

- **Initialization**: `x` is initialized before the loop. This is crucial since the loop's condition relies on `x`.
  
- **Condition**: The loop continues as long as `x < 10` remains `True`.
  
- **Loop Body**: The indented code under the `while` statement is the loop's core. It prints `x` and its square.
  
- **Increment**: `x` increases with each iteration. Without this, the loop would run indefinitely, causing an "infinite loop".

## 2. `for` Loop

### Introduction

The `for` loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string). It's a more concise way to iterate through items, especially when you know the number of iterations beforehand.

### General Structure

```python
for [Item] in [Sequence]:
    [Loop Body]
```

- **Item**: Represents the current position in the sequence during the iteration.
  
- **Sequence**: The list, tuple, string, etc. you want to iterate over.
  
- **Loop Body**: The main set of statements that will be executed for each item in the sequence.

### Example with a List

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

This loop will print each fruit in the list.

### Introduction to `range()`

When working with loops, often you might want to iterate over a sequence of numbers. Instead of writing them out explicitly like:

```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
for number in numbers:
    print(number)
```

You can use the `range()` function, which is a built-in function in Python that generates a sequence of numbers. 

```python
for x in range(10):
    print(x)
```

The `range()` function returns a sequence of numbers, starting from 0 by default, and increments by 1 (also by default), and stops before a specified number. The `range()` function is a versatile tool that can be used to generate sequences of numbers for iteration, offering both simplicity and efficiency. `range()` is just one of many Python objects (including lists, tuples, and strings) that can be iterated over by a loop.
 
## 3. Choosing Between `while` and `for` Loops

When writing a loop in Python, you'll often have to decide between using a `while` loop or a `for` loop. Both can achieve similar outcomes, but the choice between them often depends on the specific problem you're trying to solve. Here are some guidelines to help you decide:

### Use a `while` loop when:

1. **The number of iterations is unknown**: If you're unsure about how many times you need to loop, a `while` loop is more appropriate. For instance, when you're waiting for a specific condition to be met, like an input from a user or a change in a file's status.

   ```python
   response = ""
   while response != "exit":
       response = input("Enter a command (type 'exit' to quit): ")
   ```
### Use a `for` loop when:

1. **You know the number of iterations**: If you're looping over a fixed set of items or a range of numbers, a `for` loop is more intuitive.

   ```python
   for i in range(5):
       print(i)
   ```

2. **You're iterating over a sequence**: `for` loops are designed to iterate over sequences like lists, strings, dictionaries, etc. They make it easy to loop through each item in these structures.

   ```python
   for letter in "Python":
       print(letter)
   ```

### In Summary:

- Use `while` loops when the loop's continuation is based on a condition rather than a sequence.
- Use `for` loops when you're iterating over a known sequence or range of numbers.

Remember, while both loop types can often be used interchangeably, choosing the right one can make your code clearer and more efficient. Always consider the specific needs of your task when deciding which loop to use.

## 4. Advanced Loops

As you become more familiar with loops, you'll encounter situations where basic loops aren't enough. Sometimes, you'll need to control the flow of your loop more precisely or even use loops within loops. This section introduces you to some advanced loop concepts: nested loops and the `break` and `continue` statements.

### Nested Loops

A loop inside another loop is called a nested loop. The "inner loop" will be executed one time for each iteration of the "outer loop".

**Example**:
```python
for i in range(3):  # Outer loop
    for j in range(3):  # Inner loop
        print(i, j)
```

This will produce a combination of values from both loops:

```
0 0
0 1
0 2
1 0
1 1
... and so on.
```

### Break and Continue

These are two loop control statements that allow more complex execution patterns.

- **break**: Exits the loop prematurely. It's typically used when a certain condition is met and there's no need to continue the loop.

  **Example**:
  ```python
  for i in range(5):
      if i == 3:
          break
      print(i)
  ```

  This will print:
  ```
  0
  1
  2
  ```

- **continue**: Skips the current iteration and continues with the next one.

  **Example**:
  ```python
  for i in range(5):
      if i == 2:
          continue
      print(i)
  ```

  This will print:
  ```
  0
  1
  3
  4
  ```

Both `break` and `continue` can be used in `for` and `while` loops, but use them wisely. Overusing or misusing these can make your code less readable.


## 5. Exercises

1. Write a `for` loop that prints numbers from 1 to 5.

      **Reflection:** Familiarize yourself with the basic structure of a `for` loop.
      
      <details>
      <summary><i>Click to reveal a possible answer</i></summary>
      
      ```python
      for i in range(1, 6):
          print(i)
      ```
      
      </details>
      </br>

2. Write a `while` loop that prints numbers from 1 to 5.

      **Reflection:** Understand the structure and flow of a `while` loop.
      
      <details>
      <summary><i>Click to reveal a possible answer</i></summary>
      
      ```python
      i = 1
      while i <= 5:
          print(i)
          i += 1
      ```
      
      </details>
      </br>
      
3. Use a `for` loop and `range()` to print numbers from 10 to 15.

      **Reflection:** Introduce the utility of `range()` in simplifying loop constructs.
      
      <details>
      <summary><i>Click to reveal a possible answer</i></summary>
      
      ```python
      for i in range(10, 16):
          print(i)
      ```
      
      </details>
      </br>
      
4. Using nested loops, print a pattern of stars (`*`) in the shape of a right triangle, where the height of the triangle is 5 lines. The output should look like:

    ```
    *
    **
    ***
    ****
    *****
    ```

      **Reflection:** This exercise helps you understand how to use nested loops to generate patterns. It's a basic introduction to the concept of controlling the number of iterations in an inner loop based on the current iteration of an outer loop.
      
      <details>
      <summary><i>Click to reveal a possible answer</i></summary>
      
      ```python
      for i in range(1, 6):
          print('*' * i)
      ```
      
      </details>
      </br>

5. Using a loop, calculate and print the following quantities for `range(10)`:
    - `x**2`
    - `exp(x)`
    - `sin(x)*cos(x)`
    - `log(1+x)`
   </br>
  
   > Note: To use the math functions above, you need to import these functions from the math library by typing the following line at the top of your script: `from math import *`

      **Reflection:** Combining loops with mathematical functions allows for efficient computations over a range of values.
      
      <details>
      <summary><i>Click to reveal a possible answer</i></summary>
      
      ```python
      from math import *
      
      for x in range(10):
          print(f"x = {x}")
          print("Square:", x**2)
          print("Exponential:", exp(x))
          print("sin(x)*cos(x):", sin(x)*cos(x))
          print("Logarithm:", log(1+x))
          print("------")
      ```
      
      </details>
      </br>
      
6. Write a `for` loop that prints numbers from 1 to 10, but stops (breaks) the loop when it reaches 5.

      **Reflection:** Understand the utility of the `break` statement in controlling loop execution.
  
      <details>
      <summary><i>Click to reveal a possible answer</i></summary>
      
      ```python
      for i in range(1, 11):
          if i == 5:
              break
          print(i)
      ```
  
      </details>
      </br>
      
7. Write a `for` loop that prints numbers from 1 to 10, but skips (continues) the loop when it reaches 5.

      **Reflection:** Grasp the concept of the `continue` statement to skip certain iterations in a loop.
      
      <details>
      <summary><i>Click to reveal a possible answer</i></summary>
      
      ```python
      for i in range(1, 11):
          if i == 5:
              continue
          print(i)
      ```
      
      </details>
      </br>

## Conclusion

Loops are a cornerstone in Python programming. You've seen how loops can simplify repetitive tasks, making your code more efficient and readable. The importance of understanding loop conditions to predict and control the number of iterations cannot be understated. The `while` loop offers versatility, especially when the iteration count isn't predetermined. In contrast, the `for` loop is ideal for iterating over sequences or when the range is known. As you progress in Python, you'll encounter more advanced loop topics, enhancing your coding efficiency and expanding your problem-solving toolkit.
