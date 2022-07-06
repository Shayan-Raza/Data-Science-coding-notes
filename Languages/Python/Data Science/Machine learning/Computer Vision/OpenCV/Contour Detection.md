# Contour Detection
Contours are boundaries of objects

1: Convert to grayscale
![[Basic Functions#Converting to grayscale]]

2: Blur
![[Basic Functions#Blur]]

3:Canny 
![[Basic Functions#Edge Cascade]]

4: Finding number of contours
```Python 
contours, hierarchies = cv.findContours(canny, cv.RETR_LIST, cv.CHAIN_APPROX_SIMPLE)

print(f'{len(contours)} contour(s) found!')
```

5: Image with contours
```Python
cv.drawContours(blank, contours, -1, (0,0,255), 1)
```