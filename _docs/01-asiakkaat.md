---
title: 'Kohan ohje suomeksi'
permalink: /dokumentaatio/asiakkaat/
redirect_from:
  - /theme-setup/
toc: true
---

# 1. Asiakkaat

Aina ennen asiakastiedon lisäämistä on hyvä tarkistaa löytyykö asiakkaan tiedot jo Kohasta. Voit 
hakea asiakkaan tietoja esim. nimihaulla sekä syntymäaikahaulla.

## 1.1. Asiakkaan hakeminen

Klikkaamalla linkkiä _Asiakkaat_ saat hakulaatikon, jossa voit selata tai
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

\- Kortin numero:
Anna asiakkaan kortin numero

\- Sähköposti:  
Anna mikä tahansa osa sähköpostiosoitteesta ja valitse hakutyypiksi
_sisältää_ (ei alkaa)

\- Asiakkaan ID:  
Anna Kohan Asiakkaan ID-numero (eri kuin kirjastokortti)

\- Käyttäjätunnus:  
Anna asiakkaan kirjastokortin numero tai osa siitä.

\- Lankapuhelin:  
Anna lankapuhelinnumero kokonaisuudessaan kuten se on syötetty järjestelmään
tai käytä tyhjää merkkiä numeroiden jaksotteluun. Esim. haettaessa
numeroa (013) 267 6200 voit kirjoittaa sen juuri samalla tavalla tai
muodossa 013 267 6200.

\- Osoite:  
Anna mikä tahansa asiakkaan osoitteen osa (kaikki osoitekentät
huomioiden) ja valitse hakutyypiksi _sisältää_.

\- Syntymäaika:  
Ohjeteksti ilmestyy kertomaan missä muodossa syntymäaika pitää antaa.
Muoto PP.KK.VVVV tarkoittaa, että päivät, kuukausi ja vuosi erotetaan
toisistaan pisteellä.

\- Etunimi:
Tee asiakashaku etunimellä tai kaikilla etunimillä.

\- Varaustunnus:
Anna asiakkaan varaustunniste.

\- Matkapuhelin:
Anna matkapuhelinnumero kokonaisuudessaan kuten se on syötetty järjestelmään
tai käytä tyhjää merkkiä numeroiden jaksotteluun. Esim. haettaessa
numeroa 0442676200 voit kirjoittaa sen juuri samalla tavalla tai
muodossa 044 267 6200.

Voit myös valita jokaisessa haussa hakutyypin alkaa tai sisältää.
Valinta _sisältää_ toimii vapaasanahaun kaltaisesti eli haettu merkkijono
voi olla missä tahansa kohdassa hakukentässä.

Saat tarkennettua hakua myös valitsemalla asiakkaan _kirjaston_ ja/tai rajaamalla hakua _asiakastyypin_ mukaan.

Voit myös selata asiakkaita sukunimen ensimmäisen kirjaimen mukaan
linkkinä olevien kirjainten mukaan.

![](/assets/files/docs/Asiakkaat/aastaoohon.png)

## 1.2. Lisää uusi asiakas

Asiakkaat lisätään menemällä Asiakkaat-välilehdelle.

![](/assets/files/docs/Asiakkaat/Lisaauusiasiakas1.png)

Sivulla on alasvetovalikkovaihtoehdot: +Uusi asiakas ja +Asiakkaan pikalisäys. Huom. Kaikissa kimpoissa ei ole Asiakkaan pikalisäys-vaihtoehtoa käytössä, joten valitse kimppasi ohjeistama asiakkaan lisäystapa.

![](/assets/files/docs/Asiakkaat/Lisaauusiasiakas2.png)

Klikkaa _Uusi asiakas_, saat alasvetovalikon, josta valitset asiakkaan tyypin.

![](/assets/files/docs/Asiakkaat/Lisaauusiasiakas3.png)

### 1.2.1. Henkilötunnus ja sotu-siilo

Kohaan on tehty Suomessa ominaisuus, sotu-siilo, jonne tallennetaan
tietoturvallisesti asiakkaiden henkilötunnukset. Sotu-siilo on yhteinen kaikille kimpoille.

Oheisissa ruutukaappauksissa käytetty sotu on tehty
henkilötunnusgeneraattorin avulla, se ei ole kenenkään henkilön oikea
tunnus, mutta täyttää tunnuksen ominaisuudet tarkistusmerkkiä myöten.
Sotu-avaimella muodossa “sotuxxxx” voi hakea asiakkaan tiedot esille,
mutta henkilötunnus ei näy.

Syötä _Lisää hetu_-kohtaan asiakkaan henkilötunnus.

![](/assets/files/docs/Asiakkaat/Lisaahetu.png)

Jos henkilötunnusta ei ole ennestään sotu-siilossa, siitä tulee ilmoitus
"Hetu tallennettu!".

![](/assets/files/docs/Asiakkaat/Hetutallennettu1.png)

Sotu-avain siirtyy automaattisesti asiakastietoihin _Muut määritteet ja
tunnukset_ -kohtaan kenttään Sosiaaliturvatunnus/Henkilötunnus/Sotu-avain
(kentän nimi voi vaihdella kimpan mukaan).

![](/assets/files/docs/Asiakkaat/Sotuavain.png)

Jos henkilötunnus on virheellinen, tulee siitä ilmoitus: “Tarkista hetu!”.

![](/assets/files/docs/Asiakkaat/Tarkistahetu.png)

Jos syötetty henkilötunnus on jo sotu-siilossa, järjestelmä tutkii automaattisesti asiakasrekisteristä löytyykö 
henkilötunnuksen sotu-avaimella asiakastietoja. 

Jos tietoja ei löydy asiakasrekisteristä, niin käyttäjälle tulee ilmoitus “Hetu asetettu!". Jatka tuolloin uuden asiakkaan
tallentamista käyttäen sotu-siilon antamaa sotu-avainta.

![](/assets/files/docs/Asiakkaat/Hetuasetettu.png)

Jos asiakastiedot löytyvät, niin käyttäjälle tulee ilmoitus "Asiakas on jo olemassa! Paina OK siirtyäksesi tietoihin." 
Klikkaamalla _OK_ käyttäjä siirtyy automaattisesti asiakkaan tietoihin, joita tarvittaessa muokataan.

![](/assets/files/docs/Asiakkaat/Sotu3.png)


#### 1.2.1.1. Sotu-siilon käyttöliittymä

Sotu-siiloon on olemassa myös toinen käyttöliittymä, jonka kautta
esimerkiksi laskuttajat voivat tarkistaa asiakkaan henkilötunnuksen
sotu-avaimella. Heillä on erilliset tunnukset tarkistusta varten.
Sotuteekistä tarkemmin Koha ohje suomeksi kohdassa 12.17.3 Sotuteekki

---

### 1.2.2. Nimi, syntymäaika ja varaustunnus

Syötä asiakkaan koko nimi ja syntymäaika. Varaustunniste täyttyy automaattisesti. Huomaathan,
että kimppasi Kohassa ei välttämättä näy kaikki kuvissa näkyvät kentät tai vaihtoehdot.

![](/assets/files/docs/Asiakkaat/Varaustunnus1.png)

Asiakaslajeihin on määritetty ikärajoituksia. Ohjelma tarkistaa
syntymäajan mukaan, voiko asiakas kuulua asiakaslajiin, johon
häntä ollaan tallentamassa. Voit saada tällaisen virheilmoituksen:  
![](/assets/files/docs/Asiakkaat/ikaraja.png)

### 1.2.3. Takaaja

Jos kyseessä on lapsiasiakas, hänelle pitää tallentaa takaaja. Klikkaa
_Lisää takaaja_ -nappia, niin pääset hakemaan rekisteristä lapselle
takaajan.

![](/assets/files/docs/Asiakkaat/Lisaatakaaja.png)

Takaajaa voi hakea joko nimellä tai kirjastokortin numerolla. Valitse
alasvetovalikoista sopivat vaihtoehdot.

![](/assets/files/docs/Asiakkaat/Valitsetakaaja.png)

Saat listan hakuun sopivista asiakkaista. Klikkaa oikealta _Valitse_-painiketta
oikean henkilön kohdalla. 

Valitse alasvetovalikosta takaajan suhde asiakkaaseen Huom. alasvetovalikon vaihtoehdot voivat vaihdella kimpoissa.

![](/assets/files/docs/Asiakkaat/Asiakastakaaja.png)

Tallennuksen jälkeen huoltajan tiedoista näkyy hänen koko nimensä sekä kirjastokortin numero. Voit 
tallentaa lapsiasiakkaalle useamman kuin yhden huoltajan tiedot.

![](/assets/files/docs/Asiakkaat/Takaajat.png)

Huom! Jos takaajaa ei löydy asiakasrekisteristä, avaa uusi välilehti ja
tallenna takaajan tiedot rekisteriin. Palaa sen jälkeen lapsiasiakkaan
tietoihin toisella välilehdelle ja tee takaajahaku uudelleen.

Roskakorin kuvaketta klikkaamalla saat huoltajatiedon poistettua. Huom. alaikäisellä asiakkaalla tulee aina olla vähintään
yksi takaaja, joten lapsiasiakkaan tietojen tallennus ei onnistu, jos häneltä puuttuu takaajatieto.

#### 1.2.3.1. Ei-asiakas takaaja-tiedon lisääminen

Kimppakohtainen.

![](/assets/files/docs/Asiakkaat/Eiasiakastakaaja.png)

### 1.2.4. Yhteystiedot

Osoite-osiossa _Kunta_ tarkoittaa käytännössä postitoimipaikkaa, ei
pelkästään kotikuntaa. Englanninkielistä sanaa City ei voi kääntää
postitoimipaikaksi tässä kohti, koska sama sana on kunta-merkityksessä
muussa yhteydessä. Voit valita postinumeron ja postitoimipaikan alasvetovalikosta tai kirjoittaa ne itse.

![](/assets/files/docs/Asiakkaat/Osoitetiedot.png)

Syötä _Yhteystiedot_-osiossa asiakkaan puhelinnumero (lankapuhelinnumero _Lankapuhelin-kenttään_ ja matkapuhelinnumero
_Matkapuhelin_-kenttään) ja sähköpostiosoite. Matkapuhelin-kenttään lisätty numero kopioituu automaattisesti asiakkaan viestiasetuksiin, jos
asiakas haluaa varausilmoitukset tekstiviestinä. Sähköpostiosoite on se osoite, johon asiakasviestit lähtevät.

Asiakas voi halutessaan valita ensisijaisen yhteydenottotavan kirjaston henkilökunnan yhteydenottoja varten. Kaikissa kimpoissa tätä valintaa 
ei välttämättä ole otettu käyttöön. 

![](/assets/files/docs/Asiakkaat/Yhteystiedot1.png)

Huom! Puhelinnumero-kenttiin ei saa kirjoittaa muuta kuin
puhelinnumeron. Ei esim. perään äiti, isä yms. eikä väliviivaa.
Kansainvälisen suunnan (esim. +358) puhelinnumeron yhteyteen voi lisätä.

Asiakkaalle voidaan tallentaa myös vaihtoehtoinen osoite. Huom! Tässä on
kimppakohtaisia eroja.

![](/assets/files/docs/Asiakkaat/Vaihtoehtoinenosoite.png)

### 1.2.5. Kirjastotiedot

#### 1.2.5.1. Kirjastonhallinta-osio

Kirjastonhallinta-osio sisältää kirjaston käyttöön liittyviä tietoja.

![](/assets/files/docs/Asiakkaat/kirjastohallinta.png)

\- Lue asiakkaan kirjastokortin numero ylimmäisenä olevaan
_Kirjastokortin numero_ -kenttään.

\- _Kirjasto_-kenttään valitaan asiakkaan kotikirjasto, jota järjestelmä
ehdottaa mm. varausta tehtäessä noutokirjastoksi.

\- _Tyyppi_-kohdassa voi vaihtaa asiakastyypin. Huom! Jos tässä kohtaa
vaihtaa asiakastyypin, muutos ei tuo esille mm. takaajatieto-kenttää tai
poista sitä näkyvistä. Tätä ei kannata muuttaa. Aloita mielummin alusta,
jos valitsit alussa väärän asiakastyypin.

\- Valitse asiakasviestien kieli kohdassa _Ilmoitusten kieli_.

#### 1.2.5.2 Kirjaston asetukset-osio
![](/assets/files/docs/Asiakkaat/Huomautuslaatikko1.png)

\- _Tullut asiakkaaksi_ -päivämäärä tulee automaattisesti kuluvan päivän
mukaiseksi.

\- _Vanhentuu_ -kohtaan ei tarvitse merkitä mitään. Tieto tulee
automaattisesti asiakaslajille tehtyjen määritysten mukaan.

\- _Huomautus_ (näkyy verkkokirjastossa) -kohtaan voi merkitä
huomautuksen, jonka asiakas näkee verkkokirjastosta. Huomautus
näkyy OPACissa ja Finnassa.

Finnassa se näkyy Omat tiedot-välilehdellä _Kirjastokortin asetukset_-laatikossa.

![](/assets/files/docs/Asiakkaat/Huomautuslaatikko2.png)

\- _Huomautus (näkyy virkailijatyökalussa)_ -laatikossa oleva huomautus
näkyy Kohassa virkailijoille tiedot- ja lainausnäytöllä.

![](/assets/files/docs/Asiakkaat/Huomautuslaatikko.png)

#### 1.2.5.3. Kirjautumistunnus-osio
_Kirjautumistunnus_-osioon voi lukea esim. kirjastokortin numeron tai
erillisen käyttäjätunnuksen, jolla asiakas voi kirjautua
verkkokirjastoon. Huom! Kimppakohtaisia eroja.

![](/assets/files/docs/Asiakkaat/kirjautumistunnus.png)

Tässä tallennettu käyttäjätunnus näkyy asiakkaan _Tiedot_-välilehdellä.

#### 1.2.5.4. Muut määritteet ja tunnukset

Tähän täytetään mm. Järjestelmäavain asiakastietojen lähetykseen. 

Henkilötunnuksen lisäyksen yhteydessä sotuavain siirtyy automaattisesti tähän Sotuavain-kenttään. 

Myös muita kimppakohtaisia määritteitä voi olla käytössä.

![](/assets/files/docs/Asiakkaat/Muutmaareetjatunnukset1.png)

### 1.2.6. Asiakkaan viestiasetukset

Lopuksi vielä tallennetaan asiakkaan viestiasetukset. Käytettävissä
olevat viestivaihtoehdot vaihtelevat kimpoittain.

![](/assets/files/docs/Asiakkaat/Asiakkaanviestiasetukset.png)

\- Ilmoitus eräpäivänä: Ilmoitus lainojen erääntymisestä eräpäivänä.

\- Ennakkoilmoitus: Etukäteisilmoitus lähestyvästä eräpäivästä (Asiakas
voi valita, montako päivää etukäteen ilmoitus tulee). HUOM! Jos tähän
valitsee 0, ei viestiä lähetetä, vaikka rasti olisi paikallaan.

\- Saapumisilmoitus: Ilmoitus asiakkaalle noudettavissa olevasta
varauksesta.

\- Palautuskuitti: Lista asiakkaan juuri palauttamasta aineistosta.

\- Lainauskuitti: Lista asiakkaan juuri lainaamista niteistä. Tämä on
  sähköinen versio lainauskuitista.

\- Lisää “Tekstiviesti numeroon” -kenttään asiakkaan puhelinnumero, johon hän haluaa viestien saapuvan.
Huom. Matkapuhelin-kenttään lisätty numero kopioituu automaattisesti asiakkaan viestiasetuksiin, jos asiakas 
haluaa varausilmoitukset tekstiviestinä. Testiviesti-vaihtoehtoon ei 
voi laittaa rastia, jos tässä kentässä ei ole puhelinnumeroa.

- SMS-palveluntuottaja-kohtaan ei tarvitse valita mitään. Ominaisuus ei
  ole käytössä.

**Tärkeää**

\- Nämä asetukset kumoavat asiakaslajeihin tehdyt oletusvalinnat.

\- Asiakas voi itse muuttaa näitä asetuksia verkkokirjastossa.

\- Valitse koosteilmoitus ennakkoilmoitukseen ja eräpäiväilmoitukseen,
  niin asiakas saa yhdessä viestissä kaikkien erääntyvien niteiden tiedot
  eikä jokaisesta lainasta erillistä viestiä! Huom. Joissain kimpoissa tämän sarakkeen 
  ruksit on valittu oletuksena ja valinnat lukittu.

## 1.3. Tallennus

Lopuksi tallenna tiedot.

Jos järjestelmä epäilee, että olet tekemässä tupla-asiakkaan, saat siitä
huomautuksen. Jos olet varma, että kyseessä ei ole kopio, valitse “Ei
kopio. Tallenna uutena tietueena”.

![](/assets/files/docs/Asiakkaat/Kopioiasiakastiedot1.png)

---

## 1.4. Ei-tilastoitavat-lainat

Tämä asiakastyyppi on luotu sellaisille lainoille, joita henkilökunta
tekee työtarkoitusta varten. Huom! Voi olla kimppakohtaisia eroja
asiakastyypin nimessä sekä käytännöissä. Tämän asiakastyypin lainoja ei
oteta mukaan tilastoihin.

![](/assets/files/docs/Asiakkaat/eitilastoituvat.png)

## 1.5. Asiakkaan tietojen muokkaaminen

Asiakkaan tietoja voidaan muokata eri painikkeiden kautta. Huom. Tässä voi olla kimppakohtaisia eroja.

Muokataksesi jotain tiettyä osiota asiakastiedoissa (esim.
Kirjastotiedot) klikkaa sen osion alla olevaa sinistä Muokkaa-linkkiä.

![](/assets/files/docs/Asiakkaat/muokkaanappi2.png)

Asiakastietojen yläreunassa olevilla painikkeilla pääset lisäämään asiakkaalle huollettavan, vaihtamaan salasanan, kopioimaan asiakkaan tiedot, tulostamaan asiakkaan haluamia kuitteja asiakaspalvelutilanteessa mm. Tänään lainatut-kuitin, tekemään asiakkaalle tiedonhaussa varauksen siten, että asiakastieto säilyy muistissa, lisäämään asiakastietoihin viestin sekä Muita toimintoja -napin takaa löytyy toiminnot, joilla pääsee uusimaan tilin, poistamaan tunnuksen sekä päivittämään lapsiasiakkaan aikuiseksi. 

Koko asiakastietueen muokkaukseen pääset Muokkaa-painiketta klikkaamalla.

![](/assets/files/docs/Asiakkaat/Muokkaanappi1.png)

### 1.5.1. Lisää huollettava

Tämän napin kautta pääset tallentamaan asiakkaalle huollettavan. Lisää huollettava-nappi avaa alasvetovalikon kimpan asiakastyypeistä, joilla tulee olla huoltaja. Valittuasi asiakastyypin pääset lisäämään asiakastiedot huollettavalle. Takaaja-tieto täydentyy automaattisesti.

### 1.5.2. Salasanan vaihtaminen

Asiakkaan salasanan pääsee muokkaamaan Vaihda salasana-painikkeen kautta. 

Asiakkaan salasanaa ei voi nähdä. Jos asiakas unohtaa salasanansa, hänelle pitää tallentaa uusi salasana.

![](/assets/files/docs/Asiakkaat/salasana.png)

\- Koha ei voi näyttää entistä salasanaa. Jätä salasanakenttä tyhjäksi tai valitse "Peruuta",
jos et halua vaihtaa salasanaa.

\- Jos haluat automaattisesti luodun salasanan, klikkaa “Valitse tästä
luodaksesi satunnaisesti luodun salasanaehdotuksen”. Salasanat näytetään
tekstinä.

- Muista tallentaa.

### 1.5.3. Asiakkaan tietojen kopioiminen

Joissakin tilanteissa on tarpeen käyttää asiakastietojen kopioimista, jos
esim. saman perheen jäsenille tehdään useita kortteja. Kohassa on
toiminto, jolla voidaan kopioida henkilötiedot, jotka toistuvat eri
tietueissa.

Avaa sen asiakkaan tiedot, jonka haluat kopioida ja klikkaa
Kopioi-nappia tietueen yläreunassa.

Sukunimi, osoite, matkapuhelinnumero, sähköpostiosoite, kirjasto, asiakastyyppi ja ilmoitusten kieli 
kopioituvat uuteen lomakkeeseen. Lisää puuttuvat tiedot ja klikkaa Tallenna.

\- Lapsiasiakkaalta kopioituu myös hänen takaajatietonsa.

\- Matkapuhelinkentän puhelinnumero kopioituu myös asiakkaan viestiasetuksiin.

- Tallennuksen jälkeen pääset uuden asiakkaan tietoihin.

### 1.5.4. Tulosta

Tästä alasvetovalikosta voit valita ja tulostaa asiakkaan haluaman kuitin. Huom. kuiteissa voi olla kimppakohtaisia eroja.

![](/assets/files/docs/Asiakkaat/Tulosta.png)

### 1.5.5. Hae ja varaa

Hae ja varaa-näppäin siirtää suoraan Tarkkaan hakuun tekemään tiedonhaun. Pääset tekemään varauksen asiakkaalle suoraan hakutuloslistalla tai tietueen tiedoissa. Hakutuloslistalla voit tarvittaessa myös poistaa toiminnon muistista asiakkaan tiedot. 

![](/assets/files/docs/Asiakkaat/Haejavaraa1.png)

Tietuetiedoissa sitä toimintoa ei ole.

![](/assets/files/docs/Asiakkaat/Haejavaraa2.png)

### 1.5.6. Lisää viesti

![](/assets/files/docs/Asiakkaat/Jataviesti1.png)

Tällä toiminnolla lisätään asiakastietoihin viestejä. Voi lisätä ns. Sisäisen viestin tai Asiakasliittymäviestin. 
Sisäinen viesti näkyy vain virkailijaliittymässä, asiakasliittymäviesti näkyy asiakkaalle verkkokirjastossa.

Voit valita esimääritellyistä viesteistä tarvitsemasi pohjan ja muokata sitä tarvittaessa tai kirjoittaa tyhjään kenttään tarvittavan tekstin.

![](/assets/files/docs/Asiakkaat/Jataviesti2.png)

Sekä sisäiset viestit että asiakasliittymäviestit näkyvät asiakkaan Lainaus- ja Tiedot-sivuilla. Ne voi poistaa klikkaamalla roskakorikuvaketta.

![](/assets/files/docs/Asiakkaat/Jataviesti3.png)

\- Viestiin tallentuu automaattisesti päivämäärä, kirjasto sekä viestin tallentaja, joten niitä ei tarvitse manuaalisesti lisätä viestiin.

### 1.5.7. Muita toimintoja -alasvetovalikko

![](/assets/files/docs/Asiakkaat/Muitatoimintoja1.png)

#### 1.5.7.1. Asiakaan käyttöoikeuden jatkaminen

Asiakastilin vanhennuttua asiakas ei pääse käyttämään korttiaan. Tilin uusimiselle on useita linkkejä ja paikkoja. 

Lainausnäytöllä vanhentumispäivämäärän perässä olevasta linkistä “Uusinta" tai Muita toimintoja-alasvetovalikosta “Asiakkaan käyttöoikeuden jatkaminen”.

![](/assets/files/docs/Asiakkaat/Tilinuusiminen1.png)

Asiakkaan tiedot sivulla tili uusitaan ruudun keskellä sijaitsevan Huomio-kohdan Uusinta-linkin kautta, Kirjastotiedot kohdasta tai 
Muita toimintoja- alasvetovalikosta “Asiakkaan käyttöoikeuden jatkaminen”. 

![](/assets/files/docs/Asiakkaat/Tilinuusiminen2.png)

![](/assets/files/docs/Asiakkaat/Tilinuusiminen3.png)

Asiakkaalle tallentuu tilin vanhentumispäivämäärä asiakastyypille määritellyn voimassaoloajan mukaan.

### 1.5.7.2. Poista

Tällä toiminnolla poistetaan asiakas rekisteristä.

Koha varmistaa, että haluatko varmasti poistaa asiakkaan. Kun klikkaat "Kyllä, poista", niin asiakastili lähtee heti pois asiakasrekisteristä. Ei, älä poista -napin klikkaus peruu toimenpiteen.

![](/assets/files/docs/Asiakkaat/Poista1.png)

Koha ilmoittaa selkeästi miksi asiakasta ei voi poistaa rekisteristä.

![](/assets/files/docs/Asiakkaat/Poista2.png)

![](/assets/files/docs/Asiakkaat/Poista3.png)

![](/assets/files/docs/Asiakkaat/Poista4.png)

### 1.5.7.3. Päivitä lapsi aikuiseksi

Lapsiasiakkaasta ei tule automaattisesti henkilöasiakasta ellei Kohassa ole
siihen liittyvä ajo käynnissä. Lapsen voi muuttaa henkilöasiakkaaksi valitsemalla Muita toimintoja -valikosta “Päivitä lapsi
aikuiseksi”. Koha antaa asiakastyyppivaihtoehdot, joista valitaan haluttua asiakastyyppi. 
Huom. päivitysnappi on aktiivinen kaikilla alaikäisillä asiakkailla ja sillä voi muuttaa tätä kautta lapsiasiakkaan myös esi. kotipalveluasiakkaaksi.

![](/assets/files/docs/Asiakkaat/Lapsiaikuiseksi1.png)

Jos asiakas on edelleen alaikäinen, niin päivitys henkilöasiakkaaksi ei ole mahdollinen.

![](/assets/files/docs/Asiakkaat/Lapsiaikuiseksi2.png)

### 1.5.8. Lapsiasiakkaan takaajan vaihtaminen

Takaajatiedot pääsee muokkaamaan Muokkaa -painikkeen takaa. Kohdassa "Asiakastakaaja" voit sekä poistaa että lisätä takaajan. 

Poistaminen tapahtuu ruksaamalla poistettava takaaja ja sen jälkeen klikkaa "Tallenna". 

![](/assets/files/docs/Asiakkaat/Poistatakaaja.png)

Lisääminen tapahtuu Lisää takaaja-painikkeella. Hae lisättävän huoltajan tiedot avautuvassa ikkunassa.

![](/assets/files/docs/Asiakkaat/Valitsetakaaja.png)

Valitse hakutuloksesta huoltaja ja klikkaa Valitse.

Valitse takaajan suhde ja tallenna.

### 1.5.9. Asiakkaan kuva

Asiakkaan kuva voidaan lisätä valitsemalla kuva koneeltasi Lataa
asiakaskuva -osiossa.

![](/assets/files/docs/Asiakkaat/asiakaskuva.png)

\- Tämä osio ei ole näkyvissä, jos järjestelmäasetuksissa on estetty
kuvien tallentaminen

\- Työkaluissa olevalla toiminnolla Asiakaskuvien lataus voi tuoda
palvelimelle eräajona kuvia

### 1.5.10. Rajoitukset

#### 1.5.10.1. Käyttäjätilin huomautukset

![](/assets/files/docs/Asiakkaat/Kayttajatilinhuomautukset.png)

Jos asiakas ilmoittaa kadottaneensa kirjastokorttinsa, voit merkitä sen
kadonneeksi klikkaamalla "Kyllä" Kortti kadonnut -kohdassa. Lainausnäytöllä tulee ilmoitus Kadonnut: Asiakkaan kortti on kadonnut.

![](/assets/files/docs/Asiakkaat/kadonnutkortti.png)

Jos haluat lainauksen virkailijan tarkistavan asiakkaan osoitteen ennen
lainaamista, laita valinta “Kyllä” päälle Tarkista osoite -kohdassa. Lainausnäytöllä tulee ilmoitus Osoite: Tarkista osoite.

![](/assets/files/docs/Asiakkaat/vaaraosoite.png)

Molemmat vaihtoehdot ovat eräänlaisia rajoituksia eli ne estävät asiakasta käyttämästä asiakastunnustaan.

#### 1.5.10.2. Asiakkaan rajoitukset

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

## 1.6. Asiakkaiden kommenttien ja muutospyyntöjen käsittely

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

## 1.7. Asiakkaan tiedot

Kun katsot asiakkaan tietuetta, on vasemmassa reunassa valittavissa
useita eri välilehtiä, joilla on erilaisia tietoja.

![](/assets/files/docs/Asiakkaat/vasen.png)

### 1.7.1. Lainaus
Lainaus-välilehden toiminnot on kuvattu tarkemmin Koha Ohje suomeksi -ohjeen kohdassa 2. Lainaaminen

### 1.7.2. Tiedot

Kaikki asiakkaan (henkilö)tiedot näkyvät Tiedot-välilehdellä. Täällä on
yhteystiedot, huomautukset, asiakkaan viestiasetukset ym.

Jos asiakas on lapsi, hänen takaajansa nimet ovat linkkinä kohdassa Takaajat.
![](/assets/files/docs/Asiakkaat/Huoltajat.png)

Takaajan tietueessa näkyy kaikkien huollettavien tiedot kohdassa Taattavat.
![](/assets/files/docs/Asiakkaat/Taattavat.png)

### 1.7.3. Maksut

Maksut -välilehden toiminnot on kuvattu tarkemmin Koha ohje suomeksi -ohjeen kohdassa 3. Maksut 

### 1.7.4. Kiertolistat

Kiertolistat tarkoittaa lehtikiertolistaa eli jos kirjaston työntekijä
on jonkun lehden sisäisellä kiertolistalla.

![](/assets/files/docs/Asiakkaat/lehtikierto1.png)  
![](/assets/files/docs/Asiakkaat/lehtikierto2.png)

### 1.7.5. Muutosloki

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
  
  Huom. Muutoslokiin pääsee myös Työkalujen kautta. Se on ohjeistettu Koha ohje suomeksi -ohjeen 
  kohdassa 12.15 Lokien katselu

### 1.7.6. Ilmoitukset

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

### 1.7.7. Tilastot

Tilastot-osiossa näkyy asiakkaan lainatilasto edelliseltä ja kuluvalta
päivältä. Lainat on jaoteltuna aineistolajeittain ja hyllypaikoittain.
Taulukossa näkyy myös kuluvan päivän palautukset ja lainat.

![](/assets/files/docs/Asiakkaat/asiakkaantilastot.png)

### 1.7.8. Hankintaehdotukset

Jos asiakas on tehnyt verkkokirjastossa hankintaehdotuksia, ne näkyvät
asiakkaan tiedoissa Hankintaehdotukset-osiossa.

![](/assets/files/docs/Asiakkaat/hankintaehdotukset.png)

Samalla sivulla voi myös tehdä asiakkaan puolesta hankintaehdotuksen.
Paina “Uusi hankintaehdotus” -nappia, jolloin avautuu lomake. Täytä
vähintään punaisella merkityt pakolliset tiedot ja paina sitten
lomakkeen alareunasta “Lähetä ehdotuksesi”.

![](/assets/files/docs/Asiakkaat/teeuusihankintaehdotus.png)

![](/assets/files/docs/Asiakkaat/teeuusihankintaehdotus2.png)

### 1.7.9. Lainat

Asiakkaan tietojen alapuolella on taulukkonäkymässä asiakkaan lainat,
maksut, varaukset ja rajoitukset. Lainoihin pääsee klikkaamalla
“Lainassa”-painiketta. Maksut välilehteä ei näy, jos asiakkaalla ei ole maksuja.

![](/assets/files/docs/Asiakkaat/lainat.png)

Tällä näytöllä näkyy myös asiakkaan huollettavien lainat Perheen lainat
-välilehdellä. Huollettavalla näkyy myös perheen sisarusten
lainat eli niiden henkilöiden lainat, joilla on sama takaaja.

![](/assets/files/docs/Asiakkaat/perheenlainat.png)

Lainoista on tarkemmin Koha-ohje suomeksi kohdassa 2.4. Asiakkaan lainat
