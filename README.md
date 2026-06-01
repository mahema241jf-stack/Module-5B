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

# NumPy Program: Replace the Second Column in a 2D Array

## 🎯 Aim
To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.

## 🧠 Algorithm
1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Get a 2D NumPy array and a new column (as another array) from the user.
3. **Delete Column**: Use `np.delete()` to remove the second column (index 1) from the original array.
4. **Insert Column**: Use `np.insert()` to insert the new column at the second column's original position.
5. **Display Result**: Print the updated array with the replaced column.

## 🧾 Program

```
import numpy as np

arr = np.array([[1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]])

new_col = np.array([10, 11, 12])

arr = np.delete(arr, 1, axis=1)
arr = np.insert(arr, 1, new_col, axis=1)

print(arr)
```

## Output
<img width="398" height="200" alt="{F3680716-405D-4484-8627-F32F65F97785}" src="https://github.com/user-attachments/assets/f5563c61-d9e5-4e85-8ef1-a31223ef833d" />


## Result
The program successfully replaces the second column of the array with a new column and displays the updated array.


# Pandas Program: Create and Display a DataFrame with Custom Index Labels

## 🎯 Aim

To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.

---

## 🧠 Algorithm

1. **Import Libraries**: Import the required libraries – `pandas` and `numpy`.
2. **Create Dictionary**: Define a dictionary `exam_data` with keys: `'name'`, `'score'`, `'attempts'`, and `'qualify'`.
3. **Index Labels**: Create a list of custom index labels called `labels`.
4. **Create DataFrame**: Use `pd.DataFrame()` to create the DataFrame by passing the dictionary and index labels.
5. **Display Output**: Display the DataFrame using `print()` or by simply calling the DataFrame variable.

---

## 💻 Program
```
import pandas as pd
import numpy as np

exam_data = {
    'name': ['Anu', 'Bala', 'Charan', 'Divya'],
    'score': [90, 85, 78, 92],
    'attempts': [1, 2, 1, 1],
    'qualify': ['Yes', 'Yes', 'Yes', 'Yes']
}

labels = ['a', 'b', 'c', 'd']

df = pd.DataFrame(exam_data, index=labels)

print(df)
```

## Output
<img width="433" height="286" alt="{0D1F9273-DC0D-4834-8399-FF61BD2E3A02}" src="https://github.com/user-attachments/assets/1a2bb290-18dd-48c3-99ce-41cefd5a0cf0" />


## Result
The program successfully creates a Pandas DataFrame from a dictionary using custom index labels and displays the DataFrame.

# 🧪 Pandas Program: Join Two DataFrames Along Rows

## 🎯 AIM

To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.

---

## 🧠 ALGORITHM

1. **Import Libraries**: Import the `pandas` library.
2. **Create First DataFrame**: Use a dictionary to create `student_data1`.
3. **Create Second DataFrame**: Use another dictionary to create `student_data2`.
4. **Concatenate DataFrames**: Use `pd.concat()` with `axis=0` to concatenate both DataFrames row-wise.
5. **Display Result**: Print the new combined DataFrame.

---

## 💻 Program

```
import pandas as pd

student_data1 = {
    'Name': ['Anu', 'Bala'],
    'Marks': [85, 90]
}

student_data2 = {
    'Name': ['Charan', 'Divya'],
    'Marks': [78, 92]
}

df1 = pd.DataFrame(student_data1)
df2 = pd.DataFrame(student_data2)

result = pd.concat([df1, df2], axis=0)

print(result)
```

## Output
<img width="419" height="300" alt="{BAF26F66-502F-49EC-B6D8-C0AFE71735D3}" src="https://github.com/user-attachments/assets/eb9d4cc3-d67d-400c-9755-e7802d6ff03b" />

## Result
The program successfully concatenates two DataFrames row-wise using pd.concat() and displays the combined DataFrame.

