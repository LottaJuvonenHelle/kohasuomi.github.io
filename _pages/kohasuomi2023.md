---
title: 'Koha-Suomen vuoden 2023 muistiot'
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
permalink: /kohasuomi2023
redirect_from:
  - /theme-setup/
toc: true
layout: single
hidden: true
---

Koha-Suomen henkilökunta kokoontuu kaksi kertaa viikossa. Uusin muistio on aina ylimmäisenä.

## Viikon 12 muistiot

### Maanantai 20.3. klo 10

Läsnä: Anneli, Emmi, Ari, Lari, Pasi, Lasse

__Aiheita__

* Kimppojen tietokantojen rakenteen yhtenäistäminen
  * Korjataan huhti-toukokuun huoltoikkunoiden yhteydessä.
* tikettien vastuutus
* Smartum
* [Versionvaihdon tiedote 2](https://github.com/KohaSuomi/Koha/discussions/471)
* Harjoittelija Mikkeliin 3.4.-31.5.2023
* Käännökset - käsitellään erillisessä palaverissa.

## Viikon 11 muistiot

### Torstai 16.3. klo 10

Läsnä: Anneli, Emmi, Kodo, Pasi, Lasse, Lari, Ari

__Aiheita__

* [Tiketti KS21-468 - Auktorisoitujen arvojen kopiointi testi-Tätistä Tätiin](https://github.com/KohaSuomi/Koha/issues/468)
* Nextien cronit päälle, 
  * ei pate, process_messages ja varmuuskopiointiin liittyvät
  * Lari tekee
* Uusi build
  * Buildit nopeampia ja käyttökatkot minimaalisen lyhyitä (muutamia sekunteja)
  * Huomattavasti parantunut vikasietoisuus, esimerkiksi buildin epäonnistuminen ei aiheuta häiriöitä käytössä oleviin Koha-installaatioihin
  * Autoreload otetaan takaisin käyttöön
* Versionvaihdon tikettien vastuutusta
* Finna-nexteillä ei toimi saatavuustietojen haku ja kirjautuminen. Virheilmoitukset Matrixissa.

### Maanantai 13.3. klo 10

Läsnä: Emmi, Ari, Pasi, Lasse, Kodo, Lari, Anneli

__Aiheita__

* [Tiketti 117 - Kaikkien asiakastietojen haun esto varauksenteossa](https://github.com/KohaSuomi/Koha-22x/issues/117#issuecomment-1463677625)
* Finnat ja OAI-PMH
* [Tiketti 33 - Teosta ei saa haettua kaikilla hakutavoilla, kun teoksen nimessä merkki](https://github.com/KohaSuomi/Koha-22x/issues/33#issuecomment-1463717242)
* Yksi hallintaksripti kaikille Kohaan liittyville daemoneille on työn alla
  * SIP, Plack, Memcached, Apache, Elastictmpfs
  * Luovutaanko erillisistä initeistä/systemd-uniteista ja hoidetaan startit ja stopit vastaisuudessa tällä yhdellä hallintaskriptillä rc.localista?
  * Tällä hetkellä mukana on myös service-checkin toiminnallisuus, mutta se tuntuu istuvan skriptiin vähän huonosti, joten riisuttanee pois.

## Viikon 10 muistiot

### Torstai 9.3. klo 10

Läsnä: Anneli, Lasse, Emmi, Pasi, Kodo, Lari

__Aiheita__

* Aputaulujen nimeämiskäytännöt ja aputauluaputaulu
  * Käytetään muotoa: ks_vvkkpp_taulunnimi_tikettinro
  * vanhat taulut nimetään uudelleen uuden käytännön mukaan.
  * tehdään aputauluaputaulu, johon listaus aputauluista -> ks_baktables -> Kodo tekee
    * aputaulun nimi
    * selite, miksi olemassa
    * vanhenemispäivä, jos tiedossa
    * taulun tekijä
* Finna-nextit ja OAI-PMH
  * Lari kyselee apua Kansalliskirjastosta, jossa haravointi on saatu toimimaan.
* no-status/no assignee -tiketit
* Lapin Kohatuessa ei ole päivystystä perjantaina 10.3. pääkäyttäjien lomien vuoksi.
* Nodeilla nyt käynnissä suuri määrä kontainereita (30), koska nexit otettu käyttöön. Tämä aiheuttaa ongelmia, koska palvelinten avointen tiedostojen määrän maksimi tulee vastaan.
  * Tutkitaan saadaanko maksimia korotettua ilman nodejen uudelleenkäynnistyksiä, jos ei saada, niin korotetaan seuraavassa huoltokatkossa.
  * Testejä voidaan mahdollisesti joutua pysäyttämään jos ongelma alkaa isossa mitassa vaivata.

### Maanantai 6.3. klo 10

Läsnä: Emmi, Pasi, Lasse, Kodo, Lari, Anneli

__Aiheita__

* Vkon 10 päivitys
  * käännöstiedostojen päivitys 
* Huoltoikkuna
  * käyttöjärjestelmäpäivityksiä tulossa
  * Kodo tekee tiedotteen 
* Kirkes-konversion 2. kierros alkaa ti 6.3.
* nextien tilanne
  * muut tehty paitsi täti ja kirkes
  * pääkäyttäjät käyvät läpi, mitä tauluja pitäisi mahdollisesti kopioida versionpäivityksen aikaan
* Versiopäivityksen ja Tikettien seurannan tikettien vastuutus. 

## Viikon 9 muistiot

### Torstai 2.3. klo 10

Läsnä: Ari, Anneli, Lasse, Pasi, Emmi, Lari, Kodo

__Aiheita__

* Lokituksen siirtäminen syslogille, facilityt:
```
facility local0 (API), =>error (api-error.log), info (api.log) ja jos tarvitaan warn+debug (api-debug.log)
log4perl.logger.api = ERROR, API
log4perl.logger.plack-api = ERROR, PLACKAPI

facility local1 (UI), =>error (ui-error.log), info (ui.log) ja jos tarvitaan warn+debug (ui-debug.log)
log4perl.logger.intranet = ERROR, INTRANET
log4perl.logger.plack-intranet = ERROR, PLACKINTRANET
log4perl.logger.plack-opac = ERROR, PLACKOPAC
log4perl.logger.opac = ERROR, OPAC

facility local2 (SIP), =>error (sip-error.log), info (sip.log) ja jos tarvitaan warn+debug (sip-debug.log)
log4perl.logger.sip = WARN, SIP
log4perl.logger.sipohttp = INFO, SIPoHTTP

facility local3-local4 varataan tulevaisuuden käyttöä varten

facility local5 (muut), =>error (misc-error.log), info (misc.log) ja jos tarvitaan warn+debug (misc-debug.log)
log4perl.logger.ceepos = INFO, CEEPOS
log4perl.logger.z3950 = ERROR, Z3950

facility local6-local7 varataan mahdollisesti cronjobien ym "kohan ulkopuolisten" juttujen lokitusta varten
```
  * Lokit olisivat siis api, ui, sip ja misc, sekä niiden -error vastineet, joihin lokitetaan virheet ja sitä korkeamman tason lokirivit (warn, error, critical ja fatal), sekä tarvittaessa debug-vastineet, joihin lokitetaan varoitukset ja debug-jutut.
  * Kohan crojobien lokitus voidaan joko pitää entisellään (skriptittäinen lokitus skriptin nimen mukaan /var/log/koha/cronjobs) tai muuttaa cronjob-triggeri käyttämään syslogin cron- tai local6 facilityä ja ohjata lokitus syslogin puolella oikeaan paikkaan.
  * Debug-lokit voisi ottaa käyttöön testiympäristöissä.

* SQL-raporttien jakaminen Koha-yhteisön Mana-tietokantaan. [Bywaterin esittelyvideo](https://bywatersolutions.com/education/monday-minutes-sharing-reports).
  * Jaa sisältö Koha-yhteisölle Mana-tietämyskannan kautta
  Mana-tietämyskanta on maailmanlaajuinen tietämyskanta kirjastokeskeiselle tiedolle. Se on suunniteltu alun perin Koha-järjestelmälle (the Open Source ILS), mutta sitä voidaan hyödyntää myös muissa järjestelmissä.
  Mana keskittää tietoa Koha asennusten välillä ja helpottaa uusien kausijulkaisutilausten, toimittajien, raporttien jne. luontia. Voit etsiä, jakaa, tuoda ja kommentoida Manassa olevaa sisältöä. Mana-tietämyskannassa jaettu tieto on jaettu lisenssillä: CC-0 lisenssi.
  Lue lisää Mana-tietämyskannasta virallinen [Mana-tietämyskannan dokumentaatio](https://wiki.koha-community.org/wiki/Mana_central_database).

* nextien tilanne
  * miten kirkes? Mahdollisimman aikaisessa vaiheessa. Toinen konversiokierros alkaa maaliskuun alussa. Siirtyminen nextiin sen jälkeen.
  * Helle, Kyyti ja Lappi tehty. Kyytissä olemattomia brancheja, mikä aiheutti ongelmia. Lapissa itemseissa linkkejä olemattomiin biblioitemseihin.
  * täti, siili ja lumme vielä

* [#5508](https://tiketti.koha-suomi.fi/issues/5508) - yhteisön bugi ratkaistu


### Maanantai 27.2.2023 klo 10

Läsnä: Anneli, Lasse, Pasi, Emmi, Lari, Ari, Kodo

__Aiheita__

* Kesälomat
  * kalenteriin ehdotukset lomajaksoista
  * Ari tarkistaa, kuinka paljon kullakin on lomapäiviä

* Päivystykset viikosta 10 eteenpäin
  * Lisätty kalenteriin

* Viikon 9 päivitys
  * ei päivitettävää

* Nextien tilanne
  * outin redusointi ma-iltana
  * muut saattaa mennä yhdessä illassa

* lokitus / Kodo & Lari

* skeeman rakentelu / Emmi
  * testattu onnistuuko skeeman rakennus nopeammin, jos tiedostot kirjoitetaan ensin /dev/shm:n alle
  * kirjoittaminen oli jopa hieman hitaampaa kuin suoraan Koha-hakemiston alle, joten tällä ratkaisulla ei valitettavasti pystytä nopeuttamaan skeeman rakennusta

* Finna-rajapinta ja asiakasmääre

## Viikon 8 muistiot

### Torstai 23.2.2023 klo 10

Läsnä: Pia Kusmin Finvoice-kohdassa, Anneli, Emmi, Pasi, Lasse, Lari, Kodo, Ari

__Aiheita__

* Torstain palaverimuistiot on nyt maanantaisten yläpuolella, jotta ovat kronologisessa järjestyksessä (uusin ylimmäisenä, niinkuin sivun alussa luvataan)

* Rovaniemelle käyttöön Finvoice (viesti support-lootassa)
  * Pia selvittelee, onko kyseessä perintä vai laskutus ja on sitten yhteydessä Emmiin.
  * Emmi vastaa Sarastialle, että selvittelemme asiaa. 

* nextien tilanne
  * Vaaran redusointi tehty, pitää tarkistaa lopputulos, kunhan vaara-next saadaan palvelu päälle.
  * Pasi tekee vielä kunnollisen skriptin, jonka jälkeen voidaan muita alkaa rakentamaan. To

* action_logs kk-siivousajojen käyttöönotto
  * keskustellaan vielä pääkäyttäjien kanssa aloitusajankohdasta

* Finnaan tulee aineistotyyppi "Äänikirja" ja Daisy-äänikirjoille oma kuvake. [Viimeisin versiotiedote](https://foorumi.kiwi.fi/t/finnan-versiopaivitykset/437/321). Pitäisikö lisätä jossain vaiheessa myös Kohaan aineistotyyppeihin?
  * [Github RecordManager-Finna](https://github.com/NatLibFi/RecordManager-Finna/commit/f6c3c1d5fc4c7a2e48ef02fdd9c8a4ff9720c5bc)
  * Päätös: lisätään Äänikirja ja Daisy-äänikirja myös Kohaan.
  * Tehdään tiketti ja toteutetaan versiopäivityksen jälkeen.

* totalissues-arvot tiketit [KohaSuomi/Koha #196](https://github.com/KohaSuomi/Koha/issues/196) ja [Redmine #1849](https://tiketti.koha-suomi.fi/issues/1849)
  * [Vkolla 44/22 keskusteltu aiheesta näin](https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Torstain-palaveri-8): Ratkaisu: katkaistaan kuvailupohjien ja biblioitems.totalissues -linkki ja tehdään erillinen cron laskemaan lainamäärät suoraan biblioitems-tauluun
  * Päätös: ohjeistetaan pääkäyttäjiä katkaisemaan jo nyt linkitys biblioitems-tauluun ja tehdään uusi tiketti cronista, joka toteutetaan versionpäivityksen jälkeen. Otetaan myös pois päältä update_totalissues-cron.

* kaksivaiheinen tunnistautuminen
  * toimii hienosti OTP:tä tukevilla mobiiliaplareilla (testattu LastPass authenticator ja FreeOTP)
  * token-laitteita halpa hankkia, mutta hankala/kallis ylläpitää (ohjelmointisoftan käyttöoikeus maksaa noin tonnin, puhelimella ohjelmointi on mahdollista, mutta vaatii NFC:llä varustetun puhelimen ja siihen token-valmistajan sovelluksen)
  * sähköpostin käyttö toisessa kirjautumisvaiheessa toimii "failsafena" jos esimerkiksi puhelin sattuu jäämään kotiin
    * viesti menee Kohan viestijonoon, mutta lähtee heti eikä vasta Kohan muiden viestien lähetyksen yhteydessä, vähän turha siellä jonossa kyllä, ne voisi siivoilla pois
    * ei voida käyttää yksinään, kaksivaiheisen tunnistautumisen käyttöönotto vaatii OTP-laitteen (puhelin tai token)
 
* päivystysnumeron käännöt
  *  Ari ottaa perjantaisin käännöt pois ja laittaa seuraavalle päivystäjälle maanantai-aamuna

* translations repoa ei sittenkään kiinni, vaan hoidetaan käännökset siellä, sen sijaan translations-branch hävitetään

* Versionvaihdon tikettien vastuutuksen jatkaminen
  * kaikille sms-plugareille on käyttöä

### Maanantai 20.2.2023 klo 12

Läsnä: Anneli, Lari, Lasse, Emmi, Pasi, Kodo

__Aiheita__

* nextien tilanne
  * redusointi ei onnistunut vielä perjantaina. Ma-iltana uusi yritys.

* viikon 8 päivitys
  * ei päivitettävää.

* versionvaihdon loppujen tikettien läpikäynti ja vastuutus

* translations
  * repo kiinni, tiketit Kohan alle -> Anneli siirtää 

## Viikon 7 muistiot

### Torstai 16.2.2023 klo 10

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi

__Aiheita__

* https://github.com/KohaSuomi/Koha/issues/409 ja https://github.com/KohaSuomi/Koha/issues/412
  * vaatii käytännössä konversion, joka on suuritöinen
  * ehdotetaan uusien kirjastoyksiköiden perustamista ja aineistojen ja asiakkaiden siirtoa uudelle yksikölle.
  * kannattaa tehdä tilastojen kannalta vuodenvaihteessa. 

* [Redminen tukipyynnöt](https://tiketti.koha-suomi.fi/projects/fbox/issues?utf8=%E2%9C%93&set_filter=1&sort=id%3Adesc&f%5B%5D=status_id&op%5Bstatus_id%5D=o&f%5B%5D=tracker_id&op%5Btracker_id%5D=%3D&v%5Btracker_id%5D%5B%5D=3&f%5B%5D=&c%5B%5D=due_date&c%5B%5D=tracker&c%5B%5D=status&c%5B%5D=priority&c%5B%5D=votes_total&c%5B%5D=subject&c%5B%5D=assigned_to&c%5B%5D=updated_on&c%5B%5D=author&c%5B%5D=category&c%5B%5D=cf_14&c%5B%5D=cf_15&group_by=&t%5B%5D=)

* GuarantorHasToBePatron-asetus vs. css-rimpsu
  * luovutaan omasta asetuksesta ja käytetään css-rimpsu + piilotetaan kentät lisäksi BorrowerUnwantedFields -asetuksella

* nextien tilanne
  * perjantaina eka yritys redusoida vaara

* smartum?

* No status -tiketit

* Finna-toimistosta vastasivat
  * tarvivat OAI-PMH-haravointiosoitteet alkuunsa ja myöhemmin myös REST-yhteystiedot testikantoja varten.
  * varaustunnuksen vaihtamista asiakasmääreeksi ja nideryhmien käyttöönottoa eivät vielä kommentoineet

* plugarit
  * Lari tekee tiketit k22xx-repoon kaikista plugareista.

### Maanantai 13.2.2023 klo 10

Läsnä: Anneli, Pasi, Lasse, Emmi, Lari, Kodo

__Aiheita__

* Vkon 7 päivitys
  * lokitusmuutokset -> 
    * sipoverhttps-lokitusta vähennetty viime viikolla
    * accesslokitusten lopetus
  * kirkes-test asiakasvarmenteen taakse

* next-kantojen tilanne
  * Pasi alkaa testaamaan tietojen redusointia
  * vaara-next ensin

* skeeman rakentelu toimii

## Viikon 6 muistiot

### Torstai 9.2.2023 klo 10

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi

__Aiheita__

* Keskiviikon huoltokatkon kuulumiset / Kodo

* [Palvelut](https://github.com/KohaSuomi/koha-suomi-utility/blob/master/docs/palvelut.md)-sivun päivitys
  * Tilastoitavuus-tägi

* No status -tikettien läpikäynti

* Ma-muistiosta: Jokainen käy assignaamassa itselle [versionvaihdon tiketeistä](https://github.com/KohaSuomi/Koha-22x/issues?page=1&q=is%3Aissue+is%3Aopen) ne, jotka on hoitanut edellisessä versionvaihdossa ja katsotaan sitten, mitä jää jäljelle ja sovitaan niille vastuuhenkilö. 

* Idea: _Bugi-perjantai_ kerran kuussa pe klo 13-15 etsitään Bugzillasta meille tärkeitä sign offattavia tikettejä ja testataan niitä sandboxeissa tai jollain meidän testillä. Mukaan kehittäjä (tai useampi) ja pääkäyttäjiä. Aloitusaikataulu versionvaihdon jälkeen. Emmi mukana. /Anneli

* https://tiketti.koha-suomi.fi/issues/5303 - tiketti yhteisöön? Ongelma toistuu myös 22.11-versiossa.

* Lari: action_logsit korjattu, mutta ajo on skipannut virheen jälkeiset päivät, eikä ne tullut mukaan takaisin.
  * Korjaus: viedään taulun loppuun, vaikka id:t menee sekaisin.

### Maanantai 6.2.2023 klo 10

Läsnä: Anneli, Emmi, Kodo, Lari, Lasse, Pasi

__Aiheita__

* Vkon 6 päivitys
  * ei päivitettävää 

* Huoltokatko ke 7-9
  * vaihdetaan palomuurin muistikammat
  * todennäköisesti ei katkoja tiedossa 

* next-kantojen tilanne
  * "normitestaajat" testamaan viimeistään huhtikuun puolivälissä?
    * Mahdollisimman valmiina omat ominaisuudet ennen kuin virkailijat testaa
    * pari viikkoa testiaikaa, jonka jälkeen vielä pari viikkoa aikaa korjauksille
  * redusointiskripti ehkä valmiiksi tällä viikolla
  * Kontainerit luodaan viikolla 6 ja palomuureille ja DNS-palvelimille tehdään tarvittavat asetukset. Asetusten käyttöönotto palomuureilla keskiviikon 8.2. huoltokatkon yhteydessä.

* mikä olisi hyvä paikka [tietoturvaohjeelle](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Koha-Suomen_tietoturvaohje)?
  * Kohan ohje suomeksi -otsikon alle viimeiseksi (jos ei löydy, niin siirretään sitten ekaksi)

* TLS-salaus lähteviin posteihin?
  * Kodo keskustellut sen käyttöönotosta BittiGurun kanssa ja se onnistuu.
  * Otetaan käyttöön, kun operaattori ehtii. 

* Anneli kertoi tieteellisten pääkäyttjien palaverissa meidän aikeista muuttaa varaustunnus asiakasmääreeksi ja ottaa käyttöön nideryhmät. Tieteellisillä vielä käytössä othernames-kenttä varaustunnukselle. Nideryhmiä ei oltu tutkittu juurikaan, eikä niille keksitty heillä äkkiseltään käyttöä.

* Siivousajot
  * action_logsin siivous kerran kuussa porrastaen kimpoittain eri päiville
  * Lari kirjaa Tietojen säilytysajat -sivulle porrastusaikataulun
  * käytetään aikataulumuutos asiantuntijaryhmän seuraavassa kokouksessa 20.2.2023
  * käyttöönotto maaliskuussa

* Jokainen käy assignaamassa itselle [versionvaihdon tiketeistä](https://github.com/KohaSuomi/Koha-22x/issues?page=1&q=is%3Aissue+is%3Aopen) ne, jotka on hoitanut edellisessä versionvaihdossa ja katsotaan sitten, mitä jää jäljelle ja sovitaan niille vastuuhenkilö. 

## Viikon 5 muistiot

### Torstai 2.2.2023

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi

__Aiheita__

* ODUECLAIM-viestien säilytysaika
  * Lari huolehtii ennen seuraavia puhdistusajoja, että ajot noudattaa [Tietojen säilysaikapäätöksiä](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Tietojen_s%C3%A4ilytysajat).

* lokitukseen muutos, että lokille tallennetaan vain muuttuneet arvot? Emmi tekee tiketin ja tutkitaan tarkemmin versionvaihdon jälkeen.

* [Kooste-viesti-triggeri tuotantoon](https://tiketti.koha-suomi.fi/issues/5269)?
  * Tähän liittyy myös tiketti [K21-389](https://github.com/KohaSuomi/Koha/issues/389)
  * käyttöliittymästä täpät piiloon, transportit pois, täpät puuttuville.

* Lapin varausten keskeytykset [K21-397](https://github.com/KohaSuomi/Koha/issues/397)

* [Varaukset ei näy Finnassa KohaSuomi/Koha #212](https://github.com/KohaSuomi/Koha/issues/212) - voisko johtua AllowRenewalIfOtherItemsAvailable-järjestelmäasetuksesta?

* Versionvaihdossa branchien nimet pidetään samoina kuin aiemmin.

### Maanantai 30.1.2023

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi

__Aiheita__

* Kimpoissa on tilauksia, jotka ovat yhtä aikaa vastaanotettu ja tilattu. Niissä on vastaanottopäivä aqorders-taulussa, mutta orderstatus on 'ordered'. Tämä aiheuttaa ongelmia vastaanotossa. Näkyville tulee tilauksia, jotka on jo vastaanotettu ja niitä ei saa vastaanotettua uudelleen.
  * select * from aqorders where datereceived is not null and orderstatus='ordered'
  * [Liittyy tiketti #300](https://github.com/KohaSuomi/Koha/issues/300) ja Pääkäyttäjien matrixissa käyty keskustelu ["Vaivaako muitakin kimppoja päivityksen jälkeen ilmestyneet vanhat jo vastaanotetut tilaukset?"](https://matrix.to/#/!XuuUEkGSyGepDvGgvN:matrix.org/$14Q-Lkxhbz80FPXzTj08OUyPqyzNCynMau-kXl1ZbtM?via=matrix.org) (linkki matrixiin, avautuu vain jäsenille)
  * Laskin, kuinka paljon on tilausrivejä, joissa on datereceivedissä päivämäärä ja orderstatus 'ordered': Lumme: 7646, Outi: 9282, Lappi: 782, Vaara: 849, Vaski 2, Kyyti: 7255, Helle: 6, Siili: 2279
  * Mitä näille voisi tehdä? Muuttaa ajolla orderstatus vastaanotetuksi (complete)?
  * Päätös: Emmi muuttaa kaikkien niiden rivien, joissa on datereceived-arvo ja orderstatus='ordered' -> orderstatus='complete' ja seurataan, tuleeko uusia.

* Viikon 5 päivitys
  * Käännösmuutoksia, joten käännökset ajettava

* Päivystysvuorot viikosta 6 alkaen
  * Vko 6 Pasi ja Kodo
  * Vko 7 Lari ja Anneli
  * Vko 8 Lasse ja Emmi
  * Vko 9 Pasi ja Kodo

## Viikon 4 muistio

### Torstai 26.1.2023 klo 10

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi

__Aiheita__

* [Koulutuksista "tilastosivu"](https://github.com/KohaSuomi/koha-suomi-utility/blob/master/docs/Koulutustilastot.md) utilityyn
  * Luotiin kokouksen aikana myös seurantasivu erilaisille [palvelumaksuun kuuluville töille](https://github.com/KohaSuomi/koha-suomi-utility/blob/master/docs/palvelut.md).

* action_logs-taulujen korjaus
  * yritetään toteuttaa ilman käyttökatkoa
  * jatketaan pohdintoja torstain palaverissa
  * Siivotaan ensin 2021:t vuositauluun work_action_logseista -> Siirretään action_logs-taulusta rivit work_action_logs-tauluun loppuun ja tuhotaan nykyinen action_logs-taulu -> nimetään uudelleen work_action_logs-taulu action_logs-tauluksi. Huolehditaan, että autoincrement-arvo on tarpeeksi suuri.
    * Tiedotettava Lapin, OUTIn ja Vaskin pääkäyttäjiä katkosta. 
    * Lari tekee tiketin ja on vastuuhenkilö

* Tikettien vastuutuksen jatko
  * Tehtävä-statuksella oleville vastuuhenkilö 
  * [Koha #212](https://github.com/KohaSuomi/Koha/issues/212) - kelle? Lasse
  * [Koha #223](https://github.com/KohaSuomi/Koha/issues/223) - Pitää selvitellä, saisiko sen taustatyö-ilmoituksen näkyville taas.
  * [KohaSuomiServices #3](https://github.com/KohaSuomi/KohaSuomiServices/issues/3) - missä mennään?
  * [Koha #240](https://github.com/KohaSuomi/Koha/issues/240) - mitä tehdään? Tiketti yhteisöön?
  * [Koha #252](https://github.com/KohaSuomi/Koha/issues/252) - Voiko mitään?
  * [Koha #372](https://github.com/KohaSuomi/Koha/issues/372) - kaikille testeille / Lasse
  * [Koha #349](https://github.com/KohaSuomi/Koha/issues/349) - näitä on taas lisääntyvä määrä ainakin OUTIssa/Vaskissa

* Viikon 5 päivitys
  * Käännösmuutoksia, joten käännökset ajettava

* Vaski-nextin tilanne & muiden nextien
  * tiedonhaku ei vielä toimi vaski-nextillä
  * datan redusointi muita kuin vaski-nextiä varten työn alla

### Maanantai 23.1.2023 klo 12

Läsnä: Ari, Anneli, Emmi, Kodo, Lari, Lassi, Pasi

__Aiheita__

* Asiantuntijaryhmässä esillä olleiden tikettien läpikäynti/vastuutus
* Viikon 4 päivitys
  * https://github.com/KohaSuomi/Koha/issues/233 - korjattu versio
  * Koha-translations #4 - vaatii vielä korefresh -r:n
* action_logs-taulujen korjaus
  * yritetään toteuttaa ilman käyttökatkoa
  * jatketaan pohdintoja torstain palaverissa
* Sanaston raporteissa meni 16 tuntia ajaessa

## Viikon 3 muistiot

### Torstai 19.1.2023 klo 12

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi

__Aiheita__

* OKM-tilastojen ongelmat Lumpeissa
  * Lumpeen pääkäyttäjiä tulee mukaan
  * ongelma johtuu siitä, että items.cn_sort-kentässä on kentän alussa kirjaimia
  * Varkaus siirtyy tekemään signumit samalla tavalla kuin muissa Lumpeiden kirjastoissa
  * Koha-Suomi (Lasse) korjaa olemassa olevien niteiden cn_sort-kentät ja signum-kentät. Anneli tekee tiketin.
  * tarkistetaan Hellessä Loviisan tilanne

* Häiriö- ja huoltotiedotteet vastaisuudessa GitHubin discussionsiin

* Outlook/Hotmail,complainttaavat asiakkaat, lähtevän postin palvelimen "maine" ja viestien perillemeno
  * Bottivastaus, käsiteltävä pääkäyttäjäryhmässä tiistaina

* Build-production-branch-skriptin muutokset
  * muutetaan toiminnalisuutta niin, että uusia brancheja ei haeta automaattisesti 
  * nimen muutos, koska tällä rakennetaan myös testit, ei pelkästään production (build-(ks)-release?)
  * lisätäänkö skriptiin myös DBIx-skeemaluokkien rakennus ja käännösten asennus?
    * jos DBIx skeemaluokat tehdään uusiksi buildissa, niitä ei enää tarvita omassa erillisessä git-branchissaan, jolloin sitä branchia ei enää tarvitse ylläpitää (voidaan hävittää?)
  * tehdäänkö nyt vai versionvaihtoon
  * Pasi tekee. Ensin testille.

* käännöstiedostot pois kaikkialta muualta paitsi translation-reposta. Lari tutkii, miten se onnistuu.

* Kirkes parametrointikanta (tuleva tuotanto-Kirkes)

* Kirkes asiakasvarmenteet
  * Emmi tekee
  * varmenteet voi olla voimassa korkeintaan 13 kk (TLS-protokollassa oleva rajoite + selaimet eivät hyväksy tuota pidempään voimassa olevia sertifikaatteja)
  * tehdään "testi-sertifikaatti", joka voimassa vuoden loppuun ja toimitetaan elokuussa uusi "tuotanto-sertifikaatti", joka on voimassa samassa rytmissä kuin muiden kimppojen sertit.

* SmartBoxin palautustoiminnallisuuden ja varaustenkäsittelyn muutokset
  * palautuksille SIP-tuki, 09-viesti
  * varausten käsittely: niteet palautetaan ensin Kohassa ja sitten piipataan vielä SmartBoxissa.

* Finna ja versionvaihto - joko päätettiin, kuka on yhteydessä Finna-toimistoon?
  * Anneli viestii Tolosen Erkille 

* Muovitustiedon lisääminen EDItX sanomiin
  * Anneli kyselee, mikä tässä on oikeasti tarve/tausta

* Sanaston raporttien ajo to-iltana

* Viikon 4 päivitys

### Maanantai 16.1.2023 klo 12

Läsnä: Emmi, Pasi, Lari, Lasse, Anneli, Kodo

__Aiheita__

* Vaski meni sunnuntaina jumiin liian pitkän kestäneen action_logsin siivousajon takia, jumittanut kyselyyn:
INSERT INTO action_logs (SELECT * from work_action_logs WHERE DATE(timestamp) >= DATE('2022-01-01'));
  * action_logs-taulusta puuttuu Lapista, OUTIsta ja Vaskista kaikki su-aamua aikaisemmat tiedot. Ne ovat tallessa work_action_logs-taulussa.
  * Lari ja Emmi tutkii, miten datan saisi vietyä tauluihin pienemmissä seteissä.

* Metatietosanasto-plugari / Antti H.
  * voi olla periaatteessa tehtävissä, tehdään kehitysehdotus

* Viikon 3 päivitys

* indeksin mappingsin sijainti
  * ne ovat nyt etc:ssä, joka on kimppakohtainen.
  * siirretään koha-repoon ja tehdään oma branch, nimetään mappings koha-suomi-mappings.yaml ja muutetaan koha-confissa hakemaan mappings sieltä
  * hävitetään mappingsit etc:n alta
  * koha-repon alta otetaan ylimääräiset mappings-tiedostot pois
  * Lari tekee ( myös tiketti)

* valvonnan muutokset
  * lähtevät viestit tarkistetaan vasta 9.30 jälkeen. Jos tarkistuksen tekee ennen tuota, saa ilmoituksen, että viestejä ei ole vielä tarkistettu.
  * konttiin kirjautuessa saa jatkossa huomautuksen yli tunnin käynnissä olleista kyselyistä.

* Sanasto-raportin muutos toimimaan nykyisessä versiossa ei olekaan niin helppo kuin alunperin ajateltiin.

## Viikon 2 muistiot

### Torstai 12.1.2023 klo 10

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lassi, Pasi

__Aiheita__

* Viikon 3 päivitys
  * 350 - osa, Pasi päivittää tikettiin, mitä tulee mukaan.
  * 308
  * https://tiketti.koha-suomi.fi/issues/5600
  
* Käännökset - messages.js.po-tiedoston kaikki käännökset eivät näy

* testien pienennys
  * dumppi, josta jätetään isoja tauluja pois
  * otetaan tyyliin 5000 viimeisintä (tai jokin muu setti) tietuetta ja niihin liittyvät niteet/lainat
  * Emmi katsoo taulut ja Pasi katsoo datan poiminnan
  * Kodo tekee Vaskin next-testin, koska sinne tulee kaikki mahdollinen mukaan

* Kun kontteja siirtelee nodelta toiselle, voi lxc vetää maton alta kontilta ennen kuin indeksit ehditään saada kokonaan levylle. Kontissa, joka siirretään, pitää ajaa elastictmpfs synctodisk (esimerkiksi nodelta kogo [kontti] sudo elastictmpfs synctodisk). Kirjoitetaan tämä osaksi koctl:ää kun ehditään, mutta tässä vaiheessa siis pitää tehdä manuaalisesti.

* principioon dokumentaatio, mitä tehdään huoltokatkon aikana

* keskiviikkona ei saatu vaihdettua palomuurien muistikampoja, koska ne oli vielä Kuopiossa postin hallussa. Nämä vaihdetaan helmikuun käyttökatkossa. 

### Maanantai 9.1.2023 klo 10

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi

__Aiheita__

* Valutus- ja hankintaongelmat ja Elasticsearch
  * "It turned out that queryParser is not thread-safe - inside it has states, access to which from several threads is not synchronized. Therefore, I came to use own queryParser for each request, and not use the previously created one." [https://stackoverflow.com/questions/71547835/org-apache-lucene-queryparser-classic-parseexception-cannot-parse](https://stackoverflow.com/questions/71547835/org-apache-lucene-queryparser-classic-parseexception-cannot-parse)
  * Vaatinee koodimuutoksia Kohaan, bugiraportti yhteisöön?
  * Ollaan yhteydessä kansalliskirjastoon, jossa ElasticSearch:ia on Kohaan kehitetty

* Viikon 2 päivitys
  * käännöksissä korjauksia 
  * Muutama XSLT-muutos, esim. hakutulosnäytön Sisältyy-linkki.

#### Tammikuun huoltokatkon toimintasuunnitelma

1. Asiakasviestintä keskeytetään katkon ajaksi.
2. Testit ja redmine pysäytetään. Kirkes-testi siirretään kakkosnodelle, koska samana päivänä yhdeksältä pitäisi olla Kirkes-järjestelmäasetusten läpikäynti.
3. Lumme, siili, täti, lappi, vaski siirretään ykkös- ja nelosnodeilta (Meg ja Amy) kakkos ja kolmosnodelle (Jo ja Beth). Vaski menee kakkoselle.
4. P2 palomuuri alas, kampojen vaihto ja palvelin ylös, P1 jatkaa edelleen hommiaan. P2 alkaa käynnistyttyään neuvotella IPSec tunneleita uusiksi ja toivottavasti ehtii valmiiksi siihen mennessä kun P1 menee alas (kohdassa 11).
5. DB1 (Nat) alas, kampojen vaihto ja palvelin ylös. Tietokantapalvelimen käyttäminen alhaalla aiheuttaa katkon kaikkiin kimppoihin. Katko päättyy kun palvelin saadaan takaisin käyntiin.
6. Nelonen (Amy) alas, kampojen vaihto ja palvelin ylös.
7. Jos tässä kohtaa ollaan vielä huoltokatkon paremmalla puolella, siirretään vaski ja lappi takaisin neloselle, jos ei niin saavat jatkaa sijaisnodella toistaiseksi. Mahdollisesti on tarpeen siinä tapauksessa muuttaa IP-osoite Turun pääkirjaston palautusautomaatilla, jolloin Vaski jäisi sitten pysyvästi kakkosnodelle.
8. Ykkönen (Meg) alas, kampojen vaihto ja palvelin ylös.
9. Jos tässäkin kohtaa ollaan vielä huoltokatkon paremmalla puolella, siirretään lumme, siili ja täti takaisin ykköselle, jos ei niin saavat jatkaa sijaisnodella toistaiseksi. Sillä ei periaatteessa ole vaikutusta mihinkään ja kontit voidaan siirtää oikealle nodelle sopivan tilaisuuden tullen, esimerkiksi illalla tai mahdollisesti vasta seuraavassa huoltokatkossa.
10. DB2 (Dan) alas, kampojen vaihto ja palvelin ylös, varmistetaan että replikointi jatkuu oikein. Tässä vaiheessa raportit eivät toimi oikein ennenkuin DB2 saadaan takaisin linjoille.
11. P1 palomuuri alas, P2:n pitäisi tässä kohtaa ottaa ohjat huomattuaan ykkösen menneen alas. Mahdollisesti tunneleiden siirtymiseen liittyvä viive voi tulla näkyväksi tässä kohtaa. Tätä on pyritty kompensoimaan antamalle P2:lle mahdollisimman paljon aikaa neuvotella tunnelit uudestaan.
12. Vaihdetaan kammat P1:lle ja nostetaan se takaisin ylös, liikenne palautetaan illalla takaisin kulkemaan P1:n kautta.
13. Laitetaan asiakasviestintä takaisin käyttöön.
14. Nostellaan testikontit ja Redmine takaisin kunhan ehditään.

## Viikon 1 muistiot

### Torstai 5.1.2023 klo 10

Läsnä: Pasi, Lari, Kodo, Lasse

__Aiheita__

* Vanhentuneiden maksujen poistoajo - Vaski kysyi pääkäyttäjäpalaverissa, että mikä sen tilanne on?
  * Päätös [Tietojen säilytysajat -wikissä](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Tietojen_s%C3%A4ilytysajat)

* Viikon 2 päivitys
  * käännöksissä korjauksia 
  * Muutama XSLT-muutos, esim. hakutulosnäytön Sisältyy-linkki.

* Onko huoltokatkoa vkolla 2 keskiviikkona?
  * On, ja iso: Fujitsun muistikampojen vaihdot. Katko saattaa kestää enemmän kuin 2 tuntia, ja koskee kaikkia kimppoja.

* Pääkäyttäjien kanssa sovittiin, että jokainen kimppa käy omat Redmine-tikettinsä Palaute-projektissa läpi ja sulkee valmiit ja sellaiset, jotka eivät ole enää ajankohtaisia. Loput käydään läpi ja päätetään, mitkä siirretään uusina tiketteinä GitHubiin.

* Siirretään käännökset build-productionista omaan repoon, symlinkataan meidän omat po-tiedostot reposta Kohan ympäristöön.
 
* datereceived-kenttä löytyy muualtakin kuin vain aqorders-taulusta? Tämä on meidän oma muutos, ja on jäänyt roikkumaan; poistetaan.

### Maanantai 2.1.2023 klo 10

Läsnä: Anneli, Lasse, Pasi, Ari, Lari, Kodo

__Aiheita__

* Viikon 1 päivitys
  * [KohaSuomi/Koha #331](https://github.com/KohaSuomi/Koha/issues/331) Suojatut kentät näkyvät tyhjinä z39.50-haulla tietueita korvattaessa
  * [KohaSuomi/Koha #334](https://github.com/KohaSuomi/Koha/issues/334)
  * SQL-raportit hakemaan slave-kannasta masterin sijaan, jotta vältytään tietokannan taulujen lukkiutuminen raskaissa kyselyissä sekä master-kannan kuormaa saadaan kevennettyä.
  * [Koha #308](https://github.com/KohaSuomi/Koha/issues/308)

* Kodo ehdottaa tämän viikon Kirkes-palaverin ajankohdaksi ke 4.1.2023

* Versionvaihto
  * viedään ensin Vaski, jotta nähdään, kuinka kauan maksimissaan menee.
  * kaikille läksyksi miettiä torstain palaveriin mennessä, miten saadaan vähennettyä testikantaan vietävän datan määrää, jotta testikantojen luonti ei vie niin kauan.
