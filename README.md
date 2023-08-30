# Selenium-Grid-4.11.0 Guide

---------------------For Selenium 4.11.2 and Selenium Grid 4.11------------------------------------------

Replace  ---->

->chromedriver.exe
->msedgedriver.exe
->geckpdriver.exe     drivers accroding to your browser version .


The Run  ---- > 


Standalone Mode ---> java -jar selenium-server-4.11.0.jar standalone    or standalone.bat

Hub Mode--->java -jar selenium-server-4.11.0.jar hub  or hub.bat

Node --->java -jar selenium-server-4.11.0.jar node --port 5555 (change port for different node)


Execution Python Code Level --->


from selenium import webdriver

#Remove # for driver you want to use

#options = webdriver.FirefoxOptions()
#options = webdriver.ChromeOptions()
#options = webdriver.EdgeOptions()


driver=webdriver.Remote('http://localhost:4444', options=options)

driver.get("https://facebook.com")
print(driver.title)
driver.quit()


 
