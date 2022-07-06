# Basic Functions 

## Converting to grayscale
```Python
grey = cv.cvtColor(img, cv.COLOR_BGR2GRAY)
```

## Blur
```Python 
blur = cv.GaussianBlur(img, (7,7), cv.BORDER_DEFAULT)
```

## Edge Cascade
Finds the edges in the image
```Python
canny = cv.Canny(img, 125,125)
```