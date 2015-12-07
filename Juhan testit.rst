####### JUHAN TESTIT ########

#User wants to change the theme of the site by clicking the button on the bottom
#of the page.

*** Test Steps ***
SearchForRobotFramework
  Open Browser  http://murobbs.muropaketti.com/
  
  Maximize Browser Window
  
  Click Element  //*[@id="uix_wrapper"]/footer/div[1]/div/div/dl/dd/a
  
  Wait Until Element Is Visible  //*[@id="XenForo"]/body/div[10]/div/ol/li[2]  5
  
  Click Element  //*[@id="XenForo"]/body/div[10]/div/ol/li[2]
  
  Close Browser

#User goes to site and wants to log in. Clicks login and inputs username, password and clicks
#login. Credentials:Testikäyttäjä;testaaja123

*** Test Cases ***
SearchForRobotFramework
  Open Browser  http://murobbs.muropaketti.com/
  
  Maximize Browser Window
  
  Click Element  link=KIRJAUDU
  
  Input Text  id=LoginControl  Testikäyttäjä
  
  Input Password  id=ctrl_password  testaaja123
  
  Click Element  //*[@id="login"]/div/dl[3]/dd/input
  
  Element Should Contain  //*[@id="navigation"]/div/div/div/nav/div/ul[3]/li[1]/a/strong[1]  Testikäyttäjä
  
  Close Browser
  
# User checks how to input cool emojis xD #

*** Settings ***
Suite Teardown  Close Browser
Library  Selenium2Library

*** Test Cases ***
SearchForRobotFramework
  Open Browser  http://murobbs.muropaketti.com/
  
  Maximize Browser Window
  
  Click Element  link=Käyttöehdot
  
  Click Element  link=Hymiöt
  
  Element Should Contain  //*[@id="content"]/div/div/div[3]/div/div/div[3]/div[$
  
  Close Browser

