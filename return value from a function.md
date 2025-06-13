In Python, a function can return a value to the caller using the `return` statement. The returned value can then be used elsewhere in the program. Let’s break it down with clear explanations and examples.

### Key Points About Return Values
1. **Purpose of `return`**: It sends a value (or multiple values) back to the caller of the function.
2. **Optional**: If no `return` statement is used, the function returns `None` by default.
3. **Exiting a Function**: The `return` statement also terminates the function’s execution, so any code after it in the function is not executed.
4. **Multiple Returns**: A function can return multiple values, typically as a tuple.

### Syntax
```python
def function_name(parameters):
    # Code block
    return value  # Returns 'value' to the caller
```

### Examples
#### 1. **Returning a Single Value**
```python
def add_numbers(a, b):
    result = a + b
    return result

# Call the function and store the returned value
sum = add_numbers(3, 5)
print(sum)  # Output: 8
```

Here, the function `add_numbers` returns the sum of `a` and `b`, which is stored in the variable `sum`.

#### 2. **No Return Statement (Returns `None`)**
```python
def greet(name):
    print(f"Hello, {name}!")

# Call the function
result = greet("Alice")
print(result)  # Output: None
```

Since `greet` doesn’t have a `return` statement, it implicitly returns `None`.

#### 3. **Returning Multiple Values**
Python allows returning multiple values, which are packed into a tuple by default.
```python
def get_user_info():
    name = "Alice"
    age = 25
    return name, age  # Returns a tuple

# Unpack the returned tuple
user_name, user_age = get_user_info()
print(user_name)  # Output: Alice
print(user_age)   # Output: 25
```

You can also access the returned tuple directly:
```python
info = get_user_info()
print(info)  # Output: ('Alice', 25)
```

#### 4. **Early Exit with `return`**
The `return` statement stops the function immediately.
```python
def check_number(num):
    if num > 0:
        return "Positive"
    return "Non-positive"

print(check_number(10))  # Output: Positive
print(check_number(-5))  # Output: Non-positive
```

Here, if `num > 0`, the function returns `"Positive"` and exits, skipping the rest of the code.

#### 5. **Returning Different Types**
Functions can return any Python data type (e.g., integer, string, list, dictionary, etc.).
```python
def get_fruits():
    return ["apple", "banana", "orange"]

fruits = get_fruits()
print(fruits)  # Output: ['apple', 'banana', 'orange']
```

### Common Use Cases
- **Calculations**: Return results of computations (e.g., `add_numbers` above).
- **Data Processing**: Return processed data, like a filtered list or modified string.
- **Validation**: Return `True`/`False` or status messages based on conditions.
- **Multiple Outputs**: Return multiple pieces of data for further use.

### Tips
- **Explicit is Better**: Always use `return` to make your function’s output clear.
- **Avoid Unnecessary Returns**: Don’t return values unless needed; use `print` for debugging or display.
- **Unpacking**: When returning multiple values, you can unpack them directly or access them as a tuple.
- **Default Return**: If you forget `return`, the function returns `None`, which might lead to unexpected behavior.

### Practice Exercise
Write a function that takes a number and returns whether it’s even or odd.
```python
def is_even(number):
    if number % 2 == 0:
        return "Even"
    return "Odd"

print(is_even(4))  # Output: Even
print(is_even(7))  # Output: Odd
```

Try writing similar functions, like one that returns the square of a number or checks if a string is a palindrome, to get comfortable with `return`.

If you want more examples, practice problems, or a deeper dive into specific use cases, let me know!
