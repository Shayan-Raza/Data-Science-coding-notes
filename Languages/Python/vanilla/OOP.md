# OOP


Creating a class
```python
class Phones() : 
    pass
```

Creating an instance of the class 
```python
class Phones() : 
    pass 

Phone1 = Phones()
```

Adding Info
```python
class Phones() : 
    pass 

Phone1 = Phones()
Phone1.name= "Samsung A70"
Phone1.price = 1000
Phone1.quantity = 10
#if you print any of these you get the value specified
```

Example with passing of arguments to calculate total price
```python
class Phones() : 
    def total_price(self, x, y) : 
        return x * y 

Phone1 = Phones()
Phone1.name= "Samsung A70"
Phone1.price = 1000
Phone1.quantity = 10

print(Phone1.total_price(Phone1.price, Phone1.quantity))
#10000 (1000 * 10)
```

---

### Constructors

Using the __ init __ method

<aside>
💡 It runs code when the class is called. It helps us automatically define the arguments that have to be passed

</aside>

We can add instances with just a single line 
```python
class Phones() : 
    def __init__(self, name, price, quantity):
        print("Created Instance of Phone")
        self.name = name
        self.price = price 
        self.quanitity = quantity
    
    def total_price(self, x, y) : 
        return x * y 

Phone1 = Phones("Samsung A70", 1000, 10)
# Phone1.name= "Samsung A70"
# Phone1.price = 1000
# Phone1.quantity = 10

Phone2 = Phones("Samsung A60", 900, 100)
# Phone2.name= "Samsung A60"
# Phone2.price = 900
# Phone2.quantity = 100
```

Setting Default Values 
```python
class Phones() : 
    def __init__(self, name, price, quantity = 0):
        print("Created Instance of Phone")
        self.name = name
        self.price = price 
        self.quanitity = quantity
    
    def total_price(self, x, y) : 
        return x * y 

Phone1 = Phones("Samsung A70", 1000, 10)
Phone2 = Phones("Samsung A60", 900, 100)
```

Making the total price efficient 
```python
class Phones() : 
    def __init__(self, name, price, quantity):
        print("Created Instance of Phone")
        self.name = name
        self.price = price 
        self.quanitity = quantity
    
    def total_price(self) : 
        return self.price * self.quanitity 

Phone1 = Phones("Samsung A70", 1000, 10)
Phone2 = Phones("Samsung A60", 900, 100)

print(Phone1.total_price())
print(Phone2.total_price())
```

Getting Verifications
```python
class Phones() : 
    def __init__(self, name: str, price: int, quantity: int):
        assert price >= 0
        assert quantity >= 0        
        
        print(f"Created Instance of {name}")
        
        self.name = name
        self.price = price 
        self.quanitity = quantity
    
    def total_price(self) : 
        return self.price * self.quanitity 

Phone1 = Phones("Samsung A70", 1000, 10)
Phone2 = Phones("Samsung A60", 900, 100)

print(Phone1.total_price())
print(Phone2.total_price())
```

Setting a Universal Attribute
```python
class Phones() : 
    
    profit_margin = 0.7
    
    def __init__(self, name: str, price: int, quantity: int):
        assert price >= 0
        assert quantity >= 0        
        
        print(f"Created Instance of {name}")
        
        self.name = name
        self.price = price 
        self.quanitity = quantity
    
    def total_price(self) : 
        return self.price * self.quanitity 

Phone1 = Phones("Samsung A70", 1000, 10)
Phone2 = Phones("Samsung A60", 900, 100)

print(Phone1.total_price())
print(Phone2.total_price())
```

__ repr __ method 

<aside>
💡 It helps you represent the instances

</aside>
```python
class Phones() : 
    all = []
    
	def __init__(self, name: str, price: int, quantity: int):
        
        assert price >= 0
        assert quantity >= 0         
        
        self.name = name
        self.price = price 
        self.quantity = quantity

        Phones.all.append(self)

    def total_price(self) : 
        return self.price * self.quantity 

    def __repr__(self) : 
        return f"Phones('{self.name}', {self.price}, {self.quantity})"

Phone1 = Phones("Samsung A70", 1000, 10)
Phone2 = Phones("Samsung A60", 900, 100)
Phone3 = Phones("Samsung A50", 800, 92)
Phone4 = Phones("Samsung A40", 750, 75)

print(Phones.all)

#Prints out a list of all the Instances
```

---

## Class Vs Static Methods

### Class Methods

<aside>
💡 Class methods cannot be used to alter the state of an instantiated object but instead, they are capable of changing the class state which is shared amongst all the instances of that class.

</aside>

Using CSV
```
name,price,quantity
Samsung A70,1000,10
Samsung A60,900,100
Samsung A50,800,92
Samsung A40,750,75
```

Reading the CSV File
```python
import csv

class Phones() : 
    all = []
    
    def __init__(self, name: str, price: int, quantity: int):
        
        assert price >= 0
        assert quantity >= 0         
        
        self.name = name
        self.price = price 
        self.quantity = quantity

        Phones.all.append(self)

    def total_price(self) : 
        return self.price * self.quantity 
    
    @classmethod
    def get_from_csv(cls) : 
        with open("Test/Phones.csv", "r") as c : 
            reader = csv.DictReader(c)
            items = list(reader)
        
        for item in items : 
            print(item)

    def __repr__(self) : 
        return f"Phones('{self.name}', {self.price}, {self.quantity})"

Phones.get_from_csv()
```

### Static Methods

<aside>
💡 In static methods neither the instance (i.e. `self` ) nor the class itself (i.e. `cls` ) is passed as an implicit argument. This means that such methods, are not capable of accessing the class itself or its instances.

</aside>

Example 
```python
import csv

class Phones() : 
    all = []
    
    def __init__(self, name: str, price: int, quantity: int):
        
        assert price >= 0
        assert quantity >= 0         
        
        self.name = name
        self.price = price 
        self.quantity = quantity

        Phones.all.append(self)

    def total_price(self) : 
        return self.price * self.quantity 
    
    @classmethod
    def get_from_csv(cls) : 
        with open("Test/Phones.csv", "r") as c : 
            reader = csv.DictReader(c)
            items = list(reader)
        
        for item in items : 
            print(item)
    
    @staticmethod
    def is_integer(num) :
        if isinstance(num, float) : 
            return num.is_integer() 
        elif isinstance(num, int) : 
            return True
        else : 
            return False

    def __repr__(self) : 
        return f"Phones('{self.name}', {self.price}, {self.quantity})"

print(Phones.is_integer(7.5))
```

### When to use Class Method or Static Method
- Class Method
    
    Usually used to manipulate different structures of data to instantiate objects like we have done with CSV or from JSON
    
- Static Method
    
    This should do something that has a relationship with the class but not something that must be unique per instance 
    

---
## Inheritance
### Parent Classes and Child Classes
Class we inherit from are called Parent Classes and those who Inherit are called Child Classes

We can get the methods 
```python
class Broken(Phones) : 
    def __init__(self, name: str, price: int, quantity: int, broken_phones=0):
        
        assert price >= 0
        assert quantity >= 0         
        assert broken_phones >= 0
        
        self.name = name
        self.price = price 
        self.quantity = quantity
        self.broken_phones = broken_phones

Broken_Phones_1 = Broken("Samsung A30", 200, 500)
Broken_Phones_1.broken_phones = 5
print(Broken_Phones_1.total_price())

Broken_Phones_2= Broken("Samsung A20", 175, 250)
Broken_Phones_2.broken_phones = 2
```

What does the Super Method do? 

<aside>
💡 It allows us to have full access to the attributes of the parent class

</aside>

```python
class Broken(Phones) : 
    def __init__(self, name: str, price: int, quantity: int, broken_phones=0):
        super().__init__(name,price,quantity)
    
        self.broken_phones = broken_phones

Broken_Phones_1 = Broken("Samsung A30", 200, 500)
Broken_Phones_1.broken_phones = 5
print(Broken_Phones_1.total_price())

Broken_Phones_2= Broken("Samsung A20", 175, 250)
Broken_Phones_2.broken_phones = 2
```
---
## Getting Classes from other files
```python
from phones import Phones
```