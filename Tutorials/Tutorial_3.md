# An Introduction to Python 3: Conditional Statements

Conditional statements are the building blocks of decision-making in programming. They allow your code to execute different actions based on specific conditions. In this tutorial, we'll explore the fundamental conditional statements in Python: `if`, `elif`, and `else`.

## Understanding Conditional Statements

At the heart of every conditional statement is a condition, which is an expression that evaluates to either `True` or `False`. Based on this result, the program decides which block of code to execute.

### Basic Structure

```python
if condition:
    # code to execute if condition is True
else:
    # code to execute if condition is False
```

The `else` part is optional.

## Dive Deeper: `if`, `elif`, and `else`

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

## Exercises

1. **Temperature Checker**: Write a program that asks the user for the current temperature and prints whether it's hot, warm, or cold. Consider above 25°C as hot, between 15°C and 25°C as warm, and below 15°C as cold.

2. **Grade Calculator**: Ask the user for their exam score and print their grade. Use the following grading system: A (>=90), B (>=80), C (>=70), D (>=60), and F (<60).

3. **Leap Year Checker**: Write a program that checks if a given year is a leap year. A leap year is divisible by 4 but not divisible by 100 unless it's also divisible by 400.

<details>
<summary>Click to reveal the answers</summary>

```python
# Temperature Checker
temp = float(input("Enter the current temperature in °C: "))
if temp > 25:
    print("It's hot!")
elif 15 <= temp <= 25:
    print("It's warm.")
else:
    print("It's cold.")

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

# Leap Year Checker
year = int(input("Enter a year: "))
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print(f"{year} is a leap year.")
else:
    print(f"{year} is not a leap year.")
```

</details>

### Reflections

After completing the exercises:

- Reflect on the importance of the order of conditions, especially when using multiple `elif` statements.
- Consider how nesting conditional statements can lead to more complex decision-making structures. How might you use nested conditions in future programs?

## Conclusion

Conditional statements are a powerful tool in programming, allowing for dynamic and responsive code. By mastering `if`, `elif`, and `else`, you can create programs that react differently to a wide range of scenarios. As you continue your Python journey, you'll find these statements to be foundational in many of the programs you write.
