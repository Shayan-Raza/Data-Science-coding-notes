# Face Detection
## 1: Convert to grayscale
![[Color Spaces#BGR to Grayscale]]

## 2: Haar cascade
[Github Link](https://github.com/opencv/opencv/tree/4.x/data/haarcascades)
```Python 
haar_cascade = cv.CascadeClassifier('haar_face.xml')
```

## 3: Detection 
```Python 
faces_rect = haar_cascade.detectMultiScale(gray, scaleFactor=1.1, minNeighbors=1)
```

## 4: Creating a rectangle
*Around the face*
```Python 
for (x,y,w,h) in faces_rect:
	cv.rectangle(img, (x,y)(x+w,y+h), 
    (0,255,0), thickness=2)
```