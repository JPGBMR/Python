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

def ClickImg(img_path=None):

        if img_path is not None:
            img_path = img_path
            
        coords = pag.locateOnScreen(img_path)
        if coords is None:
            print('Image not found on the screen!')
        else:
            print(f"Imagen encontrada en: {coords}")
            l,x,w,y = coords
            pag.click(coords,clicks=1)

```
