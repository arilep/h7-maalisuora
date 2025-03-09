### H7-Maalisuora: [Tehtävänanto](https://terokarvinen.com/linux-palvelimet/#h7-maalisuora)

## Tehtävissä käytetty ympäristö

- Käyttöjärjestelmä: Windows 11 Home 64-bit
- Suoritin: AMD Ryzen 7 5800X 8-Core Processor
- Muisti: 32GB RAM
- Näytönohjain: NVIDIA GeForce RTX 3080
- Virtualisointiohjelmisto: Oracle VM VirtualBox 7.0

- Internet yhteys: DNA Netti 400M (Download 400Mbps / Upload 200Mbps)

## Tehtävä-A
Aloitin osion 9.3.2025 noin klo: 15:45

Ensi alkuun päivitin paketit `sudo apt-get update`

Tehtävänannon vinkeistä silmäilin eri ohjelmointikieli vaihtoehtoja ja valikoin sieltä seuraavat: python, java ja lua.
Jatkoin ajamalla komennon `sudo apt-get install python3 openjdk-17-jdk lua5.4`

"After this operation, 283 MB of additional disk space will be used. Do you want to continue? [Y/n]" kohtaan vastasin 'y'. Asennus kesti muutamia sekunteja.

### Java

Päätin aloittaa javalla. /home/ap/ hakemistoon loin tiedoston ajamalla komennon `micro HelloWorld.java`.

Kyseiseen tiedostoon kirjasin seuraavaa:

![image](https://github.com/user-attachments/assets/fe1b996d-23ee-4fdb-81cd-f2b98d483807)

Ctrl+S tallennus ja sitten Ctrl+Q takaisin terminaaliin.

Ajoin komennon `javac HellowWorld.java` ja sain seuraavanlaisen virheilmoituksen:

![image](https://github.com/user-attachments/assets/b3473ab9-16e1-468b-8abe-92a8dd846954)

Google haulla "linux java error variable out of type PrintStream" löysin ratkaisun Stack Overflow -sivustolta (https://stackoverflow.com/questions/9298980/variable-out-of-type-printstream-error-occured).

Ongelmana oli perus aloittelijan moka (=typo). System.out.println "print" sanan jälkeen pieni L, eikä i kirjainta.

Kävin korjaamassa kyseisen kirjoitusvirheen. Tämän jälkeen `javac HelloWorld.java` meni läpi ja ajoin komennon `java HelloWorld`.

![image](https://github.com/user-attachments/assets/5a54109d-0376-41bf-98c2-e305935ff7c5)

### Python

Python olikin itselleni jo aiemmin tuttu. Vaiheet olivat aika helpot.

`micro helloworld.py`, editoriin koodi `print("tekstitähän")`, tallennus Ctrl+S ja takaisin terminaaliin Ctrl+Q.

![image](https://github.com/user-attachments/assets/5fcccf85-e8b8-4d38-813b-b6dee0345cb0)

Suoritetaan komennolla `python3 tiedostonimi`

![image](https://github.com/user-attachments/assets/aa74e337-d3f2-44ee-989b-7eae4b21e704)

### Lua

Ja viimeisenä Lua, joka oli yllätyksekseni vaiheiltaan lähes identtinen Pythonin kanssa.

`micro helloworld.lua`

![image](https://github.com/user-attachments/assets/06767a19-2d18-45c7-a416-cf95fde139a4)

![image](https://github.com/user-attachments/assets/ee7a7ed4-9f0f-4ca2-9cc4-1e8ccde47fac)

### C++

Päätin testata vielä C++ jota en ollut aikaisemmin kokeillut. Asennus tapahtuu `sudo apt-get install g++`

Tiedostonimi päättyy .cc

![image](https://github.com/user-attachments/assets/0aae7062-aca5-4d98-aeb8-f82dfd9b3300)

Editoriin sisältö:

![image](https://github.com/user-attachments/assets/a92d2955-8fa7-46a6-8dcf-1d694afc0606)

Ja sitten suoritus

![image](https://github.com/user-attachments/assets/a7f89159-1bef-4071-8c80-4904830a6b5f)

Osio valmis noin 16:15.

## Tehtävä-C
Osio vei aikaa 5-10min.

Luodaan tiedosto "jekku" --> `micro jekku`

![image](https://github.com/user-attachments/assets/1ee21469-d97b-4697-8d00-c5f7a3d0f16e)

Tarkistetaan ja lisätään oikeudet tiedostolle. `ls -lh` listaa polussa tiedostot oikeuksineen, `chmod a+x tiedostonimi` antaa kaikille käyttäjille suoritusoikeuden kyseiseen tiedostoon.

![image](https://github.com/user-attachments/assets/d173db3a-ced5-45bc-8389-d268200d95f4)

Oikeudet päivitelty, jonka jälkeen kopioin tiedoston polkuun /usr/local/bin jotta se on kaikkien käyttäjien ajettavissa.

![image](https://github.com/user-attachments/assets/93df1e4e-d14b-4523-a370-3b5ca8cd8997)

Ja sitten jekku käyntiin:

![image](https://github.com/user-attachments/assets/31118f2c-c709-4164-9b72-db81beb48093)

Ja hetken päästä...

![image](https://github.com/user-attachments/assets/8355911d-f174-4eb9-a0a4-fe637e1403dc)

## Tehtävä-D


## Tehtävä-E

### Lähteet
https://stackoverflow.com/questions/9298980/variable-out-of-type-printstream-error-occured
