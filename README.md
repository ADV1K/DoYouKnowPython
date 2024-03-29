# Do you think you know Python?

## What Will be the output? Why?

```python
for i in range(3):
    print(i)
else:
    print(‘Else block!’)
```

<details><summary>Show Answer</summary>  

```
0
1
2
Else block!
```

</details>
<details><summary>Show Reason</summary>  
    
Python loops have an extra feature that is not available in most other programming languages: you can put an else block immediately after a loop’s repeated interior block. The Else block executes when the loop is not terminated by a break block.

</details>
<details><summary>Reference</summary>

https://docs.python.org/3/tutorial/controlflow.html#break-and-continue-statements-and-else-clauses-on-loops

</details>

## What Will happen when you run this code?

```python
def func():
    try:
        return 42
    finally:
        print(42)
print(func())
```

<details><summary>Show Answer</summary>  
    
42 will be printed twice.  

</details>
<details><summary>Show Reason</summary>  
    
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
    
`42 is the answer to life.` is printed to the screen

</details>
<details><summary>Show Reason</summary>
    
The exit() function raises SystemExit Exception which exits the program but since it is placed in a try block this exception is caught and the code in except block runs.  

</details>
<details><summary>Reference</summary>  
    
https://docs.python.org/3/library/sys.html#sys.exit  

</details>

---

## What Will Be The Output?

```python
print('abc'.replace('', '|'))
print("".replace("", "advik"))
print("".replace("", "advik", 4))
```

<details><summary>Show Answer</summary>  
    
```
|a|b|c|
advik

```

</details>
<details><summary>Show Reason</summary>
    
In the first all the empty strings (empty space between letters) is replaced by "|"  
In the second one empty string is replace by "advik"  
actually a bug which was fixed in the latest version of python. more details here: https://bugs.python.org/issue28029  

</details>

---

## What Will Be The Output?

```python
bad = 'python2'
print('python2' is bad)

bad = 'python3!'
print('python3!' is bad)
```

<details><summary>Show Answer</summary>  
    
```
True
False
```

</details>
<details><summary>Show Reason</summary>
this is due to string interning.
</details>

<details><summary>Reference</summary>
https://stackabuse.com/guide-to-string-interning-in-python/

</details>

---
