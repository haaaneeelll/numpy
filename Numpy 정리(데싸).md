```python
import numpy as np
```


```python
lst = [1,2,3,4,5]
```


```python
a = np.array(lst)
```


```python
a
```




    array([1, 2, 3, 4, 5])




```python
b = [[1,2,3], [4,5,6]]
```


```python
np.array(b)
```




    array([[1, 2, 3],
           [4, 5, 6]])




```python
np.zeros((2,3))
```




    array([[0., 0., 0.],
           [0., 0., 0.]])




```python
np.ones((2,2))
```




    array([[1., 1.],
           [1., 1.]])




```python
np.empty((2,3))
```




    array([[0., 0., 0.],
           [0., 0., 0.]])




```python
arr = np.array([0,1,2,3,4,5,6,7,8,9,10,11])
print("Original array:")
print(arr)

reshaped_arr = np.reshape(arr, (3,4))
print("\nReshaped array (3x4):")
print(reshaped_arr)
```

    Original array:
    [ 0  1  2  3  4  5  6  7  8  9 10 11]
    
    Reshaped array (3x4):
    [[ 0  1  2  3]
     [ 4  5  6  7]
     [ 8  9 10 11]]



```python
np.arange(0, 5)
# 5미만
```




    array([0, 1, 2, 3, 4])




```python
np.arange(0, 20, 2)
```




    array([ 0,  2,  4,  6,  8, 10, 12, 14, 16, 18])




```python
np.linspace(0,5,10)
```




    array([0.        , 0.55555556, 1.11111111, 1.66666667, 2.22222222,
           2.77777778, 3.33333333, 3.88888889, 4.44444444, 5.        ])




```python
np.eye(4)

# identity matrix
```




    array([[1., 0., 0., 0.],
           [0., 1., 0., 0.],
           [0., 0., 1., 0.],
           [0., 0., 0., 1.]])




```python
a.max()
```




    5




```python
a.min()
```




    1




```python
a.argmax() # 0,1,2,3,4 인덱스 값
```




    4




```python
a.argmin() # min값 리턴 
```




    0




```python
a.dtype
```




    dtype('int64')




```python
a1 = a[:1]
```


```python
a1
```




    array([1])




```python
a1[0] = 10
```


```python
a
# 기존의 array가 바뀜! 
# array 조작을 많기때문에 파생 array가 변하면 원본 array도 변한다.
```




    array([10,  2,  3,  4,  5])




```python
b = a.copy() #위의 상황을 피하기 위함
```


```python
b
```




    array([10,  2,  3,  4,  5])




```python
b[0] = 11
```


```python
a
# 안바뀜 
```




    array([10,  2,  3,  4,  5])




```python
b
```




    array([11,  2,  3,  4,  5])




```python
# broadcasting
x = np.array([[1,2,3],[4,5,6],[7,8,9]])
```


```python
y = np.array([1,2,3])
```


```python
z= x + y
```


```python
z
```




    array([[ 2,  4,  6],
           [ 5,  7,  9],
           [ 8, 10, 12]])




```python
arr = np.array([0,1,2,3,4,5,6,7,8,9])
```


```python
condition = arr > 5
```


```python
print(condition)
```

    [False False False False False False  True  True  True  True]



```python
filtered_arr = arr[condition]
```


```python
print(filtered_arr)
```

    [6 7 8 9]



```python
# operation
```


```python
arr + 1
```




    array([ 1,  2,  3,  4,  5,  6,  7,  8,  9, 10])




```python
arr - 1
```




    array([-1,  0,  1,  2,  3,  4,  5,  6,  7,  8])




```python
arr * arr
```




    array([ 0,  1,  4,  9, 16, 25, 36, 49, 64, 81])




```python
arr / 1
```




    array([0., 1., 2., 3., 4., 5., 6., 7., 8., 9.])



 # sin

 
 ![%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202023-06-15%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%203.48.47.png](attachment:%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202023-06-15%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%203.48.47.png)


```python

```

 # agg
 ![%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202023-06-15%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%203.49.47.png](attachment:%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202023-06-15%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%203.49.47.png)

![%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202023-06-15%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%203.54.20.png](attachment:%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202023-06-15%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%203.54.20.png)


```python

```


```python

```
