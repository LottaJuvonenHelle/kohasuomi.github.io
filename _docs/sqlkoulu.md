---
title: 'Miten tehdä SQL-rapORtteja'
permalink: /dokumentaatio/sqlkoulu/
redirect_FROM:
  - /theme-setup/
toc: true
---

Ohjeen tekijä: Johanna Räisä
Päivittänyt: Anneli Österman / 3.4.2020


"Koha-Suomen tietokantaskeema löytyy Dokumenteistä":https://tiketti.koha-suomi.fi/documents/52.

Tutkimusmatka Kohan tietokantaan -koulutuksen tallenne löytyy "täältä":https://youtu.be/lH7Z8OetO3c

## SQL-lauseiden rakentaminen

### SELECT-lause

Lause, jolla haetaan tietoa tietokannasta.
Yksinkertaisimmillaan lause on:

```
SELECT * FROM bORrowers;
```

Tällä komennolla haetaan kaikki taulun kentät ilman rajausta. Tätä tulee välttää rapORtteja luodessa, niissä pitäisi määritellä tarvittavat kentät.

Taulusta voidaan myös kysellä pelkästään tiettyjä kenttiä kirjoittamalla tähden tilalle halutut kentät.

```
SELECT bORrowernumber, cardnumber, address FROM bORrowers;
```

Kenttien nimiä voidaan myös muuttaa, jos ei haluta näyttää englanninkielisiä sarakeotsikoita. Tämä tapahtuu "as"-sanalla.

```
SELECT bORrowernumber as 'Asiakasnumero', cardnumber as 'KORtin numero', address as 'Osoite' FROM bORrowers;
```

Nimi kannattaa laittaa yksöishipsuihin, varsinkin jos se on kaksiosainen tai sisältää ääkkösiä.

### WHERE

Jos halutaan rajata haku tiettyjen parametrien mukaan, niin silloin SELECT-lauseeseen lisätään WHERE-komento.

```
SELECT * FROM bORrowers WHERE categORycode = 'LAPSI';
```

Arvot, joissa on kirjaimia tulee olla hipsujen sisässä. Jos et tiedä onko kenttä numerokenttä, niin on turvallisinta ympäröidä hipsuilla.

WHERE-komentoon voi lisätä useita rajoituksia AND- ja OR-sanalla.

```
SELECT * FROM items WHERE itype = '28VRK' AND location = 'A';
SELECT * FROM items WHERE itype = '14VRK' OR itype = '28VRK';
```

Mallissa AND-sanan tulosjoukko muodostuu riveistä, joilla on nidetyyppi 28VRK ja hyllypaikka aikuiset.
Mallissa OR-sanan tulosjoukko muodostuu riveistä, joilla on nidetyyppi 14VRK tai nidetyyppi 28VRK. Eli tulosjoukko muodostuu kummastakin nidetyypistä.

Joskus on helpompi saada tulosjoukko rajoittamalla negatiivisesti. Siihen käytetään määritystä !=

```
SELECT * FROM items WHERE itype != '28VRK' AND homebranch = 'MLI_PK';
```

Mallin haussa tulosjoukko muodostuu Mikkelin pääkirjaston kaikista muista niteistä paitsi e-kirjasta.

Jos Kohassa halutaan valita kirjastopiste ennen raportin käynnistystä niin silloin raporttin laitetaan ohjelmoitu valintatyökalu.

```
SELECT * FROM items WHERE itype != '28VRK' AND homebranch=<<Kotikirjasto|branches>>;
```

Käyttääksesi WHERE-rajauksia sinun tulee tietää tunnusarvot. Tietokannassa käytetään lyhyitä tunnuksia, joilla on nopeampi hakea. Kuvaukset ovat yleensä ihmisiä varten ja ne näytetään vain käyttöliittymässä.

### LIKE

SELECT-lauseissa voidaan käyttää vertailussa myös LIKE-sanaa. Esim, jos halutaan jonkun tietyn kunnan kirjastopisteet samaan tulosjoukkoon.

```
SELECT * FROM items WHERE homebranch LIKE 'MLI%';
```

Mallin tulosjoukkoon tulee kaikki niteet kirjastopisteistä joiden lyhenne alkaa sanalla MLI. LIKE-vertailussa pystytään käyttämään %-merkkiä, joka toimii villinä korttina haussa. Tämä on todella paljon hitaampaa, kuin suoraan =-merkillä muodostettu lause.

LIKE-komennossakin on mahdollisuus negatiiviseen rakenteeseen. Tällöin käytetään määritettä 'NOT LIKE'.

```
SELECT * FROM items WHERE homebranch NOT LIKE 'MLI%';
```

### JOIN

Haussa tulosjoukkoon saadaan tietoa muista tauluista relaatioiden avulla. JOIN-komento on keskeisessä roolissa tässä yhdistelyssä.

```
SELECT b.author as 'Tekijä', b.title as 'Nimeke', i.location as 'Hyllypaikka', i.homebranch as 'Kotikirjasto' FROM items i 
JOIN biblio b on i.biblionumber = b.biblionumber 
WHERE i.itype = '28VRK';
```

Mallissa yhdistetään items-taulu ja biblio-taulu ja otetaan kummastakin tietoa tulosjoukkoon. Lauseessa tauluille on annettu lyhenteet, joita käytetään selventämään mistä taulusta tieto pitäisi tulla. Jos tauluissa on paljon saman nimisiä kenttiä, SQL ei tiedä kummasta on kyse, siksi kentän eteen tulee laittaa tietoa taulusta joko taulun koko nimellä tai sitten määritellyllä lyhenteellä.

Lauseessa voi olla ääretön määrä join-komentoja, jos vain tauluilla on jokin yhdistävä kenttä (relaatio). Kuitenkin mitä enemmän yhdistetään taulujen tietoa sitä hitaammaksi haut käyvät.

JOIN-komentoja on erilaisia. [Katso visuaalinen esittely JOINien eroista](https://www.codeproject.com/Articles/33052/Visual-Representation-of-SQL-Joins).

### Taulujen aliakset

Kyselyssä voi määrittää tauluille aliaksen, jolla voi viitata muualla kyselyssä tauluun. Tämä on helppo ja nopea tapa kertoa, mistä taulusta tieto halutaan hakea, jos useassa taulussa on sama sarake käytössä. Jos taulua ei määrittele, ilmoittaa Koha tiedon olevan "ambiguous" eli epämääräinen eikä aja raporttia.

Aliaksen voi keksiä itse, mutta se kannattaa olla helposti muistettava ja lyhyt. Alias kirjoitetaan kyselyssä heti taulun nimen perään. Alla olevassa kyselyssä biblionumber löytyy kummastakin taulusta, joten se on määritetty haettavaksi biblio-taulusta.

```
SELECT b.title,b.biblionumber,i.barcode
FROM biblio b
JOIN items i USING (biblionumber)
WHERE i.holdingbranch='OUPK'
```

### Ajalla rajaaminen

Tulosjoukkon rajaaminen ajan mukaan voidaan määritellä monella eri tavalla, mutta yksin kertaisin on opetella BETWEEN-lause.

```
SELECT *
FROM items
WHERE date(dateaccessioned) BETWEEN '2022-01-01' AND '2022-12-31';
```

Tietokannassa päivämäärät ovat yleensä muodossa 2016-01-01 12:00:00, mallin lauseessa halutaan vain päiväys eikä kellonaikaa. Siksi päivämäärä-kenttä on ympyröity date:lla.

Kohassa päivämäärä valinnan saa raporttiin kun vaihtaa nuo luvut sisäänrakennettuun valintatyökaluun.

```
SELECT *
FROM items
WHERE date(dateaccessioned) BETWEEN <<AloitusPvm |date>> AND <<LopetusPvm |date>>;
```

Aloitus- ja lopetuspäivämäärien kuvaus eli yllä esim. AloitusPvm, kannattaa olla eri nimiset, muuten Koha yhdistelee ne samaksi kentäksi.

### COUNT

COUNT-komennolla voidaan laskea tulosjoukon rivien määrä yhteen.

```
SELECT count(*) FROM items WHERE itype = 'KIRJA';
```

## GROUP BY

GROUP BY -komennolla voidaan ryhmitellä tulosjoukkoa.

```
SELECT * FROM issues group by itemnumber;
```

Mallin lause antaa lainat-taulusta tulosjoukon niteen numeron mukaan, eli joka rivillä on eri itemnumber. Tätä joudutaan käyttämään joskus jos tulosjoukkoon tulee paljon samoja rivejä.

### ORDER BY

ORDER BY -komennolla voidaan järjestää tulosjoukkoa halutulla tavalla.

```
SELECT * FROM borrowers ORDER BY surname ASC;
```

Mallin lause järjestää tulosjoukon sukunimen mukaan nousevasti (ascending), eli A:sta Ö:hön.

```
SELECT * FROM borrowers ORDER BY surname DESC;
```

Mallin lause järjestää tulosjoukon sukunimen mukaan laskevasti (descending), eli Ö:stä A:han.

## LIMIT

LIMIT-komennolla voidaan rajata hakutuloksen tulosjoukkoa.

```
SELECT * FROM borrowers LIMIT 100;
```

Mallin  lause hakee 100 ensimmäistä riviä borrowers-taulusta.


## CONCAT

CONCAT-komennolla voidaan muodostaa yhtenäisiä merkkijonoja. 

```
SELECT concat(b.surname,' ', b.firstname) as 'Asiakas' FROM borrowers WHERE categorycode = 'HENKILO';
```

Mallissa yhteen sarakkeeseen tulee asiakkaan sukunimi, väli ja etunimi.

## ExtractValue

ExtractValue-komennolla voidaan kysellä tietoa kentän sisällä olevasta rakenteesta. Kannattaa huomioida, että nämä voivat hidastaa kyselyä.

```
SELECT * FROM biblio_metadata bm
WHERE ExtractValue(bm.metadata, '//datafield[@tag="773"]/subfield[@code="w"]') = '';
```

Jos MARC-kentän tiedot halutaan hakea vain taulukon sarakkeeseen, sen voi tehdä näin:

```
SELECT title, ExtractValue(bm.metadata, '//datafield[@tag="264"]/subfield[@code="c"]')
FROM biblio_metadata bm
JOIN biblio b using (biblionumber)
WHERE biblionumber=1234
```

Mallissa mennään marcxml-kentän sisälle ja tarkastellaan xml-rakennetta. Mallin haku antaa tulosjoukoksi luettelointitiedot, joilla ei ole kenttää 773w eli se on tyhjä.

Nimiöstä 7. merkkipaikalta lähtien 2 merkkiä eteenpäin ei ole "im":
```
SUBSTR(ExtractValue(bm.metadata,'//leader'),7,2) NOT IN ('im') 
```

Kiinteämittaisista kentistä 007-kentässä 1. merkkipaikalta 2 merkkiä eteenpäin on "ss":
```
SUBSTR(ExtractValue(bm.metadata,'//controlfield[@tag="007"]'),1,2) IN ('ss')
```

## NULL ja tyhjä

Tietokannassa voi olla kahden tyyppisiä "tyhjiä"-kenttiä. NULL tarkoittaa, että kenttään ei ole määritelty mitään. Toinen vaihtoehto on, että kentässä on tyhjä merkkijono. NULL-määreen kanssa käytetään IS-sanaa =-merkin tilalla. Negatiivisia hakuja tehdessä käytetään 'IS NOT NULL'.

```
SELECT * FROM items WHERE barcode IS NULL AND homebranch = 'MLI_PK';
SELECT * FROM items WHERE barcode = '' AND homebranch = 'MLI_PK';
```

Jos "tyhjiä" halutaan käyttää vertailussa niin silloin kannattaa testata kumpaakin yhtä aikaa.

```
SELECT * FROM items WHERE (barcode IS NULL OR barcode = '') AND homebranch = 'MLI_PK';
```

Mallin tulosjoukko muodostuu niteistä, joilla ei ole viivakoodia. *Huomaa sulut OR-vertailujen ympärillä!* Jos sekoitellaan AND- ja OR-vertailua, niin OR pitää ympyröidä suluilla.

## Relaatiot

Relaatioilla tarkoitetaan tauluja yhdistäviä tekijöitä, kuten asiakkaiden relaatiota lainoihin.

```
SELECT count(*) FROM borrowers b
JOIN issues i on b.borrowernumber = i.borrowernumber
JOIN old_issues oi on b.borrowernumber = oi.borrowernumber
WHERE b.borrowernumber = 1;
```

Mallin lause antaa kaikki nykyiset ja vanhat lainat asiakkaalle, jonka borrowernumber on yksi.

Kohan relaatiot löytyvät tietokantarakenteesta. http://schema.koha-community.org/
Yleensä relaatiot on nimetty samalla nimellä, kuten mallissa kaikista tauluista löytyy borrowernumber-kenttä.

## Lauseen rakentaminen

Lausetta rakentaessa kannattaa miettiä mikä on päätaulu, eli mitä tietoa halutaan ja tarvitseeko siihen yhdistellä muita tauluja.

Esimerkki: Haluan asiakkaat ja niille maksut ajalta 01.06.2022-10.06.2022, lisäksi sellaiset maksut joita ei ole vielä maksettu. Järjestetään ne vielä päivämäärän mukaan laskevasti, eli uusimmasta vanhimpaan.

```
SELECT b.surname as 'Sukunimi', b.firstname as 'Etunimi', a.amountoutstANDing as 'Maksun määrä', a.description as 'Kuvaus' FROM borrowers b
JOIN accountlines a on b.borrowernumber = a.borrowernumber
WHERE a.amountoutstanding != 0 AND date(a.date) between '2022-06-01' AND '2022-06-10' ORDER BY date desc;
```

Kannattaa myös katsoa ensin [Koha-yhteisön raporttikirjastosta](https://wiki.koha-community.org/wiki/SQL_Reports_Library) onko siellä mallia, josta saisi pienellä muokkauksella sopivan.


## Tallennetut raportit

Kohan tallennetuissa raporteissa voi käyttää ehdoissa hyväksi myös auktorisoituja arvoja, jolloin ne saadaan kyselyn ajovaiheessa alasvetovalikkoon. Ne määritellään käyttöön seuraavasti:

_sarakkeen nimi = <<Kuvaus tiedosta|auktorisoitu arvo>>_

Se näkyy raportin ajovaiheessa näin:
!kuvausauktORisoitu.jpg!

### 1. Kirjasto

```
SELECT * FROM items WHERE homebranch=<<Valitse kirjasto|branches>>
```

!kirjasto.png!

tai

```
SELECT * FROM bORrowers WHERE branchcode=<<Asiakkaan kotikirjasto|branches>>
```

## 2. Hyllypaikka

```
SELECT * FROM items WHERE location=<<Hyllypaikka|loc>>
```

!hyllypaikka.png!

## 3. Aineistolaji

```
SELECT * FROM items WHERE itype=<<Aineistolaji|itemtypes>>
```

!aineistolajit.png!

## 4. Kokoelma

```
SELECT * FROM items WHERE ccode=<<Kokoelma|ccode>>
```

!kokoelma.png!

## 5. Päivämäärän valinta kalenterista

```
SELECT * FROM issues WHERE issue_date=<<Lainauspäivä|date>>
```

!kalenterivalikko.png!

## 6. Linkin lisääminen rapORtille

RapORttiin voi lisätä linkin esimerkiksi asiakkaaseen, teokseen, niteeseen, luettelointitietueeseen tai varaukseen. Se tehdään CONCAT-toiminnolla SELECT-riville. Kohdeosoitteen voi tarkistaa osoiteriviltä halutussa Kohan osiossa.

### Asiakkaaseen

Linkki asiakkaaseen siten, että tekstinä näkyy kirjastokORtin numero ja osoitteeseen lisätään asiakkaan bORrowernumber. Linkki avautuu uuteen välilehteen.

```
SELECT CONCAT('<a href=\"/cgi-bin/koha/members/mORemember.pl?bORrowernumber=',b.bORrowernumber,'" target="_blank">',b.cardnumber,'</a>') AS 'Asiakas'
FROM bORrowers b
WHERE zipcode=<<Postinumero>>
```

b.cardnumber-tiedon sijalle voi periaatteessa laittaa minkä tahansa bORrowers-taulun tiedon, mutta kannattaa muistaa ettei tee turhia asiakastietojen katseluja rapORteillakaan.

### Teoksen perustiedot-näytölle

Linkki teokseen siten, että tekstinä näkyy teoksen nimeke ja osoitteeseen lisätään teoksen biblionumber. Linkki avautuu uuteen välilehteen.

```
SELECT CONCAT('<a href=\"/cgi-bin/koha/catalogue/detail.pl?biblionumber=',b.biblionumber,'" target="_blank">',b.title,'</a>') AS Nimeke
FROM biblio b
WHERE datecreated BETWEEN <<Luontipäivä aikaisintaan|date>> AND <<Luontipäivä viimeistään|date>>
```

###  Niteen muokkaukseen

Linkki tietyn niteen muokkaukseen niin, että osoitteeseen lisätään biblionumber, itemnumber ja linkkitekstiksi tulee viivakoodi. Linkki avautuu uuteen välilehteen.

```
SELECT CONCAT('<a href=\"/cgi-bin/koha/cataloguing/additem.pl?op=edititem&biblionumber=',i.biblionumber,'&itemnumber=',i.itemnumber,'" target="_blank">',i.barcode,'</a>') AS 'Viivakoodi'
FROM items i
WHERE i.ccode='CELIA'
```

### Tietueen muokkaukseen

Linkki tietueen muokkaukseen siten, että osoitteeseen lisätään biblionumber ja linkin tekstiksi tulee biblionumber. Linkin tekstiksi voi helposti muokata myös teoksen nimen halutessaan vaihtamalla jälkimmäiseen b.biblionumber-kohtaan b.title. Linkki avautuu uuteen välilehteen.

```
SELECT CONCAT('<a href=\"/cgi-bin/koha/cataloguing/addbiblio.pl?biblionumber=',b.biblionumber,'" target="_blank">',b.biblionumber,'</a>') AS 'Teos',
FROM biblio b
WHERE datecreated=<<Valitse päivä|date>>
```

### Varausjonoon

Linkki tietueen varausjonoon siten, että linkkitekstinä on tietueen title. Linkki avautuu uuteen välilehteen.

```
SELECT CONCAT('<a href=\"/cgi-bin/koha/reserve/request.pl?biblionumber=',b.biblionumber,'" target="_blank">',b.title,'</a>') AS 'Varausjonoon'
FROM reserves r
JOIN biblio b USING (biblionumber)
WHERE r.branchcode=<<Valitse noutokirjasto|branches>>
```

## Pölkyillä vai ei?

Monesti kyselyt kirjoitetaan niin, että "käskyt" kirjoitetaan pölkkykirjaimin, jolloin ne on helpompi erottaa tekstin seasta. Kohan kannalta ei ole merkitystä, kirjoitetaanko pölkyillä vai ei.

## Ei toimi?

* tarkista, että hipsuilla " tai ' on vastakappaleet, monesti ne esiintyvät pareittain
* tarkista kirjoitusvirheet. Esimerkiksi biblionumber-sanan voi kirjoittaa kovin monella tapaa väärin (bilionumber, biblionumer..)
