h3 Versionhallinta
z) Opiskele yllä aikataulussa olevat artikkelit. Noissa artikkeleissa opetetaan ne asiat, joilla läksyt saa tehtyä. Tätä z-kohdan lukutehtävää ei tarvitse raportoida. Luettava materiaali on kunkin tapaamiskerran kohdalla.


#a) MarkDown. Tee tämän tehtävän raportti MarkDownina. Helpointa on tehdä raportti GitHub-varastoon, jolloin md-päätteiset tiedostot muotoillaan automaattisesti. Tyhjä rivi tekee kappalejaon, risuaita ‘#’ tekee otsikon, sisennys merkitsee koodinpätkän.

# aloitin asentamalla uuden virtuaalikoneen ja sinne piti ladata git
#yritän selventää seuraavaksi itselle vähän git komentoja, git komennot ajetaan:
	git argumentti, esim git init, git clone


#.md pääte on markdown formaatti
#git init alustaa/valmistelee työkansion gitin käyttöön, tässä työkansion nimi on gitti.

#git add lisää tiedoston git ympäristöön
#git commit tämä esittelee kaiketi mm muutoksia joita versioiden muuttuessa tapahtuu.
#git branch komennolla voi luoda erilaisia haaraumia, esimerkiksi jos haluaa kellokahden aikaan yolla muuttaa jotain koodin rimpsuja niin branch olisi siis turvallisin ratkaisu extreme kokeiluille?

# aloitin asentamalla uuden virtuaalikoneen ja sinne piti ladata git
	apt-get install git
# lisäsin omat tietoni komennolla 

	 git config --global user.name "Eetu Innanen"
	 git config --global user.email eetu.innanen@gmail.com

	tein kansion nimeltä gitti johonka loin  tiedoston mikä on nimetty: minungitti.txt tiedoston 
	readme tiedostoon kirjoitin tekstiä sekä alla olevat koodit opettelin gitin kanssa.
		mkdir gitti
		nano minungitti.txt -> "tekstiä""
		## tästä alkaa git koodit
		git init
		Initialized empty Git repository in /home/eetu/gitti/.git/
	Seuraavaksi lisätään luotu tiedosto git ympäristöön.
		git add minungitti.txt
	Tehdään ensimmäinen commit
		git commit -m "This is my very first commit"

	Luodaan haara komennolla:
	git branch -m haara







##d) Näytä omalla git-varastollasi esimerkit komennoista ‘git log’, ‘git diff’ ja ‘git blame’. Selitä tulokset.

##Komennolla git log näkee logit
	root@debianmaster:/home/eetu/gitti# git log
	commit ac96882870e6b6b9d8da00f3ee4c93f05966d2f5 (HEAD -> haara)
	Author: Eetu Innanen <eetu.innanen@gmail.com>
	Date:   Thu Nov 12 18:31:23 2020 +0200

	this is my very first commit
	root@debianmaster:/home/eetu/gitti# 

##Komennolla git diff näkee muutokset
git diff
diff --git a/minungitti.txt b/minungitti.txt
index f4694e6..4ddaa76 100644
--- a/minungitti.txt
+++ b/minungitti.txt
@@ -1 +1,2 @@
 Tässä on h3 tehtävän .tiedosto
+tyhmä muutos asdfadsasd
diff --git a/minungitti1.txt b/minungitti1.txt
index 77f2f60..8be9ee4 100644
--- a/minungitti1.txt
+++ b/minungitti1.txt
@@ -1,2 +1,3 @@
 Tässä on h3 tehtävän .tiedosto
 tyhmä muutos
+tyhmä muutos asdfadsasd



##Komennolla git blame näkee viimeksi muokatut tiedot ja muokkaajan.
root@debianmaster:/home/eetu/gitti# git blame minungitti.txt
^ac96882 (Eetu Innanen 2020-11-12 18:31:23 +0200 1) Tässä on h3 tehtävän .tiedosto

















##e) Tee tyhmä muutos gittiin, älä tee commit:tia. Tuhoa huonot muutokset ‘git reset –hard’. Huomaa, että tässä toiminnossa ei ole peruutusnappia.
	root@debianmaster:/home/eetu/gitti# echo "tyhmä muutos" >> minungitti.txt
	root@debianmaster:/home/eetu/gitti# cat minungitti.txt 
	Tässä on h3 tehtävän .tiedosto
	tyhmä muutos
	root@debianmaster:/home/eetu/gitti# git reset --hard
	HEAD is now at ac96882 this is my very first commit
	root@debianmaster:/home/eetu/gitti# git log
	commit ac96882870e6b6b9d8da00f3ee4c93f05966d2f5 (HEAD -> haara)
	Author: Eetu Innanen <eetu.innanen@gmail.com>
	Date:   Thu Nov 12 18:31:23 2020 +0200

	    this is my very first commit
	root@debianmaster:/home/eetu/gitti# cat minungitti.txt 
	Tässä on h3 tehtävän .tiedosto

f) Tee uusi salt-moduli. Voit asentaa ja konfiguroida minkä vain uuden ohjelman: demonin, työpöytäohjelman tai komentokehotteesta toimivan ohjelman. Käytä tarvittaessa ‘find -printf “%T+ %p\n”|sort’ löytääksesi uudet asetustiedostot. (Tietysti eri ohjelma kuin aiemmissa tehtävissä, tarkoitushan on harjoitella Salttia)

d) Vapaaehtoinen: Laita srv/salt/ gittiin. Tee uusi moduli. Kloonaa varastosi toiselle koneelle (tai poista srv/salt ja palauta se kloonaamalla) ja jatka sillä.
