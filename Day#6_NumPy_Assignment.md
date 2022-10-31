```python
import numpy as np
```

## Q#1: Create x array with elements equal to 1.


```python
x=np.ones((5,), dtype=int)
x
```




    array([1, 1, 1, 1, 1])



## Q#2: Create y array with elements equal to 0.


```python
y=np.zeros((5,), dtype=int)
y
```




    array([0, 0, 0, 0, 0])



## Q#3: Add x and y arrays.


```python
z=np.add(x,y)
z

```




    array([1, 1, 1, 1, 1])



## Q#4: Print x array characteristics (e.g: dimension, shape, size, type)


```python
print("x ndim: ", x.ndim)
print("x shape:", x.shape)
print("x size: ", x.size)
print("x dtype:", x.dtype)
```

    x ndim:  1
    x shape: (5,)
    x size:  5
    x dtype: int64


## Q#5: Create a 2D array "called w" as the following:

|       |          |
| ----- | -------- |
| 11    | 12       |
| 13    | 14       |
| 15    | 16       |



```python
w=np.array([['11', '12'],['13', '14'],['15', '16']])
w
```




    array([['11', '12'],
           ['13', '14'],
           ['15', '16']], dtype='<U2')



## Q#6: Create z array contains the numbers from 1 to 3.


```python
z=np.array([1,2,3])
z

```




    array([1, 2, 3])



## Q#7: Combine the arrays z and w in vertical way then save it in a new variable "newArray".


```python
col_vector = z.reshape((3,1))
col_vector
z=col_vector
z
newArray=np.concatenate((z, w), axis=1)
newArray
```




    array([['1', '11', '12'],
           ['2', '13', '14'],
           ['3', '15', '16']], dtype='<U21')



## Q#8: Print all elements of "newArray" using the loop.


```python
for row in newArray:
    for item in row:
        print(item)
```

    1
    11
    12
    2
    13
    14
    3
    15
    16


## Q#9: Reverse the columns and rows of "newArray".


```python
newArray=np.flip(newArray, axis=1)
newArray
```




    array([['12', '11', '1'],
           ['14', '13', '2'],
           ['16', '15', '3']], dtype='<U21')



## Q#10: Decrement all elements of "newArray" with 1.


```python
newArray = newArray.astype(int)
newArray -= 1

newArray
```




    array([[11, 10,  0],
           [13, 12,  1],
           [15, 14,  2]])



## Q#11: Find smallest and biggest values in "newArray".


```python
smallest=np.min(newArray)

biggest=np.max(newArray) 
print(smallest)
print(biggest)
```

    0
    15


## Q#12: Print the first row of "newArray" using indexing.


```python
newArray[0]
```




    array([11, 10,  0])



## Q#13: Print the number equals 12 of "newArray" using indexing.


```python
newArray[1][1]

```




    12



## Q#14: Print the numbers equal 0 and 13 of "newArray" using Slicing.


```python
newArray[0][2]
```




    0




```python
newArray[1][0]
```




    13



## Q#15: Change the shape of "newArray" to (9,1).


```python
newArray.reshape(9, 1)

```




    array([[11],
           [10],
           [ 0],
           [13],
           [12],
           [ 1],
           [15],
           [14],
           [ 2]])



## Q#16: Change the shape of "newArray" to (3,2).


```python
newArray.reshape(3, 2)

```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-71-26c86a79e7a5> in <module>
    ----> 1 newArray.reshape(3, 2)
    

    ValueError: cannot reshape array of size 9 into shape (3,2)


# Well Done 🎉
