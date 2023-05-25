---
title: 'Kohan ohje suomeksi'
permalink: /dokumentaatio/tiedonhaku/
redirect_from:
  - /theme-setup/
toc: true
---

# 10. Tiedonhaku
## 10.1. Perushaku

Kun haluat hakea Kohasta, napauta _Hae tietokannasta_-linkkiä, kirjoita hakusanat ja paina Enter. Haun voi käynnistää myös valkeaa nuolta klikkaamalla.

![](/assets/files/docs/Tiedonhaku/Tiedonhaku1_haun_suorittaminen.png)

Haku yhdistää oletuksena hakusanat AND-operaattorilla, eli palauttaa tietueet, joiden tiedoissa esiintyvät kaikki annetut hakusanat. AND-operaattorin lisäksi haussa voi käyttää myös OR- ja NOT-operaattoreita. 

Hakusanojen automaattinen katkaisu on kimppakohtainen asetus (QueryAutoTruncate). Mikäli asetus on päällä hakusanat katkaistaan automaattisesti, eli haku _seitse_ kohdistuu kaikkiin merkkijonon _seitse_ sisältäviin sanoihin, kuten _seitsemän, seitsemäs tai kuusikymmentäseitsemän_.
Jos asetus ei ole päällä, tulee hakusanat katkaista *-merkillä.

Sanojen järjestys ei vaikuta hakutulokseen. Haku _tiedonhaku kirjastot_ antaa saman tuloksen kuin _kirjastot tiedonhaku_.  

Perushakuun voi lisätä rajauksen hakuindeksiin eli haluttuihin kenttiin tai haluttuun kirjastoon. Nämä ovat kimppakohtaisia asetuksia (_IntranetCatalogSearchPulldown_ ja _IntranetAddMastheadLibraryPulldown_). Rajaukset saa näkyviin hakulaatikon lopussa olevasta valikko-kuvakkeesta. Molemmat rajaukset ovat samanlaiset kuin tarkassa haussa.
Hakuindeksirajauksissa voi valita mihin kenttään haku kohdistuu. Kirjastorajaus rajaa hakutuloksen vain sellaisiin tietueisiin, joiden niteissä on joko koti- tai sijaintikirjastona valittu kirjasto.

![](/assets/files/docs/Tiedonhaku/Tiedonhaku1_haun_rajaus.png)

## 10.2. Hakusanojen etuliitteet

Voit kohdistaa haun tiettyihin kenttiin kirjoittamalla hakusanojen eteen etuliitteitä:

- ti: nimeke  
  esim. ti:kuparisydän

<!-- -->

- su: asiasana  
  esim. su:pilapiirrokset

<!-- -->

- pb: kustantaja  
  esim. pb:wsoy

<!-- -->

- au: tekijä  
  esim. au:lehtolainen

<!-- -->

- lcn: luokka  
  esim. lcn:78.61

<!-- -->

- ln: kieli  
  esim. ln:est

<!-- -->

- ccode: kokoelmakoodi  
  esim. ccode:lyla

[Lista etuliitteistä ja tarkemmat ohjeet etuliitteiden
käyttämiseen](https://koha-community.org/manual/21.11/en/html/searching.html#indexes) (englanniksi). 

## 10.3. Tarkka haku

Tarkassa haussa voit määrittää haun perushakua täsmällisemmin. 

Tarkka haku aukeaa napauttamalla Haku-painiketta ylälaidan valikossa. 
![](/assets/files/docs/Tiedonhaku/Tiedonhaku4_tarkka_haku.png)

Voit hakea kirjoittamalla hakusanat hakukenttiin ja valitsemalla alasvetovalikoista hakusanojen kohteet. Voit määrittää hakusanojen rajaavuuden valitsemalla niille alasvetovalikosta operaattorin _ja, tai, ei_. Lisää hakuehtoja voit lisätä \[+\]-painikkeella.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku5_tarkan_haun_hakulauseet.png)

Luokkarajaus on valikossa Standardinumero-kohdan alla:  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku7_luokkarajaus.png)

Voit valita hakutulosten järjestyksen _Järjestä_-valikosta. Oletuksena tulokset järjestetään julkaisuvuoden perusteella uusimmasta vanhimpaan. Muita vaihtoehtoja ovat esimerkiksi tekijä, nimeke ja suosio (lainamäärä).

![](/assets/files/docs/Tiedonhaku/Tiedonhaku6_jarjestys.png)

## 10.4. Hakutuloksen rajaaminen faseteilla

Hakutulosta voi rajata hakutuloslistan vasemman reunan faseteilla. Fasettien sisältö riippuu hakutuloksesta.

Jos olet hakenut hakusanalla _valokuvaus_,  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku14_fasetit_lahtotilanne.png)

voit rajata hakutulosta luonnonvalokuvausta käsitteleviin teoksiin valitsemalla _Asiasanat_-fasetista termin _luonnonvalokuvaus_. 
![](/assets/files/docs/Tiedonhaku/Tiedonhaku15_fasetit_rajaus.png)

Tämän jälkeen tuloslista näyttää vain luonnonvalokuvausta käsittelevät teokset. 
![](/assets/files/docs/Tiedonhaku/Tiedonhaku16_fasetit_lopputilanne.png)

## 10.5. Hakuhistoria

Tehtyjä hakuja voi tarkastella ja suorittaa uudelleen hakuhistoria-toiminnolla. Hakuhistoria on oikean yläkulman alasvetovalikossa. 
![](/assets/files/docs/Tiedonhaku/Tiedonhaku18_hakuhistoria_valikko.png)

Hakuhistoriassa haut on jaettu kuluvan istunnon aikana ja aiemmissa istunnoissa tehtyihin hakuihin.
![](/assets/files/docs/Tiedonhaku/Tiedonhaku19_hakuhistorianakyma.png)

Historian voi poistaa valitsemalla poistettavat haut ja klikkaamalla _Poista_.

**Huom.** Jos hakuhistoriaa ei itse poista, se säilyy Kohassa 1 kk ajan. Koha-Suomen [säilytysajat](https://koha-suomi.fi/dokumentaatio/tietojensailytysajat/#hakuhistoria).
{: .notice--warning}

## 10.6. Nidehaku

Nidehaulla voit esimerkiksi:

- Tutkia luokan niteiden määrää karsintaa varten. Huomaa kuitenkin, että haku palauttaa myös lainassa olevat niteet.
- Hakea nollalainoja.
- Hakea joukon niteitä ja muokata niiden tietoja eräajona.
- Tarkastaa, ovatko kaikki lehtiniteet siirretty pois lehtiemon alta.
- Tarkastaa, onko lehtien vanhoja numeroita jäänyt tietokantaan.

Nidehaku on _Haku_-valikossa.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku18_1_nidehaku.png)

Nidehaku palauttaa tuloksena listan hakuehdot täyttävistä niteistä. Haun muotoilu vastaa pääosin tarkkaa hakua.

Haun voi kohdistaa esimerkiksi niteiden viivakoodeihin, luokkiin, nimekkeisiin ja tekijöihin. Käytä hauissa aina valintalistan alaosan räätälöityjä hakukenttiä

![](/assets/files/docs/Tiedonhaku/Tiedonhaku19_1_hakukentat.png)

Muista kentistä ainoastaan ISBN ja ISSN toimivat luotettavasti.

Hakusanoja voi yhdistää operaattoreilla JA ja TAI. _Uusi kenttä_ lisää uuden hakukentän. 

Alla esimerkissä on lisätty uusi hakukenttä, asetettu molemmat hakusanat vaadituiksi JA-operaattorilla ja kohdistettu hakusanat _Nimeke_- ja _Henkilötekijä_-kenttiin. Lisäksi hakusanat on katkaistu %-merkeillä. 
![](/assets/files/docs/Tiedonhaku/Tiedonhaku20_nidehaun_tekstihaku.png)

Nidehaussa hakusanoja ei katkaista automaattisesti, joten ne kannattaa aina katkaista %-merkeillä. Esimerkiksi tekijä-haku _jansson, tove_ ei palauta  osumia, koska MARC-kentästä haettu tekijätieto päättyy pisteeseen tai pilkkuun. Haku _%jansson, tove%_ toimii oikein. Katkaisun lisäksi hakusanat on kirjoitettava aina tarkasti oikein. Esimerkiksi haku *%tove jansson*% ei palauta mitään, koska tekijätieto on muodossa _Jansson, Tove_. Yksittäisen merkin voi korvata merkillä \_ (alaviiva).

Hakua voi rajata myös sivun yläosan valintalistoilta. Valintalistoilla voi valita useita arvoja tekemällä valinnat CTRL-näppäin pohjassa. Ylimmän tyhjän arvon valinta ohittaa ehdon. Jos haluat rajata hakutuloksesta pois ehtoja, valitse valintalistalta _ei ole_, joka vastaa NOT-operaattoria.

Valitaan esimerkiksi Kotkan pääkirjaston lasten ja nuorten osaston niteet.

![](/assets/files/docs/Tiedonhaku/Tiedonhaku21_nidehaun_rajaukset.png)

Sivun alalaidassa on vielä rajaus luokkavälillä, niteen tilalla ja lainatiedoilla. Luokkavälillä rajaaminen toimii epäloogisesti. Haku palauttaa vain luokkarajauksen ylärajaa pienemmät tulokset. Esimerkiksi haku ![](/assets/files/docs/Tiedonhaku/Tiedonhaku22_nidehaku_luokkahaku.png) palauttaa luokkien 84.2-84.5 teokset. Haku luokasta 91 luokkaan 92 palauttaisi puolestaan vain 91-alkuisten luokkien niteet. Luokalla rajaaminen onnistuu helpommin käyttämällä räätälöityä kenttää “Luokka (084$a)”.

_Lainauksien määrä_ -valinnalla voit hakea niteitä lainamäärän perusteella. Lainauspäivämäärästä rajataan tuloksia niteen lainojen ajankohdan perusteella. Alla on haettu kaikki alle 10 kertaa lainatut niteet, jotka on lainattu 15.10.2022. 
![](/assets/files/docs/Tiedonhaku/Tiedonhaku27_nidehaun_lainarajat.png)

Kun olet valinnut ehdot, voit hakea napauttamalla _Haku_-painiketta. 
![](/assets/files/docs/Tiedonhaku/Tiedonhaku26_nidehaku_hakupainike.png)

Esimerkeissä valituilla ehdoilla hakutuloslista näyttää tältä. 
![](/assets/files/docs/Tiedonhaku/Tiedonhaku23_nidehaku_tulokset.png)

Voit tarkentaa hakua sarakkeiden ylälaidassa olevilla rajauskentillä: 
![](/assets/files/docs/Tiedonhaku/Tiedonhaku24_nidehaku_tulosten_lisafiltterit.png)

### Tulosten vienti CSV- tai -viivakooditiedostoksi

Tulokset voi halutessaan viedä ohjelmasta CSV- tai -viivakooditiedostona jatkokäyttöä varten ylälaidan painikkeilla. 
![](/assets/files/docs/Tiedonhaku/Tiedonhaku25_nidehaku_tulosten_painikkeet.png)

Hakua pääsee muokkaamaan painamalla _Muokkaa hakua_-painiketta.

## 10.7 Teostiedot

Yksittäisen teoksen tietoihin pääsee monta reittiä, esimerkiksi asiakkaan lainojen kautta tai tiedonhaun tuloksista. Teoksen Perustiedot-näytöllä näkee yleisimmin tarvittavat tiedot. Eri otsikot tulevat näkyville vain, jos teokselle on tallennettu kyseinen tieto.

Vasemmassa reunassa on näkyvissä järjestelmäastuksista ja käyttäjän oikeuksista riippuen seuraavat välilehdet

- Perustiedot
- MARC
- Otsikoitu MARC
- ISBD-näkymä
- Niteet
- Varaukset, sulkeissa varausten määrä
- Lainahistoria
- Muutosloki (vaatii erillisen käyttäjäoikeuden)

### Kuvailutiedot

![](/assets/files/docs/Tiedonhaku/tietue1.png)

- nimeke
- tekijät ja heidän funktiot
- osakohteissa linkki emotietueeseen
- teoksen kieli
- julkaisutiedot
- fyysinen kuvaus
- alkuteoksen nimi
- musiikkiaineistossa mm. soitinkokoonpano
- sisällön kuvailu eli asiasanat ja kohdehenkilöt ja -yhteisöt yms.
- luokitus (ykl ja fiktiivinen lisäluokka)
- linkit kansikuvaan ja kuvaukseen
- linkki verkkokirjastoon (sekä Kohan omaan että Finnaan, jos
  sellainen on käytössä)
- linkki MARC-esikatseluun, josta näkee kaikki teokselle tallennetut
  tiedot MARC-kentittäin
- kansikuva, jos sellaiseen on linkki
- linkki varauksiin
- musiikkiaineistolla ja erilaisilla artikkelikokoelmilla useimmiten
  linkit osakohteisiin ja tieto osakohteiden määrästä

### MARC-, Otsikoitu MARC ja ISBD-välilehdet

MARC  
![](/assets/files/docs/Tiedonhaku/tietue5.png)  
Otsikoitu MARC  
![](/assets/files/docs/Tiedonhaku/tietue6.png)  
ISBD  
![](/assets/files/docs/Tiedonhaku/tietue10.png)

### Nidetiedot ja niiden suodattaminen

Teoksen kuvailutietojen alla on tiedot siihen liittyvistä niteistä ja
niiden saatavuudesta. Näkyvillä olevia niteitä voi myös suodattaa
Valitsemalla nidetaulukon yläpuolelta _Suodata_. Järjestelmäasetuksesta
riippuen niteet ovat joko yhdellä välilehdellä tai jaettuna
kirjautumiskirjaston kokoelmaan ja muihin kokoelmiin. Kokoelman nimen
perässä näkyy välilehdellä olevien niteiden määrä.

![](/assets/files/docs/Tiedonhaku/tietue2.png)  
Niteistä kerrotaan

- aineistolaji
- sijaintikirjasto
- kotikirjasto, jonka yhteydessä myöa hyllypaikka ja hyllytarkenne
- kokoelma
- luokka (eli käytännössä “Kohan koko signum”)
- tila: saatavana, lainassa, kuljetettavana, kadonnut, ei lainata jne
  - jos teos on lainassa, kerrotaan asiakkaan kirjastokortin numero,
    mikä toimii myös linkkinä asiakastietoihin.
- viimeisin havainto (päivittyy mm. lainatessa ja palautettaessa. Myös
  silloin, kun palautetaan hyllyssä olevana)
- viivakoodi, jota klikkaamalla pääsee niteen tietoihin vasemman
  reunan Niteet-välilehdelle.
- kausijulkaisun numerointi, eli lehden numero, esim. 2019 : 1
- Yleiset huomautukset

Suodatus on kätevä toiminto  
![](/assets/files/docs/Tiedonhaku/tietue4.png)

Voit suodattaa näkyville esim.

- tietyn kirjaston niteet (sijainti- tai kotikirjasto)
- tietyn kokoelman niteet
- saatavana olevat niteet: kirjoita Tila-kenttään “Saatavana”
- tietyn viivakoodin
- tietyn lehden numeron: kirjoita Kausijulkaisun numerointi -kenttään
  esim. 2019 : 1
  - _vinkki_, jos haluat näkyville vain esim. numeron 1 eikä muita
    ykkösellä alkavia numeroita, niin laita loppuun vielä yksi
    välilyönti, jolloin muut ykkösellä alkavat numerot eivät enää
    täsmää hakuun.
- tietyllä huomautuksella olevan niteen

### Niteet-välilehti

Vasemman reunan niteet-välilehdellä näkee tarkempia historiatietoja
niteistä. Sinne pääsee myös klikkaamalla yksittäisen niteen viivakoodia
Kokoelmat-taulukosta.  
![](/assets/files/docs/Tiedonhaku/tietue7.png)  
Niteestä näkee mm.

- hankintapaikan ja -hinnan
- kenellä nide on tällä hetkellä lainassa
- kuinka monte kertaa lainaa uusittu
- voi asettaa niteen
  - kadonneeksi (Huomioi, että järjestelmäasetuksista riippuen tästä
    kadonneeksi asettaminen voi viedä niteen korvaushinnan asiakkaan
    maksuihin.)
  - Vahingoittuneeksi (sama kuin Varattavuus niteen muokkauksessa)
  - Pois kierrosta -tilaiseksi (jos sallittu)

![](/assets/files/docs/Tiedonhaku/tietue8.png)  
Historia-tiedoista näkee

- tilaukseen liittyviä tietoja
- niteen lainakerrat
- viimeisin havainto ja lainauspäivä
- viimeksi palauttaneen asiakkaan kirjastokortin numeron
- viimeisimmän ja kaksi sitä edellistä lainaajaa
- näkee ja voi asettaa yleisen huomautuksen tai viesti virkailijalle
  -huomautuksen

### Hankintatiedot

Hankintatiedot-välilehdeltä näkee mm., miltä toimittajilta teosta on
tilattu, milloin ja kuinka monta kappaletta. Jos on tarvittavat
käyttäjäoikeudet, niin välilehden linkeistä pääsee toimittajatietoihin
ja tilauskoreihin.  
![](/assets/files/docs/Tiedonhaku/tietue3.png)

### Teoksen ja niteen lainahistoria

Teoksen kaikkien niteiden lainahistoriaan pääsee vasemman reunan
Lainahistoria-linkistä. Myös yksittäisen niteen lainahistoriaa pystyy
tarkastelemaan Niteet-välilehden kautta.

Lainahistoria-sivulla näkee  
![](/assets/files/docs/Tiedonhaku/tietue9.png)

- teoksen kaikkien niteiden kaikki lainakerrat
- viivakoodin, lainanneen kirjaston, onko uusittu, koska lainattu,
  mikä oli eräpäivä ja koska palautettu

Yksittäisen niteen lainahistoria  
![](/assets/files/docs/Tiedonhaku/tietue11.png)  
Näytöllä on listattuna kaikki kirjastot ja kuinka monta kertaa kyseinen
nide on kirjastosta lainattu sekä viimeisin havaintopäivä.

**Huomioi**: Jos nide palautetaan eri kirjastoon kuin mistä se on
lainattu, tieto ei kirjaudu tälle näytölle. Eli tällä näytöllä näkyy
vain lainaava kirjasto ja viimeisin havaintopäivä kirjautuu lainanneelle
kirjastolle, vaikka palautus on tapahtunut toisessa kirjastossa.
