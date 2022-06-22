# Numpy and CSV
<aside>💡 CSV stands for comma seperated values and is a way to store data in text files</aside>

---
### CSV to Numpy [[Arrays]] 
```Python 
climate_data = np.genfromtxt("example.txt", delimiter=",", skip_header=1)
```
*skip_header is for skipping the first line as it includes the field names 
delimiter is the seperator*

---
### Exporting to CSV
```Python 
np.savetxt('climate_results.txt', #Filename
     climate_results, #Array
     fmt='%.2f', #Decimal Points
     delimiter=',', #Delimiter
     header='temperature,rainfall,humidity,yeild_apples'), #Field Names
```