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

Ja sitten suoritus, joka tapahtui seuraavasti:

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

Vanhan labran tehtävänanto löytyy täältä: [Final Lab for Linux Palvelimet 2024 Spring](https://terokarvinen.com/2024/arvioitava-laboratorioharjoitus-2024-linux-palvelimet/)

### Ei kolmea sekoseiskaa

Kansio "raportit" polkuun /home/ap ja kansion sisään tiedosto "raportti".

![image](https://github.com/user-attachments/assets/a7b99973-6a1b-444d-9274-566a062f3f6e)

![image](https://github.com/user-attachments/assets/ca0282ca-4eea-4a00-a673-d525c3d72598)

raportti -tiedoston oikeudet pois käyttäjiltä 'group' ja 'others'

![image](https://github.com/user-attachments/assets/dcf17c13-6a77-4c1b-ae0c-3d8b011f3e12)

kansion 'raportit' oikeuksien tarkastus

![image](https://github.com/user-attachments/assets/16ddea04-f7c9-4bc5-b207-97d0742657db)

poistetaan vielä kansion oikeudet käyttäjiltä 'group' ja 'others'

![image](https://github.com/user-attachments/assets/439238c5-fa59-4ea6-aa38-8ab348e927f8)

### 'howdy'

Tiedosto kotihakemistoon /home/ap komennolla `micro howdy`

Tulostaa näytölle käyttäjänimen, päivämäärän, kellonajan ja tietokoneen isäntänimen

![image](https://github.com/user-attachments/assets/539072d1-1fed-4999-9f7d-3d1eb42dca3c)

`chmod ugo+x howdy` käyttäjille user,group,others suoritusoikeudet

`sudo cp -v howdy /usr/local/bin` kopioidaan tiedosto polkuun /usr/local/bin, jotta se on kaikkien käyttäjien ajettavissa

![image](https://github.com/user-attachments/assets/9cb8103b-68bb-47c0-a309-f619220de49a)

### Etusivu uusiksi

Asensin uuden virtuaalikoneen tehtävää varten aiemman raporttini [h1-oma-linux](https://github.com/arilep/h1-Oma-Linux/blob/main/h1-oma-linux.md) mukaisesti (osio a).

Päivitysten ajo `sudo apt-get update`

Tämän jälkeen Apachen asennus:

`sudo apt-get install apache2`

Testataan että selain vastaa localhost-osoitteesta:

![image](https://github.com/user-attachments/assets/89354b92-8447-4580-8d31-6349d57f02af)

Asennetaan micro helpottamaan työskentelyä `sudo apt-get install micro`

siirrytään polkuun /var/www/html, poistetaan vanha index.html tiedosto ja luodaan uusi tilalle `sudo rm index.html` `micro index.html`

Lisätään tiedot uuteen index.html -tiedostoon:

![image](https://github.com/user-attachments/assets/c725b4aa-7067-4576-9341-997ce8511066)

Potkaistaan demonia `sudo systemctl restart apache2`, haetaan IP-osoite komennolla `hostname -I` ja testataan syöttää IP-osoite selaimeen:

![image](https://github.com/user-attachments/assets/f9b2e00c-46ab-4bcc-930c-0e09e6585c01)

Sivustoa pitää pystyä muokkaamaan normaalikäyttäjän oikeuksin ilman sudoa. Tämä onnistuu esimerkiksi ajamalla komento `sudo chown -R ap:ap index.html`

### Salattua hallintaa

Asennetaan ssh-palvelin

`sudo apt-get install openssh-server`

Tämän jälkeen lisäsin uuden käyttäjän 'aptesti01': `sudo adduser aptesti01` ja syötin tarvittavat tiedot.

Vaihdetaan käyttäjää

![image](https://github.com/user-attachments/assets/03ca8e5f-adf4-4264-9029-d09deea1ebfc)

Luodaan ssh-avain

![image](https://github.com/user-attachments/assets/e57ebecb-4495-4b82-957c-f9215d5bff9c)

Avaimen lisäys palvelimelle:

![image](https://github.com/user-attachments/assets/c0acbee8-60e8-422f-ab62-1b1f2bbb672d)

Testaus:

![image](https://github.com/user-attachments/assets/bd755291-8c7a-4f2d-abfa-58442a610c9f)


### Lähteet

Karvinen, T. 12.3.2024. Final Lab for Linux Palvelimet 2024 Spring. Luettavissa: https://terokarvinen.com/2024/arvioitava-laboratorioharjoitus-2024-linux-palvelimet/. Luettu 9.3.2025.

Karvinen, T. 12.3.2024. h7 Maalisuora. Luettavissa: https://terokarvinen.com/linux-palvelimet/#h7-maalisuora. Luettu 9.3.2025.

Karvinen, T. 27.9.2018. Hello World Python3, Bash, C, C++, Go, Lua, Ruby, Java – Programming Languages on Ubuntu 18.04. Luettavissa: https://terokarvinen.com/2018/hello-python3-bash-c-c-go-lua-ruby-java-programming-languages-on-ubuntu-18-04/. Luettu 9.3.2025.

Karvinen, T. 4.12.2007. Shell Scripting. Luettavissa: https://terokarvinen.com/2007/12/04/shell-scripting-4/. Luettu 9.3.2025.

Stack overflow. s.a. "Variable out of type PrintStream" error occured. Luettavissa: https://stackoverflow.com/questions/9298980/variable-out-of-type-printstream-error-occured. Luettu 9.3.2025.

SSH Academy. s.a. SSH Copy ID for Copying SSH Keys to Servers. Luettavissa: https://www.ssh.com/academy/ssh/copy-id. Luettu 9.3.2025.

Orace Help Center. s.a. Generate an SSH Key Pair. Luettavissa: https://docs.oracle.com/en/cloud/cloud-at-customer/occ-get-started/generate-ssh-key-pair.html. Luettu 9.3.2025.


