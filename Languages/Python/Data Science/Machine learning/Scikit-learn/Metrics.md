# Metrics
## GridSearchCV
Finds the best parameters for model

**Importing**
```Python 
from sklearn.model_selection import GridSearchCV
```

**Using it**
```Python 
grid = GridSearchCV (
					 estimator=model,
					 param_grid {Dictionary with parameters},
					 cv= number of cross validations
					 n_jobs = number of cores
)
```

**Result**
```Python 
pd.DataFrame(grid.cv_results)
```

## Precision score
The precision is the ratio `tp / (tp + fp)` where `tp` is the number of true positives and `fp` the number of false positives. The precision is intuitively the ability of the classifier not to label as positive a sample that is negative.

The best value is 1 and the worst value is 0.

**Importing**
```Python 
from sklearn.metrics import precision_score
```

**Using it**
```Python 
precision_score(y, grid.predict(x))
```

## Recall score
The recall is the ratio `tp / (tp + fn)` where `tp` is the number of true positives and `fn` the number of false negatives. The recall is intuitively the ability of the classifier to find all the positive samples.

The best value is 1 and the worst value is 0.

**Importing**
```Python
from sklearn.metrics import recall_score
```

**Using it**
```Python 
precision_score(y, grid.predict(x))
```