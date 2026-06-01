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
