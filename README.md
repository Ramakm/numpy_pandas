
l = [4,5,6,2,41,2,5]


import numpy as np

arrary = np.array(l)

np.array(arrary*3)
array([ 12,  15,  18,   6, 123,   6,  15])
# Numpy
heights = [54,24,65,23,569,78,42]

heights *2
[54, 24, 65, 23, 569, 78, 42, 54, 24, 65, 23, 569, 78, 42]
# pip install numpy

import numpy as np

np_heights = np.array([54,24,65,23,569,78,42])

type(np_heights)
numpy.ndarray
np_heights * 2.35
np_heights
array([ 54,  24,  65,  23, 569,  78,  42])
#Numpy with its own sets of methods and operations

list1 = [1, 2, 3]

list2 = [4,5,6]

list1 + list2
[1, 2, 3, 4, 5, 6]
np1 = np.array([1, 2, 3])

np2 = np.array([7,8,9])

np1+np2
array([ 8, 10, 12])
# 1D Numpy Array
heights = [54 , 65, 85 ,96,47,75,67,53,64,55,22,44,65]

import numpy as np

heights_in = np.array(heights)

heights_in
array([54, 65, 85, 96, 47, 75, 67, 53, 64, 55, 22, 44, 65])
type(heights_in)
numpy.ndarray
# Count the no of participants in that numpy array
len(heights_in)
13
#OR

heights_in.size
13
#OR 

heights_in.shape
(13,)
# Converting a list to Numpy array and converting Lb to Kg without using a Loop

weights_lb = [182,165,142,175,186,164,152,153,154,162,156,145,155]
weights_in_kg = np.array(weights_lb) * 0.4532

weights_in_kg
array([82.4824, 74.778 , 64.3544, 79.31  , 84.2952, 74.3248, 68.8864,
       69.3396, 69.7928, 73.4184, 70.6992, 65.714 , 70.246 ])
# Calculate BMI 

bmi = weights_in_kg /(heights_in**2)
bmi
array([0.02828615, 0.01769893, 0.00890718, 0.00860569, 0.03815989,
       0.0132133 , 0.0153456 , 0.0246848 , 0.01703926, 0.02427055,
       0.14607273, 0.03394318, 0.01662627])
# Sub-setting Numpy Arrays
bmi[0]
0.028286145404663923
bmi[-1]
0.01662627218934911
bmi[:5]
array([0.02828615, 0.01769893, 0.00890718, 0.00860569, 0.03815989])
bmi[:-5]
array([0.02828615, 0.01769893, 0.00890718, 0.00860569, 0.03815989,
       0.0132133 , 0.0153456 , 0.0246848 ])
# Conditional sub-Setting Array
bmi  <0.025
array([False,  True,  True,  True, False,  True,  True,  True,  True,
        True, False, False,  True])
bmi [bmi<0.025]
array([0.01769893, 0.00890718, 0.00860569, 0.0132133 , 0.0153456 ,
       0.0246848 , 0.01703926, 0.02427055, 0.01662627])
underweight_players = bmi [bmi<0.025] #Storing the value in a Numpy Array
underweight_players.size #No of players whose are underweight_players
9
# Numpy Functions:
# Find largest BMI value

max(bmi)
0.14607272727272727
bmi.max()
0.14607272727272727
bmi.min()
0.00860568576388889
bmi.sum()
0.39285352236666526
# Extracting Elements from Array
# Description
# From a given array, extract all the elements which are greater than 'm' and less than 'n'. Note: 'm' and 'n' are integer values provided as input.

# Input format:

# A list of integers on line one

# Integer 'm' on line two

# Integer 'n' on line three

# Output format:

# 1-D array containing integers greater than 'm' and smaller than 'n'.

# Sample input:

# [ 1, 5, 9, 12, 15, 7, 12, 9 ] (array)

# 6 (m)

# 12 (n)

# Sample output:

# [ 9 7 9 ]

# Sample input:

# [ 1, 5, 9, 12, 15, 7, 12, 9 ]

# 12

# 6
# Sample output:

# [ ]
input_list = list(map(int,input().split()))
m=int(input())
n=int(input())

import numpy as np
array_1 = np.array(input_list)
final_array = array_1[(array_1>m) & (array_1<n)]

print(final_array)
5 4 2 6 12 85
2
12
[5 4 6]
# Multidimensional Arrays
players = [(74,180), (74,215),(72,210), (72,210),(73,188), (69,176),(69,180)]

len(players)
7
import numpy as np

np_players = np.array(players)
np_players
array([[ 74, 180],
       [ 74, 215],
       [ 72, 210],
       [ 72, 210],
       [ 73, 188],
       [ 69, 176],
       [ 69, 180]])
np_players.size
14
#Structure of the array

np_players.shape
(7, 2)
# Dimenssion of the array

np_players.ndim
2
#data type of the elements in the array

np_players.dtype
dtype('int64')
#Print the size of the single item of array
np_players.itemsize
8
# shape: It represents the shape of an array as the number of elements in each dimension.

# ndim: It represents the number of dimensions of an array. For a 2D array, ndim = 2.
# conert heights to meter and weights to Kgs
players_converted = np_players * [0.0254, 0.4532]

players_converted
array([[ 1.8796, 81.576 ],
       [ 1.8796, 97.438 ],
       [ 1.8288, 95.172 ],
       [ 1.8288, 95.172 ],
       [ 1.8542, 85.2016],
       [ 1.7526, 79.7632],
       [ 1.7526, 81.576 ]])
# In NumPy, the dimension is called axis. In NumPy terminology, for 2-D arrays:

# axis = 0 - refers to the rows
# axis = 1 - refers to the columns
# Fetch first row of the 2D array

players_converted[0]
array([ 1.8796, 81.576 ])
# First row and 2nd element of the array

players_converted[0][1]
81.576
If you want column of a numpy array
players_converted[rows,columns]
players_converted[:,0]  #Giving me all the  value of 1st column in numpy array
array([1.8796, 1.8796, 1.8288, 1.8288, 1.8542, 1.7526, 1.7526])
Fetch height of the(1st column) of 5th player from array
players_converted[6][0]
1.7526
Which of the following would extract all the rows of the first 3 columns in a 2D array?
array_name[ : , :3]

array_name[:,:3] extracts all the rows of the first 3 columns. Note that even though the first 3 columns have the indices 0, 1, and 2, respectively, we need to mention array_name[:,:3]instead of array_name[:,:2] since the last column index mentioned is not included, i.e., array_name[:,:2] will give you just the first two columns, i.e., 0 and 1.

##### The indexing and slicing of nD arrays are similar to those of 1D arrays. 
##### The only difference between the two is that you need to give the slicing
##### and indexing instructions for each dimension separately. See example below:
players_converted[:, 0]
array([1.8796, 1.8796, 1.8288, 1.8288, 1.8542, 1.7526, 1.7526])
# Conditional Sub-setting
# fetch the height of the players whose height is more than 1.8m

tall_players = players_converted[players_converted[:,0]>1.8]

tall_players
array([[ 1.8796, 81.576 ],
       [ 1.8796, 97.438 ],
       [ 1.8288, 95.172 ],
       [ 1.8288, 95.172 ],
       [ 1.8542, 85.2016]])
tall_players.shape
(5, 2)
skills = np.array(["Keeper","Batsman", "Bowler", "Bowler", "Batsman", "Weicket-keeper", "Bowler" ])

skills
array(['Keeper', 'Batsman', 'Bowler', 'Bowler', 'Batsman',
       'Weicket-keeper', 'Bowler'], dtype='<U14')
#Fetch Heights of the batsman

batsman = players_converted[skills=="Batsman"]

batsman
array([[ 1.8796, 97.438 ],
       [ 1.8542, 85.2016]])
batsman.shape
(2, 2)
batsman[:,0]  #Batsman with heights and skills is Batsman
array([1.8796, 1.8542])
# size of the array beforehand:

# np.ones(): It is used to create an array of 1s.
# np.zeros(): It is used to create an array of 0s.
# np.random.randint(): It is used to create a random array of integers within a particular range.
# np.random.random(): It is used to create an array of random numbers.
# np.arange(): It is used to create an array with increments of fixed step size.
# # np.linspace(): It is used to create an array of fixed length.
import numpy as np
# creating 1D array
arr = np.ones(10, dtype = int)

arr
array([1, 1, 1, 1, 1, 1, 1, 1, 1, 1])
arr = np.ones((5,3), dtype = int)
arr
array([[1, 1, 1],
       [1, 1, 1],
       [1, 1, 1],
       [1, 1, 1],
       [1, 1, 1]])
arr2 = np.zeros((5,3), dtype = int)
arr2
array([[0, 0, 0],
       [0, 0, 0],
       [0, 0, 0],
       [0, 0, 0],
       [0, 0, 0]])
# range in numpy array is arange()
np.arange(3)
array([0, 1, 2])
np.arange(3.0)
array([0., 1., 2.])
# range of 3 to 35 with a step count 2
np.arange(3,36, 2)
array([ 3,  5,  7,  9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35])
# Arry of Random Numbers using random module:
np.random.randint(2,size = 10) #maximum integer value is 2 and total no of elements =10
array([0, 1, 1, 0, 0, 1, 0, 1, 1, 1])

np.random.randint(5, size =10)
array([4, 3, 2, 1, 3, 0, 1, 0, 2, 1])
np.random.randint(5,9, size =10) # 5 is lower value and 9 is higher value but 5 included not 9
array([7, 8, 6, 8, 7, 8, 5, 5, 8, 5])
# 2D array of random numbers
np.random.random([3,4] )  #random.random used to create a 2D array
array([[0.97356465, 0.59703111, 0.16405859, 0.12186255],
       [0.37283301, 0.17355727, 0.53864877, 0.03241622],
       [0.14916137, 0.31398436, 0.3451915 , 0.62095899]])
Sometimes you know length of array but not the step size.

Array of length 20 between 1 and 10


np.linspace(1,10,20)
array([ 1.        ,  1.47368421,  1.94736842,  2.42105263,  2.89473684,
        3.36842105,  3.84210526,  4.31578947,  4.78947368,  5.26315789,
        5.73684211,  6.21052632,  6.68421053,  7.15789474,  7.63157895,
        8.10526316,  8.57894737,  9.05263158,  9.52631579, 10.        ])
n = int(input())

import numpy as np

border_array = np.ones((n, n), dtype = int)
border_array[1:-1, 1:-1] = 0
print(border_array)
5
[[1 1 1 1 1]
 [1 0 0 0 1]
 [1 0 0 0 1]
 [1 0 0 0 1]
 [1 1 1 1 1]]
np.full(): It is used to create a constant array of any number ‘n’.

np.tile(): It is used to create a new array by repeating an existing array for a particular number of times.

np.eye(): It is used to create an identity matrix of any dimension

NUMPY

LIVE LECTURE IN NUMPY

from calendar import*

year = int(input("Enter a new Year:"))

print(calendar(year,3,1,8,4))

# 2 = 2 characters for days (Mo,Tu, etc)
# 1 = 1 line (row) for each week
# 8 = 8 rows for each month
# 4 = 4 columns for all months of the year.
Enter a new Year:2022
                                                                2022

          January                            February                            March                              April
Mon Tue Wed Thu Fri Sat Sun        Mon Tue Wed Thu Fri Sat Sun        Mon Tue Wed Thu Fri Sat Sun        Mon Tue Wed Thu Fri Sat Sun
                      1   2              1   2   3   4   5   6              1   2   3   4   5   6                          1   2   3
  3   4   5   6   7   8   9          7   8   9  10  11  12  13          7   8   9  10  11  12  13          4   5   6   7   8   9  10
 10  11  12  13  14  15  16         14  15  16  17  18  19  20         14  15  16  17  18  19  20         11  12  13  14  15  16  17
 17  18  19  20  21  22  23         21  22  23  24  25  26  27         21  22  23  24  25  26  27         18  19  20  21  22  23  24
 24  25  26  27  28  29  30         28                                 28  29  30  31                     25  26  27  28  29  30
 31

            May                                June                               July                              August
Mon Tue Wed Thu Fri Sat Sun        Mon Tue Wed Thu Fri Sat Sun        Mon Tue Wed Thu Fri Sat Sun        Mon Tue Wed Thu Fri Sat Sun
                          1                  1   2   3   4   5                          1   2   3          1   2   3   4   5   6   7
  2   3   4   5   6   7   8          6   7   8   9  10  11  12          4   5   6   7   8   9  10          8   9  10  11  12  13  14
  9  10  11  12  13  14  15         13  14  15  16  17  18  19         11  12  13  14  15  16  17         15  16  17  18  19  20  21
 16  17  18  19  20  21  22         20  21  22  23  24  25  26         18  19  20  21  22  23  24         22  23  24  25  26  27  28
 23  24  25  26  27  28  29         27  28  29  30                     25  26  27  28  29  30  31         29  30  31
 30  31

         September                           October                            November                           December
Mon Tue Wed Thu Fri Sat Sun        Mon Tue Wed Thu Fri Sat Sun        Mon Tue Wed Thu Fri Sat Sun        Mon Tue Wed Thu Fri Sat Sun
              1   2   3   4                              1   2              1   2   3   4   5   6                      1   2   3   4
  5   6   7   8   9  10  11          3   4   5   6   7   8   9          7   8   9  10  11  12  13          5   6   7   8   9  10  11
 12  13  14  15  16  17  18         10  11  12  13  14  15  16         14  15  16  17  18  19  20         12  13  14  15  16  17  18
 19  20  21  22  23  24  25         17  18  19  20  21  22  23         21  22  23  24  25  26  27         19  20  21  22  23  24  25
 26  27  28  29  30                 24  25  26  27  28  29  30         28  29  30                         26  27  28  29  30  31
                                    31

#Python test

import sys

num =6

print(sys.getsizeof(num), 'bytes')
28 bytes
#Numpy test

import numpy as np

list1 = [4,56,6,4,879,85]
myarr = np.array(list1) #it will return you 1 single element ND array

print(myarr.itemsize,'bytes')
8 bytes
import numpy as np

import time

size = 1000000

A1 = range(size)
A2 = range(size)

l1 = np.arange(size)
l2 = np.arange(size)

start = time.time()

result = [x+y for x,y in zip(A1,A2)]

stop = time.time()
print('Python took', (stop-start)*1000,'ms')

start = time.time()
result = l1 + l2
stop = time.time()

print('Numpy took', (stop-start)*1000,'ms')
Python took 145.4486846923828 ms
Numpy took 22.843599319458008 ms
input_List = list(map(int,input().split()))

input_List[0], input_List[-1] = input_List[-1], input_List[0]

print(input_List)
4 5 6 2 4 3
[3, 5, 6, 2, 4, 4]
import cv2
import numpy

mypic = cv2.imread('F:\100DaysOfCode\Header.jpg')
type(mypic)
numpy.array(mypic)
array(None, dtype=object)
WORKING WITH NUMPY ND ARRAY

import numpy as np

b = [[1,2,3], [4,5,6]]

b_arr = np.array(b)

b_arr
array([[1, 2, 3],
       [4, 5, 6]])
# N-D Array is a group of (N-1)-D array

# 3D array is a group of 2D array
b_arr[1,2]
6
b_arr[1][2]
6
b_arr[0,1]
2
Python to make border 1's and Inside elements 0's

import numpy as np

n = int(input("Enter the size of n: "))
    
border_array = np.ones((n,n), dtype = int)  #Making all elements in the ND array as 1's

border_array[1:-1, 1:-1] = 0 #making inside elements other than border as 0's

print(border_array)
Enter the size of n: 4
[[1 1 1 1]
 [1 0 0 1]
 [1 0 0 1]
 [1 1 1 1]]
print(b_arr)
b_arr [1,1:3] 

# 1 means targetting 1st row 
# 1:3 means targetting column indexes 1 and 2 (3 is not included)
[[1 2 3]
 [4 5 6]]
array([5, 6])
b_arr[:,:2]

# : Means all rows
# :2 means column index from 0 to 1
array([[1, 2],
       [4, 5]])
c = [[1,2,3,4,5],
     [6,7,8,9,10],
     [11,12,13,14,15]]

c_arr = np.array(c)

c_arr
array([[ 1,  2,  3,  4,  5],
       [ 6,  7,  8,  9, 10],
       [11, 12, 13, 14, 15]])
c_arr[:2, 1:4]
array([[2, 3, 4],
       [7, 8, 9]])
c_arr[0:,1:4]
array([[ 2,  3,  4],
       [ 7,  8,  9],
       [12, 13, 14]])
c_arr[:2,1:4]
array([[2, 3, 4],
       [7, 8, 9]])
PANDAS

import pandas as pd

df = pd.read_csv("file_path")

len(df)

df.Gender.value_counts()

df.Gender.value_counts(normalize=True)*100

#Extract facts from the available data or we can say we will analysze the data
Pandas is built on top of Numpy!!! Its called as Panel Data::
Cv2 was suing numpy only
Advantages of Nupy is already there in pandas
Numpy provides stastitical / Matrix Manipulation functionalities
Pandas provides stastical / Matrix manipulation / Analytical functionalities
Pandas has its own Data structures for storage / processing or Manipulation / Analysis of Data
- Series : Series is used to store/ process / analyse linear or 1D data
- DataFrame : Is used to store/ process/ analyse tabular data or 2D data eg. Table/sheet in MSExcel
import pandas as pdS
sampleList = [10,20,30,40,50,60]

myseries = pd.Series(sampleList)

myseries
0    10
1    20
2    30
3    40
4    50
5    60
dtype: int64
#object is same as String in pandas
import pandas as pd

nba = pd.read_csv("filename")
type(nba)
nba
# What to do after dataframe has been created ??
#Data Inspections:
#shape(rows,cols)
nba.shape()
#dtype

nba.dtype
# info() regarding the present table

nba.info()
nba.isnull().sum()  #how many missing value in a particular cloumn
nba.sort_values(by="weight", ascending=False).head(3)
nba.iloc[200:205]

#iloc used to get the values according the row indexes.
nba.iloc[200:205] [['Name', 'Position', 'College']]

#Cols will be Name, Position and College

#Rows indexes will be 200,201,202,203,204




