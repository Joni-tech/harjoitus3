## a) MarkDown. Tee tämän tehtävän raportti MarkDownina. Helpointa on tehdä raportti GitHub-varastoon, jolloin md-päätteiset tiedostot muotoillaan automaattisesti. Tyhjä rivi tekee kappalejaon, risuaita ‘#’ tekee otsikon, sisennys merkitsee koodinpätkän.

### Repositoryn luominen

Tein aluksi GitHubissa uuden repositoryn nimeltä harjoitus3. Lisenssiksi valitsin GNU GPL3 v3.0, minkä lisäksi pistin ruksin kohtaan, josta sai valittua automaattisen README -tiedoston luonnin. Repositoryn tilaksi valitsin Publicin ja klikkasin "Create Repository". 
Repository luotiin osoitteeseen:  https://github.com/Joni-tech/harjoitus3
Repositoryn luomisen jälkeen siirryin terminaaliin, missä päivitin ensin paketit ja asensin gitin:

**sudo apt-get update**

**sudo apt-get -y install git**


Kloonasin juuri luomani repositoryn koneelleni komennolla:

**git clone https://github.com/Joni-tech/harjoitus3.git**


Käyttäjän kotihakemistoon luotiin repositoryn nimeä kantava kansio (harjoitus3). Kansio sisälsi samat tiedostot (LICENCE ja README), mitkä näkyivät GitHubin verkkosivuillakin, olihan kyseessä klooni. Loin kansioon tiedoston, johon aloin kirjoittamaan tätä raporttia: 

**nano harjoitus3/raportti3.md**


Saatuani tekstiä raporttiin, päivitin tekemäni muutokset komennolla:

**$ git add . && git commit; git pull && git push**

Kyseinen komento synkronoi tehdyt  muutokset kaikkien projektiin osallistuvien kesken, jolloin kaikilla on saatavilla viimeisimmät versiot tiedostoista. Samalla voidaan kommentoida tapahtuneita muutoksia (commit).

https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet


## d) Näytä omalla git-varastollasi esimerkit komennoista ‘git log’, ‘git diff’ ja ‘git blame’. Selitä tulokset.

## e) Tee tyhmä muutos gittiin, älä tee commit:tia. Tuhoa huonot muutokset ‘git reset –hard’. Huomaa, että tässä toiminnossa ei ole peruutusnappia.

## f) Tee uusi salt-moduli. Voit asentaa ja konfiguroida minkä vain uuden ohjelman: demonin, työpöytäohjelman tai komentokehotteesta toimivan ohjelman. Käytä tarvittaessa ‘find -printf “%T+ %p\n”|sort’ löytääksesi uudet asetustiedostot. (Tietysti eri ohjelma kuin aiemmissa tehtävissä, tarkoitushan on harjoitella Salttia)
