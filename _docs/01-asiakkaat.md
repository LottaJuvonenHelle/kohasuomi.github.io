---
title: 'Kohan ohje suomeksi'
permalink: /dokumentaatio/asiakkaat/
redirect_from:
  - /theme-setup/
toc: true
---

# 1. Asiakkaat

## 1.1. Lisää uusi asiakas

Asiakkaat lisätään menemällä Asiakkaat-välilehdelle.

![](/assets/files/docs/Asiakkaat/Lisaauusiasiakas1.png)

Sivulla on alasvetovalikkovaihtoehdot: +Uusi asiakas ja +Asiakkaan pikalisäys. Huom. Kaikissa kimpoissa ei ole Asiakkaan pikalisäys-vaihtoehtoa käytössä, joten valitse kimppasi ohjeistama asiakkaan lisäystapa.

![](/assets/files/docs/Asiakkaat/Lisaauusiasiakas2.png)

Klikkaa Uusi asiakas, saat alasvetovalikon, josta valitset asiakkaan
tyypin.

![](/assets/files/docs/Asiakkaat/Lisaauusiasiakas3.png)

### 1.1.1. Henkilötunnus ja sotu-siilo

Kohaan on tehty Suomessa ominaisuus, sotu-siilo, jonne tallennetaan
tietoturvallisesti asiakkaiden henkilötunnukset. Sotu-siilo on yhteinen kaikille kimpoille.

Oheisissa ruutukaappauksissa käytetty sotu on tehty
henkilötunnusgeneraattorin avulla, se ei ole kenenkään henkilön oikea
tunnus, mutta täyttää tunnuksen ominaisuudet tarkistusmerkkiä myöten.
Sotuavaimella muodossa “sotuxxxx” voi hakea asiakkaan tiedot esille,
mutta henkilötunnus ei näy.

Syötä Lisää hetu-kohtaan asiakkaan henkilötunnus.

![](/assets/files/docs/Asiakkaat/Lisaahetu.png)

Jos henkilötunnusta ei ole ennestään sotu-siilossa, siitä tulee ilmoitus
"Hetu tallennettu!".

![](/assets/files/docs/Asiakkaat/Hetutallennettu1.png)

Sotu-avain siirtyy automaattisesti asiakastietoihin Muut määritteet ja
tunnukset -kohtaan kenttään Sosiaaliturvatunnus/Henkilötunnus/Sotu-avain
(kentän nimi voi vaihdella kimpan mukaan).

![](/assets/files/docs/Asiakkaat/Sotuavain.png)

Jos henkilötunnus on virheellinen, tulee siitä ilmoitus: “Tarkista hetu!”.

![](/assets/files/docs/Asiakkaat/Tarkistahetu.png)

#### 1.1.1.1. Sotu on jo olemassa

Jos syötetty henkilötunnus on jo sotu-siilossa, järjestelmä tutkii automaattisesti asiakasrekisteristä löytyykö 
henkilötunnuksen sotuavaimella asiakastietoja. 

Jos tietoja ei löydy asiakasrekisteristä, niin käyttäjälle tulee ilmoitus “Hetu asetettu!". Jatka tuolloin uuden asiakkaan
tallentamista käyttäen sotu-siilon antamaa sotu-avainta.

![](/assets/files/docs/Asiakkaat/Hetuasetettu.png)

Jos asiakastiedot löytyvät, niin käyttäjälle tulee ilmoitus "Asiakas on jo olemassa! Paina OK siirtyäksesi tietoihin." 
Klikkaamalla OK käyttäjä siirtyy automaattisesti asiakkaan tietoihin, joita tarvittaessa muokataan.

![](/assets/files/docs/Asiakkaat/Sotu3.png)


#### 1.1.1.2. Sotu-siilon käyttöliittymä

Sotu-siiloon on olemassa myös toinen käyttöliittymä, jonka kautta
esimerkiksi laskuttajat voivat tarkistaa asiakkaan henkilötunnuksen
sotu-avaimella. Heillä on erilliset tunnukset tarkistusta varten.

---

### 1.1.2. Nimi, syntymäaika ja varaustunnus

Syötä asiakkaan koko nimi ja syntymäaika. Varaustunniste täyttyy automaattisesti. Huomaathan,
että kimppasi Kohassa ei välttämättä näy kaikki kuvissa näkyvät kentät.

![](/assets/files/docs/Asiakkaat/Varaustunnus1.png)

Asiakaslajeihin on määritetty ikärajoituksia. Ohjelma tarkistaa
syntymäajan mukaan, voiko asiakas kuulua asiakaslajiin, johon
häntä ollaan tallentamassa. Voit saada tällaisen virheilmoituksen:  
![](/assets/files/docs/Asiakkaat/ikaraja.png)

### 1.1.3. Takaaja

Jos kyseessä on lapsiasiakas, hänelle pitää tallentaa takaaja. Klikkaa
“Lisää takaaja” -nappia, niin pääset hakemaan rekisteristä lapselle
takaajan.

![](/assets/files/docs/Asiakkaat/Lisaatakaaja.png)

Takaajaa voi hakea joko nimellä tai kirjastokortin numerolla. Valitse
alasvetovalikoista sopivat vaihtoehdot.

![](/assets/files/docs/Asiakkaat/Valitsetakaaja.png)

Saat listan hakuun sopivista asiakkaista. Klikkaa oikealta “Valitse”-painiketta
oikean henkilön kohdalla. 

Valitse alasvetovalikosta takaajan suhde asiakkaaseen Huom. alasvetovalikon vaihtoehdot voivat vaihdella kimpoissa.

![](/assets/files/docs/Asiakkaat/Asiakastakaaja.png)

Tallennuksen jälkeen huoltajan tiedoista näkyy nimi, varaustunniste sekä kirjastokortin numero. Voit 
tallentaa lapsiasiakkaalle useamman kuin yhden huoltajan tiedot.

![](/assets/files/docs/Asiakkaat/Takaajat.png)

Huom! Jos takaajaa ei löydy asiakasrekisteristä, avaa uusi välilehti ja
tallenna takaajan tiedot rekisteriin. Palaa sen jälkeen lapsiasiakkaan
tietoihin toisella välilehdelle ja tee takaajahaku uudelleen.

#### 1.1.3.1. Ei-asiakas takaaja-tiedon lisääminen

Kimppakohtainen.
![](/assets/files/docs/Asiakkaat/Eiasiakastakaaja.png)

### 1.1.4. Yhteystiedot

Osoite-osiossa “Kunta” tarkoittaa käytännössä postitoimipaikkaa, ei
pelkästään kotikuntaa. Englanninkielistä sanaa City ei voi kääntää
postitoimipaikaksi tässä kohti, koska sama sana on kunta-merkityksessä
muussa yhteydessä. Voit valita postinumeron ja postitoimipaikan alasvetovalikosta tai kirjoittaa ne itse.

![](/assets/files/docs/Asiakkaat/Osoitetiedot.png)

Syötä Yhteystiedot-osiossa asiakkaan puhelinnumero (lankapuhelinnumero Ensisijainen puhelin/lankapuhelinkenttään ja matkapuhelin
Muu puhelin/matkapuhelinkenttään) ja sähköpostiosoite. Matkapuhelin-kenttään lisätty numero kopioituu automaattisesti asiakkaan viestiasetuksiin, jos
asiakas haluaa varausilmoitukset tekstiviestinä. Sähköpostiosoite on se osoite, johon asiakasviestit lähtevät.

Asiakas voi halutessaan valita ensisijaisen yhteydenottotavan kirjaston henkilökunnan yhteydenottoja varten. Kaikissa kimpoissa tätä valintaa 
ei välttämättä ole otettu käyttöön. 

![](/assets/files/docs/Asiakkaat/Yhteystiedot1.png)

Huom! Puhelinnumero-kenttiin ei saa kirjoittaa muuta kuin
puhelinnumeron. Ei esim. perään äiti, isä yms. eikä väliviivaa.
Kansainvälisen suunnan (esim. +358) numeron yhteyteen voi lisätä.

Asiakkaalle voidaan tallentaa myös vaihtoehtoinen osoite. Huom! Tässä on
kimppakohtaisia eroja.

![](/assets/files/docs/Asiakkaat/Vaihtoehtoinenosoite.png)

### 1.1.5. Kirjastotiedot

#### 1.1.5.1. Kirjastonhallinta-osio

Kirjastonhallinta-osio sisältää kirjaston käyttöön liittyviä tietoja.

![](/assets/files/docs/Asiakkaat/kirjastohallinta.png)

\- Lue asiakkaan kirjastokortin numero ylimmäisenä olevaan
“Kirjastokortin numero” -kenttään.

\- Kirjasto-kenttään valitaan asiakkaan kotikirjasto, jota järjestelmä
ehdottaa mm. varausta tehtäessä noutokirjastoksi.

\- Tyyppi-kohdassa voi vaihtaa asiakastyypin. Huom! Jos tässä kohtaa
vaihtaa asiakastyypin, muutos ei tuo esille mm. takaajatieto-kenttää tai
poista sitä näkyvistä. Tätä ei kannata muuttaa. Aloita mielummin alusta,
jos valitsit alussa väärän asiakastyypin.

![](/assets/files/docs/Asiakkaat/Lapsellapitaaollatakaaja.png)

\- Valitse asiakasviestien kieli kohdassa “Ilmoitusten kieli”.

#### 1.1.5.2 Kirjaston asetukset-osio
![](/assets/files/docs/Asiakkaat/Huomautuslaatikko1.png)

\- Tullut asiakkaaksi -päivämäärä tulee automaattisesti kuluvan päivän
mukaiseksi.

\- Vanhentuu -kohtaan ei tarvitse merkitä mitään. Tieto tulee
automaattisesti asiakaslajille tehtyjen määritysten mukaan.

\- Huomautus (näkyy verkkokirjastossa) -kohtaan voi merkitä
huomautuksen, jonka asiakas näkee verkkokirjastosta. Huomautus
näkyy OPACissa ja Finnassa.

Finnassa se näkyy Omat tiedot-välilehdellä "Kirjastokortin asetukset"-laatikossa.

![](/assets/files/docs/Asiakkaat/Huomautuslaatikko2.png)

\- Huomautus (näkyy virkailijatyökalussa) -laatikossa oleva huomautus
näkyy Kohassa virkailijoille tiedot- ja lainausnäytöllä.

![](/assets/files/docs/Asiakkaat/Huomautuslaatikko.png)

#### 1.1.5.3. Kirjautumistunnus-osio
Kirjautusmistunnus-osioon voi lukea esim. kirjastokortin numeron tai
erillisen käyttäjätunnuksen, jolla asiakas voi kirjautua
verkkokirjastoon. Huom! Kimppakohtaisia eroja.

![](/assets/files/docs/Asiakkaat/kirjautumistunnus.png)

#### 1.1.5.4. Muut määritteet ja tunnukset

Tähän tulee mm. sotu-avain ja OUTI-kimpalla tässä asetetaan
omatoimikirjaston käyttöesto. Myös muita kimppakohtaisia määritteitä voi
olla käytössä.

![](/assets/files/docs/Asiakkaat/Muutmaareetjatunnukset1.png)

### 1.1.6. Asiakkaan viestiasetukset

Lopuksi vielä tallennetaan asiakkaan viestiasetukset. Käytettävissä
olevat viestivaihtoehdot vaihtelevat kimpoittain.

![](/assets/files/docs/Asiakkaat/Asiakkaanviestirajoitukset1.png)

\- Ilmoitus eräpäivänä: Ilmoitus lainojen erääntymisestä eräpäivänä.

\- Ennakkoilmoitus: Etukäteisilmoitus lähestyvästä eräpäivästä (Asiakas
voi valita, montako päivää etukäteen ilmoitus tulee). HUOM! Jos tähän
valitsee 0, ei viestiä lähetetä, vaikka rasti olisi paikallaan.

\- Saapumisilmoitus: Ilmoitus asiakkaalle noudettavissa olevasta
varauksesta.

\- Palautus: Lista asiakkaan juuri palauttamasta aineistosta.

\- Lainaus: Lista asiakkaan juuri lainaamista niteistä. Tämä on
  sähköinen versio lainauskuitista.

\- Lisää puhelinnumero “Tekstiviesti numeroon” -kenttään, jotta
tekstiviestit lähetetään. Huom. Matkapuhelin-kenttään lisätty numero 
kopioituu automaattisesti asiakkaan viestiasetuksiin, jos asiakas 
haluaa varausilmoitukset tekstiviestinä. Testiviesti-vaihtoehtoon ei 
voi laittaa rastia, jos tässä kentässä ei ole puhelinnumeroa.

- SMS-palveluntuottaja-kohtaan ei tarvitse valita mitään. Ominaisuus ei
  ole käytössä.

Tärkeää

\- Nämä asetukset kumoavat asiakaslajeihin tehdyt oletusvalinnat.

\- Asiakas voi itse muuttaa näitä asetuksia verkkokirjastossa.

- Valitse koosteilmoitus ennakkoilmoitukseen ja eräpäiväilmoitukseen,
  niin asiakas saa yhdessä viestissä kaikkien erääntyvien niteiden tiedot
  eikä jokaisesta lainasta erillistä viestiä!

Lopuksi tallenna tiedot.

Jos järjestelmä epäilee, että olet tekemässä tupla-asiakkaan, saat siitä
huomautuksen. Jos olet varma, että kyseessä ei ole kopio, valitse “Ei
kopio. Tallenna uutena tietueena”.

![](/assets/files/docs/Asiakkaat/Kopioiasiakastiedot1.png)

---

## 1.2. Ei-tilastoitavat-lainat

Tämä asiakastyyppi on luotu sellaisille lainoille, joita henkilökunta
tekee työtarkoitusta varten. Huom! Voi olla kimppakohtaisia eroja
asiakastyypin nimessä sekä käytännöissä. Tämän asiakastyypin lainoja ei
oteta mukaan tilastoihin.

![](/assets/files/docs/Asiakkaat/eitilastoituvat.png)

## 1.3. Asiakkaan tietojen muokkaaminen

Asiakkaan tietoja voidaan muokata eri painikkeiden kautta. Huom. Tässä voi olla kimppakohtaisia eroja.

Muokataksesi jotain tiettyä osiota asiakastiedoissa (esim.
Kirjastotiedot) klikkaa sen osion alla olevaa sinistä Muokkaa-linkkiä.

![](/assets/files/docs/Asiakkaat/muokkaanappi2.png)

Asiakastietojen yläreunassa olevilla painikkeilla pääset vaihtamaan salasanan, kopioimaan asiakkaan tiedot, tulostamaan asiakkaan haluamia kuitteja asiakaspalvelutilanteessa mm. Tänään lainatut-kuitin, tekemään asiakkaalle tiedonhaussa varauksen siten, että asiakastieto säilyy muistissa, lisäämään asiakastietoihin viestin sekä Muita toimintoja -napin takaa löytyy toiminnot, joilla pääsee uusimaan tilin, poistamaan tunnuksen sekä päivittämään lapsiasiakkaan aikuiseksi. 

Koko asiakastietueen muokkaukseen pääset Muokkaa-painiketta klikkaamalla.

![](/assets/files/docs/Asiakkaat/muokkaanappi.png)

### 1.4.1. Salasanan vaihtaminen

Asiakkaan salasanan pääsee muokkaamaan Vaihda salasana-painikkeen kautta. 

Asiakkaan salasanaa ei voi nähdä. Jos asiakas unohtaa salasanansa, hänelle pitää tallentaa uusi salasana.

![](/assets/files/docs/Asiakkaat/salasana.png)

\- Koha ei voi näyttää entistä salasanaa. Jätä salasanakenttä tyhjäksi,
jos et halua vaihtaa salasanaa.

\- Jos haluat automaattisesti luodun salasanan, klikkaa “Valitse tästä
luodaksesi satunnaisesti luodun salasanaehdotuksen”. Salasanat näytetään
tekstinä.

- Muista tallentaa.

### 1.4.2. Asiakkaan tietojen kopioiminen

Joissakin tilanteissa on tarpeen käyttää asiakastietojen kopioimista, jos
esim. saman perheen jäsenille tehdään useita kortteja. Kohassa on
toiminto, jolla voidaan kopioida henkilötiedot, jotka toistuvat eri
tietueissa.

Avaa sen asiakkaan tiedot, jonka haluat kopioida ja klikkaa
Kopioi-nappia tietueen yläreunassa.

Sukunimi, lapsiasiakkaalla takaajatiedot, osoite, sähköpostiosoite, kirjasto sekä asiakastyyppi 
kopioituvat uuteen lomakkeeseen. Lisää puuttuvat tiedot ja klikkaa Tallenna.

Tallennuksen jälkeen pääset uuden asiakkaan tietoihin.

### 1.4.2. Muita toimintoja -alasvetovalikko

#### 1.4.2.1. Asiakaan käyttöoikeuden jatkaminen

Asiakastilin vanhennuttua asiakas ei pääse käyttämään korttiaan. Tili uusitaan lainausnäytöllä vanhentumispäivämäärän perässä olevasta linkistä
“Uusinta”, asiakkaan tiedot sivulla Kirjastotiedot kohdasta tai Muita toimintoja- alasvetovalikosta “Asiakkaan käyttöoikeuden jatkaminen”. 

![](/assets/files/docs/Asiakkaat/tilinvanh.png)

![](/assets/files/docs/Asiakkaat/Uusitili.png)

![](/assets/files/docs/Asiakkaat/Uusitili2.png)

Asiakkaalle tallentuu tilin vanhentumispäivämäärä asiakastyypille määritellyn voimassaoloajan mukaan.

### 1.4.2.2. Päivitä lapsi aikuiseksi

Lapsiasiakkaasta ei tule automaattisesti aikuista ellei Kohassa ole
siihen liittyvä ajo käynnissä. Lapsen voi muuttaa aikuiseksi Asiakkaan
tiedot -näytöllä valitsemalla Muita toimintoja -valikosta “Päivitä lapsi
aikuiseksi”.

![](/assets/files/docs/Asiakkaat/lapsiaikuiseksi.png)

### 1.4.3. Lapsiasiakkaan takaajan vaihtaminen

Takaajatiedot pääsee muokkaamaan Muokkaa -painikkeen takaa. Kohdassa "Asiakastakaaja" voit sekä poistaa että lisätä takaajan. 

Poistaminen tapahtuu ruksaamalla poistettava takaaja ja sen jälkeen klikkaa "Tallenna". 

![](/assets/files/docs/Asiakkaat/Poistatakaaja.png)

Lisääminen tapahtuu Lisää takaaja-painikkeella. Hae lisättävän huoltajan tiedot avautuvassa ikkunassa.

![](/assets/files/docs/Asiakkaat/Valitsetakaaja.png)

Valitse hakutuloksesta huoltaja ja klikkaa Valitse.

Valitse takaajan suhde ja tallenna.

### 1.4.4. Asiakkaan kuva

Asiakkaan kuva voidaan lisätä valitsemalla kuva koneeltasi Lataa
asiakaskuva -osiossa.

![](/assets/files/docs/Asiakkaat/asiakaskuva.png)

\- Tämä osio ei ole näkyvissä, jos järjestelmäasetuksissa on estetty
kuvien tallentaminen

\- Työkaluissa olevalla toiminnolla Asiakaskuvien lataus voi tuoda
palvelimelle eräajona kuvia

### 1.4.4. Rajoitukset

#### 1.1.5.4. Käyttäjätilin huomautukset

![](/assets/files/docs/Asiakkaat/Kayttajatilinhuomautukset.png)

Jos asiakas ilmoittaa kadottaneensa kirjastokorttinsa, voit merkitä sen
kadonneeksi klikkaamalla "Kyllä" Kortti kadonnut -kohdassa. Lainausnäytöllä tulee ilmoitus Kadonnut: Asiakkaan kortti on kadonnut.

![](/assets/files/docs/Asiakkaat/kadonnutkortti.png)

Jos haluat lainauksen virkailijan tarkistavan asiakkaan osoitteen ennen
lainaamista, laita valinta “Kyllä” päälle Tarkista osoite -kohdassa. Lainausnäytöllä tulee ilmoitus Osoite: Tarkista osoite.

![](/assets/files/docs/Asiakkaat/vaaraosoite.png)

Molemmat vaihtoehdot ovat eräänlaisia rajoituksia eli ne estävät asiakasta käyttämästä asiakastunnustaan.

#### 1.1.5.5. Asiakkaan rajoitukset

Asiakkaalle lisätään vapaamuotoinen rajoite joko lainausnäytöllä välilehdellä "Rajoitukset" tai asiakkaan tiedot-näytöllä välilhedellä "Rajoitukset" tai "Muokkaa"-painikkeen takaa.

![](/assets/files/docs/Asiakkaat/Lisaarajoitus3.png)

![](/assets/files/docs/Asiakkaat/Asiakkaanrajoitukset1.png)

Klikkaa kohdasta "Lisää rajoitus", kirjoita selityskenttään rajoituksen syy. Tallenna "Lisää rajoitus"-painikkeella. 

![](/assets/files/docs/Asiakkaat/Lisaarajoitus4.png)

Muokkaa-painikkeen kautta lisätty rajoite tallennetaan "Tallenna" -painikkeella. 

![](/assets/files/docs/Asiakkaat/Asiakkaanrajoitukset2.png)

Rajoitteelle voi tarvittaessa määrittää automaattisen päättymisajan Vanhenee -kenttään. Vain myöhäisin päättymispäivämäärä näkyy 
lainausnäytöllä, kun rajoitteita on enemmän kuin yksi ja niille on asetettu päättymispäivämäärä. Jos et määritä päättymisaikaa, on rajoite voimassa toistaiseksi. 

![](/assets/files/docs/Asiakkaat/Rajoitettu.png)

Rajoitteet voi ohittaa klikkaamalla “Ohita rajoitus tilapäisesti”. Tässä toimitaan kirjaston/kimpan ohjeiden mukaan.

![](/assets/files/docs/Asiakkaat/Rajoitukset6.png)

Kimppakohtaisia määritteitä/rajoitteita voi olla käytössä “Muut määreet ja tunnukset”-kohdassa.

## 1.5. Asiakkaiden kommenttien ja muutospyyntöjen käsittely

Jos järjestelmäasetuksissa annetaan asiakkaille oikeus muuttaa tietojaan
verkkokirjaston kautta, täytyy muutokset hyväksyä virkailijaliittymän
kautta ennen niiden voimaantuloa. Jos järjestelmässä on hyväksymistä
odottavia muutoksia, niistä näkyy linkki "Tietojensa muokkaamista haluavat asiakkaat"
Kohan etusivulla. 

![](/assets/files/docs/Asiakkaat/Etusivunlinkki.png)

Kun klikkaat linkkiä, saat listan kaikista odottavista muutospyynnöistä ja klikkaamalla asiakkaan
nimen kohdalta saat hänen tekemät muutokset näkyviin. Voit hyväksyä muutokset, kieltää ne tai jättää
ne kokonaan huomioimatta.

![](/assets/files/docs/Asiakkaat/tietojenmuutos.png)

Asiakkaan tiedot -linkistä pääset asiakkaan tietoihin katsomaan mm. onko asiakkaalla
rajoitteita, jotka päivityksen yhteydessä on syytä ottaa pois.

Asiakkaan tiedoissa käsittelemätön muutospyyntö näkyy sekä lainaus- että tiedot-sivulla.

![](/assets/files/docs/Asiakkaat/Odottavatmuutokset.png)

## 1.6 Asiakkaan tiedot

Kun katsot asiakkaan tietuetta, on vasemmassa reunassa valittavissa
useita eri välilehtiä, joilla on erilaisia tietoja.

![](/assets/files/docs/Asiakkaat/vasen.png)

### 1.6.1. Lainaus
Lainaus-välilehden toiminnot on kuvattu tarkemmin Koha Ohje suomeksi -ohjeen kohdassa 2. Lainaaminen

### 1.6.2. Tiedot

Kaikki asiakkaan (henkilö)tiedot näkyvät Tiedot-välilehdellä. Täällä on
yhteystiedot, huomautukset, asiakkaan viestiasetukset ym.

Jos asiakas on lapsi, hänen takaajansa nimet ovat linkkinä kohdassa Takaajat.
![](/assets/files/docs/Asiakkaat/Huoltajat.png)

Takaajan tietueessa näkyy kaikkien huollettavien tiedot kohdassa Taattavat.
![](/assets/files/docs/Asiakkaat/Taattavat.png)

### 1.6.2. Maksut

Asiakkaan maksuhistoria näkyy maksuissa Tapahtumat-välilehdellä. Siellä näkyy
myöhästymismaksujen lisäksi kaikki Kohan kautta käsitellyt maksut, esim.
uusi kortti, noutamaton varaus, palautuskehotus..

![](/assets/files/docs/Asiakkaat/Tapahtumat8.png)

Tällä näytöllä on seuraavat sarakkeet:

\- _Luotu:_ päiväys, jolloin maksu luotiin

\- _Päivitetty:_ päiväys, jolloin maksuriviä on päivitetty

\- _Tilin tyyppi:_ tapahtuman selite

\- _Maksujen kuvaus:_ tieto mistä niteestä maksu muodostuu ja myöhästyneen
niteen eräpäivä sekä linkki nidetietoon

\- _Viivakoodi:_ Niteen viivakoodi -linkki

\- _Eräpäivä:_ Lainan eräpäivä

\- _Palautuspvm:_ Lainan palautuspäivä

\- _Lainauspvm:_ Niteen lainauspäivä

\- _Lainauspiste:_ Kirjasto, josta nide on lainattu

\- _Kotikirjasto:_ Niteen kotikirjasto

\- _Huomautus:_ tähän tulee maksuun liittyvä huomautus esim. Online transaction-koodi, manuaalisesti lisätty tieto 

\- _Summa:_ maksettavien maksujen kokonaissumma

\- _Maksettavaa:_ vielä maksamatta oleva määrä

\- _Toiminnot:_ Kimppakohtaisia eroja tämän sarakkeen painikkeissa.

![](/assets/files/docs/Asiakkaat/Toiminnot3.png)

- _"Tulosta" vie ko. maksun tiedot tulostusnäkymään

-"Tiedot" vie ko. maksun veloitustietoihin

![](/assets/files/docs/Asiakkaat/Veloitustiedot.png)

-"Maksa" vie Maksa maksuja -välilehdelle maksamaan ko. yksittäisen maksun.

![](/assets/files/docs/Asiakkaat/Toiminnotmaksa.png)

-"Peruuta veloitus" -painiketta painamalla ko. maksu peruuntuu.

![](/assets/files/docs/Asiakkaat/Peruutaveloitus.png)

-"Luo hyvitys"

![](/assets/files/docs/Asiakkaat/Luohyvitys2.png)

-"Mitätöi maksutapahtuma"

![](/assets/files/docs/Asiakkaat/Mitatoimaksutapahtuma.png)

Mitätöinnin jälkeen maksu näkyy uudella rivillä seuraavasti:

![](/assets/files/docs/Asiakkaat/Mitatoimaksutapahtuma2.png)

-"Käytä alennusta"

![](/assets/files/docs/Asiakkaat/Kaytaalennusta.png)

#### 1.6.2.1. Maksujen maksaminen/poistaminen rivi kerrallaan

Jokaisen rivin maksu voidaan maksaa tai poistaa erikseen klikkaamalla
rivillä joko Maksa tai Poista. Maksu voidaan maksaa kokonaan tai
osittain.

![](/assets/files/docs/Asiakkaat/maksurivi.png)

Maksun maksaminen riviltä kokonaan

\- Valitse Maksa sen maksun kohdalla, mikä maksetaan

- Maksun summa tulee Peri asiakkaalta: -laatikkoon

![](/assets/files/docs/Asiakkaat/periasiakkaalta.png)

\- Klikkaa Hyväksy

- Maksu poistuu maksamattomista maksuista ja näkyy kokonaan maksettuna.

Maksun maksaminen riviltä osittain

\- Valitse Maksa sen maksun kodalla, mikä maksetaan.

- Muokkaa summaa, joka tulee Peri asiakkaalta-laatikkoon. Hyväksy.

![](/assets/files/docs/Asiakkaat/osamaksu2.png)

\- Loput maksusta jää Maksettava- sarakkeeseen Maksa
maksuja-välilehdelle.

Maksun poistaminen riviltä

\- Klikkaa Poista sen maksun kohdalta, joka poistetaan. Jatka
valitsemalla Poista tämä maksu.

![](/assets/files/docs/Asiakkaat/poistamaksu2.png)

Maksu siirtyy Maksa maksuja-välilehdeltä Tili-välilehdelle.

![](/assets/files/docs/Asiakkaat/poistettu2.png)

#### 1.6.2.2. Maksa kaikki tai jokin tietty summa maksuista

Maksa kaikki

\- Klikkaa Maksa kaikki -nappia.

![](/assets/files/docs/Asiakkaat/maksa1.png)

\- Klikkaa Hyväksy

Maksa tietty summa maksuista

\- Klikkaa Maksa kaikki -nappia.

- Kirjoita Peri asiakkaalta -laatikkoon asiakkaalta perimäsi rahamäärä.
  Kokonaisvelka näkyy Saatavia yhteensä -kohdassa.

![](/assets/files/docs/Asiakkaat/maksa2.png)

\- Klikkaa Hyväksy.

\- Maksu päivittyy kuittaamaan vanhimmat maksut ensin.

#### 1.6.2.3. Maksa valitut maksut

\- Laita valintamerkki niiden maksujen kohdalle, jotka maksetaan,
klikkaa Maksa valitut.

![](/assets/files/docs/Asiakkaat/maksa3.png)

Valittujen maksujen summa näkyy Peri asiakkaalta -laatikossa.

![](/assets/files/docs/Asiakkaat/maksa4.png)

\- Klikkaa Hyväksy

- Maksu päivittyy kuittaamaan valitun maksun.

#### 1.6.2.4. Poista kaikki maksut

Klikkaa Poista kaikki maksut -nappia listauksen alapuolella

![](/assets/files/docs/Asiakkaat/maksa5.png)

\- Kaikki maksut poistuvat saatavista ja näkyvät poistettuina maksuina

#### 1.6.2.5. Maksun peruminen

Jos vahingossa merkitset niteen maksun maksetuksi, voit kumota maksun
klikkaamalla Toiminnot-sarakkeessa Peruuta.

![](/assets/files/docs/Asiakkaat/maksa6.png)

\- Klikkauksen jälkeen tulee uusi rivi, jossa näkyy maksun peruutus

![](/assets/files/docs/Asiakkaat/maksa7.png)

Peruutuksen voi vielä perua klikkaamalla uudelleen “Peruuta”.

HOX HOX!!Jos kirjastossa on käytössä kassajärjestelmä, joka on
yhteydessä kirjastojärjestelmään, ohje löytyy kohdasta 4.8.3.6. KORJAA
TÄMÄ

#### 1.6.2.6. Maksun luominen

Sellaisia maksuja, joita järjestelmä ei tee automaattisesti, voi
virkailija tallentaa Lisää maksu -välilehdellä.

![](/assets/files/docs/Asiakkaat/lisaamaksu.png)

\- Valitse ensin maksun tyypppi

- Jos maksu liittyy johonkin niteeseen, voit lisätä sen viivakoodin
  linkiksi niteeseen

Kuvaus-kenttään voi antaa maksun kuvauksen

![](/assets/files/docs/Asiakkaat/maksunkuvaus.png)

Summa-kenttäään annetaan pelkästään maksun määrä (vain numeroita ja
desimaaleja). Tallennuksen jälkeen maksu näkyy yhteenvedossa.

![](/assets/files/docs/Asiakkaat/maksunsumma.png)

#### 1.6.2.7. Hyvitysten luominen

Tämä toiminto luo asiakkaalle saldoon “plussasaldoa”. Hyvitystä voidaan
käyttää maksujen maksamiseen tai maksun anteeksiantoon. HUOM! Tarkista
ensin kirjastosi käytäntö plussasaldon lisäämisestä asiakkaalle. Tämän
käyttäminen ei ole sallittua mm. OUTI-kirjastoissa.

![](/assets/files/docs/Asiakkaat/hyvitys.png)

\- Valitse ensin hyvityksen tyyppi

\- Jos maksu liittyy johonkin tiettyyn niteeseen, lue niteen viivakoodi
Viivakoodi-kenttään

\- Kuvaus-kenttään voit kirjoittaa selityksen

- Anna Summa-kenttään vain numeroita ja desimaaleja, ei
  valuuttamerkkejä.

#### 1.6.2.8. Maksujen tulostaminen

Jokaisen maksurivin lopussa on Tulosta-linkki. Klikkaamalla tästä
linkistä saat tulostettua niteen nimeke- ja maksutiedot sekä tilin
kokonaissaldon.

![](/assets/files/docs/Asiakkaat/maksujentulostus.png)

#### 1.6.2.9. Maksujen maksaminen Ceepos-kassaliittymän kautta

##### 1.6.2.9.1. Valmistelut ennen maksujen vastaanottoa

Avaa Kohassa asiakkaan Maksa maksuja-välilehti. Valitse sieltä ne
maksut, jotka asiakas maksaa ja klikkaa joko Maksa kaikki tai Maksa
valitut.

![](/assets/files/docs/Asiakkaat/maksamaksuja2.png)

Jos toimipistekoodia ei ole näkyvissä, klikkaa Lisää toimipiste.

![](/assets/files/docs/Asiakkaat/lisäätoimipiste.png)

Toimipiste on sama kuin kassan numero. Jos kirjastossa on useampi kassa,
tulee tähän toimipistekoodi.

![](/assets/files/docs/Asiakkaat/lisäätoimipiste2.png)

![](/assets/files/docs/Asiakkaat/lisäätoimipiste3.png)

Kun toimipiste on valittu, se näkyy näytöllä. Toimipiste näkyy niin
kauan kuin evästeitä (cookies) ei tyhjennetä. Jos evästeet poistetaan,
pitää toimipiste lisätä uudelleen.

![](/assets/files/docs/Asiakkaat/lisäätoimipiste4.png)

##### 1.6.2.9.2. Maksun lähettäminen kassaohjelmaan

Kun klikkaat toimipisteen numeroa, se muuttuu vihreäksi ja tieto siirtyy
kassaan.

![](/assets/files/docs/Asiakkaat/ceepos6.png)

Odota, että kassajärjestelmä käsittelee maksun. Se ilmenee siten, että
näytölle ilmestyy keltainen pyörivä ympyrä. Voit siirtyä Ceeposiin ja
veloittaa asiakkaalta maksun. Toimi kirjaston Ceepos-ohjeiden mukaisesti
ja palaa sitten takaisin Kohaan, jossa asiakkaan maksut ovat
automaattisesti merkitty suoritetuiksi.

##### 1.6.2.9.3. Näkymä Kohan Maksut-osiossa

Kohassa asiakkaan Tili-välilehdellä näkyy maksutapahtuman numero. Muista
aina varmistaa, että maksusta on ilmestynyt yksi uusi maksurivi maksun
tapahtumanumerolla, ja että maksurivillä maksettu summa on oikein.

![](/assets/files/docs/Asiakkaat/testimaksu.png)

Kun klikkaat maksutapahtuman rivillä, se maalaa siihen maksutapahtumaan
liittyvät rivit.

![](/assets/files/docs/Asiakkaat/testimaksu2.png)

Ongelmatilanteissa ota yhteyttä joko oman kirjaston/kimpan Koha-tukeen
tai kirjastosi Ceepos-ohjelman pääkäyttäjään.

### 1.6.3. Kiertolistat

Kiertolistat tarkoittaa lehtikiertolistaa eli jos kirjaston työntekijä
on jonkun lehden sisäisellä kiertolistalla.

![](/assets/files/docs/Asiakkaat/lehtikierto1.png)  
![](/assets/files/docs/Asiakkaat/lehtikierto2.png)

### 1.6.4. Muutosloki

Muutoslokille kertyy tietoa, kun asiakkaan tietoja on katsottu tai
muokattu ja jos asiakastieto on tullut asiakashaussa hakutuloslistalle.
Täällä näkyvät myös lainaus- ja palautustapahtumat, jos niin on
asetuksissa määritetty.

![](/assets/files/docs/Asiakkaat/lokitiedot.png)

\- _Pvm-sarake_ kertoo tarkan ajan (päivämäärä ja kellonaika), jolloin
asiakkaan tiedoissa on tapahtunut jotain

\- _Virkailija-sarake_ näyttää sen työntekijän tunnuksen, joka tietoja
on katsellut tai tehnyt muutokset/haun (virkailijan nimi ja
borrowernumber)

\- _Osio-sarake_ näyttää missä Kohan osiossa katselu/muutos on
tapahtunut

\- _Toiminto-sarakkeesta_ näkee mitä asiakkaan tiedoissa on tehty

\- _ID-tunnus-sarakkeessa_ näkyy, kenen asiakkaan tietoja on muutettu
(asiakkaan nimi ja borrowernumber)

\- _Tiedot-sarake_ kertoo tarkemmin mitä tapahtuma koskee esim. mikä
nide on lainattu tai asiakkaan kirjautuminen automaatille

- _Käyttöliittymä-sarakkeesta_ näkee onko loki kertynyt
  virkailijaliittymästä (intranet), Kohan verkkokirjastosta tai Finnasta
  (opac) tai palautus-/lainausautomaatilta (sip, opac). Rest-merkintä
  tulee silloin, kun asiakkaan tietoihin on otettu yhteyttä restin kautta
  esim. Ceepos ja Ellibs.

### 1.6.5. Ilmoitukset

Tällä näytöllä näkyy asiakkaalle lähteneet tai lähtemässä olevat
ilmoitukset. Ilmoittamistapa valitaan asiakastiedoissa asiakkaan
viestiasetuksissa.

<img src="Lahetetytilmoitukset.PNG" title="Kuvakaappaus Ilmoitukset-välilehdeltä" alt="Kuvakaappaus Ilmoitukset-välilehdeltä" style="width:65.0%" />

\- _Ilmoitus_-sarakkeessa näkyy viestin otsikko. Klikkaamalla viestin
nimeä pääset näkemään koko viestin.

\- _Tyyppi_-sarakkeessa näkyy, missä muodossa viesti on lähetetty.
Koha-Suomessa käytössä: printti, sms, sposti, suomi.fi

\- _Tila_-sarakkeesta näkee viestin lähetyksen tilan  
lähetetty: viesti on lähetetty eteenpäin järjestelmästä varsinaiseen
lähettävään järjestelmään  
odottaa: viestiä ei ole vielä lähetetty eteenpäin lähettävään
järjestelmään  
\\**\\** epäonnistunut: viestin lähetys on epäonnistunut. Osa
lähettävistä järjestelmistä (esim. tekstiviestioperaattorit) palauttaa
Kohaan epäonnistumisen syyn, jolloin se näkyy
Toimitushuomautus-sarakkeessa.

\- _Aika_-sarakkeessa näkyy viestin lähetysaika. Tieto päivittyy aina,
kun viestiä yritetään lähettää uudelleen eli kyse ei ole viestin
luontiajankohdasta.

- _Toimitushuomautus_-sarakkeeseen tulee näkyviin viestin lähetyksen
  epäonnistumisen syy, jos Koha saa siitä tiedon. Lähinnä
  tekstiviestioperaattorit palauttavat virheen syyn.  
  _Message is duplicate_ tarkoittaa, että Koha on hylännyt viestin, koska
  se on täsmälleen samanlainen kuin hiljattain lähetetty toinen viesti.
  Näitä näkyy erityisesti tekstiviestien yhteydessä.  
  _Message validity period has expired_ tarkoittaa, että viestiä on
  yritetty lähettää maksimimäärä kertoja.  
  _Unknown error_ tarkoittaa, että viestin epäonnistumisen syytä ei
  tiedetä tai pystytä tarkentamaan. Syy voi olla esim. asiakkaan
  puhelinnumero voi olla väärä tai hänen puhelimensa ei ota vastaan
  tekstiviestejä, tai operaattorin päässä on häiriö.  
  _Recipient is temporarily unreachable_ tarkoittaa, että vastaanottajaan
  ei ole saatu yhteyttä  
  \\**\\** _ERROR 4 2 messages failed: Unallowed recipient phone number_
  tarkoittaa, että asiakkaan puhelinnumerossa on jotain vikaa tai se on
  väärässä muodossa (esim. lankapuhelin)

### 1.6.6 Tilastot

Tilastot-osiossa näkyy asiakkaan lainatilasto edelliseltä ja kuluvalta
päivältä. Lainat on jaoteltuna aineistolajeittain ja hyllypaikoittain.
Taulukossa näkyy myös kuluvan päivän palautukset ja lainat.

![](/assets/files/docs/Asiakkaat/asiakkaantilastot.png)

### 1.6.7 Hankintaehdotukset

Jos asiakas on tehnyt verkkokirjastossa hankintaehdotuksia, ne näkyvät
asiakkaan tiedoissa Hankintaehdotukset-osiossa.

![](/assets/files/docs/Asiakkaat/hankintaehdotukset.png)

Samalla sivulla voi myös tehdä asiakkaan puolesta hankintaehdotuksen.
Paina “Uusi hankintaehdotus” -nappia, jolloin avautuu lomake. Täytä
vähintään punaisella merkityt pakolliset tiedot ja paina sitten
lomakkeen alareunasta “Lähetä ehdotuksesi”.

![](/assets/files/docs/Asiakkaat/teeuusihankintaehdotus.png)

![](/assets/files/docs/Asiakkaat/teeuusihankintaehdotus2.png)

### 1.6.8. Lainat

Asiakkaan tietojen alapuolella on taulukkonäkymässä asiakkaan lainat,
maksut, varaukset ja rajoitukset. Lainoihin pääsee klikkaamalla
“Lainassa”-painiketta. Maksut välilehteä ei näy, jos asiakkaalla ei ole maksuja.

![](/assets/files/docs/Asiakkaat/lainat.png)

Tällä näytöllä näkyy myös asiakkaan huollettavien lainat Perheen lainat
-välilehdellä. Huollettavalla näkyy myös perheen sisarusten
lainat eli niiden henkilöiden lainat, joilla on sama takaaja.

![](/assets/files/docs/Asiakkaat/perheenlainat.png)

## 1.7. Asiakkaan hakeminen

Klikkaamalla linkkiä Asiakkaat saat hakulaatikon, jossa voit selata tai
hakea asiakkaiden tietoja. Haku toimii millä tahansa nimen osalla tai
kortin numerolla.

![](/assets/files/docs/Asiakkaat/haeasiakkaita.png)

Klikkaamalla pientä plus-merkkiä \[+\] hakulaatikon oikealla puolella
saat lisää hakuominaisuuksia käyttöösi. Täällä voit mm. rajata hakusi
kirjastoittain tai asiakaslajeittain.

![](/assets/files/docs/Asiakkaat/plushaku.png)

Hakukenttiin tekemiesi valintojen perusteella voit hakea asiakasta eri
tavoin.

![](/assets/files/docs/Asiakkaat/hakukentät.png)

\- Perushaku:  
Anna asiakkaan nimi tai nimen osa, käyttäjätunnus tai kirjastokortin
viivakoodi.

\- Sukunimi:  
Anna asiakkaan sukunimi tai sukunimen osa.

\- Sähköposti:  
Anna mikä tahansa osa sähköpostiosoitteesta ja valitse hakutyypiksi
_sisältää_ (ei alkaa)

\- Asiakkaan ID:  
Anna Kohan Asiakkaan ID-numero (eri kuin kirjastokortti)

\- Käyttäjätunnus:  
Anna asiakkaan kirjastokortin numero tai osa siitä.

\- Puhelinnumero:  
Anna puhelinnumero kokonaisuudessaan kuten se on syötetty järjestelmään
tai käytä tyhjää merkkiä numeroiden jaksotteluun. Esim. Haettaessa
numeroa (013) 267 6200 voit kirjoittaa sen juuri samalla tavalla tai
muodossa 013 267 6200.

\- Katuosoite:  
Anna mikä tahansa asiakkaan osoitteen osa (kaikki osoitekentät
huomioiden) ja valitse hakutyypiksi _sisältää_.

\- Syntymäaika:  
Ohjeteksti ilmestyy kertomaan missä muodossa syntymäaika pitää antaa.
Muoto PP.KK.VVV tarkoittaa, että päivät, kuukausi ja vuosi erotetaan
toisistaan pisteellä.

Voit myös valita jokaisessa haussa hakutyypin alkaa tai sisältää.
Valinta sisältää toimii vapaasanahaun kaltaisesti eli haettu merkkijono
voi olla missä tahansa kohdassa hakukentässä.

![](/assets/files/docs/Asiakkaat/syntymäpäivä.png)

Voit myös selata asiakkaita sukunimen ensimmäisen kirjaimen mukaan
linkkinä olevien kirjainten mukaan.

![](/assets/files/docs/Asiakkaat/aastaoohon.png)
