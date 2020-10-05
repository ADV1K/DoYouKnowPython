# Do you think you know Python?

## What Will happen when you run this code?

```python
def func():
    try:
        return 42
    finally:
        print(42)
print(func())
```

Answer: 42 will be printed twice.
Reason: finally block will run no matter what happens in the try-block. if try block raises a error, encounter a break, continue or return statement then finally block will run.

---

## What Will be returned when you call the function?

```python
def func():
    try:
        return 42
    finally:
        return 69
```

Answer: 69
Reason: If a finally clause includes a return statement, the returned value will be the one from the finally clause’s return statement, not the value from the try clause’s return statement
Reference: https://docs.python.org/3/tutorial/errors.html#defining-clean-up-actions

---

## What Will happen when you run this code?

```python
try:
    import sys
    sys.exit()
except:
    print("42 is the answer to life.")
```

Answer: the code inside except block will run.
Reason: the exit() function raises SystemExit Exception which exits the program but since it is placed in a try block this exception is caught and the code in except block runs.
Reference: https://docs.python.org/3/library/sys.html#sys.exit

---
