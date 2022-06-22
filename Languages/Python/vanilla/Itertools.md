# Itertools

<aside>
💡 Iterators are data types that can be used in a for loop. Itertools offer more advanced tools

</aside>
---
Importing Itertools
```python
from itertools import product
```
---
Product
```python
from itertools import product
a = [1, 2]
b = [3, 4]
prod = product(a, b)
print(list(prod))
#Result: [(1, 3), (1, 4), (2, 3), (2, 4)]
```
---
Permutations
```python
from itertools import permutations
a = [1, 2, 3]
perm = permutations(a)
print(list(perm))
```
---
Combinations
```python
from itertools import accumulate
a = [1, 2, 3, 4]
acc = accumulate(a)
print(list(acc))
#1, 3, 6, 10
```
---
Groupby
```python
from itertools import groupby

def smallerthan3(x): 
	return x < 3
a = [1, 2, 3, 4]
obj = groupby(a, key=smallerthan3)
for key,value in obj: 
	print(key, list(value))
#True [1, 2]
#False [3, 4]
```
```python
from itertools import groupby
persons = [{'name': 'Tim', 'age': 25}, {'name': 'Dan', 'age': 25}, 
           {'name': 'Lisa', 'age': 27}, {'name': 'Claire', 'age': 28}]

for key, group in groupby(persons, key=lambda x: x['age']):
    print(key, list(group))
#25 [{'name': 'Tim', 'age': 25}, {'name': 'Dan', 'age': 25}]
#27 [{'name': 'Lisa', 'age': 27}]
#28 [{'name': 'Claire', 'age': 28}]
```
---
Infinite Variables
```python
from itertools import count,cycle,repeat
for i in count(10): 
	print(i)
	if i == 13: 
		break
#Result: 
#10
#11
#12
#13
```