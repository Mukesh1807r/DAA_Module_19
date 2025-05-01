# EX 1C Quick Sort
## DATE:01:04:2025

## Aim
To write a Python program to sort an array using the Quick Sort algorithm with a randomized pivot.

## Algorithm
1. Define a `partition()` function:
   - Randomly select a pivot index and swap it with the last element.
   - Use the last element as the pivot.
   - Rearrange the array so elements less than the pivot come before it.
   - Return the correct position of the pivot.
2. Define the `quick_sort()` function:
   - Recursively sort the elements before and after the pivot.
3. Read the size of the array and its elements from the user.
4. Call `quick_sort()` on the full array.
5. Print the sorted array.

## Program
```python
import random

def partition(arr, low, high):
    pivot_index = random.randint(low, high)
    arr[pivot_index], arr[high] = arr[high], arr[pivot_index]
    pivot = arr[high]
    i = low - 1

    for j in range(low, high):
        if arr[j] < pivot:
            i += 1
            arr[i], arr[j] = arr[j], arr[i]

    arr[i + 1], arr[high] = arr[high], arr[i + 1]
    return i + 1

def quick_sort(arr, low, high):
    if low < high:
        pi = partition(arr, low, high)
        quick_sort(arr, low, pi - 1)
        quick_sort(arr, pi + 1, high)

# Input
n = int(input())  
arr = [int(input()) for _ in range(n)]  

quick_sort(arr, 0, n - 1)
print(arr)
```
## Output 
![image](https://github.com/user-attachments/assets/7fbff611-cb51-4c0c-a3ba-7c3d84640236)

## Result 
The Python program successfully sorts the given array using the Quick Sort algorithm with a randomized pivot.

