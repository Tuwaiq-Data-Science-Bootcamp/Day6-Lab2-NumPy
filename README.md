# Day6-Lab2-NumPy

Q1: Import numpy library

import numpy as np


Q2: Generate a sequence of 15 floats using linspace() function

np.linspace(0,15,15)


Q3: Create a 3-D array in shape (2, 2, 3) containing the four arrays given below
Note : the array's name is up to you.




arr1
1.1
2.1
3.1
arr2
4.1
5.1
6.1
arr3
7.1
8.1
9.1
arr4
10.1
11.1
12.1

my3Darr=np.array([[[1.1,2.1,3.1],[4.1,5.1,6.1]], [[7.1,8.1,9.1], [10.1,11.1,12.1,]]])
my3Darr



Q4: Print the following:
Note: use the same array from Q3.
	•	Array's type.
	type(my3Darr)

	•	Array's elements datatype.
	my3Darr.dtype

	•	Array's shape.
	my3Darr.shape

	•	Array's size.
	my3Darr.size
	
	•	Array's dimention.
	my3Darr.ndim


Q5: Change the array dimention from 3-D to 4-D

Note: use the same array from Q3.
	•	Create a new array to hold the changes.
	•	Print the new array's dimention and shape.



Q6: Change the array's elements datatype to integer
Note: use the same array from Q5.
	•	Create a new array to hold the changes.
	•	Print the new array.

my4Darr.astype(int)



Q7: Print all array's elements using for loop
Note: use the same array from Q6.
Hint: use nditer()
nditer is to visit every element of an array
for x in np.nditer(a):
	print(x)
reference: https://numpy.org/doc/stable/reference/arrays.nditer.html


Q8: Print number 8 using array slicing
Note: use the same array from Q6.
myfind=np.where(my4Darr==8)



Q9: Print number 5 and number 6 using array slicing
Note: use the same array from Q6.



Q10: Search for number 8 using where()
Note: use the same array from Q6.
Note: where() is only used with small data.
the output represents the path of the index that leads to number 8



Q11: Reshape the array as the following
array([[[ 1, 2],
        [ 3,  4],
        [ 5,  6]],

       [[ 7,  8],
        [ 9, 10],
        [11, 12]]])

Note: use the same array from Q6.



Q12: Join the given arrays below
arr1 = np.array([['A', 'B'], ['E', 'F']])
arr2 = np.array([['C', 'D'], ['G', 'H']])
Q12.1: Join the arrays without specifying the axis



Q12.2: Join the arrays along rows with axis = 1



Q13: Split the array into two arrays with axis = 1, each array should contain four arrays.
Note: use the same array from Q12.1

