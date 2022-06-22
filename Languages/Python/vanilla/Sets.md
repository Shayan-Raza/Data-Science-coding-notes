# Sets

<aside>
🧑‍💻 Sets are a collection Data type that are unordered and mutable with no duplicates

</aside>

---

Creating a set

```python
set = {1, 2, 3}
```

```python
set = set()
```

---

String in a set

```python
set = set("Hello)
#{H,l,o,e}
```

---

Creating an empty set

```python
set = set()
```

---

Adding to a set

```python
set.add("Shayan")
```

---

Removing in a set

```python
set.remove("Shayan")
```

Clearing a set

```python
set.clear()
```

---

Looping over a set

```python
for item in set: 
	print(item)
```

---

Union in a set

<aside>
🧑‍💻 Union combines the elements from 2 sets without duplication

</aside>

```python
union = set.union(set2)
```

Intersection

<aside>
🧑‍💻 Intersections only take stuff in both sets

</aside>

```python
union = set.intersection(set2)
```

---

Copying a set

```python
set2 = set
```

But what if we want to modify the copy but not the original

```python
set2 = set.copy()
```

```python
set2 = set(set)
```

---

Create an immuntable set

```jsx
set = forzenset()
```