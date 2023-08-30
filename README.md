# Selenium-Grid-4.11.0 Guide

---------------------For Selenium 4.11.2 and Selenium Grid 4.11------------------------------------------


-----------------------------------------Java-----------------------------------------------------------
Install Java 11 --->

I used  - > jdk-11.0.20_windows-x64_bin.exe


Environment Variable Setup --->
 
Open Environment Variable->  System Variables->  New 

Variable name : JAVA_HOME
Variable value : C:\Program Files\Java\jdk-11 

also,

Open Environment Variable->  System Variables->  Path -> Edit -> New - > Paste

 %JAVA_HOME%\bin



Now goto terminal Type  -->       java -version
It will show your java version

----------------------------------------------------------------------------------------------------------









--------------------------------------------Driver------------------------------------------------------


Replace  ---->

->chromedriver.exe
->msedgedriver.exe
->geckpdriver.exe     drivers accroding to your browser version .

Downloas from here  https://github.com/SergeyPirogov/webdriver_manager

The Run  ---- > 


Standalone Mode ---> java -jar selenium-server-4.11.0.jar standalone    or standalone.bat

Hub Mode--->java -jar selenium-server-4.11.0.jar hub  or hub.bat

Node --->java -jar selenium-server-4.11.0.jar node --port 5555 (change port for different node)


--------------------------------------------------------------------------------------------------------


--------------------------------------------Code Level--------------------------------------------------

Execution Python Code Level Example --->


from selenium import webdriver

#Remove # for driver you want to use

#options = webdriver.FirefoxOptions()
#options = webdriver.ChromeOptions()
#options = webdriver.EdgeOptions()


driver=webdriver.Remote('http://localhost:4444', options=options)

driver.get("https://facebook.com")
print(driver.title)
driver.quit()

------------------------------------------------------------------------------------------------------------