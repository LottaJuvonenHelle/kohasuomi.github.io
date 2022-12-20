---
title: 'Kohan ohje suomeksi'
permalink: /dokumentaatio/kuvailu/
redirect_from:
  - /theme-setup/
toc: true
---

# 5. Kuvailu

Kuvailuun meno: Muita toimintoja -&gt; Kuvailu. Jos linkkiä ei
näy, käyttäjätunnuksellasi ei ole kuvailuoikeuksia.

![](/assets/files/docs/Luettelointi/kohaversio2111.png)

## 5.1. Bibliografiset tietueet

Kohassa bibliografinen tietue (nimeketietue) sisältää kuvailutiedot
aineistosta. Näitä tietoja ovat mm. nimeke, tekijä, ISBN ym. Tieto on
tallennettu MARC 21 -formaatin mukaisesti. Kun nimeketiedot on
tallennettu, voidaan tietueelle lisätä niteitä.

### 5.1.1. Tietueen lisääminen

#### Tyhjästä tietueesta

Tietue voidaan lisätä kuvailemalla tai kopioimalla. Uusi nimeke
voidaan kuvailla tyhjälle pohjalle.

Klikkaa _Uusi tietue_ ja valitse sopiva kuvailupohja valikosta.

![](/assets/files/docs/Luettelointi/kohaversio2111k2.png)

#### Z39.50/SRU-haulla

Jos haluat tuoda valmiin kuvailutietueen toisesta
kirjastosta/tietokannasta

Klikkaa _Uusi Z39.50/SRU-haku_ ja tee haku

![](/assets/files/docs/Luettelointi/kohaversio2111k3.png)

**Vinkki** Jos hakutuloksia ei löydy, kokeile hakua vähemmillä
hakusanoilla, sillä kaikki Z39.50/SRU -kohteet eivät löydä tietoja
kaikista kentistä. Sanahakua kannattaa myös kokeilla.

Hakutuloksia voit tarkastella MARC-muodossa tai korttimuodossa tai tuoda
tietueen Kohaan

![](/assets/files/docs/Luettelointi/kohaversio2111k5.png)

![](/assets/files/docs/Luettelointi/kohaversio2111k6.png)

\*Jos et löydä hakemaasi, klikkaa _Tee uusi haku_ näytön vasemmassa
alareunassa.

![](/assets/files/docs/Luettelointi/kohakuvat722.png)

Kun olet avannut tyhjän kuvailupohjan tai tuonut nimeketietueen
Z39.50/SRU -haun kautta, pääset jatkamaan kuvailua.

![](/assets/files/docs/Luettelointi/kohaversio2111k4.png)

### 5.1.2. Osakohteiden lisääminen

Nimekkelle voi lisätä osakohteita eli sisältöä haettavassa muodossa.
Valitse nimeketiedoissa _Uusi -&gt; Uusi osakohde_.

![](/assets/files/docs/Luettelointi/luettelointi8.png)

Musiikin osakohteille on tehty oma tallennuspohja. Valitse se valikosta,
mikäli kuvailet musiikkiaineistoa.

![](/assets/files/docs/Luettelointi/kohakuvatkausi540.jpg)

Kuvaile osakohde. Pakollisia kenttiä ovat 245a (päänimeke), 300a
(laajuus tai kesto), 942c (aineistolaji, valitaan valikosta) sekä
tallennuksen jälkeen muodostuva 008-kenttä (jos ei halua tarkemmin
määritellä osakohteiden ominaisuuksia, riittää kun tallennat toiseen
kertaan tietueen). Automaattisesti täyttyy linkkikenttä 773
tarvittavilla emon tiedoilla, kuten kuvassa alla:

![](/assets/files/docs/Luettelointi/kohakuvatkausi541.png)

Osakohteella ei ole niteitä, joten niteidentallennusnäytölle ei tarvitse
tallentaa mitään, vaan voit palata vasemmalta _Perustiedot_-painikkeesta
teoksen tietoihin.

### 5.1.3. Tietueiden muokkaaminen peruseditorissa

Muokataksesi nimeketietuetta ollessasi Kuvailu-osiossa klikkaa
_Muokkaa tietuetta_ hakutulosnäytöllä

![](/assets/files/docs/Luettelointi/luettelointi11.png)

tai klikkaa Tiedonhaun puolella _Muokkaa_-valikosta _Muokkaa tietuetta_.

![](/assets/files/docs/Luettelointi/kohakuvat580.png)

Tietue avautuu MARC-muokkaukseen.

![](/assets/files/docs/Luettelointi/kuvailu13.png)

Kun muokkaat tietuetta, kentän nimen perässä on kuvakkeet, joista
vasemmalla oleva kopioi kentän ja oikealla puolella oleva tyhjentää
kentän. Kopiointilinkki on näkyvissä vain, jos formaatin mukaan kenttä
on toistettavissa.

![](/assets/files/docs/Luettelointi/luettelointi002.png)

Kiinteämittaisten kenttien oikealla puolella on kuvake, jota
klikkaamalla avautuu valikko, jonka avulla kenttää muokataan.

![](/assets/files/docs/Luettelointi/luettelointi003.png)

![](/assets/files/docs/Luettelointi/luettelointi004.png)

Kentän 008 editorissa pystyy valitsemaan maa- ja kielikoodin valikosta.
Kentät alkavat ehdottamaan koodeja, kun niihin kirjoitetaan joko koodin
tai sen kuvauksen alkua. Esim. _fi_ tai _suo_. Sen jälkeen voi joko
valita koodin listalta tai kirjoittaa jotain muuta.  

![](/assets/files/docs/Luettelointi/luettelointi0041.png) 

![](/assets/files/docs/Luettelointi/luettelointi0042.png)

Huomaa! Joidenkin kiinteämittaisten kenttien arvo muuttuu sen
perusteella, minkä tyyppistä aineistoa olet kuvailemassa ja mikä
tallennuspohja on valittuna.

![](/assets/files/docs/Luettelointi/luettelointi005.png)

#### Finto-liitännäiset

Täti-tietokannassa on käytössä Finto-liitännäiset (pluginit), joilla pystyy hakemaan termejä Fintosta. Toiminnon kuvaus löytyy Teknisestä
dokumentaatiosta [Finto-plugin](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Finto)-sivulta.

#### Tietueen tallentaminen

Kun olet muokannut nimeketietueen, muista tallentaa se
_Tallenna_-painikkeesta, jossa on kolme eri vaihtoehtoa.

![](/assets/files/docs/Luettelointi/luettelointi006.png)

#### Kuvailutietueen korvaaminen uudella Z39.50/SRU-haun kautta

Vaihtoehtoisesti voit etsiä Z39.50/SRU -haun kautta toisesta kirjastosta
täydellisemmän kuvailutietueen, jolla korvaat nykyisen
tietueen.

![](/assets/files/docs/Luettelointi/luettelointi14.png)

Jos käytät tätä korvaamista, pääset Z39.50/SRU -hakusivulle valitsemaan
valikosta kirjaston, jonka tietueella nimeketietue korvataan.

![](/assets/files/docs/Luettelointi/luettelointi15.png)

Oletusarvona on tässä haku TäTistä, Melindasta ja Helmetistä, mutta voit
valita mitä tahansa valikon kirjastoista hakukirjastoksesi.
_Haku_-painike alareunassa aloittaa haun.

Tässä hakutuloksena on kaksi tietuetta. Valitse haluamasi tietueen
kohdalla Täsmäyttäjä-sarakkeesta _Yhdistelysääntö_, niin
hankintavaiheessa tietueeseen tallennetut kansikuva ja kuvaus säilyvät
tietueessa. Klikkaa sen jälkeen _Tuo_ -painiketta oikeassa reunassa.

![](/assets/files/docs/Luettelointi/luettelointi16.png)

Teitpä muutokset tietueeseen kummalla tavalla tahansa, muista klikata
_Tallenna_ -painiketta.

![](/assets/files/docs/Luettelointi/luettelointi17.png)

### 5.1.4. Tietueiden muokkaaminen uudessa editorissa (kehittynyt editori)

Jos halutaan käyttää uutta editoria, se pitää laittaa päälle ylläpidon asetuksessa EnableAdvancedCatalogingEditor. Editori ei ole vielä täysin
luotettava, joten kannattaa suhtautua varauksella sen käyttöön.

HUOM! Ongelma on tietueen tallentamisessa, sillä uusi editori tuo tietueen ISBN:n viivojen kera ja silloin ei toimi tuplakontrolli, koska
olemassa olevat tietueet ovat ilman ISBN:ssa olevia viivoja.

![](/assets/files/docs/Luettelointi/kohakuvatkausi542.png)

Voit avata uuden, tyhjän tietueen tai tuoda toisesta järjestelmästä
haluamasi tietueen haun kautta.

![](/assets/files/docs/Luettelointi/kohakuvatkausi543.png)

Z39.50/SRU-haun kautta voit tuoda haluamasi tietueen omaan
kirjastojärjestelmään.

![](/assets/files/docs/Luettelointi/luettelointi103.png)

Oikeassa reunassa on sarake _Työkalut_, josta voit katsoa MARC-tietueen
sisällön ja tuoda sen omaan kirjastojärjestelmääsi.

Kun haluat lisätä kentän kuvailutietueeseen, syötät kentän numeron ja
indikaattorien paikat ja indikaattorit sekä osakentän tunnuksen ja sen
sisällön.

![](/assets/files/docs/Luettelointi/luettelointi104.png)

#### 5.1.4.1. Pikanäppäimet uudessa editorissa

_Pikanäppäimet_-valikon alta löytyy tarvittavat pikanäppäimet: 

![](/assets/files/docs/Luettelointi/kohakuvatkausi545.png)

### 5.1.4.2. Virtuaalinäppäimistö 

Näppäinyhdistelmällä Shift-Ctrl-K saat esiin virtuaalinäppäimistön ja valikkorivillä olevasta painikkeesta
_Näppäimistöasettelu_ pääset valitsemaan, millä kielellä haluat virtuaalinäppäimistön näkyville.

![](/assets/files/docs/Luettelointi/kohakuvatkausi546.png)

#### 5.1.4.3. Makrot uudessa editorissa

Makro on kätevä tapa lisätä kenttiä tietueeseen uudessa editorissa. Makro otetaan käyttöön
valikkorivin _Makrot_-painikkeesta. Anna ensin uudelle makrolle kuvaava nimi ja sen jälkeen lisää
tarvittavat toiminnot. Voit lisätä useita toimintoja samaan makroon. Makro tallentuu automaattisesti.

![](/assets/files/docs/Luettelointi/kohakuvaedi2.png)

![](/assets/files/docs/Luettelointi/kohakuvaedi3.png)

![](/assets/files/docs/Luettelointi/kohakuvaedi1.png)

Valmiita makroja löydät yhteisön wikistä https://wiki.koha-community.org/wiki/Advanced_editor_macros (englanniksi)

### 5.1.5. Tietueen kopioiminen

Aina et löydä haluamaasi tietuetta Z39.50/SRU -haun kautta. Näissä
tapauksissa voit tehdä kopion samantyyppisestä tietueesta ja muokata
kopiota vastaamaan luetteloitavaa nimekettä. Tehdäksesi kopion klikkaa
_Muokkaa uutena kopiona_.

![](/assets/files/docs/Luettelointi/kohakuvatkausi547.png)

Tämä avaa uuden MARC-tietueen, jossa kentät on täytetty kopioidun
tietueen tiedoilla ja voit muokata tietoja haluamiksesi.  
Muista tyhjentää kentän 001 sisältö, kun aloitat tietueen muokkauksen.
Näin tietueelle tulee uusi tietueen kontrollinumero tähän kenttään, kun
tallennat tietueen etkä saa kysymystä kopiosta:

![](/assets/files/docs/Luettelointi/kohakuvatkausi548.png)

### 5.1.6. Tietueiden yhdistäminen

Useita tietueita (tuplia) voidaan yhdistää yhdeksi tietueeksi
Kuvailun tai tiedonhaun kautta.

#### 5.1.6.1 Tietueiden yhdistäminen kuvailun kautta

Hae yhdistettävät tietueet kuvailuhaun kautta, valitse niistä
haluamasi tietueet ja käytä _Yhdistä valitut_ -toimintoa.

![](/assets/files/docs/Luettelointi/kohakuvat550.png)

Voit tehdä yhdistelyn myös _Listat_-työkalulla. Valitse yhdistettävät
tietueet tiedonhaun kautta ja lisää ne jollekin listallesi, josta voit
ottaa nimekkeet yhdistettäväksi. Yhdistämistoiminnon avulla saat kaikki
niteet ja nimekkeeseen liittyvät varaukset oikeassa järjestyksessä
jäljelle jäävään nimeketietueeseen.

![](/assets/files/docs/Luettelointi/kohakuvat552.png)

Valitse listalta se tietue, mikä jää kohdetietueeksi (mihin muut
tietueet yhdistetään) ja voit valita myös kuvailupohjan.  
Vertaile tietueiden tietoja ja tarvittaessa siirrä muista tietueista
tarvittavia kenttiä kohdetietueeseen. Jos kentän toistaminen on estetty
kuvailuformaatissa, kentän toistaminen antaa virheilmoituksen.

![](/assets/files/docs/Luettelointi/luettelointi553.png)

![](/assets/files/docs/Luettelointi/luettelointi014.png)

Kun kuvailu näyttää valmiilta, klikkaa ruudun alareunassa _Yhdistä_.
Asetuksissa voidaan määritellä, mitkä kentät näkyvät
yhdistämisraportissa. Tässä tapauksessa kentät ovat 001, 245ab, 650.

![](/assets/files/docs/Luettelointi/luettelointi012.png)

Yhdistämisraportti näyttää tältä edellä mainittujen asetusten mukaan:

![](/assets/files/docs/Luettelointi/luettelointi013.png)

#### 5.1.6.2 Tietueiden yhdistäminen tiedonhaun kautta

Hae tiedonhaussa teokset ja vie ne haluamaasi listaan.

<img src="/assets/files/docs/Luettelointi/tietueenyhdistaminen2.png" alt="" style="width:50.0%" />

Avaa lista, valitse kaikki ja sen jälkeen _“Yhdistä valitut”_

<img src="/assets/files/docs/Luettelointi/tietueenyhdistaminen3.png" alt="" style="width:50.0%" />

Voit valita yhdistettävät tietueet myös suoraan tiedohaun tuloksesta.

![](/assets/files/docs/Luettelointi/kohakuvat551.png)

Tämän jälkeen prosessi jatkuu kuten [kuvailun kautta
aloitettaessa](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/3_Luettelointi#3161-Tietueiden-yhdist%C3%A4minen-luetteloinnin-kautta),
kuvasta “Yhdistetään tietueita”.

### 5.1.7. Tietueiden poistaminen

Tietue voidaan poistaa valitsemalla _Muokkaa_-valikosta _Poista tietue_.

![](/assets/files/docs/Luettelointi/kohakuvat581.png)

Tietuetta ei voi poistaa, mikäli tietueeseen liittyy niteitä. Tällöin
_Poista tietue_ -teksti näkyy harmaana.

![](/assets/files/docs/Luettelointi/kohakuvat582.png)

## 5.2. Nidetietueet

Kohassa jokaisella nimeketietueella (bibliografinen tietue) voi olla
yksi tai useampi nide. Jokaisella nitellä on omistajakirjasto ja sijaintikirjasto
sekä hyllypaikka.

### 5.2.1. Niteiden lisääminen

Uuden nimeketietueen lisäämisen jälkeen pääset suoraan tyhjään
nidetietueeseen, johon voit liittää niteen tai useampia niteitä. Niteitä
pääset lisäämään myös klikkaamalla _Muokkaa niteitä_.

![](/assets/files/docs/Luettelointi/luettelointi22.png)

Katso myös ohje “Vanhan niteen tallentaminen uutena niteenä”:
https://tiketti.koha-suomi.fi/documents/46

Tai voit lisätä uuden niteen milloin tahansa nimeketietuenäytöllä
klikkaamalla _Uusi_ ja valitsemalla _Uusi nide_.

![](/assets/files/docs/Luettelointi/luettelointi23.png)

Nimekkeen tallennusnäyttö näyttää tältä:

![](/assets/files/docs/Luettelointi/luettelointi24.png)

Pakolliset kentät on merkitty punaisella, mutta vähintään seuraavat
tiedot olisi hyvä täyttää, jotta niteitä voisi lainata:

- 2 - Luokitus
- a - Omistajakirjasto
- b - Sijaintikirjasto
- o - Kohan koko signum
- p - Viivakoodi
- v - Korvaushinta  
  &gt;\*Tämä summa peritään asiakkaalta, kun nide merkitään
  kadonneeksi asiakkaalta
- y - Kohan aineistolaji

_Huom! Näkyvissä olevat kentät voivat vaihdella kirjastokimpan ja
käytetyn kuvailupohjan mukaan._

Jos kentän lopussa näkyy kolme pistettä, sitä klikkaamalla saa kyseisen
kentän päivitettyä (esimerkissä signumin muodostaminen ja viivakoodin
muodostaminen).

![](/assets/files/docs/Luettelointi/luettelointi015.png)

Nidetietojen alla on kolme nappia, joista valitset haluamasi toiminnon.

![](/assets/files/docs/Luettelointi/luettelointi25.png)

- _Lisää nide_ lisää vain yhden niteen
- _Lisää ja kopioi_ lisää niteen ja täyttää lomakkeen uudelleen
  samoilla arvoilla, joita voit muuttaa
- _Lisää useita kopioita niteestä_ kysyy, montako nidettä haluat
  lisätä ja lisää niin monta nidettä lisäten jokaiselle oman
  viivakoodin (lisäämällä +1 edelliseen)

![](/assets/files/docs/Luettelointi/luettelointi25a.png)

Lisäämäsi tietue tulee taulukkoon.

![](/assets/files/docs/Luettelointi/luettelointi26.png)

Voit suodattaa kokoelmatietoja, kun klikkaat _Suodata_.  
![](/assets/files/docs/Luettelointi/kohakuvat570.png)

![](/assets/files/docs/Luettelointi/kohakuvat571.png)

Riittää, kun aloitat kirjoittamaan suodatinta, kaikki siihen sopivat
tulokset listataan.

### 5.2.2. Niteiden muokkaaminen

Niteitä voi muokata monella tavalla.

#### Klikkaamalla _Muokkaa -&gt; Muokkaa niteitä_ nimeketietonäytöltä

![](/assets/files/docs/Luettelointi/kohakuvat556.png)

Tämä avaa listauksen, missä voit klikata _Toiminnot_-linkkiä sen niteen
rivin alussa, mitä nidettä haluat muokata.

![](/assets/files/docs/Luettelointi/kohakuvat557.png)

#### Klikkaamalla _Muokkaa_ Niteet-välilehdellä halutun niteen kohdalla

![](/assets/files/docs/Luettelointi/luettelointi31.png)

Tämä avaa listauksen, kuten edellä (valitsemasi nide näkyy korostetulla
pohjalla valmiiksi)  

![](/assets/files/docs/Luettelointi/luettelointi32.png)

#### Klikkaamalla _Muokkaa -&gt; Muokkaa niteitä eräajossa_

![](/assets/files/docs/Luettelointi/kohakuvat560.png)

Tämä avaa erämuokkaustyökalun, jossa voit muokata useiden niteiden
tietoja yhtä aikaa.

Jos järjestelmäasetuksissa on määritelty, että niteiden valinta on
mahdollista, voit klikata nidetietojen näytöllä kunkin niteen vasemmalla
puolella valintalaatikosta ne niteet, joita haluat käsitellä. Voit
poistaa niteitä tai muokata niitä.

![](/assets/files/docs/Luettelointi/kohakuvat564.png)

Voit käyttää myös erämuokkaustyökalua muokkaukseen.

### 5.2.2.1. Niteen tilatietojen pikamuokkaus

Toisinaan pitää vaihtaa kadonneiden tai vaurioituneiden niteiden tila.
Tällöin ei tarvitse muokata koko nidetietuetta, vaan voi klikata niteen
viivakoodia lainausnäytöllä tai lainahistoriassa ja päästä niteen
yhteenvetoon. Siellä pääsee merkitsemään niteen kadonneeksi tai
vaurioituneeksi.

![](/assets/files/docs/Luettelointi/kohakuvat563.png)

Täällä voit alasvetovalikosta valita tilan, joka merkitsee niteen
_kadonneeksi_ tai _ilmoittaa palauttaneensa_ -tilaan. Huom! Noudata
kadonnut-tilaa käytettäessä kimpassasi sovittuja käytänteitä.
Kadonnut-tila voi lisätä kimpan asetuksista riippuen niteen
korvaushinnan asiakkaan velkasaldoon.

![](/assets/files/docs/Luettelointi/kohakuvat562.png)

Jos valitset _Ilmoittaa palauttaneensa_ ja klikkaat _Aseta tila_
-nappia, nide poistuu asiakkaan lainoista ja näkyviin tulee päivämäärä,
milloin tila on merkitty.

![](/assets/files/docs/Luettelointi/kohakuvat572.png)

Viimeisin lainaaja jää näkyviin _Historia_-tietoihin.

![](/assets/files/docs/Luettelointi/kohakuvat573.png)

Voit merkitä niteen myös vahingoittuneeksi.

![](/assets/files/docs/Luettelointi/kohakuvat561.png)

### 5.2.2.2. Niteiden erämuokkaus

#### Tiedon lisääminen

Jos haluat muokata jonkun nimekkeen useamman niteen tietoja kerralla,
sen pääsee tekemään valitsemalla nimeketietonäytöllä _Muokkaa -&gt;
Muokkaa niteitä eräajossa_.

![](/assets/files/docs/Luettelointi/kohakuvat560.png)

Siellä voit valita joko kaikki niteet tai valitsemalla vasemmalla
olevasta sarakkeesta vain ne niteet, joihin muutokset kohdistuvat.
Nidelistauksen alapuolella näkyy _Muokkaa niteitä_ -taulukko, johon
tarvittavat muutokset tehdään. Tässä esimerkissä muutetaan kaikille
niteille kokoelmakoodiksi _Lyhytlaina_.

![](/assets/files/docs/Luettelointi/luettelointi46.png)

Rivillä 8 _Kokoelmakoodi_ valitaan tässä tapauksessa Lyhytlaina.  
Sivun alareunassa on painike _Tallenna_ eli muista tallentaa muutokset.

![](/assets/files/docs/Luettelointi/luettelointi47.png)

Muutokset näkyvät tallennuksen jälkeen uutena sarakkeena
_Kokoelmakoodi_. Tämä sarake on näkyvissä vain, jos siellä on jotain
kokoelmatietoa, tyhjää saraketta ei näytetä.

![](/assets/files/docs/Luettelointi/luettelointi48.png)

#### Tiedon poistaminen

Esimerkissä olevan _Lyhytlaina_-kokoelmakoodin poistaminen tapahtuu
vastaavalla tavalla.  
Haetaan nimeke, jonka niteiltä kokoelmakoodi poistetaan, valitaan
_Muokkaa -&gt; Muokkaa niteitä eräajossa_.

![](/assets/files/docs/Luettelointi/luettelointi49.png)

Kokoelmakoodi-kentän valintaruutuun tehdään valinta (laitetaan täppä) ja
tallennetaan, niin _Lyhytlaina_-kokoelmakoodi poistuu valituilta
niteiltä.

### 5.2.3. Nidetiedot

Jokaisen nimeketietueen vasemmalla puolella on valikko, josta pääset
tarkastelemaan niteitä.

![](/assets/files/docs/Luettelointi/luettelointi50.png)

Jos nide on hankittu Kohan hankintamoduulin kautta, näkyy _Historiassa_
myös hankintatiedot. Jos tilaus- tai saapumispäivä näkyy linkkinä, siitä
pääsee niteen hankintatietoihin.

### 5.2.4. Niteen siirtäminen

Nide voidaan siirtää nimeketietueelta toiselle käyttämällä _Liitä nide_
-toimintoa.

![](/assets/files/docs/Luettelointi/kohakuvat574.png)

Liittämiseen tarvitaan siirrettävän niteen viivakoodi, joka luetaan sen
nimekkeen tietoihin, mihin nide halutaan siirtää.

![](/assets/files/docs/Luettelointi/luettelointi52.png)

Yksinkertaisesti lisäät siirrettävän niteen viivakoodin ja klikkaat OK.

Jos haluat siirtää useita niteitä yhteen tietueeseen, voit käyttää
_yhdistä tietueet_ -toimintoa.

### 5.2.5. Niteiden poisto

Niteiden poisto voidaan tehdä eri tavoilla. Jos haluat poistaa vain
yhden niteen, on yksinkertaisinta avata nimeketietueen tarkat tiedot ja
sieltä _Muokkaa -&gt; Muokkaa niteitä_.

![](/assets/files/docs/Luettelointi/luettelointi53.png)

Jokaisen niteen vasemmalla puolella on _Poista_-linkki.

![](/assets/files/docs/Luettelointi/luettelointi54.png)

Kun klikkaat _Poista_, saat vielä varmistuskysymyksen:

![](/assets/files/docs/Luettelointi/luettelointi55.png)

Nidettä ei voi poistaa, jos se on lainassa. Jos haluat poistaa kaikki
niteet nimekkeeltä, voit käyttää _Muokkaa -&gt; Poista kaikki niteet_.

![](/assets/files/docs/Luettelointi/luettelointi56.png)

Jos järjestelmäasetuksissa on määritelty mahdollistamaan niteiden
valinta, voit klikata nidetietojen näytöllä kunkin niteen vasemmalla
puolella valintalaatikosta ne niteet, joita haluat käsitellä. Voit
poistaa niteitä tai muokata niitä.

![](/assets/files/docs/Luettelointi/luettelointi57.png)

Voit käyttää myös _Muokkaa -&gt; Poista niteitä eräajossa_, jos poistat
enemmän niteitä kerralla.

![](/assets/files/docs/Luettelointi/luettelointi58.png)

Täällä voit valita niteet, jotka poistetaan.

![](/assets/files/docs/Luettelointi/luettelointi59.png)

### 5.2.6. Niteen lainahistoria

Jokaisella nimekkeellä säilytetään lainahistoria (asiakastietojen kanssa
tai ilman niitä, riippuu järjestelmän asetuksista), mutta jokaisella
niteellä on myös oma lainahistoriansa. Tämä löytyy
_Niteet_-välilehdeltä.

![](/assets/files/docs/Luettelointi/luettelointi60.png)

Historia-otsikon alla näkyy linkki _Näytä niteen lainahistoria_, jota
klikkaamalla näkyy tämän niteen lainaushistoria.

![](/assets/files/docs/Luettelointi/luettelointi016.png)

## 5.3. Auktoriteetit

ohje tehdään myöhemmin

## 5.4. Kuvailuohjeet

[Yhteisön kuvailuohjeet](https://koha-community.org/manual/21.11/en/html/cataloging.html)

### 5.4.1. Niteiden tarrat ja niiden tulostaminen

Tallennusohje löytyy täältä [tarratulostus](https://tiketti.koha-suomi.fi/attachments/5489/Tarratulostus%2021.11%20versio.docx)

### 5.4.2. Niteiden tallennusohjeet

<table>
<thead>
<tr class="header">
<th>Kenttä</th>
<th>Otsikko</th>
<th>Kuvaus</th>
<th>Huomautus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>952$0</td>
<td>Pois kierrosta -tila</td>
<td>Oletusarvot:<br />
0 = (tyhjä)<br />
1 = Pois kierrosta</td>
<td>Koodattu arvo, taulukko Auktorisoidut arvot -&gt; WITHDRAWN</td>
</tr>
<tr class="even">
<td>952$1</td>
<td>Kadonnut-tila</td>
<td>Oletusarvot:<br />
0 = (tyhjä)<br />
1 = Kadonnut<br />
2 = Myöhässä (kadonnut)<br />
3 = Kadonnut ja korvattu<br />
4 = Puuttuu</td>
<td>Koodattu arvo, taulukko Auktorisoidut arvot -&gt; LOST<br />
Asetuksissa voi muokata hidelostitems-määrityksellä, näkyykö kadonnut aineisto verkkokirjastossa</td>
</tr>
<tr class="odd">
<td>952$2</td>
<td>Luokitus</td>
<td>Luokitusjärjestelmä, jonka mukaan luokkanumerot järjestyvät</td>
<td>Asetuksissa luokituslähteet, jonne on tallennettu ykl = Yleisten kirjastojen luokitus oletusarvoksi (Luokitus - &gt; DefaultClassificationSource)</td>
</tr>
<tr class="even">
<td>952$3</td>
<td>Liitteiden määrä</td>
<td>Moniviestimien tms. osien määrä tai liitteiden määrä ja kuvaus</td>
<td>Näkyy lainaus- ja palautusnäytöllä, ilmoittaa niteeseen kuuluvan aineiston määrän (esim. montako liitettä). Luettelointitieto kentässä 952$h ja $t näkyy normaalinäytössä.</td>
</tr>
<tr class="odd">
<td>952$4</td>
<td>Vaurioitunut-tila</td>
<td>Oletusarvot:<br />
0 = (tyhjä)<br />
1 = Vaurioitunut</td>
<td>Koodattu arvo, taulukko Auktorisoidut arvot - &gt; DAMAGED</td>
</tr>
<tr class="even">
<td>952$5</td>
<td>Käyttörajoitukset</td>
<td>Oletusarvot:<br />
0 = (tyhjä)<br />
1 = Rajoitettu pääsy</td>
<td>Koodattu arvo, taulukko Auktorisoidut arvot - &gt; RESTRICTED.<br />
Tällä arvolla ei ole vaikutusta lainauksessa.</td>
</tr>
<tr class="odd">
<td>952$7</td>
<td>Ei lainattavissa</td>
<td>Oletusarvot:<br />
0 = (tyhjä)<br />
–1 = Tilattu<br />
1 = Ei lainata<br />
2 = Henkilökunnan käsikirjasto</td>
<td>Koodattu arvo, taulukko Auktorisoidut arvot -&gt; NOT_LOAN<br />
Negatiiviset arvot sallivat varaamisen.</td>
</tr>
<tr class="even">
<td>952$8</td>
<td>Kokoelmakoodi</td>
<td>Esim. Pikalaina, Celia-kokoelma</td>
<td>Koodattu arvo, taulukko Auktorisoidut arvot -&gt; CCODE</td>
</tr>
<tr class="odd">
<td>952$R</td>
<td>Saapumispäivämäärä</td>
<td>Niteen vastaanottopäivämäärä</td>
<td>Pakollinen tieto, päivittyy automaattisesti hankinta-osiossa niteen vastaanotossa. Tähän tietoon perustuu raportointityökalun hankintavuosi-tieto.</td>
</tr>
<tr class="even">
<td>952$S</td>
<td>Hyllytarkenne</td>
<td>Esim. koulukirjaston nimi, Isotekstiset. Täsmentää hyllypaikka-tietoa</td>
<td>Koodattu arvo, Auktorisoidut arvot -&gt; SUBLOC</td>
</tr>
<tr class="odd">
<td>952$9</td>
<td>Niteen numero</td>
<td>Järjestelmän tuottama niteen numero</td>
<td>Ei näy nidetietueessa</td>
</tr>
<tr class="even">
<td>952$a</td>
<td>Omistajakirjasto</td>
<td>Kirjaston nimi</td>
<td>Vaaditaan. Nimi on määriteltävä perusasetuksissa Kirjastot ja ryhmät.</td>
</tr>
<tr class="odd">
<td>952$b</td>
<td>Sijaintikirjasto</td>
<td>Kirjaston nimi</td>
<td>Vaaditaan. Nimi on määriteltävä perusasetuksissa Kirjastot ja ryhmät.</td>
</tr>
<tr class="even">
<td>952$c</td>
<td>Hyllypaikka</td>
<td>Esim. Aikuiset, Lapset, Kotiseutukokoelma</td>
<td>Koodattu arvo, taulukko Auktorisoidut arvot -&gt; LOC.</td>
</tr>
<tr class="odd">
<td>952$d</td>
<td>Hankintapvm</td>
<td>VVVV-KK-PP</td>
<td>Päiväyksen tulee olla järjestelmän ymmärtämässä muodossa: VVVV-KK-PP</td>
</tr>
<tr class="even">
<td>952$e</td>
<td>Hankintapaikka</td>
<td>Koodattu arvo tai toimittajan nimi</td>
<td>Täytetään automaattisesti hankintamoduulissa Kohaan tallennetun toimittajan tunnuksella, kun nide on saapunut</td>
</tr>
<tr class="odd">
<td>952$g</td>
<td>Hankintahinta</td>
<td>Desimaalinumero, ei valuuttamerkkejä (esim. 10.00)</td>
<td>Täytetään automaattisesti hankinnan tiedoilla, kun nide on saapunut</td>
</tr>
<tr class="even">
<td>952$h</td>
<td>Sarjanumero</td>
<td>Esim. 2016 : 3</td>
<td>Täytetään automaattisesti kausijulkaisuissa, jos niteet on merkitty saapuneeksi saapumisvalvonnan kautta</td>
</tr>
<tr class="even">
<td>952$o</td>
<td>Kohan koko signum</td>
<td>Esim. AIK 84.2 JAA</td>
<td>Voidaan täyttää automaattisesti, perustuu järjestelmäasetukseen <em>itemcallnumber</em></td>
</tr>
<tr class="odd">
<td>952$p</td>
<td>Viivakoodi</td>
<td>Max. 20 merkkiä</td>
<td>Pakollinen tieto lainauksen kannalta, mutta ei muuten.</td>
</tr>
<tr class="even">
<td>952$t</td>
<td>Nidenumero</td>
<td>Max. 32 merkkiä</td>
<td>Ei käytössä</td>
</tr>
<tr class="odd">
<td>952$u</td>
<td>URI</td>
<td>Niteen oma URL</td>
<td>Koko URL, joka alkaa http: Täytetään vain, jos niteellä on oma URL, mutta ei ole tarpeellinen, jos nimekkeellä on 856$u-kenttään osoite tallennettuna</td>
</tr>
<tr class="even">
<td>952$v</td>
<td>Korvaushinta</td>
<td>Desimaalinumero, ei valuuttamerkkejä (esim. 10.00)</td>
<td>Täytetään automaattisesti hankintamoduulista, kun nide on saapunut</td>
</tr>
<tr class="odd">
<td>952$w</td>
<td>Hinta voimassa alkaen</td>
<td>VVVV-KK-PP</td>
<td>Päiväyksen tulee olla järjestelmän ymmärtämässä muodossa: VVVV-KK-PP. Täytetään automaattisesti hankintamoduulista, kun nide on saapunut</td>
</tr>
<tr class="even">
<td>952$x</td>
<td>Huomautus virkailijoille</td>
<td></td>
<td>Tämä huomautus ei näy verkkokirjastossa. Tällä hetkellä tämä huomautus näkyy vain niteiden muokkausnäytöllä ja Niteet-välilehdellä virkailijatyökalussa.</td>
</tr>
<tr class="odd">
<td>952$y</td>
<td>Kohan aineistolaji</td>
<td>Esim. Kirja, CD-levy</td>
<td>Pakollinen tieto. Koodattu arvo, määritellään perusasetuksisssa <em>Aineistolajit</em>.</td>
</tr>
<tr class="even">
<td>952$z</td>
<td>Yleinen huomautus</td>
<td>Esim. Liitteenä 3 CD-levyä</td>
<td>Näkyy verkkokirjastossa ja virkailijaliittymässä</td>
</tr>
</tbody>
</table>
