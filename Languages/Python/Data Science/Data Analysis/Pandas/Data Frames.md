# Pandas Data Frames
<aside>💡 Data Structure for Pandas </aside>
```Python 
import pandas as pd
```
---
### Reading a CSV file 
```Python 
covid_data = pd.read_csv("italy-covid-daywise.csv") 
```
---
### Retrieving Data
*Similar to [[Dictionaries]]*
#### Accessing a  column
```Python 
covid_df."new_cases"
```
#### Accessing a specific value from index notation
```Python
covid_df["new_cases"][246] #Acceses the 246th row
```
#### Using the .at method 
```Python 
covid_df.at[246,"newcases"] #Row no. , Column
```
#### To access multiple columns
```Python 
covid_df[["date, "new_cases"]]
```
#### Last and First Rows 
``` Python 
covid_df.head() #first rows number in ()

covid df.tail()# last rows number in ()
```
#### Random sample 
```Python 
covid_df.sample() #no of samples in ()
```

#### Adding a new column
```Python
covid_df["postive_rate"] = covid_df.new_cases / covid_df.new_tests
#Dataframe[header name] = formula
```

***To remove it***
```Python 
covid_df.drop(columns=["positive_rate"])
```
---

## Merging Data from Multiple sources
```Python 
merged_df = covid_df.merge(locations_df, on="location")

#variable = dataframe.merge(dataframe, on="field")
```
*Finds the location in the other dataframe and finds matching fields and then adds the columns matching*

---

## Exporting Data Frames 
*Create a new Data Frame with the fields required*
```Python 
result_df = merged_df[['date',
                       'new_cases', 
                       'total_cases', 
                       'new_deaths', 
                       'total_deaths', 
                       'new_tests', 
                       'total_tests', 
                       'cases_per_million', 
                       'deaths_per_million', 
                       'tests_per_million']]
```

*Using the to_csv function export the data*
```Python
result_df.to_csv("results.csv", index = None)
```

## Replacing Data
```Python
DataFrame.replace(

to_replace=None,

value=None,

inplace=False,

limit=None,

regex=False,

method='pad')
```
*Let’s take a closer look at what these actually mean:*

-   **to_replace**: take a string, list, dictionary, regex, int, float, etc. and describes the values to replace
-   **value**: The value to replace with
-   **inplace**: whether to perform the operation in place
-   **limit**: the maximum size gap to backward or forward fill
-   **regex**: whether to interpret _to_replace_ and/or _value_ as regex
-   **method**: the method to use for replacement

**Replacing specific data**
```Python
df['Sex'] = df['Sex'].map({'female':0, 'male':1})
```