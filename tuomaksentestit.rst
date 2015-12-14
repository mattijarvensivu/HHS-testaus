#Pekka narkomaani menee tutkimaan muron sivuja tietääkseen mitä tietotekniikkaa
#pitää nykyään varastaa, että saa rahat aineisiin. Hän hyppää prossut,
#emolevyt ja muistit ketjuun ja valitsee 6 sivun etsien silmillään sanaa uusi
#Tämä testi toimii noin puolet ajasta, tutki asiaa jos haluat

*** Settings ***
Suite Teardown  Close Browser
Library  Selenium2Library  5

*** Test Cases ***
SearchForRobotFramework
    Open Browser  http://murobbs.muropaketti.com/  ff
    Set Selenium Speed  0.5
    Click Element  link=Prosessorit, emolevyt ja muistit
    Click Element  link=6
    Page Should Contain  prosessoreista
    Close Browser



#Pekka narkomani Tajusi ettei hyötynyt äskeisestä yhtään mitään ja meneekin
#tällä kertaa murobbs etusivulta hintavertailuun kirjoittaa sanan kallis

*** Test Cases ***
SearchForRobotFramework
    Open Browser  http://murobbs.muropaketti.com/  ff
    Maximize Browser Window
    Set Selenium Speed  0.5
    Click Element  link=HINTAVERTAILU
    Input Text  q  kallis
    Close Browser
	


#Piri päissään Pekka klikkaa muron työpaikka osiota
#ja pettyy että sieltä päätyy pois sivulta
#Klikkaa kuitenkin sivun linkkkiä keskusteluun

*** Test Cases ***
SearchForRobotFramework
    Open Browser  http://murobbs.muropaketti.com/  ff
    Set Selenium Speed  0.5
    Click Element  link=TYÖPAIKAT
    Click Element  xpath=.//*[@id='inner-wrapper']/div[2]/p[3]/a
    Page Should Contain  Duunitori.fi
    Close Browser
