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

## Viikon 46 muistio

### Maanantai 13.11.2023 klo 9

Läsnä: Anneli

* https://github.com/KohaSuomi/Koha/issues/906 Virkailijatilin voimassaoloajan pidentämisen rajoitus
* Onko ajatusta milloin viestien lähetys muutetaan tapahtumaan 5 minuutin välein (https://koha-suomi.fi/kohasuomi2023#torstai-5102023-klo-10)
* "Too many open files" johtunee inotifyn max_user_instance:sta (nyk. 128) https://bugs.launchpad.net/ubuntu/+source/lxd/+bug/1602192
* Joulunajan lomat

  
## Viikon 45 muistio

### Maanantai 6.11.2023 klo 9

Läsnä: Emmi, Lasse, Kodo, Ari, Kassu, Johanna

* Redminessä Teknisessä dokumentaatiossa olevien dokumentaatioiden siirron vastuutuspalaverista sopiminen
  * Siirretään tämän käsittely ensi maanantaihin
* Käytännöt API-tunnuksien käsittelystä ja toimittamisesta
  * kehittäjät luovat tunnukset kimpan pääkäyttäjän pyynnöstä, pyyntö tehdään tiketillä
  * kehittäjät toimittavat tunnukset suoraan integraation toteuttajalle onetimesecretillä
* Kellutusoptimoinnista palaveerattu perjantaina Weaselin ja Turun väen kanssa
  * Käyty läpi tietotarpeet ja niistä muodostettu taulukko, homma jatkuu keskiviikkona tietosettien määrittelyllä
  * Asiakkaiden profilointi kontra yksiköiden profilointi edelleen keskustelun alla erityisesti asiakkaan sukupuolen arvaamisen osalta, Kodo on yhteydessä Rebekkaan. Mielekkäämmältä tuntuisi profiloida aineistojen käytön "intressiryhmiä", sikäli kun asiakkaiden profilointi on ensinkään tarpeen. Esimerkiksi "sotakirjallisuudesta kiinnostuneet henkilöt" mieluummin kuin "35-50 vuotiaat etunimen perusteella miesarvatut".
  * Kassu voisi mahdollisesti kokeilla hampaitaan SQL-raporttien laadinnassa tietopaketteja varten
* Huoltoikkunassa 8.11. ei tule katkoja tuotantoihin, testeille voi tulla. OCFS-murheiden selvittelyä Jannen kanssa ohjelmassa.

## Viikon 44 muistio

### Maanantai 30.10.2023 klo 9

Läsnä: Anneli, Lasse, Pasi, Emmi, Kodo, Johanna

* Vaskin tuotantoon raportteri-plugin
  * tiistain päivityksessä
* vkon 44 päivitys
* Emmi:
  * Järvenpään laskutusta varten toimitettu IP-osoitteet 

## Viikon 43 muistio

### Maanantai 23.10.2023 klo 9

Läsnä: Anneli, Lasse, Lari, Emmi, Pasi, Johanna, Ari, Kodo

* Päivystysvuorot viikosta 44 eteenpäin kirjattu kalenteriin
  * Lari ja Lasse
  * Pasi ja Kodo
  * Anneli ja Johanna
  * Emmi ja Lari 
* Viikon 43 päivitys
  * Päivitystiedote [täällä](https://github.com/KohaSuomi/Koha/discussions/856) 
* Genren lisäluokka (084 9_ ‡a) biblio_data_elements-tauluun.
  * Lisätään tälle oma sarake, johon lisätään kaikki tietueen genren lisäluokat pilkulla eroteltuna 
* Versionvaihdon tikettien vastuutukset, milloin hoidetaan? Tarvitaanko erillinen palsu?
  * pidetään erillinen palaveri torstaina 26.10. klo 9 

## Viikon 42 muistio

### Maanantai 16.10.2023 klo 9

Läsnä: Anneli, Ari, Kodo, Emmi, Lasse, Lari, Johanna, Pasi

* Viikon 42 päivitys
  * HUOM! ajetaan päivityksen yhteydessä git gc --prune=now, jotta pois siivottujen vanhojen build-branchien luomat välitiedostot poistuvat 
* Koha-seminaarin matkajärjestelyt /Anneli
* kirjataan miitinkikäytännöt /Anneli
  * päivystäjä tekee muistiopohjan valmiiksi, mutta jos joku lisää sitä ennen asiaa, niin hän tekee muistiopohjan samalla.
  * jokainen kirjoittaa omat asiansa ja nimensä läsnäolijalistaan
  * päivittäiset pikapalaverit siirretään klo 11.00-11.15 ja pyritään siihen, että siihen ei oteta muita kokouksia päälle.
* Emmi:
  * Tasku-Warkaus ei saa tehtyä API-kutsua availability/item-endpointiin
    * johtuu siitä, että Lumpeissa on käytössä decreaseLoanHighHolds-asetus, jonka vuoksi kutsutaan muuttujia $patron->unblessed ja $item-unblessed, noista jompikumpi tai molemmat johtaa virheeseen "Can't call method "unblessed" on unblessed reference"
    * otettu yhteys Ere Maijalaan ja kysytty lyötyykö tähän korjausta
  * Monetralta pyydetty laskutuksen testiaineistoa, toimitettu zip-pakettina Erika Miettiselle
  * Ainakin Kirkeksen testillä tulee runsaasti Elasticsearch-virheitä bde-ajon yhteydessä, bde-taulusta puuttuu 60000 tietuetta
    * ajoon vipu, jolla voi testata yhden tietueen viemistä bde-tauluun, helpottaa testailua  
* Anneli
  * Perjantaina pidettiin ensimmänen Bugi-perjantai ja osallistujia oli parisen kymmentä sekä Koha-Suomen kirjastoista että tieteellisistä kirjastoista.
    * Katsottiin ensin, että kaikilla on tunnukset Bugzillaan ja käytiin läpi, miten tikettejä sign offataan.
    * Bugeja saatiin sign offattua 3-4 ja yksi meni Failed QA -tilaan.
    * huomattiin, että kaikkia ennakkoon valittuja ei pystynytkään testaamaan sandboxissa ja todettiin, että tarvitsisimme oman yhteisön masteria ajavan testin.
    * tässä kokouksessa todettiin, että meillä on jo yksi kontti, jossa se on mahdollista, kunhan saamme hidastelu/tilaongelmat ratkaistua.
    * mietittävä myös, miten sinne yhteisön masteria ajavaan konttiin saadaan tuotua patchit testattavaksi.
  * RDA-konversio:
    * todettiin, että se kannattaa tehdä yhtä aikaa YSO-konversion kanssa, koska kummassakin pitää käsitellä koko tietokanta. Ei ole järkeä tehdä kaksi kertaa.
    * vastuutettiin Johannalle ja Emmille RDA-konversiokin.
    * ennen konversioita kannattaa varsinkin TäTissä tehdä vanhojen ja virheellisten tietueiden poistoja reilulla kädellä. Kuvailuryhmä pystyy arvioimaan, mitä voidaan poistaa.
* Kodo
  * Kirkeksen EDItX on tuotannossa ja käy ja kukkuu.
  * Redminen tikettien konversio Githubin RedGrave repoon on työn alla. Sen jälkeen täytyy vielä katsoa mitä muuta siirrettävää Redminessä on ennen sen ajamista alas.
  * Ajojärjestysmuutos on tehty viime keskiviikon huoltokatkossa, tuotannot nyt Jo:lla ja Amy:llä. Meg ja Beth ajavat testejä.
  * OCFS-murheita selvitelty. Kirjoitussuorituskyky on osoittautunut aivan surkeaksi. Selvittely jatkuu Bittigurun kanssa viikolla 43.
  * Build-skriptistä uusi versio testillä, mutta ei vielä commitoitu eikä tuotannossa. Stashaamisen sijaan vanhan release-branch resetoidaan viimeisimpään committiin (jolloin päästään eroon DBIx -skeematiedostoista) ennen branchin vaihtoa buildin alussa. Branchin vaihdon jälkeen vanhan release-branch poistetaan kokonaan ja ajetaan git gc --prune=now.
* Johanna
  * Valutuksen uudelleen kirjoittelua "koha-plugin-broadcast-biblios"-liitännäiseen. Vähitellen siirretään toiminnot pois Mikropalvelusta, koska nykyinen Koha tukee jo siihen tarvittavia toimintoja.
  * Turun kellutuksen hallintatyökalun aloituspalaveri, selvitettiin mistä rajapinnoista tietoa kannattaa hakea.
  * Selvitetty tietueiden siirtoihin liittyviä ongelmia

## Viikon 41 muistio

### Maanantai 9.10.2023 klo 9

Läsnä: Anneli, Lari, Emmi, Kodo, Pasi, Lasse, Ari, Johanna

* Viikon päivitys
  * päivitetään vain liitännäisiin liittyvät ongelmat, koska ne voi päivittää ilman buildia
* Elasticsearch-koulutus ke 1.11.2023 klo 13
* Outi-tuotannossa ollut viime torstaista /dev/shm:llä (/dev/shm/var/log/koha) sipohttp-lokitus. Viiveet loppuneet. Siirretään sipohttp-lokitus muillekin kimpoille /dev/shm alle ja muutetaan lokirotaatiota, jotta päivän /dev/shm:lle kertynyt loki siirretään /var/log/koha alle.


## Viikon 40 muistiot

### Torstai 5.10.2023 klo 10

Läsnä: Anneli, Kodo

* Viestien lähetyksen ajastusmuutos taululukkojen hallitsemiseksi?
  * Tällä hetkellä viestejä lähetetään 15 minutin välein klo 9.30 - 20.00. Vartissa viestejä ehtii kertyä jonoon ehkä hieman turhan paljon, jolloin viestitaulun lukitus lähetyksen ajaksi voi kenties olla osasyyllinen taululukkojen aiheuttamiin tahmailuihin.
  * Päätös: Muutetaan viestien lähetystä siten että viestit lähetetään viiden minuutin välein ja yhdessä setissä lähetetään maksimissaan 500 viestiä. Viestijonot pysyvät lyhyempinä, purkautuvat nopeammin ja taululukot jäävät lyhyemmiksi.
* Käytäntöehdotus: Vaskilaiset huomasivat lisätä Elementissä/Matrixissa näyttönimeen, kun ovat lomalla. Otetaanko sama tapa yleiseksi käytännöksi kaikille? Esim. Anneli Österman | Lomalla 1.10.-3.10.2023
  * Päätös: otetaan käytännöksi
* [Kirjastopalvelun päiväpakettien tuonnissa](https://github.com/KohaSuomi/Koha/issues/815) TäTiin tällä viikolla jo kahdesti ongelmia. Anneli
  * Tämäkin liittynee file handle -ongelmaan. Seuraillaan tilannetta ja koitetaan edelleen korjata ongelman syy.
* Vanhojen maksujen poisto: testataan testillä, pääkäyttäjät tutkivat testitapauksia ennen ajoa rapsojen avulla
* sipohttp-lokitus /dev/shm:lle io-viiveiden takia
* Tiedoksi: Harjoittelija aloittaa 1.11.2023
* Emmi:
  * Timmi-palaveri pidetään keskiviikkona 11.10. klo 12.30 

### Maanantai 2.10.2023 klo 9

Läsnä: Anneli, Emmi, Pasi, Lari, Johanna, Kodo, Lasse, Ari

* jokainen kirjaa jatkossa omat kertomansa/käsittelemänsä asiat muistioon
* pidetään viikosta 41 lähtien yksi pidempi palaveri maanantaisin ja muina viikonpäivinä klo 9 max 15 minuutin palaveri.
  * Lastulaisille viestiä, että aloitetaan ke-palsut 9.15
* Lari:
  * vanhentuneet maksut, lisätään credit-tapahtuma (EXPIRED) ja debit-puolella muutetaan vanhentuneen maksurivin amountoutstanding nollaksi.
  * cinast, tarjottu borrowers/statusta
* Emmi:
  * Tasku-Warkaudelle pyydetty pääsyä Kohan rajapintaan
    * mallia Siilinjärvestä/Haminasta (API-avain toimitettu Katjalle)
  * Timmi-tilanvarausjärjestelmä
    * sovitaan palaveri (sovittu 11.10 klo 12.30), Lari mukaan  
* redusointipalaveri, Anneli kysyy pääkäyttäjistä halukkaita mukaantulijoita
* bugi-perjantain bugien etsintä Annelin, Larin ja Emmin kanssa klo 13

## Viikon 39 muistiot

### Torstai 28.9.2023 klo 10

Läsnä: Anneli, Emmi, Pasi, Lari, Johanna, Kodo, Lasse, Ari

* [Syntymäaikojen poistoajolle](https://github.com/KohaSuomi/Koha/issues/778) tekijä
* Vanhentuneet maksut -poistoajoa kaipailtiin pääkäyttäjäpalsussa.
  * miten tehdään? (write off?)
    * luodaan uusi credit-maksutyyppi "Vanhentuneen maksun mitätöinti" tms., tunnukseksi EXPIRED
      * pyydetään pääkäyttäjiä luomaan uusi credit-tyyppi
    * luodaan päivittäin ajettava cron
    * tehdään raportti, jolla saa tarvittaessa haettua kirjanpitoon merkittävän luottotappion määrän eli lasketaan yhteen EXPIRED-maksut accountlines-taulusta.
  * kuka tekee?
    * Lari
  * aikataulu?
    * Lari aloittaa heti koodaamaan ja ensimmäinen ajo, kunhan pääkäyttäjät ovat lisänneet uuden credit-tyypin.
    * testataan ensin testillä.


### Maanantai 25.9.2023 klo 9

Läsnä: Anneli, Pasi, Johanna, Lasse, Kodo, Lari, Emmi, Ari

* "Bugi-perjantait" - milloin aloitetaan?
  * "Bugiton" perjantaina 13.10.2023 klo 13-15
* [Tulossa: metatietowebinaari](https://www.kirjastot.fi/ammattikalenteri/koulutus-ja-seminaarit/tulossa-metatietowebinaari?language_content_entity=fi) 27.11.2023 (Koha-seminaaria edeltävä päivä)
* Kirkes-matrixin ja repon "sulku" lokakuun aikana.
* Viikon 39 päivitys

## Viikon 38 muistiot

### Torstai 21.9.2023 klo 10

Läsnä: Anneli, Ari, Emmi, Johanna, Lasse, Lari, Pasi

* Mitä tehdään Versionvaihto-projektissa oleville version 22.xx-tiketeille?
  * siirto Tikettien seuranta -projektiin? Vai jotain muuta?
  * Annetaan olla Versionvaihto-projektissa ja pyritään saamaan ne valmiiksi ennen 23-versiota.
* Entä siirretäänkö 22.xx-tiketit Koha-repoon?
* Tilastointiliitännäisen, Raportteri (Gispositio), rajapinta PowerBI:lle, mikä näiden keskinäinen rooli ja tilanne?
  * voiko Raportterin kautta tuotettuja JSONeja hyödyntää PowerBI:n osalta? Emmi ehdottaa palsua Turun kanssa.
  * Raportterin osalta odotetaan edelleen Helsingin kaupunginkirjastosta uusia palvelintietoja.
  * keskustellaan asiantuntijaryhmässä päällekkäisistä tilastointiratkaisuista
    * tarvitaanko tilastointiliitännäiseen muita kuin okm-tilastot, jos tietoja viedään PowerBI:hin.
* Cinast.fi lähestynyt Aria rajapintayhteyttä pyytäen. Lari vastaa tarjoten borrowers/status-endpointia.
* Vkon 39 päivitys

### Maanantai 18.9.2023 klo 9

Läsnä: Anneli, Ari, Emmi, Johanna, Lari, Lasse, Pasi

* [YSO-konversion](https://github.com/KohaSuomi/Koha/issues/390) vastuutus ja aikataulutus
  * Johanna ja Emmi ottavat työn alle
* Kodo ja Lari tekee Lastun käyttöönoton.

## Viikon 37 muistiot

### Torstai 14.9.2023 klo 10

Läsnä: Anneli, Pasi, Emmi, Ari, Lasse, Lari, Kodo

* Viikon 38 päivitys

### Maanantai 11.9.2023 klo 9

Läsnä: Anneli, Lari, Pasi, Emmi, Lasse, Kodo

* Huoltoikkuna ke 13.9.2023
  * palvelimien buuttaus, kaikki nodet käytetään alhaalla
* Viikon päivitys
  * ei tehdä, jotta ei aiheuteta Kirkesläisille heti ensimmäisenä aamuna katkoa
* Kirkeksen aloitus ti
  * crontabin tarkistus ja ajastus maanantaina: Lari tekee
    * process_messages vasta ti
    * ei valutusta
    * ei tilastoja
    * ei editx
    * ei laskutus


## Viikon 36 muistiot

### Torstai 6.9.2023 klo 10

Läsnä: Lasse, Emmi, Pasi, Ari, Lari, Kodo

* Timmi-tilanvarauspalvelu (Mäntyharju/Lumme)
  * Timmiltä pyydetty Kohan ja Lumme-Finnan rajapinta tiedot tarjouksen laatimisen avuksi
  * Toimitettu kehotus pyytää Finna-rajapinnan tiedot Finna-toimistosta sekä kuvaus borrower/status-endpointista 

### Maanantai 4.9.2023 klo 9

Läsnä: Anneli, Lasse, Emmi, Pasi, Ari, Lari, Kodo

* [Viestiasetusten muutos asiakastyyppiä vaihtaessa #755](https://github.com/KohaSuomi/Koha/issues/755)
* Tätissä indeksoitumattomia tietueita
  *  Pasi korjaa tietueet illalla.
* Kirkeksessä indeksointi- ja virhe 500 -ongelmia.

## Viikon 35 muistiot

### Torstai 31.8.2023 klo 10

Läsnä: Anneli, Emmi, Pasi, Lari, Lasse, Ari

* Tikettien vastuutus
  * [ Kausijulkaisun vastaanottoon Lisää tulostuslistaan -valintamahdollisuus #508](https://github.com/KohaSuomi/Koha/issues/508) - hyväksytty jo asiantuntijaryhmässä
  * [Tietueen varaukset-sivulta puuttuu Ensimmäinen ja Viimeinen -linkit sivutuksesta #523](https://github.com/KohaSuomi/Koha/issues/523)
  * [Asiakastiedot: uuden muotoinen henkilötunnus ei tallennu #745](https://github.com/KohaSuomi/Koha/issues/745)
  * [Lumme: cardnumber-userid-yhtenäistämisajo](https://github.com/KohaSuomi/Koha/issues/741)
* Tuodaan [Template Toolkit error](https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=32442)
* Kirkes-muistettavaa
  * okm ja biblio_data_elements-taulu
  * cronit
  * triggerit
  * valutus
  * valuebuilderit ja plugarit
  * editx jossain vaiheessa
* siirretään maanantain palaverit alkamaan klo 9, jotta Ari ehtii paremmin olemaan mukana palaverissa. Kokeillaan, onko muutoksesta apua. Muutos viikosta 36 lähtien.
 
### Maanantai 28.8.2023 klo 10

Läsnä: Anneli, Pasi, Emmi, Lasse, Lari, Ari

* Päivystykset viikosta 36 eteenpäin
* Viikon 35 päivitys
  * Finna-pluginin päivitys
  * Käännösmuutos
  * Ceepos-logitus
* Lumpukoiden virhe 500 -ongelmat/haravointi
  * ainakin palautuksessa tulee toisinaan virhe 500 -ilmoituksia. Kaivataan lisää esimerkkejä, jotta ongelmaa saisi paremmin selvitettyä
    * ongelman kohdanneita virkailijoita pyydetään myös tyhjentämään selaimesta välimuisti ja evästeet, jotta voidaan sulkea pois niistä johtuvat ongelmat.
  * haravoinnissa oli ongelmia, joka johtui kahdesta tietueesta, joiden tiedot löytyi sekä biblio että deletedbiblio-taulusta. Tietojen poisto biblio-taulusta auttoi ja haravointi Finnaan onnistui taas. 
* Kirkeksen aloituksesta uutinen?
* Yhteiskäyttöinen tekstienmuokkauspaikka tiedotteille yms.
  * ei oikein löydy mitään ilman, että pitää itse hostata.
* Koha-repon wikiin luotu uusi sivu ["Ongelmatilanteita ja niiden ratkaisuja"](https://github.com/KohaSuomi/Koha/wiki/Ongelmatilanteita-ja-niiden-ratkaisuja)

## Viikon 34 muistiot


### Torstai 24.8.2023 klo 10

Läsnä: Anneli, Emmi, Kodo, Lari, Lasse, Pasi

* Tärkeää olisi saada aineistotyyppi näkyviin tiettyihin raportteihin kätevästi. Pitäisi saada bibliodataelements-tauluun omaksi sarakkeekseen. Tällöin vältyttäisiin taulujen liitoksilta?
  * todettiin, että aineistotyyppi löytyy jo biblio_data_elements-taulusta
  * Emmi tarkentaa dokumentaatiota ja lisää taulun tiedot sinne
* Tätistä Kirjastopalvelun tietueet/päiväpaketi Melindaan, mikä järkevin toimintatapa?
  * OAI-PMH
  * päiväpakettien välitys Kirjastopalvelulta suoraan Melindalle?
    * Emmi kyselee Melinda-slackissa olisiko tämä mahdollinen toimintatapa, koska se olisi teknisesti kaikista yksinkertaisin tapa.
    * jos paketit pitää sopimusteknisistä syistä tulla meidän kautta, niin myös me voisimme suorittaa välittämisen.
* [Ilmoitukset-välilehden hitaus](https://github.com/KohaSuomi/Koha/issues/691#issuecomment-1689957259) - Mikon kommentti
  * pyydettiin esimerkkiasiakkaan borrowernumber ja testaillaan

### Maanantai 21.8.2023 klo 10

Läsnä: Anneli, Pasi, Emmi, Lari, Lasse, Kodo

* Tulevaisuus-workshopin kuulumiset?
* Viikon 34 päivitys?
  * Lari tekee ma-iltana
  * Anneli kirjoittaa tiedotteen
* Nextit
  * jouduttaneen odottamaan seuraavaan huoltokatkoon, jotta saadaan ensin nostettua file handlejen määrää
  * valmistellaan sitä odotellessa omilla koneilla 
* Lari hoitaa triggerit ja ruksien poistot projektina:
  * puhelinnumeron kopioiva triggeri kaikille ensin päivitys
  * ajo, että numero on sekä mobilessä että smsalertnumberissa
  * ajo, jolla vieksiruksit pois niiltä, joilla ei ole smsalertnumberia
  * ruksien poistavat intranetuserjs-rimpsu kaikille

## Viikon 32 muistiot

### Torstai 10.8.2023

Läsnä:

**Aiheet**

* Voiko tuoda meille korjauksen [tikettiin 630?](https://github.com/KohaSuomi/Koha/issues/630)
  * Tuodaan
* Message_queue-taulun lukot: vaihtoehtoinen toteutus? [Lukkototeutus lisätty digest-viestejä varten](https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=15854)
  * yritetään keskustella ongelmasta KohaConissa
* [Niteiden muokkaukseen/lisäykseen nidetyypin automaattinen valinta #336](https://github.com/KohaSuomi/Koha/issues/336) - toteutetaanko plugarina vai value builderina?
  * Emmi työstänyt value builderina
  * puretaan editx:stä viime vuonna (?) tehty ratkaisu hyllypaikan valintaan
* [Kausijulkaisujen numeroinnin järjestäytyminen #544](https://github.com/KohaSuomi/Koha/issues/544), korjaus ei toimi ilman templatemuutosta. Kannattaako tehdä paikallisesti ja mennäänkö kauemmaksi yhteisökoodista?
  * järjestämistä ei saada virheettömästi toimimaan ilman julkaisupäivämäärää, koska kenttä ei ole numeerinen.
  * ei mielellään template-muutoksia, varsinkaan kun ongelma johtuu puuttellisesta datasta
  * ratkaisu: kaikki käyttää kausijulkaisujen vastaanottoa ja julkaisu-kenttään laitetaan vastaanottopäivä (reklamoiduilla, jälkikäteen tulleilla julkaisupäivä)
* JSON Reports -palvelu
  * keskusteltiin JSON Reportista ja tutkitaan asiaa lisää.
* Pitäiskö ens viikosta tehdä jokin tiedote Discussionsiin?
* Kansalliskirjastosta tuli tiedote: Melindan REST-API päivitetään viikolla 32, tämä saattaa aiheuttaa huoltokatkoja.
* Suomi.fi-viesteissä tehdään huoltotöitä lauantaina 26.8.2023 klo 8.00–22.00. Tarkempi viesti suomi.fi-lootassa.

### Maanantai 7.8.2023

Läsnä: Anneli, Lari, Ari, Kodo, Pasi, Lasse, Emmi

**Aiheet**

* Vkon 32 päivitys
  * ei päivitettävää
* Oulussa ja Turussa tällä viikolla tilastodata-palaverit, pitäiskö Kodon osallistua kumpaankin?
  * Oulun 9.8. klo 9, Turun 11.8. klo 12
  * Emmi ja Lari ja Kodo + Anneli
* liitännäisten dokumentaatiot - readme vai wiki?
  * kehittäjien dokumentaatio Readmehin ja pääkäyttäjien dokumentaatio wikiin.
* onko säännöllistä huoltokatkoa 9.8.?
  * ei ole huoltokatkoa

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-32-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 31 muistiot


### Torstai 3.8.2023 klo 10

Läsnä: Anneli, Ari, Lasse, Lari, Pasi

**Aiheet**

* 503 service unavailabe -katkos tullut outissa tällä viikolla tiistaina 1.8.2023 klo 9.36 maissa ja keskiviikkona 2.8.2023 klo 9.36 aikoihin.
  * Lari lisää OUTIin viestien lähetykseen rajoituksen, että lähetetään viestejä vain maksimissaan 1000 kerralla. Testataan, onko sillä mitään vaikutusta.
  * MariaDB:lle on olemassa liitännäinen, jolla saa näkyviin, mikä prosessi on lukinnut taulun. Keskustellaan sen asentamisesta, kun Kodo palaa lomilta.
* KohaCon
  * onko meiltä esityksiä?
    *  ei ole, mutta yritetään puhua tulevaisuus-osiossa ja muissa epävirallisissa tilanteissa Bibframesta.
  * mihin laitetaan junalippujen kulut?
    * eFinaan päivärahat, junaliput liitteeksi 
  * päivystykset
* nexteille seuraava versio - aikataulu?
  * KohaConin jälkeen, jos tarvitsee conissa esitellä meidän versiota
* Lastu-kirjastot Koha-Suomi-karttaan?
  * Lisätään karttaan tiedolla "syksyllä 2024"
* [Tarkan haun hakutuloksia ei esitetä järjestelmäasetuksessa valitun mukaan](https://github.com/KohaSuomi/Koha/issues/579) - tuodaanko nykyiseen vai odotetaanko, että tulee seuraavan version mukana?
  * tuodaan
* Kiireellinen? [Sähköpostina lähetettävien noutoilmoitusten lähettäjäosoite muuttunut](https://github.com/KohaSuomi/Koha/issues/616)
  * Lasse tutkii

### Maanantai 30.7.2023 klo 10

Läsnä: Anneli, Lasse, Pasi, Lari, Ari

**Aiheet**
* Asiakasvarmenteiden teko ja jako pääkäyttäjille
  * pääkäyttäjien muistiossa lista, kenelle toimitetaan (Matrixissa) missäkin kimpassa
  * Lari hoitaa
* Service unavailable -ongelmat
  * tehdään vuositaulut viesteille -> Lari hoitaa, tehdään uusi tiketti
  * saattaisi johtua siitä, että perl lukitsee taulun, kysely jää niin pitkäks aikaa pyörimään että perl-prosessi tapetaan, ja sitten taulun avaavaa perl-koodia ei ajeta koska se prosessi tapettiin
* Viikon 31 päivitys
  * [Koha #668](https://github.com/KohaSuomi/Koha/issues/668)
  * Vaskin tekstiviesteissä ei näy vieraat kirjaimet

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-31-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 30 muistiot

### Maanantai 24.7.2023 klo 10

Läsnä: Anneli ja Lasse

* Siilissä ssh connection warning: Failed to fetch keys for xxx from remote (KSMessaging) su 23.7.2023

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-30-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 29 muistiot

### Torstai 20.7.2023 klo 10

Läsnä: Anneli, Lasse

* Vaskissa service unavailable 503 ma 17.7.2023 klo 13.05 aikoihin. table lock, lastseen-arvojen kirjauksia jonossa. Kyselyt ei tahtonut kuolla pois.
* OUTIssa service unavailable 503 to 20.7.2023 klo 9.36 aikoihin, ei table lockia tai jumiutuneita kyselyjä. Pelkkä korefresh auttoi.
* kokouksen ulkopuolelta tieto ylös, että OUTIssa ollut vastaava katko myös ke 5.7.2023 n. klo 9.38. Katko oli mennyt ohi itsestään. Matrix-keskustelujen perusteella silloin on näkynyt lokeilla read erroreita ja proxy erroria: The timeout specified has expired: ja sitten toinen proxy error AH10154: pass request body failed to 0.0.0.0:0
 
### Maanantai 17.7.2023 klo 10

Läsnä: Anneli, Lasse

* OUTIssa oli vkolla 28 tiistaina 11.7.2023 klo 9.06 maissa ja Vaskissa keskiviikkona 12.7.2023 klo 12.59 maissa Koha alhaalla hetken aikaa ja tietokanta ilmoitti  "Waiting for table metadata lock". Ilmeisesti message_queue-taulu menee taas lukkoon herkästi.
  * OUTIn kohdalla syy saattoi olla Annelin kysely message_queue-tauluun, Vaskin osalta Mikko testaili Ilmoitukset-välilehden hitautta ja joutui tappamaan selaimen prosessin. Ei varmuutta, johtuiko käyttökatko juuri noista, mutta osuvat ajallisesti samoihin aikoihin.
* Ei päivitystä
* asiakasvarmenteiden jakelu siirtyy vkolta 30 seuraavalle viikolle, kun paikalla on henkilöitä, joilla on pääsy palomuurille.

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-29-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 28 muistiot

### Maanantai 10.7.2023 klo 10

Läsnä: Anneli, Lari ja Lassi

* Viikon 28 päivitys:
  * OKM-plugarin päivitys: uusi sarake [publication_year](https://github.com/KohaSuomi/koha-plugin-OKM-stats/issues/8)
  * [Palautuskuittiin ei tule palautettujen lainojen tietoja, jos laina- ja palautuskirjasto ovat erit #449](https://github.com/KohaSuomi/Koha/issues/449)
  * [Listan kautta tietueiden erämuokkaus](https://github.com/KohaSuomi/Koha/issues/574)

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-28-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 27 muistiot

### Torstai 6.7.2023 klo 10

Läsnä: Lasse, Lari, Kodo, Emmi

* Viikon 28 päivitys:
  * OKM-plugarin päivitys: uusi sarake publication_year
* Yhteisön tiketti [33734](https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=33734)
  * Lasse hoitaa
* Biblioitems.datereceived on edelleen kiinni MARC-pohjissa kentässä 942$1
  * pääkäyttäjille hoksautus 

### Maanantai 3.7.2023 klo 10

Läsnä: Lasse, Lari, Kodo, Emmi

* Varmenteiden luominen
* Keravan laskutuspalaveri 30.6. klo 9 /Emmi
  * laskut kulkevatkin Lowellin eteenpäin kautta eli yhteys on muodostettava Kohan ja Lowellin välille
  * Lowelliin oltu yhteydessä Keravan kunnan toimesta 
* Käytiin läpi laskutustyökalun käyttöönotto
  * lisätään ohjeistusta vielä työkalun [wikiin](https://github.com/KohaSuomi/koha-plugin-overdue-tool/wiki)  

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-27-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 26 muistiot

### Torstai 29.6.2023 klo 10

Läsnä: Emmi, Kodo, Lasse

* Keravan laskutuspalaveri 30.6. klo 9
  * paikalla Sarastian, Keravan kaupungin ja Koha-Suomen väkeä, pyydetään mukaan myös joku kirkesläinen

### Maanantai 26.6.2023 klo 10

Läsnä: Emmi, Kodo, Lasse

* Deleted-taulujen aikaleimojen korjauksia ohjelmassa tänään.

* Lapin korjaus sovittu tehtäväksi 4.7. kello 8 aamulla.

* Kuntasovelluksesta keskusteltu nykyään Koha-Suomen hallituksessa istuvan Tiia Häsän kanssa. Pidetään asiasta palaveri Hionin kanssa elokuussa kesälomien jälkeen.

* Kirkes-data on saatu kantaan poistamalla ongelmia aiheuttaneet niteet. Osalla niteistä kuvailutietueen id ei vastaa Aurorassa 001-kentässä olevaa tietue-id:tä. Tämä korjattiin tällä konversiokierroksella tarkistamalla kaikkien niteiden kuvailutietue-id:t ja poistamalla käsin ongelmaniteet. Dumppien toistuvista virheilyistä reklamoitu Axiellia, joka kuitenkin ehtii selvittelemään ongelmia vasta heinäkuun puolella. Tutkimukset täällä meidän päässä jatkuvat.

* Tilastointi-plugin käyttää nyt deleted_on-saraketta poistoissa. Jos sarake on tyhjä, käytetään timestamp-saraketta.

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-26-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 25 muistiot

### Torstai 22.6.2023 klo 10

Läsnä: Lasse, Emmi, Kodo, Lari, Ari

* Viikon 26 päivitys
  * [Vanhenemispäivä jää puuttumaan varaukselta, jolta perutaan odottaa tai kuljetettavana -tila #650](https://github.com/KohaSuomi/Koha/issues/650)

* Deleteditems ja deletedbiblioitems taulujen biblioitemnumberit oikaistu muualla paitsi Lapissa, jossa oikaisu vaatii hieman erilaista lähestymistapaa.

* Deleted* -taulujen päivityksessä taulujen timestampit muuttuivat, joka voi aiheuttaa poistotilastoihin virheitä.
  * Korjataan deletedbiblioitemsien timestamp vastaamaan vastaavan deletedbiblion timestamppia.
  * Korjataan deleteditemsin timestamp vastamaamaan datelastseeniä, jotta virheelliset timestampit eivät sotke tämän kuun tilastoja (datelastseen lienee vähiten väärä käytettävissä oleva tieto)

* Deleteditems-tauluun on uutuutena tullut deleted_on -kenttä, mutta se on toistaiseksi suurimmalla osalla tietueita tyhjä
  * Ajetaan deleted_on kentään tietueen timestamp ja muutetaan tilastointia niin että tietueen poistoajankohdan määrittelyyn käytetään ensisijaisesti deleted_on -kenttää. Tämä poistaa jatkossa timestamppien muuttumiseen liittyvät ongelmat tauluja päivitettäessä.

* Lapin korjaus on hahmoteltu tiketissä #606.

* Korjausta ei ole vielä lisätty re-align -skriptiin, sen toteutus täytyy miettiä erikseen.

* Siilinjärven, Haminan ja Varkauden kuntasovelluksesta keskusteltu ohjelmistotoimittajan (Hion) kanssa.
  * Keskustelu jatkuu edelleen, pyritään pitämään tästä tekninen palaveri mahdollisimman pian.
  * Toteutettuna on käytännössä Finnan kanssa rinnakkainen, mutta toiminnoiltaan huomattavan riisuttu kuntakohtainen verkkokirjastototeutus.
  * Kodon testauksissa esimerkiksi kirjastokortin liittäminen Haminan sovellukseen ei onnistunut, vaan tuloksena on "Virhe, tarkista kentät ja yritä uudelleen."
  * Sovelluksen haku tuntuu palauttelevan vähän mitä sattuu ja teoksista esitettävät tiedot ovat erittäin suppeat. Esimerkiksi osakohteiden emot kyllä tuntuvat tarttuvan hakuun, mutta teostiedoissa ei ole mitään mainintaa osakohteista. Muutenkin tietojen suppeuden vuoksi on hyvin hankala hahmottaa mikä tietueessa tarkalleen ottaen vastasi hakua. Usein vastaavuutta ei näyttäisi olevan lainkaan, Esimerkiksi "Siiri ja Hurja Hunskeli" tuskin vastaa millään tavalla hakua "Totalimmortal". Hakutuloksia tuntuu saavan hieman vaihtelevasti ja sama haku palauttaa eri hakukerroilla eri tuloksia. Teoksen tekijänä näkyy usein toimitetuissa teoksissa teoksen toimittaja, joka ei ole tekijä jne.

### Maanantai 19.6.2023 klo 10

Läsnä: Lasse, Emmi, Kodo, Lari

* Viikon 25 päivitys
  * OKM-plugin: bde-tauluun on lisätty sarake biblionumber, lisäksi taulun päivityksen yhteydessä haetaan myös sieltä puuttuvat tietueet (aiemmin tämä onnistui vain tekemällä ajo force vivun kanssa)
  * Tietueen niteiden järjestäminen lehtinumeroinnin mukaan [#544](https://github.com/KohaSuomi/Koha/issues/544)
  * Asiakastaulukon sarakkeiden piilotus Varauksenteko-sivulla [#571](https://github.com/KohaSuomi/Koha/issues/571)
  * Taustatöiden siivousskripti päivittäin ajettavaksi [#618](https://github.com/KohaSuomi/Koha/issues/618)

* [deleted-tauluissa biblioitemnumberin ja biblionumberin epäsynkka #606](https://github.com/KohaSuomi/Koha/issues/606)
  * Kodo lisää deleted-taulujen korjauksen realign-skriptiin

* Ceepos-ongelma ratkaistu
  
* Kohan oma lokitus puutteellista, Kodo tutkii

* Parilta kimpalta vielä tekemättä ajo jolla kopioidaan asiakkaan puhelinnumero smsalertnumberista mobileen

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-25-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 24 muistiot

### Torstai 15.6.2023 klo 10

Läsnä: Emmi, Kodo, Lari, Lasse, Pasi

* Maanantai-illan käyttökatko
  * Kyseessä oli runkoverkko-ongelma, eli meidän kannalta jo "neljännen osapuolen (Ficix) järjestelmässä ollut toimintahäiriö.

* Pluginien releaset
  * Hypernova toivoisi että plugineista tehdään releaset.
  * Ei tässä vaiheessa tehdä, koska aiheuttaisi meidän kannalta turhaa työtä.
  * Releasen voi rakentaa halutessaan itse käyttämällä deploy-skriptiä.

* Integraatioasioita
  * Tilausten vastaanoton automatisointi eli Puppe (Vaski)
    * Palaveerattu nyt ohjelmistotoimittajan (Broomworks kanssa) Kodon koollekutsumana.
    * Paikalla oli Koha-Suomelta Kodo, Vaskista Anni Rajala, Kaisa Hypén ja Aki Pyykkö ja Broomworksilta Urho Kaipainen.
    * Viedään aineistontoimittajan sanomatunnus EDItX hankinnoissa aqbasket-taulun booksellernote -kenttään tilausten täsmäytystä varten.
    * Varmistetaan booksellernoten hyödynnettävyys API:n kautta.
    * Lari hoitaa Koha-Suomen suunnassa eteenpäin.
    * Kodo toimittaa API-avaimen Vaski-testille Broomworksia varten ja Anni tekee tunnukset Kohaan.
  * Kokoelman tasapainotustyökalu (Vaski)
    * Palaveerataan ohjelmistoitoimittajan kanssa kunhan toimittaja on valittu. Vaski kutsuu kokouksen koolle.
    * Tutkitaan mahdollisuutta saada kuljetusten painomatriisin automaattinen optimointi mukaan työkaluun.
    * Toteutus vielä täysin avoin ja vaatii monenlaista selvittelyä.
  * PowerBI (Vaski ja muut)
    * Vaskissa rakenneltu raportteja datan saamiseksi Kohasta PowerBI:hin.
    * Toiveissa datan siirron automatisointi Kohasta muihin järjestelmiin.
    * Vaski avaan keskustelun PowerBI-ryhmässä.
    * Tärkeää löytää yhteiset Koha-Suomen laajuiset käytännöt ja vakioitu datapaketti, ei kuntakohtaisia ratkaisuja!
  * Tasku-Warkaus (Varkaus)
    * Äkkipäätä vaikuttaisi siltä että Varkaudessa ollaan rakentamassa omaa verkkokirjastoa, johon ei tietenkään ole tarvetta, koska kansallinen ratkaisu on jo olemassa.
    * Yhteystiedot saatu Lumme-kimpan pääkäyttäjältä, järjestetään palaveri ja käydään läpi mitä ollaan tekemässä ja miksi, Kodo kutsuu koolle.

* Integraatioista "paimenkirje" kirjastoille. Koha-Suomi ja pääkäyttäjät on pidettävä kartalla siitä mitä aiotaan tehdä ja integraatioiden toteutuksesta on sovittava Koha-Suomen kanssa ennakkoon.

### Maanantai 12.6.2023 klo 10

Läsnä: Emmi, Pasi, Ari, Lasse, Lari, Kodo

* [Lumme: Kohan rajapinnan avaus mobiilisovellukseen](https://github.com/KohaSuomi/Koha/issues/639)

* Raahen laskutus: Nyt lähtee eteenpäin.
  * raahelaskutus-domain on .ssh/config:ssa, ssh-avainten tarkistus valittaa, Kodo korjaa

* Lumme haravointi valittaa 500-virhettä
  * Logissa: _DBIC result _type isn't of the type BiblioMetadata at /home/koha/Koha/Koha/OAI/Server/Repository.pm line 181.
  * Vaikuttaa siltä kuin bibliolla ei olisi biblio_metadata-taulussa vastaavaa riviä

* Lappi 500-virhe tietueessa, jossa ei 942-kentässä ollut osakenttää
  * Luetteloijan korjattava

* Varausten vanhentuminen cron
  * Ei laiteta käyttöön, Kohassa on nykyisin DefaultHoldExpirationDate -järjestelmäasetus jolla saa asetettua automaattisesti
  * Onko tuossa asetuksessa bugi, kun varaukset eivät vanhene? Emmi tutkii.

* Lapin biblionumber/biblioitemnumbereiden renumerointi ja synkkaus: Emmi korjaa.

* MARC-virhelistaan: ilmottaako se xml-virheistä, ne pitäisi näkyä paremmin. Pasi muuttaa.

* Tiistain päivitys
  * Vaara: SIP-viesteissä tulee mukaan PA-kenttä, laitetaan vähitelle myös muille kimpoille

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-24-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 23 muistiot

### Torstai 8.6.2023 klo 10

Läsnä: Pasi, Ari, Lasse, Lari, Kodo

* Tietokantapalvelimien synkkausviive
  * slave-palvelimella oli pari kauan kestänyttä raporttia, ja yksi "Waiting for table metadata lock"; seurataan asiaa.

* Kirjastokortin viivakoodin esittäminen asiakkaan tietonäytöllä
  * Voidaan toteuttaa, ei tarvitse käyttää asiantuntijaryhmässä
  * Pasi tutkii voidaanko toteuttaa esimerkiksi JavaScriptillä intranetuserjs:ään, Kodo tekee tiketin

* Svean kanssa yritetty löytää yhteisymmärrystä SSH host-avainten skannauksesta. Svean palvelin blokkaa yhteyden jos tietyn ajan sisällä tulee liikaa pyyntöjä. "Liikaa pyyntöjä" on tässä tapauksessa neljä ja ssh-keyscan lähettää viisi pyyntöä avainskannauksella.

* Laskutus Raahessa ei edelleenkään toimi, laskut eivät mene perille Raahen palvelimelle #634
  * Kodo tutkii tiedonsiirtoyhteyttä

* Finna-haravointi on rikki Lumpeessa ja Lapissa, kysymyksessä ilmeisesti viallinen kuvailutietue, johon koko homma kaatuu.

* set_expirationdate_for_holds.pl täytyy siirtää utilityyn #631, Lasse hoitaa

* Lumpeessa otettu toistaiseksi käyttöön debug-lokitus, koska ongelmia Lumpeissa tuntuu olevan kaikenlaisia kummallisia ongelmia #611.
  * Tilanne on outo, koska Lumme-Koha on sama kuin kaikilla muillakin, vian on melkein pakko olla Lumpeen datassa.

### Maanantai 5.6.2023 klo 10

Läsnä: Emmi, Pasi, Ari, Lasse, Lari, Kodo

* [Seuraava yhteisön kehittäjien irc-tapaaminen 7.6.2023](https://wiki.koha-community.org/wiki/Development_IRC_meeting_7_June_2023)

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-23-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 22 muistiot

### Torstai 1.6.2023 klo 10

Läsnä: Anneli, Emmi, Pasi, Ari, Lasse, Lari, Kodo

* Pääkäyttäjät kysyy: onko tulossa testeille uudempi sisältö (asiakkaat, tietueet yms.) (lähiaikoina)?
  * Pasi päivittää
  * redusoituun kantaan isompi setti tietueita, asiakkaita, lehtitilauksia. Osakohteita enemmän. Enemmän erilaisissa nidetiloissa olevia niteitä. Asiakastiedot: asiakkailta puuttui huollettavia ja varauksia -> helpompi, jos asiakkaan kaikki huollettavat, varaukset ja lainat otettaisiin mukaan. -> Määrät mietintään vko 23 pääkäyttäjäpalsussa

* Pääkäyttäjäpalsusta: varmenne toivottiin vanhenemaan kesälomajan ulkopuolelle ja ehdotettiin toukokuuta.
  * Koha-Suomi pitäisi varmenteen vaihtoajankohdan mielummin syksyllä. Keskustellaan asiasta lisää pääkäyttäjien kanssa loppuvuodesta.

* Pääkäyttäjien palaveriin osallistuminen Annelin loman aikana.
  * Päivystäjät osallistuvat palavereihin ja tiedottavat esim. päivityksistä

* Versiopäivityksen tietokantamuutosten jakaminen Hypernovalle?
  * Emmi ja Kodo katselee läpi skriptit ja jaetaan sitten Hypernovalle

* Miten saataisiin testilaskuja Kirkes-testiltä Sarastialle?
  * Kirkesläisille laitettu ohjeita laskutustyökalun käyttöön ja konfiguraatioon.
  * Testilaskut voi tehdä työkalulla valmiiksi.
  * sanoman muodostamiseen ja lähettämiseen tarvitaan sitten kehittäjien apua.
  * Emmi ja Lasse avuksi

* Omituisia puhelinnumeroiden katoamisia ja muuttumisia raportoitu ainakin OUTIssa ja Kyytissä:
  * [OUTI: asiakkaan tiedoissa on ruksattuna noutoilmoitus tekstiviestinä, mutta puhelinnumero SMS-kentästä puuttuu #607](https://github.com/KohaSuomi/Koha/issues/607)
  * [OUTI: Asiakkaalle muuttunut vanha puhelinnumero matkapuhelin- ja tekstiviesti numeroon -kenttiin #608](https://github.com/KohaSuomi/Koha/issues/608)
  * Onko jotain tehty meillä ke 17.5.2023 klo 21 jälkeen?
    * Ei ole
  * Anneli testaa vielä erilaisia skenaarioita, mitkä voisi tyhjentää numerot

*  [deleted-tauluissa biblioitemnumberin ja biblionumberin epäsynkka #606](https://github.com/KohaSuomi/Koha/issues/606)

*  [Lumme: 500-virhe tehtäessä kirjaston perustoimintoja #611](https://github.com/KohaSuomi/Koha/issues/611)

*  Tikettien vastuutus

*  Taustatyöt
  * Kaikissa indeksoinneissa raportissa _/ tietuetta indeksoitu onnistuneesti. Joitain virheitä esiintyi._, vaikka indeksointi tuntuisi kuitenkin onnistuneen. -> Anneli tekee tiketin
  * Anneli tekee tiketin jonon siivoamisestakin

* noreply(at)koha-suomi.fi osoitteesta Kohasta koha-suomi.fi-päätteisiin osoitteisiin lähetetyt viestit feilaa: _Recipient address rejected: User unknown in local recipient table_

* Varausten noutoilmoitukset lähtevät versionvaihdon jälkeen kirjaston osoitteesta eli kirjaston tiedoissa olevasta replyto-osoitteesta, eikä kirjaston osoitteesta, jossa on noreply(at)koha-suomi.fi-osoite.
  * MariaDB [outiprod]> select message_id,to_address,from_address,reply_address from message_queue where borrowernumber=246585 order by 1 desc limit 1;

| message_id | to_address                    | from_address                 | reply_address |
|---|---|---|---|
|   10891322 | anneli.osterman(at)koha-suomi.fi | kaijonharju.kirjasto(at)ouka.fi | NULL          |




### Maanantai 29.5.2023 klo 10

Läsnä: Anneli, Emmi, Ville, Pasi, Ari, Lasse, Lari, Kodo

* Vaskin asiakasvarmenne vanhenee jo elokuussa
  * uusi varmenne kaikille jakoon ma 24.7.2023
  * muilla kimpoilla uusi ja vanha pidempään

* [Tietueen tuominen TäTistä Vaaraan ei tuo oikeaa tallennuspohjaa](https://github.com/KohaSuomi/Koha/issues/592)

* Tekstiviestien merkistöongelmat LinkMobilityn kanssa.

* Lapin realign
  * biblioitemnumberit saadaan luultavasti korjattua nappaamalla niiden arvoksi rivin biblionumberin arvo
  * lisätään tämä näiden korjaus realign-biblionumber-biblioitemnumber.sh skriptiin

* Vkon 23 päivitys
  * Käännöskorjauksia:
    * [Kaksi käännösvirhettä liittyen takaajiin/taattaviin #577](https://github.com/KohaSuomi/Koha/issues/577)
    * [Käännösvirhe taustatyön tiedot -sivulla #11](https://github.com/KohaSuomi/Koha-translations/issues/11)
  * [Taustatöissä hitautta](https://github.com/KohaSuomi/Koha/issues/582)

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-22-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 21 muistiot

### Torstai 25.5.2023 klo 10

Läsnä: Anneli, Emmi, Ville, Pasi, Ari, Lasse, Lari, Kodo

* Lapin realign ei onnistunut /Emmi

* Asiantuntijaryhmässä päätetty purkaa varauksenteko-sivun taulukon piilotus. Jotta se voidaan tehdä, mitää tiketin [Varauksenteko-sivulla ei toimi asiakastaulukon sarakkeiden piilotus](https://github.com/KohaSuomi/Koha/issues/571) ongelma ensin korjata. Vastuutus.

* Päivystysvuorot viikosta 23 eteenpäin.
* [Lomat githubin yhteystiedot-wikiin](https://github.com/KohaSuomi/Koha/wiki/Koha-yhteystiedot)

* Vkon 23 päivitys
  * Käännöskorjauksia:
    * [Kaksi käännösvirhettä liittyen takaajiin/taattaviin #577](https://github.com/KohaSuomi/Koha/issues/577)
    * [Käännösvirhe taustatyön tiedot -sivulla #11](https://github.com/KohaSuomi/Koha-translations/issues/11)

### Maanantai 22.5.2023 klo 10

Läsnä: Anneli, Emmi, Ville, Pasi, Lasse, Lari, Kodo

* tiistain päivityksen sisältö
  * [KohaSuomi/Koha/Kausijulkaisujen vastaanotossa ei toimi viivakoodinmuodostus #539](https://github.com/KohaSuomi/Koha/issues/539)
  * [KohaSuomi/Koha/Realign-korjauksen ajo kimppoihin #548](https://github.com/KohaSuomi/Koha/issues/548)

* [tutkitaan, saako Print summary -tulosteen siirrettyä viestipohjiin.](https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=11340)

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-21-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 20 muistiot

### Perjantai 19.5.2023 klo 10

Läsnä: Anneli, Emmi, Ville, Pasi, Lasse, Lari, Kodo

* päivityksissä paluu normaaliin eli tiistai-aamuihin. Ellei kyseessä ole kriittinen korjaus.

* pääsääntöisesti versionvpäivitys meni hyvin.
  * päivityksen jälkeen tuli esille ongelmia, joita ei ollut huomattu testeissä. Osa saatiin korjattua tiistaina/keskiviikkona, lopuista tehdään tiketit ja tutkitaan sitä mukaa kun ehditään.


### Maanantai 15.5.2023 klo 10

Läsnä: Anneli, Emmi, Ville, Pasi, Ari, Lasse, Lari, Kodo

* Tuotannon kopiointi, nextiltä vai testiltä?
  * koskee konttipohjia
  * Päätös: next

* Emmi ja Kodo aloittaa päivityksen ma-iltana klo 10.

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-20-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 19 muistiot

### Torstai 11.5.2023 klo 10

Läsnä: Anneli, Emmi, Ville, Pasi, Ari, Lasse, Lari, Kodo

* cronit, milloin laitetaan päälle versionvaihdon aikaan?
  * onnistuuko ODUE-viestien lähetys jälkikäteen? (muistaakseni onnistuu /AÖ)
  * saako duedst- ja preduedgs-viestit muodostettua tiistaina? (saanee /KK)
  * **Päätös:** Luodaan viestit jonoon ja lähetetään ne, kun viestiliikenne taas käynnistetään. Tieto lisätty versionvaihdon muistiinpanoihin.

* Lumpeelta kysellään voiko stopata/stopataanko viestiliikenne sulun ajalta?
  * **Päätös:** Sovitaan Lumpeiden kanssa, koska heidän viestiliikenne käynnistetään.

* [Tietokantatriggerit päivityksen jälkeen heti käyttöön?](https://github.com/KohaSuomi/Koha-22x/issues/137)
  * varmistettava, että esim. kirjastokortin numero tulee kopioiduksi userid-kenttään joko triggerillä tai js-rimpsulla.
  * **Päätös:** Lisätty versionvaihdon muistiinpanoihin

* Editx-virheviestin lähetysajankohta
  * ongelmana elasticsearch-virheestä muodostuvat vialliset tilauskorit
  * Ei onnistu helposti, tutkitaan elasticsearch-virheen syytä tarkemmin versionvaihdon jälkeen.

* KOHA_AUTO_FETCH ympäristömuuttujan voi asettaa joko /etc/environmentissa tai komentorivillä export KOHA_AUTO_FETCH=1 ennen buildia.
Se hakee/päivittää kaikki ksdev/* branchit. Ei voi käyttää tuotannossa.

* Lari testaa Ceepos-maksuja emulaattorissa


### Maanantai 8.5.2023 klo 10

Läsnä: Anneli, Lasse, Lari, Ari, Emmi, Ville, Kodo, Pasi

* lomat kalenteriin
* versionvaihdon tilanne
* käännökset?

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-19-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 18 muistiot

### Torstai 4.5.2023 klo 10

Läsnä: Anneli, Lasse, Lari, Ari, Emmi, Ville, Kodo

* versionvaihdon tikettien tilanne

* koha-suomi.fi-sertifikaatti vanhenee 20.5.2023
  * Kodo muistuttaa Bittigurua hoitamaan sertifikaatin uusimisen.

### Tiistai 2.5.2023 klo 10

Läsnä: Anneli, Lasse, Lari, Ari, Emmi, Ville, Kodo

* Mitä tehdään Koha-repositoriolle versiopäivityksessä. Koodikanta pitäisi saada päivitettyä siten että vanha koodi säilytetään myös "jossain", tai homma pitäisi saada hoidettua muuten elegantisti niin että tiketit, wikit ja diskussiot pysyvät matkassa.
  * Luodaan uusi repo Koha-21x ja kloonaataan nykyinen Koha-repo siihen?
  * Päivitetään Koha-repon sisältämä koodikanta Koha-22x version mukaiseksi? Miten?
  * Päivitetään test-kannat uuteen versioon ke 10.5.2023

* Ceepoksessa 503 virhe
  * testataan keskiviikkona lisää

* [Z39.50-haku tiputtaa 001-kentästä BTJ:n kontrollinumeron pois](https://github.com/KohaSuomi/Koha-22x/issues/171)
  * Pääkäyttäjäpalsussa päätettiin, että otetaan käyttöön vanha 001-liitännäinen järjestelmäasetuksen tilalle.

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-18-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 17 muistiot

### Torstai 27.4.2023 klo 10

Läsnä:

* [Keskiviikon käyttökatkos](https://github.com/KohaSuomi/Koha/discussions/520)

* Versionvaihdon tilanne

### Maanantai 24.4.2023 klo 10

Läsnä: Anneli, Emmi, Lasse, Pasi, Lari, Kodo, Ville

* Versionvaihdon tikettien läpikäynti
  * Tiketit käytiin läpi ja kirjoitettiin kommentit tiketteihin.
  * Arvioitiin versionvaihdon aikataulua.

* Käytiin suppeasti läpi Kirkes-kimpan tietoturvavaikutusten arviointiraportti.

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-17-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 16 muistiot

### Torstai 20.4.2023 klo 10

Läsnä: Anneli, Pasi, Emmi, Ville, Lari, Lasse, Ari, Kodo

* Käyttöhäiriö 19.4.

* Lokilevelit eri konteissa, ehdotus:
  * tuotannot: error
  * testit: warn
  * nextit: warn
  * kehitysympäristöt: debug/trace/info

* Tikettien [Raporttien kyselyiden siirtäminen tietokantaslavelle - ksdev/ks-0082-KD-5239-altdbh](https://github.com/KohaSuomi/Koha-22x/issues/163) ja [Raporttien kyselyiden siirtäminen tietokantaslavelle - ksdev/ks-0083-KD-5239-use-altdbh-for-reports](https://github.com/KohaSuomi/Koha-22x/issues/164) vastuutus

* [Työkaluliitännäiset/Tulosta ilmoituksia - viestin poistomahdollisuus tulostussivulle](https://github.com/KohaSuomi/Koha/issues/505)
  * Kehitysehdotus, mutta voisiko tästä ottaa Villelle pienen projektin ilman että tarvii käyttää tätä asiantuntijaryhmän kautta?
* Kaukolainat Raportointi(OKM)-plugarissa
  * OKM- tilastoihin ei pitäisi laskea kaukolainoja (joillakin kimpoilla on laskettu), mutta esim. Vaara haluaa kaukolainat kuukausitilastoihin
  * tällä hetkellä asetukset mahdollistavat vain joko-tai-tilanteen
  * [Valmiissa SQL-raporteissa](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Valmiita_SQL-raportteja#Kaukolainat) on kaukolainoihin liittyviä kyselyjä. Riittäisikö ne siihen saakka, kunnes raportointityökaluun saadaan kaukolaina-osio toimimaan?

* Labyrintti sertifikaatti 25.4.2023

* Elasticsearch-herjoja alkanut tulemaan taas EDItX-tilausten käsittelyssä.

* Versionvaihdon tikettien vastuutus

* Koha-Suomen po-tiedostot -> luodaan uudet kun perustiedot-näytön ja hakutulos-näytön muutokset tehty.

### Maanantai 17.4.2023 klo 10

Läsnä: Emmi, Kodo, Lari, Lasse, Pasi, Ville

* [Jos DefaultHoldExpirationdate on asetettu, varauksen aloituspäivä menee asetuksen mukaiseksi](https://github.com/KohaSuomi/Koha-22x/issues/42) - ei etene yhteisössä tarpeeksi nopeasti, mitä tehdään? Tiketti [Varauksen voimassaoloaika ei päivity](https://github.com/KohaSuomi/Koha-22x/issues/104) on myös riippuvainen tästä korjauksesta.
  * viedään yhteisöön korjaus ja tuodaan korjauksineen meille

* Patet olleet pois päältä viikonlopun Suomi.fi-huoltokatkon vuoksi
  * Sovittu viikon 14 palaverissa, mutta tarkoitus oli poistaa käytöstä ainoastaan suomi.fi -viestit, nyt pois päältä oli suomi.fi:n lisäksi myös kirjeviestintä. Ei kuitenkaan vahinkoa tapahtunut, koska kusti ei kuitenkaan polje viikonloppuna. Viikonloppuna muodostuneet kirjeet lähtevät maanantaina.

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-16-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 15 muistiot

### Torstai 13.4.2023 klo 10

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi, Ville

* ruotsinkieliset käännökset

* tietokanta-ajot suurin osa tehty, outissa vielä muutama ajo tekemättä.

* kontrollerin vaihto meni ok. Loppujen lopuksi sinne oli vaihdettu vain levy, joka oli mennyt rikki.

### Tiistai 11.4.2023 klo 12

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi, Ville

* [Ilmoitusten kieli -valinnaksi oletuksena Suomi](https://github.com/KohaSuomi/Koha-22x/issues/154)
  * Pystyttäneen toteuttaa

* Kontrollerin vaihto keskiviikkona vaikuttaa suunniteltuihin tietokanta-ajoihin.
  * Emmi tekee old_issues-taulun ajon ti-ke yönä, koska niissä menee kauimmin aikaa, eikä ole varmuutta, että ne valmistuvat 8.30 mennessä, jolloin kontrollerin vaihto alkaa.

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-15-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 14 muistiot

### Torstai 6.4.2023 klo 10

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi, Ville

* Suomi.fi paperipostitukseen liittyvä käyttökatko 15.4.2023 klo 10.00–18.00
  * Pasi laittaa cronin tauolle perjantaina ja ma-päivystäjä laittaa cronin taas päälle.

* Finnassa huolto tiistaina 11.4.2023 klo 13 - 15

* tikettien tilanne, versionvaihtoon reilu kuukausi
  * käytiin läpi tilannetta.

* KohaPerlCon, Call for papers
  * laitetaan discussionsiin Kansalliskirjaston ilmoitus.

* [Järjestelmäasetus: DebarmentsToLiftAfterPayment - ksdev/ks-0006-bug-16223](https://github.com/KohaSuomi/Koha-22x/issues/49)
  * Anneli kyselee pääkäyttäjien viikkopalaverissa, käyttääkö tätä ominaisuutta joku kimppa.

* Huhtikuun huoltokatko
  * tehdään skeemamuutoksia, Emmi testaa testeillä kauan muutoksissa menee.
  * skeemapäivitysten aikaan katkot ovat mahdollisia.
  * ei muuta

* Viikon 15 ma-palaveri siirretään pääsiäisen takia tiistaille klo 12.

### Maanantai 3.4.2023 klo 10

Läsnä: Anneli, Lari, Emmi, Ville, Pasi, Lasse, Kodo

* versionvaihdon tiketit
  * muista sulkea tiketti, kun piikissäsi oleva tiketti on saanut 2-3 hyväksyvää testausta.

* kerrattiin parin viikon aikana tulleet ongelmat ja tapahtumat

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-14-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 13 muistiot

### Torstai 30.3.2023 klo 10

Läsnä:

* Versionvaihdon aloitusajankohta, eli kellonaika?
  * ma 15.5.2023 klo 22

* tikettien vastuutus

* palvelimen kuorma

* Apache-konfiguraatiot

* Heikkisen Antti kyseli slackista erään tietuepaketin tilasta, onko kellään näistä havaintoa miten pitäisi päivittyä?
  * Kellään ei tietoa, mitä listan tietueet ovat. Odotetaan Johannan paluuta.

* [Kirkekseen numerointikaavat ja ilmestymistiheydet](https://github.com/KohaSuomi/Kirkes/issues/9)

* tieteellisten versionvaihto-ongelmat

### Maanantai 27.3.2023 klo 10

Läsnä: Anneli, Emmi, Ari, Lari, Pasi, Lasse

* Apache-konfiguraatiot (skel/setEnv:it mm. MEMCACHED NAMESPACE/lastu/MV/OPAC-konffi/http redirect? https://linuxize.com/post/redirect-http-to-https-in-apache/)
  * Keskustellaan torstain palsussa

* Päivystysvuorot viikosta 14 eteenpäin

* Lumpeesta ei ole lähtenyt printti viestejä 13.2. alkaen
  * Sama ongelma kuin viime vuoden lopulla, yksi viallinen zip-tiedosto estää kaiken liikenteen
  * Emmi poistaa viallisen zipin
  * tsekit ei ole valittanut pending-tilaisista viesteistä jostain syystä

* Ke klinikka, ketkä mukana?
  * Ari, Anneli ja Lari

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-13-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

## Viikon 12 muistiot

### Torstai 23.3. klo 10

Läsnä: Anneli, Emmi, Ari, Lari, Pasi, Lasse

* Testattaviin testaussuunnitelma + tikettien ajantasalla pito

* Tikettien vastuutusta

* Emmi tutkii valutuksen käyttöönottoa

* Lari ajaa nexteille käännökset, kun saa skriptin kuosiin.


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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-12-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-11-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-10-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-9-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-8-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-7-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-6-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-5-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-4-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-3-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-2-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)

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

[Palaa viikon muistioiden alkuun](https://koha-suomi.fi/kohasuomi2023#viikon-1-muistiot) - [Palaa sivun alkuun](/kohasuomi2023)
