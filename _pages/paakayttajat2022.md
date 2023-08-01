---
layout: single
permalink: /paakayttajat2022
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
toc: true
title: 'Koha-Suomen pääkäyttäjäryhmän muistiot 2022'
---

Pääkäyttäjäryhmän viikkopalaverimuistiot vuodelta 2022.


## Viikko 52 muistio

Aika: 27.12.2022 klo 9.15
Läsnä: Anni Rajala (Vaski), Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Kati Sillgren (Helle)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-52-muistio)

**Yhteiset**
* Kirkes-kimpan järjestelmäasetusten läpikäyntiä ke 11.1.2023 klo 9-11.15. [Linkki kokoukseen](https://teams.microsoft.com/l/meetup-join/19%3ameeting_Y2JlMGUwZjgtNzk4OS00YmYxLThlNjgtOTIxZDg3NzAyMWIz%40thread.v2/0?context=%7b%22Tid%22%3a%225cc89a67-fa29-4356-af5d-f436abc7c21b%22%2c%22Oid%22%3a%229fb701ba-ed03-4130-af66-87d3c323bb9a%22%7d%3E). Tallennetaan tarvittaessa. Mukaan saa tulla kaikki haluavat, mutta pääpaino on Kirkeksen asioissa. :)

* [Versionvaihto-repositorio tehty](https://github.com/KohaSuomi/Koha-22.x)

* [Pääkäyttäjien ja Koha-Suomen yhteystiedot Koha-repositorion wikissä](https://github.com/KohaSuomi/Koha/wiki/Koha-yhteystiedot)
  * [Koha-Suomen yhteystiedot nyt myös Koha-Suomen nettisivuilla](https://koha-suomi.fi/yhteystiedot)

* Seuraava palaveri 3.1.2023 ja [muistiot uudessa osoitteessa Githubissa](https://koha-suomi.fi/paakayttajat2023)
  * muokkaus osoitteessa https://github.com/KohaSuomi/kohasuomi.github.io/blob/master/_pages/paakayttajat2023.md

**Vaski**
* Jonkin verran kirjastojen väliaikaisia sulkemisia / väistötilojen perustamista.
* Virkailija törmäsi tapaukseen, jossa toisena varausjonossa ollut varaus kiilasi palautuksessa jonon ensimmäisen ohi. Epäilys, että johtuisi samalla sekunnilla tehdystä uudesta varauksesta, mutta tehty kuitenkin tiketti Palautuksessa toisena ollut varaus kiilasi jonossa ohi https://github.com/KohaSuomi/Koha/issues/328.

**Lumme**
* Mäntyharjun kirjastolle vaihdettiin 15.12. noreply-osoite, ja tästä tuli jo palautetta että nyt sähköpostit ovat saavuttaneet asiakkaat. Muutos tehty nyt 27.12. myös Mikkelin seutukirjaston kirjastopisteille. 

**OUTI**
* Viikon 51 laskutuserästä oli jäänyt kolme laskua siirtymättä Kohasta Intimeen, koska laskutettavissa teoksissa oli ollut pitkiä nimekkeiden nimiä. Oulussa saman tägin väliin tulee myös viivakoodi ja nidetyyppi. Merkkimäärä ei saa olla pidempi kuin 100 merkkiä. Testataan niin, että tägiä, joissa nyt ovat nimeke, viivakoodi ja nidetyyppi, toistetaan niin, että jokainen tieto laitetaan omaan tägiin. Emmi oli myös ehdottanut, että viivakoodin ja nidetyypin voisi laittaa ArticleDescription-tägiin.
* Koulukirjaston entinen oppilas oli saanut palautuskehotuksia lainoista, joiden eräpäivät ovat olleet 2008 ja 2009. OUTIssa koulukirjaston aineistosta lähtee palautuskehotus, kun lainan eräpäivästä on kulunut 5000 päivää. Koulukirjaston vastaavalle kirjastonhoitajalle vinkattu raporttia, jolla voi hakea kirjaston vanhoja lainoja ja "siivota" pois ne entisiltä oppilailta, jos niitä ei haluta karhuta.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-52-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 51 muistio

Aika: 20.12.2022 klo 9.15
Läsnä: Pia Kusmin ja Leena Kinnunen (Lappi), Anneli Österman, Veli-Pekka Marjoniemi, Piia Semenoff, Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen ja Auli Rantasalo (Vaara), Kati Sillgren (Helle), Heli Auranen, Timo Pesonen (Lumme)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-51-muistio)

**Yhteiset**

* Uuden kehittäjän Lasse Pourun esittäytyminen
* Finna ja matkapuhelinnumeron kopioituminen Kohan kenttiin (https://github.com/KohaSuomi/Koha/issues/311)
  * pyydettiin, että kaikki tarkistavat, että Finnassa tehty puhelinnumeron muutos välittyy Kohassa sekä mobile (matkapuhelin) että smsalertnumber (tekstiviesti numeroon) -kenttiin, jotta kentät pysyvät keskenään synkassa. Tällä estetään tilanne, että asiakas muuttaa smsalertnumberin Finnassa, sen jälkeen virkailija käy tallentamassa asiakkaan tiedot ja mobile-kentästä triggeröityy vanha numero smsalertnumber-kenttään. Eli asiakkaan tekemä muutos menee "hukkaan".
  * kaikille laitetaan triggeri, joka kopioi tallennuksen yhteydessä mobile-kentän tiedon smsalertnumber-kenttään.
* [Pääkäyttäjien vuoden 2023 muistioiden muokkaussivu](https://github.com/KohaSuomi/kohasuomi.github.io/blob/master/_pages/paakayttajat23.md)
  * muokataan samalla tavalla kuin Kohan ohje suomeksi -sivuja.

**Lappi**
* Ensi vuoden hankinnan korit ja tilit tarkistettu.
* Ohjelmassa vuodenvaihteen käyttäjätunnusten tarkistaminen.
* Muutoin normaalia ylläpitoa.

**OUTI**
* Normaalia tukitöitä.
* Koha-tuki muuttanut väistötiloihin. 

**Vaara**
* Normaalit tukityöt, ei erityisempää.
* Päivi päivitti Koha-ohjeisiin kuvailua, kun Z39.50-ohje oli vanhentunut.

**Helle**
* Hyllyvarauslistalla on ollut kaksi varausta noutopaikkanaan Porvoon pääkirjasto. Varauksiin tärppäävät niteet on palautettu Porvoon pääkirjastossa. Koha on ilmoittanut noutokirjastoksi Kevätkummun kirjaston. [Tiketti #310](https://github.com/KohaSuomi/Koha/issues/310)

**Lumme**
* Siiretty Koha-Suomen Dokumentaatioon Varaus otsikon alle Varaukseen liittyvät tiedot Lainauksen alta.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-51-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 50 muistio

Aika: 13.12.2022 klo 9.15
Läsnä: Päivi Knuutinen ja Auli Rantasalo (Vaara), Heli Auranen, Timo Pesonen (Lumme), Pia Kusmin ja Leena Kinnunen (Lappi), Anni Rajala (Vaski), Kati Sillgren (Helle), Reetta Pihlaja (Siilinjärvi), Anneli Österman, Piia Semenoff ja Veli-Pekka Marjoniemi (OUTI)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-50-muistio)

**Yhteiset**

* Kuinka monella pääkäyttäjällä on työajasta pääkäyttäjyyttä yli 30-40%?
  * Vaarassa Päivillä
  * OUTIssa Piialla, Pirkko-Liisalla, Vellulla
  * Vaskissa Anni, Mikko ja Tuula
  * Hellessä Katilla
  * Siilinjärvellä -
  * Kyytissä ei määritetty prosenttiosuutta, voi kulua 0-100 %.


* Onko vuodenvaihteessa tehtäviä töitä, mitä Koha-Suomen pitäisi tehdä?
  * avatkaa tukipyynnöt

* Muistattehan seurailla Testattavia Githubissa.

**Vaara**
* ei mitään erityistä

**Lumme**
* ei erityistä kohassa
* Mikkelissä Lumpeille haussa Informaatikko, Koha- ja verkkokirjaston pääkäyttäjä. Saa jakaa eteenpäin: https://www.kuntarekry.fi/fi/tyopaikat/informaatikko-481020/

**Lappi**
* Normi ylläpitoa
* Leena palannut takaisin töihin

**Vaski**
* Kausijulkaisu-ohjeen numerointi korjattu.
* Asiakaslajin perusteella muodostuva viesti tilin vanhenemisesta ei toimi vielä halutulla tavalla (https://github.com/KohaSuomi/Koha/issues/268), koitetaan vielä kertaalleen jos joku kehittäjistä keksisi mikä viestin määrittelyssä oikein mättää.

**Siilinjärvi**
* Ei erityistä
* Varmistettu, että turhan hyllytarkenteen voi poistaa, jos siinä ei ole kiinni niteitä (poisto onnistui)


**OUTI**
* Paytrail-siirtyminen meni huomaamatta. Kaupunki hoisi ilmeisesti kaiken.
* normaalia ylläpitoa muuten

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-50-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 49 muistio

Aika: Ke 7.12.2022 klo 9.15
Läsnä: Päivi Knuutinen (Vaara), Pia Kusmin (Lappi), Heli Auranen (Lumme), Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Emmi Takkinen,

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-49-muistio)

**Yhteiset**
* Githubin kokemukset - onko esteitä siirtymiselle?
  * Esille ei tullut mitään esteitä siirtyä tikettien osalta käyttämään Githubia Redminen sijaan.
* [Tikettien työnkulku](https://github.com/KohaSuomi/Koha/wiki/Tikettien-ty%C3%B6nkulku)
  * ei tarvitse laittaa kimppatietoa kehitysehdotuksiin, koska kehitys tehdään lähtökohtaisesti kaikille. :)
  * tulossa sama kuvana
* [Versio 22.11](https://koha-community.org/koha-22-11-released/) julkaistu.
* [Discussions-toiminto Githubissa](https://github.com/KohaSuomi/Koha/discussions) - hyödynnettävissä?
  * Päivitysuutiset - Announcements?
  * Kehitysehdotusten ideointia - Ideas? -> Keskustelun voi viedä tiketiksi.
* Viikolla 49 ei päivitystä.
* Viikon 50 huoltoikkunassa ei näillä näkymin ole odotettavissa käyttökatkoja.
* Nalkutin saatu toimimaan Tätissä. Ohitettu kentät 09x,046z,59x,880,9xx,xxx9,8565,579
  * 046z-kenttää liittyy tiketti #5404
  * Laitettu kuvailijoiden seuraavan kokouksen asialistalle, laitetaanko päälle myös paikalliskannoissa.
* dateaccessioned-liitännäinen 952d-kentässä ACQ-kuvailupohjassa
  * toimiiko kaikilla hankinassa tilausta lisättäessä, jos merkitty pakolliseksi?
  * ei ole tullut valituksia, joten oletetaan, että toimii.
* Vuoden 2023 muistioille luonnosteltu paikka Koha-Suomen sivuilla: https://koha-suomi.fi/muistiot
  * muistioita pääsee muokkaamaan samassa repositoriossa kuin Kohan ohje suomeksi -wikiä -> pages -> paakayttajat23.md
* [Missään mennään Kohan ohje suomeksi -wikin päivityksen kanssa](https://koha-suomi.fi/paakayttajat2022#viikko-4-muistio)
  * 3. Varaukset -osiosta puuttuu vielä sisältö?
  * Onko numerointi kunnossa kaikkialla lisättyjen osioden (Maksut ja Varaukset) jäljiltä?

**Vaara**
* normaalia ylläpitoa
* Vaaralle laitettu Nalkutin toimimaan maanantaina

**Lappi**
* Normaalia ylläpitoa

**Lumme**
* Ei mitään erikoista
* Päivitetty Lyngsoen osalta ohjeita, miten oviohjaus, automaatit käyttäytyvät, jos tulee sähkökatko eri automaattitoimittajien laitteilla? 
https://github.com/KohaSuomi/Koha/wiki/Omatoimilaitteet-ja-s%C3%A4hk%C3%B6katkot

**OUTI**
* Normaalia ylläpitoa

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-49-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 48 muistio

Aika: 29.11.2022 klo 9.15
Läsnä: Anni Rajala (Vaski), Pirkko-Liisa Lauhikari, Anneli Österman ja Veli-Pekka Marjoniemi (OUTI), Pia Kusmin (Lappi), Heli Auranen, Timo Pesonen, Katja Valjakka (Lumme), Kati Sillgren (Helle), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Tuomas Kunttu (Kyyti)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-48-muistio)

**Yhteiset**
* "KohaSuomi/Koha #246":https://github.com/KohaSuomi/Koha/issues/246 Myöhässä olevat (tilaukset) -haku antaa virheilmoituksen /Emmi
  * Kuhunkin kimppaan tehdään valebudjetti, budjetittomat johon  tilit liitetään. Tämä korjaa 500 errorin, mutta listaus ei silti aukea niillä kimpoilla joilla vanhentuneita tilauksia on paljon. Tehdään tästä oma tiketti ja tuodaan yhteisöön tehty ehdotus tilauksien rajaamisesta asetuksella meille testattavaksi. 
* "KohaSuomi/Koha #278":https://github.com/KohaSuomi/Koha/issues/278 Niteettömän tietueen varaaminen /Emmi
  * Ongelma korjaantuu seuraavassa versiossa, tiedotetaan ongelmasta kirjastoja. Tiketti laitettu Odottaa -tilaiseksi.


**Vaski**
* Canonin kirjastokorttitulostus otettu ensimmäisessä toimipisteessä käyttöön eilen. Laajenee joulu-tammikuussa muille osastoille ja lähikirjastoihin.
* Varausmuistutuksen käyttöönottoa ollaan aikeissa ehdottaa Vaskin johtoryhmälle, mutta lähetyksen parametroinnissa askarruttaa onko muistutus pakko lähettää joka päivä triggeröitymisen jälkeen. Emmiltä saatiin palaverissa tieto, että tähän ei parametroinnilla pysty vaikuttaa.

**OUTI**
* Oulun Finvoice tuotantolaskutus aloitetaan ke 30.11.2022 pienellä erällä. Samalla testataan automaattisten ajojen ajastukset.

**Lappi**
* Varausongelmia riittää edelleen. Osa saatu selvitettyä ja Finnaan liittyvä varausongelma tiketöity tiedoksi kaikille kimpoille #280.
* Omatoimen blokkilistat selvitetty ja siivous jatkuu.

**Lumme**
* Lumme-ohryssä työstetään ohjeita, miten oviohjaus, automaatit käyttäytyvät, jos tulee sähkökatko eri automaattitoimittajien laitteilla? Mikroväylältä saatu yksityiskohtainen tieto ja Lysyltä odotetaan vastausta. [Laitamme vastaukset kaikkien hyödynnettäväksi](https://github.com/KohaSuomi/Koha/wiki/Omatoimilaitteet-ja-s%C3%A4hk%C3%B6katkot)
* Sähköpostiositteiden muuttaminen noreply[at]koha-suomi.fi aloitetaan Mäntyharjusta joulukuun toisella viikolla.

**Helle**
* Kuvailupohjiin lisätty käyttöön kenttä 942b = Estä valutus. Kentässä valittavina vaihtoehdot: Kyllä JA Ei.

**Vaara**
* Ei mitään erityistä.

**Kyyti**
* Hankintaportaalin käyttöönotto loppusuoralla, Woiman järjestämä koulutus ensi viikolla
* Sen jälkeen kun Kohan viivakoodit muuttuivat sellaisiksi, että jo tilausvaiheessa tulee oikea viivakoodi (aiemmin tuli tilausvaiheessa HANK-alkuinen), eikä luetteloinnissa vastaanoton jälkeen ole viivakoodia enää muutettu, on täällä tuskailtu, ettei uutuushyllyn ylläpito ole enää helppoa kun ei viivakoodista näe aineiston on saapumispäivää. Ratkaisuksi on kokeiltu lisätä infotarraan items.dateaccessioned-kenttä, josta näkee niteen vastaanottopäivämäärän.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-48-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 47 muistio

Aika: 22.11.2022, klo 9.15
Läsnä: Anni Rajala (Vaski), Päivi Knuutinen ja Auli Rantasalo (Vaara), Pia Kusmin (Lappi), Heli Auranen, Katja Valjakka, Timo Pesonen (Lumme), Veli-Pekka Marjoniemi, Pirkko-Liisa Lauhikari ja Piia Semenoff (OUTI), Kati Sillgren (Helle), Reetta Pihlaja (Siilinjärvi), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-47-muistio)

* Epäonnistuneiden kirjautumisyritysten aktiivinen seuranta / Kodo
  * Raportointi palvelimilla/kontainereissa
  * Raportti Kohassa [Asiakkaat, joilla on paljon epäonnistuneita kirjautumisyrityksiä](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Valmiita_SQL-raportteja#Asiakkaat-joilla-on-paljon-ep%C3%A4onnistuneita-kirjautumisyrityksi%C3%A4)
  * Automaattiset asiakashuomautukset/käytönestot?
  * Koha-Suomi tekee kehitysehdotuksen ja automaattinen käytönesto/asiakashuomautus viedään seuraavaan asiantuntijaryhmä-kokoukseen.

* EDItX-sanomien automaattinen uudelleenkäsittely pois käytöstä tai sen harventaminen tapahtuvaksi esimerkiksi vain kerran päivässä, koska tunnittaisesta käsittelystä vaikuttaa olevan enemmän riesaa kuin hyötyä / Kodo
  * Harvennetaan automaattista uudelleenkäsittelyä tapahtumaan kerran päivässä ja ajoitetaan se iltaan (luultavasti kirjaston sulkemisajan jälkeen). Tuolloin kuluneen päivän korjaukset ehtivät mukaan uudelleenlähetykseen ja epäonnistunut uudelleenlähetys ehtii seuraavan päivän virheraporttiin, jos korjaus ei ole auttanut. 

* Githubin uudet näkymät ja tikettien seuranta / Kodo
  * [Luokiteltu status-näkymä](https://github.com/orgs/KohaSuomi/projects/4/views/10)
  * [Testattavat](https://github.com/orgs/KohaSuomi/projects/4/views/8)
  * [Tuotantoon](https://github.com/orgs/KohaSuomi/projects/4/views/11)
  * [Valmiit](https://github.com/orgs/KohaSuomi/projects/4/views/4)
  * Järjestetään tieteellisille pääsy katsomaan tikettejä Githubiin.

* Vanhojen omatoimiblokkien kanssa toimiminen [G-232](https://github.com/KohaSuomi/Koha/issues/232) / Kodo
  * Mikroväylän omatoimiovikoneilta siivottava blokkilistat, jos niitä ei ole vielä poistettu
  * Toveri: tarkistus Hypernovalta 

* Lähettäjä-osoitteen muutos muillekin kimpoille tarvittaessa
  * OUTIssa saatu lisättyä kaikille kirjastoille lähettäjäosoitteeksi noreply(at)koha-suomi.fi ja poistettu palautusosoite.
  * Perille menemättömistä viesteistä valitukset ovat vähentyneet tai eivät ole ainakaan kantautuneet Koha-tukeen saakka OUTIssa.
  * Seuraavaksi voisi muutoksen tehdä Lumpukat, koska yhdestä heidän kunnastaan jo IT-henkilö kysyi, voiko sen tehdä myös heille.
  * Kirjastojen sähköpostitiedot kannattaa muuttaa useammassa erässä, jotta ei yhtäkkiä lähetetä suuria määriä viestejä uudesta osoitteesta.
  * Kannattaa myös tiedottaa asiakkaita uudesta lähetysosoitteesta ajoissa.
  * Pirkko-Liisa ja Piia voi tarvittaessa neuvoa.

* Uusi raportti: [Nimekkeet, joihin on varauksia mutta ainut nide merkitty kadonneeksi](https://koha-suomi.fi/dokumentaatio/raporttikirjasto/#nimekkeet-joihin-on-varauksia-mutta-ainut-nide-merkitty-kadonneeksi)

* Viikon 47 päivitys
  * Perustiedot-näytölle muutoksia
    * Aineistotyyppi ei vielä näy suomenkielisessä Kohassa
  * Niteen hyllytarkenteen kuvaus näkyville Finnaan
    * Näkyvät selkokielisinä kunhan Finnan puolella tehdään muutos

* Githubin tiketti #204
  * testatataan ja otetaan asialistalle ensi viikon palaveriin.

*OUTI*
* Vuoden 2023 kalenterit tehty Oululle
  * Kirjastokohtaiset ylitysten poistot eivät toimineet yhdellä poistokerralla, vaan poistoja saattoi joutua tekemään viis-kuusikin kertaa, ennen kuin poistettava ylitys lähti pois kalenterinäkymästä. Kodo tutki asiaa ja ainakin OUTIssa on tietokannassa päällekkäisiä ylityksiä eli jokainen päällekkäinen ylitys piti poistaa myös tietokannasta ennen kuin ylitys poistui kalenterista.
  * Testikannassa "Aikavälillä" -toiminto ei toiminut oikein vaan se teki laajempia ylityksiä kuin oli tarkoitus. Tuotannossa emme käyttäneet "Aikavälillä"-toimintoa lainkaan vaan tallensimme ylitykset yksittäisinä.
* Oulussa on laitettu ensimmäisen kerran asiakkaalle omatoimikirjaston esto nyt niin, että kehittäjät laittoivat sen päälle ja Koha-tuki laittoi asiakkaan Viestit-osioon tiedon asiasta.
  * Tikettiin:
    * Kohan linkki asiakkaan tietoihin, jolle rajoite asetetaan tai asiakkaan borrowernumber.
    * Käyttörajoituksen aika (lain mukaan enintään 30 päivää).
    * Mihin kirjastoon rajoite asetetaan.
* Vuoden 2021 lehtitilaukset suljettu ja tilauksiin liittyvät odottavat numerot ”pysäytetty”, jotta eivät näy enää reklamoitavissa.

**Vaski**
* Pikalainojen muutos jouduttiin pistämään vielä jäähylle, koska tuotannossa ilmeni ongelma saatavuustietojen lataamisessa Finnassa (tiketti https://github.com/KohaSuomi/Koha/issues/266).
* Viestiasetusten automaattinen poistaminen (tiketti https://github.com/KohaSuomi/Koha/issues/204) sovittiin viime viikolla lisättäväksi kaikille, mutta Vaskilla tuli testauksen yhteydessä esille muutostoiveita ehdotettuun rimpsuun. Sovittiin palaverissa, että muutkin kimpat kommentoivat mahdollisen näkemyksensä seuraavan viikon pääkäyttäjäpalaveriin mennessä.

**Vaara**
* ei varsinaista tiedotettavaa, vain pari kysymystä
* Miten usein Marc-virheraportti päivittyy? Vastaus: kerran vuorokaudessa
* Vaaralle tehty 942b-kentän lisäys kaikkiin kuvailupohjiin. Koskee valutusta. Miten toimii? Vastaus: Valinnat kyllä/ei tarkoitettu valutuksen estämiseen eli Kyllä ei valuta tietoja tietueen päälle. Tarvitaan esim. Celioiden kuvailussa.
* Selvitettävä asia Hypernovalta: G232-tikettiin liittyen Toverien attribuutit, ovatko edelleen tarpeen vai voiko poistaa. 

**Lappi**
* Ongelmia varauksissa, noutopaikkoina mitä sattuu. Myöskään Finnassa ei näy kaikkien asiakkaiden varaukset. Molemmat asiat selvityksen alla.

**Lumme**
* Aloitetaan muutos sähköpostien lähetysosoitteeksi noreply[@]koha-suomi.fi. Ensimmäisenä muutos tehdään Mäntyharjulle. Parin viikon jälkeen muutos seuraavalle kirjastolle.

**Helle**
* Kirjaston Koha-kalenteriin tallennettuja kiinniolopäiviä lainojen eräpäivinä (https://github.com/KohaSuomi/Koha/issues/273)

**Siilinjärvi**
* Ei kummempia paitsi muistin ettei meillä ole käytössä perustiedot-näytön XSLTDetailsDisplay-määritystä, kun asia oli kesken kun viimeksi sitä tutkin. Selvisi että siinä voi olla default, määritykset tulevat nyt automaattisesti.

**Kyyti**
* Hankintaportaalin käyttöönotossa on viimein saatu (toistaiseksi) kaikki sanomat tulemaan onnistuneesti Kohaan.
* Kokoelmatyössä oli tullut tarve saada tehtyä monta nidevarausta massana. Kohassa tällaista toiminnallisuutta ei ilmeisesti ole. Kokouksen jälkeen huomasimme, että tavallisia varauksia kyllä voi tehdä massana Lista-toiminnon avulla, mutta nidevarauksia ei.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-47-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 46 muistio

Aika: 15.11.2022, klo 9.15
Läsnä: Anneli Österman, Veli-Pekka Marjoniemi ja Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen ja Auli Rantasalo (Vaara), Anni Rajala (Vaski), Heli Auranen, Timo Pesonen (Lumme), Pia Kusmin (Lappi), Reetta Pihlaja (Siilinjärvi), Kati Sillgren (Helle)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-46-muistio)

**Yhteiset**
* tiketit ja repositoriot
  * tiketit tehdään kuten ennenkin Koha-repositorioon, mutta siirretään tarvittaessa muihin repoihin, jos ne liittyvät niihin. Esim. jos tiketti liittyy tarratyökaluun, Koha-Suomen kehittäjät siirtää sen kyseiseen repoon.
*  * lisätään repositorioihin tieto suomeksi selkokielisesti, mihin toimintoon se liittyy.
  * Tiketin seuranta -projektissa näkyy kaikki tiketit reposta huolimatta, jos niihin vain on muistettu laittaa projekti-tieto.
  * Kaikki Koha-Suomen tiketit näkyvät, kun klikkaa Githubin yläreunasta "Issues-linkkiä":https://github.com/issues ja muuttaa hakukenttään seuraavan tiedon "is:open is:issue user:kohasuomi archived:false" (ilman hipsuja).
  * tikettien siirrolla pyritään sujuvoittamaan koodikannan ylläpitoa, kun tiettyyn koodiin liittyvät tiketit ovat koodin yhteydessä.
* [Koha #204](https://github.com/KohaSuomi/Koha/issues/204)
  * laitetaan kaikkiin kimppoihin käyttöön.

**OUTI**
* Veli-Pekka Marjoniemi aloittanut 14.11.2022 Koha-pääkäyttäjänä 2 pv/viikko.
* Oulun Finvoice-laskutusta säädetään yhä.

**Vaara**
* Finnaan kirjautumisesta ei ole tullut valituksia
* Kuvailija ihmetteli, miksei kuvailupohja enää automaattisesti muutu aineiston mukaiseksi. Tämä on tekemättä versionvaihdon jälkeen, tiketti
* Eräpäivien siirto eräajona on näppärä, kun kehittäjää ei tarvita sitä tekemään, onnistuu pääkäyttäjiltä ihan hyvin.

**Vaski**
* Lukki-kirjastot kävivät tutustumassa Kohaan. Ei päätöstä järjestelmänvaihdosta, mutta kartoittivat vaihtoehtoja.
* Oletusvaraussääntö pikalaina-nidetyypille otettu käyttöön ja tällä viikolla poistetaan pikalainoilta tarpeettomat DAMAGED-tilat.
* Finnaan kirjautumisesta ehtinyt tulla pari palautetta.

**Lumme**
* Osalla asiakkaista on ollut ongelmia kirjautumisessa verkkokirjastoon.
* FailedLoginAttempts-järjestelmäasetuksen luku nostettu kymmeneen, eli tuplattu, koska Finna-kirjautumiset tekevät kaksinkertaisen kirjauksen borrowers.login_attempts-kenttään.

**Lappi**
* Lapin pääkäyttäjät pitivät maanantaina virkistäytymispäivän.
* Tiedotettu kirjastoja ajankohtaisista asioista.
* Normi ylläpitoa.

**Siilinjärvi**
* Rauhallista.
* [Tehty kehitysehdotus asiakkaan lainatietojen uusinta-sarakkeesta](https://github.com/KohaSuomi/Koha/issues/261).

**Helle**
* Epäonnistuneita Helle-Finnaan kirjautumisia oikeiden tunnustietojen käytöstä huolimatta.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-46-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 45 muistio

Aika: 8.11.2022 klo 9.15
Läsnä: Anneli Österman, Pasi Kallinen, Heli Auranen, Katja Valjakka, Timo Pesonen (Lumme), Pia Kusmin (Lappi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Susanna Sandell (Vaski)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-45-muistio)

**Yhteiset**
* [Viikon 45 päivitys](https://tiketti.koha-suomi.fi/news/44)
  * seurailkaa valutuksen toimivuutta
* [Uusi CSS-säätö Lisää viesti -popparin valikon leveydelle](https://koha-suomi.fi/dokumentaatio/intranetusercss/#s%C3%A4%C3%A4d%C3%A4-lis%C3%A4%C3%A4-viesti--popparin-alasvetovalikon-leveytt%C3%A4)
* [Korjattu versio asiakastietojen piilotuksesta varausruudussa palautuksessa](https://koha-suomi.fi/dokumentaatio/intranetusercss/#piilota-asiakkaan-tiedot-varaus-popupeista). Liittyy tikettiin [244](https://github.com/KohaSuomi/Koha/issues/244)
* Matrixissa eri huoneiden roolit: Pääkäyttäjät - Yleinen vs. Koha-Suomi - Yleinen
  * Päätös: keskitetään puheet pääkäyttäjien huoneeseen ja seurataan, tuleeko mitään sellaista, joka olisi tarpeellista laittaa Koha-Suomi yleiselle. Jos ei tule mitään, niin harkitaan Koha-Suomi yleisestä luopumista.
* superlibrarians-keskustelupalsta Githubissa - onko vielä tarvetta vai suljetaanko se?
  * Päätös: ei käytetä enää, mutta ei hävitetä vielä, jotta tiedot eivät katoa. Seurataan, tuleeko palstalle vielä tarvetta.
* Totalissues - halutaanko mukaan sekä lainat että uusinnat?
  * Päätös: halutaan sekä lainat että uusinnat
* #5633 - asiakkaiden tilin voimassaoloaika 10 vuoteen. Joko tehty kaikille, joille tarvitsee?
  * tehty kaikille, tiketti suljettiin palaverin aikana.
* Hyllytarkenne-kenttä saadaan testi-Finnoihin näkyville to 10.11.

**Lumme**
* Kohassa ei mitään erityistä.

**Lappi**
* Ei mitään erityistä. Normaalia ylläpitoa.

**Vaara**
* Ei mitään mainittavaa.

**OUTI**
* Uuden Paytrailin kauppiasportaalin käyttöönoton vuoksi OUTIn päivystyspuhelin on ehkä vaihdettava peruskapulasta älypuhelimeksi, sillä uusi kauppiasportaali vaatii kaksivaiheisen kirjautumisen. Kaksivaiheiseen kirjautumiseen tarvitaan älyluuria. Tutkimme onnistuisiko kirjautuminen, jos pääkäyttäjillä (3) on vain yksi älyluuri käytettävissä.

**Kyyti**
* Hankintaportaalin ensimmäisten tilaussanomien kanssa ollut suuria ongelmia.

**Vaski**
* Kaksi yritystä ottaa uusi suomi.fi-verkkomaksurajapinta tuotantoon Turun maksupalvelun kanssa. Edelleen kyselyissä puutetta, joten Vaski käyttää toistaiseksi vanhaa rajapintaa.
  * Sähköpostivaatimus uutena: sähköpostikuittaukset ja palautukset. Sähköposti siirretään Finnan sähköposti-kentästä, joka on ongelmallista. Koha-Suomen pääkäyttäjäryhmä kannatti sähköpostitiedon kopioimista Kohasta Finnan sähköpostikenttään. (ongelmana vain ne tapaukset, joissa nyt eri sähköpostit – kumpi on oikea?)
* DNA:lta tekstiviestirajapinnassa tulee nyt tieto onko viesti saatu toimitettua perille. 
  * Raportissa näkyy nämä uudet statukset: undeliverable (Illegal Subscriber), expired, undeliverable (Unknown Subscriber), undeliverable (Invalid destination address). 
  * Asiakkaan tiedoissa on vain tieto toimituksen epäonnistumisesta ja toimitushuomautuksena harhaanjohtava viesti: Virhe sähköpostia lähetettäessä.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-45-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 44 muistio

Aika: 1.11.2022 klo 9.15
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Heli Auranen, Tenho Volanen, Timo Pesonen (Lumme), Pia Kusmin (Lappi), Anneli Österman ja Pirkko-Liisa Lauhikari, Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-44-muistio)

**Yhteiset**

* Oskari-harjoittelijan esittäytyminen

* [Viikon 44 Koha-päivitys](https://tiketti.koha-suomi.fi/news/43)

* [G-tiketti #217](https://github.com/KohaSuomi/Koha/issues/217) Käyttöoikeuden suggestions_manage poistaminen käyttäjiltä /Emmi
  * Tehdään ajot kimppoihin (paitsi OUTIin) tällä viikolla. Jos on jotain huomioon otettavaa, kommentoikaa tikettiin.   

* Testattavat - miten hoidetaan jatkossa?
  * Testattaville laitetaan nyt Tikettien seuranassa tilaksi "Testattava", seurataanko sitä, vai laitetaanko lisäksi vielä johonkin hoksautus/pyyntö?
    * Päätös: Kaikki yrittää seurata Testattava-statusta, mutta pyydetään kehittäjiä hoksautamaan silti jatkossa matrixissa Pääkäyttäjät - Yleinen -kanavalla, kun jokin siirtyy testattavaksi.
    * Keskusteltiin myös, mikä on riittävä määrä testauksia, jotta korjauksen/muutoksen voi viedä tuotantoon. Päätettiin, että 2-3 testausta riittää. Jos muutos voi näkyä eri tavoilla eri kimpoissa (esim. eri signum-liitännäisiä käytössä), niin sitten olisi hyvä, että odotellaan useampi testaus. 

* Github-tiketit - älä poista otsikkoriviltä Bugi, Kehitysehdotus ja Tukipyyntö -sanoja. Tikettien seuranta -projektissa ne helpottaa seuraamista.

**Vaara**
* Kohassa ei mitään erityistä.
* Finnan evästeasetuksia muokattu.
* Paytrailin uuden rajapinnan ongelma tai joku muu, kun asiakkaan maksu Finnan kautta ei näkynyt heti Kohassa viime torstaina. Keskiviikkona otettiin käyttöön uusi rajapinta.

**Lumme**
* Perjantaina 4.11. Mikkelin pääkirjasto suljettu ja Pieksämäen pääkirjasto omatoiminen. Henkilökunnan toiminnansuunnittelupäivä.
* Finnan evästemäärittely tehty. 

**Lappi**
* Rovaniemen kellutus otettu pois päältä 1.11.
* Leena on käynyt tekemässä Finnaan tarvittavat eväisteisiin liittyvät muutokset
* Tehty uusi tarrapohja (rullatarra viivakoodilla)
* Tehty tiketti vanhan omatoimen esto -tiedon poistamiseksi. Github 232 ja Redmine 5414 

**OUTI**
* Finvoice:
  * Oulun pienessä tuotantolaskutuserässä huomattiin vielä puutteita esim. eräpäivätieto ei ollut tullut laskuille, vaikka oli testilaskuilla, laskupohjasta puuttui ns. vapaatekstikenttä, johon voi lisätä kaikkiin laskuihin tulevan vakiotekstin. Eli testilaskujen tekeminen jatkuu...
* Kaikki uudet osakohteet eivät aina valu oikein TäTistä paikalliskantoihin, vaan osa osakohteista tai joskus myös kaikki osakohteet jäävät valumatta. Nämä valumatta jääneet osakohteet näkyvät siirtoraportissa Keskeytyneet-välilehdellä ja useimmiten virheviestinä on "Aborting! Newer export added". [Bugitiketti](https://github.com/KohaSuomi/Koha/issues/229)
* Siirtoraportin Keskeytykset-sivulle on tullut yli 10 sivua tietueita, joissa virheilmoitus Internal Server Error. Virheilmoitukset ovat tulleet 29.10. yöllä n. klo 3.46 - 4.00 välillä. Anneli kysynyt kehittäjiltä, mistä virheilmoitukset olisivat voineet tulla. Syytä ei ole vielä löytynyt. [Tiketti #239](https://github.com/KohaSuomi/Koha/issues/239)
* Oulussa aloitettu 31.10.2022 Oulun pääkirjaston remontin ajaksi yksipuolinen kellutus viiden muun OUTI-kirjaston kanssa. Eli Oulun tietyt nidetyypit kelluvat näissä kirjastoissa, mutta heidän aineistot eivät kellu Oulussa. 
* Oulussa henkilökunnan virkistyspäivä pe 4.11., jolloin Koha-tuki ei päivystä.

**Helle**
* Muutamia Hankintaportaalin kautta ilmestyneitä tuplatilauksia: tuplat poistettu.
* Muutamia Hankintaportaalin virheellisiä tilaussanomia: pyydetty Hankintaportaalin ylläpitäjää lähettämään sanomat uudestaan korjattuina. 


[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-44-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 43 muistio

Aika: 25.10.2022 klo 9.15
Läsnä: Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen ja Auli Rantasalo (Vaara), Pia Kusmin (Lappi), Heli Auranen, Timo Pesonen, Tiina Pietikäinen (Lumme), Kati Sillgren (Helle), Mikko Liimatainen (Vaski), Reetta Pihlaja (Siilinjärvi)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-43-muistio)

**Yhteiset**

* [Viikon 43 päivitys](https://tiketti.koha-suomi.fi/news/42)
  * Käykää muokkaamassa kuvailupohjiin näkyville 942him-kentät
  * [RDA ja poikkeavat pääsanat](https://koha-suomi.fi/dokumentaatio/rdanuotti/)

**OUTI**
* Finvoice:
  * Oulussa tarvitaan laskutuksen täsmäytystä varten laskutettujen niteiden määrät ja euromääräinen yhteissumma. Pyydetty Oulun Digiltä.
  * Laskutusliitännäisessä kun hakee asiakkaan laskutettuja lainoja, päivämäärärajaus ei toimi. [Tiketti #228](https://github.com/KohaSuomi/Koha/issues/228)
  * Raahen Finvoice testilaskut tehty ja ajettu eteenpäin.
* Pyhäjoella Pirttikosken kirjasto on lopettanut toiminnan. Kirjasto poistetaan järjestelmästä, kun vuoden 2022 tilastot otettu.
* Tarkoitus ottaa ensi viikolla käyttöön yksipuolinen kellutus viiden OUTI-kirjaston kanssa Oulun pääkirjaston remontin ajaksi. Eli Oulun tietyt nidetyypit kelluvat kellutuksessa mukana olevissa kirjastoissa, mutta Oulussa näiden kirjastojen aineistot eivät kellu.

**Vaara**
* ei ihmeempiä, mutta tänä aamuna heti 8 jälkeen tuli viesti, että niteiden tallennus ei onnistu. Signumia ei saanut tehtyä o-kentästä kuten normaalisti on tehty kirjoille. Ilmeni, että Vaaraa oli kohdannut typo, koska muilla toimi viikkokorjausten jälkeenkin niteiden tallennus. Asia saatiin kuntoon palaverin aikana.

**Lappi**
* Uutta tarrapohjaa muokataan.
* Uuden Paytrailin käyttöönotto 27.10.2022. Testit ja tilitykset menneet oikein.
* SmartBox päivitetään uuteen versioon ja muutetaan toimimaan automaatin tavoin.

**Helle**
* Tiistai-aamusta 18.10.2022 alkaen tunneloitujen automaattien (2 kpl) toimimisessa ongelmia. Keskiviikko-aamupäivästä 19.10.2022 alkaen molemmat automaatit toimineet ok.
* Elokuussa 2022 käyttöön otetulla automaatilla on ollut väärä kirjastotieto. Automaattiin liittyvät kirjastoyksikkötiedot muutettu oikealle kirjastolle. Emmi vaihtanut tietokantaan automaatilla lainatuille niteille oikean kirjaston. [Tiketti #219](https://github.com/KohaSuomi/Koha/issues/219)

**Vaski**
* Huoltokatkojen venyessä eräpäivämuistutusten lähetys jää tekemättä, jos katko menee yli yhdeksään. Mietitty viestien lähetyksen viivästyttämistä tai kehittäjien tekemää viestien lähetystä ongelmatilanteissa.

**Siilinjärvi**
* Ei kummempia, PIN-koodin palautustoiminto Finnassa saatu käyttöön ensin testiin ja nyt myös tuotantoon. Siili ei tarvitse toimintoa varten erillistä Koha-asiakastunnusta, mutta ei selvinnyt tarvitsevatko muut kirjastot vielä vanhoja tunnuksiansa.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-43-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 42 muistio

Aika: ti 18.10.2022 klo 9.15
Läsnä: Päivi Knuutinen, Auli Rantasalo (Vaara), Anni Rajala (Vaski), Reetta Pihlaja (Siilinjärvi), Pia Kusmin (Lappi), Kati Sillgren (Helle), Heli Auranen, Timo Pesonen, Tenho Volanen (Lumme)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-42-muistio)

* Lisäättekö [Integraatiolistalle viestitysrajapinnat](https://github.com/KohaSuomi/Koha/wiki/Integraatiot)
  * tekstiviestit, paperikirjeet, suomi.fi jne
* [Viikon päivitys](https://tiketti.koha-suomi.fi/news/41)
* [Githubin wikin lisättiin sivu](https://github.com/KohaSuomi/Koha/wiki/Kohan-kanssa-yhteensopivat-laitteet), johon voidaan listata Kohan kanssa yhteensopivaksi testattuja oheislaitteitta, kuten kuittareita ja viivakoodinlukijoita.
* Valmiisiin SQL-raportteihin lisätty [kysely](https://koha-suomi.fi/dokumentaatio/raporttikirjasto/#kirjaston-voimassa-olevien-lainojen-m%C3%A4%C3%A4r%C3%A4-er%C3%A4p%C3%A4iv%C3%A4aikav%C3%A4lill%C3%A4), jolla voi laskea tietyn kirjaston eräpäiväaikavälin lainojen määrän. Raporttilla voi tarkistaa esim. kirjaston yllättävissä kiinnimenotilanteissa, onko tarpeen tehdä eräpäiväsiirtoja ja voiko ne tehdä Eräpäivien siirto eräajona -työkalulla vai pyytääkö ajoa kehittäjiltä. Eräpäivine siirrolla voi tehdä kerrallaan noin 1000 lainan eräpäivän siirtoja ja jos eräpäiviä on tuota enemmän, niin niitä voi käsitellä myös osina esim. asiakastyyppien perusteella. Jos siirrettäviä eräpäiviä on 1000-3000, voi ne hyvin tehdä itse työkalulla, sitä suuremmat määrät kannattaa pyytää ajona.

**Vaara**
* ei mitään erityistä
* Finnan evästeasetuksia pähkäilty ja kysytty neuvoja

**OUTI**
* selvitelty EditX-ongelmasanomia
* Oulussa käynnistetty pienellä laskutuserällä Finvoice-laskutus ja Raahen laskutuksen käynnistäminen on vielä alussa.

**Vaski**
* Yhdellä TäTi-käyttäjällä ei ole onnistuneet tietueiden siirrot Melindaan. Ongelmaan näyttää löytyneen syy Melindan päästä: "Melindan käyttäjätunnusten hallinta ei ollut näemmä vielä kärryillä siitä, että Vaskin kuvailijat ovat siirtyneet TäTi-kuvailijoiksi. Se, että puute käyttäjätunnusten päivityksessä ilmeni vasta nyt, johtuu oletettavasti siitä, että vanhemmilla Vaskin tunnuksilla TäTi lähettää päivitykset Melindaan aina (default-)tunnuksella OUTI1002, jolloin oikeusongelmaan ei törmätä."
* Vaskissa kymmenkunta automaattia, joiden yksikkötieto puuttuu tai on väärä. Aiheuttavat sip-lokissa virheilmoituksia, pyydetään toimittajia korjaamaan.
* Emo-/osakohde-fasettia kaivataan takaisin tiedonhakuun. Ei pystytä toteuttamaan samalla tavalla kuin muut fasetit vaan vaatii template-muutoksen, Anneli kyselee vielä tämän muutoksen perään.
* Viimeisin huoltokatko aiheutti ennakoitua pidemmän palvelukatkon Vaskissa (Turun pääkirjaston tunneloidun palautusautomaatin takia Vaskia ei voitu siirtää väliaikaisesti toiselle nodelle) ja tieto viivästymisestä tuli myöhään.
Varsinkin kun tapahtui kahtena kuukautena perätysten, on aiheuttanut harmitusta ja lisännyt epäluottamuottamusta huoltokatkojen suhteen henkilökunnassa. Tunneloidusta automaatista ei olla pääsemässä eroon vielä parin vuoden sisällä, joten Vaski on kiinnostunut proxy-ohjelmistosta joka keskustelisi sip2ohttps-yhteydellä Kohan kanssa Kohan ja automaatin välissä.

**Siilinjärvi**
* Juuri kun sertifikaatti-asennuksista oli selvitty, meillä luovuttiin lopultakin lainaustiskillä kimppa-tunnuksista ja siirryttiin henk.koht. tunnuksiin. Asennettiin siis paljon lisää sertifikaatteja.
* Mikroväylän automaatit päivitetään 1.11. kyselemään pin-koodia.
* [Otetaan käyttöön pin-koodin palautus Finnassa](https://www.kiwi.fi/pages/viewpage.action?pageId=103197538) Anneli hoksasi ohjeessa tosin vanhan version käyttäjäoikeuden, nyt kai delete_borrowers ja edit_borrowers
* Henkilöasiakkuuden 10 v voimassaoloaika, miten jatkossa pidetään yhteystiedot ajan tasalla? Pitää pohtia.

**Lappi**
* Asiakkaan varaukset eivät näy Finnassa, Kohassa näkyy. Tehty tiketti #212. Jatketaan asian selvittelyä.
* Hankinnan tilit vuodelle 2023 melkein valmiit. 
* Kehittäjiltä tuli viesti, että meidän automaattien salasanat ovat liian lyhyitä. Uusiin/päivitettyihin automaateihin on jo laitettu paremmat salasanat. Vanhojen muuttaminen olisi todella suuritöinen ja tarkkaa ajankohtaa vaativa operaatio. Keskusteltiin pääkäyttäjien kanssa ja salasanoja ei ehkä kannata lähteä vaihtamaan vaan muuttaa ne luonnollisen poistuman/muutoksen kautta.

**Helle**
* Lari muuttanut kirjastokortin omaavien henkilöasiakastyyppien asiakastietojen vanhentumisajan 10 vuoden päähän
* Keskiviikon 12.10.2022 palvelinhuollon käyttökatko odotettua pidempi (indeksiin liittyvä ongelma). Helle-Koha oli katkon jälkeen käytössä n. klo 10.50 alkaen.

**Lumme**
* Yhden asiakkaan kirjautumisessa e-palveluihin ja kohaan edelleen ongelmia. Selvitellään. Kysellään myös täällä ehdotettu kirjautumistietojen tallennuksen ja niiden päivitysten tila.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-42-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 41 muistio

Aika: ti 11.10.2022 klo 9.15
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Heli Auranen, Tiina Pietikäinen, Timo Pesonen (Lumme), Anneli Österman ja Piia Semenoff (OUTI), Kati Sillgren (Helle), Pia Kusmin (Lappi), Mikko Liimatainen (Vaski)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-41-muistio)

**Yhteiset**
* [Viikon päivitys](https://tiketti.koha-suomi.fi/news/39) tehdäänkin ti-iltana.
* Ke-aamuna huoltoikkuna klo 7-9, katkoksia tiedossa. Laiterikon aiheuttanut ongelma saatu korjattua ja nyt päästään tekemään viime kuussa suunnitellut huoltotoimenpiteet.
* Githubin säädöt
* Asiakkaalta tuli Oulussa ehdotus, että Finnassa näkyisi lainan viimeisin uusintapäivä. Tieto kulkee "op-get-checkouts":https://outi.koha-suomi.fi/api/v1/.html#op-get-checkouts -endpointissa, joten se todennäköisesti saadaan Finnallekin kulkemaan. Finnan pitäisi vain tukea sitten sen näyttämistä asiakkaalle.
* #5633 - käykää lisäämässä oman kimppanne listaus ja tieto, onko käytössä hetuttomille 1 vuoden voimassaoloaika.
* Onhan kaikissa kimpoissa päällä pseudonymisointi sekä tuotannossa että testillä?
  Pseudonymization
  PseudonymizationPatronFields
  PseudonymizationTransactionFields 
* 10 v voimassaoloaika -ajo -> muistakaa muokata asiakastyyppien voimassaoloajat myös Kohaan.
* Kaikille kimpoille ajetaan tänään uusiksi koko kuluvan vuoden tilastot vanhassa OKM-tilastointi työkalussa olleen virheen vuoksi.  

**Vaara**
* ei mitään erityistä Kohassa
* Finnan evästeasetukset aiheuttavat toimenpiteitä tämän kuun aikana

**Lumme**
* Hupsuja sähköpostiosoitteita löytyi noin parisen sataa
* Finnan muutoksia tutkaillaan

**OUTI**
* virheellisiä editx-sanomia selvitelty
* koulukirjaston niteillä oli virheellisiä nidetyyppejä, jolloin lainoista syntyi myöhästymismaksuja. Nidetyypit korjattu oikeanlaisiksi koulukirjastossa.

**Helle**
* Virheelliset n. 50 sähköpostiosoitetta korjattu asiakastiedoissa.
* Asiakas ei saanut uusittua Finnassa lainojaan. Lainoilla oli Kohassa näkyvä tieto: Ajastettu automaaattista uusintaa varten. Hellessä ei ole ko. toimintoa käytössä, mutta Lainauksen Lainausasetuksissa oli käytettävissä Automaattinen uusinta -vaihtoehto valintaruutuineen. Vaihtoehto on nyt piilotettu.
* Tietueiden yhdistelysäännöt ovat aiheuttaneet säilytettävien kenttien katoamista, kun ei ole molempiin yhdistelytapoihin (Z39.50 ja Vie/Tuo) tarvittavalla tavalla toimivaa yhdistelysääntöä. 

**Lappi**
* Rovaniemen pääkirjasto palannut takaisin väistötiloista.
* Virheelliset sähköpostiosoitteet korjattu.
* Paljon ollut pientä sälää, mutta pääosin normi ylläpitoa.
* Finnan muutoksia selvitellään.

**Vaski**
* Vaskin kimpan laajuinen musiikin kellutus työn alla. Kellutusta varten perustettavaa kellutusyksikköä mietitään.
* Jokeri-ongelmaan mietitty ratkaisua. Turhista damaged-tiloista haluttaisiin eroon.
* Tarratulostuksen pohjien muokkauksessa havaittu ongelma, jossa kenttien tiedot menevät yhdelle riville. Tarrojen tulostus toimii silti oikein.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-41-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 40 muistio

Aika: ti 4.10.2022 klo 9.15
Läsnä: Heli Auranen, Katja Valjakka, Tiina Pietikäinen (Lumme), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Pia Kusmin (Lappi), Anni Rajala (Vaski), Kati Sillgren (Helle), Reetta Pihlaja (Siilinjärvi)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-40-muistio)

**Yhteiset asiat**
* Lari pyysi minua (Tuomas Kunttu)  kysymään Kansalliskirjastolta muutosta Finnaan, että Kohassa asiakkaan kotikirjasto ja Finnan Ensisijainen noutopaikka olisivat aina synkronissa: muutos toiseen muuttaisi aina myös toisen. Rajapinnan mukaan tämä olisi mahdollista. (Nythän Kohasta Finnaan kotikirjasto siirtyy sen ensimmäisen kerran, ei sen jälkeen ja toiseen suuntaan ei ollenkaan.)
Jäin miettimään, että jos saavat muutoksen tehtyä, niin kumpaan suuntaan muutoksen pitäisi ensin tapahtua Kohasta Finnaan vai Finnasta Kohaan. Useimmissa tapauksissa ja ainakin meillä muutos saisi mennä Finnasta Kohaan. Mutta entä tapaukset joissa Kohassa asiakkaiden kotikirjastoja on muutettu ajoilla (esim. Oulu #5603), onko näissä tapauksissa pyydetty muutosta myös Finnaan ja voiko muutos Finnasta Kohaan aiheuttaa näissä jotain ongelmaa?
  * triggeröikö tietokanta-ajot Kohassa muutoksen myös Finnaan?
  * Finnassa oleva tieto oikeampi, eli käytetään sitä pohjana.

* #5629 - Yhteisössä statistics-tauluun on lisätty sarake categorycode, joka vastaa K-S:n lisäämää usercode-saraketta. Tuodaan muutos myös meille, näin vähennetään työtä seuraavassa versionvaihdossa sekä vältetään datan vääristymistä (asiakkaan categorycode voi/on voinut muuttua). Muutos vaatii seuraavat toimenpiteet:
  * koodin tuonti
  * usercode arvojen kopiointi categorycode-sarakkeeseen
  * jäljelle jääneiden NULL arvoisten categorycode-sarakkeiden täyttäminen
  * sarakkeen usercode tiputus
  * Kohan skeeman päivitys

* Varaustunnus asiakasmääreeksi seuraavassa versionvaihdossa.
* Muistattehan sulkea tiketit, kun ne ovat valmiit tai muuttaa tilaksi jokin muu. [Ratkaisu ehdotettu -tilaisia on tällä hetkellä 30 kpl](https://tiketti.koha-suomi.fi/projects/fbox/issues?utf8=%E2%9C%93&set_filter=1&sort=id%3Adesc&f%5B%5D=status_id&op%5Bstatus_id%5D=%3D&v%5Bstatus_id%5D%5B%5D=3&f%5B%5D=&c%5B%5D=due_date&c%5B%5D=tracker&c%5B%5D=status&c%5B%5D=priority&c%5B%5D=votes_total&c%5B%5D=subject&c%5B%5D=assigned_to&c%5B%5D=updated_on&c%5B%5D=author&c%5B%5D=category&c%5B%5D=cf_14&c%5B%5D=cf_15&group_by=&t%5B%5D=)
* Finna-Koha-kirjanmerkin lisäys/muokkausohje tiketissä #5616 ja laitettu myös Matrixiin.
* #5487
* #5452 - verkkokirjastouusinnat
* Branchtransfers
  * Branchtransfersissa on niteiden kuljetustiloja vuodesta 2014 asti (Vaara), näitä lienee turha säilytellä
  * Puhuttu kehittäjäkanavalla 1-2 vuoden säilytysajasta, vanhemmat pois?
  * Branchtransfersin voisi ehkä ottaa siivousten jälkeen mukaan tietokantojen tuntidumppeihin
  * Päätös: kaksi vuotta
* Tikettien seuranta -projekti
  * oikeuksia lisätty, onnistuuko nyt tikettiin projektin ja statuksen lisääminen?

**Lumme**
* Vanhentunut varaus ei poistunut, antoi vanhan varausajan kuittiin.
* Virkailijan antaa uusia, vaikka sakkoa yli 10 e. 
* Finnassa uusinta antoi 4 vkoa laina-aikaa, vaikka 2 vko laina (varattu aineisto). Millaisia laina ja maksusääntöjä käytetään Finnassa määritellään CircControl ja HomeOrHoldingBranch

**Vaara**
* Varmistuskysymys, voiko PowerBI:hin tarvittavia tilastoja ajaa päivällä (voi)
* Huokailua, miksi esihenkilöt eivät voi pyytää työntekijöille tarvittavia Koha-oikeuksia ajoissa vaan vasta sitten, kun työntekijä on jo talossa
* Irina kyseli itsepalvelulainauksen toimintatavasta, kun asiakas yrittää lainata toiselle varattua teosta
* Varauksen noutoajan ja viimeisen voimassaolopäivän ongelma (jos asiakas valinnut lyhyemmän voimassaoloajan, varaus saattaa tulla vaikka viimeisenä voimassaolopäivänä, jolloin noutoaikaa ei jää)

**Kyyti**
* Versionvaihdosta asti aikakauslehtien vastaanotossa on tullut väärää vuotta joidenkin lehtien kohdalla. Ongelma tarkentunut kerran kuussa ilmestyviin lehtiin. Vika voi olla numerointikaavoissa. Mutta miksi se on muuttunut, kun on aikaisemmin toiminut.
* Varauksen viimeinen voimassaolopäivä on ollut sulkupäivä. Syy voi olla asiakkaan muuttama varauksen viimeinen voimassaolopäivä. Näkikö jostain jälkikäteen mikä on ollut viimeinen voimassaolopäivä varausta tehtäessä. Anneli vinkkasi: https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Valmiita_SQL-raportteja#Varauksen-tiedot-lokilla

**Lappi**
* Paytrail muutokset tulevat Lapin kirjastoille lokakuun aikana.
* Keminmaan kirjastoauton laina- ja maksusäännöt puuttuivat jostain syystä kokonaan. 
* Ensimmäinen GitHub-tiketti tehty.

**Vaski**
* FloatRules-järjestelmäasetuksen toiminnallisuutta päivitetty tuotantoon, minkä ansiosta Vaskissa nyt valmiudet aloittaa Vaski-tasoisen kellutuksen kokeilu. Vaski-johtoryhmä tekee päätöksen aloitusajankohdasta.

**Helle**
* Emmi poistanut käyttäjätunnuksilta tarpeettoman hankintaehdotuksiin liittyvän oikeuden (suggestions_manage). #5621
* Sotuteekin käyttöongelmia yhdellä Sotuteekki-tunnuksella: tunnuksella Sotuteekkiin kirjautuminen Firefox-selaimessa heitti ulos Kohasta. Chrome-selaimella onnistui yhden sotun haku. Tehty uusi tunnus, jonka Kati testasi ja havaitsi toimivaksi. Pyydetty tunnuksen omaavaa tarkistamaan/tarkistuttamaan selaimen asetukset (mm. pluginien sallimisen).
* Tarkka haku -toimintoon lisätty Kirjastoryhmät-hakuehto.

**Siilinjärvi**
* Vanhentuneiden maksujen sql-raportin päivitykseen apuja Annelilta ja Katilta. Reetta pohti ääneen voisiko vanhentuneet maksut lisätä raportointityökaluun, mutta ehkä niitä on järkevämpää hakea sql:llä jatkossakin.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-40-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 39 muistio

Aika: ti 27.9.2022 klo 9.15
Läsnä: Tiina Pietikäinen, Timo Pesonen, Heli Auranen (Lumme), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Kati Sillgren (Helle), Susanna Sandell (Vaski), Pia Kusmin (Lappi), Anneli Österman (OUTI)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-39-muistio)

**Yhteiset asiat**
* Githubin testiaika loka-marraskuu
  * [Tiketit tehdään tänne](https://github.com/KohaSuomi/Koha/issues)
    * jokaista kohtaa tiketissä ei tarvitse täyttää
    * tiketin avaaja laittaa tilaksi Done, kun tiketti on valmis
    * Huomiot ja kehitysehdotukset yms. [tikettiin 188](https://github.com/KohaSuomi/Koha/issues/188)
  * [Tikettejä voi seurata visuaalisesti täällä](https://github.com/orgs/KohaSuomi/projects/4)
* [Vkon 39 päivitys](https://tiketti.koha-suomi.fi/news/37)
* Kohan ohje suomeksi -wikin päivitystilanne?

**Lumme**
* Asiakkaalla ongelma vaihtaa varauksen noutopistettä varausta tehdessä. Onnistui jälkikäteen. Epäselväksi jäi, tekikö asiakas nidevarausta. Tähän liittyen tiketissä 5475 oleva koodi lisätty Lumpeen CSS:n.
* Uuden sertin asentamisessa pientä säätöä eri pisteissä.

**Vaara**
* Viime viikon varmenteiden asentamisessa ongelmia, kun entinen vanhentui eikä uusi toiminut automaattisesti. Onneksi saatiin useita erilaisia ohjeita päivän mittaan ja useimmat ongelmat saatiin ratkaistua ohjeiden avulla. Ilmeisesti kovin monenlaisia koneita/selaimia/selainversioita käytössä, kun niin paljon tuli kyselyitä.
* Kohan itsepalvelu testauksessa, toiveessa saada ihan lähipäivinä käyttöön.

**Kyyti**
* #5614 hankintaportaalin käyttöönotto. Mikä on Woiman tarvitsema osoite? Anneli selvittää. (Kokouksen jälkeen Lari antoi tarvittavat tiedot)
* Mikä on tilanne kesäkuun uusintojen kanssa? Tehty korjaus, joka ei aivan onnnistunut. Korjauksen korjaus tekeillä. (Ja kokouksen jälkeen Emmi ilmoitti, että korjaus on onnistunut)

**Vaski**
* Joistain kirjastoista raportoidaan, että tarratulostus on hieman muuttunut, eli ei enää pyydä valitsemaan tulostusohjelmaa. Syynä on oletettavasti se, että selain on päivitetty uuteen versioon. 

**Lappi**
* Rovaniemen muutto takaisin pääkirjastolle väistötiloista etenee ja työllistää.
* Me naiset kausijulkaisupohja tilauksineen oli onnistuttu poistamaan. Koitetaan saada palautettua testipuolelta tai ehkä joudutaan tekemään kokonaan uudestaan.
* Paytrail uudistus etenee ja ensi maanantaina pidetään aloituskokous. Finna-tukeen toimitetaan uusi kauppiastunnus ja varmenne heti kun ne saadaan. Sitten päästään testaamaan.

**OUTI**
* Noutokirjastottomien varausten syntymekanismi selvisi. Ongelma johtui Finna-Koha-bookmarkletin käytöstä. Ilmeisesti Finnassa on jotain muuttunut ja osoiteriville kertyy biblionumberin jälkeen kauttaviivalla "polku", joka tulee bookmarkletia klikatessa mukaan Kohan puolelle. Jos ei huomaa, että Kohassa varauksen teko näyttää oudolta vaan tekee varauksen loppuun asti, syntyy noutokirjastoton varaus. Pasi korjasi bookmarkletin JavaScript-rimpsun ja uusi laitetaan jakeluun.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-39-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 38 muistio

Aika: 20.9.2022 klo 9.15
Läsnä: Päivi Knuutinen ja Irina Halminen (Vaara), Susanna Sandell (Vaski), Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Pia Kusmin (Lappi), Reetta Pihlaja (Siilinjärvi, alkuosan paikalla), Kati Sillgren (Helle), Heli Auranen, Timo Pesonen, Tiina Pietikäinen (Lumme)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-38-muistio)

**Yhteiset asiat**
* Kansikuvat pienemmäksi / tietyn kokoiseksi. #5420 ja "IntranetUserCSS-sivulla":https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/IntranetUserCSS#S%C3%A4%C3%A4d%C3%A4-kansikuvan-kokoa.
* Lari kaipaa testauskommentteja uudesta "OKM-liitännäisestä":https://github.com/orgs/KohaSuomi/teams/superlibrarians/discussions/3/comments/74, joka on testeillä.
* Kaikki lainojen verkkokirjastouusinnat kirjatuivat versionvaihdon jälkeen parin viikon ajan Finna-käyttäjän kotikirjaston mukaan. Kirjastotiedot korjataan niin, että uusinnoille laitetaan kirjastoksi lainauskirjasto.
* "Tämän viikon päivitys":https://tiketti.koha-suomi.fi/news/36
* Kun luodaan uusi osakohde, osakohteen 773-kenttään ei siirry kaikki tarvittavat tiedot. Kenttiin 773w, t ja a tiedot menevät satunnaisessa järjestyksessä. #5609
* Alkuvuoden OKM-tilastojen laskennassa on löytynyt virhe. Ensin näytti, että mukaan ei ole tulleet lainat, joiden nide on poistettu, mutta loppujen lopuksi ei ole varma, mistä virhe johtui. Emmi tutkii asiaa. Virhe koskee siis vanhasta liitännäisestä konvertoituja tilastoja (tammi-toukokuu).
* "Asiantuntijaryhmän 6/22 muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Asiantuntijat_-_Vuosi_2022#Muistio-622

**Vaara**
* Varaamisen ongelmista on mm. tiketti 3983. Vaarassa on ainakin pari asiakasta, joille ei mene sana perille varaamisen käytännöistä ja haluttaisiin rajoittaa ohjelmallisesti paremmin varaamista. Kohan määritykset lainojen ja varausten määrästä eivät toimi kaikilta osin.
* Itsepalvelulainauksen näkymä on nyt hyvä, kun käännöksiä saatu paikoilleen.

**Vaski**
* Finna: Verkkomaksujen tuplamaksumahdollisuus on todennäköisesti ratkennut. Kansalliskirjasto löysi maksutapahtumasta tilanteen, jossa oli mahdollista esim. selaimen taaksepäin navigoinnilla päätyä tilanteeseen, jossa selain kysyi lomakkeen uudelleenlähettämistä. Tämä korjattu ja tuotannossa.
* Jos virkailijaliittymässä lainaa ja 15-20 minuutin sisällä palauttaa automaattiin, saattaa tapahtua uusi lainaus palautuksen yhteydessä. https://tiketti.koha-suomi.fi/issues/5611

**Lappi**
* Lisää huollettava -nappi aiheuttanut päänvaivaa, mutta nyt vihdoin korjattu ja huoltajan tiedot kopioituvat huollettavalle.
* Rovaniemen muuttoon liittyvät siirrot tiketöidään ja pyydetään kehittäjiä apuun. 

**OUTI**
* Oulun koulukirjastojen itsepalvelutoiminnon Valmis-painikkeen ongelma selvinnyt. Itsepalvelutoiminto on määritetty niin, että sinne mennessä ei tarvita asiakasvarmennetta. Ilmeisesti jotain oli muuttunut kesäkuussa tehdyssä versiopäivityksessä ja pieni, uusi osa itsepalvelun tarvitsemista tiedoista ei ollutkaan varmenteen ”ulkopuolella”. Koha-Suomen palomuurille on tehty muutos, että puuttuva osio sallittiin ilman varmennetta.
* Sähköpostiviestien palautusosoite poistettu kaikikilta kirjastoila, lähettäjäosoitteen (@koha-suomi.fi) muutoksia jatketaan pikkuhiljaa. Viestien otsikoihin lisätty selkeästi tieto, että viesti tulee OUTI-kirjastosta.
* Jälleen onnistuttu tekemään varaus, jossa tietokantaan ei ole tallentunut varauksen noutopaikkaa. Kun yrittää lainata tai palauttaa varatun tietueen niteitä, tulee Virhe 500.
* Oulun Ceepos-ympäristöön tehdään päivitys ti 20.9. klo 20.15 alkaen. Päivitys kestää noin kaksi tuntia, jonka aikana OUTIn verkkomaksupalvelu ei ole käytettävissä. 

**Siilinjärvi**
* paikalla vain alkuosan, varmistui se että Siilinjärvellä palataan jatkossa henkilöasiakkuuden 10v voimassaoloaikaan.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-38-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 37 muistio

Aika: 13.9.2022 klo 9.15
Läsnä: Pia Kusmin (Lappi), Päivi Knuutinen (Vaara), Tiina Pietikäinen, Katja Valjakka, Heli Auranen, Timo Pesonen (Lumme), Reetta Pihlaja (Siilinjärvi), Mikko Liimatainen (Vaski), Anneli Österman ja Piia Semenoff (OUTI), Kati Sillgren (Helle)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-37-muistio)

**Yhteiset asiat**
* Kirkesläisten esittely
* Vaskissa oli jälleen onnistuttu hyppäämään 9000 viivakoodin yli #5545 /Emmi
  * Viivakoodin perään ei saa kirjoittaa numeroita/merkkejä, koska generointi menee höpsis.
  * Pitää painaa kentän vieressä olevaa kolmea pistettä, jos pitää luoda uusi generointi.
* Pääkäyttäjien vuosisuunnitelma. attachment:paakayttajatvuosisuunnitelma2022.docx
* Päivitys ja huoltokatko
* Uusi IntranetUserCSS-rimpsu, jolla saa piilotettua Varaukset odottaneet yli 7 päivää -välilehti #5586


**Lappi**
* Rovaniemen pääkirjaston paluumuutto lähenee ja työllistää.
* Huoltajan tiedot eivät kopioidu lapselle, vaikka PrefillGuaranteeField on käytössä. Tehdään tiketti.
* Siirtokokoelman uutta ohjetta kaipaillaan, että saadaan ohjeistus henkilökunnalle vanhojen siirtolainojen korjaamisesta ja ohjeistus uudesta toimintatavasta.
* Keskeneräisiä töitä paljon. 

**Vaara**
* Asiakkaan pikalisäys-painike piilotettiin, kun se oli lähinnä hämäävä eikä mitään käyttötarkoitusta keksitty
* Karsikon kirjaston muutto on vaiheessa, jossa uuden kirjaston hyllyjä täytetään ja vanhaan kirjastoon jätetty vanha aineisto poistetaan tietokannasta. 
* Uuden sertifikaatin ohjeistus lähetetty henkilökunnalle.

**Siilinjärvi**
* Ei mainittavaa, sertifikaattia asennellaan viimeisillekin käyttäjille.

**Vaski**
* Verkkomaksujen tuplaantuminen edelleen riesana. Maksujen tuplaantumista tapahtunut melkein joka viikko.

**OUTI**
* Pekurin avaus- ja pääkirjaston sulkutoimenpiteitä mm. asiakkaiden kotikirjaston muutos, varausten noutokirjastomuutos, Finnaan tilattu asiakkaiden oletusnoutokirjastomuutos jne..
* Finnatoimistosta pyydetty varausten Peruutus- sanan muuttoa Poisto-sanaksi

**Helle**
* Sertifikaatti jaettu edellisellä viikolla (viikko 36).
* Kohan Asiakkaan pikalisäys -toiminnon painike piilotettu.
* Noudettavat varaukset -toiminnon Varaukset odottaneet noutoa yli 7 päivää -välilehti piilotettu.
* Uudelle asiakkaalle lisätyt lähes kaikki tiedot katoavat tallentaessa, kun asiakastietoon on lisätty jo olemassa oleva varaustunniste (vain osoitetiedot jäävät). Tiketti tästä https://tiketti.koha-suomi.fi/issues/5605
* Helle-Finnassa ruotsinkielisen teoksen esittelyteksti oli englanninkielinen kaikilla käyttöliittymäkielillä. Ko. teoksen esittelyteksti haetaan Kansalliskirjaston palvelimelta. Korjausliikkeenä Finna-toimisto lisäsi esittelytekstin linkkikenttään 856q kentästä puuttuneen arvon (text TAI text/html). Korjauksen jälkeen esittelyteksti on ruotsinkielinen. [Teostiedot Helle-Finnassa](https://helle.finna.fi/Record/helle.710689)

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-37-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 36 muistio

Aika: 6.9.2022 klo 9.15
Läsnä: Leena Kinnunen, Pia Kusmin (Lappi), Heli Auranen, Timp Pesonen, Katja Valjakka (Lumme), Reetta Pihlaja (Siilinjärvi), Anni Rajala (Vaski), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Anneli Österman (OUTI)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-36-muistio)

**Yhteiset asiat**
* Kirkesläisten esittely
* Renewallogit päälle Siili ja Lumme
  * [yhdessä sovittu, että nämä lokitukset laitetaan päälle](https://koha-suomi.fi/paakayttajat2022#viikko-7-muistio)
* Redmineä hieman siivoiltu, vanhoja tikettejä ja projekteja suljettu, "Manage" -projekti nimetty uudelleen "Muistiot ja keskustelu" sekä tiketöinti sieltä poistettu käytöstä. Kysykää jos tulee murheita tai ette pääse käsiksi johonkin, T. Kodo
* signum-plugarit tuottavat tällä hetkellä välilyönnilliset pääsanat, niin että välilyönti tulee mukaan. Esim. 7 autoa -> "7 A". Tarratulostimen signumheader-toiminto ei osaa tulkita välilyönti oikein, joten pääsana muodostuu väärin. Kehittäjät ehdottivat korjaukseksi pääsana-pluginin päivittämistä joko niin että välilyönti poistetaan kokonaan (7AU) tai se korvataan alalyönnillä (7_A).
  * Päätös: äänestettiin jitsin Poll-toiminnolla näiden kahden vaihtoehdon välillä ja 83 % äänesti niin, että signumeihin välilyönnilliset luodaan niin, että välilyönti korvataan alaviivalla.


**Lappi**
* Asiakastietoihin on jäänyt hämäävästi tieto “Ei huoltajan lupaa omatoimikäyttöön”. Nykyisin asia toteutetaan asiakastyypillä, poitettava, lisää tiketissä #5414 
* Webkake-liittymä valmiina, käyttöönotto tällä vikolla. Käyttäjinä Rovaniemi ja muutama muu kirjasto. 
* Asiakkaan muutospyyntöä ei voinut hyväksyä, ongelmana näytti olevan jo olemassaoleva varaustunnus - toinen kirjoitettu pienillä kirjaimilla, toinen kapiteeleilla. Onko merkkikoolla väliä varaustunnuksessa?
* Onko muilla käytössä yhtenevät kuitit ja ilmoitukset, vai oletteko tehneet kirjastokohtaisesti omia pohjia?
* Kemissä Ceepos-kassa edelleen vähän kesken, testaillaan
* Hankintaportaali/Woima ilmoitti tuoneensa uudelleen postponed-tilaiset varaukset, tuotu joko toisilla nimillä tai ei tuotu, selvitetään. 
* Huoltajan tieto ei kopioidu huollettavalle kun käytetään Lisää lapsi-toimintoa. Ratkaisu: PrefillGuaranteeField -asetus. 
* Leena jää opintovapaalle 9.9., palaa 12.12. Ei sijaista, pääkäyttäjinä jatkavat Pia, Noora ja Maria.

**Lumme**
* Pieksämäen ja Savonlinnan kirjastoautoille tehtiin oma laina- ja maksusääntö pidemmän varausajan vuoksi. 
* Yhteisesti sovitut lokitukset on loputkin laitettu päälle (AcquisitionLog, AuthFailureLog, AuthSuccessLog (tämä ei ehkä pakollinen), BorrowersLog, CataloguingLog, FinesLog, HoldsLog, IssueLog, RenewalLog, ReturnLog
* Selvitelty, että jatkossa tietosuojalakiin perustuvat asiakkaiden tietopyynnöt pyydetään kehittäjiltä. Kirjaston/kunnan edustaja sitten lähettää tiedot turvapostilla asiakkaalle. Tietopyynnöt pääkäyttäjien kautta.
* Toenperän kimppa purkautuu vuodenvaihteessa, eli Joroinen ja Rantasalmi toimivat jatkossa omina kirjastoinaan.

**Siilinjärvi**
* Meillä ei toistaiseksi ole täti/melinda-luetteloijaa.
* Lokiasetukset korjattu viikon 7 muistion mukaisesti
* Ei muuta erikoista.

**Vaski**
* Damaged-tila yliajaa Finnassa esim. kuljetettavana-tilan ja notforloan-tilat. Erityisesti pikalainojen kanssa tämä nyt ongelma. Sovittiin, että Vaski tekee tästä tiketin Kehitysehdotukset-projektiin, josta Koha-Suomi voi sitten edistää asiaa yhdessä Kansalliskirjaston kanssa.

**Vaara**
* Koha keskustelee nyt Ceepos-kassan kanssa Joensuun pääkirjastossa.
* kysely toimipistekoodien muutostarpeesta: Vaaran lisäksi ainakin Outissa tarvetta, samoin tulee Lumpeessa. Muutoksen toteutusta mietitään eri näkökulmista, jotta saataisiin mahdollisimman kestävä ratkaisu isoon muutokseen. Kehittäjien resurssipula ongelmana.

**Helle**
* Tietueyhdistely esim. Helle-tietueen korvaaminen TäTi-tietueella hävittää Helle-tietueen 856-kentät. Pääkäyttäjäpalaverissa mainittu, että Vie/Tuo-toimintoa käyttäen 856-kentät säilyvät. Z39.50-toiminto kadottaa 856-kentät. 
* Uusi kehitysehdotustiketti varaustunnisteeseen liittyen https://tiketti.koha-suomi.fi/issues/5595 (vanhassa tiketissä muutakin)

**OUTI**
* Virkailija oli onnistunut taas tekemään varauksen, jolla ei ole noutokirjastoa. Tästä aiheutui se, että asiakkaan varaukset eivät näkyneet ollenkaan Varaukset-välilehdellä asiakkaan tiedoissa. Anneli koitti toistaa virhettä mm. kirjautumalla toisella välilehdellä ulos kesken kaiken, odottamalla aikakatkaisua, vaihtamalla toisella välilehdellä kirjautumiskirjastoa, mutta mikään näistä ei aiheuttanut vastaavaa virhetilannetta.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-36-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 35 muistio

Aika: 30.8.2022 klo 9.15
Läsnä: Anneli Österman, Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Leena Kinnunen ja Pia Kusmin (Lappi), Päivi Knuutinen ja Auli Rantasalo (Vaara), Heli Auranen, Katja Valjakka, Tiina Pietikäinen, Timo Pesonen (Lumme), Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Reetta Pihlaja (Siilinjärvi), Susanna Sandell (Vaski)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-35-muistio)

**Yhteiset asiat**

* Testien kantojen anonymisointi
  * tietoturvasyistä anonymisoidaan testikannat niin, että asiakkaille generoidaan uudet tiedot.
  * kirjastokortin numero ja biblionumber säilyy samana kuin tuotannossa.
  * Anneli tekee tiketin aiheesta.
* Paperikirjeiden uudelleenlähetyksen tarve, koskee pdf-muotoisia e-kirjeitä eli lähinnä Lumme/Kyyti
  * Jos käyttäjä klikkaa lähetä uudelleen -nappia, niin viestiä ei lähetetä uudelleen ja kirjataan toimitushuomautukseen, että viestiä ei lähetetty uudelleen.
* Sähköpostien lähetys
  * kun lähetys- ja palautusosoitteiden domain on eri, niin sähköpostipalvelut (esim. gmail) tulkitsee sen roskapostiksi, eikä viestit mene perille.
  * ehdotettu, että lähetetään osoitteesta noreply@koha-suomi.fi ja luovutaan palautuvien viestien tarkistamisesta eli bounce-osoite olisi tuo sama ja viestit menee "bittiavaruuteen", koska sitä ei oikeasti ole olemassa.
  * suurimmalle osalle tämä kävisi, mutta OUTI ja Vaski haluaa vielä varmistaa muutoksen kimpan sisällä.
* Automaattien tippuminen saatu enimmäkseen korjantumaan, kun sip-lokien rotaatio korjattiin ja tiedosto ei ole enää niin iso ja tiedoston tallennuksessa ei tule enää niin isoa viivettä.
* Ceepos muuallekin kuin OUTIin käyttöön
  * Vaara ja Lappi ottaa yhteyttä Johannaan.
  * [Ceepoksen käyttöönotto-ohje](https://github.com/KohaSuomi/koha-plugin-ceepos-integration)
* Pidetään testijakso, jolloin kokeillaan riittääkö Githubin toiminnallisuudet korvaamaan Redminen toiminnot. Päätetään asiantuntijaryhmässä ajankohta ja kesto.
* Testeillä on raporttiliitännäinen, jossa on OKM-tilastot paikallaan. Lari pyysi testaamaan ja tekee liitännäiseen liittyviä tikettejä Kehitysehdotukset-projektiin.
* Hankinnan henkilöiden yhteydenpitofoorumi -kohta viime viikolta: Lisättiin Koha Teamsiin oma kanava hankintaa tekeville.

**Lappi**

* Kohan varmenne jaettu alueen johtajille ja tiedotettu kirjastojen henkilökuntaa varmenteen päivittämisestä. 
* Yhteisöasiakkaille ei generoitunut salasanaa,  puuttui salasanan pituustieto asiakaslajin hallinnasta. 
* Ensi vuoden budjetteja ja tilejä on alettu lisätä Kohaan. 
* Varatuimmat-listan siirto tehdään jatkossa JSON:lla, kiitos ohjeista!
* Hankintaportaali/Woima ei edelleenkään vastaa, tilauksia postponed-tilassa
* Rovaniemen remontti-exit-työlista työn alla. 

**Lumme**
* Paperikirjeiden osalta ollut ongelmana viestien uudelleen lähetys, aiheuttaa virhetilanteen. Mietitään siirtymistä epl-lähetykseen pdf-viestien sijaan.
* Kohan varmenne jaettu alueen johtajille ja pääkäyttäjille.
* EDItX tilaussanomien käsittelyssä oli ongelmia (Sanomien muodostamisessa aineistontoimittajan järjestelmässä tai niiden siirrossa Koha-palvelimelle on tapahtunut virhe, tai siirto palvelimelle on edelleen kesken.) – viestejä alkanut tulla.

**Vaski**
* havaittu, että syntyy asiakastietueita, joihin ei ole hetua liitettynä. Teorian mukaan ne syntyvät siten, että hetun lisäämisen yhteydessä ei muisteta painaa Tallenna-painiketta. Ehdotus, että tallennus ja syntymäajan generointi yhdistettäisiin samaan "käskyyn", jolloin tallennuksen unohtuminen olisi näkyvämpää. Myös sotuavaimen siirto lähemmäksi hetun syöttökenttää selkeyttäisi.
* toivotaan, että muutkin ehtisivät testata uusia kellutussääntöjä https://tiketti.koha-suomi.fi/issues/5380

**OUTI**
* Ceepos tuotantokäytössä, Vaalan käyttöönotto seuraavaksi.
* Viddlan ikärajatarkistus on saatu toimimaan.
* Kirjastojen lähettäjäsähköpostiosoitteen noreply@koha-suomi.f muutoksia tehty pikkuhiljaa, mutta ongelmaksi osoittautunut palautusosoite, joka on eri.
* EditX-tilauksissa tullut outoja virheellisiä tilaussanomia Raahelle ja Oululle. Sanomat koskevat tilejä esim.  RAPKAIK2000, OUPKMUS2000

**Siilinjärvi**
* Meillä ollaan valmiita luopumaan palautuvien sähköpostiviestien tarkistelusta ilomielin.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-35-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 34 muistio

Aika: 23.8.2022 klo 9.15
Läsnä: Leena Kinnunen (Lappi), Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen ja Irina Halminen (Vaara), Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Susanna Sandell (Vaski)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-34-muistio)

**Yhteiset asiat:**
* Hankinnan henkilöiden yhteydenpitofoorumi?
* OUTIsta ehdotettiin, voisiko Kohan ohje suomeksi -ohjeeseen laittaa pääotsikot myös Varauksille ja Maksuille. 


**Lappi**
* Kaksi tilausta POSTPONED-tilassa, pyydetty korjausta Hankintaportaalin ylläpitäjältä
* Paytrailin rajapinta- ja kauppiastilin uudistus menossa Rovaniemellä, ollaan kuulolla
* Kohan käyttäjätunnusten tekovastuu ollut yhdellä informaatikolla, siirtyy pääkäyttäjille, päivitetään toimintatapoja
* Muutoin sangen rauhallista

**OUTI**
* Piia päivittää uuden varmenteen asennusohjeen.
* Tullut yksi tilaussanoma, joka oli POSTPONED-tilassa eli sanoma oli tyhjä. Hankintaportaali lähettänyt sanoman uudestaan. EDItX-sanoman virheestä tulleessa s-postiviestissä ei ollut kerrottu, missä tilaussanomassa on ongelma. Kodo on luvannut korjata, että jatkossa kaikissa s-postiviesteissä ilmoitetaan, missä sanomassa ongelma on.
* Koha-Ceepos-maksuliittymä on saatu käyttöön Oulun pääkirjaston yhdellä kassalla pe 19.8.2022. Toiminut ongelmitta. Käyttöä laajennetaan, kun muiden kirjastojen tuotteet saadaan tallennettua Ceepos-liitännäiseen. Tällä hetkellä ohjelma ilmoittaa "Request-URI Too Long" eli liikaa dataa. :) Johanna korjaa.
* Oulun Finvoice-laskutukseen liittyvä palaveri pidetty 22.8., jossa oli mukana kaikkien osapuolten asiantuntijat. Kirjasto on ensimmäinen Oulussa, joka ottaa Finvoice-muotoisen laskutuksen käyttöön. Ensimmäiset testiaineistot lähetetty ja ne olivat näyttäneet hyviltä, kun ne oli siirretty Monetran Intimeen. Muutamia muutoksia tuli vielä Johannalle tehtäväksi, jonka jälkeen testauksia jatketaan.
* Oli onnistuttu tekemään varuaus, jolla Kohassa näkyi noutopaikka, mutta tietokannassa noutopaikkaa ei ollut. Kun yritti palauttaa tietueen niteitä, johon varaus oli, ohjelma antoi Virhe 500. Myös asiakkaan varauksia Koha ei näyttänyt. Kun kehittäjä lisäsi tietokantaan noutopaikan, ongelma poistui. 
* Oulun hankinnasta tuli palautetta, että kun tilauksen poistaa ja jos tilauksen tietueessa on varaus, ohjelma ei poista nidettä automaattisesti kuin se teki vanhassa versiossa. Ohjelma ilmoittaa, ettei nidettä ole poistettu. Virkailijan pitää käydä erikseen poistamassa nide. Tultiin siihen päätelmään, ettei muutosta pyydetä, koska näin virkailija huomioi varauksen paremmin ja toimii kirjastossa sovittujen käytänteiden mukaan.

**Vaara**
* Finnassa tehty muutospyyntö asiakkaan tietoihin näkyy lokissa kuin se olisi tehty virkailijatyökalussa. Ennen versionvaihtoa se näkyi eri tavalla. Ongelma Finnan päässä?

**Kyyti**
* Ei mainittavaa

**Vaski**
* valmistellaan Vaski-tasoista musiikin CD:iden kellutusta. 
* odotellaan edistymistä näissä, koska uuden aineiston käsittely on merkittävästi hidastunut (näkyy asiakkaille asti):
  * [Redmine #4582](https://tiketti.koha-suomi.fi/issues/4582)
  * [Redmine #4590](https://tiketti.koha-suomi.fi/issues/4590)
  * [Redmine #4604](https://tiketti.koha-suomi.fi/issues/4604)
* uuden niteen lisäämisessä törmätään erityisesti iltapäivisin usein siihen, että Kohan tarjoama nidetunnus on jo käytössä (vaikka nidetunnus haettaisiin viimeisenä toimenpiteenä, juuri ennen tallennusta). Tällöin tallennus epäonnistuu, tietueeseen lisätyt tiedot häviävät ja pitää aloittaa alusta.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-34-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 33 muistio

Aika: 16.8.2022 klo 9.15
Läsnä: Päivi Knuutinen (Vaara), Katja Valjakka, Tiina Pietikäinen, Heli Auranen (Lumme), Mikko Liimatainen (Vaski), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Leena Kinnunen, Pia Kusmin (Lappi) 


[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-33-muistio)

**Yhteiset asiat:**
* Varauksen noutoaikamuistutus, halutaanko muissa kimpoissa päälle? (Lumme toimii) [Redmine #5499](https://tiketti.koha-suomi.fi/issues/5499) Ilmoitukset tikettiin, jos kimpasa halutaan se päälle.
* Luetteloinnin kentissä Lukko-ongelma [Redmine #5554](https://tiketti.koha-suomi.fi/issues/5554) Heikkisen Antti mietti, että jos poistetaan linkitetyt sanastot paikalliskannoissa, niin jääkö silloin muodostumatta myös Kohan omat auktoriteettitietueet kokonaan ja, että tarvitaanko niitä edes? Hänen mukaansa paikalliskannassa joutuu muokkaamaan niin monia erilaisia tietueita vanhoista uusiin hankinta- ja minitietueisiin ja hän ehdottikin, että väliaikaisesti laitetaan paikalliskannoissa takaisin päälle tuo 9-osakenttiin vaikuttava järjestelmäasetus, jotta tietueita pääsee taas käsittelemään, jollei siitä ole mitään muita haittoja paikalliskannoissa kuin tuo siirtoraporttien turha 100a-ilmoitus. 31.8. on seuraava Koha-Suomen kuvailuryhmän kokous, jossa asiasta voisi keskustella.
  * voidaan ajona ottaa linkitykset eikä poiston pitäisi aiheuttaa mitään ongelmia
* Kohan varmenne vanhenee 21.9.2022.
  * ilmoitetaan Koha-Suomi- Yleinen Matrix-keskustelussa kenelle Johanna toimittaa uuden varmenne-tiedon. Uudet varmenteet tehdään 17.8. (salasana pysyy samana) ja toimitetaan tieto kimpoille. Uusi ja vanha varmenne toimivat 21.9. asti rinnakkain eli on kuukausi aikaa ottaa uusi varmenne käyttöön. OUTIn tekemään varmenne-ohjeeseen päivitetään miten toimitaan varmenteen vaihtuessa. Ohje jaetaan muiden kimppojen käyttöön pävityksen jälkeen.

**Lappi**
* Smartboxiin tulossa lisätoimintoja
* Asiakkaalla tulostuu lainakuittiin maksuja, mutta Kohassa maksut näyttävät nollaa
* Nidetyyppi Ei lainattava näkyy Finnassa saatavana, jos sille ei ole merkitty notforloan-tilaa eisaatavana-eivarattavissa. Lainamaksutaulukossa ko. nidetyypin lainaus ja varaus estetty. Tilastoituvatko kaikki lainaukset raporteille huolimatta siitä, mikä notforloan- tai muu auktorisoitu arvo niille on annettu?
* Niteet-välilehdellä näkyy tieto Sija jonossa : Jätä pois paikallisten varausten jonosta. Onko tätä mahdollista piilottaa, ei kannattene valita vaihtoehtoa Kyllä?
* Siirtokokoelmien niteiden kotikirjastot vaihtuneet #5567
* Niteelle tullut 235 väärää osakohdetta #5544


**OUTI**
* Koha-Ceepos-maksuliittymä ei ole vielä OUTIssa käytössä. Vielä ääkkösongelma ratkaistavana, muuten liittymä toimii.
* Asiakkaan käyttäjäoikeuden jatkaminen ei onnistunut, kun asiakkaan varaustunnisteen edessä oli välilyönti ja toisella asiakkaalla oli samanlainen tunniste (ilman välilyöntiä). Tilin uusinta antoi virhe 500. Tunnisteen vaihto auttoi ja tilin uusinta onnistui. Jostain syystä Koha on antanut tallentaa edellisessä versiossa lähes samanlaiset tunnisteet.
* Joidenkin asiakkaiden PIN-koodit eivät ole toimineet lauantaina eikä eilen maanantaina . Uudelleen tallennus on auttanut.
* Koulukirjastoissa on ilmennyt itsepalvelulainauksen käytössä hitautta. Lainaus ja palautus toimivat normaalisti, mutta "Valmis"-näppäimen jälkeen pitää odottaa miltei minuutti, ennen kuin seuraava asiakas voi kirjautua sisään.

**Vaara**
* Finna-listojen teko. Ennen versionvaihtoa oli oma raporttinsa, jonka sai vietyä Finna-muodossa Finnaan ja sillä sai suoraan korvattua edellisen vastaavan listauksen. Nyt tällaista ei ole, on vain mahdollisuus tehdä lista raportista. Mutta miten lista viedään eteenpäin, kun ei ole mitään painikkeita? Tein tiketin [Redmine #5573](https://tiketti.koha-suomi.fi/issues/5573)
* Ulkomaisen puhelinnumeron tallentaminen/viestin lähettäminen siihen. Johannan mukaan ulkomaisiin numeroihin lähetettävät viestit tarvitsevat operaattorin kanssa sopimisen. Vaarassa ei voi tällä hetkellä käytössä olevan IntranetUserJS-asetuksen mukaan tallentaa ulkomaista puhelinnumeroa puhelinkenttään, koska siinä on estetty ulkomaisten numeroiden tallentaminen. Ulkomaisen numeron voi tällä hetkellä tallentaa asiakkaan huomautuskenttään.
* Kuvailutietojen valutuksessa on viivettä Vaarassa. Osa ongelmista johtuu siitä, että Vaarassa on nimekkeen aikaleima vanhempi kuin Tätissä olevan tietueen aikaleima eikä valutusta tapahdu, kun nimeke ei ole Vaarassa aktivoituna. Valutusongelma on osittain johtunut myös Johannan jo korjaamasta ongelmasta, jonka mukaan ison osakohdemäärän valuminen on saattanut estää muiden nimekkeiden tietojen valumisen. 

**Lumme**
* Lumpeissa, kuten Vaarassa, hitautta teostietojen valutuksessa.
* Maksuissa ongelmia. Maksuja ilmestynyt takaisin, vaikka virkailija poistanut maksut. Asiaa tutkitaan. Myös kuiteilla näkyy toisinaan väärin.
* Mäntyharjulla ihmetelty poistotilastojen suuruutta. Heinäkuussa pääkäyttäjissä puhuttu tästä.
* Budjettiraporttien toimivuus selvittelyn alla.

**Vaski**
* Budjeteissa eivät käytetty sarakkeen summat näytä aina pitävän paikkaansa.
* Valmistaudutaan koko Vaskin laajuiseen musiikki CD:iden kellutukseen. Kellutussäännöt eivät vielä toimi oikein.

**Kyyti**
* Kun Tätistä hakee ennakkotietojen päälle täydelliset tiedot Tietueen Muokkaa-valikon Korvaa tietue Z39.50/SRU-kyselyn kautta -toiminnolla, häviää tietueesta kansikuva sekä esittelylinkit. Tähän neuvottiin, että kannattaa käyttää tietuenäytön Vie/Tuo-toimintoa. Myös itse ongelmaa on ratkaistu tiketti #5500. Testeillä on korjaus olemassa.
* Kysyin viime palaverissa omatoimikirjastokäytännöistä. Kiitos vastauksista Outi, Vaski ja Vaara.
* Kirjastoautossa on tuskailtu klikkausten määrää, joita tulee kun muiden pisteiden aineistoa palautuu paljon kirjastoautoon.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-33-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 32 muistio

Aika: 9.8.2022 klo 9.15
Läsnä: Heli Auranen, Katja Valjakka (Lumme), Pirkko-Liisa Lauhikari (OUTI), Antti Kiviniemi ja Lari Strand (kehittäjät), Tuomas Kunttu (Kyyti), Päivi Knuutinen (Vaara), Mikko Liimatainen (Vaski)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-32-muistio)

**Yhteiset asiat:**
* Finnassa näkyvän palautuskehotuksen otsikon ja selitteen muutokset, tiketti: [Redmine #5561](https://tiketti.koha-suomi.fi/issues/5561).
  * Muutos tehtävä Finnan päässä.
  * Kehittäjien ehdotus: Pyydetään kääntämään "Overdue" suomeksi: "Palautuskehotus". Tällöin kuvaus olisi: "Palautuskehotus - 1. huomautus". Otsikkotieto "ei tietoa" korvataan viivalla.
  * Ehdotus hyväksyttiin. Pirkko-Liisa laittaa pyynnön Finna-tukeen.
* Huoltoikkuna ke 10.8. klo 7-9. Tiedossa ei ole käyttökatkosta.

**Lumme**
* Osa uusista täti-kokelaistamme valitellut lukittuja kenttiä, eli samaa kuin Outissa viime viikolla
”Luetteloijat ilmoittivat, että esim. luettelointikentissä 1xx ja 65x ja 7xx lukot päällä eli kenttiä ei pääse muokkaamaan. Tiketti: https://tiketti.koha-suomi.fi/issues/5554”
* Varausmuistutukset vielä vaiheessa, ei ollut ihan yksinkertainen ominaisuus.
* Tilanahtaus tila poistui aiemmin lainattaessa, nyt ei enää poistu. Tutkitaan auktorisoituja-arvoja.

**OUTI**
* Oulun kirjakaapille oli muuttunut jossain vaiheessa vanha laina-aika 7 vrk, joka on ollut 1.12.2021 lähtien 14 vrk. Olisikohan voinut päivittyä testiltä versiopäivityksen yhteydessä? Kirjakaappi on ollut kiinni 17.6.-31.7.2022, joten isoa vahinkoa ei ollut ehtinyt tapahtua. 
* OUTIn laskutusliitännäisessä, kun lasku luodaan, tallentuu rajoite automaattisesti sekä lapselle että takaajalle. Kun kaikki laskutetut lainat on palautettu, poistuu rajoite tällä hetkellä automaattisesti vain lapselta, mutta ei takaajalta. [Redmine #5566](https://tiketti.koha-suomi.fi/issues/5566)
* Outo tapaus, jossa varaus oli noudettavana asiakkaalle noutokirjastossa, vaikka nidettä ei oltu vielä palautettu noutokirjastossa, ainakaan lokien mukaan. [Redmine #5568](https://tiketti.koha-suomi.fi/issues/5568). Ilmeisesti Vaarassa ollut samalla viikolla vastaavanlainen tapaus.
* Oulun luetteloijalta tullut toivomus, että saisiko Tätiin Celia-aineiston kuvailupohjan kentän 100 e-osakentän toistettavaksi. Päivi muuttaa kentän toistettavaksi.
* Johannan kanssa jatkettu Oulun Finvoice-muotoisten laskujen testiaineiston vientiä Monetran Intimeen.

**Kyyti**
* Hankintaportaali on tulossa käyttöön Kyytissä. Elokuun aikana pitäisi alkaa tapahtua.
* Hyllyvarauslistalta puuttuu varauksia #5565. Varaukset on pahimmillaan tehty kuukausi sitten. Nyt ohjeistettu käyttämään myös varausjono-toimintoa. Palaverissa kuultiin, että huomenna voisi asiaan tulla korjaus.
* Juuri tänään tuli asiakaspalaute että miksi finnan lainaushistoriassa näkyy ei nimekettä tuntematon. Tiketistä #5537 sai selityksen.

**Vaara**
* Budjettien summiin toivottiin saatavan pian korjausta, että verot eivät näkyisi hinnoissa. Tämä on työn alla ja ilmeisesti saadaan korjaus huomisessa ajossa.
* Vaarassa on myös valitettu kuvailupohjien kenttien lukoista. Kaikilla kuvailijoilla ei ole Täti-oikeuksia (Celia-kuvailijoita) ja ongelmana on myös vanhojen ilman isbn:ää olevien tietueiden korjaaminen silloin kun se on tarpeen, koska Melindassa voi olla useita eri tavoin kuvailtuja tietueita samasta nimekkeestä. Toivotaan pikaista ratkaisua, miten päästäisiin yhtenäiseen käytäntöön kuvailuissa.
* Päivi muistutellut mieleen kevättalven PowerBI-koulutuksen oppeja yrittämällä saada aikaan vertailutaulukoita mm. kirjastojen kävijämääristä.

**Vaski**
* Omatoimikirjastoissa laitteistomuutoksia. Yksi tehty ja yksi tulossa.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-32-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 31 muistio

Aika: 2.8.2022 klo 9.15
Läsnä: Katja Valjakka, Heli Auranen (Lumme), Päivi Knuutinen (Vaara), Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Maria Joona (Lappi), Tuomas Kunttu (Kyyti), Emmi Takkinen (kehittäjä)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-31-muistio)

**Yhteiset**
* Muistattehan tarkistaa ja sulkea "ratkaisu ehdotettu" -tilaiset tiketit, ettei ne jää roikkumaan avoimena.
* Tarratulostin-tiketti #4580 suljettu, koska se kävi jo liian massiiviseksi. Jos siellä on vielä jotain kehitysehdotuksia, joita ei ole huomioitu, niin tehkää niistä erilliset tiketit Kehitysehdotukset-projektiin.
* Finnassa asiakkaalle näkyvien palautuskehotusten maksujen otsikko "ei tietoa" ja selitteessä "Overdue - 1. huomautus"  tai "Overdue - 2. huomautus". 
  * Totesimme, että otsikkotieto "ei tietoa" ei anna luotettavaa kuvaa palvelusta ja selite tulisi olla asiakkaalle informatiivisempi. Pirkko-Liisa tekee tiketin kehitysehdotuksiin.

**Lumme**
* Mäntyharjussa sitkeä sähköpostiongelma. Viestit eivät mene edes roskapostiin. Kokeillaan Outin mallin mukaan lähetyssähköpostiksi noreply@koha-suomi.fi. Tähän asti olleet kuntakohtaiset osoitteet.
* On aika paljonkin tullut palautetta siitä että myös keskeytetyt varaukset lyhentävät laina-aikaa. Nytkin oli Hotakaisen Tarina-kirjalla 6 keskeytettyä varausta ja siitä johtuen 2 vkon laina-aika. Asetus laina-ajan lyhenemisestä automaattisesti varausten määrän mukaan, vaikuttaa tähän.

**Vaara**
* Valitettu valutuksen hitautta, Johanna selvittänyt asiaa. Vaarassa oli tuhansia aikaleimattomia nimekkeitä, ainakin osa tullut hankintaportaalin kautta. Tämä on yksi syy, miksi tiedot eivät tule Tätistä nimekkeille. Aikaleimoja päivitetty, seurataan tilannetta.
* Versionvaihdon jälkeen kaikki tilastoraportit eivät ole toimineet täysin, koska osa tiedoista haetaan nyt eri taulusta kuin aikaisemmin. Emmi korjannut näitä.
* Rantakylän kirjastossa valitettu palautuksen hitautta, jonka sanottu olevan syy siihen miksi asiakkaiden palauttamaa aineistoa löytyy hyllystä. Muista kirjastoista ei ole tullut vastaavaa tietoa, joten tämän syy jää vielä auki.

**OUTI**
* Koskelan kirjasto yhä suljettuna. Eräpäiviä taas siirretty eteenpäin eräpäivien erämuokkauksella. Saatavana-tilassa oleville niteille on muutettu nidetilaksi Muuttolaatikossa (ei lainattavissa, ei varattavissa). Reilu 10 000 nidettä.
* Finna-tuesta pyydettiin asiakkaille, joilla on Koskelan kirjasto varausten ensisijaisena noutopaikkana, muuttamaan se Oulun pääkirjastoksi, koska Koskelan kirjasto on poistettu varausten noutopaikkavalikosta, niin Finna ehdotti asiakkaille noutopaikaksi kirjastolistauksen ensimmäistä kirjastoa, eikä asiakkaat katsoneet varausta tallentaessa, mitä kirjastoa ohjelma ehdottaa varauksen noutopaikaksi. 
* Heikkisen Antti on pyytänyt Kirjastopalvelulta, että laittaisivat jatkossa osakohteille 035a-kenttään oman täsmäytystunnisteen, koska nyt on käynyt niin, että osakohteita on tuplana, jos Kirjastopalvelun korjaustietueissa on ollut mukana osakohteita.
* Tietueen vienti Melindaan oli epäonnistunut. Mikropalvelussa ei ollut conflict-tietueen numeroa, vain ilmoitus ”epäonnistunut”. Forcettamalla Anneli sain tietueen viedyksi.
* Henkilökunnalta tullut toive, että Listat-toiminnossa Luokka-sarakkeen tiedot, jossa kaikkien niteiden sijaintikirjasto ja hyllypaikkatieto, saisi poistaa kokonaan tai voisiko näkymän saada samanlaiseksi kuin tiedonhaun tuloksissa. Isoissa kimpoissa lista venyy kohtuuttoman pitkäksi. Pirkko-Liisa tekee tiketin kehitysehdotuksiin.
* Finnan lainahistoriassa, kun historian päivittää palautuspäivän mukaan, nimekkeen kohdalle tulee lainan eräpäivä eikä palautuspäivä. Samoin, jos historian järjestää lainauspäivän mukaan, tulee lainan eräpäivä. Virheestä mennyt 1.8. tieto Finna-tukeen, josta on vastattu, että tästä jo tehtävä olemassa.
* Koha alhaalla 1.8.2022 n. klo 17-17.15. Tietokannan päässä näkyy kuormapiikki kyseiselle ajalle. Selvää syytä kuormapiikille ei ole ainakaan vielä löydetty.
* Luetteloijat ilmoittivat, että esim. luettelointikentissä 1xx ja 65x ja 7xx lukot päällä eli kenttiä ei pääse muokkaamaan. Tiketti: [Redmine #5554](https://tiketti.koha-suomi.fi/issues/5554 )

**Lappi**
* Rovaniemellä automaatit hidastelleet edellisviikolla, mutta hitauteen saatiin apuja automaatimäärityksiä säätämällä
* normaaleja tukitoimia

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-31-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 30 muistio

Aika: 26.7.2022 klo 9.15
Läsnä: Päivi Knuutinen (Vaara), Anni Rajala (Vaski), Timo Pesonen (Lumme), Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Reetta Pihlaja (Siilinjärvi)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-30-muistio)

**Yhteiset**
* Kohan haussa jos rajaa saatavilla-oleviin, niin hakutulos rajautuu niihin tietueisiin, joissa on kaikki niteet saatavilla. Mukaan ei tule niitä tietuita, joissa jokin nide on saatavilla (mikä olisi siis se toivottu toimintatapa). [Löysin yhteisöstä bugin](https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=25375), joka näyttäisi liittyvän aiheeseen.
* [Kuitti- ja viestipohjat Redminessä](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Kuitti-_ja_viestipohjat.)
* Oudot osakohteet #5544 eli osalla tietueista näkyy osakohteita, vaikka niillä ei oikeasti ole niitä.
  * ongelma johtuu siitä, että osakohteet haetaan emon 001:n perusteella hakusanan katkaisulla, jolloin lyhyissä kontrollinumeroissa mukaan tulee myös niitä osakohteita, joissa on 773w:ssa samanalkuinen kontrollinumero.
* Perjantaina 22.7.2022 oli hidastelua Kohassa erityisesti liitännäisissä, tiedonhaussa ja kuvailussa, joka johtui siitä, että liitännäiset hakevat tarvitsemiaan JavaScript-kirjastoja ulkopuolisesta unpkg.com -palvelusta ja se oli alhaalla. Kun liitännäiset eivät saaneet tarvitsemiaan tietoja, jäi ne odottamaan niitä ja se näkyi hitautena Kohassa. Jotta tämä ei toistuisi, muutetaan liitännäiset käyttämään paikallisia kopioita JavaScript-kirjastoista. Tähän muutokseen menee hetki.
* Täti-Melinda-ongelmiin saadaan hiljalleen ratkaisuja, nyt kun Johanna palaili lomilta.
* [Hyllyvarausraportin korjauksia testattavana](https://github.com/orgs/KohaSuomi/teams/superlibrarians/discussions/3/comments/59)
* Keskeytetyt varaukset eivät ole jatkuneet 12.7.2022 jälkeen ohjelmavirheen vuoksi. Korjattu nyt.

**Vaara**
* Eilen kotipalvelun hoitaja tiedotti varausten keskeytysten "jumista" eli varaukset eivät jatkuneet kuten piti tietyn päivämäärän jälkeen. Selvisikin lopulta, että ongelma koski kaikkia tietyllä aikavälillä.
* Ongelmia pääkirjaston lainausautomaattien tilastoraportissa. Antaa yhden automaatin lainat, ei muiden, vaikka raportti aikaisemmin toiminut. Toukokuun tilasto jo virheellinen, mutta silloin antanut kuitenkin kaikille automaateille edes jotain. Nyt antaa vain yhdelle automaatille lukuja, muille tyhjää. https://tiketti.koha-suomi.fi/issues/5546

**Vaski**
* Kyseltiin tilannetietoa Finto-pluginista. Anneli uskoi, että Finto-pluginin työstäminen jatkuisi kun Nalkutin on saatu päiväjärjestyksestä pois.
* Toivottiin, että Redmineen saataisiin ajan tasalle tiedot siitä mitkä tietokantatriggerit ovart missäkin käytössä (voitaisiin sen perusteella tarkastella mitä turhaa intranetuserjs-asetuksissa on). Teknisestä dokumentaatiosta löytyy toimivat triggerit, mutta tieto niitä käyttävistä kimpoista ei ole ajan tasalla. Pyritään päivittämään jollain aikavälillä.

**OUTI**
* Ei mitään erikoisempaa. Normaalia tukipäivystystä.

**Siilinjärvi**
* ei mainittavaa

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-30-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 29 muistio

Aika: 19.7.2022 klo 9.15
Läsnä: Anneli Österman, Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen (Vaara), Kati Sillgren (Helle), Timo Pesonen (Lumme), Anni Rajala (Vaski)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-29-muistio)

**Yhteiset**
* Tulostusjonot tyhjennetään ke-aamuna 20.7.2022, jotta saadaan korjattua niihin liittyvä ongelma.
* [Ylimääräiset välilyönnit signumin lopussa](https://tiketti.koha-suomi.fi/issues/5495) aiheuttaa ongelmaa nidehaussa. Hakutulokset eivät valmistu, jos tulosjoukossa on niteitä, joiden signumissa on ylimääräisiä välillyöntejä lopussa. Koha-Suomi tekee ajon, joka poistaa ylimääräiset välilyönnit. Jokaisessa kimpassa kannattaa tarkistaa, onko lehtitilauksissa Luokka-kentässä ylimääräisiä välilyöntejä, koska ne päätyy myös niteisiin. Valmiissa SQL-raporteissa on uusi raportti [Lehtitilaukset, joiden luokka-kentässä on ylimääräisiä välilyöntejä lopussa](https://koha-suomi.fi/dokumentaatio/raporttikirjasto/#lehtitilaukset-joiden-luokkakent%C3%A4ss%C3%A4-on-ylim%C3%A4%C3%A4r%C3%A4isi%C3%A4-v%C3%A4lily%C3%B6ntej%C3%A4-lopussa), jonka avulla voi tarkistuksen tehdä. Lisätkää raportti oman kimpan tallennettuihin raportteihin.
* Uusi CSS-rimpsu [Iän piilottaminen Tiedot-sivulla](https://koha-suomi.fi/dokumentaatio/intranetusercss/#piilota-asiakkaan-ik%C3%A4-tiedot-v%C3%A4lilehdell%C3%A4), liittyen tikettiin #4698.
  * Koko IntranetUserCSS-sivu päivitetty ja lisätty Versionvaihto-projektista uudet ja päivitetyt rimpsut tuolle sivulle.
* Yhdenvertaisuusvaltuutetun toimiston vastaus kysymykseen, voiko hetuttomille henkilöille antaa lyhyemmän voimassaoloajan kirjastokortille kuin muilla henkilöasiakkailla on: "Vaikka kirjastokorttien voimassaolon rajoitus asettaa hetuttomat henkilöt eri asemaan, on korttien voimassaolorajoituksilla kuitenkin hyväksyttäviä ja oikeasuhtaisia tavoitteita kirjaston toiminnan turvaamiseksi. Emme myöskään katso, että kirjastokortin uusiminen välttämättä asettaa hetuttomat henkilöt sellaiseen epäedulliseen asemaan, mitä voitaisiin tulkita syrjinnäksi yhdenvertaisuuslain nojalla. Tällaisesta tilanteesta voisi olla kyse, jos hetuttomien henkilöiden kirjastopalveluita tai lainausoikeutta olisi rajoitettu laajemmin."
* deleteditems-taulussa timestampit ovat päivittynyt osalla niteistä versionvaihdon erilaisissa ajoissa versionvaihdon päivämäärälle ja poistotilastot heittää kuperkeikkaa. OKM-tilastoihin ei tarvitse jatkossa ilmoittaa poistotilastoja vaan he laskevat ne kaavalla. Ongelmaksi jää kokoelmatyön tilastot. Pohdinnassa on, että voisiko niteen lastseen-arvoa hyödyntää tietojen oikaisussa, mutta todennäköisesti ei pysty, koska tänä vuonna on saatettu poistaa nide, joka on oottanut hyllyssä viimeiset neljä vuotta ja lastseen-arvo on sen mukainen. 
  * Yhteisössä on bugi, jossa toivotaan erillistä deleted on -arvoa items-tauluihin, jolloin tilastot eivät olisi timestampin varassa.

**OUTI**
* Siirtoraportin määrityksiin lisätty myös ilmoitukset osakentille 084a,100a,100b,100c,110a,111a,245a,245b,245n,245p. Ilmeisesti vajaat määritykset olivat kopioituneet versiopäivityksessä testikannasta.
* 12.7. Kohan korjauspäivityksen seurauksena suomenkielinen palautussivu meni rikki eli kun palautti teoksen, tuli pelkkä valkoinen plankkosivu. Ongelma korjautui, kun kehittäjät tekivät templatecahcen tyhjennyksen.
* Niteiden muokkaus eräajona päätyy virheeseen 500, jos laittaa täpän kohtaan ”Täytä kentät oletusarvoilla, oletuspohjasta”. https://tiketti.koha-suomi.fi/issues/5526
* Tietueiden yhdistämissäännöt Z39.50/SRU—kyselyn kautta ei toimi. Ongelmaa pitää testailla, mistä johtuu. 
* Lyngsoen automaateissa kaikkien lainojen uusintatoiminnossa sip-lokille ilmestyy Kohan SIP-palvelimen HASH-viestejä. https://tiketti.koha-suomi.fi/issues/5530
* Käynnistellään pikkuhiljaa sähköpostiviestien lähettäjäosoitteen muutosprojektia, koska OUTIn viestejä menee asiakkailla hylkyyn ja roskaposteihin. 
* Noudettavissa olevan varauksen rikkoutumisongelmasta on saatu korjaus OUTIn testille. https://tiketti.koha-suomi.fi/issues/5484 

**Vaara**
* Versionvaihdossa tullut hyvitettyjen maksujen ongelma korjattu manuaalisesti Annelin ohjeen mukaan (tiketti 5465). Korjattavaa oli reilussa 400 asiakkaan maksutiedoissa.
* Eilen huomattiin, että versionvaihdossa henkilökunnan oikeuksiin on tullut kummallisesti ihan tarpeettomia oikeuksia. Täytynee käydä kaikkien oikeudet läpi ja korjata outoudet.
* OKM-tilastojen puute huolestuttaa, elokuun alussa tarvittaisiin tilastoja myös kaupungille osavuosikatsausta varten.

**Lumme**
* Vanhentuneiden varausten raportti ei anna tuloksia raportoidaan Savonlinnasta. Tarkistetaan raportin 563 SQL-koodi.
* Asiakkuutta luotaessa Hetu ei tallennu Sotu-avain kenttään. Sotu-avaimen lisäävässä JS-rimpsussa oli väärä tunniste sotu-avain-kentälle, joten versionvaihdon jälkeen lisätyille asiakkaille ei ole tallentunut sotu- avainta. Reilu 400 Sotuavaimetonta asiakasta kertynyt Lumpeille versionvaihdon jälkeen. Tehty tiketti ja asiakkaille lisätty huomautus: "Henkilötunnus puuttuu, olkaa yhteydessä kirjastoon". https://tiketti.koha-suomi.fi/issues/5535#change-26207

**Vaski**
* Automaatti-asiakaslajille tehdylle asiakasmääreelle asetettu Pakollinen-rasti aiheutti ongelmia kaikkien asiakkaiden tallentamisessa (tiketti https://tiketti.koha-suomi.fi/issues/5539).
* Osa kirjastoista ei ole vastaanottanut tilauksia hankinnan kautta vaan muokannut suoraan niteitä. Nyt tullut kysymystä siitä aiheutuuko tästä jotain suurempaa ongelmaa vai voiko näin toimia jatkossakin. Keskusteltiin siitä, että suositeltava tapa olisi vastaanottaa tilauksen hankinnan kautta, mutta jos näin ei haluta toimia, pitää tiedostaa että a) budjetti ei pidä paikkaansa b) jos avoimet tilaukset siirtää seuraavan vuoden budjettiin, siirtyy sinne käytännössä kaikki tilaukset mitä on tehty c) dateaccessioned-kenttään pitää muistaa päivittää saapumispäivä käsin nidettä muokattaessa. Vaara-kirjastoissa oli lisäksi tehty sellainen havainto, että hankinnan toiminnot olisivat hidastuneet jos tilauksia on paljon käsittelemättöminä.
* Palaverissa ei tullut mainittua, mutta tiedoksi kumminkin että Vaskissa on tehty ajot joilla poistettiin edit_catalogue ja advanced_editor -käyttöoikeudet niiltä käyttäjätunnuksilta, joilla oikeutta ei aiemminkaan ollut (tiketti https://tiketti.koha-suomi.fi/issues/5454). Vaskissa tultiin siis ennen versionvaihtoa siihen tulokseen, ettei tietueiden muokkaus -oikeutta haluta niin laajaan käyttöön (varsinkin kun niteiden eräpoistossa tietueen pystyy poistamaan myös ilman edit_catalogue -käyttöoikeutta mikäli kyseessä on tietueen viimeisen niteen poisto).

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-29-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 28 muistio

Aika: 12.7.2022 klo 9.15
Läsnä: Anneli Österman ja Pirkko-Liisa Lauhikaari (OUTI), Auli Rantasalo (Vaara), Reetta Pihlaja (Siilinjärvi), Anni Rajala ja Susanna Sandell (Vaski)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-28-muistio)

**Yhteiset:**

* Tiistai-aamun päivityksessä korjattiin seuraavat:
  * sähköpostittomille asiakkaille ei enää lähde sähköpostia tilin vanhenemisesta.
  * useamman tietueen pystyy nyt varaamaan kerralla.
* Muistattehan päivitellä Kohan ohje suomeksi -wikiä. [Päivitysvastuut sovittiin tammikuussa](https://koha-suomi.fi/paakayttajat2022#viikko-4-muistio). [Viikon 9 muistiossa](https://koha-suomi.fi/paakayttajat2022#viikko-9-muistio) on linkki GitHub-ohjeeseen, jossa neuvotaan myös wikin päivittäminen.
* Maanantaina 4.7.2022 suomenkielinen termi Piirros muuttuu termiksi Piirustus. Toive muutoksesta on tullut sekä arkistoilta että museoilta. Uusi termi on paremmin linjassa organisaatioiden kuvailukäytäntöjen kanssa, ja se vastaa merkitykseltään paremmin rajattavia aineistoja. Muutos kohdistuu ainoastaan käyttäjälle näkyvän aineistotyypin suomenkieliseen käännökseen, ei muihin kielikäännöksiin, eikä siihen, mitä metadatassa tulevia termejä ohjataan kyseisiin kategorioihin. Muutos ei vaikuta myöskään Finnan fasettirajaukseen perustuviin linkkeihin. Muutos ei edellytä toimenpiteitä Finnan asiakasorganisaatioilta.
  * Muutetaanko myös Kohassa Piirroksen kuvaukseksi Piirustus? Aineistotyypit luotiin vastaamaan Finnan materiaalityyppejä. Jos muutetaan, pääkäyttäjät voivat muuttaa arvon *kuvauksen* auktorisoiduissa arvossa MTYPE/PIIRROS. Itse arvoa ei saa muuttaa, jotta OKM-tilastot toimivat oikein.
  * Päätös: Muutetaan kuvaus Piirros -> Piirustus
* Jos käyttäjä yrittää sivulle, johon hänellä ei ole pääsyoikeutta, saa hän kirjautumisruudun ja sen yläpuolelle ilmoituksen "Sinulla ei ole oikeutta tähän sivuun". Koha myös kirjaa käyttäjän ulos. Uloskirjautuminen todennäköisesti uusi ilmiö verrattuna vanhaan versioon. Kannattaa tiedottaa muutoksesta kimpoissa.
* Täti ja KP:n päiväpaketit
  * Kirjastopalvelun päiväpaketit tuodaan Tätiin käyttämällä täsmäytyssääntöä 'RCN', johon oli määritetty, että täsmäytykseen käytetään kenttiä 035a ja 020a. Noilla säännöillä ei kuitenkaan osakohteet täsmäytyneet, koska niillä ei ole noita kenttiä olemassa. Testi-Tätissä oli samassa säännössä määritys, että täsmäytykseen käytetään yhdistelmää 001/003 ja Heikkisen Antin mukaan tuo riittää päiväpakettien osalta sekä emoille että osakohteille. Tuotanto-Tätissä on nyt samat säännöt ja täsmäytys tuntuisi toimivan oikein. Ennen säännön korjausta on kuitenkin voinut syntyä tuplaosakohteita joillekin tietuille, ne kannattaa yhdistää, jos niitä tulee vastaan.
* Huoltoikkunassa ke 13.7.2022 ei tiedossa katkosta.
* Editx:ssä on tehty muutos, että kaikki hinnat viedään verottomana. Taustalla syynä se, että Hankinnat-sivulla Tilattu-sarake laskee hinnat verrollisen hintakentän mukaan, jolloin budjetti näennäisesti ylittyy. Korjauksena myös tuohoon verolliseen kenttään viedään veroton hinta, jotta tilattu-sarakkeen tiedot näyttävät seurannan kannalta oikein verotonta hintaa.

**Lappi**
* Tanhuan ja Korvatunturin kirjastot lakkautettu, poistettu Kohasta
* Pieniä ulkoasumuutoksia IntranetuserCSS:ään
* Henkilöasiakkaiden tietojen voimassaoloaika 10 vuotta –muutosta edistetty: menossa esitys käyttösääntöjen ja tietosuojaselosteen muutokseen kimpan jorylle 1.9.  Voimassaoloaikaa ei vielä muutettu, koska henkilökuntaa ei ole tiedotettu. 
* Kohan ohjetta päivitetty Listojen ja korien osalta, vielä kesken, samoin osuus työkaluohjeiden päivityksestä

**OUTI**
* Laskutustyökalu-liitännäisestä oli hävinnyt versiopäivityksessä kirjastojen tietoja tai asetuksiin oli tallentunut vääriä tietoja.
* Oulun ja Raahen laskutuksen toteutus Finvoice-laskutusrajapinnalla odottaa Johannan lomalta paluuta.
* Versiopäivityksestä johtuvien tiedossa olevien ongelmien selvittelyä: mm. hyllyvarausraportin rikkoutumisia, tarratulostustyökalun omaan jonoon liittyviä ongelmia.
* Poistettavien niteiden taustatyökaluongelmat saattavat johtua siitä, että poistettavan niteen viivakoodi löytyy jo ennestään poistettujen taulusta.

**Siilinjärvi**
* Kohan ohje suomeksi -wikin päivitystä varovasti aloitettu

**Vaski**
* Hyllyvarausraportille toivottu näkyville 710a-osakenttää, jotta taidemusiikin äänitteiden osalta osassa tapauksista näkisi myös esittäjän nimen (ovat pääosin säveltäjän mukaan). Keskusteltiin ehdotuksesta yhdessä ja todettiin, ettei tätä lähdetä lisäämään, sillä ei oikein ole sopivaa kenttää mihin mäpätä (kyseessä lisäkirjaus, joten ei oikein haluta biblio.author-kenttäänkään). Turussa ei ilmeisesti edelleenkään käytetä niin aktiivisesti hyllyvarausten haussa tabletteja, joten hyllyvarausraportille kaivataan siksi välillä aika paljon tietoa.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-28-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 27 muistio

Aika: 5.7.2022 klo 9.15
Läsnä: Anni Rajala (Vaski), Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Auli Rantasalo (Vaara), Heli Auranen (Lumme), Kati Sillgren (Helle), Leena Kinnunen (Lappi)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-27-muistio)

**Yhteiset**
* Koha-Suomi on päättänyt, että tarratulostukseen ei toistaiseksi toteuteta ominaisuutta, jolla voi tarra-arkilla ohittaa käytetyt tarrat. Syynä on, että ei mahdollisteta tulostimien väärinkäyttöä. Tulostimien valmistajat eivät suosittele, että sama arkki syötetään uudelleen tulostimeen, koska sen mukana voi mennä mustetta ja likaa tulostimen sisään ja tulostin voi pahimmassa tapauksessa rikkoutua. Käytetystä tarra-arkista voi myös irrota tarroja tulostimen sisään, jolloin laite voi rikkoutua tai voi syntyä tulipalon vaara. Syyt on listattu myös [tikettiin 4580](https://tiketti.koha-suomi.fi/issues/4580).
* päivitys 5.7.2022 ei onnistunut, uusi yritys ke-aamuna.
* Viddlassa ongelma, että asiakkaat eivät voi jatkaa keskeytetyn elokuvan katsomista toisella laitteella. Syynä on, että palvelu ei saa asiakkaan ikätietoa enää samalla tavalla. Kirjastopalvelun kanssa on keskusteltu asiasta ja päädytty siihen, että he alkavat käyttämään borrowers/status-endpointia, jossa tulee tarvittava ikä mukana. Muutos vaatii heiltä teknisiä muutoksia.
* Tietueiden viennissä Melindaan on jonkinlainen vika, joka estää osakohteettomien tietueiden viennin Tätistä Melindaan. Osakohteellinen tietue siirtyy ja palaa ongelmitta. Ongelmaa tutkitaan.

**Lappi**
* Poistettu käyttäjätunnuskenttä asiakkaan muokkausnäkymästä
* Henkilökunnan käyttäjätunnusten tarkistus menossa, listat johtajien kommentoitavana
* Tarratulostusongelmia...
* Asiakastietojen voimassaoloa ei vielä muutettu 10 vuoteen, korjattava käyttösäännöt. Onko tehty massana nykyisten voimassaoloaikojen muutoksia?

**Vaski**
* Henkilökunnan tukipyyntöjen osalta tilanne tasaantunut
* Palautuskuitista valitettu, että niteiden näkymisessä kuitilla olisi joskus viive, mutta tämän ei pitäisi olla mahdollista. Anneli kehoitti pyytämään käyttäjiä tyhjentämään selaimen välimuistin.

**OUTI**

* Oulussa on oltu huolissaan, kun joillain asiakkailla on useampi varaus samaan tietueeseen. Anneli on tutkinut asiaa ja noin 14 000 tuhannesta varaajasta noin 40 asiakkaalla on kolme varausta tai enempi samaan tietueeseen. Suurimmalla osalla asiakkaista varauksia on vain yksi per tietue. OUTIn käyttösääntöjen mukaan asiakkaat saavat tehdä useamman varauksen per tietue.
* Muhoksen kirkonkylän alakoulun hyllytarkenteessa oli 11 merkkiä vanhan version aikana. Uudessa versiossa merkkejä sallitaan hyllytarkenteessa (items.sub_location) vain 10, jonka seurauksena tarkenteen kuvaus ei tullut näkyviin. Kun hyllytarkenteen nimestä otettiin yksi merkki pois, ongelma korjaantui.
* Budjeteissa tilattu-sarakkeeseen tulee alvillinen hinta ja käytetty-sarakkeeseen tulee alviton hinta, josta syystä näyttäisi, että budjetti ylittyy. Ongelmaa koitettu korjata viemällä alviton hinta siihen kenttään, josta tilattu-sarakkeen tiedot lasketaan. Tuloksena oli, että osassa tileistä tilattujen kokonaissumma suureni, osalla pieneni. Pitää vielä tutkia tarkemmin, miksi näin kävi.
* Hyllytarkenne-kentät eivät näy vielä verkkokirjastossa. Kansalliskirjaston Finna-tuki tutkii ongelmaa.
* Nidehaussa ei tule näkyviin tiettyjä hakutuloksia. Ongelma liittyy ilmeisesti RESTiin, tai siihen, että yritetään hakea tietuetta, jonka biblionumber on NULL.
* Versionvaihdon jälkeen tukipostien määrä rauhoittunut.

**VAARA**
* noutamattomat varaukset raportti (656)ei toimi luotettavasti. Anneli päivitti sen ja nyt toimii.

**LUMME**
* Palautuksessa Lumpeissa laitettu isompi fontti, jota jo säädetty, Laskutettu infolle. Samalla suurentuivat muut saman ryhmän tekstit esim. Viimeisteltävänä. Kovin isoina suurennetut tekstit menevät keltaisen infolaatikon sisällä päällekkäin. Myös ei lainata erottuu suuremman fonttinsa ansiosta.
* Varaushuomautus laitettu päälle. Ilmoituksen lähtemisaika on vielä liian pitkä ja teemme tiketin lyhyemmälle ajalle. Pääkäyttäjien Githubissa on varaushuomautuksesta keskustelunaloitus.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-27-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 26 muistio

Aika: 28.6.2022 klo 9.15
Läsnä: Christer Skog (Kyyti), Heli Auranen, Katja Valjakka, Timo Pesonen (Lumme), Auli Rantasalo (Vaara), Mikko Liimatainen (Vaski), Leena Kinnunen (Lappi)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-26-muistio)

**Yhteiset**
* [pilkut ja pisteet]:https://tiketti.koha-suomi.fi/issues/5481
* kehittäjistä paikalla 2 + harjoittelija
* Muistattehan, että uudessa versiossa on olemassa eräpäivien erämuokkaus, jota voi käyttää esim. yllättävissä kirjastojen kiinnimenoissa.
* korjattiin branchloc_084a_mainheading_signum_builder.pl, jossa tippui eka merkki, kun tieto otettiin 110a-kentästä


**Lappi**
* Käyttäjätunnuspyyntöjä tullut, oikeudet pyritty antamaan aiempien oikeuksien tapaan. Kootusti olisi hyvä olla tieto, mihin mikäkin oikeus vaikuttaa. 
* Nidetyyppikonversiossa jäi väärinymmärryksen vuoksi tekemättä nidetyypit lanu-aineistoille, jotta Rovaniemellä voidaan toteuttaa näiden myöhästymismaksuttomuus. Lisätty nidetyypit 14VRKLNLE	28VRKLN 28VRKLNES, myös kelluntasääntöön ja laina-maksutaulukoihin.
* Kellutus saatu toimimaan tekemällä pelkkä floatrules-järjestelmäasetus. 
* Tarratulostuksen kanssa edelleen ongelmia, esim. tiketti 5456.
* Muutamalla asiakkaalla lainatiedot lataantuvat hitaasti Kohassa, Finnassa tulee virheilmoitus, tiketti 5485
* Laitettu kuntoon myös muita säätöjä Intranetuserjs:ään ja muihin asetuksiin, esim. kirjastoautojen poikkeavat noutoajat laina-maksutaulukkoon.

**Kyyti**
* Kirjastopalvelun verkkokaupasta (Aarteesta) tilattua aineistoa ei tarvitse erikseen muokata, sillä hintatiedot on valmiiksi oikein. Tässä oli ollut vanhoja käytäntöjä joissakin kimpan kunnissa.
* Varaamo saatiin juttelemaan uuden rajapinnan kanssa vähin äänin ja on nyt taas tuotantokäytössä.
* Sähköinen kirjastokortti / Kouvola mobiili ei toimi uuden rajapinnan kanssa. Sovellus kuitenkin toimii vanhalla kirjautumisella, mikäli asiakas ei kirjaudu ulos. 
* Lehtien lisänumeron tallennus jää testattavaksi (tiketti 5436).

**Lumme**
* Muutamaan Marc- pohjaan tehty Antin (TäTiin) läpikäymät osakenttäjärjestykset. Indikaattoreita omat TäTit toivoneet valmiiksi
* Joillain lasten tiedoissa ollut punaisella Tili lukittu tai vastaavaa. Ei vaikuta lainaukseen, mutta ehkä kyseessä on riittävä määrä virheellisiä kirjautumisyrityksiä Finnassa. Uuden salasanan määrittely poistaa herjan. Taitaa olla uusi ominaisuus ja siksi kiinnittää huomiota.
* Viestin näkyminen Finnassa omientietojen alussa on mahdollista, mutta ei näy Lumpeissa (vielä)
* Varauksen noutomuistutus -täppä Kohan puolelta muokkauslomakkeelta asetuksen saa piiloon CSS-rimpsulla /* Noutomuistutuksen piilotus asiakaslomakkeelta */
body#pat_memberentrygen #memberentry_messaging_prefs tr:last-child { display:none; } Finnassa oma säätönsä

**Vaara**
* Auli kyseli mikä on tilanne Vaarassa versionvaihdossa tulleiden hyvitysmaksujen tilanne
* muutama kysely tullut työntekijöiltä mikseivät saa keskeytettyä kaikkia varauksia kerralla, liittyy annettuihin oikeuksiin
* muutama epäselvyys lehtien kellutukseen liittyen on ollut

**Vaski**
* Statistics/pseudonymized_transactions taulujen yhdistelyä eri raporteille koska versionvaihdon jälkeisiä ja edeltäviä tietoja ei enää saa yhdestä taulusta tarpeen mukaan.
* Jos nidemuokkaus auki, kun nide lainataan ja niteen tiedot tallennetaan lainauksen jälkeen tulee tilanne, jossa nide näyttää verkkokirjaston mukaan olevan vapaana, vaikka on lainassa.

**OUTI**
* OUTIssa ja Hellessä on ilmennyt semmoinen ongelma, että jos noudettavana olevan varauksen laittaa Siirto-toiminolla toiseen kirjastoon tai noudettavana olevan varauksen palauttaa jossain muussa kirjastossa kuin noutokirjastossa, niin Hyllyvaraukset-raportti menee rikki. Henkilökuntaa ohjeistamalla mennään siihen asti, että ongelmaan saadaan korjaus. Anneli on tehnyt raportin, jonka avulla Hyllyvaraukset-raportin rikkova varaus löytyy. [Redmine #5484](https://tiketti.koha-suomi.fi/issues/5484)
* OUTIn aineistobudjetit eivät näy samalla tavalla kuin ennen versionvaihtoa, kirjastojen budjetit oli ylitetty ja määrärahat käytetty, joten Anneli tutki mihin rahat on virranneet. Tässä versiossa tilattu-sarake/sivu laskee hinnat verollisen hinnan mukaan. Käytetty-sarake/sivu taas verottoman hinnan mukaan. Budjetti on veroton, joten se luonnollisesti on ylittynyt, kun toinen sivu laskee mukaan myös verot. Ehkä yksinkertaisin korjaus on viedä kaikkiin hintakenttiin veroton hinta, jolloin ei tarvitse tehdä järjestelmään koodimuutoksia ainakaan itse. [Redmine #5487](https://tiketti.koha-suomi.fi/issues/5487)

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-26-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 25 muistio

Aika: 21.6.2022 klo 9.15
Läsnä: Anneli Österman (OUTI), Heli Auranen, Timo Pesonen ja Katja Valjakka (Lumme), Kati Sillgren (Helle), Anni Rajala (Vaski), Irina Halminen ja Auli Rantasalo (Vaara), Christer Skog (Kyyti)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-25-muistio)

**Yhteiset**
* Ruotsinkieliset käännökset
  * Vaskilaiset lupasivat joskus aiemmin kysellä ruotsinkielisille käännöksille tekijää. Anni tarkistaa, onko muistettu kysellä ja jos ei, niin kyselee nyt. Anneli antaa tarvittaessa koulutuksen ja teknistä tukea käännösten tekemiseen.
* verkkokirjaston/restin kautta tehdyt uusinnat tilastoituivat versionvaihdon jälkeen API-käyttäjätunnuksen kotikirjaston mukaan. Tähän tehtiin ma 20.6.2022 korjaus, jossa uusinnat tilastoituvat nyt OpacRenewalBranch-asetuksen mukaisesti. Uusintojen tilastoitumisessa on näiden muutosten jälkeen [ongelma virkailijaliittymässä](https://tiketti.koha-suomi.fi/issues/5452). Uusinnat kirjautuvat uusinnan tehneelle kirjastolle. Eräpäiväkalenterina käytetään kuitenkin lainanneen kirjaston kalenteria. Pohdittiin, onko tämä ongelma vai looginen toimintatapa. Päätettiin, että seurataan tilannetta ja lasketaan verkkokirjastouusintojen osuus uusinnoista. Lisäksi viedään asia asiantuntijaryhmän pohdittavaksi ryhmän seuraavaan kokoukseen.
* 001-kenttään asetetaan nyt pluginilla biblionumber
* Päiväpakettien vienti Tätiin ei toiminut, Johanna tuo korjauksen yhteisöstä ti 21.6.2022.
* Kannattaa käydä muokkaamassa 999-kentät kuvailupohjissa ei-toistettavaksi.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-25-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 24 muistio

Aika: 14.6.2022 klo 9.15
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Heli Auranen, Katja Valjakka, Timo Pesonen (Lumme), Anneli Österman ja Piia Semenoff (OUTI), Reetta Pihlaja (Siilinjärvi, osan aikaa), Mikko Liimatainen (Vaski)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-24-muistio)

**Yhteiset**
* kirjastokortin numeron userid-kenttään kopioiva triggeri paikalleen kaikille kimpoilla?
  * sovitaan kimpoittain aikataulu, tehdään yksi yhteinen tiketti, johon pääkäyttäjät kirjaavat, kun heille sopii muutos. Myös he kirjaavat, joilla asia on jo kunnossa, että heillä asia on kunnossa.
* hankintapäivämäärä (dateaccessioned) puuttuu osalla niteistä, koska sitä ei ilmeisesti ole ollut datereceived-kentässä. Mitä laitetaan? 1.1.2000?
  * ajetaan pvm 1.1.2000
  * myöhemmin korjausajoja biblio-taulusta datecreated-arvon mukaan?
  * tarkistakaa, että kuvailupohjissa (erityisesti ACQ) dateaccessioned on pakollinen, jotta vastaavaa ei pääse tapahtumaan.
* vastaanotossa lisänumeron tallennuksessa ollut ongelma, johon löytyi korjaus
* omatoimen rajoitukset
  * jatkossa rajoitteen lisäävät kehittäjät pääkäyttäjien pyynnöstä. Support-lootaan salattu viesti, jossa asiakkaan borrowernumber, rajoitettu kirjasto (tunnus), rajoitusaika ja tarvittaessa huomautus. Asiakkaalle lisätään verkkokirjastossa näkyvä viesti, että hänellä on omatoimirajoite kirjastoon x ja mihin saakka se on voimassa.
* matrixin threadit käyttöön
  * testataan, auttaisiko asioiden seuraamisessa.
  * toiminnon saa päälle asetuksista -> kaikki asetukset -> laboratorio -> Threads
* koha-suomi xslt
  * Anneli tekee testauspyynnön superlibrarienseihin

**Vaara**
* Itä-Suomen AVIsta Virpi Launonen oli Vaara-johtajien kokouksessa viime viikolla ja häneltä kysyin asiantuntijaryhmässä puheeksi tulleesta hetuttoman asiakkaan kirjastokortin voimassaoloajan pituudesta, voiko se olla vuosi vai pitääkö olla sama kuin muilla henkilöasiakkailla. Tähän haluaisimme AVEilta yhtenäisen kannanoton, niin että kaikissa kirjastoissa meneteltäisiin samalla tavalla oikein. Virpi lupasi tiedustella asiaa heidän valtakunnallisessa keskustelufoorumilla, oli itsekin kiinnostunut tietämään mikä linja asiassa on.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-24-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 22 muistio

Aika: 31.5.2022 klo 9.15
Läsnä: Päivi Knuutinen, Auli Rantasalo (Vaara), Anneli Österman, Piia Semenoff ja Pirkko-Liisa Lauhikari (Outi), Reetta Pihlaja (Siilinjärvi), Tuomas Kunttu (Kyyti)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-22-muistio)

**Yhteiset**

* Versionvaihdon aikataulun koeponnistuksen tulokset
  * "Tarkistelkaa asiakkaiden maksuja, onko balanssit ok":https://tiketti.koha-suomi.fi/issues/5365
* Asiakastyyppien automaattiset päivitykset
  * Käykää merkitsemässä [tikettiin 5414](https://tiketti.koha-suomi.fi/issues/5414), miten kimpassa asiakastyypit muuttuu toiseksi. Esim. LAPSI->HENKILO
* Ominaisuudet/toiminnallisuudet, jotka eivät hyvin todennäköisesti tule toimimaan heti versionvaihdon jälkeen
  * Ceepos-kassayhteys
  * Finto-pluginit
* Testi-Finnoihin ei pääse kirjautumaan, koska testiponnistuksessa vaihtui [api-tunnus](https://github.com/orgs/KohaSuomi/teams/superlibrarians/discussions/8). Selvitellään, miten kannattaa toimia nyt api-avaimen kanssa.
  * Tiistaina avaimet Finnalle ja Viddlalle
* Päivittäkää loma-aikanne (myös vuosiluku) [Koha-tiimi-sivulle](https://tiketti.koha-suomi.fi/projects/mls/wiki/KohaSuomi_tiimi)

**Vaara**
* testailua, silloin kun testikanta ollut käytettävissä

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-22-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 21 muistio

Aika: 24.5.2022 klo 9.15
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Pia Kusmin ja Leena Kinnunen (Lappi), Reetta Pihlaja (Siilinjärvi), Anni Rajala & Mikko Liimatainen (Vaski), Kati Sillgren (Helle), Heli Auranen, Katja Valjakka, Timo Pesonen (Lumme), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-21-muistio)

**Yhteiset**

* Versionvaihdon kuivaharjoitukset

* testiltä siirrettävät tuontantoon: 
  * laina- ja maksusäännöt (admin/smart-rules.pl)
  * järjestelmäasetukset (admin/preferences.pl)
  * kirjastoryhmät (admin/library_groups.pl)
  * asiakastyypit (admin/categories.pl)
  * taulujen asetukset (columns_settings.pl)
  * työkaluliitännäiset (plugins/plugins-home.pl?method=tool)
    * tarratulostuspohjat
    * laskutukseen liittyvät pohjat
  * ilmoitukset ja kuitit (tools/letter.pl)
  * Marc-yhdistämisen säännöt (admin/matching-rules.pl)
  * Marc overlay rules (admin/marc-overlay-rules.pl)
  * maksutyypit (admin/debit_types.pl)
  * myöhästymisilmoitusten määrittely (tools/overduerules.pl)  Vaara, lisätty 30.5.

* [Ohjeet versionvaihdon ajalle](https://tiketti.koha-suomi.fi/news/32)

Helle haluaa:
* kuvailupohjat siirrettäväksi (tai talteen, jos ei siirretä suoraan)
* tulosta ilmoituksia sekä sotuteekki

**Vaara**
* testailua
* tarratulostusohje lisätty Redmineen, sitä voi täydentää tai muokata omaan tarkoitukseen

**OUTI**
* Testifinnassa yhteystietojen päivitys nyt onnistuu. Muutospyyntö tulee Kohaan.
* Tuotantofinnassa näkyvät nyt hyllypaikat sekä kirjastojen yhteydessä että Osasto-faseteissa.
* Nalkutin ei päästä läpi kentän 046 kaikkia tietoja. Nalkutin herjaa OUTIssa jostain syystä MARCin vastaisista virheistä, vaikka kyseiset kentät ja indikaattorit kuuluvat MARCiin. [Tiketti #5404](https://tiketti.koha-suomi.fi/issues/5404)
* Koskelan kirjasto yhä toistaiseksi kiinni. Kirjaston voimassa olevien varausten noutopaikat muutettu pääkirjastolle ja eräpäivät siirretty syyskuun loppuun. 

**Lappi**
* Testailtu, muuten rauhallista
* Kellutus ei suostu toimimaan vaikka säädöt tehty tikettien #5380 ja #4574 mukaan
* Tiedot-näytöllä (members/moremember.pl) ylimäääräisenä lainat-varaukset-rajaukset-laatikoita, ei kuitenkaan sisältöä. Kokeillaan onko vika IntranetuserJS-määrityksessä. 
* Palautuskuitti ei näytä nimeketietoja, tehdään pohja uudelleen

**Siilinjärvi**
* Testailtu, muuten rauhallista

**Vaski**
* Asiakasvarmenne päivitetty uuteen, sujui kaiken kaikkiaan hyvin

**Helle**
* Otettu käyttöön henkilöasiakastyyppien vanhentumisajaksi 120 kuukautta. (Olemassa olevien asiakastietojen voimassaoloaikojen pidennyspyyntö kehittäjille joskus versionvaihdon jälkeen.)

**Lumme**
* Tarrapohjien säätöä. Pieksämäellä Firefoxissa ei meinaa A4-arkille signumit osua ruutuihinsa, käytetään alkuun chromen tarratulostusta, johon oli suht helppo saada kentät paikoilleen. Lumpeissa useita tarrapohjia tulossa.
* Maksutyyppejä kokeilin lisätä, ohjelma hyväksyi, mutta ei ilmestynyt listalle. Muokkaaminenkaan ei onnistu.
* Kellutusryhmiä kokeiltu.
* Testikannan testailua ja säätämistä.

**Kyyti**
* Tarroissa teksti meni seuraavan tarran puolelle, sain vinkin säätää tarran oikeaa marginaalia.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-21-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 20 muistio

Aika: 17.5.2022 klo 9.15
Läsnä: Reetta Pihlaja (Siilinjärvi), Leena Kinnunen ja Pia Kusmin (Lappi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Mikko Liimatainen (Vaski), Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Anneli Österman ja PirkkoLiisa Lauhikari (OUTI)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-20-muistio)

**Yhteiset**


**Siilinjärvi**
* Kyseltiin onko kellään käytössä MaxFine eli myöhästymismaksujen enimmäismäärä -asetus nidekohtaisten enimmäismäärien lisäksi. Ei ollut. Otetaan tämä varmaan käyttöön, kun käyttösäännöissä on määritelty kerralla enintään perittäväksi 20 € myöhästymismaksuja.
* Tehty tiketti #5395 Varauksen noutomuistutus -valintamahdollisuuden piilottamisesta viestiasetuksissa.

**Lappi**
* Leena on palannut takaisin töihin
* Ranuan muuttoon littyvät työt alkavat työllistämään
* Uuden version testausta ja asetusten määrittelyä

**Vaara**
* Käyttäjäoikeuksia tarkasteltu ja tehty excel-taulukko, johon ryhmitelty eri oikeuksia tarvitsevia työtehtävien mukaan. Oikeuksia testatessa tuli esiin mm. tarratulostusoikeuden ongelma: uusi plugin tarratulostukseen vaatii oman oikeuden, mutta se ei yksin riitä, henkilö tarvitsee jonkun oikeuden myös tools-oikeuksien valikosta. Suositellaan inventointioikeutta, jos henkilö ei työssään tarvitse mitään muuta oikeutta ko. valikosta.
* Päivi päivittänyt Githubiin kuvailun käyttöohjetta. Kehittyneen editorin makrot toimivat ja niistä on kuvakaappaukset ja linkki joihinkin valmiisiin makroihin. Ainakin testikannassa on edelleen ongelmana viivalliset ISBN:t, ne eivät toimi oikein tuplatarkistuksessa, joten sellaisesta nimekkeestä tulee tuplatietue tietokantaan. Redmineen viittavat linkit päätettiin korjata sen jälkeen, kun näille tiedoille on olemassa uusi paikka, tällä hetkellä ei tiedetä mihin niitä tietoja siirretään.


**Vaski**
* Maksutyyppien muokkaus ei vaikuta automaattisiin maksuihin. Noutamattoman varauksen maksu ei ole sama kuin maksutyypeissä ja maksukuitille ei tulostu siitä selitettä.
* Uuden asiakasvarmenteen asennukset käynnissä.
* Versiopäivityksen aikataulusta toivottaisiin tarkempaa tietoa.
* CSS- ja JS-koodien tarkistukset menossa. Uudet koodit rikkovat välillä vanhoja, mikä tekee testaamisesta haastavaa.

**Helle**
* Otettu käyttöön omatoimikirjastojen käytön estoon asiakastyypi Lapsi, omatoimi sallittu
* Otettu käyttöön asiakastietojen Lisää huollettava -nappi (IntranetUserJS-rimpsu)

**Kyyti**
* Tarratulostuksen säätöjen kanssa tapeltu

**OUTI**
* OUTIssa mikrofilmejä ei ole voinut varata verkkokirjastossa, koska aineistotyyppinä on ollut kausijulkaisu. Finnan yleisissä varausasetuksissa on säädetty, ettei kausijulkaisuihin voi tehdä tietuetason varauksia. Tämän pystyy ohittamaan, mutta tällöin mahdollistuu varauksen teko myös tietuetasolla. OUTIssa tämä ratkaistiin niin, että mikrofilmien nidetyypeiksi muutettiin aikakauslehtien nidetyyppi "28 vrk - Lehti", joka mahdollistaa nidevarauksen tekemisen.
* Testi-finnassa asiakkaan yhteystiedoissa näkyy nyt myös varaustunnus ja postinumero, mutta korjauksen jälkeen yhteystietoja ei voi muuttaa, tulee ilmoitus: Updating of patron information failed. Ongelmasta mennyt tieto Finna-ylläpitoon.
* Tuotanto-finnassa hyllypaikkojen lisääminen fasetteihin vielä vaiheessa, pyydetty kirjaston yhteyteen ja erillisenä Osasto-fasettiin. Käännökset vielä puuttuvat.
* Finvoicen käyttöönotto Oulussa ja Raahessa versiopäivityksen jälkeen.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-20-muistio) - [Palaa sivun alkuun](/paakayttajat2022)


## Viikko 19 muistio

Aika: 10.5.2022 klo 9.15
Läsnä: Anni Rajala (Vaski), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Pia Kusmin (Lappi), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Anneli Österman, Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Reetta Pihlaja (Siilinjärvi), Kati Sillgren (Helle)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-19-muistio)

**Yhteiset**

**Vaski**

* Canon-tulostinta asennetaan Turun pk:lla kirjastokorttitulostamista varten.
* Kentältä kysytty miten toimitaan, jos huoltaja haluaa poistaa huollettavalta pin-koodin käytöstä. Ratkaisuna pin-koodin vaihto (ja huollettavan sähköpostiosoitteena huoltajan sähköposti).

**Vaara**
* Uuden version testausta, ei mitään muuta mainittavaa tällä kertaa.

**Lappi**
* Testausta ja määritysten tekoa.
* Rullatarran asettelu ei onnistu. Pitää pyytää apua Johannalta.

**Kyyti**
* Kyytin testikannassa lainattaessa lapsi-asiakkaalle, tulee aina virhe 500. Silti aineisto menee lainaan. Kaikilla muilla asiakastyypeillä lainaus onnistuu. #5383
* Tarvittavat kirjastoryhmät: hakuryhmät, kellutusryhmät, okm-ryhmät
* Mistä saa pois automaattisen uusinnan viestiasetukset? Oli jäänyt päälle AutoRenewalNotices-asetukseen arvo asiakkaan viestiasetuksen mukaisesti. vaihdettu ei koskaan.
* Finna-tiketin #5288 asiat eivät ole edistyneet. Päivitettiin prioriteetti välittömäksi. 

**OUTI**
* Edistetty hyllypaikkasijaintia Finnaan.
* Uuden version testausta.
* Koha-tuessa rauhallista.

**Siilinjärvi**
* Ei mitään muuta kuin testausta aina kun ehditään.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-19-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 18 muistio

Aika: 3.5.2022 klo 9.15
Läsnä: Heli Auranen, Katja Valjakka, Timo Pesonen (Lumme), Anneli Österman ja Pirkko-Liisa Lauhikari, Anni Rajala (Vaski), Päivi Knuutinen ja Irina Halminen (Vaara), Kati Sillgren (Helle), Reetta Pihlaja (Siilinjärvi), Pia Kusmin (Lappi), Tuomas Kunttu (Kyyti)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-18-muistio)

**Yhteiset**
* pseudonymisointi - päätetään, mitä asetukseen laitetaan päälle.
  * PseudonymizationPatronFields: Asiakas lisätty Kohaan (päivämäärä), asiakastyyppi, asiakkaan kirjasto, kaupunki, postinumero
  * PseudonymizationTransactionFields: kaikki
* ovedue-maksujen määrittely, siirrettäisiinkö koko maksukuvio kirjepohjien yhteyteen, jolloin voitaisiin liittää maksu mihin tahansa viestiin? / Kodo
  * voisi kelvata yhteisölle, siellä on hieman tämänsuuntainen tiketti, joka on kuitenkin pysähtynyt [Bugzilla #12769](https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=12769)
  * varsinaisen maksun lisäämisen asiakkaalle voisi kirjoittaa viestien käsittelyyn, kun viesti merkitään lähetetyksi ja sen voisi lisätä vain jos lähetys on onnistunut
  * maksun selitteeksi voisi tulla kirjepohjan otsikko suoraan ja tyypiksi vaikka joku "messages" tai sitten kirjepohjan koodi?
* [Tietoturvaohje päivitetty](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Koha-Suomen_tietoturvaohje) / Kodo
  * Varaustunnus (othernames) ei saa olla sama kuin korttinumero, koska varaustunnuksella ei ole tarkoitus päästä kirjautumaan järjestelmään
*  * tarkistakaa omat kohanne ja korjatkaa jos näitä on
*  * poikkeuksena huoltaja/takaajatunnukset, joilla ei muutenkaan pääse kirjautumaan 
  * Kahden rinnakkaisen tunnuksen käyttö ei ole suositeltavaa (kirjastokortti ja erillinen käyttäjätunnus)
*  * Tulisi lukita samaksi, koska rinnakkaisuus voi aiheuttaa sekaannuksia, toimintahäiriöitä ja avata ylimääräisiä hyökkäysreittejä
* Huoltokatko 11.5.2022
  * voi olla muutaman minuutin katko

**Lumme**
* Tarrapohjan tekoa ja signumien sijainnissa ongelmia
* Uuden version testausta ja säätämistä.

**OUTI**
* Anneli säätänyt ja testannut tarrapohjia.
* Koha-suomi.fi -selainvarmenteen uusiminen 27.4. aiheutti osalle käyttäjistä ongelmia kirjautumisessa Kohaan. Osalle ongelmaan on auttanut varmenteen uudelleen asennus ja osalle varmenteen todennuspäätöksen poistaminen selaimen tietoturva-asetuksista.
* Finnasta pyydetty fasetteihin rajausta myös hyllypaikan mukaan ja olisiko mahdollista rajata haku kirjasto- ja hyllypaikkarajauksella niin, että hakutulokseen tulee vain valitun kirjaston ja hyllypaikan teokset. Päätettävä, otetaanko rajausmahdollisuudet käyttöön sekä Kirjasto-rajauksessa että erillisessä Osasto-rajauksessa.
* Uuden version järjestelmäasetuksista käyty läpi muut paitsi Verkkopalvelut-osio.
* Vaalan kirjastossa otetaan käyttöön Koha-Ceepos-maksurajapinta version vaihdon jälkeen.
* Yhdelle asiakkaalle laitettu OUTIssa ensimmäinen omatoimikirjaston käyttörajoitus Kohaan.
* Oulussa 3.-9.5. auki lakon vuoksi vain pääkirjasto, Haukiputaan, Kaakkurin ja Myllyojan kirjastot. Omatoimikirjaston käyttö on mahdollista vain Kaakkurissa. Viikonlopun kaikki kirjastot ovat kiinni.
* Tehty uuden version testauksia.

**Vaski**
* Turun kaikki toimipisteet kiinni lakon vuoksi 3.-9.5.
* Portaalin tilauskori-sotku siivottu suurimmalta osin, mutta jäljelle jääneissä tilauskoreissa virheellisiä tilauksia ja lisäksi tilauksia luultavasti jäänyt tulematta. Woiman kanssa ei vielä saatu sovittua voidaanko puuttuville tilauksille tehdä jotakin.
* Yritetään aloittaa lähiaikoina Githubissa Kausijulkaisut -ohjeosion päivitys.

**Vaara**
* Viime viikolla virkailijalla ongelma kirjautumisessa. Salasanan vaihto ei auttanut, Koha ei hyväksynyt tunnusta vaan ilmoitti internal server errorin. Ongelma johtuu Vaarassa käytössä olevasta rinnakkaiskäyttäjätunnuksesta eli Kohaan voi kirjautua kirjastokortin numerolla tai erillisellä käyttäjätunnuksella. Virkailija oli (epähuomiossa?) vaihtanut lainaajatilinsä käyttäjätunnukseksi virkailijatilin kortin tunnuksen ja siitä syntyi ristiriita tietokantaan. Kuten tuolla yhteisissä asioissa mainitaan, tämä ei ole järkevä eikä tietoturvallinen tapa ja tästä pyritään pääsemään eroon mahdollisimman pian.
* Viime viikolla siivottiin myös varaustunnuksia, joissa oli joko käyttäjätunnus tai kirjastokortin numero. Henkilökuntaa ohjeistettiin olemaan hyväksymättä tällaisia tunnuksia varaustunnuksiksi.
* Koha-Suomen dokumentoinnissa kuvailuohjeen päivitystä tehty uuden version mukaiseksi sen mitä pystyy. Vielä ei ole kaikkia ominaisuuksia siirretty, joten ei voi saada kuvakaappauksia ja siten ohjeen päivitys ei onnistu.
* Vaaran henkilökunnalle ryhdytty kokoamaan Annelin tekemän listauksen pohjalta uuden version ominaisuuksista listaa niistä asioista, jotka Vaaran Kohassa muuttuu versionvaihdon jälkeen.
* Tarratulostuspohjat tehty 12 ja 14 tarran A4-arkeille. Toimii Päivin koneella, muilla testaus tekemättä.
* Lainaus- ja palautusautomaateilla (MikroVäylä ja Lyngsoe) otettu käyttöön uusintaominaisuus.

**Helle**
* Hankintaportaalin tilaussanomien virheellisyydet loppuneet. Tilaukset siirtyvät taas oikein Helle-Kohaan.
* Henkilökuntaa ihmetyttää/harmittaa, kun asiakastietojen Lisää taattava -toiminnon muokkauksessa asiakastyyppi Lapsi ei ole enää oletusasiakastyyppi (eli ensimmäinen valittava asiakastyyppi) Kirjastonhallinta-osiossa. Ensimmäisenä on nyt Holhottava aikuinen. Mistä muutos johtuukaan?
* overdue - maksujen uuteen määrittelykuvioon liittyen toive: tiettyjen kirjastojen osalta (koulukirjastot) saisi estettyä automaattisesti maksujen muodostumisen (ilman omia kirjepohjia)

**Siilinjärvi**
* Tarrapohjia työstetty meilläkin. Ei muuta ihmeellisempää.
* Maksut viestipohjien yhteydessä kävisi Siilinjärvelle oikein hyvin.

**Lappi**
* Vuoden 2021 lehtitilaukset suljettu ja kirjastoja pyydetty siivoamaan lehtitietueita.
* Versionvaihto työllistää kovasti


[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-18-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 17 muistio

Aika: 26.4.2022 klo 9.15
Läsnä: Päivi Knuutinen ja Auli Rantasalo (Vaara), Pia Kusmin (Lappi), Heli Auranen, Timo Pesonen, Katja Valjakka (Lumme), Reetta Pihlaja (Siilinjärvi), Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Mikko Liimatainen (Vaski)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-17-muistio)

**Yhteiset**
* kirjastoryhmät saatu pois search_groups-ryhmän alta. Käykää lisäämässä tarvittaville ryhmille "Käytä virkailijaliittymän hakuryhmille" -täppä, jotta ne tulee näkyviin Tarkan haun sivulle kirjasto-valikon alapuolelle kirjastoryhmiin.
  * ihan kaikkia kirjastoryhmiä ei tarvita jatkossa, joten ne voi poistaa. Mutta ensin pitää varmistaa, mitkä saa poistaa.
* "Korostetut kohteet" -suomennos?
  * säilytetään ennallaan.

**Vaara**
* ei erityisempää Kohasta muuta kuin testaamista
* Päivi kyseli tarratulostusmuokkauksen ohjeita, tänään uuden version tarratulostus käsittelyssä

**Lappi**
* Rovaniemen pääkirjaston muutto väistötiloihin on alkanut. Varaukset siirretty toiseen toimipisteeseen ja niteet ajettu ei-lainattavana tilaan.
* SmartBox palvelua testataan ja kaikki näyttää olevan ok (viestit, laitteen toiminta, jne.). Palvelu otetaan virallisesti käyttöön 9.5.
* Rovaniemen pääkirjaston aineisto on laitettu kellumaan koko Lappiin 14.4. alkaen. 
* Versionvaihtoon liittyvät työt jatkuvat. 

**Lumme**
* Tarra pluginia tutkittu
* ei muuten erikoisempaa.

**Siilinjärvi**
* Ei erikoisempaa meilläkään, yritetään taas päästä testaamisessa vauhtiin.

**OUTI**
* Verkkokirjaston Suomi.fi-maksujen rajapintamuutos Oulun kaupungin (kirjasto mukana) osalta toteutetaan marraskuussa.
* Asiakkaiden iki.fi-sähköpostiosoitteet, jotka asiakkaat ovat kääntäneet gmailiin, eivät ole menneet perille, koska gmail hylkää ne epäluotettavina tai roskaposteina. Iki.fi-sivustolla opastetaan käyttäjiä näihin ongelmatilanteisiin.
* OUTIssa ollaan luopumassa asiakastilien vanhenemisesta. OUTI-ohjausryhmä hyväkyy asian vielä toukokuun kokouksessaan.

**VASKI**
* Tarratulostustyökalun kanssa ollut ongelmia. Tarrat asettuivat arkille oikein vasta kun Firefoxin asetuksista muutti print.tab_modal.enabled arvoksi true.
* Hankintaportaalin aiheuttamat ongelmat yhä selvityksessä. Saapuneissa sanomissa ollut 29 tilausriviä, joista viimeinen puuttuvin tiedoin. Näistä muodostunut koreja, joissa näkyy 28 tilausta, mutta useat tilaukset eivät ole olleet oikeita tilauksia.
* Näytettävien osakohteiden määrälle tarve yli 600 kohdetta.
* Uuden version hauissa huomattu ongelmia. Tarkastellaan uudelleen indeksoinnin jälkeen. 


[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-17-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 16 muistio

Aika: 19.4.2022 klo 9.15
Läsnä: Päivi Knuutinen ja Auli Rantasalo, (Vaara), Anni Rajala (Vaski), Pirkko-Liisa Lauhikari (OUTI), Kati Sillgren (Helle)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-16-muistio)

**Vaara**
* Ei mitään erityistä Kohaan liittyvää, uuden version testausta vain.
* Automaattien toiminta pitkien pyhien aikana omatoimikirjastossa on ongelmallista, jos vika tulee automaattiin (esim. järjestelmäpäivityksen takia). Sattumalta Päivi kävi omalla asialla Outokummun kirjastossa omatoimiaikana toisena pääsiäispäivänä ja huomasi, että automaatti (MikroVäylä) ei toimi. Uudelleenkäynnistys auttoi ja automaatti jäi toimimaan sen jälkeen, mutta mitä olisi tehtävissä, että näistä käyttöongelmista tulisi tieto jollekin, joka voisi auttaa asiassa? Mitään varsinaista päivystystä ei voida järjestää, se on selvää kustannusten takia.

**Vaski**
* Kohan asiakasvarmenne vanhenee Vaskin osalta ensi kuussa, valmistaudutaan uuden varmenteen jakeluun. Jatkossa Vaski samassa syklissä muiden kimppojen kanssa.
* Mikro-Väylän ja Bibliothecan automaattia testattu uutta versiota vasten ja näyttäisi toimivan kuten pitää. attachment:Vaskin-automaattitestauksen-tulokset.xlsx
* Finna-testaus suoritettu myös, muu testaus vielä kesken mutta ihan hyvällä mallilla. Testausta saatu jalkautettua hankinnan, kausijulkaisujen, kuvailun ja tiedonhaun osalta muualle Turkuun.

**OUTI**
* Rauhallista, normaalia tuki- ja ylläpitotoimenpiteitä.
* Uuden version testausta.


[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-16-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 15 muistio

Aika: 12.4.2022 klo 9.15
Läsnä: Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen ja Auli Rantasalo (Vaara), Katja Valjakka, Timo Pesonen, Heli Auranen (Lumme), Pia Kusmin (Lappi), Mikko Liimatainen (Vaski), Kati Sillgren (Helle)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-15-muistio)

**Yhteiset**
* Ke huoltoikkunassa ei tiedossa katkoksia.

**OUTI**
* Pyhäjoelle Saaren koulukirjastoon tulossa Lyngsoen lainaava/palauttava-automaatti.
* Uuden version asetuksia käyty läpi. Vielä vähän kesken.
* Testattu Johannan tekemää uutta tarratulostustoimintoa.
* Anneli käynyt läpi OUTIn IntranetUserCSS-asetukset ja testannut mitkä toimivat uudessa versiossa ja mitkä ei.

**Vaara**
* testausta jatkettu uuden version toiminnoissa
* Hankintaportaaliin (ja muihin hankinta-asioihin) liittyviä ongelmia varten toivottu keskustelu- tms. palstaa hankintaa tekeville. Päätettiin kokeilla Oulun Teamsin kuvailukanavan käyttöä, koska paljon samoja henkilöitä näissä tehtävissä.

**Lumme**
* Hiljaista
* Testaus jatkuu

**Lappi**
* Lisää huollettava -nappi korjattu ja lisätty takaisin.
* Etusivun Asiakastietojen muutospyynnöt jumitti (Internal Server Error). Vika löytyi jo käytetystä varaustunnisteesta. #5340
* Rovaniemen remontti työllistää: kellunta, varaustennoutoautomaatti, varausten siirrot, jne.
* Versionvaihtoon liittyviä töitä tehdään se mitä keretään.

**Vaski**
* Laina- ja maksusääntöjen mahdollisuuksien selvittämistä. Vanhojen sääntöjen toisintaminen vaatisi uudessa versiossa jopa 2000 sääntöriviä.

**Helle**
* Hankintaportaalista edelleen ylimääräisiä tilaussanomia ja paljon. Johanna stoppasi tilaussanomien siirtymisen Helle-Kohaan pe 8.4.2022.


[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-15-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 14 muistio

Aika: 5.4.2022 klo 9.15
Läsnä: Päivi Knuutinen, Auli Rantasalo (Vaara), Reetta Pihlaja (Siilinjärvi), Anneli Österman ja Piia Semenoff (OUTI), Katja Valjakka, Timo Pesonen, Heli Auranen (Lumme), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Kati Sillgren (Helle), Noora Suvanto (Lappi)

[Kehittäjien viikon muistio](https://koha-suomi.fi/kohasuomi2022#viikon-14-muistio)

**Yhteiset**
* Koha suomeksi -wikin otsikoiden numeroinnin yhtenäistäminen
  * Päätettiin lisätä kaikille alaotsikoille numerointi. Tehdään wikin päivityksen yhteydessä.
* Maanantain kehittäjäpalsussa merkittiin prioriteetilla "välitön" ne tiketit, jotka on oltava toiminnassa, kun versio vaihtuu. Prioriteetti ei siis tässä yhteydessä tarkoita, että toiminto toteutetaan välittömästi.
* Seuraava huoltoikkuna ensi viikon keskiviikkona. Selvitetään, onko tulossa katkosta.
* Heikkisen Antti tarkisti viikon 13 palaverissa asetetut Koha2MARC-mäppäykset. Liitteenä lista päätetyistä mäppäyksistä. attachment:Koha2MARC-mappings.pdf

Lista Koha-kirjastojen yhdessä sopimista Kohan MARC-määrityksistä. Kimpat tallentavat määritykset omiin
testikantoihinsa, joista ne siirretään uuteen Koha-versioon 7.-8.6.2022.
Testikantaan tallennettuja mäppäyksiä voi testata tekemällä testikannassa uuden tai tallentamalla vanhan
tietueen.

Tietokannan kenttä|MARC-kenttä
---|---
Biblio.abstrac | 520 ‡a
Biblio.author | 100 ‡a, 110 ‡a, 111 ‡a
biblio.biblionumber | 999 ‡c
biblio.copyrightdate | (automaattisesti)
Biblio.datecreated | (automaattisesti)
Biblio.frameworkcode | 999 ‡b
biblio.medium | 245 ‡h
biblio.notes | 500 ‡a
biblio.part_name | 245 ‡p
biblio.part_number | 245 ‡n
biblio.serial | 942 ‡s
biblio.seriestitle | 830 ‡a
biblio.subtititle | 245 ‡b
biblio.timestamp | (tulee automaattisesti)
biblio.title | 245 ‡a
biblio.unititle | 130 ‡a, 240 ‡a
biblioitems.agerestriction | 049 ‡c
biblioitems.biblioitemnumber | 999 ‡d
biblioitems.biblionumber | (tulee automaattisesti)
biblioitems.cn_class | 084 ‡a
biblioitems.cn_item | 942 ‡i
biblioitems.cn_sort | 942 ‡6
biblioitems.cn_source | 942 ‡2
biblioitems.cn_suffix | 942 ‡m
biblioitems.collectionissn | 490 ‡x
biblioitems.collectiontitle | 490 ‡a
biblioitems.collectionvolume | 490 ‡v
biblioitems.datereceived | 942 ‡1
biblioitems.ean | 024 ‡a
Biblioitems.editionresponsibility | 028 ‡b
biblioitems.editionstatement | 250 ‡a
biblioitems.illus | 300 ‡b
biblioitems.isbn | 020 ‡a
biblioitems.issn | 022 ‡a
biblioitems.itemtype | 942 ‡c
biblioitems.lccn | (automaattisesti)
biblioitems.notes | (automaattisesti)
biblioitems.number | 830 ‡v
biblioitems.pages | 300 ‡a
biblioitems.place | 260 ‡a, 264 ‡a
biblioitems.publicationyear | 260 ‡c, 264 ‡c
biblioitems.publishercode | 028 ‡a
biblioitems.size | 300 ‡c
biblioitems.timestamp | (automaattisesti)
biblioitems.totalissues | 942 ‡0
biblioitems.url | 856 ‡u
biblioitems.volume | 362 ‡a
biblioitems.volumedate | (automaattisesti)
biblioitems.volumedes |c (automaattisesti)
items.barcode | 952 ‡p
items.biblioitemnumber | (automaattisesti)
items.biblionumber | (automaattisesti)
items.booksellerid | 952 ‡e
items.ccode 952 | ‡8
items.cn_sort 952 | ‡6
items.cn_source 952 | ‡2
items.coded_location_qualifier | 952 ‡f
items.copynumber | 952 ‡t
items.damaged | 952 ‡4
items.damaged_on | (automaattisesti)
items.dateaccessioned | 952 ‡d
items.datelastborrowed | 952 ‡s
items.datelastseen | 952 ‡r
items.enumchron | 952 ‡h
items.exclude_from_local_holds_priority | (automaattisesti)
items.holding_id | (automaattisesti)
items.holdingbranch | 952 ‡b
items.homebranch | 952 ‡a
items.issues | 952 ‡l
items.itemcallnumber | 952 ‡o
items.itemlost | 952 ‡1
items.itemlost_on | (automaattinen)
items.itemnotes | 952 ‡z
items.itemnotes_nonpublic | 952 ‡x
items.itemnumber | 952 ‡9
items.itype | 952 ‡y
items.location | 952 ‡c
items.materials | 952 ‡3
items.more_subfields_xml | (automaattisesti)
items.new_status | (automaattisesti)
items.notforloan | 952 ‡7
items.onloan | 952 ‡q
items.permanent_location | (automaattinen)
items.price | 952 ‡g
items.renewals | 952 ‡m
items.replacementprice | 952 ‡v
items.replacementpricedate | 952 ‡w
items.reserves | 952 ‡n
items.restricted | 952 ‡5
items.stack | (automaattisesti)
items.stocknumber | 952 ‡i
items.sub_location | 952 ‡S, 952 ‡j (952 ‡S on Koha-Suomen viritys, Vaskin käyttöönotossa tähän laitettiin
952 ‡j ja tarkoitus laittaa se kaikille muillekin versionvaihdossa)
items.timestamp | (automaattinen)
items.uri | 952 ‡u
items.withdrawn | 952 ‡0
items.withdrawn_on | (automaattinen)

**Lappi**
* Järjestelmäasetusten testaus jatkuu. Kysyttiin palaverissa järjestelmäasetuksista joiden nimessä on OPAC, liittyvätkö Finnaan vai pelkkään Kohan OPACiin.

**Vaara**
* Ei mitään erityistä.Päivi poissa,osallistui kyllä palaveriin.

**Siilinjärvi**
* Ei erityistä, henkilöstötilanne jatkuu tiukkana.
* Siili jatkaa pelkillä suomenkielisillä asiakasviesteillä kuten tähänkin asti.

**OUTI**
* Testikannan järjestelmäasetusten läpikäyntiä ja normaalia tukihommaa.

**Lumme**
* Järjestelmäasetuksien läpikäyntiä.
* Torstaina, 31.3., Pieksämäellä ja Rantasalmella oli pieni katkos Kohassa. Katkos n klo 10 kieppeillä. Syystä ei ole tietoa.
* Savonlinnassa verkkomaksu epäonnistunut. Syy ei ole vielä selvinnyt. Toivottavasti yksittäinen tapaus.

**Kyyti**
* Kyytissä viime viikolla pääkäyttäjäpalaveri, jossa jaettiin testausvastuita ja keskusteltiin asetuksista.
* Siirrettävät asetukset olisi hyvä listata johonkin. Anneli lupasi laittaa Githubin Superlibrarians-keskusteluun.
* Kävin läpi testin viestipohja. Toimiiko ODUE viestipohjissa maksujen näkyminen? Ei tiedetä, pitää testata, kun cronit laitetaan testissä päälle.
* Tilin maksutyypit: ylimmäisenä on tunnukseton _Unexpected type found during upgrade_, jota ei pysty uudelleen nimeämään eikä arkistoimaan (error_on_archive). Se näkyy asiakaspuolella ylimmäisenä Lisää maksu -toiminnossa. Ei nyt ihan akuutti asia, voi laittaa kuntoon versionvaihdon jälkeenkin.

**Helle**
* Hankintaportaalista tulee Helle-Kohaan ylimääräisiä tilaussanomia. Ensimmäinen havaittu pe 1.4.2022.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2022#viikko-14-muistio) - [Palaa sivun alkuun](/paakayttajat2022)

## Viikko 13 muistio

Aika: 29.3.2022 klo 9.15
Läsnä: Päivi Knuutinen, Auli Rantasalo (Vaara), Tiina Pietikäinen, Timo Pesonen, Heli Auranen (Lumme), Reetta Pihlaja (Siilinjärvi), Pia Kusmin ja Maria Joona (Lappi), Anni Rajala (Vaski), Anneli Österman, Pirkko-Liisa Lauhikari, Piia Semenoff (OUTI), Kati Sillgren (Helle)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-13-muistio

*Yhteiset*
* Käytiin läpi Koha2marc mäppäykset. Sovittiin, että annetaan tehdyt määritykset vielä Heikkisen Antin tarkistettavaksi.

*Vaara*
* Ei mitään erityistä, Päivi lomaili muutaman päivän. Jatketaan uuden version testausta.

*Lumme*
* Pikkuhiljaa tehdään uusia säätöjä testikantaan.

*Siilinjärvi*
* Onneksi ei mitään mainittavaa, koska henkilöstötilanne todella haastava just nyt. Yritetään testata kuitenkin, kun ehditään.

*Lappi*
* Uusi versio ja järjestelmäasetusten läpikäynti työllistää.
* Lappiin saatu vihdoin tehtyä korjausajo videopelien ja lautapelien osalta.
* Rovaniemen remontti/muutto lähenee. Pitääkö tehdä muutokset sekä tuotantoon että testille? Pyydetään kehittäjiä kopioimaan tehtyjä muutoksia tuotannosta testille, jotta voidaan testata niiden toimivuus myös uudessa ympäristössä (esim. kellutusmatriisi, laina-maksusäännöt, smartbox).

*Vaski*
* Mietitty Asiakkaan tiedot -näkymän muokkausta, koska viestit ja odottavat varaukset siirtyneet tietojen yläpuolelle. Laaditaan ehdotuksesta tiketti Redmineen.

*OUTI*
* Testattu Lyngsoen automaattia testikannassa. Vaikuttaisi hyvältä. Liitteenä testausmuistiinpanot. attachment:Versionvaihto2022_automaattitestaus.docx
* Oulussa vastaanotettiin 8 nidettä, kun olisi pitänyt vastaanottaa vain 2. Virkailija perui vastaanoton ja otti vastaan vain ne kaksi. Muuten näytti hyvältä, mutta tiedonhaussa kaikki 8 nidettä oli edelleen Saapunut-tilassa eikä virkailija tiennyt mihin kahteen niteeseen vastaanotto oikeasti oli kohdistunut. Neuvoimme menemään takaisin teoksen vastaanottoon, jolloin hän näkee mitä jäljellä olevia niteitä Koha ehdottaa vastaanotettaviksi ja niiden viivakoodien perusteella virkailija pystyi vertailemaan mitkä kaksi oli oikeasti vastaanotettu. Anneli laittoi OUTIssa päälle asetuksen AcqItemSetSubfieldsWhenReceiptIsCancelled, jolla pystyy määrittämään mihin tilaan nide menee, kun tilauksen vastaanotto perutaan.

*Helle*
* Ensimmäinen verkkomaksu, joka ei ole poistunut asiakkaan Helle-Koha-tiedoista.
* Muutama virheellinen saman tilin EDItX-sanoma. Hankintaportaalissa asiakasnumeron määrittelyssä puutteita.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-13-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 12 muistio

Aika: 22.3.2022 klo 9.15
Läsnä: Katja Valjakka, Timo Pesonen, Heli Auranen, Tiina Pietikäinen (Lumme), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Anni Rajala (Vaski), Pia Kusmin (Lappi), Tuomas Kunttu ja Christer Skog (Kyyti), Reetta Pihlaja (Siilinjärvi), Anneli Österman, Piia Semenoff (OUTI), Kati Sillgren (Helle)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-12-muistio

*Yhteiset*
* Koulutusvideoiden tekemistä Teams-kokouksina, kunhan K-S-ominaisuuksien siirrot valmiimpia.

*Kyyti*
* Tutkittu testikohaa, järjestelmäasetukset käyty läpi.
* Ensi viikolle kutsuttu Kyytin pääkäyttäjäpalaveri. Tarkoituksena keskustella uusista ominaiuuksista ja jakaa testausvastuuta.
* Mikroväylän etähallinta tulossa käyttöön (saatu tunnukset).

*Lumme*
* Kirjakaappi tulossa Mikkelin lähikirjastoon (varausten nouto). Toukokuussa tarkoitus ottaa käyttöön.
* Tutkittu uusia tulevia Kohan ominaisuuksia.

*Vaara*
* järjestelmäasetusten säätöä testikannassa. Automaatteja koskevat asetukset AllowItemsOnHoldCheckoutSIP ja HoldsNeedProcessingSIP aiheuttivat huolta, kun ei voi testata, mutta onneksi Outi ja Vaski voivat testata näitä
* muuten normaalia ylläpitoa, ei mitään kiirettä

*Vaski*
* Keskitytty uuden version järjestelmäasetusten läpikäyntiin, saataneen loppuviikkoon mennessä valmiiksi
* Uusia tukipyyntöjä tullut henkilökunnalta viime aikoina harvakseltaan
* Henkilökunnalle pidetään tänään verkkokirjaston ideointipaja, pääpaino yhteisen viestinnän ja sisällöntuotannon kehittämisessä
* Vaskissa pystytään näillä näkymin testaamaan uutta versiota MikroVäylän ja Bibliothecan automaatin kanssa

*Lappi*
* Järjestelmäasetusten läpikäyminen aloitettu.
* Luotu uusi tarrapohja leveälle rullatarralle viivakoodilla. 
* SmartBox-hanketta viety eteenpäin. Rovaniemi toimii pilottina "varaustennoutoautomaatti-hankkeessa", joka toimii samalla tyylillä kuin postin pakettiautomaatit.
* Rovaniemen remonttiin liittyviä töitä aloitellaan.
* Tietokannan/hankinnan siivousta tehty hiljaisina hetkinä. 

*Siilinjärvi*
* Järjestelmäasetusten läpikäyminen aloitettu.

*OUTI*
* Koskelan kirjaston vesivahinkosulku jatkuu, tehty erä- ja noutopäiväylityksiä lisää. Kuusamon kirjaston remotin loppusilaus, tehty eräpäiväylityksiä sinne myös. Pääkirjaston remontin aineiston muuttotoimenpiteitä tehty myös.
* Järjestelmäasetuksien läpikäynti vielä kesken. 
* OUTIn pääkäyttäjät lupasivat hoitaa uuden version automaattitestaukset Lyngsoen automaatilla. Testataan sitten, kun automaatti on yhteydessä testikantaan.
* ODUE1 / ODUE2: Saimme palautetta virkailijalta, että asiakkaan maksuissa lukee harhaanjohtavasti "Huomautus", kun pitäisi lukea Palautuskehotus. Tutkimme asiaa ja korjaamme paremmalla ajalla eli varmaan versiopäivityksen jälkeen.
* Asiakas oli poistanut vahingossa kaikki varauksensa Finnassa, joten mietimme, että voisiko Finnassa Varaukset -sivun "Peru kaikki varaukset" -napin tekstin muuttaa muotoon "Poista kaikki varaukset"? Toinen vaihtoehto olisi piilottaa nappi.
* Asiakkaan kanssa käyty pitkään keskustelua, kun hän ei saa kirjaston viestejä. As. oli selvittänyt omalta sähköpostin tarjoajaltaan (eräs valtion virasto), että Kohasta lähtevien sähköpostien pitäisi käyttää TLS:ää, jotta viestit eivät esty. Anneli kysyy asiasta kehittäjiltä.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-12-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 11 muistio

Aika: 15.3.2022 klo 9.15
Läsnä: Päivi Knuutinen ja Irina Halminen (Vaara), Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Pia Kusmin (Lappi), Reetta Pihlaja (Siilinjärvi), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Susanna Sandell (Vaski), Tiina Pietikäinen, Katja Valjakka, Timo Pesonen, Heli Auranen (Lumme), Kati Sillgren (Helle)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-11-muistio

*Yhteiset*
* Testikannat yhteisöversiossa
  * tiedonhaku ei vielä toimi, indeksointi tehdään tänään Siiliin, Lumpeeseen ja Kyytiin. Jos niissä ei ole ollut kummempia ongelmia, laitetaan ajo ensi yöksi Helleen, Vaaraan ja Lappiin. Outi ja Vaski ajetaan keskiviikon ja torstain välisenä yönä.
  * käännökset vielä vanhat, selvitellään, miten saadaan uudemmat.
  * Tehdään Githubiin Superlibrarians-ryhmään keskustelu, johon laitetaan keskitetysti Koha-Suomi-ominaisuuksien testauspyynnöt. Raportointi ongelmista Versionvaihto-projektin tiketteihin, jotta keskustelu pysyy kompaktina. Keskustelun voi laitta seurantaan halutessaan, jolloin saa sähköpostiin ilmoituksen uudesta viestistä.
* Uusi raportti: "Niteet ja asiakkaat, joiden nide on lainassa ja kiinni kuljetettavassa varauksessa":https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Valmiita_SQL-raportteja#Niteet-ja-asiakkaat-joiden-nide-on-lainassa-ja-kiinni-kuljetettavassa-varauksessa

*Vaara*
* Päivi tehnyt mm. järjestelmäasetusten käännöksiä, mutta valitettavasti käännöksiä ei vielä saa uuteen versioon (toivottavasti muutaman päivän sisällä saa)
* Finna-tukeen tehtiin pyyntö, että varaustunnistetta asiakas ei voi tallentaa tyhjänä (Koha ei hyväksy tyhjää varaustunnistetta) ja se muutos tapahtui saman päivän aikana

*OUTI*
* Anneli kaivanut nuorten selkokirjoista lainaus- ja nidetilastoja vuosilta 2017 ja 2021 liittyen Seinäjoen kaupunginkirjaston ErTeltä tulleeseen pyyntöön. Annelilla valmiita raporttipohjia, joita voi tarvittaessa hyödyntää.
* Tyrnävän Murron koululle tulossa uusi Lyngsoen kirjakaappi. Ei tule varausten noutopisteeksi.
* Henkilökunnalta tullut palautetta, ettei kaikki 0-kiertoiset niteet tule nidehaulla tehtyyn 0-kiertoisten raporttiin. Raportille tulee vain niteet, joilla Issues-taulussa on arvo 0. Niteillä, joilla arvona on null jäävät raportilta pois. Arvolla null oleville niteille voisi jossain vaiheessa tehdä korjausajon.
* Palautetut laskutetut niteet -raportin päivityksessä oli viivettä alku viikosta, joka johtui ilmeisesti kun kehittäjät testasivat/säätivät kimppojen uuden version testikantoja.
* Useammasta kirjastosta tullut viime aikoina palautetta, ettei gmailin s-postiviestit mene perille asiakkaille. Muistutettu taas kimpan kirjastoja, että ovathan pyytäneet kunnian it-tukea tekemään sähköpostipalvelimelleen SPF-säännöt, jotta sähköpostin lähettäjäpalvelimella (Bittigurulla) on oikeus lähettää heidän nimissään viestejä. 
* Henkilökunnalta tullut palautetta, ettei pääkirjaston muuttoon liittyvä nidetila ”Muuttolaatikossa” poistu automaattisesti, jos nide palautetaan palautusautomaatilla. 

*Lappi*
* Laskutuksen ohje saatu päivitettyä ja laskutus otettu käyttöön.
* Sähköpostien perillemeno takkuaa edelleen.

*Siilinjärvi*
* Ei mainittavaa.

*Kyyti*
* Tuli ilmoitus, että asiakas oli virkailijalta pyytäessään saanut palautuskuitin, jossa ei näkynyt palautettuja niteitä. 
Oulusta kerrottiin, että ainakin tilanteessa, jossa nide on lainattu toisesta kirjastosta ja palautettu toisen kirjaston automaattiin, virkailijan tulostamaan palautuskuitti ei tulostu palautettujen niteiden tietoja.
* Aloitettu uuden version ihmettely

*Vaski*
* Versionvaihdon asioita pyöritellään. Testauksen mahdollinen työnjako, katkon tarkka ajankohta ja tunnistautuminen mm e-aineistoihin katkon aikana mietityttävät.
* Vaskin Finnassa Searchspecs.yamlista oma versio, jolla säädetään hakutuloksen relevanssia. Nyt kävi ilmi, että se estää mm aihehaun 655-kentästä. Tarkoitus on säätää haku kuntoon säilyttäen oma relevanssi.
* Ilmoitukset vanhenevasta kirjastokortista eivät ole lähteneet, croni puuttui.

*Lumme*
* Huomattiin, että asiakas voi lainata 5 kpl lasten ja 5 kpl aikuisten konsolipeliä. Säännöissä on, että 5 konsolipeliä saa olla lainassa kaiken kaikkiaan. 
* Varkaudessa tyhjennetään väestösuojaa.

*Helle*
* Helle-Kohasta löytyi Kyyti-kimpan raportilla (kiitos Tuomas!) n. 500 tietuetta ilman 001-kenttää. 001-kenttäpuutteita on myös äskettäin tallennetuissa tietueissa. Mistä johtuukaan tuo? Helle-kuvailijoita pyydetty tarkistamaan, että käsitellyllä tietueella on 001-kenttä (ja siihen liittyvä 003-kenttä). Ja ilmoittamaan, miten toimien 001-kenttä on jäänyt puuttumaan. 


"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-11-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 10 muistio

Aika: 8.3.2022 klo 9.15
Läsnä: Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Reetta Pihlaja (Siilinjärvi), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Pia Kusmin (Lappi), Kati Sillgren (Helle), Timo Pesonen, Katja Valjakka, Heli Auranen (Lumme), Susanna Sandell (Vaski)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-10-muistio

*Yhteiset*
* Tätiin "yhteiset" viestipohjat?
  * Todettiin, että ehdotus on hyvä. Viestipohjia ei ole pakko käyttää, mutta halutessaan voi tarvittavan viestipohjan kopioida itselle ja muokata sen omalle kimpalle sopivaksi.
* "Versionvaihdon alustava aikataulu":https://tiketti.koha-suomi.fi/projects/versionvaihto/wiki/Aikataulu

*OUTI*
* Asiakkaalta tullut ihmettelyä, kun lainat voi uusia Finnassa saman päivän aikana useamman kerran. Kävi ilmi, että OUTIssa ei ole määritelty mitään laina- ja maksusääntöjen kohtaan ”Ei uusintaa ennen”. Osalla kimpoista ko. kohtaan on määritelty arvoksi 1 päivä vähemmän kuin nidetyypin varsinainen laina-aika on, eikä heillä uusinta saman päivän aikana useamman kerran ole mahdollista.
* Laskutusliitännäisen käyttäjä ihmetteli, kun kaikki laskutetut niteet on palautettu, asiakkaalta lähtee rajoite (=lainauskielto) pois automaattisesti, mutta asiakkaan huomautuksiin jää merkintä, että asiakkaalle tai hänen huollettavalleen on lähetetty lasku ja niteille jää laskutettutila päälle. Järjestelmä toimii asiakkaan kannalta oikein, koska kun hän on palauttanut tai muuten korvannut laskutetut aineistot, hänellä on oikeus päästä heti lainaamaan. OUTIssa selvitetään, sopiiko tämä käytäntö kaikille kimpan laskuttajille.
* Koskelan kirjasto meni viime tiistaina kesken päivän kiinni, koska rakennuksessa oli huomattu vesivuoto. Tehty sulkuun liittyviä toimenpiteitä, mm. oma noutoilmoituspohja, koska varaukset noudettavissa pääkirjastosta, erä- ja noutopäivien siirtoja. Kirjaston avaamisesta ei ole vielä tietoa.
* Tullut ilmi, että uuden kirjastoauton uusi automaatti on käyttänyt testitunnusta tammikuun alusta alkaen, jolloin kirjastoauto lähti reitille. M-V ei ollut päivittänyt ilmoitettua tuotantotunnusta automaattiin ennen tuotantokäyttöönottoa.
* Asiakas oli ottanut yhteyttä Kaukovainion kirjastoon ja ihmetellyt, kun Finnassa ei näy Maksut-sivulla hänen maksuja eikä painiketta, josta hän olisi voinut siirtyä maksamaan maksut verkkomaksuna. Sivulla ilmoitukset ”Ei maksamattomia maksuja” ja ”Kirjastojärjestelmään ei saatu yhteyttä. Tietoja, jotka liittyvät tiliisi kirjastossa, ei voida näyttää. Jos ongelma jatkuu, ota yhteyttä kirjastoon.” Kohassa maksut näkyivät oikein. Asiakkaan Laina-sivulla kyllä ilmoitettiin, että asiakkaalla on kertyneitä maksuja 21,46 €, josta syystä hän on lainauskiellossa. Tapaus ilmoitettu Finna-tukeen ja Koha-Suomen kehittäjille. 
* Huomen aamulla 9.3. klo 7-9 taas Kohan huoltoikkuna. Tulossa ainakin n. 20 s. käyttökatko.
* OUTIlle ja ilmeisesti kaikille kimpoille on tuotantoon laitettu tänään ylimääräisten kuljetustilojen tiputuskoodi. Testattu OUTIn testillä virkailijaliittymässä ja palautusautomaatilla ja todettu toimivaksi.

*Vaara*
* Irina testannut liikuntaesineille kuvien saamista Finnaan, saa virheilmoituksen kuvia ladattaessa. Tutkitaan asiaa.
* ei muuta mainittavaa

*Siilinjärvi*
* Myös meiltä puuttui laina- ja maksusäännöistä ei uusintaa ennen -määritys, mutta kukaan ei ollut tainnut edes huomata sitä Finnassa.
* Huomautus edelliseen: arvo 1 kyseisessä sarakkeessa esti meillä uusinnan kokonaan päivää ennen eräpäivää asti. Päivin ohje: arvo on 1 päivä vähemmän kuin normaali uusinta-aika.
* Yhteiset viestipohjat on hyvä idea, vaikka meillä on käytössä vain suomenkieliset viestit. Kielivalinta ei ole myöskään näkyvissä asiakastiedoissa kirjastonhallinnassa.
* Ei muuta mainittavaa.

*Kyyti*
* Ollaan tutkittu AllowItemsOnHoldCheckout-asetusta. Meillä on ollut älä salli, jolloin ei asiakas ei ole voinut lainata nidettä, johon kohdistuu varaus. Kuitenkin hän on sen voinut lainata tiskillä, koska paikalla olijalla on etuoikeus. Testaus on kesken.
* Henkilökuntaa on vaihtunut sen verran on, että on alettu taas ihmetellä eri asiakkaiden samoja varaustunnisteita. Meillä varaukset on järjestetty neljän viimeisen numeron mukaan. Pitää kerrata taustaa asialle.

*Lappi*
* Gmail ilmoittelee "ei turvallisesta" viestistä ja osa viesteistä on kääntynyt takaisin kirjastolle. Ohjeistettu tarkistamaan kunnan/kaupungin tietohallinnosta, että siellä on tarvittava SFP-sääntö. Muistutetaan kirjastoja myös auttamaan asiakkaita sähköpostin käytössä ja sallimaan kirjaston viestit sähköposteissaan.
* Remontit/kiinniolot työllistävät varmaan koko kevään.

*Lumme*
*  Mikkeli palauusautomaatti hajosi.
* Laina- ja maksusäännöissä myös Lumpeilla ”Ei uusintaa ennen” kohta tyhjä, korjataan asia. Eli asiakas pn voinut uusia Finnassa saman päivän lainoja.
* Osassa Lumpeita tullut asiakkaille ilmoituksia tietoturvallisuudesta (kuten Lapille). Ilmoitetaan tietohallinnoille säätöjen tarpeesta.

*Vaski*
* laskutuksen hiontaa vielä, mm laskutuslisän lisääminen asiakkaan maksuihin niille joilla tällainen on ollut aiemmin käytössä (PDF-lasku)
* Ruskon pääkirjasto meni kiinni homevaurion takia, aineistoa jaettu usean muun kunnan toimipisteen kesken. Ns yhdensuuntainen kellutus. Turun kirjastoautoille pysäkki Ruskolle ja sille uusi yksikkö, jotta saadaan varaukset kohdistumaan
* Verkkokirjastoon Vaskin näkymään suunnitteilla: Peru kaikki varaukset -painikkeen piilottaminen, Lehtivarauksen jononumeron piilottaminen 



"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-10-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 9 muistio

Aika: 1.3.2022 klo 9.15
Läsnä: Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen, Auli Rantasalo, Irina Halminen, Tiina Vauhkonen (Vaara), Pia Kusmin (Lappi), Timo Pesonen, Katja Valjakka, Tiina Pietikäinen, Heli Auranen (Lumme), Reetta Pihlaja (Siilinjärvi, klo 10 asti), Kati Sillgren (Helle), Mikko Liimatainen (Vaski)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-9-muistio

*Yhteiset*
* Onko toiveita, missä järjestyksessä "K-S-ominaisuuksia":https://tiketti.koha-suomi.fi/projects/versionvaihto/issues toteutetaan?
  * päivittäiset välttämättömät: lainaukseen, palautukseen, hyllyvarauksiin
* Versiopäivityksen "testausohjeita":https://tiketti.koha-suomi.fi/projects/versionvaihto/wiki/Testausohjeet ja "aikataulu":https://tiketti.koha-suomi.fi/projects/versionvaihto/wiki/Aikataulu
* Asiakkaan tietopyyntöön liittyvää linkkiä ei lähetetä jatkossa enää asiakkaan s-postiin, koska s-postiin tuleva linkki, joka vei tietopyynnön verkkosivulle ei enää toimi. Tietopyynnöt otetaan pdf-tiedostona ja toimitetaan asiakkaalle jotenkin turvallisesti. Toiminnallisuudesta luovutaan versionvaihdoksen yhteydessä. Jatkossa tietopyynnöt pyydetään kehittäjiltä.
* Uusi versio GitHubin käyttö -ohjeesta, mukana myös wikin päivittäminen: attachment:GitHubinkaytto.pdf

*OUTI*
* Asiakkaalta tullut ihmettelyä, kun gmailin s-postiin tuleviin OUTIn s-postiviesteihin tulee kysymysmerkki, joka tarkoittaa sitä, ettei viestiä ole todennettu. Koska Kohasta lähetettävät viestit lähetetään Bittigurun palvelimelta kuntien domainien nimissä, domainien haltijoiden pitää sallia viestien lähetys Bittigurun nimissä. Kaikissa OUTIn kunnissa sitä ei oltu tehty, pyynnöstä huolimatta. Versiopäivityksen jälkeen s-postiviestin lähetykset siirretään lähtemään Koha-Suomen palvelimelta.
* Asiakkaalta tullut kehitysehdotus, että tulisi muistutus tekstiviestillä varauksen noudosta ennen viimeistä noutopäivää. Uudessa versiossa on viestipohja HOLD_REMINDER.
* Marc-mäppäysten uudelleen tallennuksen jälkeen Mikropalvelu valutti tietueet uudelleen tietueille, joille ei ollut aiemmin tallentunut ean-koodi tietokantaan virhetilanteen vuoksi. Kun mäppäykset korjattiin ja tietueet tallennettiin uudelleen, ean-koodi tallentui myös tietokantaan ja Mikropalvelu teki valutuksen kuin pitääkin. 
* Kempeleen liikuntavälinelainaamo aloittaa maaliskuussa.

*Vaara*
* OKM-raporttien tulokset ovat täysin mielivaltaisessa järjestyksessä, kun avaa raporttisivun. Toki oikean raportin löytää, kun järjestää raportit id:n mukaan uudelleen pariin kertaan, että saa uusimman ylimmäiseksi, mutta olisi kiva jos olisi aina tässä järjestyksessä
* Ihmetelty Heinäveden kanssa raportilla Aineistotyypitön monografiatietue saatuja tuloksia. Nimekkeiden joukossa on jopa nimeke, josta viimeinenkin nide on poistettu viime vuonna. Raportin tuloksessa nimekkeissä 942-kenttä on tuplasti (ei siis puutu vaan on kahteen kertaan) ja ihmetys kohdistuu siihen, mistä näitä virheitä tulee. Olen ottanut raportin muutaman viikon välein ja eilen listalla olleet 11 nimekettä (9 Blu-ray, 2 cd-rom) olivat siis uusia virheitä.

*Lappi*
* Laskutuspohjat, laskutusryhmät ja asetukset saatu tehtyä. Johanna siirtää ne testiltä tuotantokantaan ja testikanta vapautuu uudelle versiolle.
* Marc-pohjat tarkistettu.

*Lumme*
* Pieksämäellä tehty laskutus eilen ensimmäistä kertaa uutta laskutuspohjaa käyttäen. Hyllytarkistusraporttia laskuttaja toivoi vielä ja semmoisen rapsan saimmekin Vaarasta.
* Mikkelissä lainauksia mennyt väärälle kortille (henkilökunnan lapselle). Vaihdetaan lapsen kortti.

*Siilinjärvi*
* Ei mainittavaa.

*Helle*
* Tilaukset siirtyvät nyt oikein Hankintaportaalista Helle-Kohaan. Jeee!
* Ylläpidon Marc-määritykset OK-klikkailtu. Erikoisuus biblio-taulun olemassa olleisiin määrityksiin liittyen: kentät 260c ja 490a näyttivät määritellyiltä, mutta kytkös puuttui kenttien Muokkaa-toiminnosta. Kenttien 260c ja 490a kytkökset lisätty nyt.
* Maanantaina 28.2.2022 illansuussa muuttui ei-kelluvien kuljetettavien niteiden käyttäytyminen. Tiketti #5280. 

*Vaski*
* Versionvaihdon testauksen suunnittelu aloitettu


"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-9-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 8 muistio

Aika: 22.2.2022 klo 9.15
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Tiina Pietikäinen, Timo Pesonen, Heli Auranen, Katja Valjakka (Lumme), Pia Kusmin (Lappi), Tuomas Kunttu (Kyyti), Reetta Pihlaja (Siilinjärvi), Anneli Österman, Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Kati Sillgren (Helle), Mikko Liimatainen (Vaski)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-8-muistio

*Yhteiset*
* GitHubin käyttöohje: attachment:GitHubinkaytto.pdf
* "Tiketin 4780":https://tiketti.koha-suomi.fi/issues/4780 taustalla oleva syy saattoi löytyä puutteellisista Kohan MARC-määrityksistä. Määritykset eivät ole tallentuneet kaikille kuvailupohjille ja mäppäyksen uudelleentallennus vie määrityksen kaikkiin kuvailupohjiin. Eli kaikkien kimppojen kannattaa käydä napsuttelemassa läpi kaikki Kohan MARC-määritykset (Muokkaa ja sitten OK). Jatkossa, jos muistaa, kannattaa käydä kliksuttelemassa ainakin standarditunnisteet uudelleen, jos tekee uusia kuvailupohjia.

*Vaara*
* Hankintaportaalin virheestä johtuva tuplatilauskorien sotku aiheuttanut töitä, toivottavasti ei sentään kuluja muuten kuin työajan kohdalla. Täytyy seurata tilannetta.
* Bugin 4780 selvittelyä eli tallennamme uudelleen MARC-mäppäykset varmuuden vuoksi.
* Selaimen versionvaihto aiheutti tietenkin ison kuittikirjoitinrumban. Henkilökunnalla ei ole oikeuksia tehdä kaikkia asetuksia koneille, joten Meitaa jouduttiin pyytämään apuun. Sen jälkeen vielä sotkua asiakaskoneiden selaimen vaihdon kanssa, aloitusnäytöksi vaihdettu väärä näkymä, joka kyselee varmennetta.

*Lumme*
* Asiakkaalla kirjasta tullut maksu (ja maksettu 18.2.2022). Muutoslokissa näkyy eräpäivä 4.2.2022. Asiakkaan Finnan lainahistoriassa teoksella on eräpäivä 28.2.2022 (Asiakas näytti puhelimestaan). Teos uusittiin 18.2. ja eräpäiväksi tuli 18.3. Maksu maksettiin, mutta asiakas tuli seuraavana päivänä ihmettelemään miksi meni maksu, vaikka hänelle näkyi eräpäivä 28.2.
* Tullut esiin perille menemättömiä varausilmoituksia ja niiden yksilöinti oli hankalaa. Nidetunnuksen jos laittaa, viesteissä näkyy yksilöinti.
* Esinekuvat eivät näy Finnassa. Ovat kuitenkin tulleet konesalipäivityksessä uudelle palvelimelle. Anneli ehdotti 800 kentässä osoitteen vaihdon.
* Hankintaportaalin virheestä johtuva tuplatilauskorien sotku näkyy myös Lumpeissa.

*Lappi*
* 16.2. siirtyneet ylimääräiset EditX-sanomat aiheuttaneet harmia. Kirjastoja ohjeistettu korjaamaan virheelliset tilauskorit itse.
* Laina- ja maksusääntötaulukkoon hieman korjauksia.
* Paljon pientä ylläpidettävää, kysymyksiä, päivityksiä raportteihin, jne.

*Kyyti*
* Onko keinoa estää varaaminen Finnassa, mutta sallia virkailijaliittymässä?
- Järjestelmäasetus AllowHoldPolicyOverride Salli/älä salli henkilökunnan ohittaa varaussääntöjä varauksia tehdessään.
* Kyytissä alkoi Kohaan tulla pienistä kunnista jonkin verran epäonnistuneita paperisia viestejä, saapumisilmoituksia lähinnä. Syyksi paljastui pienten kirjastojen tapa soittaa asiakkaalle varauksesta ja sen jälkeen peruuttaa viesti eli Tulosta ilmoituksia | Peruuta -> viestin lähetys "epäonnistunut"

*Siilinjärvi*
* Ylimääräiset 16.2. tilauskorit siivottu pois
* Tiketti #5261 mietitytti, meillä on ilmeisesti aineiston vastaanotossa muutettu käsin korvaushinta jo valmiiksi verottomaksi.

*OUTI*
* Raahen kirjastossa on pari kertaa tullut vastaan tilanne, ettei sotu avain ole tallentunut automaattisesti asiakkaan sotu-kenttään, kun Koha on ilmoittanut asiakkaan sotun lisäysvaiheessa, että sotu on jo olemassa. Sotun lisäystä oli yritetty ainakin toisessa tapauksessa useammalla koneella, selaimella ja selainversiolla onnistumatta siinä. Sotu-avaimen lisääminen oli lopulta onnistunut toisena päivänä.
* Pääkirjaston muuttoon liittyviä kokoelmien siirtoja tehty.
* Luetteloinnista tullut pyyntö, saisiko Siirtoraportti-liitännäiseen sellaisen muutoksen, että tietue-linkit muuttuisivat toisen väriseksi sen jälkeen, kun käyttäjä on klikannut niitä (https://tiketti.koha-suomi.fi/issues/5276).
* Woima oli tehnyt hankintaportaalissa jonkin korjauksen Aurora-kirjastoille, joka oli vaikuttanut myös OUTIn tilauksiin niin, että joillekin kirjastoille oli muodostunut uudet tilauskorit jo tilattuihin ja toimitettuihin aineistoihin (tilaukset tehty 2019, 2020, 2021). Oulun ylimääräiset tilaukset olivat syntyneet myös hankintaportaaliin eli kaikki ylimääräiset tilaukset pitää selvittää portaalista pois Woiman kanssa, etteivät laskuta niistä enää kirjastoa. 
* Virkailijalle oli tullut vastaan peli, jossa oli ollut viivakooditarra ja infotarra, mutta nidettä ei ollut löytynyt tietokannasta. Nidettä ei löytynyt myöskään poistettujen niteiden taulusta, mutta tietue löytyy poistettujen tietueiden taulusta vuodelta 2018. Mysteeriksi jää, miten on pystytty tulostamaan infotarra niteelle, jota ei ole koskaan ollut järjestelmässä.
* Finnassa on ollut lähes vuoden käytössä ominaisuus, joka ainakin OUTIssa on jäänyt huomaamatta eli käyttäjälle lähetetään vahvistusviesti annettuun sähköpostiosoitteeseen Finna-tilin luomisen yhteydessä ja vaihdettaessa Finnaan tallennettua sähköpostiosoitetta. Uusi tili tai osoite tulee voimaan vasta, kun käyttäjä on klikannut vahvistusviestin linkkiä. Sähköpostiosoitetta vaihdettaessa myös vanhaan osoitteeseen lähetetään ilmoitus tapahtumasta.
* 22.2.2022 olisi Finnaan pitänyt tulla korjaus, että asiakas pystyy poistamaan oman s-postiosoitteensa itse verkkokirjastosta. Ei toiminut ainakaan vielä.
* Läpikäyty uuden version ominaisuuksia mitä niistä otetaan käyttöön OUTIssa.

*Helle*
* Hankintaportaalin tilaukset eivät siirry Helle-Kohaan.
* Miten Nidehaun hakutuloksen saa Exceliin? Kiitos Anneli, kun näytit palaverissa tavan. (Nidehaun tulosten vienti Exceliin -tiketti vuodelta 2018 #2915)

*Vaski*
* Ylimääräiset tilauskorit poistettu
* Kaukopalveluvaraukset jäävät lainaamisen yhteydessä noudettavana-tilaan

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-8-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 7 muistio

Aika: 15.2.2022 klo 9.15
Läsnä: Katja Valjakka, Timo Pesonen, Heli Auranen (Lumme), Reetta Pihlaja (Siilinjärvi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Pia Kusmin (Lappi), Anneli Österman ja Piia Semenoff (OUTI), Kati Sillgren (Helle), Mikko Liimatainen (Vaski)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-7-muistio

*Yhteiset*

* Lokitukset kaikille samoiksi (uudessa versiossa)
  * Ehdotus: laitetaan uudessa versiossa päälle seuraavat lokitukset:  AcquisitionLog,  AuthFailureLog,  AuthSuccessLog (tämä ei ehkä pakollinen),  BorrowersLog,  CataloguingLog,  FinesLog,  HoldsLog,  IssueLog,  RenewalLog,  ReturnLog
* GitHub
  * käykää hyväksymässä kutsut Superlibrarian-ryhmään, kutsu pitäisi olla sähköpostissa.
  * jos ette ole vielä rekisteröityneet, teettehän sen piakkoin, jotta pääsette muokkaamaan ohjeita ja tekemään tikettejä, kun sen aika tulee.

*Lumme*
* Viddla ei tunnu toimivan hyvin vieläkään, mutta ongelma lienee Viddlalla, selvitellään.
* Eräpäivämuistutusten lähettäjä- ja vastaanottajakenttien sovitus ikkunakuoreen korjattu. Koodissa oli liian pieni marginaali.

*OUTI*
* Yhteyden katketessa on tullut tapauksia, että varauksen lainaaminen on epäonnistunut automaatilla sekä virkailijalla. Varauksen poistaminen on auttanut ongelmaan. Yhteyden katkeamisessa tapahtuu jotain, joka muuttaa asiakkaan varauksen löytymään yhtäaikaa sekä aktiivisten että vanhojen varausten taulusta tietokannassa.
* Ruukin pääkirjastolla asiakaspalvelutiskin koneessa oli ongelmia kuittien tulostuksessa. Koneessa oli Firefoxin versio 91.5.0 esr. Ongelmaan auttoi, kun koneeseen päivitettiin Firefoxin vanhempi versio.
* Oulun koulukirjaston ongelmat itsepalvelulainauksessa jatkuivat korjauksista (poistettiin kuitintulostus-valikko ja muokattiin kielivalintoja), joten Koha-Suomi teki päätöksen luopua varmenteen käytöstä itsepalvelulainauksen osalta. Muutos tehtiin järjestelmään viime huoltokatkon ohessa 9.2.2022. Kielivalinnat oli jo aiemmin korjattu, mutta edelleen tuottivat ongelmia koulukirjastoissa, joten se korjattiin uudelleen. 
* Virkailija kummasteli, kun ei saanut tuloksia käyttäessään hipsuja tiedonhaussa esim. ti:"luontaisterveys". Hän sai tuloksen vasta toisella täsmälleen samanlaisella hakukerralla. Häntä ohjeistettiin käyttämään sulkuja hipsujen sijaan ja se tuntuisi antavan tuloksia. Hipsu-ongelmaa on havaittu muuallakin.
* Teimme uuden tilan "Muuttolaatikossa" (15) Oulun pääkirjaston remonttimuuttoa varten. Oulussa on  tehty useita tikettejä tila- ja sijaintimuutoksia varten ja niiden muodostaminen oikein on teettänyt töitä, jotta ajot menevät oikein.
* Laskutusliitännäiseen tehtiin vielä asetussäätöjä. Oli jäänyt määrittelemättä kolmas myöhästymissääntö, jolloin kaikkia laskutettuja ei näkynyt liitännäisessä vaikka ne näkyivät laskutuslistalla.
* OUTIssa laitettiin pois päältä TrackLastPatronActivity-järjestelmäasetuksen (päivittää asiakkaan lastseen-arvon). Nyt seurataan, onko sillä vaikutusta katkoksiin, joita on ollut paljon varsinkin OUTIssa.

*Siilinjärvi*
* Ei mitään poikkeavaa.

*Vaara*
* Viime viikolla tiistai-iltana lakkasi hyllyvarausraportti toimimasta. Ongelman syynä oli parissa nimeketietueessa ollut "haamunide" eli olematon nide, joka oli käytännössä tyhjä rivi nidevalikossa. Toiseen nimekkeeseen oli tullut varaus, jonka takia hyllyvarausraportti lakkasi toimimasta. Haamuniteet poistamalla ongelma korjaantui.
* Pahasti jälkijunassa pyydettiin vihdoin selaimen päivitys Vaara-kirjastojen työkoneille. Meita ilmoitti, että Software Centerissä on asennettavissa Firefox 91.5.1 ESR-versio. Erilaisia ongelmia eri kirjastoissa parhaillaan: jotku eivät pysty asentamaan ollenkaan versiota, kuittitulostus tökkii jne. 

*Lappi*
* Tietokannassa niteetön tietue, jolla 451 000 osakohdetta. Selvittelyn jälkeen huomattiin, että tietueelta puuttuu 001-kentästä kontrollinumero kokonaan. Sen kun lisäsi, osakohteet poistuivat ja tietueen uskalsi poistaa.
* pp.inet.fi sähköpostit lukevat kohan viestien linkit väärin. Pyydetty asiakkaita olemaan yhteydessä sähköpostipalvelun tarjoajaan. 
* Muutoin normiylläpitoa.

*Vaski*
* OKM musiikki ja muut äänitteet rajausta ihmetelty
* Konversio yksikön poistoa suunniteltu
* Laskutustyökalu käyttökunnossa, aloitetaan käyttökoulutukset ja -testaukset

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-7-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 6 muistio

Aika: 8.2.2022 klo 9.15
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Reetta Pihlaja (Siilinjärvi, klo 10 asti), Tuomas Kunttu, Christer Skog (Kyyti), Anneli Österman, Pirkko-Liisa Lauhikari ja Piia Semenoff (OUTI), Kati Sillgren (Helle), Leena Kinnunen ja Pia Kusmin (Lappi), Mikko Liimatainen (Vaski)


"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-6-muistio

*Yhteiset*
* onko noudettavien varausten tuplakuljetustiloja vielä havaittu?
* PostiMessaging ilmoittanut huoltokatkoista 12.2.2022 ja 19.2.2022
  * Tarkistelkaa huoltokatkojen jälkeen (ne, joilla on PostiMessaging käytössä), onko paljon epäonnistuneita paperikirjeitä. Jos niitä on vähän, käykää kliksuttamassa ne asiakkaiden tiedoissa "Lähetä uudelleen" -linkistä takaisin jonoon. Jos niitä on vähän, tehkää tukipyyntö Redmineen.
  * Lapilla valmiina raportti, jolla voi tutkia, onko epäonnistuneita paperikirjeitä
<pre>
SELECT message_id, cardnumber, message_queue.borrowernumber, 
borrowers.email
, borrowers.smsalertnumber, status, delivery_note, subject, content, letter_code, message_transport_type, time_queued
FROM message_queue
LEFT JOIN borrowers ON borrowers.borrowernumber = message_queue.borrowernumber
WHERE message_transport_type = 'print' 
AND (status = 'failed' OR status = 'pending') 
AND time_queued >= NOW() - INTERVAL '1' DAY 
ORDER BY time_queued DESC
</pre>
* Tätin käyttäjätunnusten muutosten lokitiedosto?
  * OUTIssa kerätään erilliseen tiedostoon kaikki käyttäjätunnuksiin tehdyt käyttäjäoikeuksien muutokset. Tämä käytäntö on otettu käyttöön muutama vuosi sitten sen jälkeen, kun Oulun sisäinen/ulkoinen tarkastus suositteli sitä. 
  * Pohdittiin, olisiko se tarpeen myös Tätissä ja tultiin siihen tulokseen, että ei ole tarvetta. OUTIlaiset merkitsevät omaan tiedostoon muutokset myös Täti-tunnuksiin.
* Huoltoikkuna 9.2.2022 klo 7-9
* Kohan kaatumiset loppuviikosta viikolla 5 johtuivat MariaDB:n tmp:n täyttymisestä. Ongelmaa selvitelty/korjailtu ja tilannetta seuraillaan.
* Tätissä säädetty Nalkutinta niin, ettei se nalkuta kentästä 579
* Matrix
  * vaihda näyttönimeksi oma nimi + kimppa
  * ota talteen security key, jos Element sitä kehottaa
  * ei kannata tyhjentää selaimen välimuistia ennen kuin olet tehnyt poikkeuksen Elementille/Matrixille, koska se tallentaa salausavaimen selaimen tietoihin
* Laskutustyökalua päivitetty
  * Lisätty Jäljenne-nappi, jolla saa tulostettua myös PDF-laskutusta käytettäessä jälkikäteen jäljenteen. Nappulan painaminen ei aiheuta laskutusmerkintöjä.
  * Korjattiin virhe, jonka vuoksi asiakkaille muodostui ekirjelasku, vaikka niteiden hinnat olivat 0 € eikä niteiden kohdalla ollut rastia.


*Vaara*
* Ei mitään erityistä. Päivillä tekeillä paikallislehden toimittajaa varten raportti viime vuoden lainatuimmista parin kirjaston osalta ja tulosta pitäisi verrata koko Vaaran lainatuimpiin. Apuja pitää kysellä, kun valmista raporttia ei ole eikä itse osaa.

*Siilinjärvi*
* Ei erityistä, yritetään ottaa Matrix haltuun.

*Kyyti*
* Laskutustyökalun ryhmäasetuksista ei poistu laskutusryhmä, vaikka ryhmän poistaa ylläpidon kirjastot ja ryhmät -osiosta. Lähinnä kauneusvirhe, eipä juuri haittaaaan.
* Kyytissä laskutustyökalun laskuttavana kirjastona on omistajakirjasto. Kuitenkin asiakkaalla näkyy laskutustyökalussa myös muiden kuntien kirjastojen niteitä. Niitä pitää sitten ruksia yksitellen pois. Laskuttajat toivoivat, että tällä asetuksella näkyisi vain oman kunnan niteet, kuten kuulemma ennenkin. Nopeutuisi laskutushomma.

*Helle*
* Hankintaportaalin käyttöönottotoimia.
* Hangossa otettu käyttöön omatoimi lehtilukusaliin.
* Siirtokokoelman kellumaton nide ei enää mene kuljetustilaan, vaikka pitäisi. Tiketti #5248

*OUTI*
* Laskutusliitännäinen
  * Laskutukseen lähti myös nolla-hintaisia laskutettavia, kyseessä oli laskutusplugarin virhe ja se on nyt korjattu.
  * Lisätty Jäljennös-nappi
* Viivakoodigeneraattori
  * viivakoodittomille lisättiin hank-alkuisia viivakoodeja, jotta asiakkaat näkevät varauksensa automaateilla.
* Kempeleen liikuntalainaamo
  * Kempeleeseen tulossa Liikuntalainaamo, jonka aineisto tallennetaan ja lainataan OUTI-Kohassa. Lainaamo otetaan käyttöön maaliskuun alussa. Asian hoitaminen on vielä kesken Kempeleen kirjaston kanssa.

*Lappi*
* Rovaniemen remontin suunnittelua. Rovaniemen aineisto alkaa myös kellumaan muille kirjastoille 14.4. alkaen.
* Leena jää opintovapaalle. Palaa toukokuun puolessa välissä.
* Normiylläpitoa.

*Vaski*
* OKM raportin tieto/kauno jaottelua ihmetelty. Kohassa joattelu tietueen mukaan, kun Aurorassa ollut niteen mukaan, joten tilastot ovat muuttuneet tuhansilla.
* Hankintojen alv jatkossa 0%. Ohjeistus kaipaa täsmennystä tämän osalta.
* Finnaan varaustunniste näkyviin varauksen tietoihin tai varaukset sivulle.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-6-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 5 muistio

Aika: 1.2.2022 klo 9.15
Läsnä: Päivi Knuutinen ja Auli Rantasalo (Vaara), Mikko Liimatainen (Vaski), Katja Valjakka, Tiina Pietikäinen, Timo Pesonen (Lumme), Anneli Österman, Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Reetta Pihlaja (Siilinjärvi), Christer Skog (Kyyti), Kati Sillgren (Helle)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-5-muistio

*Yhteiset*

* "GitHubin":https://github.com ja pikaviestiohjelman käyttöönotto
  * GitHubilla tullaan korvaamaan Redmine, mitä varten pääkäyttäjät tarvitset tunnukset GitHubiin.
  * Pikaviestipalvelu Matrix korvaa ircin: "Matrix, jota voi käyttää useammalla eri clientilla":https://matrix.org/clients/ - testattu Element.io ja Cinny (Lisätietoja Matrixista Wikipediassa https://fi.wikipedia.org/wiki/Matrix_(protokolla))
  * Matrixiin voi kirjautua GitHub-tunnuksilla: 
## kaikki pääkäyttäjät rekisteröityy ensin GitHubiin 
## ja sen jälkeen matrixiin esim. https://app.element.io -osoitteessa. Valitse kirjautumiskenttien alta ensin GitHubin logo.
!{width:40%}kirjautuminen.png!
## ilmoita sen jälkeen Annelille matrixin tunnus, niin saat kutsun Koha-Suomen "huoneeseen".
  * Elementillä on myös mobiiliappi, jonka voi asentaa halutessan.
  * GitHubin koulutus tulossa vähän myöhemmin.

* Seuraava huoltoikkuna 9.2.2022. Tulossa pieni katko.
* Luettelointi-termin muuttaminen kuvailu-termiksi Kohassa.
  * Kuvailu-termiä käytetään nykyään, joten siirrytään käyttämään sitä Kohassa ja ohjeissa. Kuvailijoilta kysytty myös mielipidettä ja muutos sai kannatusta.
* Koha-Suomi-tiimi-sivulla olevat pääkäyttäjien yhteystiedot.
  * siirretään Koha-Suomen sivuille, kun Redminestä luovutaan.
  * mietitään loma-ajoille toinen sijainti julkisen nettisivun sijaan (Redminekin julkinen, mutta ei niin helposti löydettävissä).
* Hyllyvarausraportin tietokantakyselyt ajetaan nyt tietokantaslavella. / Kodo
  * Konesalissa on kaksi tietokantapalvelinta, master ja slave. Kaikki master-palvelimen tapahtumat toistetaan (replikoidaan) slavelle, jolloin palvelimet ovat käytännössä koko ajan identtiset keskenään dataa myöten.
  * Homman ajatus on, että slave ottaa ohjat jos masterille tapahtuu jotain ikävää, jolloin käyttökatko jää hyvin lyhyeksi (enintään muutamia minuutteja).
  * Käyttökuormaa on suorituskyvyn vuoksi kuitenkin järkevää pyrkiä normaalioloissakin tasaamaan näiden kahden palvelimen välillä. Hyllyvarausraportin kyselyjen siirtäminen slaven hoidettavaksi on ensimmäinen askel tähän suuntaan.
  * Tulevaisuudessa kaikki Kohan raportit ajetaan slavella, jolloin hyvin raskaidenkaan kyselyjen ajamisella ei ole vaikutusta Kohan muuhun käyttöön.
  * Muutos oli testattavana Vaara-kirjastoissa viikolla 4 ja korjatun skandiongelman lisäksi muita ongelmia ei havaittu.
  * Ajotavan muutos hyllyvarausraporttien osalta on tehty kaikille kimpoille 31.1.
* Tammikuun tilastot okm-raportilla ovat virheelliset. Tilastot ajetaan uudelleen ti-ke-välisenä yönä.

*Vaara*
* Keskiviikkona siirrettiin Vaaran hyllyvarauslistan ajo slavelle. Ensin oli ääkkösongelma, mutta se saatiin pian korjattua. Palautetta ei ole tullut, joten toimii kunnolla.
* muuten normaalia ylläpitoa

*Vaski*
* Rusko kokoelmien kellutus edelleen suunnittelussa
* Salon palautusluukun ongelma korjattu
* Soittimien varaamisen parantaminen

*Kyyti*
* Ei lisäyksiä pöytäkirjaan

*Lumme*
* Muutamalle varaukselle tullut 3 pv noutoaika Varkaudessa. Tutkitaan varauslokia rapsalla.
* L14 nidetyypin lautapeleille tulee 28 vrk laina-aika. Testataan vielä laina- ja maksuaikataulukon testikalulla. 

*OUTI*
* Uuden laskutusliitännäisen koulutus pidetty. Koulutus on tallennettu, mutta siihen on tullut harmillinen katkos. Koulutuksessa toivottiin takaajan osoitetta näkyville laskutustietoihin ja laskutettavan aineiston minimisummaksi 0 €. Johanna on tehnyt muutokset OUTIn testille, jossa ne ensin testataan.
* Kempeleen kirjastolle ei saatu tuotantoon tallennettua laskutusliitännäisen ryhmäasetuksia, tallennuksessa tuli aina ilmoitus ”Tapahtui virhe”. Johanna tutkii ongelmaa.
* Yhdellä työntekijällä Koha-tunnus lukkiutuu mystisesti, kun hän vaihtaa koneelta toiselle. Virheellisten kirjautumiskertojen määrä on ylittynyt.
* Siikajoen kirjastoissa on ollut samaa kuitin tulostusongelmaa kuin Kyytissä, tiketit https://tiketti.koha-suomi.fi/issues/3604 ja https://tiketti.koha-suomi.fi/issues/5231. Kirjastoissa on käytössä Firefoxin selainversio ESR 91.5.0. Ehdotettu, että auttaisiko ongelmaan, jos palauttaisivat testimielessä jollekin koneelle käyttöön vanhemman selainversion. Voisi ehdottaa myös välimuistin, evästeiden yms. tyhjennystä ja Firefoxin asetusten nollaamista.

*Siilinjärvi*
* Ei (taaskaan) mainittavaa.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-5-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

----

## Viikko 4 muistio

Aika: 25.1.2022 klo 9.15
Läsnä: Leena Kinnunen, Pia Kusmin (Lappi), Anneli Österman, Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Reetta Pihlaja (Siilinjärvi), Päivi Knuutinen ja Auli Rantasalo (Vaara), Tuomas Kunttu ja Christer Skog (Kyyti), Kati Sillgren (Helle), Mikko Liimatainen (Vaski)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-4-muistio

*Yhteiset*
* Laskutustyökalu päivitetty kaikille kimpoille tuotantoon.
* "Kohan ohje suomeksi":https://koha-suomi.fi/dokumentaatio/asiakkaat/ - uusi koti Kohan suomen verkkosivuilla, johon tehdään versionpäivitykseen liittyvät muutokset ohjeisiin.
* Kohan ohje suomeksi -wikin päivitysvastuut:
  * Asiakkaat - Piia Semenoff : kesken, kohdassa 1.6.
  * Lainaus - Pirkko-Liisa Lauhikari alkuosa, päivitetty, Lumpeet loppuosa 2.8 loppuun: päivitetty / Siirretty 20.12. Varaukset osio Varaukset-nimiselle uudelle välilehdelle.
  * Kuvailu - Päivi Knuutinen : päivitetty
  * Kausijulkaisut - Vaski : päivitetty
  * Hankinta - Anneli Österman : Valmis kohtaa 7.7 lukuunottamatta. Sitä ei voinut päivittää, koska sivu ei avaudu Kohassa.
  * Listat ja kori - Lappi : päivitetty
  * Raportit - Anneli Österman : päivitetty
  * Tiedonhaku - Kyyti
  * Kuittitulostuksen asetukset - Pirkko-Liisa Lauhikari, päivitetty
  * Työkalut
*  * 10.1-10.3 Reetta Pihlaja : päivitetty 10, 10.1, 10.2, 10.3 ja korjattu niiden numerointi 12-alkuisiksi.
*  * 10.4 Lähetä laskuja -toimintoa ei siirretä
*  * 10.5 -10.10 Lappi : päivitetty luvut 10.5.-10.10. 
*  * 10.11 Kati Sillgren : jonkun aiemmin tekemä ohje pätee myös uudessa versiossa. En tehnyt muutoksia.
*  * 10.12 Anneli Österman : päivitetty
*  * 10.13 Kati Sillgren : jonkun aiemmin tekemä ohje pätee myös uudessa versiossa. Yhden Koha-näyttökuvan vaihdolle oli tarve. Vaihdoin.
*  * 10.14 Piia Semenoff : päivitetty
*  * 12.15-12.18 Tuomas Kunttu, päivitetty 12.15, 12.16, 12.17.1., 12.17.2, 12.17.3, 12.17.4 ja 12.18. Eli kaikki tehty.



*Lappi*
* Tukipostiin tulee viestejä virheellisistä EditX-sanomista, mutta viestissä ei ole tietoa virheestä, eikä virheitä ole myöskään Kohan EditX-sanomissa
* Huollettava, muu kuin lapsi - asiakastyypiltä puuttui takaajakenttä. Asiakastiedoissa pitää olla valittuna oikea asiakastyyppiryhmä. 
* Vanhentuneita maksuja poistettu. Osalla asiakkaista antaa erroria, tiketti #4941
* Kalenteriin merkitty kuluvan vuoden pyhät sekä remonteista aiheutuvia sulkuja
* Tornion remontti tulossa, kirjasto sulkeutuu 31.1.
* Rovaniemen remontti alkamassa toukokuussa, työlistaa rakennetaan. 
* Leena opintovapaalla 11.2. - 15.5., ei sijaista pääkäyttäjiin. Pia asiantuntijoissa varajäsen. 

*OUTI*
* Uuden laskutustyökalu-liitännäisen koulutus 26.1. OUTIn laskuttajille. 
* Oulun pääkirjasto menee vuoden 2023 alusta remonttiin. Remonttimuuttoon liittyviä kokoelmasiirtoja tehty järjestelmässä muihin sijoituskirjastoihin ja määritelty siirron ajaksi niteet ”Ei lainattavissa” -tilaan. Unohtui, ettei saa muuttaa varattujen niteiden tilaa, jotka olivat kuljetustilassa tai odottivat noutoa.
* Kun Kohan itsepalvelulainauksessa vaihtaa kielen toiseen, tulee ilmoitus "not found". Tiketti: https://tiketti.koha-suomi.fi/issues/5236 

*Siilinjärvi*
* Ei mainittavaa.

*Vaara*
* Ei erityistä, laskutusta testataan huomenna.

*Kyyti*
* Laskutustyökalun esittelyä kimpan laskuttajille tänään 25.1.
* Nide ottanu kiinni kahteen varaukseen. Ensimmäisellä palautuksella nide otti varaukseen kiinni, mutta kuittia ei tulostunut. Toisella palautuksella nide otti jo seuraavaan varaukseen kiinni ja kuitti tulostui. Tämä on tapahtunut kahdesti viikon sisällä eri kirjastoissa. Tiketti 5231. Yksi vaihtoehto on, että vika on selaimessa. Kannattaa ehkä tehdä selaimessa toimenpiteitä: tehdä Firefox profiili uudelleen, nollata tulostusasetukset ja ponnahdusikkuna-asetukset.

*Helle*
* Auktorisoituihin arvoihin (MANUAL_INV) lisättyjen maksutyyppien Kuvaus-kentän arvo ilmestyy nyt automaattisesti asiakastiedon Lisää maksu -toiminnon Summa-kenttään. Itse lisättyjen maksutyyppien Kuvaus-kentät muutettu arvottomiksi.
* Nidehaussa Kokoelmakoodi-arvoon liitetty ei ole -hakuehto toimii erikoisesti. Vastaavaa erikoisuutta havaittu myös sql-raportin not like ccode -hakuehdolla haettaessa. Tiketti #5230
* Webkake-yhteys toimii nyt.

*Vaski*
* Näyttelyssä erikoistila estää lainaamisen automaatilla. Mietitään toista tapaa näyttelyissä olevien niteiden tunnistamiseen.
* Erääntyneille varauksille toivotaan asetettavaksi jotain erikoistilaa ajastetun poiston yhteydessä, jotta niteet eivät näy vapaana verkkokirjastossa.
* Ruskon kirjasto suljettu, aineiston kellutusta muihin kirjastoihin suunnitellaan.
* SQL-raportteihin työn alla kattava tyhjien kenttien hyödyntäminen joustavampien raporttien tekemistä varten.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-4-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 3 muistio

Aika: 18.1.2022 klo 9.15
Läsnä: Katja Valjakka, Timo Pesonen ja Heli Auranen (Lumme), Reetta Pihlaja (Siilinjärvi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Tuomas Kunttu, Christer Skog (Kyyti), Leena Kinnunen ja Pia Kusmin (Lappi), Kati Sillgren (Helle), Anneli Österman, Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Mikko Liimatainen (Vaski)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehittäjät_-_vuosi_2022#Viikko-3-muistio

*Yhteiset*:
* Smartbox, onko kimpoissa ollut kiinnostusta ottaa käyttöön? Koha-Suomelta kysytty integraatiota.
  * Lapissa kyselty kauan sitten. Lumpeissa pohdittu asiaa.
* Tietokannan taulujen siivoukset
  * Seuraavat siivoukset on tehty kaikkiin kimppoihin: 
# action_logs-taulu jaettu vuositauluihin, aktiiviseen tauluun jäi 3 vuotta. Vanhempia tietoja pitää tutkia tarvittaessa SQL-kyselyillä.
# statistics-taulu vuositauluihin,
# edifact_messages-taulusta yli vuoden vanhat poistettu. Taulu sisältää EDIFACT-sanomat-sivulla näkyvät sanomat.
# message_queue-taulusta (asiakkaille lähetetyt viesti) yli 3 vuotta vanhemmat poistettu
# search_history-taulusta eli hakuhistoriaa säilytetään 1 kk (ja kuluva) siivotaan kuun alussa. 
# Kirjautumiset + zebraqueue tyhjentyy joka yö

* indeksoinnit
  * kaikille muille paitsi Lapille on tehty uudelleenindeksointi, joka korjaa seuraavat 
# Vuosi-haku (copydate) hakee nyt myös uudempaa aineistoa. Kyseisen haun "mäppäyksiin" lisättiin, että julkaisuvuosi haetaan entisen 260c-kentän lisäksi myös 264c-kentästä ja 008_/7-10.
# Asiasana/aihehakuun (subject/su) tarkennettiin 651- ja 611-kenttien määrityksiä. Niistä oli ennen mäpätty kaikki osakentät, minkä vuoksi esim. fasetteihin saattoi tulla linkkejä finto-sanastoon. Nyt mukana on kyseisistä kentistä vain alla olevat osakentät: 611 -> 611a, n, c, d, e ja t sekä 651 -> 651a

*Lumme*
* AutomaticItemReturn- asetus otettu pois päältä, eli teokset eivät mene enää automaateilla kuljetustilaan. Virkailijaliittymässä kysyy laitetaanko kuljetukseen.

*Siilinjärvi*
* To 13.1. ehkä n. 45 min vakava häiriö lainauksessa ja palautuksessa, johtui ilmeisesti Kohassa tehdyistä Elastic search -säädöistä. Sattui onneksi iltapäivän hiljaisena tuntina.
* OKM-tilastoja tutkailtu, vaikuttaisivat meillä tänä vuonna olevan kunnossa ja järkeviä lukuja. Hyvä! 

*Vaara*
* Tekstiviestien perille menemättömien viestien ilmoitusta ei tule edelleenkään. Asian selvittely vielä kesken, ilmeisesti stoppaavat johonkin palomuuriin.
* Mikroväylän automaattien uuden ohjelman toiminnasta tehty ilmoituksia, mm. maksuista johtuva lainauskielto ei toimi kunnolla, vaan päästää asiakkaan "lainaamaan" ensimmäisen niteen ennen kuin huomauttaa että lainausoikeutta ei ole. Asiakas ei välttämättä huomaa viestiä vaan luulee lainauksen onnistuneen.

*Kyyti*
* Mikroväylän ServManager takunnut sip2 over https ohjelmistopäivityksen jälkeen. Asian selvittely vielä kesken. Mikroväylän koodari tutkii asiaa.
* Keskusteltiin mahdollisuudesta saada croni, joka poistaa kuljetustilan noudettavana olevista varauksista #5222
* Laskutustyökalua on testailtu. Sen kommentit ovat tiketissä #5159

*Lappi*
* Tornion remonttiin liittyviä muutostöitä kohassa.
* Laskutuksen säätöä. Hyvä, että käytiin yhdessä läpi!
* Kotipalvelu-asiakkaiden lainahistorian käyttöä selvitellään Annelin kanssa.

*OUTI*
* Ceeposin verkkomaksuportaalin alusta on vaihtunut Drupalista Wordpressiin. Vaihdos sujui ongelmitta.
* Itsepalvelulainauksesta on otettu kuittitulostus pois, sillä kuittitulostuksen valitseminen aiheutti ohjelmaan "Not found"-virheilmoituksen eikä ohjelma toennut virhetilanteesta itsekseen. Itsepalvelulainausta käyttävissä kouluissa ei ole kuittitulostimia, joten tulostuksen poistaminen oli sen vuoksi mahdollista ja saimme ongelman poistettua helposti.
* Eräpäiväilmoitukset eivät lähteneet 12.1., sillä sen aamuinen huoltokatko kesti klo 8.45 saakka ja eräpäiväilmoitukset oli ajastettu muodostumaan klo 8.40. Ajastusta muutettiin alkamaan myöhemmin, jotta tilanne ei toistuisi.
* 18.1. otettiin Oulussa käyttöön uusi Webkake-kaukolainatilauslomake. Nyt lomaketta pääsee käyttämään vain kirjautumalla kirjastokorttitunnuksella ja PIN-koodilla. Lomakkeen yhteyteen on lisätty myös kaukolainojen tarkistus- ja uusinta, joten sekin toiminto vaatii nyt kirjautumisen.

*Helle*
* Hellessä toivottu Hyllyvaraukset-raportin automaattisesti näytettävän hakutuloksen arvoksi Kaikki nykyisen arvon 20 tilalle. Emmi testannut ja huomannut, että kimppakohtaisesti muutosta ei saa toimimaan oikein. Muilta kimpoilta kannatus Kaikki-muutokselle. Tiketti #5065
* OKM-raportin hakutuloksen ladattuun Excel-taulukkoon toivottu muutosta sarakejärjestykseen. Tuomas vinkkasi palaverissa tavan, jolla sarakejärjestyksen voi muuttaa itse: taulukon tietojen kopiointi ja liittäminen uuteen tyhjään Excel-taulukkoon käyttäen tapaa Liitä määräten - Transponoi.

*Vaski*
* Kellutuksessa siirrytään käyttämään siirto-toimintoa
* OKM ja lainaus/palautus-raporteissa eroja
* Käyttöönottoprojektin auki olevien tikettien sulkeminen

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-3-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 2 muistio

Aika: 11.1.2022 klo 9.15
Läsnä: Christer Skog (Kyyti), Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen ja Auli Rantasalo (Vaara), Tiina Pietikäinen, Timo Pesonen, Katja Valjakka, Heli Auranen (Lumme), Susanna Sandell (Vaski), Reetta Pihlaja (Siilinjärvi), Leena Kinnunen ja Pia Kusmin (Lappi)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehittäjät_-_vuosi_2022#Viikko-2-muistio

*Yhteiset*
* Huoltoikkuna ke 12.1.2022 klo 7-9. Kohan käyttö estetään huoltokatko-ilmoituksella siksi aikaa, kun se on tarpeen.
  * muistutelkaa henkilökuntaa ja asiakkaita katkoksesta.
* OKM-tilastot ja celia
  * OKM-tilastot otetaan OKM-tilastot-raportilla. 
  * Celia-tiedot ajetaan ma-ti-yönä. Tarviiko kuukausitilastoja ajaa uudelleen Celioiden vuoksi? Päätettiin, että ei ajeta uudelleen.

*OUTI*
  * Asiakas ei pystynyt poistamaan s-postiosoitettaan itse finnasta. Osoite piti poistaa ensin Kohasta, jolloin se poistui myös finnasta. Toimiiko muissa kimpoissa samalla tavalla?
  * Asiakas oli maksanut kirjastomaksut kahteen kertaan finnan verkkomaksupalvelussa, koska ensimmäinen maksu ei ollut kirjautunut Kohaan. Ensimmäisen maksukerran yhteydessä asiakas oli ensin uusinut myöhässä olleet lainat ja muutaman tunnin päästä käynyt maksamassa maksut. Finnan hallintaliittymään ei ollut tullut tietoa epäonnistuneesta maksukuittauksesta.
  * Raahen uudessa palautusautomaatissa oli sama ongelma kuin esim. Kotkassa ja Lieksassa on ollut eli Koha ei tulostanut palautusautomaattipalautuksen jälkeen varauksen kuljetuskuittia. Raahen ongelmaan auttoi sama kuin Kotkassa eli automaatin toimittaja tyhjensi automaatin määrityksistä AP-kentän.
  * Ollaan säädetty uuden laskutustyökalu-liitännäisen asetuksia. Ohjelman dokumentaatioon tulee vielä päivityksiä, koska ohjelmaan on tullut lisäyksiä.
https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Laskutusty%C3%B6kalu-liit%C3%A4nn%C3%A4inen  

*Vaara*
  * Tilastointia vuodelta 2021 aloiteltu.
  * Laskutustoimintoa kaivataan, on pitkä aika kun on päästy viimeksi laskuttamaan.
  * Pääkirjaston kassa ja Koha eivät keskustele keskenään, joku yhteysongelma.

*Lumme*
* Laskutuksen toimivuutta odotellaan
* Finnan Paytrial säädetty

*Vaski*
* Finnassa oletusnoutopaikka muuttuu välillä kotikirjastoksi joillakin asiakkailla. Ilmeni, että jokin triggeröi oletusnoutopaikkojen muuttumisen kotikirjastoiksi aika ajoin.

*Helle*
* Verkkomaksaminen otettu käyttöön pe 7.1.2022.
* Varausta lainatessa tullut Vahvista lainaus -ilmoitus ilman vahvistustarpeen syytä. Anneli kertoi palaverissa, että ko. ilmoitus tulee lainatessa kuljetustilaista varattua nidettä.
* Emmi korjannut Failed-tilaiset EditX-tilaukset.

*Siilinjärvi*
* Ei erityistä
* Meiltä laitettu ehdotus Finnaan korttipeli-aineistotyypistä

*Kyyti*
* ICT-Kymin kohapalvelin ajettu alas 5.1.2022. 

*Lappi*
* Myöhästymisilmoitusten määrittelyjen tarkastelua. Onko muilla tehty oletus-pohjalla vai kirjastokohtaisesti?
* Laskutustyökalun määrittelyjä.
* Kemin kassa ei keskustele kohan kanssa vieläkään.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-2-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 1 muistio

Aika: 4.1.2022 klo 9.15
Läsnä: Anneli Österman ja Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Leena Kinnunen ja Pia Kusmin (Lappi), Susanna Sandell (Vaski), Kati Sillgren (Helle)Katja Valjakka, Tiina Pietikäinen, Timo Pesonen (Lumme)

"Kehittäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehittäjät_-_vuosi_2022#Viikko-1-muistio

*Yhteiset*
* Perjantain katkos
* "Videopeli ja lautapeli -aineistotyypit ajettu tietueille":https://tiketti.koha-suomi.fi/issues/5082
  * KONSOLIP-aineistotyypin voi poistaa MTYPE-arvosta ja OKM-järjestelmäasetuksesta.
* Huoltoikkuna 12.1.2022 - tulossa lyhyt katko kaikissa kimpoissa.
* hakuhistoria nollattu kaikilta kaikissa kimpoissa paitsi Vaski ja Kyyti
* OKM-tilastot
  * poistoihin ei lasketa enää mukaan tilattu-tilaisia niteitä
  * videopeli ja lautapeli mukana
  * puuttuu vielä Celia-tilastot. Koodimuutos viedään tuotantoihin ja tilastot ajetaan uudelleen.
* EDItX ja vaihtoehtoiset hyllypaikat
* Community-versiossa Siilinjärven tietokanta. Tunnukset tuodaan vanhemmasta community-version tietokannasta.
* Linkki raportointityökaluun poistettu Raportit-sivulta.


*OUTI*

* Epäonnistuneiden tekstiviestilähetysten raportilla epäilyttävän vähän sisältöä. Kysellään Link Mobilityltä, lähettävätkö he edelleen kuittauksia. Kohan puolesta kaikki pitäisi olla kunnossa.
* Lyhytlainalle tullut automaatilla lainatessa eräpäiväksi lainauspäivä. Sama tapahtunut aiemminkin, kirjattu tikettiin https://tiketti.koha-suomi.fi/issues/4018.
* Asiakas ei ollut pystynyt tekemään kausijulkaisuun varausta Finnassa, koska niteellä oli kirjan nidetyyppi (28 vrk). Kun nidetyypin vaihtoi lehteen, varauksen teko onnistui. 
* Uuden kirjastoauton vuoksi kirjastoautojen Koha-lyhenteet muutetaan geneerisimmiksi.
* Tehty uuden laskutusliitännäisen konfigurointia ja testailua.
* OUTIn vanhat palvelimet on ilmoitettu Oulun Digille, että ne saa ajaa alas.
* Finnasta voi piilottaa tietueen laittamalla luettelointitietoihin 942n-kenttään arvon y.

*Vaara*
* Vuodenvaihteessa oli tarkoitus ajaa lainauskielto asiakkaille, joilla on maksamattomia maksuja yli 1 euron. Ajo oli jostain syystä jäänyt ajamatta ja se tehdään ensi yönä.
* Juuan ja Valtimon kirjastojen tunnukset pitäisi vaihtaa, koska ne vaikuttavat mm. kirjastohierarkiaan Finnassa. Tämä on iso operaatio, joten odotetaan ensin Outissa tapahtuvaa vastaavaa muutosta ja sen onnistumista.

*Lappi*
* Tiedonhaussa hipsujen käyttö hakulauseessa ja Palaa hakutuloksiin -linkin käyttö aiheuttaa virheilmoituksen.
* Varausjonojen korjauksia mm. kuljetustilojen ja inhimillisten kämmien vuoksi. 

*Vaski*
* Hakuhistorian nollaus ok.
* Huolena, että joku poistaa esim viime vuoden budjetin vahingossa. Selkeämpi varoitus voisi estää vahingot.

*Helle*
* Odottamaton käyttökatko 28.12.2021 n. klo 11.59-12.09.
* 15-vuotta täyttäneen lapsi-asiakkaan muutosautomatiikka ollut toimimaton 30.11.2021 alkaen. Lari korjasi tilanteen #5197.
* Lari poistanut toimimattoman Raportointi-toiminnon linkin #5192.
* Helle-toive: lapsi-asiakkaan kirjeenä lähetettävä 2. myöhästymisilmoitus automaattisesti lapsen huoltajalle.


*Lumme*
* Joillain virkailijoilla tökkii edelleen lehtien vastaanotto. Kodo ehdottanut uusia käyttäjätunnuksia. EDIT myöhemmin: tämä korjasi asian:) Ei enää proxy erroria!
* asiakkaille ei enää tule lainauskieltoa vuodenvaihteessa maksamattomista maksuista (jos alle 10 e) : Lari poistanut myös vanhat, aiemmissa vuodenvaihteissa muodostuneet lainakiellot.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-1-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022

---
