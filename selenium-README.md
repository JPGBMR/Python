# Python_Selenium_Intro <img src="https://media.giphy.com/media/dxn6fRlTIShoeBr69N/giphy.gif" width="45">

Introducción a Selenium con Python...

Instalacion:

```bash
pip install selenium
```
Uso:

```bash
# Selenium Python
#   Chrome_WebDriver link: https://chromedriver.storage.googleapis.com/index.html (CHROME VERSION!)
#   Selenium Doc https://www.selenium.dev/documentation/en/

from selenium import webdriver
from selenium.webdriver.common.keys import Keys

RUTA = r"/Users/JuanPablo/Documents/selenium/chromedriver"
driver = webdriver.Chrome(RUTA)

# Lanzar Nav
driver.get("https://www.selenium.dev/")
driver.implicitly_wait(5) # Alternativamente --> (Import time - time.sleep(x))

# Interactuar con elem
elem = driver.find_element_by_class_name("headerLink") # 'headerLink' depende del elem
driver.click()
driver.send_key("asdf")
```
