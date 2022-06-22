# Tuples

<aside>
🧑‍💻 A Tuple is a collection data type that is ordered and immutable and allows duplicate elements. Kinda similar to lists

</aside>

---

Create a Tuple

```python
mytuple = ("Shayan", "Raza", 15)
```

---

Create a Tuple from a list

```python
mytuple = tuple([list])
```

---

Accessing tuple elements

```python
item = mytuple[0]
```

---

Iterating over a tuple

```python
mytuple = ("Shayan", "Raza", 15)
for item in mytuple:
	print(item)
```

---

Checking if a element exists in a Tuple

```python
mytuple = ("Shayan", "Raza", 15)
if "Shayan" in mytuple: 
	print("Yes)
else: 
	print("No)
```

 U can also use 

```python
print("Shayan" in mytuple)
```

---

Checking the number of elements in our tuple

```python
mytuple = ("Shayan", "Raza", 15)
print(len(mytuple))
```

Counting specific elements

```python
mytuple = ("Shayan", "Raza", 15)
print(mytuple.count("a"))
```

Finding the index for a specific element

```python
mytuple = ("Shayan", "Raza", 15)
print(mytuple.index("a"))
```

---

Converting tuple to list

```python
mytuple = ("Shayan", "Raza", 15)
mylist = list(mytuple)
```

Converting list to tuple

```python
mytuple = ("Shayan", "Raza", 15)
mylist = list(mytuple)

mytuple2 = tuple(mylist)
```

---

Slicing tuple

```python
a = (1, 2, 3, 4, 5, 6, 7, 8)
b = a[3:6]
#start of a Tuple
c = a[:5]
#end of the tuple
d = a[0:]
#count in steps
e = a[2::1]
#a[Start:: Steps to jump]
```

---

Tuple unpacking

```python
mytuple = "Shayan", 15, "Doha"
name, age, city = mytuple
print(name)
#Shayan
print(age)
#15
print(city)
#Doha
```

---

> Tuples can be more useful with large data as it takes less space compared to a list and is faster to make and iterate over
>