## Interactive Programming
### input()
```python
input() #prompts the user for input, evaluates and returns whatever the user enters
```
>[!warning]
>*Always returns a string!*

## Conditional Branching
### if...else
```python
#formatting for if...else statements

if condition:

statement_if_true1

statement_if_true2

statement_if_true3

...

else:

statement_if_false1

statement_if_false2

...

statement_regardless1

statement_regardless2

```

### if...elif...else
```
## Interactive Programming
### input()
```python
input() #prompts the user for input, evaluates and returns whatever the user enters
```
>[!warning]
>*Always returns a string!*

## Loops
### while

```python
# Counting from 0 to 20
counter = 0
while counter < random_integer:
	...
```
### for
```python
for item in list:
	...
```
### for...range
```python
for item in range(n)
	...
```

## Modules/Packages
### Importing
```python
import module_name
```

```python
#renames the imported module as x within the project
import module_name as x
```

```python
#imports a specific function from a module and renames it
from module_name import function_name as renamed_function_name
```
### Numpy
```python
import numpy as np
```
#### Arrays
```python
a = np.array[...]
```
##### Zero Arrays
```python
np.zeros(n) #creates an array of zeros with length n
np.zeros((a,b)) # creates a matrix of zeros with dimensions a * b
```
#### Methods/Operations
##### .shape()
```python
print(a.shape) #returns the dimensions of an array in a tuple (x, y)
```
##### .arange()
```python
#creates an array within the intervals a and b, with the optional additional argument of n as steps (defaults to 1)
np.arange(a, b, n)
```
##### .linspace()
```python
#creates an array within intervals a and b, while spacing n number of points between a and b
np.linspace(a, b, n)
```
##### Operators
```run-python
import numpy as np

v1 = np.array([1, 2, 3])
v2 = np.array([4,5,6])

print(v1 + v2)
print(v1 - v2)
print(v1 * v2)
print(v1 / v2)
print(v1 @ v2) #matrix multiplication
```

#### Slicing
```run-python
import numpy as np

v1 = np.array([1, 2, 3])

print(v1[1:2])
print(v1[1:])
print(v1[:1])

v2 = np.array([[1, 2, 3],[4, 5, 6],[7, 8, 9]])

print(v2[:, 1:])
```
### Matplotlib
```python
import matplotlib.pyplot as plt
```
#### Methods
##### .plot()
```python
#creates a visual lineplot, "zipping" values from x and y to create the points
plt.plot(x, y)

#creates a scatterplot by adding the third argument of 'O'
plt.plot(x, y, 'o')
```
##### .legend()
```python
#creates a legend for the plot
plt.plot(...)
plt.legend()
```
##### .title()
```python
#creates a title the plot based on the string argument provided
plt.plot(...)
plt.title(a)
```
##### .grid()
```python
#adds a grid to the plot based on the boolean argument provided (defaults to False)
plt.grid(a)
```
##### .bar()
```python
#creates a barchart with labels in x and heights in y
plt.bar(x, y)
```
##### .hbar()
```python
#similar to plt.bar(), escept with a horizontal bar
plt.hbar(x, y)
```
##### .xlabel()
```python
#adds a label s to the x-axis with font size n
plt.bar(...)
plt.xlabel(s, n)
```
##### .ylabel()
```python
#adds a label s to the y-axis with font size n
plt.bar(...)
plt.ylabel(s, n)
```
##### .style.available
```python
# prints a list of available style schemes in the matplotlib package
plt.style.available
```
##### plt.style.use()
```python
#takes in a string argument and changes the style of the plot to such
plt.style.use(a)
```
##### .tick_params()
```python
#takes in an argument for which axis to act upon, and another  (n) defining label size, which then formats the plot
plt.tick_params(axis = "...", labelsize = n)
```
##### .style.available
```python
#prints a list of available plotting styles, including different color schemes
plt.style.available
```
##### .style.use
```python
#takes in the string of the name of a style used in python, and applies it to the plot being created
plt.style.use("...")
```
### Pandas
```python
import pandas as pd
```
#### .Series()
```python
#creates a Series object by taking in a list of objects of a single type
s = pd.Series([...])
```

```python
#returns a list of elements based on the indexes defined in the list provided
s[[...]]
```
##### Series Methods
###### .index
```python
#returns the index values
s.index
```
###### .values
```python
#returns the pandas object values
s.values
```
###### .mean()
```python
#finds the mean of a Series
s.mean()
```
###### .max()
```python
#calculates the max of a Series
s.max()
```
###### .idxmax()
```python
#similar to max, except instead of giving the value of the Series it returns the index of the max value
s.idxmax()
```
#### .DataFrame()
```python
#creates a DataFrame object by taking in an array, and two lists of strings labeled index (row names) and column (names)
d = pd.DataFrame(array, index = list1, columns = list2)
```
##### DataFrame Methods
###### .read_csv()
```python
#reads a csv file by taking in the file name/path, as well as a label for the first column (of names)
d = pd.read_csv("path_name", index_col = "...")
```
###### .head()
```python
#displays only the first few rows of a DataFrame
d.head()
```
###### .sort_values()
```python
#sorts a DataFrame's rows by the column (labeled by "by"), and ordered either descending or ascending (labeled by "ascending")
d.sort_values(by = "column_name", ascending = Boolean)
```
###### .loc\[\]
```python
#grabs rows from a DataFrame by taking the name of the row as an argument
d.loc["row_name"]

#or grabs a value in the DataFrame by taking the name of the row and column as an argument
d.loc["row_name", "column_name"]
```
###### .iloc\[]
```python
#similar to .loc[], but instead works by instead indexing the table
d.iloc[row_index, column_index]
```
###### Slicing
```python
d["row_name", ["column_names", ...]]
```
###### Indexing (with Conditions)
```python
(d["column_name"] == boolean)
```
###### .describe()
```python
#prints an overview of the minimum/maximums, means, medians, standard deviations, and/or percentiles of the dataframe
d.describe()
```
###### .corr()
```python
#returns the correlation of a dataframe with an optional argument (labeled numeric_only)
d.corr(numeric_only = Boolean)
```
###### .columns
```python
#returns the columns' labels
d.columns
```
###### .dtypes
```python
#returns the types within each column
d.dtypes
```
###### .map()
```python
#maps a function (that takes a single argument) to a Series, resulting in a new Series
df.map(function)
```
###### .to_numeric()
```python
#converts a Series (or Dataframe column) ot numeric
pd.to_numeric(Series/df_column)
```
###### .astype()
```python
#more general function that takes in the desired type (as a string) and converts a Series/Dataframe column as the desired type
df["col_name"].astype("desired_type")
```
###### .isnull()
```python
#returns the values that are null per column
df.isnull()
```
###### .dropna()
```python
#drops the null values, (any/all = if any/all value(s) is null in row/col, remove the row/col)
df.dropna(axis=0, how="any/all")
```
###### .iterrows()
```python
#used to iterate through the rows of a dataframe, as such:
for index, row in df.iterrows():
	...
```
###### .hist()
```python
#creates a histogram with bins' number of bars from a Series or Dataframe col
df["col_name"].hist()
```
###### .boxplot()
```python
#similar to hist, except makes boxplots instead of hist()
df["col_name"].boxplot()
```
###### .read_csv()
```python
#reads a csv file into a dataframe
df = pd.read_csv("filename", names = string_list_of_column_names)
```
###### to_csv()
```python
#writes a dataframe file to csv
df.to_csv("filename")
```
### Regular Expressions
```python
import re
r""
```
#### Methods
##### .search()
```python
#takes in two strings, a and b, and returns a if it is found within b, otherwise returns None
re.search(a, b)
```
##### .group()
```python
#takes a match object and returns the string that was found
match.group()
```
##### find()
```python
#works with the same arguments similar to search, except instead of just finding the first match, it looks through the entire target string and returns a list of matches
re.findall()
```
### CSV
```python
import csv
```

#### with/open/reader/writer
```python
#"cleans up everything in the object once its indented block is done" 

#with open takes a file name string, as well as a string (labeled as mode) and returns the file object if it is found, with permission to perform mode (ex. read = "r", write = "w", etc etc)
with open(filename, mode = "r/w") as my_csv:
#reads my_csv file and returns a reader file
	reader = csv.reader(my_csv)
	...
#or alternatively, one can create a writer object that is used when the mode is in "w"
	writer = csv.writer(my_csv)
```
### JSON
```python
import json
```
#### .dump()
```python
#writes a JSON object to file
with open(filename, mode= "w") as my_json:
	dictionary = {}
	json.dump(dictionary, my_json)
```
#### .load()
```python
#reads a json file into a dictionary
with open(filename, mode = "r") as my_json:
	dictionary = json.load(my_json)
```
### SciKit
```python
import sklearn
```
#### KNeighborsClassifier
```python
#A class hat classifies using the K-nearest neighbors strategy, where n_neighbors speciifies the number of neighbors to consider in its classification process (see lecture 22)
knn = KNeighborsClassifier(n_neighbors = k)
```
##### .fit()
```python
#a KNeihborsClassifier object method, it takes in the digits data (x_train) and the targets for the training (y_train)
knn.fit(x_train, y_train)
```
##### .score()
```python
#another KNeighborsClassifier object method, it computes the mean score based on the given parameters and the object itself
knn.score(x_train, y_train)
```
#### Train/Test Split

```python
#splits training data x any y into training and testing data based on what percent test_size is set to
data_train, data_test, label_train, label_test = train_test_split(x_train, y_train, test_size = int_zero_to_one, random_state = seed)
```
#### Cross-Validation
```python
#takes in the k-nearest neighhbors function in question, as well as its data train and label train and cross-validates it across five examples (80-20, 60+20-20, 40-)
cross_val_score(knn_object, data_train, label_train)
```
#### DecisionTreeClassifier
```python
dtree = DecisionTreeClassifier(criterion = "entropy", random_state = n)
```
##### .fit()
```python
dtree.fit(train_data, labels_train)
```
##### .score()
```python
dtree.score(train_test, labels_test)
```
##### .plot_tree()
```python
tree.plot_tree(dtree, feature_names = data.feature_names, class_names = data.target_names)
```
#### LinearRegression
```python
linear_model = LinearRegression()
x = x.reshape(-1,1)
linear-model.fit(x,y)
y_hat = linear_model.predict(x)
```
##### .coef_
```python

```
### Random
```python
import random
```
#### randInt()
```python
#takes in two integers and outputs 
```
### SQLite
```python
import sqlite3
```

#### Methods
##### connect
##### read_sql
```python
#reads a 
```

## Tuples
```python
my_tuple = (...,...,...,...)


...,...,... = my_tuple
```
## Functions
```python
def add_an_s(string):
    new_string = string + 's'
    return new_string

add_an_s('example')
```
## Dictionaries
```python
my_dict = {}
```
### Inserting Key-Value Pairs
```python
my_dict = {}

my_dict["key"] = value
```
### Methods
#### get()
```python
my_dict.get("key", value) # returns value parameter

my_dict.get("key") # returns value of key, but can also return KeyError if key does not exist
```
#### items()
```python
my_dict.items() # returns a view object that reflects the changes in the dictionary
```
### Iteration
```python
for ... in worddict.items(): # important to call the items() method to generate iterable key/value pairs
	...
```
## Sets
```python
my_set = {"key"}
```
### Methods
#### add()
```python
my_set.add("key") # adds a new key to the set
```
## Formatted Strings
```python
#a formatted string always has an f before the ""
s = f"..."{}"..."

#something like a double can go in between the brackets
```

```python
my_cost = 12.95821

print(f'The total cost was {my_cost:.2f} dollars')
# where :.(n)f gives n places after a decimal place
```
## Strings

### Methods
#### .split()
```python
#a string is split wherever a appears, and takes the split strings to make a list of strings
s.split(a)
```
#### .join()
```python
#takes a list of strings, and joins them using s as a delimiter
s.join(l)
```
#### .strip()
```python
#gets rid of the empty space on either end of a string
s.strip()
```
#### .splitlines()
```python
#splits a string into a list of strings based on the \n escape character
s.splitlines()
```
#### .startswith()
```python
#returns a boolean based on whether a string contains the string a in string s
s.startswith(a)
```

### Escape Characters
#### \n
```python
#\n: new line
print("string\nstring")
```
#### \t
```python
#\t: tab character
print("string\tstring")
```
#### \\\
```python
#\\: backslash (useful when you actually want to print "\n")
print("\n")
print("\\n")
```
## Exceptions
### try/except
```python
#try comes before e a block of code to catch an esception that may occur within said block. if an exception is caught, it jumps to an block of code marked by except. at the end, else blocks can then be executed if no exceptions are caught.

try:
	...
except Exception_Object:
	...
else: #happens when no exceptions occur
	...
finally: #happens regardless of exceptions
	...
```
### raise
```python
#raises an exception
raise ...
```
#### ValueError()
```python
#raises an ValueError, meaning the data type is correct, but not within the range scope of the method
raise ValueError(exception_string)
```

## Classes/Objects
```python
class A
	...
```

```python
class subclass(parent_class)
	...
```

```python
#used to refer to the parent class
super()
```
### Attributes
```python
Class.attribute = ...
```

## Data Structures
### Lists

#### Creating Lists

```python
#using array notation/bracket notation
my_list = [...,...,...,...]

#creating empty lists
my_list = []
```
#### List Comprehension
```python
my_list = [x ... for x in ... if ... else ...]
```
#### Methods
##### .append()

```run-python
my_list = [1, 2, 3]
print(my_list)

my_list.append(4)
print(my_list)
```
##### Concatenation
```python
#using the + operator
new_list = old_list_1 + old_list_2
```
##### Indexing
```run-python
my_list = ["a", "b", "c"]

print(my_list[2])
```
>[!important]
>*If the first item in a list or string has index 0 instead of 1, then taht shifts the index of everything else as well; the second item has index 1, the third item has index 2, and so on down to the last item, which has index len(my_list) - 1*

>[!warning]
>*Trying to index the list at index len(my_list) results in an error*

##### .sort()
```run-python
my_list = [3, 2, 1]
my_list.sort() #sorts the list, but doesn't return anything

print(my_list)

```
##### .copy()
```run-python
my_list1 = [3, 2, 1]
my_list2 = my_list1.copy()

#creates a new copy of a list with a new address
my_list1.sort()

print(my_list1)
print(my_list2)
```

### Linked Lists
```python
class ll_node:
  def __init__(self, num):
    self.number = num
    self.next = None

  def append(self, num):
    if self.next == None:     # End of the list - add the node
      self.next = ll_node(num)
    else:
      self.next.append(num) # Recursively append to rest of list
    
  def contains(self, othernum):
    if self.number == othernum:  # We found it
      return True
    elif self.next == None:  # We reached the end, didn't find it
      return False
    # Not here, there's more list - so, keep looking (recursively)
    return self.next.contains(othernum)

  def __str__(self):
    if self.next == None:  # Last number
        return str(self.number)
    # Print this and print the rest (more recursion)
    return str(self.number) + ' ' + str(self.next)
```
### Dynamic Arrays (Lists)
```python
import numpy as np

class dynamic_array:  # Showing how Python lists work
  def __init__(self, initial_size):
    self.memory = np.zeros(initial_size)
    self.occupied = 0
    self.size = initial_size

  def __str__(self):
    return str(self.memory)
  
  def append(self, val):
    if self.occupied == self.size:
      print('Resizing...')
      new_memory = np.zeros(self.size*2)
      # A "hiccup" in running time as everything's copied
      for i in range(len(self.memory)): 
        new_memory[i] = self.memory[i] 
      self.memory = new_memory
      self.size = self.size*2
    print('Adding ' + str(val))
    self.memory[self.occupied] = val
    self.occupied += 1
```
### Trees 
#### Binary Trees
```python
class BinaryTree:
  # binary left and right are its fields
  def __init__(self, val):
    self.left = None
    self.right = None
    self.val = val
  
  def addLeft(self, node):
    self.left = node
  
  def addRight(self, node):
    self.right = node
  
  def find(self, v):
    if self.val == v:
      return True
    # "if self.left" is checking that self.left exists - 
    # else error when we run self.left.find()
    if self.left and self.left.find(v):
      return True
    if self.right and self.right.find(v):
      return True
    return False
```
### 
## Sorting
### Insertion

```python
def insertion_sort(A):
	for j = 1 to length(A):
		key = A[j]
		i = j - 1
		
		while i > 0 and A[i] > key:
			A[j + 1] = A[i]
			i = i-1
		A[i+1] = key
	return A
```
### Mergesort
```python
def merge(L1, L2):
	result = list()

	while(True):
		if not L1:
			return result + L2
		if not L2:
			return result + L2
		if L1[0] > L2[0]:
			result.append(L1[0])
			L1 = L1[1:]
		else:
			result.append(L2[0])
			L2 = L2[1:]
			

def mergesort(A):
	if |L| = 1 or |L| = 0:
		return L
	return merge(mergesort(left), mergesort(right))
```
### 
## 
## Other Functions
### len()
```python
#gets the length of objects
len()
```

### Boolean Operators
```python

if condition1 and condition2 #both conditions must be true for the expression to evaluate to true
	...

if condition1 or condition2 #either condition must be true for the expression to evaluate to true
	...

if not condition1 #the condition must be false to be true, and vice-versa
```
### zip()
```python
zip(list1, list2, ...) #creates a list of tuples from two different lists
```
### copy()
```python
my_object.copy() # for objects stored by reference, created a new copy of the copied object
```
### isinstance()
```python
# takes in an object and a class, and checks if the object is an instance of said class
isinstance(object, Class)
```
### pass
```python
#used as a placeholder for future code
def ...:
	pass

class ...:
	pass
```
