# Dataframe
A dataframe is used to store the data in the form of a table

> We use the data.frame() function to create a dataframe

**Example**
```R
df <- data.frame(gender = c("Male", "Female"), name = c("Shayan", "Fatima"), age = (10,10))
```

*Output*
| Gender    |Name     | Age     |
| --- | --- | --- |
|Male     | Shayan     |   10  |
|Female    | Fatima     | 10    |

---
## Creating a dataframe with variables 
1: Create [[Vectors]]
```R
gender <- c("Male", "female")
name <- c("Shayan", "fatima")
```
2:Use the function
```R
df<- data.frame(gender, name) #Column names are the variable names
```

---
## Indexing
```R
df[3,2]
# df[rowindex, column index]
# starts with 1
```

**Viewing an entire row**
```R
df[3,]
```

**Viewing an entire column**

Using the column number
```R
df[[2]]
```

Using the column name
```R
df[["age"]]
```

**Multiple Columns**
```R 
df[1:2]
```

**Operators**
```R
df[df<30]
```

## Removing Na values 
```R
sum(order_detail, na.rm=T)
```