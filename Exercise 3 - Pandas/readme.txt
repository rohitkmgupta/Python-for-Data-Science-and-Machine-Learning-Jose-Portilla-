My Notes: 
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

 



