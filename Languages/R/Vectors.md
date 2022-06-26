# Vectors
A vector is a sequence of data elements of the same basic type

> We use the c() function to declare a vector

**Example**
```R 
variable <- c(1,2,3,4,5)
```
```R 
variable <- c("shayan", "ahmed", "talha")
```

## Using the vector function 
```R
variable <- vector("[[Variables and Data types#Datatype |Datatype]]" length = length)
```

**Example**
```R 
variable <- vector("numeric" length=10)
```

## Concatenating 
```R 
variable <- c(vector1, vector2)
```

*If you concatenate different datatypes then everything is converted into character datatype*

---
## Using math functions with vectors
```R
sum(v1) # Add the values in a vector
sd(v1) # Finds the standard deviation
var(v1) # To display the variance
prod(v1) # Give the product of the vector values
max(v1) # Returns the maximum value
min(v1) # Returns the minimun value
```