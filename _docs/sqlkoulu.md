---
title: 'Miten tehdä SQL-raportteja'
permalink: /dokumentaatio/sqlkoulu/
redirect_from:
  - /theme-setup/
toc: true
---

Ohjeen tekijä: Johanna Räisä
Päivittänyt: Anneli Österman / 3.4.2020


"Koha-Suomen tietokantaskeema löytyy Dokumenteistä":https://tiketti.koha-suomi.fi/documents/52.

Tutkimusmatka Kohan tietokantaan -koulutuksen tallenne löytyy "täältä":https://youtu.be/lH7Z8OetO3c

# SQL-lauseiden rakentaminen

## Select-lause

Lause, jolla haetaan tietoa tietokannasta.
Yksinkertaisimmillaan lause on:
```
select * from borrowers;
```
Tällä komennolla haetaan kaikki taulun kentät ilman rajausta. Tätä tulee välttää raportteja luodessa, niissä pitäisi määritellä tarvittavat kentät.

Taulusta voidaan myös kysellä pelkästään tiettyjä kenttiä kirjoittamalla tähden tilalle halutut kentät.

```
select borrowernumber, cardnumber, address from borrowers;
```

Kenttien nimiä voidaan myös muuttaa, jos ei haluta näyttää englanninkielisiä. Tämä tapahtuu "as"-sanalla.

```
select borrowernumber as 'Asiakasnumero', cardnumber as 'Kortin numero', address as 'Osoite' from borrowers;
```

## Where

Jos halutaan rajata haku tiettyjen parametrien mukaan, niin silloin select-lauseeseen lisätään where-komento.

```
select * from borrowers where category = 'LAPSI';
```

Arvot, joissa on kirjaimia tulee olla hipsujen sisässä. Jos et tiedä onko kenttä numerokenttä, niin on turvallisinta ympäröidä hipsuilla.

Where-komentoon voi lisätä useita rajoituksia and- ja or-sanalla.

```
select * from items where itype = 'KIRJA' and location = 'A';
select * from items where itype = 'KIRJA' or itype = 'CD';
```

Mallissa And-sanan tulosjoukko muodostuu riveistä, joilla on aineistolaji kirja ja hyllypaikka aikuiset.
Mallissa Or-sanan tulosjoukko muodostuu riveistä, joilla on aineistolaji kirja tai aineistolaji cd. Eli tulosjoukko muodostuu kummastakin aineistolajista.

Joskus on helpompi saada tulosjoukko rajoittamalla negatiivisesti.

```
select * from items where itype != 'EKIRJA' and homebranch = 'MLI_PK';
```

Mallin haussa tulosjoukko muodostuu Mikkelin pääkirjaston kaikista muista niteistä paitsi e-kirjasta.

Jos Kohassa halutaan valita kirjastopiste ennen raportin käynnistystä niin silloin raporttin laitetaan ohjelmoitu valintatyökalu.

```
select * from items where itype != 'EKIRJA' and homebranch=<<Kotikirjasto|branches>>;
```

Käyttääksesi where-rajauksia sinun tulee tietää tunnusarvot. Tietokannassa käytetään lyhyitä tunnuksia, joilla on nopeampi hakea. Kuvaukset ovat yleensä ihmisiä varten ja ne näytetään vain käyttöliittymässä.

## Like

Select-lauseissa voidaan käyttää vertailussa myös like-sanaa. Esim, jos halutaan jonkun tietyn kunnan kirjastopisteet samaan tulosjoukkoon.

```
select * from items where homebranch like 'MLI%';
```

Mallin tulosjoukkoon tulee kaikki niteet kirjastopisteistä joiden lyhenne alkaa sanalla MLI. Like-vertailussa pystytään käyttämään %-merkkiä, joka toimii villinä korttina haussa. Tämä on todella paljon hitaampaa, kuin suoraan =-merkillä muodostettu lause.

Like-komennossakin on mahdollisuus negatiiviseen rakenteeseen.

```
select * from items where homebranch not like 'MLI%';
```

## Join

Haussa tulosjoukkoon saadaan tietoa muista tauluista relaatioiden avulla. Join-komento on keskeisessä roolissa tässä yhdistelyssä.

```
select b.author as 'Tekijä', b.title as 'Nimeke', i.location as 'Hyllypaikka', i.homebranch as 'Kotikirjasto' from items i 
join biblio b on i.biblionumber = b.biblionumber 
where i.itype = 'KIRJA';
```

Mallissa yhdistetään items-taulu ja biblio-taulu ja otetaan kummastakin tietoa tulosjoukkoon. Lauseessa tauluille on annettu lyhenteet, joita käytetään selventämään mistä taulusta tieto pitäisi tulla. Jos tauluissa on paljon saman nimisiä kenttiä, sql ei tiedä kummasta on kyse, siksi kentän eteen tulee laittaa tietoa taulusta joko taulun koko nimellä tai sitten määritellyllä lyhenteellä.

Lauseessa voi olla ääretön määrä join-komentoja, jos vain tauluilla on jokin yhdistävä kenttä (relaatio). Kuitenkin mitä enemmän yhdistetään taulujen tietoa sitä hitaammaksi haut käyvät.

Join-komentoja on erilaisia. "Katso visuaalinen esittely joinien eroista":https://www.codeproject.com/Articles/33052/Visual-Representation-of-SQL-Joins

## Taulujen aliakset

Kyselyssä voi määrittää tauluille aliaksen, jolla voi viitata muualla kyselyssä. Tämä on helppo ja nopea tapa kertoa, mistä taulusta tieto halutaan hakea, jos useassa taulussa on sama sarake käytössä. Jos taulua ei määrittele, ilmoittaa Koha tiedon olevan "ambiguous" eli epämääräinen eikä aja raporttia.

Aliaksen voi keksiä itse, mutta se kannattaa olla helposti muistettava ja lyhyt. Alias kirjoitetaan kyselyssä heti taulun nimen perään. Alla olevassa kyselyssä biblionumber löytyy kummastakin taulusta, joten se on määritetty haettavaksi biblio-taulusta.

```
SELECT b.title,b.biblionumber,i.barcode
FROM biblio b
JOIN items i USING (biblionumber)
WHERE i.holdingbranch='OUPK'
```

## Ajalla rajaaminen

Tulosjoukkon rajaaminen ajan mukaan voidaan määritellä monella eri tavalla, mutta yksin kertaisin on opetella between-lause.

```
SELECT *
FROM items
WHERE date(dateaccessioned) BETWEEN '2016-01-01' AND '2016-12-31';
```

Tietokannassa päivämäärät ovat yleensä muodossa 2016-01-01 12:00:00, mallin lauseessa halutaan vain päiväys eikä kellonaikaa. Siksi päivämäärä-kenttä on ympyröity date:lla.

Kohassa päivämäärä valinnan saa raporttiin kun vaihtaa nuo luvut sisäänrakennettuun valintatyökaluun.

```
SELECT *
FROM items
WHERE date(dateaccessioned) BETWEEN <<AloitusPvm |date>> AND <<LopetusPvm |date>>;
```

## Count

Count-komennolla voidaan laskea tulosjoukon rivien määrä yhteen.

```
select count(*) from items where itype = 'KIRJA';
```

## Group by

"Group by"-komennolla voidaan ryhmitellä tulosjoukkoa.

```
select * from issues group by itemnumber;
```

Mallin lause antaa lainat-taulusta tulosjoukon niteen numeron mukaan, eli joka rivillä on eri itemnumber. Tätä joudutaan käyttämään joskus jos tulosjoukkoon tulee paljon samoja rivejä. Tämä ei toimi yhdessä countin kanssa.

## Order by

"Order by"-komennolla voidaan järjestää tulosjoukkoa halutulla tavalla.

```
select * from borrowers order by surname asc;
```

Mallin lause järjestää tulosjoukon sukunimen mukaan nousevasti, eli A:sta Ö:hön.

```
select * from borrowers order by surname desc;
```

Mallin lause järjestää tulosjoukon sukunimen mukaan laskevasti, eli Ö:stä A:han.

## Limit

"Limit"-komennolla voidaan rajata hakutuloksen tulosjoukkoa.

```
select * from borrowers limit 100;
```

Mallin  lause hakee 100 ensimmäistä riviä borrowers-taulusta.


## Concat

Concat-komennolla voidaan muodostaa yhtenäisiä merkkijonoja. 

```
select concat(b.surname,' ', b.firstname) as 'Asiakas' from borrowers where category = 'HENKILO';
```

Mallissa yhteen sarakkeeseen tulee asiakkaan sukunimi, väli ja etunimi.

## ExtractValue

ExtractValue-komennolla voidaan kysellä tietoa kentän sisällä olevasta rakenteesta. Kannattaa huomioida, että nämä voivat hidastaa kyselyä.

```
select * from biblio_metadata bm
where ExtractValue(bm.metadata, '//datafield[@tag="773"]/subfield[@code="w"]') = '';
```

Jos MARC-kentän tiedot halutaan hakea vain taulukon sarakkeeseen, sen voi tehdä näin:

```
select title, ExtractValue(bm.metadata, '//datafield[@tag="264"]/subfield[@code="c"]')
FROM biblio_metadata bm
JOIN biblio b using (biblionumber)
where biblionumber=1234
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

## Null ja tyhjä

Tietokannassa voi olla kahden tyyppisiä "tyhjiä"-kenttiä. Null tarkoittaa, että kenttään ei ole määritelty mitään. Toinen vaihtoehto on, että kentässä on tyhjä merkkijono.

```
select * from items where barcode is null and homebranch = 'MLI_PK';
select * from items where barcode = '' and homebranch = 'MLI_PK';
```

Jos "tyhjiä" halutaan käyttää vertailussa niin silloin kannattaa testata kumpaakin yhtä aikaa.

```
select * from items where (barcode is null or barcode = '') and homebranch = 'MLI_PK';
```

Mallin tulosjoukko muodostuu niteistä, joilla ei ole viivakoodia. *Huomaa sulut or-vertailujen ympärillä!* Jos sekoitellaan and- ja or-vertailua, niin or pitää ympyröidä suluilla.

h1. Relaatiot

Relaatioilla tarkoitetaan tauluja yhdistäviä tekijöitä, kuten asiakkaiden relaatiota lainoihin.

```
select count(*) from borrowers b
join issues i on b.borrowernumber = i.borrowernumber
join old_issues oi on b.borrowernumber = oi.borrowernumber
where b.borrowernumber = 1;
```

Mallin lause antaa kaikki nykyiset ja vanhat lainat asiakkaalle, jonka borrowernumber on yksi.

Kohan relaatiot löytyvät tietokantarakenteesta. http://schema.koha-community.org/
Yleensä relaatiot on nimetty samalla nimellä, kuten mallissa kaikista tauluista löytyy borrowernumber-kenttä.

h1. Lauseen rakentaminen

Lausetta rakentaessa kannattaa miettiä mikä on päätaulu, eli mitä tietoa halutaan ja tarvitseeko siihen yhdistellä muita tauluja.

Esimerkki: Haluan asiakkaat ja niille maksut ajalta 01.06.2016-10.06-2016, lisäksi sellaiset maksut joita ei ole vielä maksettu. Järjestetään ne vielä päivämäärän mukaan laskevasti, eli uusimmasta vanhimpaan.

```
SELECT b.surname as 'Sukunimi', b.firstname as 'Etunimi', a.amountoutstanding as 'Maksun määrä', a.description as 'Kuvaus' FROM borrowers b
join accountlines a on b.borrowernumber = a.borrowernumber
where a.amountoutstanding != 0 and date(a.date) between '2016-06-01' and '2016-06-10' order by date desc;
```

Kannattaa myös katsoa ensin Koha-yhteisön raporttipohjista onko siellä mallia, josta saisi pienellä muokkauksella sopivan.
https://wiki.koha-community.org/wiki/SQL_Reports_Library

h1. Tallennetut raportit

Kohan tallennetuissa raporteissa voi käyttää ehdoissa hyväksi myös auktorisoituja arvoja, jolloin ne saadaan kyselyn ajovaiheessa alasvetovalikkoon. Ne määritellään käyttöön seuraavasti:

_sarakkeen nimi = <<Kuvaus tiedosta|auktorisoitu arvo>>_

Se näkyy raportin ajovaiheessa näin:
!kuvausauktorisoitu.jpg!

## 1. Kirjasto

```
SELECT * FROM items WHERE homebranch=<<Valitse kirjasto|branches>>
```

!kirjasto.png!

tai

```
SELECT * FROM borrowers WHERE branchcode=<<Asiakkaan kotikirjasto|branches>>
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

## 6. Linkin lisääminen raportille

Raporttiin voi lisätä linkin esimerkiksi asiakkaaseen, teokseen, niteeseen, luettelointitietueeseen tai varaukseen. Se tehdään CONCAT-toiminnolla SELECT-riville. Kohdeosoitteen voi tarkistaa osoiteriviltä halutussa Kohan osiossa.

### Asiakkaaseen

Linkki asiakkaaseen siten, että tekstinä näkyy kirjastokortin numero ja osoitteeseen lisätään asiakkaan borrowernumber. Linkki avautuu uuteen välilehteen.

```
SELECT CONCAT('<a href=\"/cgi-bin/koha/members/moremember.pl?borrowernumber=',b.borrowernumber,'" target="_blank">',b.cardnumber,'</a>') AS 'Asiakas'
FROM borrowers b
WHERE zipcode=<<Postinumero>>
```

b.cardnumber-tiedon sijalle voi periaatteessa laittaa minkä tahansa borrowers-taulun tiedon, mutta kannattaa muistaa ettei tee turhia asiakastietojen katseluja raporteillakaan.

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
