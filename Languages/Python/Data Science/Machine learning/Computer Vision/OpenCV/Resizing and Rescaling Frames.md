# Resizing and Rescaling frames

**Rescaling Frames**
```Python 
def rescale(frame, scale = 0/75):
	width = frame.shape[1] * scale #1 is width
	height = frame.shape[0] * scale #0 is width

	dimensions = (width, height)

	return cv.resize(frame, dimensions, interpolation=cv.INTER_AREA)
```
```Python 
frame_resized = rescaleFrame(frame)
```

**Resizing Frames**
```Python 
def changeres(width,height) : 
	capture.set(3, height)
	capture.set(4,height)
```