# PROGRAMMING ASSIGNMENT 3
### GREFALDEO, Lettice Hyacinth P. | 2ECE-C

This repository contains Python scripts designed to solve the different problems given in ECE 2112, Programming Assignment 3. Below is a summary of each script

### Import and Load .csv file
```python
#import and load csv file
import pandas as pd

cars = pd.read_csv('cars.csv')
cars
```

**Output:**

<img width="710" height="692" alt="image" src="https://github.com/user-attachments/assets/1241e424-ddec-49d3-a064-7c6fd9eb436a" />
<img width="712" height="587" alt="image" src="https://github.com/user-attachments/assets/c5363fde-6a5c-4079-bea8-3e585ce1b2f1" />

## Programming Problems

#### A. POSITIONAL AND LABEL-BASED SLICING

This problem allows us to utilize and practice the use of slicing and stating important details of the array before proceeding to more specific problems about the array.

**Display shape and column names of the cars:**
```python
#display shape of cars array and display the column specification
print("Shape of cars:", cars.shape)
print("Column names:", list(cars.columns))
```

Output:

<img width="815" height="77" alt="image" src="https://github.com/user-attachments/assets/9ee3a43f-628b-4ff5-98e4-c7967efb57ac" />

**Array slicing:**
```python
#slice the array by displaying cars in rows 6-10 only
cars_6_to_10 = cars.iloc[5:10]

print("Rows 6 to 10:")
cars_6_to_10
```

Output:

<img width="817" height="272" alt="image" src="https://github.com/user-attachments/assets/f2411cb7-ae93-4c3f-a36f-a3e4377d17f1" />


**Show specific columns from sliced array:**
```python
#display specific columns only from rows 6-10
cars_subset = cars_6_to_10[['Model', 'mpg', 'cyl', 'hp', 'gear']]

print("selected columns:")
cars_subset
```


Output:

<img width="822" height="265" alt="image" src="https://github.com/user-attachments/assets/c76f8e4b-54b1-47fc-9111-1520dd042afb" />


#### B. MODEL LOOKUP

This problem will help us look at certain car models quickly by calling them and displaying the requested specifications.

**Display details of Toyota Corolla:**
```python
#dispay the details of Toyota Corolla
toyota = cars[cars['Model'] == 'Toyota Corolla']

print("Toyota Corolla:")
toyota
```

Output:

<img width="815" height="107" alt="image" src="https://github.com/user-attachments/assets/b64300e1-8801-4196-a368-e0b7dabc2d25" />

**Display specific details only of Pontiac Firebird:**
```python
#display the specific column details of the Pontiac Firebird
pontiac = cars[cars['Model'] == 'Pontiac Firebird'][['Model', 'mpg', 'hp', 'wt']]

print("Pontiac Firebird:")
pontiac
```

Output:

<img width="816" height="107" alt="image" src="https://github.com/user-attachments/assets/a30f3f26-e49f-44ad-8ebc-0151268f6ea9" />

#### C. MULTI-MODEL SUBSETTING

This problem will select specific cars (rows) and specifications (columns) and will display it in a new array

```python
selected_cars = cars[
    cars['Model'].isin(['Datsun 710', 'Lotus Europa', 'Ferrari Dino'])
][['Model', 'mpg', 'cyl', 'hp', 'gear']]

# Display the result
print("Selected Cars:",)
selected_cars
```

Output:

<img width="810" height="197" alt="image" src="https://github.com/user-attachments/assets/3bef50dd-4c68-4424-992f-fd3441ca1889" />

**Define the shape of the array:**
```python
#display the shaoe of the array 
print("\nshape of selected_cars:", selected_cars.shape)
```

Output:

<img width="810" height="56" alt="image" src="https://github.com/user-attachments/assets/6e6391df-6e59-42ca-87cd-9a8b4ad83f11" />




