Aloitin tehtävien tekemisen 20.4.2020 klo 22:15 (UTC +3)

Käyttämäni komennot on poimittu Tero Karvisen ohjeista: http://terokarvinen.com/2016/publish-your-project-with-github

## a) MarkDown. Tee tämän tehtävän raportti MarkDownina. Helpointa on tehdä raportti GitHub-varastoon, jolloin md-päätteiset tiedostot muotoillaan automaattisesti. Tyhjä rivi tekee kappalejaon, risuaita ‘#’ tekee otsikon, sisennys merkitsee koodinpätkän.

### Repositoryn luominen

Tein aluksi GitHubissa uuden repositoryn nimeltä harjoitus3. Lisenssiksi valitsin GNU GPL3 v3.0, minkä lisäksi pistin ruksin kohtaan, josta sai valittua automaattisen README -tiedoston luonnin. Repositoryn tilaksi valitsin Publicin ja klikkasin "Create Repository". 
Repository luotiin osoitteeseen:  https://github.com/Joni-tech/harjoitus3
Repositoryn luomisen jälkeen siirryin terminaaliin, missä päivitin ensin paketit ja asensin gitin:

	sudo apt-get update
	sudo apt-get -y install git

Kloonasin juuri luomani repositoryn koneelleni komennolla:

	git clone https://github.com/Joni-tech/harjoitus3.git


Käyttäjän kotihakemistoon luotiin repositoryn nimeä kantava kansio (harjoitus3). Kansio sisälsi samat tiedostot (LICENCE ja README), mitkä näkyivät GitHubin verkkosivuillakin, olihan kyseessä klooni. Loin kansioon tiedoston, johon aloin kirjoittamaan tätä raporttia: 

	nano harjoitus3/raportti3.md


Saatuani tekstiä raporttiin, päivitin tekemäni muutokset komennolla:

	git add . && git commit; git pull && git push

Kyseinen komento synkronoi tehdyt  muutokset kaikkien projektiin osallistuvien kesken, jolloin kaikilla on saatavilla viimeisimmät versiot tiedostoista. Samalla voidaan kommentoida tapahtuneita muutoksia (commit). Samalla kysyttiin GitHubin käyttäjätunnusta ja salasanaa. Tunnuksia kysytään aina, kun muutoksia viedään Gitiin. Tunnuksien jatkuvalta kirjoittamiselta vältytään antamalla komento **git config --global credential.helper "cache --timeout=3600"**, joka muistaa tunnuksesi tunnin ajan (60 x 60 sekuntia).

Kävin kurkkaamassa tiedostoa githubista ja huomasin tekstin kaipaavan muotoilua. Googlaamalla läysin Markdown-Cheatsheetin, mistä sain mallia otsikointiin, boldauksiin jne.
https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

Keskeytin tehtävien tekemisen 21.4.2020 klo 0:45 (UTC +3)

## d) Näytä omalla git-varastollasi esimerkit komennoista ‘git log’, ‘git diff’ ja ‘git blame’. Selitä tulokset.

## e) Tee tyhmä muutos gittiin, älä tee commit:tia. Tuhoa huonot muutokset ‘git reset –hard’. Huomaa, että tässä toiminnossa ei ole peruutusnappia.

## f) Tee uusi salt-moduli. Voit asentaa ja konfiguroida minkä vain uuden ohjelman: demonin, työpöytäohjelman tai komentokehotteesta toimivan ohjelman. Käytä tarvittaessa ‘find -printf “%T+ %p\n”|sort’ löytääksesi uudet asetustiedostot. (Tietysti eri ohjelma kuin aiemmissa tehtävissä, tarkoitushan on harjoitella Salttia)
