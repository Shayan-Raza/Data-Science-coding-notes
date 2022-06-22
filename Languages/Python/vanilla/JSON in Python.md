# Json in Python

Example Json
```json
{
    "firstName": "Jane",
    "lastName": "Doe",
    "hobbies": ["running", "swimming", "singing"],
    "age": 28,
    "children": [
        {
            "firstName": "Alex",
            "age": 5
        },
        {
            "firstName": "Bob",
            "age": 7
        }
    ]
}
```
---
How to import the Json module
```python
import JSON
```
---
To load Phyton from a string use the json.loads method
```python
data = json.loads(jsonstring)
```
---
 To loop through the list we can use a for loop
```python
for person in data["key"] : 
	print(person["key"])
```
---
 To delete Values we can use
```python
for person in data["key"] : 
	del person["key"]
```

Now we will have to dump it back to Json
```python
new_string = json.dumps(data)
```
---
For a cleaner output
```python
new_string = json.dumps(data, indent = 2)
```
---
To load from another file 
```python
with open("filename.json") as f:
	data = json.load(f)
```

*More about files on ![[File objects]]*

---
Dump the data to a new file
```python
with open("newfile.json", "w") as f:
	json.dump(data, f)
```
---
Difference between load and dump
[What is the difference between json.dumps and json.load?](https://stackoverflow.com/questions/32911336/what-is-the-difference-between-json-dumps-and-json-load)

---
Classes with Json

```python
import json 

class User: 
    def __init__(self, name, age) : 
        self.name = name
        self.age = age

user = User("Max", 27)

def encode_user(o) : 
    if isinstance(o, User) : 
        return {"name" : o.name, "age" : o.age, o.__class__.__name__:True}
    else: 
        raise TypeError

userJSON = json.dumps(user, default=encode_user)
print(userJSON)

```
Also see ![[OOP]]

---
