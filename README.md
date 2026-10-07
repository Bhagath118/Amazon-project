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
<img width="1902" height="1007" alt="Screenshot 2026-10-07 112056" src="https://github.com/user-attachments/assets/4908bac3-bca9-4bea-9077-e1b697028e94" />
<img width="1915" height="1013" alt="Screenshot 2026-10-07 112043" src="https://github.com/user-attachments/assets/35fc78c9-8787-485a-b8f4-7b131011e121" />



