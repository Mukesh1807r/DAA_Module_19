# EX 1A GCD Calculator
## DATE:

## Aim
To write a Python program to find the Greatest Common Divisor (GCD) of two numbers using the Euclidean algorithm.

## Algorithm
1. Define a recursive function `gcd(a, b)`.
2. If `b == 0`, return `a`.
3. Else, return `gcd(b, a % b)`.
4. Read two integers from the user.
5. Call the `gcd()` function and print the result.

## Program
```python
def gcd(a, b):
    if b == 0:
        return a
    else:
        return gcd(b, a % b)

num1 = int(input(""))
num2 = int(input(""))

print(f"{gcd(num1, num2)}")
```
---
## Output
![image](https://github.com/user-attachments/assets/f538c363-7ae4-45b2-93e7-ad48abc17f52)

## Result
The Python program successfully calculates and displays the GCD of two given integers.


