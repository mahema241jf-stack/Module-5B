# NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

## 🧠 Algorithm

1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Accept a 2D NumPy array from the user.
3. **Sort Column-wise**: Use the `np.sort()` function with `axis=0` to sort each column in ascending order.
4. **Store Result**: Store the sorted result in a new array.
5. **Display Output**: Print the original array and the column-wise sorted array.

## 🧾 Program
```
import numpy as np

rows = int(input("Enter number of rows: "))
cols = int(input("Enter number of columns: "))

print("Enter the elements:")
arr = np.array([[int(input()) for j in range(cols)] for i in range(rows)])

sorted_arr = np.sort(arr, axis=0)

print("Original Array:")
print(arr)

print("Column-wise Sorted Array:")
print(sorted_arr)
```
## Output
<img width="404" height="677" alt="{B3D4F06B-D84C-4CE4-948B-C561851A1E00}" src="https://github.com/user-attachments/assets/6dd89ae4-e1a3-417c-8145-2ce817b5e7de" />

## Result
The program successfully accepts a 2D NumPy array from the user, sorts each column in ascending order using np.sort() with axis=0, and displays both the original array and the column-wise sorted array.


# # NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

## 🎯 Aim
To write a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

## 🧠 Algorithm
1. **Import NumPy**: Import the NumPy library.
2. **Define Arrays**: Define two NumPy arrays, `x` and `y`, with the same shape (i.e., same number of elements).
3. **Use Boolean Indexing**: 
   - `x > y` gives a boolean array where elements of `x` are greater than `y`.
   - `x == y` gives a boolean array where elements of `x` are equal to `y`.
4. **Find Indices**: Use `np.where()` to get the indices where the conditions `x >= y` are satisfied.
5. **Print Indices**: Print the indices where the condition holds true.

## 🧾 Program

```
import numpy as np

x = np.array([10, 20, 30, 40, 50])
y = np.array([5, 25, 30, 35, 60])

indices = np.where(x >= y)

print("Indices where x >= y:")
print(indices)
```

## Output
<img width="393" height="124" alt="{985DF6AD-F564-46B9-BCA2-354D3B6203D1}" src="https://github.com/user-attachments/assets/c05e64a1-c4b5-4c51-9a47-298daea0ea92" />

## Result
The program successfully uses Boolean indexing and np.where() to find and print the indices where the elements of array x are greater than or equal to the corresponding elements of array y.
