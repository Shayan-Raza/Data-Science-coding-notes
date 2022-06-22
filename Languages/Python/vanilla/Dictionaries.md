# Dictionaries

<aside>
🧑‍💻 A Dictionary is a collection data type that is unordered and Mutable. It consists of a collection of Key Value Pairs

</aside>
---
Creating a dictionary 
```python
dict = {"name" : "Shayan", "age" : 10, "city" : "Qatar"}
```

Another way of creating a Dictionary
```python
dict = dict("name" = "Shayan", "age" = 10, "city" = "Qatar")
```
---
Accessing Values 
```python
value = dict["name"]
```
---
Adding new values
```python
dict["email"] = "shayanraza07@gmail.com"
```
---
Deleting from a Dictionary
```python
del dict["email"]
```

We can also use
```python
dict.pop("email")
```
---
Checking if a key exists
```python
if "email" in dict : 
	print("It exists!")
```
---
Looping through a dictionary
```python
for key in dict: 
	print(key)
```

Looping through values
```python
for value in dict.values : 
	print(value)
```

Print both
```python
for key, value in mydict.items()
	print(key, value)
```
---
Copying a dictionary
```python
copy = dict
```

Making a copy that doesn't modify the original one 
```python
copy = dict.copy()
#or
copy = dict(dict)
```

Merging a dictionary
```python
dict.update(newdict)
```