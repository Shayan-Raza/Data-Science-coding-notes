# Lambda

<aside>
💡 Lambda function is a small one line anonymous function that is defined without a name

</aside>

---
Example
```python
add10 = lambda x: x + 10
print(add10(5))
#15
```

Similar to def
```python
def add(x) : 
	return x + 10 
print(add(5))
#15
```
---
Sorting with Lambda
```python
points2D = [(1, 9), (4, 1), (5, -3), (10, 2)]
sorted_by_y = sorted(points2D, key= lambda x: x[1])
print(sorted_by_y)
```

Sorting with a def
```python
points2D = [(1, 9), (4, 1), (5, -3), (10, 2)]
def sortbyy(): 
	return x[1]
sorted_by_y = sorted(points2D, key=sortbyy)
print(sorted_by_y)
```
---
Map function with Lambda

*map(func, seq)*
```python
a = [1 ,2, 3, 4, 5, 6, 7, 8, 9, 10]
b = map(lambda x : x * 2 , a )
print(list(b))
#2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
```
---
Filter function with Lambda

*filter(func, seq)* 
```python
a = [1 ,2, 3, 4, 5, 6, 7, 8, 9, 10]
b = filter(lambda x : x * 2 == 10 , a )
print(list(b))
#[5]
```
---
Reduce function with lambda

*reduce(func, seq)*
```python
from functools import reduce
a = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

product_a = reduce(lambda x,y : x*y, a)
print(product_a)
#3628800

```