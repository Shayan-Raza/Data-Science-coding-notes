# Masking

## Create a blank image
![[Drawing shapes and putting text#Creating a blank image]]

## Create shape 
![[Drawing shapes and putting text#Drawing a rectangle]]

## Merge the shape 
![[Bitwise Operators#bitwise AND]]

## Create the mask
```Python 
masked = cv.bitwise_and(img,img,mask=weird_shape)
```