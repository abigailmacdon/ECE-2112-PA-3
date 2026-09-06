# **ECE-2112-PA-3**
**Made by: Abigail T. Macdon | 2ECE-B**

This repository contains the content of the *Programming Assignment 2* for the course subject **"Advanced Computer Programming and Algorithms"** for the First Semester of A.Y. 2026-2027

It includes three Python problems based on **Module 3 - Pandas** which are the following:

  **A. POSITIONAL AND LABEL-BASED SLICING**
 
  **B. MODEL LOOKUP**

  **C. MULTI-MODEL SUBSETTING**

  Using the given CSV file named "cars" to load and create a DataFrame. Here is the link for the "cars.csv": https://github.com/abigailmacdon/ECE-2112-PA-3/blob/main/cars.csv.

To load the file this code is needed:

```python
import pandas as pd

cars = pd.read_csv('cars.csv')
cars
```

• `import pandas as pd` - This imports the Pandas library and uses "pd" as a shorter term when coding.

• `pd.read_csv()` - reads the csv files uploaded to make it the DataFrame.

# **A. POSITIONAL AND LABEL-BASED SLICING**
 
   ***a.1. Display the shape and complete list of column names of cars***
    
   • `cars.shape` - Shows the shape of the table which are the total numbers of rows and columns.

   • `.columns` - Displays only the columns name labels of the DataFrame.
     
   ***a.2. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the datasets, where the first data row is row 1.***
   
   • `.iloc[5:10]` - Specifically locate for rows 6 to 10 starting from the number one index in python which is 0, so starting from index 6 (row 5) and ending with index 10 (row 9). In this case, the code is built `5:10` because in slicing the last index number is not included. 
   
   ***a.3. From cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order.***

   • `cars_6_to_10[['Model', 'mpg', 'cyl', 'hp', 'gear']]` - Illustrates only the selected column labels.
  
# **B. MODEL LOOKUP**
Using Boolean indexing on the Model column to answer both requests.

   ***b.1. Display the complete row for Toyota Corolla and storing the result to "Toyota".***

   • `Toyota = cars.loc[cars['Model'] == 'Toyota Corolla']` - Locates and shows only the row for Toyota Corolla while storing it in the named `Toyota`.

   ***b.2. Display the selected row for Pontiac Firebird and storing the result to "Pontiac".***

   • `Pontiac = cars.loc[cars['Model'] == 'Pontiac Firebird']` - Locates and shows only the row for Pontiac Firebird while storing it in the named `Pontiac`.

   • `Pontiac = Pontiac [['Model', 'mpg', 'hp', 'wt']]` - Shows only the selected columns and their respective data about Pontiac Firebird.
    
# **C. MULTI-MODEL SUBSETTING**
Create a DataFrame named selected cars containing only the records for three models: Datsun 710, Lotus Europa, and Ferrari Dino.


```python
selected_cars = pd.DataFrame(cars[(cars ['Model'] == 'Datsun 710') | (cars ['Model'] == 'Lotus Europa') | (cars ['Model'] == 'Ferrari Dino')],
                             columns = ['Model', 'mpg', 'cyl', 'hp', 'gear'])
selected_cars
``` 

   • This codes create a new DataFrame from the cars.csv files named `selected_cars`. In this case, the models *Datsun 710*, *Lotus Europa* and *Ferrari Dino* are chosen. This code will only show the rows, columns and data respectively for the set models. 

   • `selected_cars.shape` - This will show the total number of rows and columns of the new DataFrame.
       

***Thank you for reading!***

To see the detailed and main python program for Program Assignment 3, please click this link: **https://github.com/abigailmacdon/ECE-2112-PA-3/blob/main/Programming_Assignment_3.ipynb** and download. Open on Jupyter Notebook or Colab Notebooks, then run all the cells.

**README file Version History:**

September 5, 2026
  - Initial README draft.

September 6, 2026
  - Finalizations of README File.
