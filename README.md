# Amazon-project
```
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

driver=webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.amazon.in/")

time.sleep(2)

driver.find_element(By.ID, "twotabsearchtextbox").send_keys("tv")
driver.find_element(By.ID, "nav-search-submit-button").send_keys(Keys.ENTER)

time.sleep(2)

old_tab=driver.current_window_handle

driver.find_element(By.XPATH,"//span[contains(text(),'Xiaomi (108 cm) 43 inch FX 4K QD-Mini LED Smart | Full Array Local Dimming | HDR10+ | Fire TV | L43MC-FSMIN')]").click()

time.sleep(2)

for tab in driver.window_handles:
    if tab != old_tab:
        driver.switch_to.window(tab)

driver.find_element(By.ID, "add-to-cart-button").click()
time.sleep(3)

driver.find_element(By.NAME, "proceedToRetailCheckout").click()
time.sleep(2)
```
<img width="1917" height="1137" alt="Screenshot 2026-10-07 103930" src="https://github.com/user-attachments/assets/ad412662-2629-4958-83c1-8f8580ff9052" />
<img width="1917" height="1127" alt="Screenshot 2026-10-07 103955" src="https://github.com/user-attachments/assets/f14bfae7-3517-482d-8d01-e369c52ac214" />



