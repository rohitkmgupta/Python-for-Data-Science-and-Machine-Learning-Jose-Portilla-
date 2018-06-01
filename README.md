# Python-for-Data-Science-and-Machine-Learning-Jose-Portilla-

#Excecise 1 (Basics about Python):
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
