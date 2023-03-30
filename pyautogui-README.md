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

#Get Coordinates

```javascript
import pyautogui as pag
from time import sleep


while True:
    posXY = pag.position()
    print(posXY, pag.pixel(posXY[0], posXY[1]))
    sleep(1)
    if posXY[0] == 0:
        break
```

#Click and Mouse Move

```javascript
import pyautogui as pag

def MoveTo():
    global x, y
    x = 330
    y = 330
    pag.moveTo(x,y, duration=0.05)
    pag.click()
    pag.rightClick()

```
#Click Image

```javascript
import pyautogui as pag
from datetime import datetime
from time import sleep

img_path = r"C:\Users\Desktop\Screenshot.jpg"

def click_img(img_path,timeout,confidence=0.8):
        initial_time=datetime.now()
        imagen=None
        while (datetime.now()-initial_time).seconds<timeout and imagen is None:
            sleep(0.3)
            try:
                imagen= pag.locateCenterOnScreen(img_path,grayscale=True,confidence=confidence)
            except:
                print('Image not found on the screen!')
                continue
            sleep(0.3)
            pag.moveTo(imagen,duration=0.25)
            pag.click()
        
click_img(img_path,timeout=3)
```
