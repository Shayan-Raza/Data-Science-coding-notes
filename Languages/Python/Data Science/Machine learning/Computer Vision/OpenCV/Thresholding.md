# Thresholding
## Simple Thresholding
```
threshold, thresh = cv.threshold(gray, 150, 255, cv.THRESH_BINARY )
```

*Inverse*
```
threshold, thresh_inv = cv.threshold(gray, 150, 255, cv.THRESH_BINARY_INV )
```

## Adaptive Thresholding
```
adaptive_thresh = cv.adaptiveThreshold(gray, 255, cv.ADAPTIVE_THRESH_GAUSSIAN_C, cv.THRESH_BINARY_INV, 11, 9)
```
