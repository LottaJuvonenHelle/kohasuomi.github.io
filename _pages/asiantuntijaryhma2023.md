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

Koha-Suomen asiantuntijaryhmään kuuluvat Leena Kinnunen (Lapin kirjasto), Noora Valkonen (OUTI-kirjastot), Päivi Knuutinen (Vaara-kirjastot), Katja Valjakka (Lumme-kirjastot), Tuomas Kunttu (Kyyti-kirjastot), Katri Sillgren (Helle-kirjastot), Susanna Sandell (Vaski-kirjastot). Koha-Suomesta mukana on puheenjohtajana Ari Mäkiranta ja asiantuntijoina Anneli Österman ja Kodo Korkalo.

Asiantuntijaryhmän valitsee kerran vuodessa Koha-Suomen hallitus.

## Asiantuntijaryhmän esityslista 2/23

Aika: 20.2.2023 klo 9.00<br />
Läsnä:

### 1. Arin ajankohtaiset

### 2. Varausten oletusvoimassaoloaika

Teokset tilataan nykyään paljon ennen kuin ne ilmestyvät ja jos ilmestyminen viivästyy voi käydä niin, että asiakkaiden varaukset ehtivät kahdessa vuodessa vanhentua ja poistua ennen kuin saavat varaamansa teoksen. Ongelmaa helpottaisi vähän oletusvoimassaoloajan muuttaminen kolmeksi vuodeksi. Muutos pitäisi tehdä sekä Kohan asetuksiin että Finnaan.

### 3. Kehitysehdotus-tikettien työnkulku

Kehitysehdotus-tikettien työkulku on kuvattu sanallisesti ja vuokaaviona (pdf) [Tikettien työnkulku -wikissä](https://github.com/KohaSuomi/Koha/wiki/Tikettien-ty%C3%B6nkulku#kehitysehdotukset). Käydään läpi.


### 4. Kehitysehdotusten läpikäyntiä

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
* [4366](https://tiketti.koha-suomi.fi/issues/4366) - onko vielä ajankohtainen?
* [4461](https://tiketti.koha-suomi.fi/issues/4461)
* [4467](https://tiketti.koha-suomi.fi/issues/4467)
  * [Vaski-testi](https://vaski-test.koha-suomi.fi/)
* [4569](https://tiketti.koha-suomi.fi/issues/4569)
* [5620](https://tiketti.koha-suomi.fi/issues/5620)



### 5. Uuden version ominaisuudet

Uudemmassa Koha-versiossa on muutamia ominaisuuksia, joiden käyttöönotosta olisi hyvä tehdä yhteinen päätös. Suurin osa uusista ominaisuuksista on kuvattu versionvaihdon repositorioon [Uutta-wikiin](https://github.com/KohaSuomi/Koha-22x/wiki/Uutta).

#### 5.1 Kaksivaiheinen kirjautuminen superlibrarian-tunnuksille?

Koha tukee jatkossa kaksivaiheista kirjautumista ja se olisi periaatteessa hyvä ottaa käyttöön ainakin superlibrarian-oikeuksilla olevilla tunnuksilla. Vaatii puhelimeen jonkin authenticator-sovelluksen. Ongelmana, että kaikilla pääkäyttäjillä ei ole henkilökohtaista älytyöpuhelinta.

### 6. Seuraava kokous

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
* Webkake on käytössä Lappi, Vaara (Joensuu), OUTI (Oulu), Kyyti, Lumme (Mikkeli). 
* Hakosalon Jukalta tulossa sopimusluonnos, jota halukkaat voivat yhdessä käsitellä.

### 8. Seuraavat kokoukset

* ma 20.2.2023 klo 9
* ke 15.3.2023 klo 9
* ke 19.4.2023 klo 9
* ke 24.5.2023 klo 9
