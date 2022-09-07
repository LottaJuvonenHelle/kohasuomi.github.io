---
title: 'Kohan ohje suomeksi'
permalink: /dokumentaatio/raportit/
redirect_from:
  - /theme-setup/
toc: true
---

# 7. Raportit

Raporteilla voi hakea tietokannasta mm. tilastotietoja ja erilaisia
listoja asiakkaista, teoksista tai niteistä. Jos sinulla on oikeus
käyttää raportteja, pääset niihin joko etusivun kautta

![](/assets/files/docs/Raportit/raportit1.png)

tai yläreunan _Muita toimintoja_ -valikosta  
![](/assets/files/docs/Raportit/raportit2.png)

Raportit-osiossa on sekä Kohan omat raporttitoiminnot, että
Koha-Suomessa kehitetty Raportointi-työkalu (Muu-osiossa
_Raportointi_).  
![](/assets/files/docs/Raportit/raportit3.png)

## 7.1 Kohan raportit

Kohan raporteissa on kolme erilaista toimintoa

1.  Ohjatut raportit -osiossa voi tehdä itse SQL-kyselyitä ohjatusti tai
    käyttää tallennettuja raportteja.
2.  Tilastovelholla voi hakea tilastoja eri aihealueista käyttäen
    valmiita vaihtoehtoja
3.  Oikeassa reunassa on valmiita raportteja

### 7.1.1 Ohjatut raportit

Ohjatuissa raporteissa voi luoda ohjatusti uusia raportteja. Tätä
käyttääksesi, sinulla pitää olla oikeus luoda raportteja. Vaikka
toiminto kuulostaa helpolta käyttää, ei se ikävä kyllä sitä ole.
Valittavissa olevat vaihtoehdot ja niiden yhdistelyvaihtoehdot ovat
rajalliset. Toiminnolla saa tehtyä helposti suhteettoman isoja hakuja.

Valitse _Luo uusi_  
![](/assets/files/docs/Raportit/raportit4.png)

Valitse sitten, mihin Kohan osa-alueeseen kohdistuvan raportin haluat
luoda.  
![](/assets/files/docs/Raportit/raportit5.png)

Valitse, mihin muotoon raportin haluat  
![](/assets/files/docs/Raportit/raportit6.png)

Valitse näytettävät/käytettävät tietokannan taulut ja sarakkeet  
![](/assets/files/docs/Raportit/raportit7.png)

Valitse rajoituskriteerit  
![](/assets/files/docs/Raportit/raportit8.png)

Valitse yhteenlaskettavat tiedot  
![](/assets/files/docs/Raportit/raportit9.png)

Valitse raportin järjestys  
![](/assets/files/docs/Raportit/raportit10.png)

Näe nyt, minkälaisella SQL-kyselyllä tietoja lähdetään hakemaan
tietokannasta. Joudut vielä tallentamaan raportin.  
![](/assets/files/docs/Raportit/raportit11.png)

Anna raportille nimi ja tallenna  
![](/assets/files/docs/Raportit/raportit12.png)

Voit nyt ajaa juuri tekemäsi raportin _Aja raportti_ -napista
painamalla.  
![](/assets/files/docs/Raportit/raportit13.png)

#### 7.1.2.1 Käytä tallennettua raporttia

Tallennettuista raporteista löytyvät ohjatun raporttien luonnin kautta
tehdyt ja SQL-kyselyillä tehdyt raportit.

![](/assets/files/docs/Raportit/raportit14.png)

- Kaikki-välilehdeltä löytyy kaikki tallennetut raportit
- Muilta välilehdiltä löytyy niihin määritetyt raportit. Määritys
  tehdään raportin tallennuksen yhteydessä.
- Haku-kentällä voi rajata taulukossa näkyviä raportteja. Jos tiedät
  raportin nimen, voit hakea sen nimellä suoraan.

Raportin voi ajaa valitsemalla rivin oikeasta reunasta _Käynnistä_  
![](/assets/files/docs/Raportit/raportit15.png)

Käynnistä-napissa on pieni nuoli, jonka alta löytyy muita vaihtoehtoja  
![](/assets/files/docs/Raportit/raportit16.png)

- _Näytä_-vaihtoehdolla näet raportin SQL-koodin
- _Muokkaa_-vaihtoehdolla voi muokata raportin SQL-koodia
- _Kopioi_-vaihtoehdolla voi kopioida raportin SQL-koodin ja muokata
  sitä uutena raporttina
- _Ajastus_-vaihtoehdolla voi ajastaa raportin käynnistymään tiettynä
  ajankohtana. **HUOM!** Ajastus ei toimi.

Ajettavan raportin ominaisuuksista/määrityksistä riippuu, mitä
käynnistyksen jälkeen tapahtuu. Osa raporteista voi pyytää käyttäjää
valitsemaan esimerkiksi kirjaston tai päivämäärän. Osa ei kysy mitään
lisämäärityksiä.  
![](/assets/files/docs/Raportit/raportit161.png)

Raportin määrityksistä riippuu myös, mitä sarakkeita ja tietoja tulee
näkyviin.

![](/assets/files/docs/Raportit/raportit18.png) ![](/assets/files/docs/Raportit/raportit17.png)

- Tulosten kokonaismäärä näkyy otsikon ja selitteen alapuolella
- Riviä sivulla -valikosta voit määrittää, kuinka monta hakutulosta
  näytetään per sivu. Joissain raporteissa on voitu määrittää
  valmiiksi, että näytetään tietty määrä rivejä.

### 7.1.2 Tilastovelho

Tilastovelholla pystyy hakemaan tietoja tietokannasta seitsemästä eri
aihealueesta.

![](/assets/files/docs/Raportit/raportit19.png)

#### Hankintatilastot

![](/assets/files/docs/Raportit/raportit20.png)

- Tilastoja voi hakea kahden kriteerin perusteella. Valitse haluamasi
  vaihtoehdot _Rivi_- ja _Sarake_-kohtiin.
- Valitse myös _Solun arvo_ -kohdasta, mitä haettaville luvuille
  tehdään. Lasketaanko esim. kuinka monta nidettä.
- Valitse _Tulostus_-kohdasta, haluatko tulokset näytölle vai
  tiedostoon.

Valinnoistasi riippuen muodostuu tulos taulukoksi.

![](/assets/files/docs/Raportit/raportit21.png)

#### Asiakastilastot

![](/assets/files/docs/Raportit/raportit22.png)

- Tilastoja voi hakea kahden kriteerin perusteella. Valitse haluamasi
  vaihtoehdot _Rivi_- ja _Sarake_-kohtiin.
- Valitse _Tulostus_-kohdasta, haluatko tulokset näytölle vai
  tiedostoon.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit23.png)

#### Kokoelmatilastot

![](/assets/files/docs/Raportit/raportit24.png)

- Tilastoja voi hakea kahden kriteerin perusteella. Valitse haluamasi
  vaihtoehdot _Rivi_- ja _Sarake_-kohtiin.
- Valitse _Solun arvo_ -kohdasta, mitä valituille kriteereille
  tehdään.
- Valitse _Tulostus_-kohdasta, haluatko tulokset näytölle vai
  tiedostoon.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit25.png)

#### Lainaustilastot

![](/assets/files/docs/Raportit/raportit26.png)

- Tilastoja voi hakea kahden kriteerin perusteella. Valitse haluamasi
  vaihtoehdot _Rivi_- ja _Sarake_-kohtiin.
- Valitse _Solun arvo_ -kohdasta, mitä valituille kriteereille
  tehdään.
- Valitse _Tulostus_-kohdasta, haluatko tulokset näytölle vai
  tiedostoon.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit27.png)

#### Kausijulkaisutilaukset

![](/assets/files/docs/Raportit/raportit28.png)

- Valitse toimittaja ja kirjasto sekä otetaanko mukaan myös loppuneet
  tilaukset.
- Valitse _Tulostus_-kohdasta, haluatko tulokset näytölle vai
  tiedostoon.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit29.png)

#### Maksutilastot

![](/assets/files/docs/Raportit/raportit30.png)

- Valitse aikaväli, maksun tyyppi ja kirjasto
- Valitse _Tulostus_-kohdasta, haluatko tulokset näytölle vai
  tiedostoon.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit31.png)

#### Varaustilastot

![](/assets/files/docs/Raportit/raportit32.png)

- Tilastoja voi hakea kahden kriteerin perusteella. Valitse haluamasi
  vaihtoehdot Rivi- ja Sarake-kohtiin.
- Valitse _Solun arvo_ -kohdasta, mitä valituille kriteereille
  tehdään.
- Valitse _Tulostus_-kohdasta, haluatko tulokset näytölle vai
  tiedostoon.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit33.png)

### 7.1.3 Eniten…

#### Asiakkaat, joilla on eniten lainoja

![](/assets/files/docs/Raportit/raportit34.png)

- Valitse haluamasi päivämäärävälit
- Valitse halutessasi kirjasto
- Valitse halutessasi aineistolaji
- Valitse halutessasi asiakastyyppi

<!-- -->

- Voit rajoittaa tulosten määrää kirjoittamalla _Rajoita:_-kenttään
  numeron
- Alemmalla otsikottomalla (englanniksi By:) valikolla voit ryhmitellä
  tietoja esim. aineistolajin mukaan
- Valitse _Tulostus_ -kohdasta haluatko tulokset näytölle vai
  tiedostoon

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit35.png)

#### Eniten lainattu aineisto

![](/assets/files/docs/Raportit/raportit36.png)

- Valitse haluamasi kriteerit. HUOM! Luokka tarkoittaa tässä
  yhteydessä signumia eli ei pysty hakemaan pelkällä ykl-luokalla.
- Voit rajoittaa tulosten määrää _Rajoitukset_-kohdassa. Alemmasta
  nimettömästä (englanniksi By:) valikosta voit valita, ryhmitelläänkö
  tulokset jonkin kriteerin mukaan.
- Valitse Tulostus -kohdasta haluatko tulokset näytölle vai
  tiedostoon.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit37.png)

### 7.1.4 Ei käytössä

#### Asiakkaat, jotka eivät ole lainanneet

![](/assets/files/docs/Raportit/raportit38.png)

- Valitse asiakastyyppi. Voit myös valita, milloin asiakkaan on
  pitänyt viimeksi lainata.
- Voit rajoittaa tulosten määrää _Rajoitukset_-kohdassa. Alemmasta
  nimettömästä (englanniksi By:) valikosta voit valita, ryhmitelläänkö
  tulokset jonkin kriteerin mukaan.
- Valitse Tulostus -kohdasta haluatko tulokset näytölle vai
  tiedostoon.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit39.png)

#### Niteitä, joita ei ole lainattu

![](/assets/files/docs/Raportit/raportit40.png)

- Valitse kirjasto ja aineistolaji.
- Voit rajoittaa tulosten määrää _Rajoitukset_-kohdassa. Alemmasta
  nimettömästä (englanniksi By:) valikosta voit valita, ryhmitelläänkö
  tulokset jonkin kriteerin mukaan.
- Tulokset tulevat vain näytölle.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit41.png)

### 7.1.5 Muu

#### Kadonnut aineisto

![](/assets/files/docs/Raportit/raportit42.png)

- Voit rajata raporttia viivakoodin, kirjaston, aineistolajin ja
  kadonnut-tilan tyypin mukaan.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit43.png)

#### Tilauksia tilin mukaan

![](/assets/files/docs/Raportit/raportit44.png)

- Valitse tili
- Valitse, haluatko tulokset näytölle vai tiedostoon

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit45.png)

#### Luettelo aineistolajeittain

Raportti laskee niteitä.

![](/assets/files/docs/Raportit/raportit46.png)

- Valitse haluamasi kirjasto tai jätä tyhjäksi, jos haluat nähdä
  kaikkien kirjastojen tilanteen

Valinnastasi riippuen tuloksista muodostuu taulukko.

![](/assets/files/docs/Raportit/raportit47.png)

#### Keskimääräinen laina-aika

![](/assets/files/docs/Raportit/raportit48.png)

- Tilastoja voi hakea kahden kriteerin perusteella. Valitse haluamasi
  vaihtoehdot _Rivi_- ja _Sarake_-kohtiin.
- Valitse _Tulostus_ -kohdasta haluatko tulokset näytölle vai
  tiedostoon.

Valinnoistasi riippuen tuloksista muodostuu taulukko

![](/assets/files/docs/Raportit/raportit49.png)

---

## 7.2 Lainaus ja palautus -osion raportit

Lainaus ja palautus -osiossa on myös muutamia hyödyllisiä raportteja.

### 7.2.1 Varausjono

Varausjono-raportin avulla voi etsiä hyllyvarauksia.

**Huomaa:** Tämä ei ole Koha-Suomen suosittelema raportti hyllyvarausten
käsittelyyn.

Varausjono ehdottaa oletuksena sitä kirjastoa, johon käyttäjä on
kirjautunut.

![](/assets/files/docs/Raportit/Raportit1001.png)

Hakutuloksia voi suodattaa ja järjestellä yläreunan valikon avulla.
Näkyvillä olevia sarakkeita voi säätää _Sarakkeen näkyvyys_
-painikkeella.

![](/assets/files/docs/Raportit/raportit1002.png)

---

### 7.2.2 Hyllyvaraukset

**Huomaa:** Koha-Suomi suosittelee käyttämään tätä raporttia, kun
etsitään hyllyvarauksia.

**Huomaa myös:** Hyllyvarausraportti ei ole täysin reaaliaikainen,
vaikka se avautuukin nykyään nopeammin kuin ennen. Hyllyvarausraportin
tiedot haetaan tausta-ajolla, jonka kesto on varausten määrästä riippuen
muutamasta sekunnista useampaan minuuttiin. Tänä aikana käsiteltävien
niteiden ja varausten tiedot voivat muuttua ja listalle voi tulla
tietoa, joka ei pidä enää katseluhetkellä paikkansa. Tästä voi myös
johtua, että listalle voi päätyä tilanne, että toisesta kirjastosta
omaan kirjastoon kuljetettavana oleva nide näyttäisi olevan listan
mukaan hyllyssä omassa kirjastossa. Nide on palautettu kesken ajon ja
mennyt kuljetustilaan. Kuljetettavan niteen sijaintikirjastona on
tietokannassa kohdekirjasto. Tälle epäreaaliaikaisuudelle ei ikävä kyllä
voi tehdä mitään, koska tausta-ajolla kuluu työhönsä oma aikansa ja
tilanne taustalla muuttuu koko ajan, kun niteitä palautetaan lainasta
tai joku muu ehtii palauttaa omassa hyllyssä paikalla olevan niteen.

Hyllyvaraukset raportilla pystyy hakemaan näytölle kaikki voimassa
olevat hyllyvaraukset. Raportin toimintaan on tehty Koha-Suomessa
muutoksia käyttäjien toiveiden perusteella.

Teknisiä muutoksia

- raportin latautuminen on nopeampaa, 1800 hyllyvarauksen
  latautumiseen menee hieman reilu 7  
  sekuntia aiemman viiden minuutin asemesta
- raportin päivitysväli on nyt minimissään minuutti ja maksimissaan
  niin pitkä kuin raportin  
  generointiin kuluva aika on. Käytännössä siis hyllyvarauslistan
  pidentyessä päivitysväli harvenee.  
  Raportin avautumisnopeuteen tällä ei ole vaikutusta.
- koska raportti generoidaan nyt ennakkoon valmiiksi, ei rajaus ajan
  perusteella ole enää käytössä.  
  Raportti noudattaa järjestelmäasetuksia “HoldsToPullStartDate” ja
  “ConfirmFutureHolds”.

Nimeketietojen näkyvyys

- painosmerkintä on lisätty nimeketietojen yhteyteen
- osanumero näkyvissä

Nidetietojen näkyvyys

- kirjastot, hyllypaikat ja kokoelmat esiintyvät nyt raportissa
  lyhenteinä. Tapa on selkeämpi ja  
  helpommin filtteröitävissä, mutta sillä on myös jonkin verran
  vaikutusta raportin  
  latautumisnopeuteen.
- varaajan tiedot pudotetaan oletuksena pois, mutta raportille on
  mahdollista saada mukaan varaajan  
  nimi, varaustunniste tai korttinumero (tai vaikka kaikki kolme).
  Virkailijat tai pääkäyttäjät eivät pysty  
  tekemään tätä valintaa, vaan pääkäyttäjien täytyy pyytää muutos
  kehittäjiltä. Tämä ei kuitenkaan ole  
  suositeltavaa, koska silloin asiakastietoja käsitellään turhaan.
- kirjasto~~, hyllypaikka~~, kokoelma ja muut sarakkeet on
  aakkostettu.
- luokkasarakkeessa ei näytetä samaa luokkatietoa moneen kertaan.
- huomaathan, että luokka, hyllypaikka, kokoelma, nidehuomautukset,
  hyllytarkenne ja genre eivät  
  ole kohdakkain kirjastotiedon kanssa. Raportin vanha versio näytti
  erilaiselta, mutta toimi tältä osin  
  samalla tavalla kuin uusi.

Rivi- ja sarakemuutokset

- lisätty kokoelma, genre ja sublocation eli hyllytarkenne -sarakkeet
- noutokirjasto ja ensimmäisenä olevan varauksen tekoaika eriytetty
  omiin sarakkeisiinsa
- filtterit on siirretty raportin ylälaitaan
- sarakkeiden järjestystä on muutettu. Järjestyksestä on varmastikin
  olemassa paljon mielipiteitä, mutta  
  ne on nyt yritetty järjestellä siten, että ne olisivat käytännön
  työn kannalta toimivasti sijoiteltu ja  
  niiden keskinäisessä sijainnissa olisi logiikka.
- huomaathan, että sarakkeita pystyy myös itse piilottamaan ja
  laittamaan näkyville yläreunan  
  _Sarakkeen näkyvyys_ -napista.
- pääkäyttäjät voivat säätää sarakkeiden oletusnäkyvyyttä Kohan
  ylläpidosta kohdasta Muut parametrit  
  _Sarakkeiden määrittely_. Siellä on Lainaus ja palautus –osiossa
  kohta (id=holds-to-pull).

**10.5.2019 Nimeke-kenttään lisätty sarja-tieto 490-kentästä**. Huomaa,
että ensin tulee 490a-kentän toistumat, vasta sitten numerot. Tämä
johtuu siitä, että tietoa ei haeta suoraan MARCista vaan tietokannan
sarakkeista, jolloin a-kenttien tiedot päätyvät samaan sarakkeeseen ja
ne myös näytetään raportilla sitten peräkkäin.

![](/assets/files/docs/Raportit/raportit1003.png)

Vinkkejä:

- valitse kirjasto-sarakkeista oma kirjasto, jolloin pystyt helposti
  tarkistamaan omassa kirjastossa paikalla olevat varaukset, joiden
  noutopiste on myös oma kirjastosi.
- rajaa lista esimerkiksi aineistolajin mukaan pelkkiin DVD-levyihin
  tai hyllypaikan mukaan aikuisten hyllypaikalle.
- tarkista, ettei listalle ole jäänyt varauksia roikkumaan pitkäksi
  aikaa järjestämällä Varauspvm-sarake nousevasti, jolloin
  ylimmäiseksi tulee vanhimmat varaukset.

### Noudettavissa olevat varaukset

### Varauksia per nide

### Vastaanotettavat kuljetukset

### Myöhässä

### Myöhässä ja maksuja

## 7.3 Koha-Suomen raportointityökalu

Koha-Suomen kehittämä raportointityökalu löytyy Raportit-osiosta
Raportointi-linkin takaa.

![](/assets/files/docs/Raportit/raportit50.png)

#### Asetukset

Työkalua varten pitää määrittää, miten tiedot jaotellaan
OKM-tilastoissa. Määrityksen voi tehdä Raportointi-osiosta löytyvän
_Asetukset_-nappulan kautta tai etsimällä se järjestelmäastuksista
hakusanalla “OKM”.

![](/assets/files/docs/Raportit/raportit51.png)

Asetuksessa määritetään, miten aineistolajit, asiakaslajit ja
hyllypaikat jaotellaan OKM-tilastoihin sekä, mitkä niteen tilat ei oteta
mukaan tilastoihin.

![](/assets/files/docs/Raportit/raportit52.png)

- _itemTypeToStatisticalCategory_-otsikon alle mitkä aineistolajit
  ovat
  - Kirja-aineistoa: _Books_
  - Äänitteitä: _Recordings_
  - Nuotteja: _SheetMusicAndScores_
    - Jaotellaan automaattisesti MARC-luettelointitietojen mukaan
      Musiikkiäänitteisiin ja Muihin äänitteisiin.
  - Videoita: Videos
  - CD-ROMeja: _CDROMs_
  - DVD:tä ja Blu-rayta: _DVDsAndBluRays_
  - Muita: _Other_
  - Aikakauslehtiä: _Serials_
  - Celia-aineistoa: _Celia_
  - Elektronisia aineistoja: _Electronic_
  - Verkkoaineistoja: _Online_

<!-- -->

- _patronCategories_-otsikon alle merkitään tilastoihin mukaan
  otettavat asiakaslajit. Eli esim. jos käytössä on
  “EITILASTO”-asiakastyyppi, jonka lainoja ei lasketa mukaan, niin
  sitä ei merkitä tähän mukaan.

<!-- -->

- _notForLoanStatuses_-kohtaan merkitään ne notforloan-tilat, joita ei
  oteta mukaan kokoelmatilastoihin. Esim. tilattu-tilassa olevat
  niteet.

<!-- -->

- _adultShelvingLocations_-kohtaan merkitään hyllypaikat, jotka
  sisältävät aikuisten aineistoa.

<!-- -->

- _juvenileShelvingLocations_-kohtaan merkitään hyllypaikat, jotka
  sisältävät lasten aineistoa.

Esimerkkikonfiguraatio:

    ---
    blockStatisticsGeneration: 0
    itemTypeToStatisticalCategory:
      KI: Books
      LA: Trash
      AR: Books
      SA: Books
      NU: SheetMusicAndScores
      KA: Recordings
      CD: Recordings
      LP: Recordings
      MP: Recordings
      SI: Recordings
      KA: Recordings
      CD: Recordings
      LP: Recordings
      MP: Recordings
      SI: Recordings
      VV: Videos
      CR: CDROMs
      BR: DVDsAndBluRays
      DV: DVDsAndBluRays
      DI: Other
      ES: Other
      KR: Other
      KP: Other
      MF: Other
      MK: Other
      MV: Other
      PE: Other
      TY: Other
      CE: Celia
      EK: Electronic
      VA: Online
    patronCategories:
      - HENKILO
      - KAUKOLAINA
      - KOTIPALVEL
      - LAPSI
      - MUUHUOL
      - YHTEISO
    notForLoanStatuses:
      - -1
    adultShelvingLocations:
      - AIK
      - VAR
      - MUS
      - LEH
      - KOT
      - OU
      - OUV
      - K
      - PALVELUT
    juvenileShelvingLocations:
      - LN
      - KOULU
      - VARLN
      - LUKIO

#### Tilastoryhmä

Kohaan pitää luoda tilastoja varten uudet kirjastoryhmät, jotta ne
näkyisi työkalun _Kirjastoryhmä_-valikossa.

![](/assets/files/docs/Raportit/raportit61.png)

Yleensä tilastoja halutaan kuntatasolla, joten luo jokaiselle kimpan
kunnalle oma ryhmä. Mene Ylläpito -&gt; Kirjastot ja ryhmät -&gt; Uusi
ryhmä  
![](/assets/files/docs/Raportit/raportit59.png)

- _Tyyppikoodi_-kohtaan pitää keksiä tunnus, joka päättyy merkkeihin
  STATS. Esim. OUSTATS, JOESTATS jne. Noiden merkkien perusteella
  raportointityökalussa näytetään vain tilastoryhmät.
- _Nimi_- ja _Kuvaus_ -kohtiin soveltuvat tiedot.
- _Luokkatyypiksi_ valitaan “Asetukset”.
- **Ei valintaa** kohtaan _“Näytä hakuvalikossa:”_.

Käy sitten muokkaamassa kaikkia (tarvittavia) kirjastoja ja valitse
niille tilastoryhmä. Muista tallentaa.

![](/assets/files/docs/Raportit/raportit60.png)

### Raportointityökalun käyttäminen

Raportointityökalu koostuu kahdesta osiosta:  
![](/assets/files/docs/Raportit/raportit53.png)

- _oma_-osiossa on ns. jokapäiväiseen käyttöön tarkoitetut raportit
- _okm_-osiossa on raportit, joilla saa otettua OKM-tilastot

### Raportin valinta

- Valitse ensin, kumpaa osiota haluat käyttää. Alasvetovalikon sisältö
  muuttuu valinnan mukaan.
- Valitse alasvetovalikosta raportti, jota haluat käyttää.
- Valitse aikaväli. Huomaa, että joissain raporteissa valittavissa on
  vain yksi päivä.

#### Suodatus

![](/assets/files/docs/Raportit/raportit54.png)

- Valitse _Suodata_-osiosta haluamasi kriteerit. Valittavissa olevat
  vaihtoehdot vaihtelevat valitun raportin mukaan.

#### Ryhmitä

![](/assets/files/docs/Raportit/raportit55.png)

- Valitse _Ryhmitä_-osiosta, minkä tietojen mukaan tulokset
  ryhmitetään. Valittavissa olevat vaihtoehdot vaihtelevat valitun
  raportin mukaan.
- Ryhmitä-osion valintojen ei tarvitse olla samoja kuin
  Suodata-osiossa.

#### Järjestä ja rajaa

![](/assets/files/docs/Raportit/raportit56.png)

- Joissain raporteissa voi rajoittaa tulosten määrää _Järjestä ja
  rajaa_ -osiossa. Tämä tulee näkyviin vain joissain raporteissa.  
  ![](/assets/files/docs/Raportit/raporti561.png)
- Joissain tapauksissa _Ryhmitä_-osion valinta tuo esille lisävalinnan

### Tulokset

![](/assets/files/docs/Raportit/raportit57.png)

- Tulokset saa joko näytölle tai tiedostoon. Voit myös tyhjentää
  valinnat tässä.

Tulosten ulkoasu riippuu valitusta raportista, suodatuksista ja
ryhmityksistä. Joissain raporteissa tuloksena on lista niteistä,
joissain numeerinen tilasto.

![](/assets/files/docs/Raportit/raportit58.png)

---

## 7.4 OKM-tilastot

OKM-tilastot -raportilla otetaan OKM:n määrittämien ehtojen mukaiset
tilastot. Se ajetaan kahdella eri syklillä: kuukausittain
kirjastoyksiköittäin ja vuosittain kunnittain.

Raporttiin liittyy järjestelmäasetus nimeltään OKM, johon tehdään tietyt
määritykset. Loput määritykset tulee suoraan työkalun koodista ja niitä
määrityksiä on avattu alla.

### 7.4.1 Järjestelmäasetuksen määritykset

Asetuksessa määritetään, miten aineistotyypit, asiakaslajit ja
hyllypaikat jaotellaan OKM-tilastoihin sekä, mitkä niteen tilat ei oteta
mukaan tilastoihin.  
<img src="/assets/files/docs/Raportit/raportit52.png" title="OKM-järjestelmäastus" alt="OKM-järjestelmäastus" style="width:80.0%" />

- _itemTypeToStatisticalCategory_-otsikon alle, mitkä aineistotyypit
  ovat
  - Kirja-aineistoa: _Books_
  - Äänitteitä: _Recordings_
  - Nuotteja: _SheetMusicAndScores_
    - Jaotellaan automaattisesti MARC-luettelointitietojen mukaan
      Musiikkiäänitteisiin ja Muihin äänitteisiin.
  - Videoita: Videos
  - CD-ROMeja: _CDROMs_
  - DVD:tä ja Blu-rayta: _DVDsAndBluRays_
  - Muita: _Other_
  - Aikakauslehtiä: _Serials_
  - Celia-aineistoa: _Celia_
  - Elektronisia aineistoja: _Electronic_
  - Verkkoaineistoja: _Online_

<!-- -->

- _patronCategories_-otsikon alle merkitään tilastoihin mukaan
  otettavat asiakaslajit. Eli esim. jos käytössä on
  “EITILASTO”-asiakastyyppi, jonka lainoja ei lasketa mukaan, niin
  sitä ei merkitä tähän mukaan.

<!-- -->

- _notForLoanStatuses_-kohtaan merkitään ne notforloan-tilat, joita ei
  oteta mukaan kokoelmatilastoihin. Esim. tilattu-tilassa olevat
  niteet.

<!-- -->

- _adultShelvingLocations_-kohtaan merkitään hyllypaikat, jotka
  sisältävät aikuisten aineistoa.

<!-- -->

- _juvenileShelvingLocations_-kohtaan merkitään hyllypaikat, jotka
  sisältävät lasten aineistoa.

Esimerkkikonfiguraatio:

    ---
    blockStatisticsGeneration: 0
    itemTypeToStatisticalCategory:
      ALEHTI: Serials
      ARTIKKELI: Other
      ATLAS: Books
      BLURAY: Videos
      BRAILLE: Books
      CD: Recordings
      PUHECD: Recordings
      CDROM: Other
      DATKAS: Other
      DIA: Other
      DVD: Videos
      EKIRJA: Electronic
      ELEKTRON: Electronic
      ELOKUVA: Videos
      ESINE: Other
      EVIDEO: Electronic
      KAAVIO: Other
      KALVO: Other
      KARTTA: Other
      PUHEKAS: Recordings
      KAUKOKART: Other
      KAUSIJULK: Serials
      KIRJA: Books
      KIRJANOSA: Books
      KOKOELMA: Other
      KOLLAASI: Other
      KONSOLIP: Other
      KASIKIRJ: Books
      LEVYKE: Other
      MAALAUS: Other
      MAGNEETTI: Other
      MIKROF: Other
      MONIVIES: Other
      MUSATAL: Recordings
      MUU: Other
      MUUPAINATE: Other
      NAUHAKAS: Other
      NUOTTI: SheetMusicAndScores
      OPTINEN: Other
      PIIRIKOT: Other
      PIIRROS: Other
      PAIVITTYVA: Other
      RAINA: Videos
      KORTTI: Other
      SLEHTI: Serials
      SARJANOSA: Other
      TYOPIIR: Other
      VALOKUVA: Other
      NEGATIIVI: Other
      VIDEO: Videos
      VIDEOKAS: Videos
      VIDEOKELA: Videos
      VIDEOLEVY: Videos
      VIDEOSILM: Videos
      AANIKAS: Recordings
      AANILEVY: Recordings
      PUHELEVY: Recordings
      AANITALL: Recordings
      PUHETAL: Recordings
    patronCategories:
      - HENKILO
      - KAUKOLAINA
      - KOTIPALVEL
      - LAPSI
      - MUUHUOL
      - YHTEISO
    notForLoanStatuses:
      - -1
    adultShelvingLocations:
      - AIK
      - VAR
      - MUS
      - LEH
      - KOT
      - OU
      - OUV
      - K
      - PALVELUT
    juvenileShelvingLocations:
      - LN
      - KOULU
      - VARLN
      - LUKIO

### 7.4.2 Kovakoodatut määritykset

#### 7.4.2.1 Kirjastot ja kirjastoryhmät

OKM-tilastoryhmät määritetään ‘Kirjastot ja ryhmät’ -sivulla
ylläpidossa. Tilastoihin otetaan mukaan ne ryhmät, joiden tunnus päättyy
‘\_OKM’. Esim. JOE_OKM, OU_OKM. Vain näihin ryhmiin kuuluvat kirjastot
otetaan mukaan OKM-tilastoihin.

#### 7.4.2.2 Jako kielen mukaan

Nide lasketaan suomenkieliseksi, jos tietueen ensimmäinen 084$a-kenttä
on ‘fin’, tai kieltä ei ole määritetty.

Nide lasketaan ruotsinkieliseksi, jos tietueen ensimmäinen 084$a-kenttä
on ‘swe’.

Nide lasketaan muun kielisiin, jos tietueen ensimmäinen 084$a-kenttä ei
ole ‘fin’ tai ‘swe’, mutta se on määritetty.

#### 7.4.2.3 Jako lasten- ja aikuisten aineistoihin

Nide lasketaan lasten materiaaliksi ‘OKM’-järjestelmäasetuksessa
tehtyjen hyllypaikkamääritysten mukaan.

#### 7.4.2.4 Jako kauno- ja tietokirjoihin

Nide on kaunokirja, jos sen YKL-luokka on 80-85. Muut ovat tietokirjoja.

#### 7.4.2.5 Musiikkiäänitteet

Nide lasketaan musiikkitallenteeksi, jos sen YKL-luokka on 78.

#### 7.4.2.6 Hankinnat

Nide lasketaan mukaan hankintoihin, jos se on vastaanotettu määritetyllä
aikavälillä. Jos Hankinnat-osiota ei käytetä, nide kuitenkin lasketetaan
hankintoihin, jos se on lisätty kokoelmiin raportin ajossa määritettynä
ajanjaksona.

Ensin tarkistetaan tilauksen datereceived, sitten tilauksen ordernumber,
sitten niteen dateaccessioned ja jos mikään noista ei mätsää palautetaan 0.

#### 7.4.2.7 Lainat

Lainat sisältävät ensilainat ja uusinnat.

Lainoiksi lasketaan määritettynä aikavälinä tehdyt lainat, joiden
lainaajat kuuluvat OKM-järjestelmäasetuksessa ‘patronCategories’-kohtaan
määritettyihin asiakastyyppeihin.

Lainat lasketaan lainanneelle kirjastolle. Verkkokirjastouusinnan
kirjastoksi lasketaan niteen nykyinen sijainti uusintahetkellä.

Poistettujen niteiden lainat lasketaan mukaan lainatilastoihin.

#### 7.4.2.8 Kausijulkaisut

Aikakauslehtiä ei lasketa mukaan kokoelmiin, poistoihin ja hankintoihin.
Ne ovat mukana kokonaislainoissa.

#### 7.4.2.9 Poistot

Kaikki määritetyllä aikavälillä poistetut niteet, pois lukien
aikakauslehdet, lasketaan poistoiksi.

Poistettuja niteitä ei lasketa määritetyn aikavälin kokoelmiin ja
hankintoihin, koska hankintatietoja ei säilytetä.

Poistettujen niteiden lainat lasketaan mukaan lainatilastoihin.

### 7.4.3 Raportin käyttöohje

OKM-tilastot -raportti löytyy Raportit-osiosta OKM-tilastot-linkin
takaa.

OKM-tilastoraportin tiedot jaotellaan OKM:n laatimien ehtojen
mukaisesti. Sarakkeiden otsikoissa noudatetaan
[tilastot.kirjastot.fi](https://tilastot.kirjastot.fi/) -sivun
termistöä.

Ensin pitää valita haluamansa tilasto alareunan taulukosta.  
<img src="/assets/files/docs/Raportit/okm.png" title="Lista tarjolla olevista raporteista" alt="Lista tarjolla olevista raporteista" style="width:40.0%" />

- Mitä isompi **Raportin ID-tunnus** on, sitä tuoreempi se on
- **Alkupvm ja Loppumispvm** -sarakkeista näkee, miltä aikaväliltä
  tilastot ovat
- **Tilastoryhmät** -sarakkeesta näkee, onko tilasto jaoteltu
  - OKM-tilastoryhmän mukaan eli käytännössä kaikki kunnan
    kirjastojen tilastot yhteenlaskettuna. Tämä otetaan
    tyypillisesti kerran vuodessa, kun raportoidaan tilastot
    OKM:lle.
  - kirjastoittain, jolloin listautuu kaikki kirjastot tunnuksen
    mukaan aakkosjärjestykseen. Tällä voi seurata kuukausitilastoja.
  - yhden kirjaston tilastot, jolloin otsikkona on kirjaston tunnus.
    Tätä vaihtoehtoa ei tyypillisesti ole ehdolla, mutta se on
    teknisesti mahdollista ajaa.
- Tilasto avataan **Näytä**-linkistä
- Tilaston voi poistaa **Poista**-linkistä. Älä kuitenkaan poista
  tilastoja.

Kun raportin on avannut Näytä-linkistä, pystyy sen myös sen jälkeen
lataamaan tiedostoksi. Valitse muoto valikosta ja klikkaa sitten
“Lataa”.  
<img src="/assets/files/docs/Raportit/okm2.png" title="Tilasto avattuna ja sen alapuolella tiedostomuodon valinta ja Lataa-nappula" alt="Tilasto avattuna ja sen alapuolella tiedostomuodon valinta ja Lataa-nappula" style="width:40.0%" />
