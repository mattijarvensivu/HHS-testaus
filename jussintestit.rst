#### JUSSIN TESTIT ######
	
#Tero haluaa lukea murobbs tarjous-keskustelun uusimmat viestit,
#hän avaa bbs.muropaketti.com sivun, ja avaa "rauta" alueen,
#sieltä hän avaa parhaat tarjoukset ketjun, josta hän avaa uusiman sivun 178

*** Test Cases ***

SearchForRobotFramework

    Open Browser  http://murobbs.muropaketti.com/  ff
    
    Maximize Browser Window
    
    Set Selenium Speed  0.5
    
    Click Element  link=Rauta
    
    Click Element  link=Hyvät tarjoukset ketju v2.0
    
    Click Element  link=178
    
    Page Should Contain  tarjous
    
    Close Browser
    
#Tero päättää  että juuri nyt on päästä lukemaan sivuston käyttöoikeudet,
#jonka jälkeen hän avaa käyttöoikeudet sivun, sen jälkeen hän katsoo mitä,
#cookieita sivusto,tallentaa käyttäjän rekisteröityessä.

*** Test Cases ***

SearchForRobotFramework

    Open Browser  http://murobbs.muropaketti.com/  ff
    
    Maximize Browser Window
    
    Set Selenium Speed  0.5
    
    Click Element  link=Käyttöehdot
    
    Page Should Contain  Ylivoimainen este (force majeure)
    
    Click Element  link=Cookiet eli evästeet
    
    Page Should Contain  Näitä tietoja ei välitetä eikä anneta mihinkään.
    
    Close Browser

#Tero menee murobbs sivulle ja haluaa käyttää hakua jotta löytää keskustelu,
#ketjun älykelloista, hän avaa keskustelun ja etsii sivulta tekstiä moto 360.

*** Test Cases ***

SearchForRobotFramework

    Open Browser  http://murobbs.muropaketti.com/  ff
    
    Click Element  link=Hae alueilta
    
    Input Text  keywords  älykello
    
    Press Key  keywords  \\13
    
    Click Element  xpath=//*[@id="post-1716389851"]/div[2]/div[1]/h3/a
    
    Page Should Contain  moto 360
    
    Close Browser
