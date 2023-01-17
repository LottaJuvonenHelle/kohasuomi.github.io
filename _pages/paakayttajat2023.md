---
layout: single
permalink: /paakayttajat2023
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
toc: true
title: 'Koha-Suomen pääkäyttäjäryhmän muistiot 2023'
---

Koha-Suomen pääkäyttäjäryhmä kokoontuu kerran viikossa. Ylimmäisenä on aina uusin muistio.

## Viikko 3 muistio

Aika: 17.1.2023 klo 9.15<br />
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Anneli Österman, Emmi Takkinen, Tuomas Kunttu (Kyyti)

**Yhteiset**
* Kohan ohje suomeksi -muotoilujen yhtenäistäminen?
  * työryhmä miettii yhtenäiset muotoiluohjeet: Päivi, Tuomas, Anneli
  * jos joku vielä haluaa mukaan, ilmoita Annelille.
* [Viikon 3 päivitys](https://github.com/KohaSuomi/Koha/discussions/369)
* Githubin esittelyvideot [kaikille](https://youtu.be/cPVSi2xFBIQ) - [pääkäyttäjille](https://youtu.be/J-lzJv7ginE)
* [Kirkesin järjestelmäasetusten läpikäynti, osa 1](https://youtu.be/lyETIF-Xd2Y)
* Tilastoinnissa virhe [KPOKM-5](https://github.com/KohaSuomi/koha-plugin-OKM-stats/issues/5) /Emmi
  * Emmi korjaa virheen ja tiedottaa, kun tilastot on luotu uudelleen.
  * Tätissä on [SQL-kysely](https://tati.koha-suomi.fi/cgi-bin/koha/reports/guided_reports.pl?phase=Run+this+report&reports=243&limit=200), jolla voi hakea tietueet, joissa luokka alkaa kirjaimella. 
* Redmineen kirjautuminen otetaan pois päältä muilta kuin pääkäyttäjiltä.
* [Asiantuntijaryhmän kokous](https://koha-suomi.fi/asiantuntijaryhma2023#asiantuntijaryhm%C3%A4n-muistio-123)
  * [Finna-kehitysehdotukset](https://koha-suomi.fi/asiantuntijaryhma2023#2-finna-kehitysehdotukset)
  * [Infoboksin piilotuksen poisto](https://koha-suomi.fi/dokumentaatio/intranetusercss/#asiakkaan-tietoruudun-piilotus-asiakastiedoista-vasemmasta-reunasta)
    * Tarkista, että HidePersonalPatronDetailOnCirculation asetus on päällä

**Vaara**
* Tuplaverkkomaksuja oli lopulta vain kourallinen, neljä oikeasti tuplasti maksettuja (suuruudeltaan 1,80-5,25 euroa). Toivotaan, että näitä ei tule enempää.
* Joensuun kaupunki ilmoitti perjantaina iltapäivällä, että Ceepos-kassaan kirjautuminen muuttuu (kysyy käyttäjätunnusta). Tieto ei tietenkään kulkeutunut lauantaina työskenteleville, joten kassa pysyi kiinni. Täytyy antaa palautetta muutosten ajankohdan suunnittelusta.

**Lumme**
* Varkaudessa huomattiin OKM tilaston epäonnistuminen vuodelta 2022. Kehittäjät korjaavat tilastot maanantaihin 23.1. mennessä.
* Normaalia ylläpitoa.

**Kyyti*
* CD-levyjen laina-aikaa pidennettiin 28 vuorokauteen viime viikolla.
* Haminan kaupunki on toteuttanut mobiiliapplikaation, jossa on myös sähköinen kirjastokortti sekä tiedonhaku, varaus ja lainojen uusinta. Rajapinta Kohaan on tehty. Löytyy sovelluskaupoista Hamina-haulla.


## Viikko 2 muistio

Aika: 10.1.2023 klo 9.15<br />
Läsnä: Anni Rajala (Vaski), Leena Kinnunen ja Pia Kusmin (Lappi), Heli Auranen, Timo Pesonen (Lumme), Reetta Pihlaja (Siilinjärvi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Veli-Pekka Marjoniemi (OUTI), Tuomas Kunttu (Kyyti), Anneli Österman ja Kodo Korkalo (Koha-Suomi), Johanna Miettunen (3AMK), Kati Sillgren (Helle)

**Yhteiset**
* [Vkon 2 päivitys](https://github.com/KohaSuomi/Koha/discussions/357)
* Keskiviikon huoltokatko / Kodo
  * Huoltokatkon aikana vaihdetaan viallisia muistikampoja. [Toimintasuunnitelma](https://koha-suomi.fi/kohasuomi2023#tammikuun-huoltokatkon-toimintasuunnitelma) 
* Keskiviikon Kirkes-kimpan järjestelmäasetuskoulutus siirretty puoli tuntia myöhemmäksi ja Jitsiin. Uusi aika ja paikka päivitetty [koulutustiedotteeseen](https://github.com/KohaSuomi/Koha/discussions/320).

**Vaski**
* Vaski-tasoinen kellutuskokeilu aloitettu eilen, kokeilussa kellutetaan vain musiikki cd:itä.
* Havaittu, että tilaussanoman käsittely epäonnistunuu välillä ensimmäisellä yrityksellä (https://github.com/KohaSuomi/Koha/issues/353). Tätä saatu jo selviteltyä ja liittyy ilmeisesti ElasticSearch-ongelmaan.


**Lappi**
* Ylimääräisiä tuplasti veloitettuja maksuja 37 kpl, muutama Finnasta ja enemmän Kemin Ceepokselta. Liittynee tikettiin #351
* Muistutettu varalainausjärjestelmästä, suositeltu KOCT:ia. Yhdellä tunnuksella pääsy ei onnistu. 
* SMS-numeron siirto Finnasta Kohaan toimii, korjattu myös mobiilinumeron kopioituminen mobile-kentästä sms-kenttään
* Kerätään kysymyksiä, ei toimivia ja toimivia juttuja Kohasta käyttäjiltä helmikuun lopun Kysy Kohasta-webinaariin
* Virkailijaoikeuksia tarkistettu, mutta ongelmana  raportit, jotka antavat liikaa tietoa

**Lumme**
* vanhentuneet varaukset eivät poistu - satunnainen mutta toistuva ongelma#356. Tehty tiketti 9.1., Emmi hoitaa asiaa
* Asiakkaalla näkyi Palautusilmoitukset välilehdellä palautusilmoituksia. Väittää palauttaneensa toiminto (https://tiketti.koha-suomi.fi/projects/versionvaihto/wiki/Uusia_ominaisuuksia#Ilmoittaa-palauttaneensa-toiminto). Piilotus Intranetusercss  /*Piilotetaan asiakastietojen sivulla näkyvä 'Palautusilmoitukset' nappula (eng. 'Claims')*/ ul.nav.nav-tabs li a#return-claims-tab { display:none;}

**Siilinjärvi**
* ei mainittavaa

**Vaara**
* Myös Vaarassa tuplasti veloitettuja/kuitattuja maksuja eli asiakkailla plussaldoa.
* Muuten normaalia ylläpitoa.

**OUTI**
* OUTIssa myös tuplasti veloitettuja maksuja, asia selvityksessä.
* Henkilökunnalta kyselyä liittyen ongelmiin kausijulkaisujen vastaanottamisessa tilauskauden päättymisen jälkeen. Ratkaisuna tilauskauden jatkaminen.
* Muuten normaalia ylläpitoa.

**Kyyti**
* Keskusteltiin pitkään maksuista, jotka asiakkaat ovat maksaneet kahteen kertaan Finnassa. Toistaiseksi näitä lienee syytä seurata raporteilla.
* CD-levyjen laina-aika muuttuu. Tehty tiketti #358 nidetyyppimuutokselle.

**Helle**
* Koha-näytön yläreunaan lisätyt omat linkit eivät ole enää päällekkäin pienemmillä näytöillä, kun osa omista linkeistä niputettiin samaan alasvetovalikkoon. 

## Viikko 1 muistio

Aika: 3.1.2023 klo 9.15<br />
Läsnä: Päivi Knuutinen ja Auli Rantasalo (Vaara), Heli Auranen, Katja Valjakka, Timo Pesonen (Lumme), Reetta Pihlaja (Siilinjärvi), Piia Semenoff ja Veli-Pekka Marjoniemi (OUTI), Anni Rajala (Vaski), Leena Kinnunen, Pia Kusmin (Lappi)

**Yhteiset**
* Tikettien label "enhancement" on jaettu "kahtia", jotta erottaa paremmin ne kehitysehdotukset, joiden kehitys on asiantuntijaryhmässä päätetty tehdä yhteisössä oman työn sijaan.
  * local enhancement -> kehitys tehdään itse
  * community enhancement -> kehitysehdotus viedään yhteisön bugzillaan.
    *  työnjakoasia: voisiko alkuperäinen tiketin tekijä tehdä bugi-ilmoituksen myös bugzillaan? Päätös: alkuperäinen tiketin tekijä tekee, muut auttaa tarvittaessa.
* [Varauksen tiedot lokilla](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Valmiita_SQL-raportteja#Varauksen-tiedot-lokilla) -raportin kuvaus päivitetty vastaaman nykyversiota.
* [Viikon 1 päivitys](https://github.com/KohaSuomi/Koha/discussions/347)
* Kaikki kimpat käy läpi tammikuun loppuun mennessä Redminessä Palaute-projektissa olevat tiketit ja sulkee valmiit ja sellaiset, jotka eivät ole enää ajankohtaisia. Lopuista katsotaan, mitkä kannattaa siirtää uusiksi tiketeiksi GitHubiin.

**Vaara**
* Kysymys Finnassa tapahtuneista varauksista ja niiden poistumisesta muilta kimpoilta. Ainoastaan Lapissa oli vastaava tapaus viime viikolla. Tutkitaan vielä asiaa.
* Ei muuta mainittavaa, vuoden viimeinen viikko oli rauhallinen.

**Lumme**
* Kirjeitä jumittunut 20 lokakuulta asti, lähetetty 14.12. ja myöhemmin muodostuneet kirjeet.
* Suomenniemen toveriin uudet aukiolot. Hypernovalta ei ole tullut blugaria Lari tekee Lumpeille oman.
* Toenperän kirjastojen erottaminen toisistaan tehty Finnassa, kohassa vielä vähän vaiheessa. Kirjastoauto Jasso jatkaa entisten Toenperän kuntien palvelemista.

**Siilinjärvi**
* Tavoitteena tänä vuonna saada käyttöön verkkomaksaminen. Aloitettu vanhojen laskutus- ja perintämappien perkaaminen ja tietojen siivous Kohasta. Kaikenlaisia maksuja sitä löytyykin!

**OUTI**
* Käyttösääntömuutoksia tehty Kohaan
  * uusintojen määrä laskettu 10 -> 7
  * konsolipelien lainamäärä nostettu 2 -> 4 eli asiakas voi lainata nyt yhteensä 8 peliä, jos lainaa 4 lasten konsolipeliä ja 4 aikuisten. Aiheuttaa henkilökunnassa keskustelua.
* Omatoimikirjastojen erä- ja noutopäivä ylityksiä vähennetty tälle vuodelle. Aiheuttaa henkilökunnassa keskustelua.

**Vaski**
* Ei erityisiä kuulumisia. Asiakaspalvelusta tiedusteltu, poistetaanko vanhentuneet maksamattomat automaattisesti. Siivousajoa ei vielä ole käytössä ja se edellyttää huolellista suunnittelua, Anneli vie asian eteenpäin kehittäjien viikkopalaveriin.

**Lappi**
* Rauhallinen vuodenvaihde.
* Käyttäjäoikeuksista on ollut kaksi raporttia, toisella voi hakea kaikkien käyttäjien kaikki oikeudet ja toisella oikeusryhmittäin. Rapsat menneet ilmeisesti rikki edellisessä päivityksessä. Vaaralla ilmeisesti näistä toimiva versio? Lari lupasi katsoa Lapin raportteja. 
* Työn alla käyttäjätunnusten tarkistus, aloitetaan vanhentuneiden maksujen poisto. 
