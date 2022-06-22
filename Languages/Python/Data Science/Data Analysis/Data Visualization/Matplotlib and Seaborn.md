# Graphs 
## Setting the size of the Graph 
```Python
plt.figure(figsize=(22,8))
```
## Line Chart
```Python 
plt.plot(yield_apples)

# plt.plot(variable)
```
*Use a semi colon at the end to avoid text*
```Python 
plt.plot(yield_apples);
```

***Adding Labels***
``` Python 
# X-Axis 
plt.xlabel("Year")
# Y-Axes
plt.ylabel("Yield")
```

***Adding Multiple Lines***
```Python 
# Line 1
plt.plot(years, apples)
#Line 2
plt.plot(years, oranges)
# X axis
plt.xlabel("Year")
# Y axis
plt.ylabel("Yield");
```

***Chart title and Legend***
```Python 
plt.title("Crop Yields in Kanto")
plt.legend(['Apples', 'Oranges']);
```

***Line Markers***
```Python 
plt.plot(years, apples, marker='o')
plt.plot(years, oranges, marker='x')
```

***Styling lines and markers***
The `plt.plot` function supports many arguments for styling lines and markers:

-   `color` or `c`: Set the color of the line ([supported colors](https://jovian.ai/outlink?url=https%3A%2F%2Fmatplotlib.org%2F3.1.0%2Fgallery%2Fcolor%2Fnamed_colors.html))
-   `linestyle` or `ls`: Choose between a solid or dashed line
-   `linewidth` or `lw`: Set the width of a line
-   `markersize` or `ms`: Set the size of markers
-   `markeredgecolor` or `mec`: Set the edge color for markers
-   `markeredgewidth` or `mew`: Set the edge width for markers
-   `markerfacecolor` or `mfc`: Set the fill color for markers
-   `alpha`: Opacity of the plot
```Python 
plt.plot(years, apples, marker='s', c='b', ls='-', lw=2, ms=8, mew=2, mec='navy')
plt.plot(years, oranges, marker='o', c='r', ls='--', lw=3, ms=10, alpha=.5)
```

*A faster way*
```Python 
fmt = '[marker][line][color]'
```
*No need to specify it the third argument is always fmt*
```Python 
plt.plot(years, apples, 's-b')
```
*Not specifying the line makes a graph without lines*

***Using the Seaborn library***
```Python 
sns.set_style("whitegrid")
```
[List of styles](https://jovian.ai/outlink?url=https%3A%2F%2Fseaborn.pydata.org%2Fgenerated%2Fseaborn.set_style.html)

---
## Scatter Plot 
***Basic Scatter Plot***
```Python 
sns.scatterplot(x=flowers_df.sepal_length, y=flowers_df.sepal_width);
```

***Adding Hues***
```Python
sns.scatterplot(x=flowers_df.sepal_length, y=flowers_df.sepal_width, hue=flowers_df.species);
```

---
## Histrogram
```Python 
plt.hist(flowers_df.sepal_width)
```

***Controlling the size and number of bins***
```Python 
plt.hist(flowers_df.sepal_width, bins=5)
```

***Multiple Histrograms***
*We use alpha*
```Python
plt.hist(setosa_df.sepal_width, alpha=0.4, bins=np.arange(2, 5, 0.25));
plt.hist(versicolor_df.sepal_width, alpha=0.4, bins=np.arange(2, 5, 0.25));
```
---
## Bar Chart 
```Python 
plt.bar(years, apples)
```

***Barcharts on top of each other***
```Python
plt.bar(years, apples)
plt.bar(years, oranges, bottom="apples")
```
---
## Heatmap
*Should be in a matrix type format* so we use .pivot*
```Python 
flights_df = sns.load_dataset("flights").pivot("month", "year", "passengers")
```

```Python 
sns.heatmap(flight_df)
```
---
## Multiple Graphs in a grid 
``` Python 
plt.subplots(2,3)
```

***To add space***
```
plt.tight_layout(pad=2)
```

***Editing the graphs***
```Python 
axes[0,0].plot()
axes[0,1].plot
#Just add the numpy index 
```
[[Arrays#Array Indexing and Slicing |Array Indexing]]

---

## Countplot
```Python 
sns.countplot(x="Survived", data = train)
```