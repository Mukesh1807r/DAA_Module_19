# EX 1B Merge Sort
## DATE:29:03:2025

## Aim
To write a Python program to sort an array of integers using the Merge Sort algorithm.

## Algorithm
1. Define a `merge()` function to merge two sorted subarrays:
   - Create temporary arrays L[] and R[].
   - Copy data to L[] and R[] from the original array.
   - Merge the arrays back into the original array.
2. Define a `mergesort()` function:
   - If left < right:
     - Find the middle index.
     - Recursively call `mergesort()` on left and right halves.
     - Call `merge()` to combine the sorted halves.
3. Read `n` elements from the user and store them in an array.
4. Print the original array.
5. Call `mergesort()` to sort the array.
6. Print the sorted array.

## Program
```python
def merge(arr,left,middle,right):
    n1 = middle - left + 1
    n2 = right - middle
    L = [0] * n1
    R = [0] * n2
    for i in range(n1):
        L[i] = arr[left + i]
    for j in range(n2):
        R[j] = arr[middle + 1 + j]
    i = j = 0
    k = left
    
    while i < n1 and j < n2:
        if L[i] <= R[j]:
            arr[k] = L[i]
            i += 1
        else:
            arr[k] = R[j]
            j += 1
        k += 1
    while i < n1:
        arr[k] = L[i]
        i += 1
        k += 1
    while j < n2:
        arr[k] = R[j]
        j += 1
        k += 1

def mergesort(arr,left,right):
    if left < right:
        middle = (left + right) // 2
        mergesort(arr, left, middle)
        mergesort(arr, middle + 1, right)
        merge(arr, left, middle, right)

def print_sort(arr):
    for i in range(len(arr)):
        print(arr[i], end=' ')

n = int(input())
arr = [int(input()) for _ in range(n)]

print("Given array is")
print_sort(arr)
mergesort(arr, 0, n - 1)
print("\n\nSorted array is")
print_sort(arr)
```
## Output 
![image](https://github.com/user-attachments/assets/b7f552d1-2c1f-41a7-8fa5-f33b09b20783)

## Result 
The Python program successfully sorts the given array using the Merge Sort algorithm.


