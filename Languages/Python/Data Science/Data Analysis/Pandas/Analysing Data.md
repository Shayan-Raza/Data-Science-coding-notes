# Analysing Data
---
#### Adding values 
```Python 
total_cases = covid_df.newcases.sum() #variable.column.method()
```
---
### Querying Data
#### Using <> Operators 
```Python 
high_new_cases = covid.df.new_cases > 1000
```
*We get a boolean series* 

***To get a result***
```Python
covid_df[high_new_cases]
```

***We can do the above steps in one line***
```Python 
high_new_cases = covid_df[covid_df.new_cases > 1000]
```

***Example*** 
``` Python
high_ratio_df = covid_df.new_cases / covid_df.new_tests > chances_of_postive
```
*Gives us only the values where the ratio was more than the average ratio*

---
## Sorting 
```Python 
covid_df.sort_values("new_cases", ascending="False")
#dataframe.sort_values("column", ascending="True/False")
```
---
### Dates
*Make a field a Data field*
```Python
covid_df["date"] = pd.to_datetime(covid_df.date)
#covid_df["field"] = pd.to_datetime(covid_df.date)
```
***Date time index***
```Python 
covid_df['year'] = pd.DatetimeIndex(covid_df.date).year
covid_df['month'] = pd.DatetimeIndex(covid_df.date).month
covid_df['day'] = pd.DatetimeIndex(covid_df.date).day
covid_df['weekday'] = pd.DatetimeIndex(covid_df.date).weekday
```
*We get seperate columns for each*

---
## Quering Data 
```Python
# Query the rows for May
covid_df_may = covid_df[covid_df.month == 5]

# Extract the subset of columns to be aggregated
covid_df_may_metrics = covid_df_may[['new_cases', 'new_deaths', 'new_tests']]

# Get the column-wise sum
covid_may_totals = covid_df_may_metrics.sum()
```
***Using data for weekdays***
*find average of cases in the weekdays*
```Python 
covid_df[covid_df.weekday == 6].new_cases.mean()
#dataframe[dataframe.weekday == 1/2/3/4/5/6].field.mean
#.mean finds average
```
---
## Grouping
### Grouping 
```
as_index=False
```
*Use this if u wanna use a index*

``` Python 
monthly_groups =  covid_df.groupby('month')[['new_cases', 'new_deaths', 'new_tests']].sum()

#variable = dataframe.groupby("groupbywhat") [[fields]].function()
```
*Gives the results of the sum on 12 months*

***Plotting a Group***
```Python 
assembly_price.plot(kind='bar', title='Relation of the assembly of the car and the price',ylabel='Price',
xlabel='Location of the assembly of the car');
```

### Finding the sum (so far)
*Use the cumsum function*
```Python 
covid_df["total_cases"] = covid_df.new_cases.cumsum()

#datadrame["set field name"] = dataframe.field.cumsum()
```
---

## Plotting with Pandas
[[Matplotlib and Seaborn]]
***Quick line graph with one line***
```Python 
result_df.new_cases.plot();

#dataframe.field.plot()
```

***Setting an index (makes it the x axis)***
```Python 
covid_df.set_index('date', inplace=True)
```

***Multiple Fields***
```Python 
covid_df.new_cases.plot()
covid_df.new_deaths.plot();
```

***Setting the title of the graph***
```Python 
covid_df.new_cases.plot(title = "New Cases")
```

***Bar Chart***
```Python 
covid_df.new_cases.plot(kind = "bar")
```