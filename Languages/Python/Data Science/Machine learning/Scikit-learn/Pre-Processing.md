# Pre-Processing
## Standard Scaler
Standardizes a feature by subtracting the mean and then scaling to unit variance.

##### Using standard scaler
*Importing*
```Python 
from sklearn.preprocessing import StandardScaler
```

*Using it*
```Python 
x = StandardScaler().fit_transform(X)
```

| Before | After |
| ------ | ----- |
|![[Pasted image 20220622111257.png]]        |![[Pasted image 20220622111318.png]]       |


## Quantile Transformer
Used for removing outliers

##### Using Quantile Transformer
*Importing*
```Python 
from sklearn.preprocessing import QuantileTransform
```

*Using it*
```Python 
x = QuantileTransform().fit_transform(X)
```

*Result*
| Before | After |
| ------ | ----- |
|![[Pasted image 20220622111158.png]]        |![[Pasted image 20220622111228.png]]       |

## One-hot encoder
Converts string values into binary

##### Using One-hot encoder
*Importing*
```Python 
from sklearn.preprocessing import OneHotEncoder
```

*Using it*
```Python
enc = OneHotEncoder
enc.fir_transform(df)
```

*Result*
| Before | After |
| ------ | ----- |
| ![[Pasted image 20220622111913.png]]       |![[Pasted image 20220622111932.png]]       |
