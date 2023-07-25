---
title: 'Automaatit ja omatoimi'
permalink: /dokumentaatio/automaatit/
redirect_from:
  - /theme-setup/
toc: true
---

Tälle sivulle on kerätty erilaisia automaatteihin ja omatoimeen liittyviä ohjeistuksia.

## Omatoimiesto lapsiasiakkaille

### Yleisohje

Osassa kimpoista lapsiasiakkaalla pitää olla huoltajan lupa omatoimikirjaston käyttöön. [Koha-Suomen asiantuntijaryhmä päätti 5/21 kokouksessa](https://koha-suomi.fi/asiantuntijaryhma2021#5-asiakastyyppi-omatoimiestoille), että omatoimi estetään erillisellä asiakastyypillä. Tämä esto voidaan toteuttaa seuraavalla tavalla:

* Luo asiakastyyppi LAOMATOIMI eli "Lapsi, omatoimi sallittu" (pääkäyttäjät). 
  * Laita asiakastyypin tyypiksi "Huollettava", jotta lisäys- ja muokkauslomakkeelle tulee takaajatieto valittavaksi.
  * Laita yläikärajaksi sama kuin LAPSI-asiakastyypillä.
  * Jos kimpassa on lapsiasiakkaita koskevia laina- ja maksusääntöjä, tee ne myös LAOMATOIMI-asiakastyypille. 
* Muuta LAPSI-asiakastyypin kuvaukseksi "Lapsi, omatoimi ei sallittu" (pääkäyttäjät).
* Muuta asiakastyypiksi LAOMATOIMI niille lapsiasiakkaille, joiden pitää päästä kirjautumaan omatoimeen. Tästä voi tehdä joko tukipyynnön tai asiakkaiden asiakastyypin voi muuttaa eräajona. 
* Omatoimijärjestelmän toimittajan pitää määrittää ovikoneiden asetuksiin, että asiakkaan pääsy sallitaan tai estetään tietyillä PC-kentän (patron class, asiakastyyppi) arvoilla, riippuen siitä mikä on omatoimijärjestelmässä ja kimppakohtaisesti helpoin tapa. Toteutustapoja on järjestelmästä riippuen erilaisia.
  * Estämällä LAPSI-asiakastyyppi nämä asiakkaat eivät pääse sisään omatoimeen. Samoin voi tehdä tarvittaessa esim. YHTEISO-asiakastyypille (yhteisöasiakas). 
  * Sallimalla vain LAOMATOIMI- ja HENKILO-asiakastyyppien pääsyn, eli estää pääsyn muilta asiakastyypeiltä. 
  * Lapsiasiakkaiden pääsyn esto pitää tehdä kimpan sisällä kaikissa kirjastoissa samalla tavalla, mutta muiden asiakastyyppien eston voi päättää/määrittää kirjastokohtaisesti, mikäli kimpan käyttösäännöt sen sallivat.
* Ajasta update_patron_category.pl-cronista toinen ajo, joka muuttaa LAOMATOIMI -> HENKILO (Tee tukipyyntö järjestelmänkehittäjille). Huomaa, että ajo pitää tehdä kummallekin lapsi-tyypille.

Kun kaikki muutokset on tehty, pitää jatkossa valita jo lapsiasiakasta lisätessä, kumpaa asiakastyyppiä käytetään sen mukaan, antaako huoltaja luvan vai ei. Jos huoltaja sallii myöhemmin omatoimen, vaihdetaan asiakastyypiksi "Lapsi, omatoimi sallittu".

### OUTIn lisäykset

OUTI-kirjastoissa toimitaan muuten samalla tavalla, mutta OUTIssa huoltajan luvan tarvitsee alle 16-vuotiaat ja lapsiasiakas muuttuu 
henkilöasiakkaaksi täytettyään 18 vuotta. Tämän vuoksi OUTIssa tarvitaan lisäksi erillinen ajo, joka muuttaa 16 vuotta täyttäneiden 
asiakastyypiksi LAOMATOIMI-asiakastyypin.

## SIP2-tunnusten käsittelyohje

Jokainen lainaus- ja palautusautomaatti sekä ovikone tarvitsee SIP2-tunnuksen, jotta se voi keskustella Kohan SIP2-palvelimen kanssa ja suorittaa oman tehtävänsä. Jos palautusautomaatissa on useampi palauttava kone (tai ns. syöttöaukko), niin jokaiselle koneelle pitää tehdä oma SIP2-tunnus.

Käyttäjätunnukset tekee ja toimittaa salattuna automaatin toimittajille ja Koha-Suomelle kimpan **pääkäyttäjät**.

### Käyttäjätunnuksen luonti

* jokaisella automaatilla/omatoimilaitteella täytyy tilastoinnin ja virheiden selvittelyjen vuoksi olla oma käyttäjätunnus Kohassa.
* kimpan pääkäyttäjät tekevät Kohaan uuden käyttäjätunnuksen, jonka asiakastyyppi on "Z Automaatti Z". Tunnuksen muodossa ja nimeämisessä kannattaa käyttää kaavaa, jolla tunnuksen tunnistaa tietyn kirjaston tunnukseksi. Esim. kirjaston lyhenne ja numeroita: KEPK0001. Tunnuksessa voi myös tulla esille automaatin tyyppi: Esim. KEPKLAI1
  * Huom. ei ääkkösiä tai erikoismerkkejä tunnukseen
* laita tunnukselle vanhentumispäiväksi kuluva päivä (muutetaan myöhemmin).
  * Kyseessä on tietoturvakysymys. Jos tunnus joutuu vääriin käsiin, niin sillä ei pääse kirjautumaan, kun tunnus ei ole voimassa.
* tunnukselle annetaan käyttäjäoikeudeksi _circulate_ -oikeus (valituksi tulee automaattisesti myös sen alaoikeudet, se on ok).
* salasanan pitää olla pitkä (kyberturvallisuuskeskus suosittelee vähintään 15 merkkiä) ja monimutkainen eli sisältää vähintään sekä kirjaimia että numeroita. Salasanan pitää olla vahva, koska SIP2-tunnuksella on laaja pääsy mm. asiakkaiden tietoihin.
* Salasanan tulee olla validia XML-koodia, eli kielletyt erikoismerkit on: & , < , > , " tai '  sen mukaan, kumpaa käytetty rajoittimena 
* merkitse asiakasmääreisiin automaatin tyyppi (lainausautomaatti, palautusautomaatti, ovikone jne) ja toimittaja.
  * Automaattityypin ja toimittajan lisääminen asiakasmääreeksi -ohje

### Käyttäjätunnuksen toimittaminen Koha-Suomelle

* käyttäjätunnus ja salasana toimitetaan järjestelmänkehittäjälle salatusti joko Matrixissa yksityisviestinä päivystäjälle/asiaa hoitavalle kehittäjälle, onetimesecretinä tai salattuna sähköpostina.
* Muista tehdä uuden tunnuksen lisäämisestä aina myös tukipyyntö GitHubiin, jotta tieto ei hautaudu vain sähköpostiin/Matrixiin ja työ saadaan myös tilastoitua.

  * Onetimesecret
    * mene osoitteeseen onetimesecret.com ja liitä käyttäjätunnus ja salasana tekstikenttään. Lisäksi tarvitaan tieto, mille SIP2-palvelimelle tunnus ja salasana lisätään sekä sen kirjastotoimipisteen koodi missä automaatti sijaitsee.
    * luo onetimesecret siten, että se on voimassa 7 päivää ja kopioi annettu url-osoite (huom. älä kopioi osoiteriviltä vaan nettisivulla ilmoitettu osoite)
    * lähetä onetimesecret-osoite kehittäjille osoitteeseen support [at] koha-suomi.fi ja pyydä kuittaamaan, kun tunnukset on otettu talteen.
  * jos sinulla on käytössä turvasähköposti, niin voit lähettää tunnukset myös suoraan sillä osoitteeseen support [at] koha-suomi.fi

* **tietoturvasyistä älä koskaan kirjaa tunnusta tai salasanaa GitHubiin tikettiin, äläkä lähetä salasanoja tai tunnuksia mihinkään salaamattomia tiedonsiirtoväyliä käyttäen (esimerkiksi salaamattomalla sähköpostilla)**
* järjestelmänkehittäjä lisää automaatin tiedot SIP2-palvelimelle.
  * automaatin XML-määritystiedosto pitää validoida aina, kun tiedostoon tehdään muutoksia, eli esim. <br />
  @ xmllint --noout your_test_file.xml; echo $?@<br />
  0 = ei virheitä<br />
  1 = virheitä (listattu)

### Käyttäjätunnuksen toimittaminen automaatin toimittajalle

* kimpan pääkäyttäjä toimittaa turvasähköpostilla tai onetimesecretinä SIP2-käyttäjätunnuksen, salasanan, organisaatiotunnuksen (institution, joka on sen kirjastotoimipisteen tunnus, jossa automaatti fyysisesti sijaitsee, esim. KEPK), SIP2-palvelimen osoitteen ja portin numeron salatusti automaatin/omatoimilaitteen toimittajalle, joka määrittää ne laitteelle.
  * mene osoitteeseen onetimesecret.com ja liitä yllä mainitut tiedot tekstikenttään.
  * luo onetimesecret siten, että se on voimassa 7 päivää ja kopioi annettu url-osoite (huom. älä kopioi osoiteriviltä vaan nettisivulla ilmoitettu osoite)
  * lähetä onetimesecret-osoite automaatin toimittajalle ja pyydä kuittaamaan, kun tunnukset on otettu talteen.
  * kun olet saanut kuittauksen, että tunnukset ovat oikean henkilön hallussa, käy muokkaamassa tunnus voimaan jatkamalla asiakkaan käyttöoikeus (hae tunnus asiakashaulla -> alemman rivin kohta: Muita toimintoja -> Asiakkaan käyttöoikeuden jatkaminen)

* jos sinulla on käytössä turvasähköposti, niin voit lähettää tunnukset myös suoraan sillä toimittajan osoitteeseen.

* **tietoturvasyistä älä koskaan kirjaa tunnusta tai salasanaa GitHubin tikettiin, äläkä lähetä salasanoja tai tunnuksia mihinkään salaamattomia tiedonsiirtoväyliä käyttäen (esimerkiksi salaamattomalla sähköpostilla)**

## Automaattityypin ja toimittajan lisääminen asiakasmääreeksi

Tässä ohjeessa neuvotaan, miten SIP2-tunnuksille eli Z Automaatti Z -asiakastyypeille voi lisätä käyttöön asiakasmääreet Automaatin toimittaja ja Automaattityyppi.

!{width:30%}Automaatti.png! !{width:30%}automaattitoim.png! !{width:30%}automaattityyppi.png!

Tee ensin auktorisoidut arvo ja sen jälkeen asiakasmääreet.

### Auktorisoitujen arvojen lisääminen

Lisää kaksi uutta auktorisoidun arvon tyyppiä ja niille auktorisoidut arvot. Eli joudut tekemään alla olevan ohjeen mukaisen prosessin kahdesti.

* Mene Ylläpito -> Auktorisoidut arvot
* Valitse _Uusi luokka_
* Kirjoita _Tyyppi_-kohtaan
  * TOIMITTAJAT kun kyseessä Automaatin toimittaja
  * AUTOMTYPE kun kyseessä Automaattityyppi
* Valitse _Uusi auktorisoitu arvo kohteelle AUTOMTYPE_ tai _Uusi auktorisoitu arvo kohteelle TOIMITTAJAT_ sen mukaan, kumpaa olet lisäämässä.
* Lisää alla olevat auktorisoidut arvot. Jos jotain puuttuu, niin voit lisätä ne tarvittaessa.

*AUTOMTYPE*

|Auktorisoitu arvo|Kuvaus| 
|---|---|
|Lainauspalautus|Lainaava ja palauttava|
|Lainaus|Lainausautomaatti|	
|Ovikone|Ovikone|
|Palautus|Palautusautomaatti|

!{width:50%}automtype.png!

*TOIMITTAJAT*

|Auktorisoitu arvo|Kuvaus| 
|---|---|
|Axiell|Axiell|
|Bibliotheca|Bibliotheca|	
|Mikrovayla|Mikroväylä|
|Supa|P. V. Supa|

!{width:50%}toimittajat.png!

Tämän jälkeen voit siirtyä tekemään asiakasmääreet.

### Asiakasmääreen lisääminen ja auktorisoitujen arvojen kytkeminen

Tee kaksi uutta asiakasmäärettä: Automaatin toimittaja ja Automaattityyppi

* Mene Ylläpito -> Asiakasmääreet
* Valitse *Uusi asiakasmääre*
* Kirjoita *Asiakasmäären tunnus* -kenttään tunnus
  * Automaatin toimittaja: TOIMITTAJA
  * Automaattityyppi: AUTOTYPE
* Kirjoita kuvaus
  * TOIMITTAJA: Automaatin toimittaja
  * AUTOTYPE: Automaattityyppi
* Laita rasti kohtaan *Haettavissa*
* Valitse *Auktorisoidun arvon luokka* -valikosta
  * AUTOTYPE: AUTOMTYPE
  * TOIMITTAJA: TOIMITTAJAT
* Valitse *Tyyppi*-valikosta Z Automaatti Z, jolloin asiakasmääre näkyy vain automaattitunnus-asiakastyypille

!{width:40%}toimittaja.png! !{width:40%}autotype.png!
