# Reading Images and Video 
**Importing**
```Python 
import cv2 as cv
```
---
## Images 
**Creating a variable with the image**
```Python 
img = cv.imread("Path")
```

**Showing the image**
```Python 
cv.imshow('Title', img)
```
---
## Videos
**Creating a variable with the video**
```Python
vid = cv.VideoCapture("path")
```

**Using webcam**
```Python
vid = cv.VideoCapture(0) #Change integer to change camera
```

**Viewing the video**
```python 
while True, 
	isTrue, frame = capture.read
```

To view the video we view the frames
```Python
cv.imshow("title", frame)
```