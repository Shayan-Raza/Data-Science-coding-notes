# Blurring
## Averaging

*The pixel intensity is the average of the pixel intensity of the surrounding pixels*
```Python
average = cv.blur(img, (3,3))
```

## Gaussian Blur

*More natural*
```Python
gauss = cv.GaussianBlur(img, (3,3), 0)
```

## Median Blur

*Similar to averaging but instead of finding the average finds the median*
```Python
median = cv.medianBlur(img, 3)
```

## Bilateral

*Applies blurring but retains the edges.*
```Python
bilateral = cv.bilateralFilter(img, 10, 35, 25)
```
