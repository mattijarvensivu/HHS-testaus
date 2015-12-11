 ### MATIN TESTIT
  # Pekka menee muropakettiin ja haluaa nähdä lisää artikkeleita ja klikkaa  
  
  # kohtaa lisää artikkeleita ja klikkaa ensimmäistä ilmestynyttä artikelia  

*** Test Cases ***  

SearchForRobotFramework  

    Open Browser  http://muropaketti.com  ff  
    
    Maximize Browser Window  
    
    Set Selenium Speed  0.5  
    
    Click Element  xpath=//*[@id="inner-wrapper"]/div[2]/div[2]/a  
    
    Click Element  xpath=//*[@id="grid-566576440d8fd"]/ul/li[1]  
    
    Close Browser

 
# pekka päättää mennä murobbssään ja etsiä ADATAN usb muisteja joten hän menee  

# murobbs.muropaketti.comiin ja painaa hintavertailu jonka jälkeen  

# etsii alhaalta usb muistit ja klikkaa sitä  

# Pekka haluaa pelkästään nähdä ADATAN muisteja joten hän klikkaa valmistajista ADATA ja  

# painaa päivitä tuotelistausnappia  

*** Test Cases ***  

SearchRobotFramework  

    Open Browser  http://murobbs.muropaketti.com/  ff  
    
    Set Selenium Speed  0.5  
    
    Click Element  link=HINTAVERTAILU  
    
    Click Element  xpath=//*[@id="hv-page"]/section[3]/nav/ul[2]/li[17]/a  
    
    Click Element  xpath=//*[@id="hvjs-filter_manufacturer"]/ul/li[1]/label  
    
    Click Element  xpath=//*[@id="hvjs-form-filter"]/div[2]/ul[1]/li/a
    
# Pekka Haluaa Hakea tietoa window 10stä ja klikkaa ylhäältä haku kuvaketta ja valitsee sieltä tarkennetun haun  

# Sinne pekka kirjoittaa hakukenttään windows 10 ja saaduista hauista valitsee kuudennen sivun   

*** Test Cases ***  

SearchForRobotFramework  

    Open Browser  http://murobbs.muropaketti.com/  ff  
    
    Set Selenium Speed  1  
    
    Click Element  xpath=//*[@id="QuickSearchQuery"]  
    
    Wait Until Element Is Visible  xpath=//*[@id="QuickSearch"]/form/div[2]/dl/dd/a  
    
    Click Element  xpath=//*[@id="QuickSearch"]/form/div[2]/dl/dd/a  
    
    Input Text  xpath=//*[@id="ctrl_keywords"]  windows 10  
    
    Click Element  xpath=//*[@id="content"]/div/div/div[3]/div/div/form/dl[5]/dd/input  
    
    Click Element  xpath=//*[@id="content"]/div/div/div[3]/div/div/div[3]/div[2]/nav/span/span/a[5]
