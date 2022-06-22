# Web Scraping 
We will use the Beautiful Soup library
``` Python 
from bs4 import BeautifulSoup
```
---
### Setup
```Python 
soup = BeautifulSoup(content, "lxml")
```
### Finding a tag 
*.find for first match 
.find_all for all matches*
``` Python 
soup = BeautifulSoup(content, "lxml")
tags = soup.find_all("Tag")
```
### Finding a class
```Python 
soup = BeautifulSoup(content, "lxml")
tags = soup.find_all("div" class_="card")

for tag in tags: 
	print(tag.h1) #After the dot any tag u want the results for
```
---
### Getting from an online website 
*Use the requests library*
``` Python 
import requests
html = requests.get("url").text
```
#### Example
```Python 
from bs4 import BeautifulSoup

import requests

  

#Get the HTML

html = requests.get("https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2380057.m570.l1313&_nkw=PS5&_sacat=0").text

  

#Use Beautiful soup and find the price

soup=BeautifulSoup(html, "lxml")

tags = soup.find_all("span", class_="s-item__price") #In the span with the class price

#Save to the file

with open("/home/shayan/Desktop/Code/Test/results.txt", "w") as f:

#Loop to get every price in the page

for tag in tags:

f.write(f"{tag.text}\n") #\n for newline after every price
```