---
title: 'EDItX-hankinta'
permalink: /dokumentaatio/editx/
redirect_from:
  - /theme-setup/
toc: true
---

EditX on avoimiin standardeihin perustuva ja helposti laajennettava tapa siirtää tietoja aineistontoimittajien ja Kohan välillä. Sen avulla pystytään toimimaan Kohan hankinnan suhteen samalla tavalla riippumatta aineistontoimittajasta.

![](/assets/files/docs/Ohjeet/editx.PNG)

## 1. Käyttöönotto Kohassa

Kohassa pitää tehdä seuraavia määrityksiä, jotta tietueiden yhdistely ja tilaussanomien käsittely toimii oikein.

### 1.1 Kohan tilit ja verkkokaupan korit

Kohaan on määriteltävä tietynmuotoiset tilit. Tilien tilikoodi pitää olla muodossa _kirjastolyhenne - hyllypaikkalyhenne - budjettivuosi_, esim.

OUPKAIK2019<br />
OUPK = kirjaston lyhenne Kohassa<br />
AIK = hyllypaikan lyhenne<br />
2019 = budjettivuosi

OUPKLN2019<br />
OUPK = Oulun kaupungin pääkirjasto<br />
LN = Lasten ja nuorten hyllypaikka<br />
2019 = budjettivuosi<br />

MUPKAIK2019<br />
MUPK = Muhoksen kirjasto<br />
AIK = Aikuisten hyllypaikka<br />
2019 = budjettivuosi<br />

*Huomioitavaa:* EditX-tilauksissa käytettävien tilien täytyy olla hyllypaikan mukaisia. Ei voida käyttää esim. AV-tiliä, jos sen nimistä hyllypaikkaa ei ole olemassa Kohassa.

*Lisähuomioitavaa:* Kirjaston lyhenteeseen pitää ottaa mukaan koko kirjaston lyhenne eli se, mikä on tallennettu Kohan ylläpidossa kirjastolle lyhenteeksi. Jos lyhenne on kaksiosainen, pitää koko tunnus ottaa mukaan, esim. JOE_ENO tai MLI_ANT.

![](/assets/files/docs/Ohjeet/kirjastojahyllypaikka.png)

Tilien luonnissa on mahdollista tehdä
* Joka vuosi uudet tilit samassa muodossa, vain vuosiluku vaihtuu.
* Ikitilit, jotka ovat nimensä mukaisesti "ikuisesti" voimassa, esim. OUPKAIK2999. Vuosiluku on tässäkin tapauksessa oltava mukana.

Toimittaja luo verkkokauppaansa tilejä vastaavat korit. Katso tarkempi ohje kohdasta _Käyttöönotto aineistontoimittajan verkkokaupassa_.  Korin nimi on vapaa, mutta tilin Koha-tilikoodi täytyy tulla tilaussanomassa FundNumber-elementissä. Esim.


Kori: AIK2019<br />
FundNumber: OUPKAIK2019<br />
DestinationLocation: OUPKAIK2019<br />
DeliverToLocation: OUPKAIK2019

Yhdellä korilla tilataan yhdelle kirjastolle ja yhdelle hyllypaikalle. Verkkokaupassa on siis oltava kori jokaiselle hyllypaikalle, jolle tilataan.

#### 1.1.1 Ikitilit

Jos käytetään ikitiliä voi tehdä myös niin, että kunnalla on Kohassa yksi tili esim. OUPK2999, joka tulee EditX-sanomassa kohtaan FundNumber. Kirjasto- ja hyllypaikkatieto tulee tällöin DestinationLocation/DeliverToLocation -kohtaan muodossa kirjaston lyhenne - hyllypaikan lyhenne - vuosiluku eli OUPKAIK2999. Käytännössä tämä tarkoittaa, että verkkokaupassa pitää todennäköisesti olla niin monta koria kuin mitä kirjasto/hyllypaikka-yhdistelmiä tarvitaan.

Kori 1 - Oulun pääkirjasto/Aikuiset:<br />
FundNumber: OUPK2999<br />
DestinationLocation/DeliverToLocation: OUPKAIK2999

Kori 2 - Oulun pääkirjasto/Lapset ja nuoret:<br />
FundNumber: OUPK2999<br />
DestinationLocation/DeliverToLocation: OUPKLN2999

Kori 3 - Oulun pääkirjasto/Musiikki:<br />
FundNumber: OUPK2999<br />
DestinationLocation/DeliverToLocation OUPKMUS2999

Ja niin edelleen, kunnes kaikki halutut kirjasto/hyllypaikkayhdistelmät on katettu.


### 1.2 Kohan toimittajatieto

Kohassa pitää olla (kuntakohtainen) toimittajatieto olemassa jokaiselle toimittajalle, jolta aineistoa tilataan, esim. Oulu Kirjastopalvelu.

Lisäksi sanomassa oleva aineiston toimittaja pitää liittää Kohan toimittajatietoon. Liitosta varten tarvitaan sanoman _VendorAssignedID_ ja sitä vastaava Koha-aineistotoimittajan id-tunnus. Sen näkee toimittajatiedoissa selaimen osoiteriviltä.

!editx6.png!

#### 1.2.1 Kohan toimittajatiedon mäppääminen toimittajan asiakastunnukseen

Kohan aineistotoimittajan liittäminen tilaussanoman toimittajatietoon tehdään käyttöliittymässä Hankinnan EDI-tilit sivulla. Sivulle pääsee myös Ylläpito-sivun kautta (Ylläpito → Hankinnan asetukset → EDI-tilit).

Valitse _Uusi tili_

![](/assets/files/docs/Ohjeet/editx5.png)

Täytä seuraavat kohdat

![](/assets/files/docs/Ohjeet/editx7.png)


* **Toimittaja:** Valitse toimittajatieto alasvetovalikosta.

* **Kuvaus:** Kuvaus on vapaaehtoinen.

* **Siirto:** Valitse "FILE".

* **Määre:** Kenttään valitaan 
** _Assigned by supplier (91)_ käytettäessä sanoman VendorAssignedID:tä
** _Assiegned by buyer (92)_ käytettäessä sanoman BuyerAssignedID:tä

* **SAN:** Kenttään tulee joko VendorAssignedID tai BuyerAssignedID, riippuen siitä, kumpaa halutaan käyttää.

* **Tilaukset sallittu*:* Laita tähän ruksi.

Valitse _OK_.

Lisätty EDI-tili tulee näkyviin EDI-tilien listalle. Olemassaolevia tilejä voi muokata valitsemalla _Muokkaa_. Tilin voi poistaa _Poista_-painikkeella.

![](/assets/files/docs/Ohjeet/editx8.png)

### 1.3 Authoriser eli tilauksen luoja

Kohaan täytyy luoda EditX-tilauksille _Authoriser_. Tämä on Kohan käyttäjätunnus, joka näkyy EditX tilauksissa tilauksen luojana. Tunnus ei tarvitse mitään oikeuksia. Katso [[1_Asiakkaat#11-Lisää-uusi-asiakas|Asiakkaan lisäys]].

Authoriser:in borrowernumber määritetään EditX-rajapinnan konfiguraatiossa (*anteeksi, jäi kaksi suomenkielistä sanaa). Tämän tekee pyynnöstä järjestelmänkehittäjä.

### 1.4 Kohan MARC-määritykset

*Huomaa:* Nämä määritykset on tärkeä tehdä, jotta kuvailutietueiden tuplakontrolli toimii oikein.

Tietueiden täsmäytys tehdään tilaussanoman MARCXML:n ja Kohan tietokannan biblioitems-taulun perusteella. Täsmäytykseen käytetään seuraavia biblioitems-taulun kenttiä:

* isbn
* ean
* publishercode + editionresponsibility

Kohan MARC-määrityksissä pitää olla seuraavat määritykset:

* ISBN-numero MARC-kentästä 020$a liitetään biblioitems-taulun kenttään _isbn_.
* EAN-koodi MARC-kentästä 024$a liitetään biblioitems-taulun kenttään _ean_. Indikaattoria ei huomioida.
* Julkaisijan tunnus MARC-kentästä 028$a liitetään biblioitems-taulun kenttään _publishercode_.
* Julkaisija MARC-kentästä 028$b liitetään biblioitems-taulun kenttään _editionresponsibility_.
** publishercodea ja editionresponsibilityä käytetään täsmäytyksessä aina yhdessä. Vain jos kumpikin täsmää, syntyy vastaavuus.

!editx2.png!

Aina kun kenttäliitoksia muutetaan, pitää vanhojen tietueiden tiedot päivittää ajan tasalle (misc/batchRebuildBiblioTables.pm --downstream --confirm). Järjestelmänkehittäjä tekee tämän pyynnöstä.

*Huomaa:* On mahdollista, että liitos näyttäisi olevan paikoillaan, vaikka ei oikeasti olekaan. Tarkista siis aina liitos _Muokkaa_-painikkeen takaa.

### 1.5 ONIX-aineistolajien määritys

Kohan tietokannassa on _map_productform_-taulu, jossa liitetään tilaussanoman "ONIX-aineistotyypit":https://ns.editeur.org/onix36/en/7 Kohan aineistolajeihin. Liitokset tekee järjestelmänkehittäjä heille toimitetun vastaavuuslistan perusteella.

Vastaavuslistan esimerkkitiedosto: attachment:map_productform_uusi.xlsx

---

### 1.5.1 Vaihtoehtoiset hyllypaikkamääritykset (ONIX-aineistolajien vaihtoehtoiset määritykset)

Tietokannassa Map_productfrom taulussa on kaksi nidetyyppi-saraketta (productform ja productform_alternative).

Ensisijaisesti käytetään productform-sarakkeen arvoa. Jos halutaan käyttää productform_alternative arvoa, niin procurement-config.xml tiedostoon määritellään asetus <productform_alternative_triggers></productform_alternative_triggers> ja sen sisään hyllypaikat pilkulla eroteltuna, joille halutaan productform_alternative-sarakkeen arvon nidetyyppi.
Esim.
```
<productform_alternative_triggers>LAP,NUO</productform_alternative_triggers>
```

### 1.6 Tietueiden täsmäytys eli tuplakontrolli

EDItX-sanomista luodaan tilauksen luonnin yhteydessä minitietue kaikista niistä teoksista, joita ei löydy ennestään tietokannasta. EDItX-sanomassa on jokaiselle teokselle kuvailutieto MARCXML-muodossa. Ennen kuin uusi tietue luodaan, tarkistetaan, löytyykö tietokannasta jo kyseinen teos. Vertailuun/täsmäytykseen käytetään biblioitems-taulun ISBN (020$a), EAN (024$a), ja publishercodea (julkaisijan tunnus 028$a) yhdessä editionresponsibilityn (julkaisijan nimen 028$b) kanssa (kumpikin pitää täsmätä). Jos millään standarditunnisteella ei löydy Kohan biblioitems-taulusta, niin luodaan uusi tietue. Jos löytyy vastaavuus, käytetään tilauksen luonnissa kyseistä tietuetta ja niteet luodaan olemassa olevaan tietueeseen.

Tietueiden täsmäytyksessä on tällä hetkellä puute, joka aiheuttaa tuplatietueita tietokantaan. Jos tietueella on biblioitems-taulun ISBN- tai EAN-sarakkeessa kaksi tai useampi tunniste, ei täsmäytys toimi. Jos tunnisteita on useampi, erotetaan ne |-merkillä toisistaan. Täsmäytys pyrkii täsmäyttämään koko sarakkeen sisältöön, jolloin esim. yhdellä ISBN-numerolla haettaessa tieto ei täsmää sarakkeen tietoon. Tästä on tehty kehitysehdotus, että täsmäyttäjä osaisi purkaa sarakkeen sisällön palasiksi ja täsmäyttää tunnisteen kumpaankin/kaikkiin tietoihin erikseen.

---

## 2. Käyttöönotto aineistontoimittajan verkkokaupassa

Aineistontoimittajan verkkokaupan täytyy tukea EditX-tilaussanomien lähettämistä. Selvitä asia ennakkoon toimittajasi kanssa. Tällä hetkellä EditX-tilaussanomia käyttää Booky/Kirjastopalvelu, Kirjavälitys sekä Woiman hankintaportaali.

Verkkokaupoissa on tehtävä seuraavat määritykset:

* tilauskori pitää määrittää EditX-tilaussanomia ”muodostavaksi”
* tilauskoriin pitää määrittää FundNumber, DeliverToLocation ja DestinationLocation -elementteihin Kohan tilikoodi
* aineistotoimittajatiedot SellerParty/PartyName/NameLine -elementissä: Tunnistettuja aineistontoimittajia ovat 'Kirjavälitys Oy', 'Booky.fi Oy' ja 'BTJ Finland Oy'. 
** Aineistontoimittajien nimien tulee olla sanoman SellerParty/PartyName/NameLine -elementissä täsmälleen tässä muodossa, esimerkiksi 'KV' ei ole tunnistettu aineistontoimittaja eikä rajapinta osaa sen perusteella arvata että kyseessä on Kirjavälitys Oy.


Toimittajalta pitää tilata tilauskorit ja niihin pitää tehdä seuraavat määritykset. Esim.

Aikuisten hyllypaikalle: FundNumber, DeliverToLocation ja DestinationLocation OUPKAIK2019
Lasten ja nuorten hyllypaikalle: FundNumber, DeliverToLocation ja DestinationLocation OUPKLN2019
Musiikki-hyllypaikalle: FundNumber, DeliverToLocation ja DestinationLocation OUPKMUS2019

*Huomioitavaa:* Tili- ja sijoitustiedot ovat sidoksissa toisiinsa. Korien sijoitustietojen on vastattava Kohan kirjastoyksiköitä ja hyllypaikkoja. Sijoitustietona ei voi käyttää esim. OUPKAV2019, jos Kohassa ei ole olemassa AV-hyllypaikkaa.

Järjestelmänkehittäjä toimittaa Koha-palvelimen osoitteen, käyttäjätunnuksen ja salasanan aineistontoimittajille pyynnöstä.

Lisäksi tarvitaan tilaussanomissa oleva VendorAssignedID (toimittajan antama tunniste) tai BuyerAssignedID (kirjaston antama tunniste), jotta tilaukset pystytään muodostamaan Kohassa oikean toimittajatiedon alle. VendorAssignedID:n saa aineistontoimittajilta. BuyerAssignedID:n voi määritellä itse ja pyytää aineistontoimittajaa käyttämään sitä sanomassa.

---

## 3. Käyttöönoton määritykset Koha-palvelimella

Järjestelmänkehittäjä tekee nämä määritykset.

### 3.1 Käyttäjätunnus aineistontoimittajalle

Luo editx käyttäjä Koha-palvelimelle: _adduser --shell /usr/sbin/nologin editx_

Tätä tunnusta aineistontoimittajat käyttävät toimittaessaan tilaussanomat Koha-palvelimelle. Yhtä ja samaa tunnusta voidaan käyttää yhteisesti kaikille aineistontoimittajille.

Tipauta liiat oikeudet: _chmod 360 /home/editx_

Käyttäjän tarvitsee ainoastaan pystyä vaihtamaan kotihakemistoonsa ja kirjoittamaan sinne tiedostoja. Tiedostojen lukeminen ei ole tarpeen (toimittajien ei ole tarpeen lukea toistensa tilaussanomia).

Tulevan chrootin takia on hyvä vähän karsia myös /home -haaran oikeuksia. Käyttäjille riittää että he pääsevät /home:n kautta siirtymään kotihakemistoonsa. Ei ole tarpeen nähdä muiden käyttäjätilien kotihakemistojen nimiä saatikka kirjoittaa /home -haaraan mitään: _chmod 711 /home_

Muuta käyttäjän kotihakemiston sijainti osoittamaan tulevan chrootin juureen (huom! älä siirrä varsinaista kotihakemistoa!): _usermod -d /editx editx_

### 3.2 SFTP

Näihin tarvitaan root-oikeudet Koha-palvelimella. Lisää tämä /etc/ssh/sshd_config loppuun:

```
Match user editx
ChrootDirectory /home
X11Forwarding no
AllowTcpForwarding no
AllowAgentForwarding no
PermitTunnel no
ForceCommand internal-sftp -u 0707
```

Käyttäjä lukitaan /home -hakemistohaaraan ja ainoastaan ryhmälle jätetään oikeudet luotuihin tiedostoihin. Käynnistä tämän jälkeen sshd-uudelleen, jotta muutokset astuvat voimaan: _service ssh restart_

### 3.3 LXC

Valmistele mount bind containeria varten. Lisää containerin config -tiedostoon (root-oikeuksin hostilla) rivi:

```lxc.mount.entry = /home/editx /var/lib/lxc/[container]/[rootfs]/home/koha/koha-dev/var/spool/editx/tmp none defaults,bind 0 0```

Siirry containerin sisälle _ssh [container]_ tai _sudo lxc-attach -n [container]_, ja luo tarvittavat hakemistot: _cd ~/koha-dev/var/spool && mkdir -p editx/tmp editx/load editx/fail editx/archive editx/failed-archived_. Luo hakemistot Koha-käyttäjänä (eli jos siirryit containeriin lxc-attachilla, niin _su koha_ ensin), jotta hakemistojen omistajat asettuvat oikein.

Lisää editx-ryhmä + liitä siihen koha-käyttäjä: _sudo sh -c "addgroup --gid [GID] editx && usermod -a -G editx koha"_

editx ryhmän GID täytyy olla sama containerin sisällä kuin hostilla. Tarvittaessa GID:tä voi muuttaa _sudo groupmod -g [GID] editx_ -komennolla. Ryhmäoikeuden perusteella koha-käyttäjä saa kaikki oikeudet tilaussanomien käsittelyyn.

Poistu containerista takaisin hostille ja tee vielä containerin uudelleenkäynnistys hostilla: _sudo sh -c "lxc-stop -n [container] && lxc-start -d -n [container]"_ TAI vaihtoehtoisesti editx-hakemiston mount-bind hostilta containerin sisälle: _sudo mount --bind /home/editx /var/lib/lxc/[container]/[rootfs]/home/koha/koha-dev/var/spool/editx/tmp_.

### 3.4 Rajapinnan konfigurointi

Konfiguraatio on tiedostossa ~/koha-dev/etc/procurement_config.xml:

```
<?xml version="1.0"?>
<data>
    <settings>
        <import_tmp_path>/home/koha/koha-dev/var/spool/editx/tmp</import_tmp_path> <!-- The folder where files should be first put. The Integrations external entrypoint -->
        <import_load_path>/home/koha/koha-dev/var/spool/editx/load</import_load_path> <!-- The path from where the script reads files to import -->
        <import_archive_path>/home/koha/koha-dev/var/spool/editx/archive</import_archive_path> <!-- The path where files are archived after succesfull import-->
        <import_failed_path>/home/koha/koha-dev/var/spool/editx/fail</import_failed_path> <!-- The path where files are archived if something fails during import-->
        <import_failed_archived_path>/home/koha/koha-dev/var/spool/editx/failed_archived</import_failed_archived_path> <!-- The path where files are archived if something fails during import-->
        <authoriser>nnnnnn</authoriser> <!-- A borrowers id (borrowernumber) used in import, change this! -->
        <allowed_locations>LN,AIK,MUS,OU</allowed_locations>
        <productform_alternative_triggers>LAP</productform_alternative_triggers> <!-- The shelving location that is found in fundnumber, used for assigning productform_alternative from db map_productform-->
        <automatch_biblios>yes</automatch_biblios> <!-- Set to 'no' if you want to create a new biblio and biblioitem on every order. -->
    </settings>
    <notifications>
        <mailto>osoite1@ouka.fi,osoite2@ouka.fi,osoite3@ouka.fi</mailto> <!-- comma separated list of email-addresses to send error reports to -->
    </notifications>
</data>
```

Polkuihin ei yleensä tarvitse koskea, oletuspolut toimivat jos käyttöönotto tehdään tässä dokumentissa kuvatulla tavalla. Authoriser on Kohassa määritelty EditX-tilausten luoja (Kohaan tarkoitusta varten lisätyn editx-käyttäjän borrowernumber) ja allowed_locations kertoo mille hyllypaikoille aineistoa voi hankkia. Kuvailutietueiden tuplakontrollin voi halutessaan kytkeä pois muuttamalla automatch_biblios asetukseksi no. Silloin tilatuista nimekkeistä muodostuu aina uudet kuvailutietueet omine niteineen.

Notifications-osan mailto-elementissä määritellään sähköpostitse lähetettävien virhesanomien vastaanottajat.

### 3.5 Sanomien käsittelyn ja virhehuomautusten ajastus

Lisää seuraavat rivit containerin koha-käyttäjän crontabiin:

```
*/1 7-22 * * * $KOHA_CRONJOB_TRIGGER cronjobs/runEditXImport.pl
01 06 * * *    $KOHA_CRONJOB_TRIGGER cronjobs/notify-failed-editx.sh
```

Sanomat käsitellään klo 7.00-22.00 välisenä aikana minuutin välein tai niin nopeassa tahdissa kuin mahdollista. KOHA_CRONJOB_TRIGGER pitää huolen sanomankäsittelyskriptin lukituksesta. Sähköpostihuomautukset virheellisistä sanomista lähetetään kello 6.01 aamuisin.

---

## 4. Tilausten seuranta ja virheraportointi

### 4.1 EDIFACT-sanomat

*Huomattavaa:* Jotta sanomat voi nähdä, pitää käyttäjätunnuksella olla edi_manage-käyttäjäoikeus. 

Tilaussanomien käsittelyn etenemistä voi seurata hankinnan EDIFACT-sanomat -sivulla.

!editx3.png!

Kenttien selitteet:

* *Tyyppi* kertoo sanoman sisällön muodon (käytännössä aina EDItX).

* *Siirretty* kertoo päivän, jolloin sanoma on tullut palvelimelle.

* *Tila* kertoo sanoman käsittelyn tilan. Tilakoodit ovat:
** PROCESSING: käsittely on käynnissä
** POSTPONED: sanoma on joko virheellinen tai ei ole tullut palvelimelle vielä kokonaan
** FAILED: käsittely on epäonnistunut
** OK: käsitelty onnistuneesti

* *Toimittaja*-kenttään tulee aineistontoimittajan toimittajatieto, jos sellainen sanomasta löytyy ja se on liitetty Koha-toimittajaan.

* *Tiedot*-kentässä on linkki Koha-laskuun (ei käytössä).

* *Tiedostonimi* on sanoman tiedostonimi.

* *Toiminnot*
** _Katso viesti_ näyttää sanoman sisällön. Viesti-popparin sisältö on sekava, mutta siitä voi etsiä tarvitsemansa tiedon selaimen hakutoiminnolla (CTRL+F).
** _Poista_ poistaa rivin EDIFACT-sanomista, mutta ei poista tilausta eikä siihen liittyviä kuvailutietueita, niteitä ja varauksia.

### 4.2 Virheraportointi sähköpostitse

Virheisiin päättyneiden sanomien käsittelystä on mahdollista saada valittuihin sähköpostiosoitteisiin ilmoitus. Järjestelmänkehittäjä lisää osoitteet osoitelistalle pyydettäessä.

Esimerkkiviesti:

!editx4.png!

### 4.3 Erilaisia virhetilanteita

Aina virheviestiin ei saada poimittua järkeviä syitä käsittelyn epäonnistumiselle, mutta alla on muutamia esimerkkejä erilaisista virheviesteistä ja kuinka toimia.

#### Sanoma odottaa käsittelyä

Toisinaan sanomien käsittelijä ei saa käsiteltyä sanomia ja sanoma jää odottamaan. Tällöin lähetetään seuraavanlainen viesti:
```
Seuraavat EDItX sanomat odottavat edelleen käsittelyä:

/home/koha/koha-dev/var/spool/editx/tmp/EditxShipNotice_id_2353578_20200722062915.xml

Sanomien siirrossa aineistontoimittajalta Koha-palvelimelle on tapahtunut virhe
ja sanomat ovat puutteellisia.

Puutteelliset sanomat on jätetty hakemistoon /home/koha/koha-dev/var/spool/editx/tmp.
```

Käsittely voi epäonnistua koska
* tilaussanoma on tullut palvelimelle sellaiseen aikaan, jolloin sanomia ei käsitellä. Esim. myöhään illalla tai aikaisin aamulla.
** käy tarkistamassa EDIFACT-sanomat-sivulla hakemalla sanoman tiedostonimellä, onko sanoman käsittely edelleen kesken. Jos sanoman tila on ok, ei tarvitse tehdä korjausliikkeitä.
* tilaussanoma yritetään ottaa käsittelyyn kesken palvelimelle siirron
** käy tarkistamassa EDIFACT-sanomat-sivulla hakemalla sanoman tiedostonimellä, onko sanoman käsittely edelleen kesken. Jos sanoman tila on ok, ei tarvitse tehdä korjausliikkeitä.
** jos sanoman käsittely on epäonnistunut uudelleen, siitä tulee toinen viesti eri syyllä.

#### Virheellinen tai puuttuva FundNumber

Sanomassa voi olla virheellinen FundNumber eli tilikoodi tai sitten tilikoodi puuttuu Kohasta.

```
=== Sanoma: LibraryShipNotice_15373634_20200406115217.xml ===

2020-04-06 12.00.04 -- Error was: Cannot insert order: Mandatory parameter budget_id is missing at /home/koha/Koha/Koha/Procurement/OrderProcessor/Order.pm line 37.

Koskee: HEI_PKM2020
```

* Jos tilikoodi on väärin sanomassa, pyydä (pääkäyttäjä tai kimpassa asiasta vastaava) aineistontoimittajaa korjaamaan tieto oikeaksi heidän järjestelmässään.
* Jos tilikoodi on oikein, mutta se puuttuu Kohasta tai on virheellinen, pääkäyttäjä tai kimpassa tileistä vastaava käy lisäämässä tilin tai korjaamassa olemassa olevan oikeaan muotoon.

#### VendorAssignedID tai BuyerAssignedID mäppäys toimittajaan puuttuu

Jos sanomassa tulee mukana VendorAssignedID tai BuyerAssignedID, jota ei ole lisätty EDI-tilit sivulle Kohassa, niin tulee seuraava sanoma:

```
Seuraavien EDItX sanomien käsittelyssä oli ongelmia:

=== Sanoma: portaali_order_20200423103001.xml ===

2020-04-23 10.30.05 -- No vendor for SAN 267139 (qualifier 91) in vendor_edi_accounts.
2020-04-23 10.30.05 -- Error was: Died at /home/koha/Koha/Koha/Procurement/OrderProcessor.pm line 544.

Koskee: RAPKAIK2020
```

* Tarkista, onko tunnus (viestissä SAN xxxx) oikein ja lisää (pääkäyttäjä) tarvittava mäppäys EDI-tilit -sivulle
* jos tunnus on väärin, pyydä (pääkäyttäjä tai muu kimpan vastaava) aineistontoimittajaa korjaamaan VendorAssignedID tai BuyerAssignedID-tieto
* Vain joko VendorAssignedID tai BuyerAssignedID vaaditaan, molempia ei tarvitse määritellä. Mäppäykseen käytettävä ID-tyyppi määritellään EDI-tilit sivulla kohdassa 'Määre'.

#### Sanomasta puuttuu tieto aineistontoimittajasta tai tieto on väärässä muodossa

Rajapinta tunnistaa aineistontoimittajan sanoman sisällön perusteella. Tämän perusteella valitaan sanomalle kutakin toimittajaa vastaava oikea sanomankäsittelijä. Joskus esimerkiksi portaalisanomissa voi olla virheellisiä toimittajatietoja. Silloin tuloksena on tällainen virheraportti:

```
=== Sanoma: portaali_order_20201016132634.xml ===

2020-10-16 13.30.05 -- Required parameter: '$notes' was not set or it was empty.
2020-10-16 13.30.05 -- Error was: Required params not set. at /home/koha/Koha/Koha/Procurement/OrderProcessor.pm line 293.

Koskee: VAR_PKA2999
```

Tunnistettuja aineistontoimittajia ovat 'Kirjavälitys Oy', 'Booky.fi Oy' ja 'BTJ Finland Oy'. Aineistontoimittajien nimien tulee olla sanoman SellerParty/PartyName/NameLine -elementissä täsmälleen tässä muodossa, esimerkiksi 'KV' ei ole tunnistettu aineistontoimittaja eikä rajapinta osaa sen perusteella arvata, että kyseessä on Kirjavälitys Oy. Aineistontoimittajan tai hankintaportaalin tulee lähettää sanoma uudelleen korjatulla toimittajatiedolla.

#### Sanoma ei ole formaatin mukainen tai se on muuten puutteellinen

Joskus saapuva sanoma on viallinen, eikä ole XML-formaatin mukainen. Sieltä voi myös puuttua jotain pakollisia tietoja. Silloin sähköpostiviesti voi olla epämääräisempi.

```
=== Sanoma: portaali_order_20200423143002.xml ===

2020-04-23 14.30.05 -- Error was: :2: parser error : Start tag expected, '<' not found

Koskee: <DeliverToLocation/>

```

```
Seuraavien EDItX sanomien käsittelyssä oli ongelmia:

=== Sanoma: portaali_order_20200217145002.xml ===

2020-01-02 15.50.04 -- File: /home/koha/koha-dev/var/spool/editx/tmp/portaali_order_20200102155003.xml is not valid XML, processing postponed.
2020-02-17 14.50.07 -- Error was: :2: parser error : Start tag expected, '<' not found

Koskee: KEPKLN2020
```

* pääkäyttäjä voi tarkistaa EDIFACT-sivulla avaamalla viestin, puuttuuko sieltä jotain oleellista, kuten FundNumber, DestinationLocation, DeliverToLocation. Sanomaa voi verrata sellaiseen, jonka käsittely on onnistunut.
* pääkäyttäjä tai kimpan vastaava ilmoittaa aineistontoimittajalle, että sanoma on virheellinen ja pyytää korjaamaan tiedot.

#### Tietueella/niteellä on väärä aineistolaji

Tietueen aineistolaji (jatkossa aineistotyyppi) tallennetaan MARC-tietueessa 942c-kenttään. Niteen aineistolaji (jatkossa nidetyyppi) tallennetaan 952y-kenttään. Aineistolaji (jatkossa siis nidetyyppi ja aineistotyyppi) määrittyy tilaussanomassa olevan ProductForm-tiedon mukaan. Tagissa kerrotaan aineiston ONIX-koodi. "Lista product form -tyyppisistä ONIX-koodeista":https://ns.editeur.org/onix36/en/7. Tietokannassa taas on map_productform-taulu, jossa määritetään, mikä ONIX-koodi vastaa mitäkin Kohan aineistolajia. Oman kimpan määritykset voi tarkistaa SQL-kyselyllä 

```select * from map_productform```

Jos tietue/nide on mielestäsi saanut väärän aineistolajin (eli 942c-kentässä olevan aineistolajin tai niteen aineistolajin), käy ensin tarkistamassa EDItX-sanomasta teoksen ONIX-koodi. Jos se on väärä, kannattaa siitä laittaa palautetta sanoman toimittajalle.

EDItX-sanoman löytää esim. näin: 

* Mene teoksen tiedoissa Hankintatiedot-välilehdelle
* Klikkaa auki (toiseen välilehteen) (vanhimman) Tilauskorin linkki
* Kopioi Huomautus-riviltä EDItX-sanoman tiedostonimi ja aukaise (toiseen välilehteen) vasemmasta reunasta EDIFACT-sanomat sivu
* Liitä kopiomasi tiedostonimi EDIFACT-sivulla Haku-kenttään, jolloin se suodattuu näkyville. Klikkaa "Katso viesti".
* Sanoma on hankala lukea, mutta selaimen ctrl-f -toiminnolla pystyy hakemaan esim. nimekkeellä.
* ONIX-koodi löytyy ProductFrom-tagin sisältä. Huomaa, että jokaisella teoksella on oma taginsa, joten tarkista, että katsot oikeaa.

Toinen vaihtoehto on mennä Hankinnat-osioon ja hakea teoksen tilauskori esille hankintahaulla. Loppu menee yllä kuvatun mukaisesti.
