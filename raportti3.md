*Tein tehtävän kotona pöytäkoneellani, jossa oli mm. Intel i5-3570K prosessori, 8GB RAM-muistia, Asus GTX 1060 (6GB) näytönohjain ja käyttöjärjestelmänä Win 10. Jatkoin tehtävien tekemistä VirtualBoxissa (versio 6.1.4) luomillani virtuaalikoneilla, joita käytin edellisissä harjoituksissa: https://joni.tech.blog/2020/04/07/ph-h1/ ja https://joni.tech.blog/2020/04/15/ph-h2/*

Tämän harjoituksen ohjeet osoitteessa http://terokarvinen.com/2020/configuration-managment-systems-palvelinten-hallinta-ict4tn022-spring-2020/

Aloitin tehtävien tekemisen 20.4.2020 klo 22:15 (UTC +3)

Suurin osa komennoista on poimittu Tero Karvisen ohjeista: http://terokarvinen.com/2016/publish-your-project-with-github

## a) MarkDown. Tee tämän tehtävän raportti MarkDownina. Helpointa on tehdä raportti GitHub-varastoon, jolloin md-päätteiset tiedostot muotoillaan automaattisesti. Tyhjä rivi tekee kappalejaon, risuaita ‘#’ tekee otsikon, sisennys merkitsee koodinpätkän.

### Repositoryn luominen

Tein aluksi GitHubissa uuden repositoryn nimeltä harjoitus3. Lisenssiksi valitsin GNU GPL3 v3.0, minkä lisäksi pistin ruksin kohtaan, josta sai valittua automaattisen README -tiedoston luonnin. Repositoryn tilaksi valitsin Publicin ja klikkasin "Create Repository".

![](https://myy.haaga-helia.fi/~bgh330/Linux/1.png "Repositoryn luominen")
 
Repository luotiin osoitteeseen:  https://github.com/Joni-tech/harjoitus3

![](https://myy.haaga-helia.fi/~bgh330/Linux/2.png "Repository luotu")

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

Kävin kurkkaamassa tiedostoa githubista ja huomasin tekstin kaipaavan muotoilua. Googlaamalla löysin Markdown-Cheatsheetin, mistä sain mallia otsikointiin, boldauksiin jne.
https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

Keskeytin tehtävien tekemisen 21.4.2020 klo 0:45 (UTC +3)
Jatkoin tehtävien tekemistä 21.4.2020 klo 14:00 (UTC +3)

## d) Näytä omalla git-varastollasi esimerkit komennoista ‘git log’, ‘git diff’ ja ‘git blame’. Selitä tulokset.

### git log

Komennolla **git log** sain listan githubiin viedyistä muutoksista. Ekalla rivillä oli ilmeisesti muutoksen ID, toisella rivillä muutoksen tekijän nimi ja sähköpostiosoite ja kolmannella rivillä muutoksen päivämäärä ja kellonaika.

	commit 4e4134090cbc1df8acf85239af5e9652f8a11fe6
	Author: Joni Smolander <bgh330@myy.haaga-helia.fi>
	Date:   Tue Apr 21 00:44:53 2020 +0300

	    A valmis

	commit 7a0f1155f7e601b2f1de78fe69993da78a83c33a
	Author: Joni Smolander <bgh330@myy.haaga-helia.fi>
	Date:   Tue Apr 21 00:42:10 2020 +0300

	    Tekstiä

Lisätietoja: https://git-scm.com/docs/git-log

### git diff

Komennolla **git diff** pystyin näkemään tekemäni muutokset, joita en vielä ollut vienyt githubiin. Tarkemmin sanoen omalla koneella olevien tiedostojen eron verrattuna gitissä oleviin. Erot näkyivät vihreänä:

![](https://myy.haaga-helia.fi/~bgh330/Linux/3.png "git diff")

Lisätietoja: https://git-scm.com/docs/git-diff

### git blame

Komennolla **git blame raportti3.md** näin rivikohtaisesti kuka on viimeeksi kirjoittanut riviä ja milloin.

	9929affa (Joni Smolander    2020-04-21 00:40:22 +0300 13)       sudo apt-get update
	7a0f1155 (Joni Smolander    2020-04-21 00:42:10 +0300 14)       sudo apt-get -y install git
	06f0dda1 (Joni Smolander    2020-04-20 23:59:11 +0300 15) 
	c7c51255 (Joni Smolander    2020-04-20 23:50:11 +0300 16) Kloonasin juuri luomani repositoryn koneelleni komennolla:
	c7c51255 (Joni Smolander    2020-04-20 23:50:11 +0300 17) 
	7a0f1155 (Joni Smolander    2020-04-21 00:42:10 +0300 18)       git clone https://github.com/Joni-tech/harjoitus3.git

Rivien alussa ilmeisesti muutoksen ID, minkä jälkeen on muutoksen tekijän nimi sekä muutoksen päivämäärä ja kellonaika. Kellonajan jälkeen näkyy rivin numero. Rivin viimeisenä on itse muutos.

Lisätietoja: https://git-scm.com/docs/git-blame

## e) Tee tyhmä muutos gittiin, älä tee commit:tia. Tuhoa huonot muutokset ‘git reset –hard’. Huomaa, että tässä toiminnossa ei ole peruutusnappia.

Kirjoitin jotakin sotkua raporttiini ja tallensin tiedoston. Tämän jälkeen annoin komennon **git reset --hard**. Sain ilmoituksen paluusta edelliseen committiin. Avasin raporttini ja huomasin kirjoittamieni sotkujen poistuneen. Muu sisältö näytti pysyneen muuttumattomana.

![](https://myy.haaga-helia.fi/~bgh330/Linux/4.png "git reset --hard")


## f) Tee uusi salt-moduli. Voit asentaa ja konfiguroida minkä vain uuden ohjelman: demonin, työpöytäohjelman tai komentokehotteesta toimivan ohjelman. Käytä tarvittaessa ‘find -printf “%T+ %p\n”|sort’ löytääksesi uudet asetustiedostot. (Tietysti eri ohjelma kuin aiemmissa tehtävissä, tarkoitushan on harjoitella Salttia)

Päätin tehdä moduulin, joka asentaa htop -nimisen ohjelman, jonka kautta voi seurata järjestelmätietoja sekä käynnissä olevia prosesseja. Asensin ohjelman ensin käsin komennolla **sudo apt-get -y install htop**, minkä jälkeen käynnistin sovelluksen komennolla **htop**. Ohjelma käynnistyi, ja näytti mm. käynnissä olleet prosessit. Siirryin tekemään aiemmassa harjoituksessani (https://joni.tech.blog/2020/04/07/ph-h1/) luomalle masterille tilatiedostoa. Tein kansioon /srv/salt/ tiedoston htop.sls, jonka sisällöksi kirjoitin:

	htop:
	  pkg.installed

Kävin orjakoneelta katsomassa, ettei htopia ollut asennettuna ennestään, minkä jälkeen annoin masterilla komennon:

	sudo salt '*' state.apply htop

Aikansa mietittyään sain ilmoituksen onnistuneesta suorituksesta.

![](https://myy.haaga-helia.fi/~bgh330/Linux/5.png "htop state ajettu")

Kävin orjalla antamassa komennon **htop**, minkä jälkeen ohjelma käynnistyi näyttäen käynnissä olleet prosessit. Luomani tila siis toimi.

![](https://myy.haaga-helia.fi/~bgh330/Linux/6.png "htop käynnistyi orjalla")

Lopetin tehtävien tekemisen 21.4.2020 klo 18:00 (UTC +3), mutta olin välissä tehnyt muutakin kuin tehtäviä. Koko harjoitukseen ja raportointiin meni tehokasta työaikaa noin viisi tuntia. 


## Lähteet

https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

http://terokarvinen.com/2020/configuration-managment-systems-palvelinten-hallinta-ict4tn022-spring-2020/

http://terokarvinen.com/2016/publish-your-project-with-github

https://git-scm.com/docs/git-blame

https://git-scm.com/docs/git-diff

https://git-scm.com/docs/git-log
