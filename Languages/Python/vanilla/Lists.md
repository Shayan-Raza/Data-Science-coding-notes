# Lists

<aside>
🧑‍💻 A list is a collection data type that is ordered mutable and allows duplicate elements

</aside>
---
Creating a list
```python
mylist = ["banana","cherry", "apple" ]
```
---
Creating an empty list
```python
mylist = list()
```
---
Lists can have different data types
```python
mylist = [True, Variable, "string" ]
```
---
They also allow duplicate elements
```python
mylist = [True, Variable, "string", "string" ]
```
---
Accessing an element in a list
```python
mylist = ["Apple","Banana", "string",]
print(mylist[0])
#Apple
print(mylist[1])
#Banana
print(mylist[2])
#string
```

-1 Refers to the last item
```python
mylist = ["Apple","Banana", "string",]
print(mylist[-1])
#string
```
---
Looping through a list
```python
for i in mylist:
	print(i)
#Apple
#Banana
#string
```
---
Checking an item in a list
```python
if "Apple" in mylist:
	print("yes")
else:
	print("no")
```

U can also use

```python
print("Shayan" in mylist)
```
---
Checking the length of a list

```python
print(len(mylist))
```
---
Appending items in a list
```python
mylist.append("lemon")
```
---
Inserting items at specific position
```python
mylist.insert(1, "blueberry")
```
---
Removing items
```python
item = mylist.remove("Apple")
```

Clear the list

```python
item = mylist.clear
```
---
Reverse the list
```python
item = mylist.reverse()
```

Sort the list
```python
mylist.sort()
#or create a new list
new_list = sorted(mylist)
```
---
Slicing

```python
mylist = [1, 2, 3, 4, 5, 6]

a = mylist[1:5]
#specify the index range in the square brackets
#start of the list
b = a[:5]
#end of the list
c = a[0:]
#count in steps
d = a[2::1]
#a[Start:: Steps to jump]
```