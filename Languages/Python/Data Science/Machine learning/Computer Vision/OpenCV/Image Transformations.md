# Image Transformations
## Translation
Shifting the image
```Python 
def translate(img, x, y) :
	transMat = np.float32([[1,0,x], [0,1,y]])
	dimensions = (img.shape[1], img.shape[0])
	return cv.wrapAffine(img, transMat, dimensions) 
```
```Python 
translated = translate(img, 100, 100)
```
```Python 
# -x -> Left
# -y -> Up 
# x -> Right
# y -> Down
```


## Rotation 
```Python 
def rotate(img, angle, rotpoint) :
	(height, width) = img.shapep[:2]

	if rotpoint is None: 
		rot point = (width//2, height//2)
	
	rotMat = cv.getRotationMatrix2D(rotPoint, angle, 1) #Value 1 is scale
	dimensions = (width, height)
	
	return cv.WrapAffine(img, rotMat, dimensions) 
```
```Python 
rotated = rotate(img, 45)
```

## Flipping 
```Python 
flip = cv.flip(img, -1)
```

## Cropping 
```Python
cropped = img[200:400. 300:400]
```
