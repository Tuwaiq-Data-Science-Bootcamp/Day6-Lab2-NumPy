# Q1: Import numpy library


```python
# write your code here ^_^
import numpy as np
```

# Q2: Generate a sequence of 15 floats using linspace() function


```python
# write your code here ^_^
a=np.linspace(0,15,15,True,False,float,0)
a
```




    array([ 0.        ,  1.07142857,  2.14285714,  3.21428571,  4.28571429,
            5.35714286,  6.42857143,  7.5       ,  8.57142857,  9.64285714,
           10.71428571, 11.78571429, 12.85714286, 13.92857143, 15.        ])



# Q3: Create a 3-D array in shape (2, 2, 3) containing the four arrays given below 
Note : the array's name is up to you.

|      |       |          |         |
|------| ----- | -------- | ------- |
|arr1 | 1.1    | 2.1       | 3.1        |
|arr2 | 4.1    | 5.1       | 6.1        |
|arr3 | 7.1    | 8.1       | 9.1        |
|arr4 | 10.1   | 11.1      | 12.1       |


```python
# write your code here ^_^
arr1=[1.1,2.1,3.1]
arr2=[4.1,5.1 , 6.1]
arr3=[7.1 ,8.1,9.1]
arr4=[10.1 ,11.1,12.1]

alist= (arr1+arr2+arr3+arr4)

x = np.array(alist)
x = x.reshape(2,2,3) 
           
x
```




    array([[[ 1.1,  2.1,  3.1],
            [ 4.1,  5.1,  6.1]],
    
           [[ 7.1,  8.1,  9.1],
            [10.1, 11.1, 12.1]]])



# Q4: Print the following:
Note: use the same array from Q3.
- Array's type.
- Array's elements datatype.
- Array's shape.
- Array's size.
- Array's dimention.


```python
# write your code here ^_^
print("ndim: ",x.astype )
print("Elements datatype:", x.dtype)
print("shape:", x.shape)
print("size: ", x.size)
print("dimention: ", x.ndim)


```

    ndim:  <built-in method astype of numpy.ndarray object at 0x7f808f85df80>
    Elements datatype: float64
    shape: (2, 2, 3)
    size:  12
    dimention:  3


# Q5:  Change the array dimention from 3-D to 4-D
Note: use the same array from Q3.
- Create a new array to hold the changes. 
- Print the new array's dimention and shape.


```python
# write your code here ^_^
d4=x.reshape(1,2,2,3)
d4
```




    array([[[[ 1.1,  2.1,  3.1],
             [ 4.1,  5.1,  6.1]],
    
            [[ 7.1,  8.1,  9.1],
             [10.1, 11.1, 12.1]]]])



# Q6: Change the array's elements datatype to integer  
Note: use the same array from Q5.

- Create a new array to hold the changes. 
- Print the new array.


```python
# write your code here ^_^
d4 = d4.astype(int)
d4
```




    array([[[[ 1,  2,  3],
             [ 4,  5,  6]],
    
            [[ 7,  8,  9],
             [10, 11, 12]]]])



# Q7: Print all array's elements using for loop
Note: use the same array from Q6.

Hint: use nditer()


```python
# write your code here ^_^
for item in d4:
        print(item)

```

    [[[ 1  2  3]
      [ 4  5  6]]
    
     [[ 7  8  9]
      [10 11 12]]]


# Q8:  Print number 8 using array slicing
Note: use the same array from Q6.


```python
# write your code here ^_^
d4[0:,1:,0:1,1:2]
```




    array([[[[8]]]])



# Q9: Print number 5 and number 6 using array slicing
Note: use the same array from Q6.


```python
# write your code here ^_^
d4[0:,:1,1:2,1:]
```




    array([[[[5, 6]]]])



# Q10: Search for number 8 using where()
Note: use the same array from Q6.

Note: where() is only used with small data.

*the output represents the path of the index that leads to number 8*


```python
# write your code here ^_^

result = np.where(d4 == 8)
result
```




    (array([0]), array([1]), array([0]), array([1]))



# Q11: Reshape the array as the following

    array([[[ 1, 2],
            [ 3,  4],
            [ 5,  6]],

           [[ 7,  8],
            [ 9, 10],
            [11, 12]]])
            
 Note: use the same array from Q6.


```python
# write your code here ^_^
d4=x.reshape(1,2,3,2)
d4 = d4.astype(int)
d4
```




    array([[[[ 1,  2],
             [ 3,  4],
             [ 5,  6]],
    
            [[ 7,  8],
             [ 9, 10],
             [11, 12]]]])



# Q12: Join the given arrays below 
    arr1 = np.array([['A', 'B'], ['E', 'F']])
    arr2 = np.array([['C', 'D'], ['G', 'H']])
## Q12.1: Join the arrays without specifying the axis 


```python
# write your code here ^_^
arr1 = np.array([['A', 'B'], ['E', 'F']])
arr2 = np.array([['C', 'D'], ['G', 'H']])
ans=np.concatenate((arr1,arr2))
ans
```




    array([['A', 'B'],
           ['E', 'F'],
           ['C', 'D'],
           ['G', 'H']], dtype='<U1')



# Q12.2: Join the arrays along rows with axis = 1 


```python
# write your code here ^_^
arr1 = np.array([['A', 'B'], ['E', 'F']])
arr2 = np.array([['C', 'D'], ['G', 'H']])
ans=np.concatenate((arr1,arr2),axis=1)
ans
```




    array([['A', 'B', 'C', 'D'],
           ['E', 'F', 'G', 'H']], dtype='<U1')



# Q13: Split the array into two arrays with axis = 1, each array should contain four arrays. 
Note: use the same array from Q12.1


```python
# write your code here ^_^
ans=np.split(d4,2,axis=1)
ans
```




    [array([[[[1, 2],
              [3, 4],
              [5, 6]]]]),
     array([[[[ 7,  8],
              [ 9, 10],
              [11, 12]]]])]




```python

```
