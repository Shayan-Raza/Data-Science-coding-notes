# Bash
**Start**
```
#! /bin/bash
```

**Comments**
Start with #

**Printing**
```
echo
```

**Command**
Are to be typed normally

**Quitting**
```
Exit
```

**Variables**
```
varibable = variable
```

**Command variable**
```
variable = "$(command)"
```

**Functions**
```
function() { 
	commands
}
```

**If else elif**
calls a function based on variable 
```
if [ "$desktop" == "GNOME" ]; then
	gnome
elif [ "$desktop" == "KDE" ]; then
	kde
elif [ "$desktop" == "XFCE4" ]; then
	xfce
elif [ "$desktop" == "Cinnamon" ]; then
	cinnamon
elif [ "$desktop" == "MATE" ]; then
	mate
elif [ "$desktop" == "LXQT" ]; then
	lxqt
elif [ "$desktop" == "Deepin" ]; then
	deepin
elif [ "$desktop" == "AwesomeWM" ]; then
	awesome
elif [ "$desktop" == "bspwm" ]; then
	bspwm
elif [ "$desktop" == "dwm" ]; then
	dwm
elif [ "$desktop" == "i3" ]; then
	i3
else
	echo "DE not found"
	exit 0
fi
```