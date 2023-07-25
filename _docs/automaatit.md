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
  * "Lapsiasiakkaat, joille ei ole omatoimiestoa":https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Valmiita_SQL-raportteja#Lapsiasiakkaat-joilla-ei-ole-omatoimiesto-asiakasm%C3%A4%C3%A4rett%C3%A4 -raportti
* Omatoimijärjestelmän toimittajan pitää määrittää ovikoneiden asetuksiin, että asiakkaan pääsy sallitaan tai estetään tietyillä PC-kentän (patron class, asiakastyyppi) arvoilla, riippuen siitä mikä on omatoimijärjestelmässä ja kimppakohtaisesti helpoin tapa. Toteutustapoja on järjestelmästä riippuen erilaisia.
  * Estämällä LAPSI-asiakastyyppi nämä asiakkaat eivät pääse sisään omatoimeen. Samoin voi tehdä tarvittaessa esim. YHTEISO-asiakastyypille (yhteisöasiakas). 
  * Sallimalla vain LAOMATOIMI- ja HENKILO-asiakastyyppien pääsyn, eli estää pääsyn muilta asiakastyypeiltä. 
  * Lapsiasiakkaiden pääsyn esto pitää tehdä kimpan sisällä kaikissa kirjastoissa samalla tavalla, mutta muiden asiakastyyppien eston voi päättää/määrittää kirjastokohtaisesti, mikäli kimpan käyttösäännöt sen sallivat.
* Ajasta j2a.pl-cronista toinen ajo, joka muuttaa LAOMATOIMI -> HENKILO (tukipyyntö). Huomaa, että ajo pitää tehdä kummallekin lapsi-tyypille.

Kun kaikki muutokset on tehty, pitää jatkossa valita jo lapsiasiakasta lisätessä, kumpaa asiakastyyppiä käytetään sen mukaan, antaako huoltaja luvan vai ei. Jos huoltaja sallii myöhemmin omatoimen, vaihdetaan asiakastyypiksi "Lapsi, omatoimi sallittu".

### OUTIn lisäykset

OUTI-kirjastoissa toimitaan muuten samalla tavalla, mutta OUTIssa huoltajan luvan tarvitsee alle 16-vuotiaat ja lapsiasiakas muuttuu 
henkilöasiakkaaksi täytettyään 18 vuotta. Tämän vuoksi OUTIssa tarvitaan lisäksi erillinen ajo, joka muuttaa 16 vuotta täyttäneiden 
asiakastyypiksi LAOMATOIMI-asiakastyypin.
