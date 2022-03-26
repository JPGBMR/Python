# Python_pyautogui <img src="https://media.giphy.com/media/dxn6fRlTIShoeBr69N/giphy.gif" width="45">

Surface Automation using pyautogui

## Setup & Instalación

Instalar ultima version de Python y VSCode

```bash
pip install pyautogui
```

```bash
pip install opencv-python
```

```bash
pip install pyperclip
```

```javascript
import pyautogui as pt
from time import sleep


while True:
    posXY = pt.position()
    print(posXY, pt.pixel(posXY[0], posXY[1]))
    sleep(1)
    if posXY[0] == 0:
        break
```

#Drawing


```javascript
import pyautogui
import math
from time import sleep

""" 
while True:
    posXY = pt.position()
    print(posXY, pt.pixel(posXY[0], posXY[1]))
    sleep(1)
    if posXY[0] == 0:
        break """


r = 100
centrex = 510
centrey = 426

y = centrey - r
x = math.sqrt((r ** 2) - ((y - centrey) ** 2)) + centrex

oldx = x
oldy = y

for i in range(r):
    pyautogui.moveTo(x, y)
    x = math.sqrt((r ** 2) - ((y - centrey) ** 2)) + centrex
    pyautogui.dragTo(x, y)
    tempx = centrex - math.sqrt((r ** 2) - ((y - centrey) ** 2))
    tempoldx = centrex - math.sqrt((r ** 2) - ((oldy - centrey) ** 2))
    pyautogui.moveTo(tempoldx, oldy)
    pyautogui.dragTo(tempx, y)
    pyautogui.dragTo(x, y) # comment this line if you want to disable fill

    oldx = x
    oldy = y

    y = y + 0.5
```

Click and Mouse Move

```javascript
import pyautogui as pt
import keyboard
from time import sleep
import pyperclip

def MoveTo():
    global x, y
    x = 39
    y = 244
    pt.moveTo(x,y, duration=0.05)
    pt.click()
    pt.rightClick()

```
