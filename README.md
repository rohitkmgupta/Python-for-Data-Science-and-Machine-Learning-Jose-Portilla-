# Python-for-Data-Science-and-Machine-Learning-Jose-Portilla-
(My Notes):
#Exercise 1 (Basics about Python):

Some basics about python: 
Data types
  Numbers : Operations ( +, -, *, /, **(power),%,); Variable Assignments : x= 2, z = x+y (cannot start a variable with number or special character)
  
  Strings: 'single quotes' , "wrap lot's of other quotes"
  
Printing : Print statement : print(x) , 

  Lists: 1. [1,2,3] ; append function to add/insert element at the end; index starts from 0.  
  Dictionaries : d  = {'key1':'item1','key2':'item2'}; d['key1']
  Booleans : True, False
  Tuples : They are immutable. 
  Sets : {1,2,3,4,5,6} (only unique values)
  
Comparison Operators: >,<,>=,<=,== , Logcal Opertors: and, or

if,elif, else Statements: 
Eg.
if 1 == 2:
    print('first')
elif 3 == 3:
    print('middle')
else:
    print('Last')
    
for Loops : Eg. 
seq = [1,2,3,4,5]
for item in seq:
    print(item)

while Loops
Eg. 
i = 1
while i < 5:
    print('i is: {}'.format(i))
    i = i+1
    
range() : function : range(5) : (0,5); list(range(5)) : [0,1,2,3,4]

list comprehension : Eg. [item**2 for item in x] %%Square each element in the list

functions: 
Eg.
def my_func(param1='default'):
    """
    Docstring goes here.
    """
    print(param1)
lambda expressions: "functions that are not bound to a name"

map and filter: Map applies a function to all the items in an input_list; filter creates a list of elements for which a function returns true.
seq = [1,2,3,4,5]
Eg. list(map(lambda var: var*2,seq)) %%Result: [2, 4, 6, 8, 10]
list(filter(lambda item: item%2 == 0,seq)) %%Result: [2, 4]

methods:
for strings: lower(), upper(), split()
dictionaries: keys(),items()
list : pop()
in function: 'x' in [1,2,3] %%Result : False

'x'  in['x','y','z'] %%Result: True

Numpy: 
-the fundamental package for scientific computing with Python
-almost all of the libraries in the PyData Ecosystem rely on NumPy as one of their main building blocks.
-used as an efficient multi-dimensional container of generic data. (Detailed Reference: http://www.numpy.org/)

Import Statement: import numpy as np

Built-in methods:
1. arange: Return evenly spaced values within a given interval.
Eg. np.arange(0,10)
array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
np.arange(0,10,2) ## 2 specifies interval
array([ 0,  2,  4,  6,  8, 10])

2. zeroes and ones: Generate arrays of zeros or ones
Eg. np.zeros(3)
array([ 0.,  0.,  0.])
np.ones(3,3)
array([[ 1.,  1.,  1.],
       [ 1.,  1.,  1.],
       [ 1.,  1.,  1.]])

3. linspace : Return evenly spaced numbers over a specified interval.
Eg.  np.linspace(0,10,3) 
array([  0.,   5.,  10.])

4. eye: Creates an identity matrix
Eg. np.eye(4)
array([[ 1.,  0.,  0.,  0.],
       [ 0.,  1.,  0.,  0.],
       [ 0.,  0.,  1.,  0.],
       [ 0.,  0.,  0.,  1.]])
 
5. rand: Create an array of the given shape and populate it with random samples from a uniform distribution over [0, 1).
Eg. np.random.rand(5,5)
array([[ 0.70154515,  0.22441999,  1.33563186,  0.82872577, -0.28247509],
       [ 0.64489788,  0.61815094, -0.81693168, -0.30102424, -0.29030574],
       [ 0.8695976 ,  0.413755  ,  2.20047208,  0.17955692, -0.82159344],
       [ 0.59264235,  1.29869894, -1.18870241,  0.11590888, -0.09181687],
       [-0.96924265, -1.62888685, -2.05787102, -0.29705576,  0.68915542]])
       
6. randint: Return random integers from low (inclusive) to high (exclusive).
Eg. np.random.randint(1,100,10)
array([13, 64, 27, 63, 46, 68, 92, 10, 58, 24])

7. Reshape: Returns an array containing the same data with a new shape.
Eg. arr.reshape(5,5)
array([[ 0,  1,  2,  3,  4],
       [ 5,  6,  7,  8,  9],
       [10, 11, 12, 13, 14],
       [15, 16, 17, 18, 19],
       [20, 21, 22, 23, 24]])
 
8. max,min,argmax,argmin
These are useful methods for finding max or min values. Or to find their index locations using argmin or argmax

9. Shape: Shape is an attribute that arrays have (not a method):
10. dtype: You can also grab the data type of the object in the array.
Eg. arr.dtype
dtype('int64')

Bracket Indexing and Selection:
#Get a value at an index
arr[8]
#Get values in a range
arr[1:5]
#Important notes on Slices
slice_of_arr = arr[0:6]

2D Array:
arr_2d = np.array(([5,10,15],[20,25,30],[35,40,45]))
#Indexing row
arr_2d[1]

#Format is arr_2d[row][col] or arr_2d[row,col]
arr_2d[1,0]

#Length of array
arr_length = arr2d.shape[1]

#Taking Square Roots#Taking  
np.sqrt(arr)

#Calcualting exponential (e^)
np.exp(arr)
 
Pandas:
- https://pandas.pydata.org/
-an open source, BSD-licensed library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language. 

Import Statement: import pandas as pd

1. Series: A Series is very similar to a NumPy array (in fact it is built on top of the NumPy array object). What differentiates the NumPy array from a Series, is that a Series can have axis labels, meaning it can be indexed by a label, instead of just a number location. It also doesn't need to hold numeric data, it can hold any arbitrary Python Object.

Converting a list, numpy array and a dictionary to Series: 
a. pd.Series(data=my_list) ##list 
b. pd.Series(arr)  ##numpy array
c.pd.Series(d) ##dictionary

Eg. ser1 = pd.Series([1,2,3,4],index = ['USA', 'Germany','USSR', 'Japan'])
ser1['USA']
Result: 1

2. DataFrames: DataFrames are the workhorse of pandas and are directly inspired by the R programming language. We can think of a DataFrame as a bunch of Series objects put together to share the same index. 
Creating a random dataframe:
df = pd.DataFrame(randn(5,4),index='A B C D E'.split(),columns='W X Y Z'.split())

Columns: df['W'], df[['W','Z']], df.W, 
Creating a new Column : df['new'] = df['W'] + df['Y']
Removing Columns: df.drop('new',axis=1,inplace=True)
Selecting Rows: df.loc['A']
df.loc[['A','B'],['W','Y']]
Conditional Selection: df[df>0]

Dropping NaN values: df.dropna() ; df.dropna(axis=1); df.dropna(thresh=2)
Filling Values: df.fillna(value='FILL VALUE'); df['A'].fillna(value=df['A'].mean())

GroupBy: df.groupby('Company'); df.groupby('Company').mean(); by_comp.describe().transpose()

Concat: pd.concat([df1,df2,df3]); pd.concat([df1,df2,df3],axis=1)
Join: 
Eg. left = pd.DataFrame({'A': ['A0', 'A1', 'A2'],
                     'B': ['B0', 'B1', 'B2']},
                      index=['K0', 'K1', 'K2']) 

right = pd.DataFrame({'C': ['C0', 'C2', 'C3'],
                    'D': ['D0', 'D2', 'D3']},
                      index=['K0', 'K2', 'K3'])
left.join(right)
left.join(right, how='outer')

Unique Values: df['col2'].unique(); df['col2'].nunique() ##Number of Unique Values
Sorting Values: df.sort_values(by='col2') #inplace=False by default

CSV: df = pd.read_csv('example'); df.to_csv('example',index=False)
Excel: pd.read_excel('Excel_Sample.xlsx',sheetname='Sheet1'); df.to_excel('Excel_Sample.xlsx',sheet_name='Sheet1')
Read HTML: df = pd.read_html('http://www.fdic.gov/bank/individual/failed/banklist.html')

SciPy : SciPy is a collection of mathematical algorithms and convenience functions built on the Numpy extension of Python. It adds significant power to the interactive Python session by providing the user with high-level commands and classes for manipulating and visualizing data. With SciPy an interactive Python session becomes a data-processing and system-prototyping environment rivaling systems such as MATLAB, IDL, Octave, R-Lab, and SciLab.

The additional benefit of basing SciPy on Python is that this also makes a powerful programming language available for use in developing sophisticated programs and specialized applications. Scientific applications using SciPy benefit from the development of additional modules in numerous niches of the software landscape by developers across the world.

Everything from parallel programming to web and data-base subroutines and classes have been made available to the Python programmer. All of this power is available in addition to the mathematical libraries in SciPy.

Linear Algebra: 
from scipy import linalg
#Compute Determinant of a Matrix:
linalg.det(A)

