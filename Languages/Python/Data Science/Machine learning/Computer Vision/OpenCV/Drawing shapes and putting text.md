# Drawing shapes and putting text

**Creating a blank image**
```Python 
blank = np.zeros((500,500) dtype="unit8")
```

**Changing color of the image**
```Python
variable[:] = R,G,B #Selects all the pixel in the image 
```

**Drawing a rectangle**
```Python 
cv.rectangle(variable, (origin), (end), (color), thickness=2)
```

**Drawing a line**
```Python 
cv.line(image, (point1), (point2), (color), thickness=1)
```

**Text**
```Python 
cv.putText(image, "Hello", (255,255), cv.FONT_FONT, 1.0, (0,255,0), 2)
```