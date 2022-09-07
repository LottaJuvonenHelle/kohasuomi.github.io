---
title: 'Kohan ohje suomeksi'
permalink: /dokumentaatio/tiedonhaku/
redirect_from:
  - /theme-setup/
toc: true
---

# 8. Tiedonhaku

Kannattaa tutustua myös document\#34 -diaesitykseen, joka on tehty
tiedonhakukoulutuksen materiaaliksi.

## 8.1. Perushaku

Perushakuun siirrytään klikkaamalla _Hae tietokannasta_-painiketta. Haku
suoritetaan kirjoittamalla hakusanat hakukenttään ja painamalla
OK-painiketta.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku1_haun_suorittaminen.png)

Hakutulos näyttää tältä:  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku2_hakutulos.png)

Haku yhdistää oletuksena hakusanat AND-operaattorilla, eli palauttaa
tietueet, joiden tiedoissa esiintyvät kaikki annetut hakusanat.
AND-operaattorin lisäksi haussa voi käyttää myös OR- ja
NOT-operaattoreita. Hakusanat katkaistaan automaattisesti, eli haku
_seitse_ kohdistuu kaikkiin merkkijonon _seitse_ sisältäviin sanoihin,
kuten _seitsemän_, _seitsemäs_ tai _kuusikymmentäseitsemän_.

Sanojen järjestys ei vaikuta hakutulokseen. Haku _tiedonhaku kirjastot_
antaa saman tuloksen kuin _kirjastot tiedonhaku_.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku3_kaanteinen_hakutulos.png)

## 8.2. Tarkka haku

Tarkalla haulla voi määrittää haun perushakua täsmällisemmin. Tarkka
haku löytyy Haku-valikon alta.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku4_tarkka_haku.png)

Tarkassa haussa voit rajata hakutuloksia esimerkiksi aineistolajilla,
julkaisuvuodella, kielellä ja saatavuudella. Hakusanojen yhdistelyssä
voit käyttää Boolen operaattoreita _JA, TAI ja EI_.

Haku suoritetaan kirjoittamalla hakusanat hakukenttiin ja valitsemalla
alasvetovalikoista hakusanojen kohteet. Voit määrittää hakusanojen
rajaavuuden valitsemalla niille alasvetovalikosta operaattorin _ja, tai,
ei_. Hakuehtoja lisätään \[+\]-painikkeella.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku5_tarkan_haun_hakulauseet.png)

Luokkarajaus löytyy Standardinumero-kohdan alta:  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku7_luokkarajaus.png)

Hakukenttien alapuolella on lisää valmiita rajausvaihtoehtoja.

Hakutulosten järjestys valitaan _Järjestys_-kohdasta. Oletuksena
tulokset järjestetään uusimmasta vanhimpaan julkaisuvuoden perusteella.
Muita vaihtoehtoja ovat esimerkiksi tekijä, nimeke ja suosio
(lainausmäärät).  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku6_jarjestys.png)

## 8.3. Hakusanojen etuliitteet

Hakutulosta voi rajata liittämällä hakusanoihin etuliitteitä:

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

- su-geo: maantieteellisen asiasana  
  esim. su-geo: pohjois-karjala

<!-- -->

- bc: viivakoodi  
  esim. 167N02205854

<!-- -->

- ln: kieli  
  esim. ln:est

<!-- -->

- ccode: kokoelmakoodi  
  esim. ccode:lyla (haetaan lyhytlainat)

Lista kaikista etuliitteistä ja tarkemmat ohjeet etuliitteiden
käyttämisestä löytyvät englanninkielisestä manuaalista:
http://manual.koha-community.org/3.16/en/searchguide.html

## 8.4. Uutuuksien ja tilattujen nimekkeiden hakeminen

Jos haluat hakea uutuuksia, valitse haluamasi aineistolaji,
vastaanottovuodeksi kuluva vuosi, _Hakupaikka ja saatavuus_-otsikon alta
_Ei tilaa_ ja järjestykseksi _Vastaanottopäivä: uusimmasta
vanhimpaan_.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku8_uutuudet_osa1.png)  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku9_uutuudet_osa2.png)  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku10_uutuudet_osa3.png)  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku11_uutuudet_osa4.png)

Jos haluat etsiä tilatut nimekkeet, valitse saatavuudeksi _Tilattu_ ja
järjestykseksi _Hankintapäivä: uusimmasta vanhimpaan_.

![](/assets/files/docs/Tiedonhaku/Tiedonhaku12_tilatus_osa2.png)  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku13_tilatut_osa2.png)

## 8.5. Hakutuloksen rajaaminen faseteilla

Hakutulosta voi rajata hakutuloslistan vasemman reunan faseteilla.
Fasettien sisältö riippuu hakutuloksesta.

Jos olet hakenut hakusanalla _valokuvaus_,  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku14_fasetit_lahtotilanne.png)

voit rajata hakutulosta luonnonvalokuvausta käsitteleviin teoksiin
valitsemalla _Asiasanat_-fasetista termin _luonnonvalokuvaus_.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku15_fasetit_rajaus.png)

Tämän jälkeen tuloslista näyttää vain luonnonvalokuvausta käsittelevät
teokset.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku16_fasetit_lopputilanne.png)

Rajauksia voi valita useita kerralla ja poistaa klikkaamalla ruksia
rajauksen perässä.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku17_rajauksen_poistaminen.png)

## 8.6. Hakuhistoria

Tehtyjä hakuja voi tarkastella ja suorittaa uudelleen
hakuhistoria-toiminnolla. Hakuhistoria löytyy oikean yläkulman
alasvetovalikosta.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku18_hakuhistoria_valikko.png)

Hakuhistoriassa haut on jaettu kahteen ryhmään: kuluvan istunnon aikana
tehtyihin hakuihin ja aiemmin suoritettuihin hakuihin.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku19_hakuhistorianakyma.png)

Historian voi poistaa valitsemalla poistettavat haut ja klikkaamalla
_Poista_.

## 8.7. Nidehaku

Nidehaulla voit esimerkiksi:

- Tutkia luokan niteiden määrää karsintaa varten. Huomaa kuitenkin,
  että haku palauttaa myös lainassa olevat niteet.
- Hakea nollalainoja.
- Hakea joukon niteitä ja muokata niiden tietoja eräajona.
- Tarkastaa, ovatko kaikki oman kirjaston lehtiniteet siirretty pois
  lehtiemon alta.
- Tarkastaa, onko lehtien vanhoja numeroita jäänyt roikkumaan
  tietokantaan.

Nidehaku löytyy _Haku_-valikon alta.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku4_tarkka_haku.png)

Nidehaku palauttaa tuloksena listan hakuehdot täyttävistä niteistä. Haun
muotoilu vastaa pitkälti tarkkaa hakua.

Hakusanat voi kohdistaa esimerkiksi niteiden viivakoodeihin, luokkiin,
nimekkeisiin ja tekijöihin. Käytä hauissa aina valintalistan alaosasta
löytyviä räätälöityjä hakukenttiä  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku19_1_hakukentat.png)

Muista kentistä ainoastaan ISBN ja ISSN toimivat luotettavasti.

Hakusanoja voi yhdistää operaattoreilla JA ja TAI. _Uusi kenttä_ lisää
uuden hakukentän. Alla olevassa esimerkissä on lisätty uusi hakukenttä,
asetettu molemmat hakusanat vaadituiksi JA-operaattorilla ja kohdistettu
hakusanat _Nimeke_- ja _Henkilötekijä_-kenttiin. Lisäksi hakusanat on
katkaistu %-merkeillä.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku20_nidehaun_tekstihaku.png)

Nidehaussa hakusanat kannattaa katkaista, koska hakusanoja ei katkaista
automaattisesti. Esimerkiksi tekijä-haku _jansson, tove_ ei tuota yhtään
osumaa, koska MARC-kentästä haettu tekijätieto päättyy pisteeseen tai
pilkkuun. Haku \_%jansson, tove\_ toimii oikein. Katkaisun lisäksi
hakusanat on kirjoitettava aina tarkasti oikein. Esimerkiksi haku*tove
jansson*% ei palauta mitään, koska tekijätieto on muodossa _Jansson,
Tove_. Yksittäisen merkin voi korvata merkillä \_ (alaviiva).

Hakua voi rajata myös sivun yläosan valintalistoilta. Valintalistoilla
voi valita useita arvoja tekemällä valinnat CTRL-näppäin pohjassa.
Ylimmän tyhjän arvon valinta ohittaa ehdon. Jos haluat rajata
hakutuloksesta pois ehtoja, valitse valintalistalta _ei ole_, joka
vastaa NOT-operaattoria.

Valitaan esimerkiksi Kotkan pääkirjaston lasten ja nuorten osaston
kirjat.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku21_nidehaun_rajaukset.png)

Sivun alalaidassa on vielä rajaus luokkavälillä, niteen tilalla ja
lainatiedoilla. Luokkavälillä rajaaminen toimii epäloogisesti. Haku
palauttaa vain luokkarajauksen ylärajaa pienemmät tulokset. Esimerkiksi
haku  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku22_nidehaku_luokkahaku.png)  
palauttaa luokkien 84.2-84.5 teokset. Haku luokasta 91 luokkaan 92
palauttaisi puolestaan vain 91-alkuisten luokkien niteet. Luokalla
rajaaminen onnistuu helpommin käyttämällä räätälöityä kenttää “Luokka
(084$a)”.

_Lainauksien määrä_ –valinnalla voit hakea niteitä lainamäärän
perusteella. Lainauspäivämäärästä voit rajata tuloksia niteen lainojen
ajankohdan perusteella. Alla on haettu kaikki alle 10 kertaa lainatut
niteet, jotka on lainattu 29.10.2018  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku27_nidehaun_lainarajat.png)

Kun kaikki ehdot on valittu, haku suoritetaan klikkaamalla
_Haku_-painiketta.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku26_nidehaku_hakupainike.png)

Esimerkeissä valituilla ehdoilla hakutuloslista näyttää tältä.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku23_nidehaku_tulokset.png)

Niteiden tietoja pääsee muokkaamaan hakutuloslistan oikean reunan
_Muokkaa_-painikkeilla.

Hakua voi rajata lisää sarakkeiden ylälaidassa olevilla
rajauskentillä:  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku24_nidehaku_tulosten_lisafiltterit.png)

### Tulosten vienti CSV- tai -viivakooditiedostoksi

Tulokset voi halutessaan viedä ohjelmasta CSV- tai -viivakooditiedostona
jatkokäyttöä varten ylälaidan painikkeilla.  
![](/assets/files/docs/Tiedonhaku/Tiedonhaku25_nidehaku_tulosten_painikkeet.png)

Hakua pääsee muokkaamaan painamalla _Muokkaa hakua_-painiketta.

## 8.8 Teostiedot

Yksittäisen teoksen tietoihin pääsee monta reittiä, esimerkiksi
asiakkaan lainojen kautta tai tiedonhaun tuloksista. Teoksen
Perustiedot-näytöllä näkee yleisimmin tarvittavat tiedot. Eri otsikot
tulevat näkyville vain, jos teokselle on tallennettu kyseinen tieto.

Vasemmassa reunassa on näkyvissä järjestelmäastuksista ja käyttäjän
oikeuksista riippuen seuraavat välilehdet

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
