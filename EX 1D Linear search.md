# EX 1D Linear search
## DATE:05:04:2025

## Aim
To write a Python program to search for an element in a tuple using a linear search method.

## Algorithm
1. Define a function `search(tup, n)`:
   - Iterate over the tuple.
   - If any element matches `n`, return `True`.
   - If no match is found, return `False`.
2. Read an integer `x` from the user (number of elements).
3. Read `x` integers from the user and store them in a list.
4. Convert the list to a tuple.
5. Read the number to be searched (`n`).
6. Call the `search()` function.
7. Print whether the element was found or not.

## Program
```python
def search(tup, n):
    for i in range(len(tup)):
        if tup[i] == n:
            return True
    return False

List = [] 
x = int(input())
for i in range(x):
    List.append(int(input()))
tup = tuple(List)
n = int(input())
if search(tup, n):
    print(f"Tuple: {n} found")
else:
    print(f"Tuple: {n} not found")
```
## Output 
![image](https://github.com/user-attachments/assets/1a985cfc-b9ff-492a-947a-8d5b7f0ff52c)

## Result
The Python program successfully searches for an element in the tuple and displays whether it is found or not.
