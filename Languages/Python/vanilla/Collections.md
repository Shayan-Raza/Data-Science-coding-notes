# Collections
### Different types of Collections :
- Counter
- namedtuple
- OrderedDict
- defaultdict
- deque
---
### Counter
<aside>
💡 Counter is a container that stores the elements as dictionary keys and their counts as dictionary values

</aside>

Importing the counter
```python
from collections import Counter
```

Counter example
```python
from collections import Counter
a = "aaabbccdd"
counter = Counter(a)
print(counter)

```

Counting the most popular Values
```python
from collections import Counter
a = "aabbccdd"
counter = Counter(a)
print(counter.mostcommon())
```

Iterating over a count
```python
from collections import Counter
a = "aabbccdd"
counter = Counter(a)
counter2 = counter.elements()
for item in counter2 : 
    print(item)
```
---
### Named Tuples

Creating a named Tuple
```python
from collections import namedtuple
```

Example
```python
from collections import namedtuple
Point = namedtuple("Point", "x,y")
pt = Point(10, 10)
print(pt)
#It prints Point(x = 10 y = 10)
```

---
### Ordered Dict
Creating a ordered dict
<aside>
💡 Its the same as dictionaries but it remembers the order in which items are sorted

</aside>

```python
from collections import OrderedDict
```

Example
```python
from collections import OrderedDict
dict = OrderedDict()
dict ["name"] = Shayan

```

---

### Default Dict
<aside>
💡 Similar to normal dictionary but it will have a default value

</aside>

```python
from collections import defaultdict
```

Example
```python
from collections import defaultdict
d = defaultdict(int) #Type in ()
d["a"] = 1 
d["b"] = 2
```

---

### Deque

<aside>
💡 Its like lists but lets u append everywhere

</aside>

```python
from collections import deque
```

Example 
```python
from collections import deque
d = deque()

d.append(1)
d.append(2)
d.appendleft(3)

print(d)
#Prints out deque([3, 1, 2])
```

Poping a deque
```python
from collections import deque
d = deque()

d.append(1)
d.append(2)
d.appendleft(3)

d.pop() #removes the last element
d.popleft() #removes the last element

d.clear() #removes all elements

d.extend() #Adds elements in the end
```