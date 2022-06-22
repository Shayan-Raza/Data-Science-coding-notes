# Arrays
<aside>💡 Numpy provides specialized data structures, function and other tools for numerical computing</aside>

---
#### Importing Numpy
``` Python 
import numpy as np
```
---
#### Python list to numpy array
``` Python
kanto = np.array([73, 67, 43])
weights = np.array([w1, w2, w3])
```
---
## Multi-dimensional arrays
#### 2D Array
```Python 
climate_data= np.array([
[73, 67, 43],
[91, 88, 64],
[87, 134, 58],
[102, 43, 37],
[69, 96, 70],
])
```
```Python
climate_data.shape
#(5,3)
```
#### 3 or more Dimensional Array
```Python 
arr3 = np.array([
    [[11, 12, 13], 
     [13, 14, 15]], 
    [[15, 16, 17], 
     [17, 18, 19.5]]])
```
```Python
arr3.shape
#(2,2,3)
```
---
### Merging 2 or more arrays
We use the concatenate function
```Python
climate_results = np.concatenate((climate_data, yields.reshape(10000, 1)), axis=1)

```
*Gives us an array with both the arrays added*
*Axis specifies the dimension for concatenation*
*Both arrays should have same number of dimensions*

---
## Array Indexing and Slicing
```Python 
arr3 = np.array([
    [[11, 12, 13, 14], 
     [13, 14, 15, 19]], 
    
    [[15, 16, 17, 21], 
     [63, 92, 36, 18]], 
    
    [[98, 32, 81, 23],      
     [17, 18, 19.5, 43]]])
```
```Python 
arr3.shape
#(3,2,4)
```
#### Finding from the array 
*We need to find 36 in the 4th row and 3rd column*
```Python 
arr3[1,1,2]
#It goes to the second dimension 
#It goes to the second row in the dimension 
#It goes to the third item
#36
```
#### Finding ranges 
```Python
arr3[0:2, 2:4] #[dimension range, column range]
```
---
### Other ways of creating arrays 
#### Array of all numbers 
```Python
np.zeros([])
```
#### All ones
```Python 
np.ones([])
```
#### Identity Matrix
```Python 
np.eye()
#Result with 3: 
#```
([[1., 0., 0.],
[0., 1., 0.],
[0., 0., 1.]])
```
#### Random Vector 
```Python 
np.random.rand()
#Result for 5
#array([0.8208279 , 0.93801216, 0.44954753, 0.17816933, 0.32049174])
```
#### Random matrix 
*Picks number for gaussian distribution*
```
np.random.randn()
```
#### Fixed Value
```Python 
np.full([], 42) # Dimensions in [], number
```
---
