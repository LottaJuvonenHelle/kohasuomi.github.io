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

## Viikko 3 muistio

### Maanantain palaveri

Aika: 16.1.2023 klo 12<br />
Läsnä: Emmi, Pasi, Lari, Lasse, Anneli, Kodo

* Vaski meni sunnuntaina jumiin liian pitkän kestäneen action_logsin siivousajon takia, jumittanut kyselyyn:
INSERT INTO action_logs (SELECT * from work_action_logs WHERE DATE(timestamp) >= DATE('2022-01-01'));
  * action_logs-taulusta puuttuu Lapista, OUTIsta ja Vaskista kaikki su-aamua aikaisemmat tiedot. Ne ovat tallessa work_action_logs-taulussa.
  * Lari ja Emmi tutkii, miten datan saisi vietyä tauluihin pienemmissä seteissä.
* Metatietosanasto-plugari / Antti H.
  * voi olla periaatteessa tehtävissä, tehdään kehitysehdotus
* Viikon 3 päivitys
* indeksin mappingsin sijainti
  * ne ovat nyt etc:ssä, joka on kimppakohtainen.
  * siirretään koha-repoon ja tehdään oma branch, nimetään mappings koha-suomi-mappings.yaml ja muutetaan koha-confissa hakemaan mappings sieltä
  * hävitetään mappingsit etc:n alta
  * koha-repon alta otetaan ylimääräiset mappings-tiedostot pois
  * Lari tekee ( myös tiketti)
* valvonnan muutokset
  * lähtevät viestit tarkistetaan vasta 9.30 jälkeen. Jos tarkistuksen tekee ennen tuota, saa ilmoituksen, että viestejä ei ole vielä tarkistettu.
  * konttiin kirjautuessa saa jatkossa huomautuksen yli tunnin käynnissä olleista kyselyistä.
* Sanasto-raportin muutos toimimaan nykyisessä versiossa ei olekaan niin helppo kuin alunperin ajateltiin.

## Torstain palaveri (esityslista)

Aika: 19.1.2023 klo 12<br />
Läsnä: 

* OKM-tilastojen ongelmat Lumpeissa
  * Lumpeen pääkäyttäjiä tulee mukaan
  * ongelma johtuu siitä, että items.cn_sort-kentässä on kentän alussa kirjaimia
* Häiriö- ja huoltotiedotteet vastaisuudessa GitHubin discussionsiin
* Outlook/Hotmail,complainttaavat asiakkaat, lähtevän postin palvelimen "maine" ja viestien perillemeno
  * Bottivastaus, käsiteltävä pääkäyttäjäryhmässä tiistaina
* Build-production-branch-skriptin muutokset
  * muutetaan toiminnalisuutta niin, että uusia brancheja ei haeta automaattisesti 
  * nimen muutos, koska tällä rakennetaan myös testit, ei pelkästään production (build-(ks)-release?)
  * lisätäänkö skriptiin myös DBIx-skeemaluokkien rakennus ja käännösten asennus?
    * jos DBIx skeemaluokat tehdään uusiksi buildissa, niitä ei enää tarvita omassa erillisessä git-branchissaan, jolloin sitä branchia ei enää tarvitse ylläpitää (voidaan hävittää?)
  * tehdäänkö nyt vai versionvaihtoon 
* Kirkes parametrointikanta (tuleva tuotanto-Kirkes)
* Kirkes asiakasvarmenteet
* SmartBoxin palautustoiminnallisuuden ja varaustenkäsittelyn muutokset
* Finna ja versionvaihto - joko päätettiin, kuka on yhteydessä Finna-toimistoon?
* Muovitustiedon lisääminen EDItX sanomiin

## Viikko 2 muistio

### Maanantain palaveri

Aika: 9.1.2023 klo 10<br />
Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lassi, Pasi

__Aiheita__

* Valutus- ja hankintaongelmat ja Elasticsearch
  * "It turned out that queryParser is not thread-safe - inside it has states, access to which from several threads is not synchronized. Therefore, I came to use own queryParser for each request, and not use the previously created one." https://stackoverflow.com/questions/71547835/org-apache-lucene-queryparser-classic-parseexception-cannot-parse
  * Vaatinee koodimuutoksia Kohaan, bugiraportti yhteisöön?
  * Ollaan yhteydessä kansalliskirjastoon, jossa ElasticSearch:ia on Kohaan kehitetty

* Viikon 2 päivitys
  * käännöksissä korjauksia 
  * Muutama XSLT-muutos, esim. hakutulosnäytön Sisältyy-linkki.

#### Tammikuun huoltokatkon toimintasuunnitelma

1. Asiakasviestintä keskeytetään katkon ajaksi.
2. Testit ja redmine pysäytetään. Kirkes-testi siirretään kakkosnodelle, koska samana päivänä yhdeksältä pitäisi olla Kirkes-järjestelmäasetusten läpikäynti.
3. Lumme, siili, täti, lappi, vaski siirretään ykkös- ja nelosnodeilta (Meg ja Amy) kakkos ja kolmosnodelle (Jo ja Beth). Vaski menee kakkoselle.
4. P2 palomuuri alas, kampojen vaihto ja palvelin ylös, P1 jatkaa edelleen hommiaan. P2 alkaa käynnistyttyään neuvotella IPSec tunneleita uusiksi ja toivottavasti ehtii valmiiksi siihen mennessä kun P1 menee alas (kohdassa 11).
5. DB1 (Nat) alas, kampojen vaihto ja palvelin ylös. Tietokantapalvelimen käyttäminen alhaalla aiheuttaa katkon kaikkiin kimppoihin. Katko päättyy kun palvelin saadaan takaisin käyntiin.
6. Nelonen (Amy) alas, kampojen vaihto ja palvelin ylös.
7. Jos tässä kohtaa ollaan vielä huoltokatkon paremmalla puolella, siirretään vaski ja lappi takaisin neloselle, jos ei niin saavat jatkaa sijaisnodella toistaiseksi. Mahdollisesti on tarpeen siinä tapauksessa muuttaa IP-osoite Turun pääkirjaston palautusautomaatilla, jolloin Vaski jäisi sitten pysyvästi kakkosnodelle.
8. Ykkönen (Meg) alas, kampojen vaihto ja palvelin ylös.
9. Jos tässäkin kohtaa ollaan vielä huoltokatkon paremmalla puolella, siirretään lumme, siili ja täti takaisin ykköselle, jos ei niin saavat jatkaa sijaisnodella toistaiseksi. Sillä ei periaatteessa ole vaikutusta mihinkään ja kontit voidaan siirtää oikealle nodelle sopivan tilaisuuden tullen, esimerkiksi illalla tai mahdollisesti vasta seuraavassa huoltokatkossa.
10. DB2 (Dan) alas, kampojen vaihto ja palvelin ylös, varmistetaan että replikointi jatkuu oikein. Tässä vaiheessa raportit eivät toimi oikein ennenkuin DB2 saadaan takaisin linjoille.
11. P1 palomuuri alas, P2:n pitäisi tässä kohtaa ottaa ohjat huomattuaan ykkösen menneen alas. Mahdollisesti tunneleiden siirtymiseen liittyvä viive voi tulla näkyväksi tässä kohtaa. Tätä on pyritty kompensoimaan antamalle P2:lle mahdollisimman paljon aikaa neuvotella tunnelit uudestaan.
12. Vaihdetaan kammat P1:lle ja nostetaan se takaisin ylös, liikenne palautetaan illalla takaisin kulkemaan P1:n kautta.
13. Laitetaan asiakasviestintä takaisin käyttöön.
14. Nostellaan testikontit ja Redmine takaisin kunhan ehditään.

### Torstain palaveri

Aika: 12.1.2023 klo 10<br />
Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lassi, Pasi

* Viikon 3 päivitys
  * 350 - osa, Pasi päivittää tikettiin, mitä tulee mukaan.
  * 308
  * https://tiketti.koha-suomi.fi/issues/5600
* Käännökset - messages.js.po-tiedoston kaikki käännökset eivät näy
* testien pienennys
  * dumppi, josta jätetään isoja tauluja pois
  * otetaan tyyliin 5000 viimeisintä (tai jokin muu setti) tietuetta ja niihin liittyvät niteet/lainat
  * Emmi katsoo taulut ja Pasi katsoo datan poiminnan
  * Kodo tekee Vaskin next-testin, koska sinne tulee kaikki mahdollinen mukaan
* Kun kontteja siirtelee nodelta toiselle, voi lxc vetää maton alta kontilta ennen kuin indeksit ehditään saada kokonaan levylle. Kontissa, joka siirretään, pitää ajaa elastictmpfs synctodisk (esimerkiksi nodelta kogo [kontti] sudo elastictmpfs synctodisk). Kirjoitetaan tämä osaksi koctl:ää kun ehditään, mutta tässä vaiheessa siis pitää tehdä manuaalisesti.
* principioon dokumentaatio, mitä tehdään huoltokatkon aikana
* keskiviikkona ei saatu vaihdettua palomuurien muistikampoja, koska ne oli vielä Kuopiossa postin hallussa. Nämä vaihdetaan helmikuun käyttökatkossa. 

## Viikko 1 muistiot

### Maanantain palaveri

Aika: 2.1.2023 klo 10<br />
Läsnä: Anneli, Lasse, Pasi, Ari, Lari, Kodo

__Aiheita__

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

__Aiheita__

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
