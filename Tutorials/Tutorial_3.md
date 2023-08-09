# An Introduction to Python: 3. Conditional Statements

Conditional statements are the building blocks of decision-making in programming. They allow your code to execute different actions based on specific conditions. In this tutorial, we'll explore the fundamental conditional statements in Python: `if`, `elif`, and `else`.

## 1. Understanding Conditional Statements

At the heart of every conditional statement is a condition, which is an expression that evaluates to either `True` or `False`. Based on this result, the program decides which block of code to execute.

### Basic Structure

```python
if condition:
    # code to execute if condition is True
else:
    # code to execute if condition is False
```

The `else` part is optional.

## 2. Dive Deeper: `if`, `elif`, and `else`

### The `if` Statement

The `if` statement checks a condition and executes the code inside its block if the condition is `True`.

```python
x = 10
if x > 5:
    print("x is greater than 5")
```

### The `elif` Statement

`elif` stands for "else if". It allows you to check multiple conditions. If the condition for `if` is `False`, it checks the condition of the next `elif`.

```python
x = 10
if x > 15:
    print("x is greater than 15")
elif x > 5:
    print("x is greater than 5 but not greater than 15")
```

### The `else` Statement

If none of the conditions specified by `if` and `elif` are `True`, the code inside the `else` block will execute.

```python
x = 3
if x > 5:
    print("x is greater than 5")
else:
    print("x is 5 or less")
```
## 3. Walkthrough Example: Heaviside Step-Function

Before diving into the exercises, let's explore a real-world example that demonstrates the use of conditional statements. We'll write a Python script to calculate the Heaviside step-function, defined piecewise as:

$$
H(x) = \begin{cases} 
      0 & \text{if } x < 0 \\
      \frac{1}{2} & \text{if } x = 0 \\
      1 & \text{if } x > 0 
   \end{cases}
$$

Here's how we can implement this function using `if`, `elif`, and `else`:

1. **Input the Value**: First, we need to ask the user for a value of \( x \) using the `input()` function. Since `input()` returns a string, we'll convert it to a float.

2. **Check for \( x < 0 \)**: We'll use an `if` statement to check if \( x < 0 \), and if so, print 0.

3. **Check for \( x = 0 \)**: Next, we'll use an `elif` statement to check if \( x = 0 \), and if so, print $\frac{1}{2}$.

4. **Handle \( x > 0 \)**: Finally, if neither of the above conditions is met, we'll use an `else` statement to handle the case where \( x > 0 \), printing 1.

Here's the code:

```python
# Heaviside Step-Function
x = float(input("Enter a value for x: "))
if x < 0:
    print("H(x) = 0")
elif x == 0:
    print("H(x) = 1/2")
else:
    print("H(x) = 1")
```

Try running this code with different values of \( x \) to see how the conditional statements guide the program to the correct output. Notice how the indentation and colons are used to structure the code. This example should give you a solid understanding of how to use conditional statements in Python.

Now, let's move on to the exercises, where you'll have a chance to apply what you've learned!

## 4. Exercises

1. **Temperature Checker**: Write a program that asks the user to input the current temperature. Then, have the program print whether it's hot, warm, or cold. Consider above 25°C as hot, between 15°C and 25°C as warm, and below 15°C as cold.

<details>
<summary><i>Click to reveal the answers</i></summary>

```python
# Temperature Checker
temp = float(input("Enter the current temperature in °C: "))
if temp > 25:
    print("It's hot!")
elif 15 <= temp <= 25:
    print("It's warm.")
else:
    print("It's cold.")
```

</details>

2. **Grade Calculator**: Write a program that asks the user to input their exam score.. Then, have the program print their grade. Use the following grading system: A (>=90), B (>=80), C (>=70), D (>=60), and F (<60).

<details>
<summary><i>Click to reveal the answers</i></summary>

```python
# Grade Calculator
score = float(input("Enter your exam score: "))
if score >= 90:
    print("Your grade is A")
elif score >= 80:
    print("Your grade is B")
elif score >= 70:
    print("Your grade is C")
elif score >= 60:
    print("Your grade is D")
else:
    print("Your grade is F")
```

</details>

3. **Leap Year Checker**: Write a program that takes an input year and checks if the given year is a leap year. A leap year is divisible by 4 but not divisible by 100 unless it's also divisible by 400.

<details>
<summary><i>Click to reveal the answers</i></summary>

```python
# Leap Year Checker
year = int(input("Enter a year: "))
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print(f"{year} is a leap year.")
else:
    print(f"{year} is not a leap year.")

```
> The code above uses a feature called an f-string. An f-string is similar to a traditional string, however prefixed with 'f'. Inside an f-string, expressions enclosed in curly braces {} can be used to embed values directly into the string. In this case, the value of the 'year' variable is embedded into the string. When the f-string is evaluated, the expression inside the curly braces is computed and then inserted into the string. F-strings are an easy way to have variables which can dynamically change depending on the program output into a string format.

</details>

### Reflections

Having completed this tutorial on Conditional Statements, let's take a moment to reflect on what we've learned:

1. **Decision Making in Programming**: Just as in real life, where we make decisions based on certain conditions, in programming, we use conditional statements to allow our code to make decisions. This is a foundational concept in all of programming, making your code dynamic and responsive to different inputs or situations.

2. **Versatility of Conditional Statements**: The exercises demonstrated the versatility of `if`, `elif`, and `else` statements. Whether determining temperature ranges, grading scales, or leap years, conditional statements provide the logic backbone to many operations.

3. **Nested and Compound Conditions**: By nesting conditions or combining them with logical operators (`and`, `or`, `not`), we can create more complex decision-making structures. This allows for more nuanced and detailed conditions in our programs.

## Conclusion

Conditional statements are a powerful tool in programming, allowing for dynamic and responsive code. By mastering `if`, `elif`, and `else`, you can create programs that react differently to a wide range of scenarios. As you continue your Python journey, you'll find these statements to be foundational in many of the programs you write.
