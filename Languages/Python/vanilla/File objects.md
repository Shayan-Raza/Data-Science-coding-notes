# File objects

Opening files with the built in open command
```python
f = open("file.txt", "r")
#To read the file use "r"
f = open("file.txt", "w")
#To write to the file use "w"
f = open("file.txt", "a")
#To append to the file use "a"
f = open("file.txt", "r+")
#To read and write the file use "r+"
```

If we open a file this way we have to close it as well
```python
f.close()
```
---
Using the context manager to open files (recommended)
```python
with open("filename.extension", "r") as f:
```

To print the contents of the file 
```python
with open("filename.extension", "r") as f:
	f_contents = f.read()
	print(f_contents)
```

To read the first line
```python
with open("filename.extension", "r") as f:
	f_contents = f.readline()
	print(f_contents)
```

Reading many lines
```python
with open("filename.extension", "r") as f:
	f_contents = f.readline(1)
	print(f_contents)
```

If we use these methods we might run out of memory so we use
```python
with open("filename.extension", "r") as f:
	for line in f:
		print(line, end="")
```

We can only read specific characters of the file
```python
with open("filename.extension", "r") as f:
	f_contents = f.read(numofcharacters)
	print(f_contents)
```