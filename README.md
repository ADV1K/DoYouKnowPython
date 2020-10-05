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

<details>
    <summary>Show Answer</summary>  
    42 will be printed twice.  
</details>
<details>
    <summary>Show Reason</summary>  
    finally block will run no matter what happens in the try-block. if try block raises a error, encounter a break, continue or return statement then finally block will run.  
</details>

---

## What Will be returned when you call the function?

```python
def func():
    try:
        return 42
    finally:
        return 69
```

<details><summary>Show Answer</summary>  
69
</details>

<details><summary>Show Reason</summary>  
If a finally clause includes a return statement, the returned value will be the one from the finally clause’s return statement, not the value from the try clause’s return statement
</details>

<details><summary>Reference</summary>  
https://docs.python.org/3/tutorial/errors.html#defining-clean-up-actions  
</details>

---

## What Will happen when you run this code?

```python
try:
    import sys
    sys.exit()
except:
    print("42 is the answer to life.")
```

<details><summary>Show Answer</summary>  
```42 is the answer to life.``` is printed to the screen
</details>

<details><summary>Show Reason</summary>  
The exit() function raises SystemExit Exception which exits the program but since it is placed in a try block this exception is caught and the code in except block runs.  
</details>

<details><summary>Reference</summary>  
https://docs.python.org/3/library/sys.html#sys.exit  
</details>

---
