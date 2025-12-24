# Shreyash_Projects
This Repository Shows All My Project That been Created myself during college
<br>
import pandas as pd
data = pd.DataFrame({
    'Category': ['Good', 'Better', 'Best', 'Good', 'Best'],
    'Gender': ['Male', 'Female', 'Female', 'Male', 'Male']
})

print("Original DataFrame:")
print(data)

encoded_data = pd.get_dummies(data, columns=['Category', 'Gender'], dtype=int)

print("\nOne-Hot Encoded DataFrame:")
print(encoded_data)


#Cleaning a dataset by identifying and removing invalid data entries. For example, a dataset having columns 'Name', ‘Gender’ and 'Age' where 'Name' contains 'invalid data'
<br>
import pandas as pd
import numpy as np
data = {
    'name': ['Alice', 'Bob', np.nan, '', 'Charlie', '12345', ' '],
    'gender': ['Female', 'Male', 'Male', 'Female', 'Male', 'Female', 'Male'],
    'age': [25, 30, 22, 28, 35, 40, 20]
}

df = pd.DataFrame(data)
print("Sample DataFrame:")
print(df)

invalid_names_mask = (df['name'].isna()) | \
                     (df['name'] == '') | \
                     (df['name'].str.strip() == '') | \
                     (~df['name'].astype(str).str.isalpha())

df_cleaned = df[~invalid_names_mask].copy()

print("\nDisplay the Cleaned DataFrame:")
print(df_cleaned) 

