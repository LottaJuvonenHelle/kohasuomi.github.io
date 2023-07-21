---
title: 'Laskutustyökalu'
permalink: /dokumentaatio/laskutustyokalu/
redirect_from:
  - /theme-setup/
toc: true
---

Laskutustyökalulla voi tällä hetkellä luoda Finvoice- ja PDF-laskuja.

## Asennus ja päivitys

https://github.com/KohaSuomi/koha-plugin-overdue-tool/tree/21.11
!2021-08-16at09-14-35Lataaliitännäinen.png!

## Käyttöönotto

Käyttöönotto vaatii muutamien asetusten lisäämistä.

* Käyttöoikeudet: Laskuttajat tarvitsevat seuraavat käyttäjäoikeudet: Plugins->tool, updatecharges, edit_borrowers ja edit_items. 
*HUOM! Muista lisätä käyttäjä myös liitännäisen asetukseen "Sallitut käyttäjät" (Yleiset-asetukset)!*

Laskuja varten täytyy lisätä ilmoituspohja, ODUECLAIM, joihin sisältö laitetaan *finvoice-*, *print-*, tai *pdf*-viestityypin pohjalle (muita tyyppejä on mm. Sähköposti, Tekstiviesti). finvoice-pohjaan määritellään Finvoice-sanoman sisältö ja pdf-pohjaan PDF-lasku HTML-muodossa. E-kirjeitä varten tehdään viestipohja ODUECLAIM-viestipohjaan print-pohjaan. ODUECLAIM-pohjaa muokkaamalla voidaan laskea osoitetietoja oikeaan kohtaan, tämä vaatii hieman html/css-tuntemusta. Viestipohjista on esimerkit saatavilla "Githubista":https://github.com/KohaSuomi/koha-plugin-overdue-tool/tree/21.11/Koha/Plugin/Fi/KohaSuomi/OverdueTool/examples. [[Viestipohjissa käytettävät tägit]] kootusti.
!Screenshot2021-12-22at08-44-05.png!

* FINVOICE-sanomaa varten käytetään ODUECLAIM-viestipohjassa finvoice-pohjaa/osiota.
* PDF-tulostusta käytettäessä käytetään ODUECLAIM-viestipohjaa ja viestin sisältö laitetaan pdf-pohjaan/osioon. Muista tehdä tarvittaessa kaikki kieliversiot. 
* E-kirjeenä lähtevien laskujen sisältö laitetaan ODUECLAIM-viestipohjaan *Tuloste*-pohjaan/osioon. Pohjaan laitetaan vain varsinainen viestin sisältö, ei lähettäjän tai vastaanottajan yhteystietoja. Viestin aihe -kentästä otetaan kirjeen "otsikko", joka tulostuu oikeaan yläreunaan. Muista tehdä tarvittaessa kaikki kieliversiot. Jos kieliversioita ei ole määritetty, käytetään Oletus-kielen tietoja.

* Myöhästymisilmoituksiin tulee määritellä sarake laskuille. Tästä asetuksesta käytetään vain viivettä, jolla haetaan laskutettava materiaali. Jos kaikilla kirjastoilla on sama viive, voi tehdä vain oletussäännön. Viestipohjakin pitää valita, koska ilman sitä tallennus ei onnistu.
!Screenshot2022-01-19at09-18-36.png!

* Laskutustyökalu löytyy työkaluliitännäisistä.
!2021-08-13at13-26-37Työkalut.png!

* Työkalun asetuksissa voidaan säätää laskuja yleisellä ja laskutusryhmä kohtaisesti.
!laskutus-plugari-asetukset.png!

* Yleisissä asetuksissa voi määrittää seuraavia asioita:
  * _Laskuttava kirjasto_: toimiiko laskuttavana kirjastona lainaava kirjasto vai niteen omistava kirjasto.
  * _Näytä lainat eräpäivästä x kuukautta taaksepäin_: oletusasetus, kuinka vanhoja lainoja näytetään laskutustyökalussa.
  * _Jätä laskuttamatta lainat, jotka ovat yli x vuotta vanhat_: oletusasetus, kuinka vanhoja laskuttamattomia lainoja näytetään laskutustyökalussa.
  * _Laskutetun niteen "ei lainata"-tila_: määritä tähän laskutettavalle aineistolle asetettavan notforloan-tilan arvo. Se on aika yleisesti arvo 6.
  * _Sallitut käyttäjät (borrowernumberit pilkulla erotettuna)_: kirjoita tähän niiden käyttäjien borrowernumberit, joilla on oikeus päästä laskutustyökaluun. Pääsy kannattaa sallia vain oikeasti laskutusta tekeville.

* Ryhmäasetuksiin tulee näkyviin jokainen määritelty laskutusryhmä ja näkyvät asetukset ovat säädettävissä laskutusryhmäkohtaisesti.
  * laskutusryhmät määritetään liitännäisessä
  !luoryhma.png!
  * lisää kirjastot ryhmään alasvetovalikosta
  !ryhmankirjastot.png!

  * valitse ryhmän laskutustapa: Finvoice, E-lasku tai PDF-lasku
  !laskutustapa.png!
    * _Finvoice_ muodostaa laskuista finvoice-muotoisen xml-tiedoston, joka voidaan viedä kunnan laskutusjärjestelmään ja varsinaiset laksut lähetetään sieltä sitten asiakkalle.
    * _E-lasku_ muodostaa asiakkaille e-kirjeenä lähetettävän laskun. Tämä vaatii, että kimpassa on käytössä e-kirjeiden lähetyspalvelu.
    * _PDF-lasku_ muodostaa pdf-tiedoston/tiedostot, jotka laskuttaja voi itse tulostaa ja lähettää asiakkaille.


  * Laskutusryhmän yhteystietoihin voi lisätä tarpeelliset tiedot. HUOM! Tilinumero- ja BIC-tunnus-kentät ovat pakollisia kaikissa laskutusmuodoissa.
  !ryhmantiedot.png!

  * Viitenumerot voivat olla kiinteitä tai juoksevia, kiinteän voi lisätä suoraan ODUECLAIM-pohjaan. Kunnan laskuttajilta tulee saada tiedot viitenumeroiden tekemiseen. *Juoksevaa viitenumeroa varten tarvitaan kehittäjän apua, plugin_data-tauluun pitää lisätä laskutusryhmälle siemenluku mistä viitenumero lasketaan. Siemennumero tulee lisätä OverdueTool-plugille ja plugin_key-kentän arvo pitää alkaa "REFNO_"*
    * ```INSERT INTO plugin_data (plugin_class, plugin_key, plugin_value) values ("Koha::Plugin::Fi::KohaSuomi::OverdueTool", "REFNO_<laskutusryhmän nimi>", "<siemenluku>");```
    !viitenumero.png!

  * Rajoitus voidaan asetettaa joko vain huollettavalle tai halutessa myös huoltajalle.
    * Huomioi, että huoltajalle lisätty rajoite ei poistu automaattisesti, kun laskutetut aineistot palautetaan. Laskutettavalta asiakkaalta rajoite poistuu automaattisesti.
    !rajoitus.png!

  * Niteen hinnan voi lisätä asiakkaan maksuihin, mutta kannattaa huomioida, että jos käytössä on verkkokirjastossa verkkomaksumahdollisuus, asiakas voi vahingossa maksaa samat korvaushinnat sekä verkkomaksuna, että laskulla.
  !niteenhinta.png!

  * Laskutettavista niteistä syntyneet myöhästymismaksut voidaan myös lisätä laskulle. Tässäkin kannattaa ottaa huomioon, että jos kimpalla on verkkokirjastossa käytössä verkkomaksutoiminto, voi asiakas maksaa myöhästymismaksut vahingossa kahteen kertaan.
  !myohastymismaksut.png!

  * Jos laskutusryhmän laskuihin halutaan lisätä _Laskutuslisä_, syötä summa siihen tarkoitettuun kenttään.
  !laskutuslisa.png!

  * _Viesti asiakkaalle_ -kenttään voit määrittää, minkälainen viesti laitetaan laskutetun asiakkaan (aikuisasiakas tai huoltaja) tietoihin. (Samanlainen viesti, mikä tulee Lisää viesti -toiminnolla)
  !viestiasiakkaalle.png!

  * _Viesti huollettavalle tai virkaholhoojalle_ -kenttään voit määrittää huollettavalle tai virkaholhoojalle lisättävän viestin.
  !viestihuollettavalle.png!

  * _Muuta takaajakäsittely (asiakastyypit pilkulla eroteltuna)_ -kohdassa voi määrittää ne asiakastyypit, joilla on ns. virkaholhoojia. Jos tähän laitetaan asiakastyyppi, virkaholhoojan tiedot tallennetaan finvoice-sanomassa eriin kohtaan kuin se tapahtuisi "normaalissa" takaajakäsittelyssä. Tämä mahdollistaa laskutusjärjestelmissä virkaholhoojan tietojen viennin eri kenttiin kuin normaalitakaajan.
!takaajakasittely.png!


## Laskujen tekeminen

Laskutustyökalu löytyy Työkaluista kohdasta Työkaluliitännäiset. Se ajetaan valitsemalla Toiminnot-valikosta "Käynnistä työkalu".

!laskutusliit.png!

* Laskutettava aineisto haetaan aikaväliltä. Sivulle tultaessa aikaväli muodostuu automaattisesti myöhästymisilmoituksissa olevan viiveen ja työkalun asetuksissa olevan "Näytä lainat eräpäivästä n kuukautta taaksepäin"-asetuksen mukaan. Aikaväliä voi muuttaa tarvittaessa.
* Laskutettava aineisto näkyy kunkin asiakkaan alla, tiedot saa auki asiakkaan tiedoissa olevasta nuolesta.
* Laskutettavasta aineistoista voi vielä tässä vaiheessa muokata korvaushintaa tai jättää jonkun aineiston pois laskulta ottamalla ruksin pois niteen kohdalta. Aineisto jolle ei ole määritelty korvaushintaa jätetään alustavasti pois laskulta, jos hinnan lisää aineisto laskutetaan. Jos hintatietoa muokkaa, tallennetaan uusi hinta myös niteen tietoihin.
* Kun on tarkistanut laskutettavan aineiston tiedot voi siitä luoda PDF:n, elasku-viestin tai Finvoice-sanoman. Tämä riippuu mitkä pohjat on lisätty laskutusryhmälle. Laskun luonti lisää niteille asetuksissa määritellyn "Laskutettu"-tilan. Jos sivun lataa uudestaan niin juuri äsken laskutettu aineisto ei enää näy listassa. Sen saa näkyviin kun valitsee "Näytä laskutetut".
** PDF:n, elasku-viestin ja Finvoice-sanoman luontiin käytetään käyttäjän kirjautumiskirjaston viestipohjaa. Jos laskuttaa kerralla useamman kirjaston aineistoa, pitää kirjautua siihen kirjastoon, jolle on luotu ODUECLAIM- tai FINVOICE-pohjat. Yleensä tämä on kunnan pääkirjasto.
* Tuloksia voi myös suodattaa asiakasryhmän ja minimisumman mukaan. Minimisumma kannattaa säätää nollaan, jotta mukaan tulee myös ne asiakkaat, joiden laskutettavien niteiden kaikki korvaushinnat ovat nolla tai tyhjä.

!Screenshot2021-12-22at13-46-46.png!

* Ennen PDF:n tulostamista pääsee esikatselu-näkymään, missä näkee sivun asettelun.
!2021-08-16at08-48-47Laskutustyökalu.png!

* Lasku luodaan asiakkaan ilmoituksiin, jolloin siitä jää jälki järjestelmään. Finvoice-sanomat lähetetään eteenpäin ajastetusti, joten korjauksia voidaan tehdä ennen lähetystä.

## Laskutettujen palautus

Kun asiakkaan kaikki laskutetut niteet palautetaan, poistuu asiakkaalta rajoite. Jos osaa laskutetuista niteistä ei palauteta, jää rajoite paikalleen. Niteille jää laskutettu-tila ja asiakkaan tietoihin tieto (viesti), että hänelle on lähettetty lasku. Nämä tiedot pitää poistaa manuaalisesti.
