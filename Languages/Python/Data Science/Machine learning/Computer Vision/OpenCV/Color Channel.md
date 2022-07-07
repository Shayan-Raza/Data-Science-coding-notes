# Color Channel

## Splitting an image into its colors 
```Python 
b,g,r = cv.split(img)
```

## Merging the images
```Python
merged = cv.merged([b,g,r])
```