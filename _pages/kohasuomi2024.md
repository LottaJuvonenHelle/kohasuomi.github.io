---
title: 'Koha-Suomen vuoden 2024 muistiot'
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
permalink: /kohasuomi2024
redirect_from:
  - /theme-setup/
toc: true
layout: single
hidden: true
---

Koha-Suomen henkilökunta kokoontuu kerran viikossa pidempään palaveriin ja päivittäin 15 minuutin pikapalaveriin. Muistio kirjoitetaan vain maanantain pidemmästä palaverista. Uusin muistio on aina ylimmäisenä.

## Viikko 4

Aika: 22.1.2024 klo 9<br/>
Läsnä: Anneli, Lasse, Pasi, Johanna, Emmi, Ari, Kassu, Kodo

**Asiat**
* Versionvaihdon tikettien katsaus? /Emmi
  * otetaan katsaus keskiviikkona klo 10.30.
* [Käännöstoive: asiakastakaajan lisäys ja select-nappi](https://github.com/KohaSuomi/Koha/issues/1014)
  * Viedään koodimuutokset yhteisöön ehdolle, ei tuoda itselle väliaikaisesti.
* Vkon 4 päivitys
  * mukaan tulossa vain yksi käännösmuutos
* Scrum:
  * Kodo: Tiedot lastun konversiotauluja varten metsästelty dumpista (tietue-id:t), Lastu konversiota, Vaaran mobiiliappi testissä, Kotkan RFID-haravakuviossa ei vielä etenemistä
  * Emmi: Nextit redusoitu ja valmiina testattavaksi
  * Johanna: RDA-konversio, Kansalliskirjasto päivittänyt konversiosäännöt
  * Pasi: Odottavien tikettien tekoa
  * Lasse: Varaussivun sivutus ja versionvaihdon tikettejä
  * Anneli & Kassu: Vanhennettujen maksujen uudelleenkertymisongelman selvittelyä
  * Lari: Vanhennettujen maksujen uudelleenkertymisongelman selvittelyä

## Viikko 3

Aika: 15.1.2024 klo 9<br />
Läsnä: Ari, Anneli, Kodo, Pasi, Lari, Lasse, Johanna, Kassu

**Asiat**
* Vkon 3 päivitys
  * [Siirtoraportilla tiedot menevät päällekkäin](https://github.com/KohaSuomi/koha-plugin-exporter-report/issues/2)
  * [Hae tietokannasta -haku ei unohda haun rajaukseen käytettyä fasettivalintaa Nykyinen paikka, kun hakutulosnäytöllä tehdään uusi Hae tietokannasta](https://github.com/KohaSuomi/Koha/issues/667)
  * [Koriin linkki teokseen verkkokirjastossa](https://github.com/KohaSuomi/Koha/issues/883)
  * [Nimekkeen katkaisu laskutuksessa vain Finvoice-sanomille](https://github.com/KohaSuomi/koha-plugin-overdue-tool/issues/7)
  * [Käännösmuutostoive: asiakastietojen yhteenvedon alaotsikko Odottavat varaukset](https://github.com/KohaSuomi/Koha-translations/issues/31)
  * [Hyllyvarausraportista katosi julkaisuvuosi](https://github.com/KohaSuomi/Koha/issues/1009)
  * [Viestitaulun lukitus kaataa Kohan](https://github.com/KohaSuomi/Koha/issues/1002)
* Bugiperjantai /Anneli
  * Katsotaan tiistaina 
* Keskiviikon Järvenpään tietovarantopalsu, ketä osallistumassa?
  * Kodo selvittää 
* Statuksettomien tikettien läpikäynti
* Scrum
  * Kodo: Plack-workerien restart muutos --graceful-vipu testissä
  * Kassu: uusien tikettien selvittelyä
  * Anneli: versionvaihdon valmistelua, tiedote päivityksestä 
  * Pasi: MARC-virheraportti hakee Nalkuttimen asetuksista skipattavat kentät. Sanaston rapsat valmiit.
  * Lasse: varaussivun sivutus
  * Lari: selvittelyä miksi batchrebuildbiblios-ajot ei mene läpi
  * Johanna: RDA, ruotsinkielisten tietueiden erottelu

## Viikko 2

Aika: 8.1.2024 klo 9<br />
Läsnä: Lari, Kodo, Pasi, Ari, Johanna, Lasse, Kassu, Anneli

**Asiat**
* Statuksettomien tikettien läpikäynti
  * ehdittiin käydä noin puolet, loput ensi viikolla.
* Elasticsearch-päivitys
  * Elasticsearch-pluginit eivät päivity käyttöjärjestelmän päivityksessä. Lukitaan Elasticsearch-versio paketinhallinnassa tulevaisuudessa.
* Viikon 2 päivitys
  * 2 muutosta tulossa.  

[Palaa viikon muistion alkuun](https://koha-suomi.fi/kohasuomi2024#viikko-2) - [Palaa sivun alkuun](/kohasuomi2024)

## Viikko 1

Aika: Keskiviikko 3.1.2024 klo 12<br />
Läsnä: Emmi, Anneli, Kodo, Ari, Pasi, Lari, Lasse

**Asiat**
* [BTJ-linkkien korjaus](https://github.com/KohaSuomi/Koha/issues/982) / Anneli
  * jos työ on tehtävissä erätyökaluilla, kimpat tekevät työn itse 
* [005-kentän päivittyminen lainattaessa](https://github.com/KohaSuomi/Koha/issues/924) jäänyt vastuuttamatta / Emmi
  * Pasi hoitaa. 
* Kuinka usein nolla-branchiin päivitetään yhteisöön tulleet muutokset? Aina kun uusi stable release julkaistaan vai harvemmin? / Emmi
  * Seuraillaan vielä miten nolla-branchin kanssa pärjäillään ja tehdään sitten tarkempi päätös.
* Terrapin-paikat ja nykytilanne / Kodo
* Ensi viikon huolto, RedMinen sulkeminen, Multipath-murhe / Kodo
  * mm. tuotantojen käyttiksien päivitys, [huoltotiedotteessa](https://github.com/KohaSuomi/Koha/discussions/993) tarkemmin
  * [Redmine kiinni](https://github.com/KohaSuomi/Koha/discussions/994) samaan aikaan
* Varmuuskopioiden tarkistus pois päältä ajastusongelman vuoksi 
* Lastun kuulumiset ja dumppi / Kodo 
* [Nidehaun tulosten järjestäminen julkaisuvuoden mukaan ei toimi oikein](https://github.com/KohaSuomi/Koha/issues/693) aikataulutus vkon 2 pääkäyttäjäpalsua varten.
  * pääkäyttäjät hoitavat uudelleenmäppäykset (ja raporttien päivitykset)
* Scrum:
  * Kodo: ei ihmeempiä yllä olevien lisäks
  * Pasi: sanasto, nextien redusointi
  * Lasse: pluginien testailua versionvaihtoa varten
  * Lari: varausten noutomuistutusajo
  * Emmi: indeksistä poistumattomien tietueiden selvittelyä
  * Anneli: versionvaihdon ominaisuuksien kirjaamista ylös, tilastojen päivitystä    

[Palaa viikon muistion alkuun](https://koha-suomi.fi/kohasuomi2024#viikko-1) - [Palaa sivun alkuun](/kohasuomi2024)
