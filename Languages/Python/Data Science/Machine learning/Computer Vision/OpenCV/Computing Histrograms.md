# Computing Histogram
Histograms allow you to visualize pixel densities.

## Grayscale histogram
```Python
gray_hist = cv.calcHist([gray], [0], mask, [256], [0,256]) #gray is the image converted to grayscaleO 
#If you dont wanna use a mask use None

plt.figure()
plt.title('Grayscale Histogram')
plt.xlabel('Bins')
plt.ylabel('# of pixels')
plt.plot(gray_hist)
plt.xlim([0,256])
plt.show()
```

## Color Histogram
```Python
plt.figure()
plt.title('Colour Histogram')
plt.xlabel('Bins')
plt.ylabel('# of pixels')
colors = ('b', 'g', 'r')

for i,col in enumerate(colors):
	hist = cv.calcHist([img], [i], mask, [256], [0,256])
	plt.plot(hist, color=col)
	plt.xlim([0,256])

plt.show()
```MANGOHUD_DLSYM=1