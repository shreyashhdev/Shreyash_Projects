# Shreyash_Projects
This Repository Shows All My Project That been Created myself during college
/n
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
