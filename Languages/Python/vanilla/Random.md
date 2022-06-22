# Random

## Random Module

Import the random module

```python
import random
```

Generate pseudo random numbers

```python
import random

a = random.random
#Will print random float
```

Random in a range 

```python
import random

a = random.uniform(1, 10)
#(Starting range, #Ending range)
```

Random integers

```python
import random

a = random.randit(1, 10)
#(Starting range, #Ending range)
```

Random choices from lists

```python
import random

list = ["Shayan", "Raza"]
choice = random.choice(list)
```

Picking more than one elements from a list

```python
import random

list1 = ["Shayan", "Raza", "Ali", "Hasaan"]
choice = random.sample(list1, 3)
print(choice)
```

Picking more than one elements from a list with duplicates

```python
import random

list1 = ["Shayan", "Raza", "Ali", "Hasaan"]
choice = random.choices(list1, k=3)
print(choice)
```

Shuffling the list

```python
import random

list1 = ["Shayan", "Raza", "Ali", "Hasaan"]
choice = random.shuffle(list1)
print(choice)
```

Reproduce Data 

```python
import random

random.seed(1)
print(random.random())
print(random.randint(1,10))

random.seed(2)
print(random.random())
print(random.randint(1,10))

```