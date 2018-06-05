# Python-for-Data-Science-and-Machine-Learning-Jose-Portilla-
(My Notes):
#Exercise 1 (Basics about Python):
Some basics about python
This notebook will just go through the basic topics in order:

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
# Format is arr_2d[row][col] or arr_2d[row,col]
arr_2d[1,0]

#Length of array
arr_length = arr2d.shape[1]

#Taking Square Roots#Taking  
np.sqrt(arr)

#Calcualting exponential (e^)
np.exp(arr)
