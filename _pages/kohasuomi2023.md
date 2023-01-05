---
title: 'Koha-Suomen vuoden 2023 muistiot'
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
permalink: /kohasuomi2023
redirect_from:
  - /theme-setup/
toc: true
layout: single
hidden: true
---

Koha-Suomen henkilökunta kokoontuu kaksi kertaa viikossa. Uusin muistio on aina ylimmäisenä.

## Viikko 2 esityslista

### Maanantain palaveri

Aika: 9.1.2023 klo 10<br />
Läsnä: 

* Valutus- ja hankintaongelmat ja Elasticsearch
  * "It turned out that queryParser is not thread-safe - inside it has states, access to which from several threads is not synchronized. Therefore, I came to use own queryParser for each request, and not use the previously created one." https://stackoverflow.com/questions/71547835/org-apache-lucene-queryparser-classic-parseexception-cannot-parse
  * Vaatinee koodimuutoksia Kohaan, bugiraportti yhteisöön?

* Viikon 2 päivitys

#### Tammikuun huoltokatkon toimintasuunnitelma

1. Asiakasviestintä keskeytetään katkon ajaksi.
2. Testit ja redmine pysäytetään. Kirkes-testi siirretään kakkosnodelle, koska samana päivänä yhdeksältä pitäisi olla Kirkes-järjestelmäasetusten läpikäynti.
3. Lumme, siili, täti, lappi, vaski siirretään ykkös- ja nelosnodeilta (Meg ja Amy) kakkos ja kolmosnodelle (Jo ja Beth).
4. Pfsense2 palomuuri alas, kampojen vaihto ja palvelin ylös, Pfsense1 jatkaa edelleen hommiaan. Pfsense2 alkaa käynnistyttyään neuvotella IPSec tunneleita uusiksi ja toivottavasti ehtii valmiiksi siihen mennessä kun Pfsense1 menee alas.
5. DB1 (Nat) alas, kampojen vaihto ja palvelin ylös. Tietokantapalvelimen käyttäminen alhaalla aiheuttaa katkon kaikkiin kimppoihin. Katko päättyy kun palvelin saadaan takaisin käyntiin.
6. Nelonen (Amy) alas, kampojen vaihto ja palvelin ylös.
7. Jos tässä kohtaa ollaan vielä huoltokatkon paremmalla puolella, siirretään vaski ja lappi takaisin neloselle, jos ei niin saavat jatkaa sijaisnodella toistaiseksi. Mahdollisesti on tarpeen siinä tapauksessa muuttaa IP-osoite Turun pääkirjaston palautusautomaatilla, jolloin Vaski jäisi sitten pysyvästi kakkos- tai kolmosnodelle.
8. Ykkönen (Meg) alas, kampojen vaihto ja palvelin ylös.
9. Jos tässäkin kohtaa ollaan vielä huoltokatkon paremmalla puolella, siirretään lumme, siili ja täti takaisin ykköselle, jos ei niin saavat jatkaa sijaisnodella toistaiseksi. Sillä ei periaatteessa ole vaikutusta mihinkään ja kontit voidaan siirtää oikealle nodelle sopivan tilaisuuden tullen, esimerkiksi illalla tai mahdollisesti vasta seuraavassa huoltokatkossa.
10. DB2 (Dan) alas, kampojen vaihto ja palvelin ylös, varmistetaan että replikointi jatkuu oikein. Tässä vaiheessa raportit eivät toimi oikein ennenkuin DB2 saadaan takaisin linjoille.
11. Pfsense1 palomuuri alas, Pfsense2:n pitäisi tässä kohtaa ottaa ohjat huomattuaan ykkösen menneen alas. Mahdollisesti tunneleiden siirtymiseen liittyvä viive voi tulla näkyväksi tässä kohtaa. Tätä on pyritty kompensoimaan antamalle Pfsense2:lle mahdollisimman paljon aikaa neuvotella tunnelit uudestaan.
12. Vaihdetaan kammat Pfsense1:lle ja nostetaan se takaisin ylös, liikenne palautetaan illalla takaisin kulkemaan Pfsense1:n kautta.
13. Nostellaan testikontit ja Redmine takaisin kunhan ehditään.

## Viikko 1 muistiot

### Maanantain palaveri

Aika: 2.1.2023 klo 10<br />
Läsnä: Anneli, Lasse, Pasi, Ari, Lari, Kodo

* Viikon 1 päivitys
  * [KohaSuomi/Koha #331](https://github.com/KohaSuomi/Koha/issues/331) Suojatut kentät näkyvät tyhjinä z39.50-haulla tietueita korvattaessa
  * [KohaSuomi/Koha #334](https://github.com/KohaSuomi/Koha/issues/334)
  * SQL-raportit hakemaan slave-kannasta masterin sijaan, jotta vältytään tietokannan taulujen lukkiutuminen raskaissa kyselyissä sekä master-kannan kuormaa saadaan kevennettyä.
  * [Koha #308](https://github.com/KohaSuomi/Koha/issues/308)

* Kodo ehdottaa tämän viikon Kirkes-palaverin ajankohdaksi ke 4.1.2023

* Versionvaihto
  * viedään ensin Vaski, jotta nähdään, kuinka kauan maksimissaan menee.
  * kaikille läksyksi miettiä torstain palaveriin mennessä, miten saadaan vähennettyä testikantaan vietävän datan määrää, jotta testikantojen luonti ei vie niin kauan.

### Torstain palaveri

Aika: 5.1.2023 klo 10<br />
Läsnä: Pasi, Lari, Kodo, Lasse

* Vanhentuneiden maksujen poistoajo - Vaski kysyi pääkäyttäjäpalaverissa, että mikä sen tilanne on?
  * Päätös [Tietojen säilytysajat -wikissä](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Tietojen_s%C3%A4ilytysajat)

* Viikon 2 päivitys
  * käännöksissä korjauksia 
  * Muutama XSLT-muutos, esim. hakutulosnäytön Sisältyy-linkki.

* Onko huoltokatkoa vkolla 2 keskiviikkona?
  * On, ja iso: Fujitsun muistikampojen vaihdot. Katko saattaa kestää enemmän kuin 2 tuntia, ja koskee kaikkia kimppoja.

* Pääkäyttäjien kanssa sovittiin, että jokainen kimppa käy omat Redmine-tikettinsä Palaute-projektissa läpi ja sulkee valmiit ja sellaiset, jotka eivät ole enää ajankohtaisia. Loput käydään läpi ja päätetään, mitkä siirretään uusina tiketteinä GitHubiin.

* Siirretään käännökset build-productionista omaan repoon, symlinkataan meidän omat po-tiedostot reposta Kohan ympäristöön.
 
* datereceived-kenttä löytyy muualtakin kuin vain aqorders-taulusta? Tämä on meidän oma muutos, ja on jäänyt roikkumaan; poistetaan.
