---
layout: single
permalink: /asiantuntijaryhma2023
hidden: true
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
toc: true
title: 'Koha-Suomen asiantuntijaryhmä 2023'
---

Tältä sivulta löydät Koha-Suomen asiantuntijaryhmän vuoden 2023 muistiot. Uusin muistio on aina ylimmäisenä.

Koha-Suomen asiantuntijaryhmään kuuluvat Leena Kinnunen (Lapin kirjasto), Piia Semenoff (OUTI-kirjastot), Päivi Knuutinen (Vaara-kirjastot), Katja Valjakka (Lumme-kirjastot), Tuomas Kunttu (Kyyti-kirjastot), Katri Sillgren (Helle-kirjastot), Susanna Sandell (Vaski-kirjastot). Koha-Suomesta mukana on puheenjohtajana Ari Mäkiranta ja asiantuntijoina Anneli Österman ja Kodo Korkalo.

Asiantuntijaryhmän valitsee kerran vuodessa Koha-Suomen hallitus.

## Asiantuntijaryhmän esityslista 4/23

Aika: 19.4.2023 klo 9<br />
Läsnä: Ari Mäkiranta (Koha-Suomi), Tuomas Kunttu (Kyyti), Päivi Knuutinen (Vaara), Kodo Korkalo (Koha-Suomi), Susanna Sandell (Vaski), Leena Kinnunen (Lappi), Kati Sillgren (Helle), Noora Valkonen (OUTI) ja Hanna Ikonen (Lumme)

### 1. Arin ajankohtaiset
* Harjoittelija Mikkelissä 1.4-31.5.
* Lastu-kirjastot halukkaita liittymään Koha-Suomeen.
### 2. Versionvaihdon tilanne

### 3. KohaPerlCon2023

[Call for papers](https://github.com/KohaSuomi/Koha/discussions/492) - ehdota aihetta KohaConiin.

### 4. Kehitysehdotusten läpikäyntiä

Käydään läpi vanhoja, käsittelemättömiä hankintaehdotuksia. Näiden jälkeen vanhoja käsiteltäviä kehitys ehdotuksia on vielä vajaa 50 kpl.

* [Tiketti 3876 - Asiakastiedot: vanhentunut Sotu-termi vaihtoon](https://tiketti.koha-suomi.fi/issues/3876)
* [Tiketti 3917 - Tilaustietuetta tehtäessä pitäisi kaikki tarvittavat MARC-kentät indikaattoreineen olla tehtävissä tilausten puolella](https://tiketti.koha-suomi.fi/issues/3917)
* [Tiketti 3918 - Uudesta tyhjästä tietueesta -toimintoon ean-koodi ja tuotetunnus](https://tiketti.koha-suomi.fi/issues/3918)
* [Tiketti 3919 - Hankintahinnan ja korvaushinnan pitäisi siirtyä tilitystiedoista niteen tietoihin](https://tiketti.koha-suomi.fi/issues/3919)
* [Tiketti 3923 - Uudesta tyhjästä tietueesta -toimintoon ikärajoitetun aineiston ikäraja](https://tiketti.koha-suomi.fi/issues/3923)
* [Tiketti 4084 - Työkalut/Asiakkaiden muokkaus eräajona -toimintoon lisää muokattavia kenttiä](https://tiketti.koha-suomi.fi/issues/4084)
* [Tiketti 4089 - Niteen poisto poistaa lainan asiakkaan lainahistoriasta](https://tiketti.koha-suomi.fi/issues/4089)
* [Tiketti 4133 - Kalenterin muokkaus: tietyn viikonpäivän kiinniolo tiettynä ajanjaksona -vaihtoehdon lisäys](https://tiketti.koha-suomi.fi/issues/4133)


### 5. Muut asiat

*kimpoista tarvitaan esitykset asiantuntijaryhmän kokoonpanoksi.
### 6. Seuraava kokous

Seuraava kokous on ke 24.5.2023 klo 9.

## Asiantuntijaryhmän muistio 3/23

Aika: 15.3.2023 klo 9<br />
Läsnä: Ari Mäkiranta (Koha-Suomi), Tuomas Kunttu (Kyyti), Päivi Knuutinen (Vaara), Kodo Korkalo (Koha-Suomi), Susanna Sandell (Vaski), Pia Kusmin (Lappi), Kati Sillgren (Helle), Anneli Österman (Koha-Suomi), Noora Valkonen (OUTI, liittyi mukaan kohdassa 5)

### 1. Arin ajankohtaiset

Kirkeksessä alkoi tieturvan vaikutusten arviointi -prosessi ulkopuolisen firman tekemänä. Koha-Suomi mukana teknisenä tukena.

### 2. Versionvaihdon tilanne

Next-kannat ovat kaikilla kimpoilla pystyssä ja Finna-nextit haravoitumassa. Vaskilla on next-kannassa koko tietokannan sisältö, mutta muille kimpoille (ja Tätiin) tietoja on redusoitu vähemmäksi palvelimen tilakapasiteetin vuoksi. Pääkäyttäjät testaavat sekä yleisesti toimintoja että Koha-Suomen omia toimintoja sitä mukaa, kun niitä valmistuu. Tulossa tarkempaa tiedotusta versionvaihdosta Koha-Suomen puolelta.

### 3. PIN-koodien pituus

PIN-koodien pituus ei ole tietoturvan kannalta optimaalinen. Mitä voitaisiin tehdä, että sen saisi pidemmäksi? - Susanna/Vaski

**Päätös:** Vaski kysyy Mikro-Väylältä ja Bibliothecalta ja OUTI Lyngsoelta tukeeko heidän laitteensa yli neljä merkkistä pin-koodia. Jos kaikki tukee, muutetaan Kohassa pin-koodin generointia (JS-rimpsu) tuottamaan pidempiä pinejä. Jos jossakin on muiden toimittajien automaatteja, olkaa yhteydessä niiden toimittajaan ja selvittäkää niiden tilanne.

### 4. Action_logs-taulujen siivous kuukausittain

Action_logs-taulut siivotaan tällä hetkellä kerran vuodessa ja tiedot siirretään aktiivisesta taulusta arkistotauluun. Taulu on kuitenkin kasvanut osassa kimpoista niin isoksi, että siivousajo kestää todella pitkään ja lokitaulu on sen aikaa pois käytöstä. Koha ei toimi tällöin, koska moni toiminto kuten varausten tekeminen tai lainojen uusiminen lokitetaan ja kirjauksia ei voi tehdä, kun tauluun ei pysty kirjoittamaan. 

Koha-Suomi ehdottaa, että siivousajo tehtäisiin jatkossa kerran kuukaudessa ja arkistoon siirretään aina reilun vuoden takainen kuukausi, esim. maaliskuussa 2023 siirretään arkistoon helmikuu 2022. Ehdotuksesta keskusteltiin pääkäyttäjien viikon 11 palaverissa, eikä siellä huomattu ongelmia asian suhteen. Tiedot pystyy tarvittaessa hakemaan arkistotauluista SQL-kyselyillä.

**Päätös:** Siivotaan jatkossa action_logs-taulu kerran kuussa ja siirretään arkistotauluun vuotta vanhemmat merkinnät. Säilytysaika jatkossa siis yksi vuosi aktiivisessa taulussa.

### 5. Kehitysehdotusten läpikäyntiä

Keskustellaan myös kehitysehdotusten määrästä ja kuinka paljon niiden käsittelyyn kuluu aikaa. Kehitysehdotuksia toivotaan edelleen tehtävän, mutta toiveena olisi, että niiden toteutuskelpoisuutta pohdittaisiin nykyistä tarkemmin jo ennen kehitysehdotuksen tekemistä. Ehdotusten läpikäyntiin kuluu tällä hetkellä paljon aikaa useilta henkilöiltä. Alla on taulukko GitHubissa olevien kehitysehdotusten määrästä. GitHub otettiin käyttöön lokakuussa 2022 ja mukana on muutamia Redminestä siirrettyjä ehdotuksia.

Tekijä | Kehitysehdotusten määrä Githubissa
--- | ---
Helle | 24
Koha-Suomi |	12
Kuvailuryhmä | 4
Kyyti | 3
OUTI | 14
Vaara | 6
Vaski | 11
Yhteensä | 74

**Päätös**: Ehdotetaan seuraavaa toimintatapaa: Kun kimpan henkilökunnalta tulee kehitysehdotus, pohditaan ensin kimpan pääkäyttäjien (tai muun pienryhmän) kesken, onko ehdotus hyvä ja tarpeellinen toteuttaa. Jos on, kimpan pääkäyttäjä esittää sen pääkäyttäjien viikkopalaverissa. Jos ehdotus koetaan sielläkin hyväksi, tehdään ehdotus Githubiin.

**Käsiteltävät ehdotukset**

Päätökset kirjattiin jokaiseen tikettiin kommenttina.

* [Tiketti 3924 - Uudesta tyhjästä tietueesta -toimintoon teoksen pääkieli](https://tiketti.koha-suomi.fi/issues/3924)
* [Tiketti 3927 - Huomautus (näkyy verkkokirjastossa) - näkyy huonosti henkilökunnalle](https://tiketti.koha-suomi.fi/issues/3927)
* [Tiketti 3966 - Asiakastiedot/Perheen lainat -välilehdellä lainojen uusintamahdollisuus](https://tiketti.koha-suomi.fi/issues/3966)
* [Tiketti 3985 - Kausijulkaisun vastaanottoon Lisää tulostuslistaan -valintamahdollisuus](https://tiketti.koha-suomi.fi/issues/3985)
* [Tiketti 3990 - Luettelointi ja 084a-kenttä ja YKL-luokkalistaus](https://tiketti.koha-suomi.fi/issues/3990)
* [Tiketti 4005 - Tietokannan tietojen siivousautomatiikkaa](https://tiketti.koha-suomi.fi/issues/4005)
* [Tiketti 4028 - Tarkka haku: YSOn termit Asiasana-haun avuksi, kun YSOn aika on](https://tiketti.koha-suomi.fi/issues/4028)
* [Tiketti 4081 - Ei uusintaa, jos uusi eräpäivä on sama kuin vanha](https://tiketti.koha-suomi.fi/issues/4081)

### 6. Muut asiat

Oppilaitosharjoittelija todennäköisesti tulossa Mikkeliin huhti-toukokuussa.

### 7. Seuraava kokous

Ke 19.4.2023 klo 9.

## Asiantuntijaryhmän muistio 2/23

Aika: 20.2.2023 klo 9.00<br />
Läsnä: Anneli Österman, Leena Kinnunen (Lappi), Tuomas Kunttu (Kyyti), Päivi Knuutinen (Vaara), Ari Mäkiranta, Piia Semenoff (OUTI), Kati Sillgren (Helle), Susanna Sandell (Vaski), Kodo Korkalo

### 1. Arin ajankohtaiset

Versionvaihdon testipalvelimia valmistellaan. Raportointipalvelun kanssa on haasteita palvelimien kanssa. Ne on siirtymässä uudelle palvelimelle.
Kirkes etenee hyvin, käyttöönotto sovittu syyskuulle 2023. Konversio 4.-11.2023.

### 2. Varausten oletusvoimassaoloaika

Teokset tilataan nykyään paljon ennen kuin ne ilmestyvät ja jos ilmestyminen viivästyy voi käydä niin, että asiakkaiden varaukset ehtivät kahdessa vuodessa vanhentua ja poistua ennen kuin saavat varaamansa teoksen. Ongelmaa helpottaisi vähän oletusvoimassaoloajan muuttaminen kolmeksi vuodeksi. Muutos pitäisi tehdä sekä Kohan asetuksiin että Finnaan.

**Päätös**: Muutetaan oletusvoimassaoloaika kolmeksi vuodeksi. Ajetaan olemassa oleville varauksille yksi vuosi lisää voimassaoloaikaa. Finnaan tehtävä muutos oletusvoimassaolokaikaan, OUTI hoitaa pyynnön kaikkien puolesta Finna-toimistoon.

### 3. Kehitysehdotus-tikettien työnkulku

Kehitysehdotus-tikettien työkulku on kuvattu sanallisesti ja vuokaaviona (pdf) [Tikettien työnkulku -wikissä](https://github.com/KohaSuomi/Koha/wiki/Tikettien-ty%C3%B6nkulku#kehitysehdotukset). Käydään läpi.

Pari pientä täsmennystä pyydetään vielä kaavioon Larilta. Päivitetään Tikettien työnkulku -sivulle uusi versio, kun se valmistuu.

### 4. Kehitysehdotusten läpikäyntiä

Käytiin läpi alla listatut tiketit ja kirjattiin päätös jokaiseen tikettiin erikseen.
* [4162](https://tiketti.koha-suomi.fi/issues/4162)
* [4174](https://tiketti.koha-suomi.fi/issues/4174)
* [4185](https://tiketti.koha-suomi.fi/issues/4185)
* [4209](https://tiketti.koha-suomi.fi/issues/4209)
* [4212](https://tiketti.koha-suomi.fi/issues/4212)
* [4223](https://tiketti.koha-suomi.fi/issues/4223)
* [4226](https://tiketti.koha-suomi.fi/issues/4226)
* [4242](https://tiketti.koha-suomi.fi/issues/4242)
* [4245](https://tiketti.koha-suomi.fi/issues/4245)
* [4257](https://tiketti.koha-suomi.fi/issues/4257)
* [4366](https://tiketti.koha-suomi.fi/issues/4366)
* [4461](https://tiketti.koha-suomi.fi/issues/4461)
* [4467](https://tiketti.koha-suomi.fi/issues/4467)
* [4569](https://tiketti.koha-suomi.fi/issues/4569)
* [5620](https://tiketti.koha-suomi.fi/issues/5620)


### 5. Uuden version ominaisuudet

Uudemmassa Koha-versiossa on muutamia ominaisuuksia, joiden käyttöönotosta olisi hyvä tehdä yhteinen päätös. Suurin osa uusista ominaisuuksista on kuvattu versionvaihdon repositorioon [Uutta-wikiin](https://github.com/KohaSuomi/Koha-22x/wiki/Uutta).

#### 5.1 Kaksivaiheinen kirjautuminen superlibrarian-tunnuksille?

Koha tukee jatkossa kaksivaiheista kirjautumista ja se olisi periaatteessa hyvä ottaa käyttöön ainakin superlibrarian-oikeuksilla olevilla tunnuksilla. Vaatii puhelimeen jonkin authenticator-sovelluksen. Ongelmana, että kaikilla pääkäyttäjillä ei ole henkilökohtaista älytyöpuhelinta.

**Päätös**: testataan toimintoa vielä tarkemmin. Miten toimia esim., jos esim. puhelin jää kotiin. Kuinka monella pääkäyttäjällä on työälypuhelin? OUTIssa selvitellään, onnistuuko tokenin liittäminen Kohan kaksivaiheiseen tunnistautumiseen.

### 6. Seuraava kokous

Ke 15.3.2023 klo 9.

## Asiantuntijaryhmän muistio 1/23

Aika: 16.1.2023 klo 9.00<br />
Läsnä: Ari Mäkiranta, Leena Kinnunen, Katri Sillgren, Päivi Knuutinen, Noora Valkonen, Tuomas Kunttu, Susanna Sandell, Katja Valjakka, Kodo Korkalo, Anneli Österman

### 1. Arin ajankohtaiset

* Huoltokatkossa vaihdettiin vialliset muistikammat palomuuri-laitteita lukuunottamatta. Niille kammat vaihdetaan seuraavassa huoltokatkossa.
* Versionvaihdon uudet testikannat on työn alla. Ongelmana on, ettei tila riitä kolmansille kannoille kaikille. Ratkaisu on työn alla.
  * Vaski, johon viedään kaikki data saataneen tällä viikolla toimintaan.
* actionlogs-taulun vuositauluihin vienti oli jumiutunut ja se jouduttiin keskeyttämään. Vaskin ja Lapin Kohat eivät toimineet sunnuntaina ennen kyselyjen keskeyttämistä n. klo 10.30.

### 2. Finna-kehitysehdotukset

Olisiko olemassa parempaa tapaa hallinnoida Finnaan liittyviä kehitysehdotuksia kuin nykyiset listaukset? /Susanna.

[Käsittelemättömät kehitysehdotukset](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/K%C3%A4sittelem%C3%A4tt%C3%B6m%C3%A4t_kehitysehdotukset)<br />
[Kansalliskirjastolle toimitetut kehitysehdotukset](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Kansalliskirjastolle_esitetyt_kehitysehdotukset)

**Päätös:** Pääkäyttäjäryhmä käsittelee jatkossa Finna-kehitysehdotukset. Tehdään uusi repositorio Finna-tiketeille. Ehdotuksen tekijä lähettää ehdotuksen Kansalliskirjastolle ja ylläpitää sen statusta meidän repositoriossa. Pääkäyttäjäryhmä käy läpi vanhat ehdotukset ja tekee keskeneräisistä uudet tiketit Finna-repositorioon.

### 3. Infoboksin piilotuksen poisto

Asiakas-sivulla on piilotettu vasemmasta reunasta ns. infoboksi, jossa on asiakkaan tiedot lyhyesti. Samassa boksissa näytetään, jos asiakkaan tili on lukittu liian monen epäonnistuneen kirjautumisen vuoksi. Pitäisikö piilotus poistaa, jotta lukitustieto saadaan näkyville? Jos piilotus poistetaan, kannattaa järjestelmäasetus HidePersonalPatronDetailOnCirculation olla "päällä". Asetuksella määritetään, näytetäänkö boksissa asiakkaan yhteystiedot vai ei. Jos yhteystiedot piilotetaan, on näkymä seuraavanlainen:
![kuva](https://user-images.githubusercontent.com/33121325/210208396-da1003b8-f863-425a-a46e-8e2ac91e72d5.png)

**Päätös:** Poistetaan piilotus ja laitetaan kaikille päälle HidePersonalPatronDetailOnCirculation, jos se ei ole päällä. Ohje pääkäyttäjien vkon 3 kokoukseen.

### 4. Tiekartan päivitys

Käydään läpi Koha-Suomen tiekartan tilanne ja päivitetään se ajantasalle.

* [TiekarttaTammikuu2023.pdf](https://github.com/KohaSuomi/kohasuomi.github.io/files/10400021/TiekarttaTammikuu2023.pdf)
* [Tiekartta2023tammikuu.xlsx](https://github.com/KohaSuomi/kohasuomi.github.io/files/10424123/Tiekartta2023tammikuu.xlsx)

Tiekartta päivitetty.

### 5. Kehitysehdotusten läpikäyntiä

Käydään läpi alla mainitut kehitysehdotukset ja päätetään, toteutetaanko ne vai ei. Päätös kirjattu tikettiin. Avataan tarvittavat tiketit GitHubiin ja Bugzillaan.

* [216](https://github.com/KohaSuomi/Koha/issues/216)
* [233](https://github.com/KohaSuomi/Koha/issues/233)
* [2](https://github.com/KohaSuomi/koha-plugin-OKM-stats/issues/2)
* [5434](https://tiketti.koha-suomi.fi/issues/5434)
* [5440](https://tiketti.koha-suomi.fi/issues/5440)
* [5493](https://tiketti.koha-suomi.fi/issues/5493)
* [5494](https://tiketti.koha-suomi.fi/issues/5494)
* [5525](https://tiketti.koha-suomi.fi/issues/5525)
* [5562](https://tiketti.koha-suomi.fi/issues/5562)
* [5566](https://tiketti.koha-suomi.fi/issues/5566)
* [5577](https://tiketti.koha-suomi.fi/issues/5577)
* [5588](https://tiketti.koha-suomi.fi/issues/5588)
* [5589](https://tiketti.koha-suomi.fi/issues/5589)
* [5609](https://tiketti.koha-suomi.fi/issues/5609)

### 6. Työryhmien vuosisuunnitelmat

Käytiin läpi asiantuntijaryhmän vuosisuunnitelma.

[Asiantuntijaryhmän vuosisuunnitelma 2023](https://github.com/KohaSuomi/kohasuomi.github.io/files/10424108/Asiantuntijaryhman_vuosisuunnitelma2023.pdf)

### 7. Muut asiat

**Webkake-sopimukset**
* Webkake on käytössä Lappi, Vaara (Joensuu), OUTI (Oulu), Kyyti, Lumme (Mikkeli), Helle. 
* Hakosalon Jukalta tulossa sopimusluonnos, jota halukkaat voivat yhdessä käsitellä.

### 8. Seuraavat kokoukset

* ma 20.2.2023 klo 9
* ke 15.3.2023 klo 9
* ke 19.4.2023 klo 9
* ke 24.5.2023 klo 9
