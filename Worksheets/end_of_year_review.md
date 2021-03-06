# String & Lists Worksheet (32 pts total)

**Due:** Monday June 16th, emailed by end of day.

**Instructions:**
* Please submit your answers to <tealsteachers@gmail.com>.
* You can use Python to answer the questions.
* **Please work on the problems individually.** 

**You can test your Python code online here:** http://repl.it/

## Question 1

The following functions are all intended to check whether a string contains _any_ lowercase letters, but at least some of them are wrong! 

**For each function below, decide whether the function works as intended. If not, describe what the function actually does.** 

You can assume that the parameter `s` is always a string and that there are no syntax errors. You may copy these functinos into Spyder to test them, but you will only get credit if you inculde the explanation of what the function actully does .

A working `any_lowercase()` function would work as follows:

Function Call              | Return value |
-------------------------- | ------------ | 
`any_lowercase("hello")`   | True  |
`any_lowercase("Hello")`   | True  |
`any_lowercase("HeLLO")`   | True  |
`any_lowercase("HELLO")`   | False |

Note, `islower()` is a string method that returns `True` if all characters in the string are lowercase. It returns `False` otherwise. Also not the answer is returned, and not printed. To see the return value try `print any_lowercase("hello")`. 

### Example:

```python
def any_lowercase1(s):
    for c in s:
        if c.islower():
            return True
        else: 
            return False
```

This function does not work because it checks only the first character, and then returns True or False. When the function returns, it ends and the rest of the characters are not checked. This would return True when the *first* character is lowercase and False otherwise, even if there was a lower case character later in the sting.

**[Here's how I tested if this function works.](http://repl.it/UIO/3)**

### (4 pts each)

```python         
def any_lowercase2(s):
    for c in s:
        if 'c'.islower():
            return 'True'
        else:
            return 'False'
```

```python
def any_lowercase3(s):
    for c in s:
        flag = c.islower()
    return flag
```

```python
def any_lowercase4(s):
    flag = False
    for c in s: 
        flag = flag or c.islower()
    return flag
```

```python
def any_lowercase5(s):
    for c in s:
        if not c.islower():
            return False
    return True
```

### Question 2 (8 pts)
The following code throws an error when you try to run it. The error is
```
Traceback (most recent call last):
  File "test.py", line 7, in <module>
    print quantity[i] + " " + ingredients[i]
    
IndexError: list index out of range
```

1. Explain why there is an error.
2. Rewrite the code so it runs without errors.

*Note: there are multiple correct answers and your answer should be valid python code! Please type your code answer into Spyder or [repl.it](http://repl.it/) and test that it runs without errors.* 

```python
ingredients = ["butter", "apples", "sugar", "nutmeg"]
quantity = ["one stick", "10", "1 cup"]

print "Ingredient:"

for i in range(len(ingredients)):
    print quantity[i] + " " + ingredients[i]
    
```

### Question 3 (8 pts)

The following code should print the items in food_list that are capitalized, the code throws an error when you try to run it. The error is 
```
Traceback (most recent call last):
  File "test.py", line 4, in <module>
    if food[0].upper() == food[0]:
TypeError: 'int' object has no attribute '__getitem__'
```

1. Explain why there is an error. You may need to copy this code into Spyder and run it to figure this out.
2. Rewrite the code so it runs without errors. 

*Note: there are multiple correct answers and your answer should be valid python code! Please type your corrected code into Spyder or [repl.it](http://repl.it/) and test that it runs without errors.* 

```python
food_list = ["Apple", "pear", "Banana", "mango"]

for food in range(len(food_list)):
    if food[0].upper() == food[0]:
        print food
```
